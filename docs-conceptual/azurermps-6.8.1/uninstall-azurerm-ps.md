---
title: 卸载 Azure PowerShell
description: 如何完整地卸载 Azure PowerShell
ms.date: 06/20/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 92af0fdd8db451e2f0f092d66a3e296ad8d6a09e
ms.sourcegitcommit: 971f19181b2cd68b7845bbebdb22858c06541c8c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/06/2018
ms.locfileid: "43383662"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="bcea0-103">卸载 Azure PowerShell 模块</span><span class="sxs-lookup"><span data-stu-id="bcea0-103">Uninstall the Azure PowerShell module</span></span>

<span data-ttu-id="bcea0-104">本文介绍如何卸载旧版 Azure PowerShell 或将其从系统中完全删除。</span><span class="sxs-lookup"><span data-stu-id="bcea0-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="bcea0-105">如果你决定彻底卸载 Azure PowerShell，请通过 [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet 为我们提供一些反馈。</span><span class="sxs-lookup"><span data-stu-id="bcea0-105">If you've decided to completely uninstall the Azure PowerShell, please give us some feedback through the [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet.</span></span>
<span data-ttu-id="bcea0-106">如果你在遇到 bug 后[提出 GitHub 问题](https://github.com/azure/azure-powershell/issues)，我们将十分感激。</span><span class="sxs-lookup"><span data-stu-id="bcea0-106">If you encountered a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues).</span></span>

## <a name="uninstall-msi"></a><span data-ttu-id="bcea0-107">卸载 MSI</span><span class="sxs-lookup"><span data-stu-id="bcea0-107">Uninstall MSI</span></span>

<span data-ttu-id="bcea0-108">若是使用 MSI 包安装的 Azure PowerShell，则必须通过 Windows 系统而不是 PowerShell 进行卸载。</span><span class="sxs-lookup"><span data-stu-id="bcea0-108">If you installed Azure PowerShell using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

| <span data-ttu-id="bcea0-109">平台</span><span class="sxs-lookup"><span data-stu-id="bcea0-109">Platform</span></span> | <span data-ttu-id="bcea0-110">说明</span><span class="sxs-lookup"><span data-stu-id="bcea0-110">Instructions</span></span> |
|----------|--------------|
| <span data-ttu-id="bcea0-111">Windows 10</span><span class="sxs-lookup"><span data-stu-id="bcea0-111">Windows 10</span></span> | <span data-ttu-id="bcea0-112">“开始”>“设置”>“应用”</span><span class="sxs-lookup"><span data-stu-id="bcea0-112">Start > Settings > Apps</span></span> |
| <span data-ttu-id="bcea0-113">Windows 7</span><span class="sxs-lookup"><span data-stu-id="bcea0-113">Windows 7</span></span> </br><span data-ttu-id="bcea0-114">Windows 8</span><span class="sxs-lookup"><span data-stu-id="bcea0-114">Windows 8</span></span> | <span data-ttu-id="bcea0-115">“开始”>“控制面板”>“程序”>“卸载程序”</span><span class="sxs-lookup"><span data-stu-id="bcea0-115">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="bcea0-116">转到此屏幕以后，会在程序列表中看到“Azure PowerShell”，可以从该处卸载。</span><span class="sxs-lookup"><span data-stu-id="bcea0-116">Once on this screen you should see "Azure PowerShell" in the program listing, and can uninstall from there.</span></span>

## <a name="uninstall-from-powershell"></a><span data-ttu-id="bcea0-117">从 PowerShell 卸载</span><span class="sxs-lookup"><span data-stu-id="bcea0-117">Uninstall from PowerShell</span></span>

<span data-ttu-id="bcea0-118">若是使用 PowerShellGet 安装的 Azure PowerShell，则可使用 [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bcea0-118">If you installed Azure PowerShell using PowerShellGet, you can use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="bcea0-119">但是，`Uninstall-Module` 只卸载一个模块。</span><span class="sxs-lookup"><span data-stu-id="bcea0-119">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="bcea0-120">若要彻底删除 Azure PowerShell，必须单独卸载每个模块。</span><span class="sxs-lookup"><span data-stu-id="bcea0-120">To remove Azure PowerShell completely, you must uninstall each module individually.</span></span> <span data-ttu-id="bcea0-121">如果安装了多个版本的 Azure PowerShell，则卸载过程可能很复杂。</span><span class="sxs-lookup"><span data-stu-id="bcea0-121">Uninstallation can be complicated if you have multiple versions of Azure PowerShell installed.</span></span>

<span data-ttu-id="bcea0-122">可以使用以下脚本彻底删除单个版本的 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="bcea0-122">The following script can be used to completely remove a single version of Azure PowerShell.</span></span> <span data-ttu-id="bcea0-123">此脚本会查询 PowerShell 库以获取依赖性子模块的列表。</span><span class="sxs-lookup"><span data-stu-id="bcea0-123">The script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="bcea0-124">然后，此脚本会卸载每个子模块的正确版本。</span><span class="sxs-lookup"><span data-stu-id="bcea0-124">Then, the script uninstalls the correct version of each submodule.</span></span>

```powershell
function Uninstall-AllModules {
  param(
    [Parameter(Mandatory=$true)]
    [string]$TargetModule,

    [Parameter(Mandatory=$true)]
    [string]$Version,

    [switch]$Force
  )

  $AllModules = @()

  'Creating list of dependencies...'
  $target = Find-Module $TargetModule -RequiredVersion $version
  $target.Dependencies | ForEach-Object {
    $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$_.requiredversion}
  }
  $AllModules += New-Object -TypeName psobject -Property @{name=$TargetModule; version=$Version}

  foreach ($module in $AllModules) {
    Write-Host ('Uninstalling {0} version {1}' -f $module.name,$module.version)
    try {
      Uninstall-Module -Name $module.name -RequiredVersion $module.version -Force:$Force -ErrorAction Stop
    } catch {
      Write-Host ("`t" + $_.Exception.Message)
    }
  }
}
```

<span data-ttu-id="bcea0-125">若要使用此函数，请将代码复制并粘贴到 PowerShell 会话中。</span><span class="sxs-lookup"><span data-stu-id="bcea0-125">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="bcea0-126">以下示例演示了如何运行此函数来删除旧版 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="bcea0-126">The following example shows how to run the function to remove an older version of Azure PowerShell.</span></span>

```powershell
Uninstall-AllModules -TargetModule AzureRM -Version 4.4.1 -Force
```

<span data-ttu-id="bcea0-127">此脚本在运行时会显示每个要卸载的子模块的名称和版本。</span><span class="sxs-lookup"><span data-stu-id="bcea0-127">As the script runs, it will display the name and version of each submodule that is being uninstalled.</span></span>

```output
Creating list of dependencies...
Uninstalling AzureRM.Profile version 3.4.1
Uninstalling Azure.Storage version 3.4.1
Uninstalling AzureRM.AnalysisServices version 0.4.7
Uninstalling Azure.AnalysisServices version 0.4.7
...
```

<span data-ttu-id="bcea0-128">请针对要卸载的每个 Azure PowerShell 版本运行此命令。</span><span class="sxs-lookup"><span data-stu-id="bcea0-128">Run this command for every version of Azure PowerShell that you want to uninstall.</span></span>
