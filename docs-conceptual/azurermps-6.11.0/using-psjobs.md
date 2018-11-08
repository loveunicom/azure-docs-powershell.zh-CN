---
title: 使用 PowerShell 作业并行运行 cmdlet
description: 如何使用 -AsJob 参数并行运行 cmdlet。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: 85e4612146c07b963ca51a7203ea7782d058b93d
ms.sourcegitcommit: 1f699b72bf544d92459da9d888cc0091f9415b65
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/06/2018
ms.locfileid: "50972020"
---
# <a name="running-cmdlets-in-parallel-using-powershell-jobs"></a><span data-ttu-id="2a3be-103">使用 PowerShell 作业并行运行 cmdlet</span><span class="sxs-lookup"><span data-stu-id="2a3be-103">Running cmdlets in parallel using PowerShell jobs</span></span>

<span data-ttu-id="2a3be-104">PowerShell 支持使用 [PowerShell 作业](/powershell/module/microsoft.powershell.core/about/about_jobs)执行异步操作。</span><span class="sxs-lookup"><span data-stu-id="2a3be-104">PowerShell supports asynchronous action with [PowerShell Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span></span>
<span data-ttu-id="2a3be-105">Azure PowerShell 严重依赖于向 Azure 发出和等待网络调用。</span><span class="sxs-lookup"><span data-stu-id="2a3be-105">Azure PowerShell is heavily dependent on making, and waiting for, network calls to Azure.</span></span> <span data-ttu-id="2a3be-106">你可能经常需要发出非阻塞调用。</span><span class="sxs-lookup"><span data-stu-id="2a3be-106">You may often find yourself needing to make non-blocking calls.</span></span> <span data-ttu-id="2a3be-107">为了解决此需求，Azure PowerShell 提供了一流的 [PSJob](/powershell/module/microsoft.powershell.core/about/about_jobs) 支持。</span><span class="sxs-lookup"><span data-stu-id="2a3be-107">To address this need, Azure PowerShell provides first-class [PSJob](/powershell/module/microsoft.powershell.core/about/about_jobs) support.</span></span>

## <a name="context-persistence-and-psjobs"></a><span data-ttu-id="2a3be-108">上下文持久性和 PSJob</span><span class="sxs-lookup"><span data-stu-id="2a3be-108">Context Persistence and PSJobs</span></span>

<span data-ttu-id="2a3be-109">由于 PSJob 作为单独的进程运行，因此必须与 PSJob 共享 Azure 连接。</span><span class="sxs-lookup"><span data-stu-id="2a3be-109">Since PSJobs are run as separate processes, your Azure connection must be shared with them.</span></span> <span data-ttu-id="2a3be-110">使用 `Connect-AzureRmAccount` 登录到 Azure 帐户后，将上下文传递给某个作业。</span><span class="sxs-lookup"><span data-stu-id="2a3be-110">After signing in to your Azure account with `Connect-AzureRmAccount`, pass the context to a job.</span></span>

```azurepowershell-interactive
$creds = Get-Credential
$job = Start-Job { param($context,$vmadmin) New-AzureRmVM -Name MyVm -AzureRmContext $context -Credential $vmadmin} -Arguments (Get-AzureRmContext),$creds
```

<span data-ttu-id="2a3be-111">但是，如果你已选择使用 `Enable-AzureRmContextAutosave` 自动保存上下文，则上下文会自动与所要创建的任何作业共享。</span><span class="sxs-lookup"><span data-stu-id="2a3be-111">However, if you have chosen to have your context automatically saved with `Enable-AzureRmContextAutosave`, the context is automatically shared with any jobs you create.</span></span>

```azurepowershell-interactive
Enable-AzureRmContextAutosave
$creds = Get-Credential
$job = Start-Job { param($vmadmin) New-AzureRmVM -Name MyVm -Credential $vmadmin} -Arguments $creds
```

## <a name="automatic-jobs-with--asjob"></a><span data-ttu-id="2a3be-112">使用 `-AsJob` 的自动作业</span><span class="sxs-lookup"><span data-stu-id="2a3be-112">Automatic Jobs with `-AsJob`</span></span>

<span data-ttu-id="2a3be-113">为方便起见，Azure PowerShell 还针对一些长时间运行的 cmdlet 提供了 `-AsJob` 开关。</span><span class="sxs-lookup"><span data-stu-id="2a3be-113">As a convenience, Azure PowerShell also provides an `-AsJob` switch on some long-running cmdlets.</span></span>
<span data-ttu-id="2a3be-114">使用 `-AsJob` 开关可以更轻松地创建 PSJob。</span><span class="sxs-lookup"><span data-stu-id="2a3be-114">The `-AsJob` switch makes creating PSJobs even easier.</span></span>

```azurepowershell-interactive
$creds = Get-Credential
$job = New-AzureRmVM -Name MyVm -Credential $creds -AsJob
```

<span data-ttu-id="2a3be-115">随时可以使用 `Get-Job` 和 `Get-AzureRmVM` 检查作业和进度。</span><span class="sxs-lookup"><span data-stu-id="2a3be-115">You can inspect the job and progress at any time with `Get-Job` and `Get-AzureRmVM`.</span></span>

```azurepowershell-interactive
Get-Job $job
Get-AzureRmVM MyVm
```

```output
Id Name                                       PSJobTypeName         State   HasMoreData Location  Command
-- ----                                       -------------         -----   ----------- --------  -------
1  Long Running Operation for 'New-AzureRmVM' AzureLongRunningJob`1 Running True        localhost New-AzureRmVM

ResourceGroupName    Name Location          VmSize  OsType     NIC ProvisioningState Zone
-----------------    ---- --------          ------  ------     --- ----------------- ----
MyVm                 MyVm   eastus Standard_DS1_v2 Windows    MyVm          Creating
```

<span data-ttu-id="2a3be-116">作业完成后，使用 `Receive-Job` 获取作业的结果。</span><span class="sxs-lookup"><span data-stu-id="2a3be-116">When the job completes, get the result of the job with `Receive-Job`.</span></span>

> [!NOTE]
> <span data-ttu-id="2a3be-117">`Receive-Job` 从该 cmdlet 返回结果，就好像未设置 `-AsJob` 标志一样。</span><span class="sxs-lookup"><span data-stu-id="2a3be-117">`Receive-Job` returns the result from the cmdlet as if the `-AsJob` flag were not present.</span></span>
> <span data-ttu-id="2a3be-118">例如，`Do-Action -AsJob` 的 `Receive-Job` 结果类型与 `Do-Action` 的结果类型相同。</span><span class="sxs-lookup"><span data-stu-id="2a3be-118">For example, the `Receive-Job` result of `Do-Action -AsJob` is of the same type as the result of `Do-Action`.</span></span>

```azurepowershell-interactive
$vm = Receive-Job $job
$vm
```

```output
ResourceGroupName        : MyVm
Id                       : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyVm/providers/Microsoft.Compute/virtualMachines/MyVm
VmId                     : dff1f79e-a8f7-4664-ab72-0ec28b9fbb5b
Name                     : MyVm
Type                     : Microsoft.Compute/virtualMachines
Location                 : eastus
Tags                     : {}
HardwareProfile          : {VmSize}
NetworkProfile           : {NetworkInterfaces}
OSProfile                : {ComputerName, AdminUsername, WindowsConfiguration, Secrets}
ProvisioningState        : Succeeded
StorageProfile           : {ImageReference, OsDisk, DataDisks}
FullyQualifiedDomainName : myvmmyvm.eastus.cloudapp.azure.com
```

## <a name="example-scenarios"></a><span data-ttu-id="2a3be-119">示例方案</span><span class="sxs-lookup"><span data-stu-id="2a3be-119">Example Scenarios</span></span>

<span data-ttu-id="2a3be-120">一次性创建多个 VM：</span><span class="sxs-lookup"><span data-stu-id="2a3be-120">Create several VMs at once:</span></span>

```azurepowershell-interactive
$creds = Get-Credential
# Create 10 jobs.
for($k = 0; $k -lt 10; $k++) {
    New-AzureRmVm -Name MyVm$k  -Credential $creds -AsJob
}

# Get all jobs and wait on them.
Get-Job | Wait-Job
"All jobs completed"
Get-AzureRmVM
```

<span data-ttu-id="2a3be-121">在此示例中，`Wait-Job` cmdlet 会在运行作业时导致脚本暂停。</span><span class="sxs-lookup"><span data-stu-id="2a3be-121">In this example, the `Wait-Job` cmdlet causes the script to pause while jobs run.</span></span> <span data-ttu-id="2a3be-122">所有作业完成后，该脚本会继续执行。</span><span class="sxs-lookup"><span data-stu-id="2a3be-122">The script continues executing once all of the jobs have completed.</span></span> <span data-ttu-id="2a3be-123">多个作业将并行运行，同时，脚本会等待作业完成，然后继续</span><span class="sxs-lookup"><span data-stu-id="2a3be-123">Several jobs run in parallel then the script waits for completion before continuing.</span></span>

```output
Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
2      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
3      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
4      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
5      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
6      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
7      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
8      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
9      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
10     Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
11     Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
2      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
3      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
4      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
5      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
6      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
7      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
8      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
9      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
10     Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
11     Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
All Jobs completed.

ResourceGroupName        Name   Location          VmSize  OsType           NIC ProvisioningState Zone
-----------------        ----   --------          ------  ------           --- ----------------- ----
MYVM                     MyVm     eastus Standard_DS1_v2 Windows          MyVm         Succeeded
MYVM0                   MyVm0     eastus Standard_DS1_v2 Windows         MyVm0         Succeeded
MYVM1                   MyVm1     eastus Standard_DS1_v2 Windows         MyVm1         Succeeded
MYVM2                   MyVm2     eastus Standard_DS1_v2 Windows         MyVm2         Succeeded
MYVM3                   MyVm3     eastus Standard_DS1_v2 Windows         MyVm3         Succeeded
MYVM4                   MyVm4     eastus Standard_DS1_v2 Windows         MyVm4         Succeeded
MYVM5                   MyVm5     eastus Standard_DS1_v2 Windows         MyVm5         Succeeded
MYVM6                   MyVm6     eastus Standard_DS1_v2 Windows         MyVm6         Succeeded
MYVM7                   MyVm7     eastus Standard_DS1_v2 Windows         MyVm7         Succeeded
MYVM8                   MyVm8     eastus Standard_DS1_v2 Windows         MyVm8         Succeeded
MYVM9                   MyVm9     eastus Standard_DS1_v2 Windows         MyVm9         Succeeded
```
