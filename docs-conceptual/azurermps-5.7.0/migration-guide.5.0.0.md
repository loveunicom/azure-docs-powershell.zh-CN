# <a name="breaking-changes-for-microsoft-azure-powershell-500"></a><span data-ttu-id="ab2a9-101">Microsoft Azure PowerShell 5.0.0 的重大更改</span><span class="sxs-lookup"><span data-stu-id="ab2a9-101">Breaking changes for Microsoft Azure PowerShell 5.0.0</span></span>

<span data-ttu-id="ab2a9-102">本文档是面向 Microsoft Azure PowerShell cmdlet 的使用者的重大更改通知和迁移指南。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-102">This document serves as both a breaking change notification and migration guide for consumers of the Microsoft Azure PowerShell cmdlets.</span></span> <span data-ttu-id="ab2a9-103">每部分都介绍了重大更改的影响和最简便的迁移路径。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-103">Each section describes both the impetus for the breaking change and the migration path of least resistance.</span></span> <span data-ttu-id="ab2a9-104">有关深入的上下文，请参考与每个更改关联的拉取请求。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-104">For in-depth context, please refer to the pull request associated with each change.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="ab2a9-105">目录</span><span class="sxs-lookup"><span data-stu-id="ab2a9-105">Table of Contents</span></span>

- [<span data-ttu-id="ab2a9-106">ApiManagement cmdlet 的重大更改</span><span class="sxs-lookup"><span data-stu-id="ab2a9-106">Breaking changes to ApiManagement cmdlets</span></span>](#breaking-changes-to-apimanagement-cmdlets)
- [<span data-ttu-id="ab2a9-107">Batch cmdlet 的重大更改</span><span class="sxs-lookup"><span data-stu-id="ab2a9-107">Breaking changes to Batch cmdlets</span></span>](#breaking-changes-to-batch-cmdlets)
- [<span data-ttu-id="ab2a9-108">计算 cmdlet 的重大更改</span><span class="sxs-lookup"><span data-stu-id="ab2a9-108">Breaking changes to Compute cmdlets</span></span>](#breaking-changes-to-compute-cmdlets)
- [<span data-ttu-id="ab2a9-109">EventHub cmdlet 的重大更改</span><span class="sxs-lookup"><span data-stu-id="ab2a9-109">Breaking changes to EventHub cmdlets</span></span>](#breaking-changes-to-eventhub-cmdlets)
- [<span data-ttu-id="ab2a9-110">见解 cmdlet 的重大更改</span><span class="sxs-lookup"><span data-stu-id="ab2a9-110">Breaking changes to Insights cmdlets</span></span>](#breaking-changes-to-insights-cmdlets)
- [<span data-ttu-id="ab2a9-111">网络 cmdlet 的重大更改</span><span class="sxs-lookup"><span data-stu-id="ab2a9-111">Breaking changes to Network cmdlets</span></span>](#breaking-changes-to-network-cmdlets)
- [<span data-ttu-id="ab2a9-112">资源 cmdlet 的重大更改</span><span class="sxs-lookup"><span data-stu-id="ab2a9-112">Breaking changes to Resources cmdlets</span></span>](#breaking-changes-to-resources-cmdlets)
- [<span data-ttu-id="ab2a9-113">ServiceBus cmdlet 的重大更改</span><span class="sxs-lookup"><span data-stu-id="ab2a9-113">Breaking Changes to ServiceBus Cmdlets</span></span>](#breaking-changes-to-servicebus-cmdlets)

## <a name="breaking-changes-to-apimanagement-cmdlets"></a><span data-ttu-id="ab2a9-114">ApiManagement cmdlet 的重大更改</span><span class="sxs-lookup"><span data-stu-id="ab2a9-114">Breaking changes to ApiManagement cmdlets</span></span>

### <a name="new-azurermapimanagementbackendproxy"></a><span data-ttu-id="ab2a9-115">**New-AzureRmApiManagementBackendProxy**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-115">**New-AzureRmApiManagementBackendProxy**</span></span>
- <span data-ttu-id="ab2a9-116">参数“UserName”和“Password”被替换为 PSCredential</span><span class="sxs-lookup"><span data-stu-id="ab2a9-116">Parameters "UserName" and "Password" are being replaced in favor of a PSCredential</span></span>

```powershell
# Old
New-AzureRmApiManagementBackendProxy [other required parameters] -UserName "plain-text string" -Password "plain-text string"

# New
New-AzureRmApiManagementBackendProxy [other required parameters] -Credential $PSCredentialVariable
```

### <a name="new-azurermapimanagementuser"></a><span data-ttu-id="ab2a9-117">**New-AzureRmApiManagementUser**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-117">**New-AzureRmApiManagementUser**</span></span>
- <span data-ttu-id="ab2a9-118">参数“Password”被替换为 SecureString</span><span class="sxs-lookup"><span data-stu-id="ab2a9-118">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmApiManagementUser [other required parameters] -Password "plain-text string"

# New
New-AzureRmApiManagementUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermapimanagementuser"></a><span data-ttu-id="ab2a9-119">**Set-AzureRmApiManagementUser**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-119">**Set-AzureRmApiManagementUser**</span></span>
- <span data-ttu-id="ab2a9-120">参数“Password”被替换为 SecureString</span><span class="sxs-lookup"><span data-stu-id="ab2a9-120">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
Set-AzureRmApiManagementUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmApiManagementUser [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-batch-cmdlets"></a><span data-ttu-id="ab2a9-121">Batch cmdlet 的重大更改</span><span class="sxs-lookup"><span data-stu-id="ab2a9-121">Breaking changes to Batch cmdlets</span></span>

### <a name="new-azurebatchcertificate"></a><span data-ttu-id="ab2a9-122">**New-AzureBatchCertificate**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-122">**New-AzureBatchCertificate**</span></span>
- <span data-ttu-id="ab2a9-123">参数 `Password` 被替换为 SecureString</span><span class="sxs-lookup"><span data-stu-id="ab2a9-123">Parameter `Password` being replaced in favor of a Secure string</span></span>

```powershell
# Old
New-AzureBatchCertificate [other required parameters] -Password "plain-text string"

# New
New-AzureBatchCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurebatchcomputenodeuser"></a><span data-ttu-id="ab2a9-124">**New-AzureBatchComputeNodeUser**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-124">**New-AzureBatchComputeNodeUser**</span></span>
- <span data-ttu-id="ab2a9-125">参数 `Password` 被替换为 SecureString</span><span class="sxs-lookup"><span data-stu-id="ab2a9-125">Parameter `Password` being replaced in favor of a Secure string</span></span>

```powershell
# Old
New-AzureBatchComputeNodeUser [other required parameters] -Password "plain-text string"

# New
New-AzureBatchComputeNodeUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermbatchcomputenodeuser"></a><span data-ttu-id="ab2a9-126">**Set-AzureRmBatchComputeNodeUser**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-126">**Set-AzureRmBatchComputeNodeUser**</span></span>
- <span data-ttu-id="ab2a9-127">参数 `Password` 被替换为 SecureString</span><span class="sxs-lookup"><span data-stu-id="ab2a9-127">Parameter `Password` being replaced in favor of a Secure string</span></span>

```powershell
# Old
Set-AzureRmBatchComputeNodeUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmBatchComputeNodeUser [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurebatchtask"></a><span data-ttu-id="ab2a9-128">**New-AzureBatchTask**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-128">**New-AzureBatchTask**</span></span>
 - <span data-ttu-id="ab2a9-129">删除了 `RunElevated` 开关并已将其替换为 `UserIdentity`。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-129">Removed the `RunElevated` switch and replaced it with `UserIdentity`.</span></span>

```powershell
# Old
New-AzureBatchTask -Id $taskId1 -JobId $jobId -CommandLine "cmd /c echo hello" -RunElevated $TRUE

# New
$autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")
$userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser
New-AzureBatchTask -Id $taskId1 -JobId $jobId -CommandLine "cmd /c echo hello" -UserIdentity $userIdentity
```

<span data-ttu-id="ab2a9-130">这还会影响 `PSCloudTask`、`PSStartTask`、`PSJobManagerTask`、`PSJobPreparationTask` 和 `PSJobReleaseTask` 的 `RunElevated` 属性。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-130">This additionally impacts the `RunElevated` property on `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask`, and `PSJobReleaseTask`.</span></span>

### <a name="psmultiinstancesettings"></a><span data-ttu-id="ab2a9-131">**PSMultiInstanceSettings**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-131">**PSMultiInstanceSettings**</span></span>

- <span data-ttu-id="ab2a9-132">`PSMultiInstanceSettings` 构造函数不再采用必需的 `numberOfInstances` 参数，而是采用必需的 `coordinationCommandLine` 参数。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-132">`PSMultiInstanceSettings` constructor no longer takes a required `numberOfInstances` parameter, instead it takes a required `coordinationCommandLine` parameter.</span></span>

```powershell
# Old
$settings = New-Object Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings -ArgumentList @(2)
$settings.CoordinationCommandLine = "cmd /c echo hello"
New-AzureBatchTask [other parameters] -MultiInstanceSettings $settings

# New
$settings = New-Object Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings -ArgumentList @("cmd /c echo hello", 2)
New-AzureBatchTask [other parameters] -MultiInstanceSettings $settings
```

### <a name="get-azurebatchtask"></a><span data-ttu-id="ab2a9-133">**Get-AzureBatchTask**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-133">**Get-AzureBatchTask**</span></span>
 - <span data-ttu-id="ab2a9-134">删除了 `PSCloudTask` 的 `RunElevated` 属性。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-134">Removed the `RunElevated` property on `PSCloudTask`.</span></span> <span data-ttu-id="ab2a9-135">添加了 `UserIdentity` 属性来替换 `RunElevated`。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-135">The `UserIdentity` property has been added to replace `RunElevated`.</span></span>

```powershell
# Old
$task = Get-AzureBatchTask [parameters]
$task.RunElevated

# New
$task = Get-AzureBatchTask [parameters]
$task.UserIdentity.AutoUser.ElevationLevel
```

<span data-ttu-id="ab2a9-136">这还会影响 `PSCloudTask`、`PSStartTask`、`PSJobManagerTask`、`PSJobPreparationTask` 和 `PSJobReleaseTask` 的 `RunElevated` 属性。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-136">This additionally impacts the `RunElevated` property on `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask`, and `PSJobReleaseTask`.</span></span>

### <a name="multiple-types"></a><span data-ttu-id="ab2a9-137">**多个类型**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-137">**Multiple types**</span></span>

- <span data-ttu-id="ab2a9-138">已将 `PSExitConditions` 的 `SchedulingError` 属性重命名为 `PreProcessingError`。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-138">Renamed the `SchedulingError` property on `PSExitConditions` to `PreProcessingError`.</span></span>

```powershell
# Old
$task = Get-AzureBatchTask [parameters]
$task.ExitConditions.SchedulingError

# New
$task = Get-AzureBatchTask [parameters]
$task.ExitConditions.PreProcessingError
```

### <a name="multiple-types"></a><span data-ttu-id="ab2a9-139">**多个类型**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-139">**Multiple types**</span></span>

- <span data-ttu-id="ab2a9-140">已将 `PSJobPreparationTaskExecutionInformation`、`PSJobReleaseTaskExecutionInformation`、`PSStartTaskInformation`、`PSSubtaskInformation` 和 `PSTaskExecutionInformation` 的 `SchedulingError` 属性重命名为 `FailureInformation`。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-140">Renamed the `SchedulingError` property on `PSJobPreparationTaskExecutionInformation`, `PSJobReleaseTaskExecutionInformation`, `PSStartTaskInformation`, `PSSubtaskInformation`, and `PSTaskExecutionInformation` to `FailureInformation`.</span></span>
  - <span data-ttu-id="ab2a9-141">每次出现任务故障时都将返回 `FailureInformation`。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-141">`FailureInformation` is returned any time there is a task failure.</span></span> <span data-ttu-id="ab2a9-142">这包括所有以前的计划错误情况以及非零任务退出代码和来自新的输出文件功能的文件上传故障。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-142">This includes all previous scheduling error cases, as well as nonzero task exit codes, and file upload failures from the new output files feature.</span></span>
  - <span data-ttu-id="ab2a9-143">它的结构与之前一样，因此使用此类型时不需要更改任何代码。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-143">This is structured the same as before, so no code change is needed when using this type.</span></span>

```powershell
# Old
$task = Get-AzureBatchTask [parameters]
$task.ExecutionInformation.SchedulingError

# New
$task = Get-AzureBatchTask [parameters]
$task.ExecutionInformation.FailureInformation
```

<span data-ttu-id="ab2a9-144">这还会影响：Get-AzureBatchPool、Get-AzureBatchSubtask 和 Get-AzureBatchJobPreparationAndReleaseTaskStatus</span><span class="sxs-lookup"><span data-stu-id="ab2a9-144">This additionally impacts: Get-AzureBatchPool, Get-AzureBatchSubtask, and Get-AzureBatchJobPreparationAndReleaseTaskStatus</span></span>

### <a name="new-azurebatchpool"></a><span data-ttu-id="ab2a9-145">**New-AzureBatchPool**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-145">**New-AzureBatchPool**</span></span>
 - <span data-ttu-id="ab2a9-146">删除了 `TargetDedicated` 并将其替换为 `TargetDedicatedComputeNodes` 和 `TargetLowPriorityComputeNodes`。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-146">Removed `TargetDedicated` and replaced it with `TargetDedicatedComputeNodes` and `TargetLowPriorityComputeNodes`.</span></span>
 - <span data-ttu-id="ab2a9-147">`TargetDedicatedComputeNodes` 具有别名 `TargetDedicated`。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-147">`TargetDedicatedComputeNodes` has an alias `TargetDedicated`.</span></span>

```powershell
# Old
New-AzureBatchPool [other parameters] [-TargetDedicated <Int32>]

# New
New-AzureBatchPool [other parameters] [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
```

<span data-ttu-id="ab2a9-148">这还会影响：Start-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="ab2a9-148">This also impacts: Start-AzureBatchPoolResize</span></span>

### <a name="get-azurebatchpool"></a><span data-ttu-id="ab2a9-149">**Get-AzureBatchPool**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-149">**Get-AzureBatchPool**</span></span>
 - <span data-ttu-id="ab2a9-150">已将 `PSCloudPool` 的 `TargetDedicated` 和 `CurrentDedicated` 属性重命名为 `TargetDedicatedComputeNodes` 和 `CurrentDedicatedComputeNodes`。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-150">Renamed the `TargetDedicated` and `CurrentDedicated` properties on `PSCloudPool` to `TargetDedicatedComputeNodes` and `CurrentDedicatedComputeNodes`.</span></span>

```powershell
# Old
$pool = Get-AzureBatchPool [parameters]
$pool.TargetDedicated
$pool.CurrentDedicated

# New
$pool = Get-AzureBatchPool [parameters]
$pool.TargetDedicatedComputeNodes
$pool.CurrentDedicatedComputeNodes
```

### <a name="type-pscloudpool"></a><span data-ttu-id="ab2a9-151">**Type PSCloudPool**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-151">**Type PSCloudPool**</span></span>

- <span data-ttu-id="ab2a9-152">已将 `PSCloudPool` 的 `ResizeError` 重命名为 `ResizeErrors`，它现在是一个集合。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-152">Renamed `ResizeError` to `ResizeErrors` on `PSCloudPool`, and it is now a collection.</span></span>

```powershell
# Old
$pool = Get-AzureBatchPool [parameters]
$pool.ResizeError

# New
$pool = Get-AzureBatchPool [parameters]
$pool.ResizeErrors[0]
```

### <a name="new-azurebatchjob"></a><span data-ttu-id="ab2a9-153">**New-AzureBatchJob**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-153">**New-AzureBatchJob**</span></span>
- <span data-ttu-id="ab2a9-154">已将 `PSPoolSpecification` 的 `TargetDedicated` 属性重命名为 `TargetDedicatedComputeNodes`。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-154">Renamed the `TargetDedicated` property on `PSPoolSpecification` to `TargetDedicatedComputeNodes`.</span></span>

```powershell
# Old
$poolInfo = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
$poolInfo.AutoPoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification.TargetDedicated = 5
New-AzureBatchJob [other parameters] -PoolInformation $poolInfo

# New
$poolInfo = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
$poolInfo.AutoPoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification.TargetDedicatedComputeNodes = 5
New-AzureBatchJob [other parameters] -PoolInformation $poolInfo
```

### <a name="get-azurebatchnodefile"></a><span data-ttu-id="ab2a9-155">**Get-AzureBatchNodeFile**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-155">**Get-AzureBatchNodeFile**</span></span>
 - <span data-ttu-id="ab2a9-156">删除了 `Name` 并将其替换为 `Path`。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-156">Removed `Name` and replaced it with `Path`.</span></span>
 - <span data-ttu-id="ab2a9-157">`Path` 具有别名 `Name`。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-157">`Path` has an alias `Name`.</span></span>

```powershell
# Old
Get-AzureBatchNodeFile [other parameters] [[-Name] <String>]

# New
Get-AzureBatchNodeFile [other parameters] [[-Path] <String>]
```

<span data-ttu-id="ab2a9-158">这还会影响：Get-AzureBatchNodeFileContent、Remove-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="ab2a9-158">This also impacts: Get-AzureBatchNodeFileContent, Remove-AzureBatchNodeFile</span></span>

### <a name="type-psnodefile"></a><span data-ttu-id="ab2a9-159">类型 **PSNodeFile**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-159">Type **PSNodeFile**</span></span>

 - <span data-ttu-id="ab2a9-160">已将 `PSNodeFile` 的 `Name` 属性重命名为 `Path`。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-160">Renamed the `Name` property on `PSNodeFile` to `Path`.</span></span>

```powershell
# Old
$file = Get-AzureBatchNodeFile [parameters]
$file.Name

# New
$file = Get-AzureBatchNodeFile [parameters]
$file.Path
```

### <a name="get-azurebatchsubtask"></a><span data-ttu-id="ab2a9-161">**Get-AzureBatchSubtask**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-161">**Get-AzureBatchSubtask**</span></span>
- <span data-ttu-id="ab2a9-162">`PSSubtaskInformation` 的 `PreviousState` 和 `State` 属性不再是 `TaskState` 类型的，而是 `SubtaskState` 类型的。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-162">The `PreviousState` and `State` properties of `PSSubtaskInformation` are no longer of type `TaskState`, instead they are of type `SubtaskState`.</span></span>
  - <span data-ttu-id="ab2a9-163">与 `TaskState` 不同，`SubtaskState` 没有 `Active` 值，因为子任务不可能处于 `Active` 状态。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-163">Unlike `TaskState`, `SubtaskState` has no `Active` value, since it is not possible for subtasks to be in an `Active` state.</span></span>

```powershell
# Old
$subtask = Get-AzureBatchSubtask [parameters]
if ($subtask.State -eq Microsoft.Azure.Batch.Common.TaskState.Running) { }

# New
$subtask = Get-AzureBatchSubtask [parameters]
if ($subtask.State -eq Microsoft.Azure.Batch.Common.SubtaskState.Running) { }
```

## <a name="breaking-changes-to-compute-cmdlets"></a><span data-ttu-id="ab2a9-164">计算 cmdlet 的重大更改</span><span class="sxs-lookup"><span data-stu-id="ab2a9-164">Breaking changes to Compute cmdlets</span></span>

### <a name="set-azurermvmaccessextension"></a><span data-ttu-id="ab2a9-165">**Set-AzureRmVMAccessExtension**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-165">**Set-AzureRmVMAccessExtension**</span></span>
- <span data-ttu-id="ab2a9-166">参数“UserName”和“Password”被替换为 PSCredential</span><span class="sxs-lookup"><span data-stu-id="ab2a9-166">Parameters "UserName" and "Password" are being replaced in favor of a PSCredential</span></span>

```powershell
# Old
Set-AzureRmVMAccessExtension [other required parameters] -UserName "plain-text string" -Password "plain-text string"

# New
Set-AzureRmVMAccessExtension [other required parameters] -Credential $PSCredential
```

## <a name="breaking-changes-to-eventhub-cmdlets"></a><span data-ttu-id="ab2a9-167">EventHub cmdlet 的重大更改</span><span class="sxs-lookup"><span data-stu-id="ab2a9-167">Breaking changes to EventHub cmdlets</span></span>

### <a name="new-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="ab2a9-168">**New-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-168">**New-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="ab2a9-169">“New-AzureRmEventHubNamespaceAuthorizationRule”cmdlet 已删除。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-169">The 'New-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="ab2a9-170">请使用“New-AzureRmEventHubAuthorizationRule”cmdlet</span><span class="sxs-lookup"><span data-stu-id="ab2a9-170">Please use the 'New-AzureRmEventHubAuthorizationRule' cmdlet</span></span>
    
### <a name="get-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="ab2a9-171">**Get-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-171">**Get-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="ab2a9-172">“Get-AzureRmEventHubNamespaceAuthorizationRule”cmdlet 已删除。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-172">The 'Get-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="ab2a9-173">请使用“Get-AzureRmEventHubAuthorizationRule”cmdlet</span><span class="sxs-lookup"><span data-stu-id="ab2a9-173">Please use the 'Get-AzureRmEventHubAuthorizationRule' cmdlet</span></span>
    
### <a name="set-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="ab2a9-174">**Set-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-174">**Set-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="ab2a9-175">“Set-AzureRmEventHubNamespaceAuthorizationRule”cmdlet 已删除。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-175">The 'Set-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="ab2a9-176">请使用“Set-AzureRmEventHubAuthorizationRule”cmdlet</span><span class="sxs-lookup"><span data-stu-id="ab2a9-176">Please use the 'Set-AzureRmEventHubAuthorizationRule' cmdlet</span></span>
    
### <a name="remove-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="ab2a9-177">**Remove-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-177">**Remove-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="ab2a9-178">“Remove-AzureRmEventHubNamespaceAuthorizationRule”cmdlet 已删除。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-178">The 'Remove-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="ab2a9-179">请使用“Remove-AzureRmEventHubAuthorizationRule”cmdlet</span><span class="sxs-lookup"><span data-stu-id="ab2a9-179">Please use the 'Remove-AzureRmEventHubAuthorizationRule' cmdlet</span></span>
    
### <a name="new-azurermeventhubnamespacekey"></a><span data-ttu-id="ab2a9-180">**New-AzureRmEventHubNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-180">**New-AzureRmEventHubNamespaceKey**</span></span>
- <span data-ttu-id="ab2a9-181">“New-AzureRmEventHubNamespaceKey”cmdlet 已删除。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-181">The 'New-AzureRmEventHubNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="ab2a9-182">请使用“New-AzureRmEventHubKey”cmdlet</span><span class="sxs-lookup"><span data-stu-id="ab2a9-182">Please use the 'New-AzureRmEventHubKey' cmdlet</span></span>
    
### <a name="get-azurermeventhubnamespacekey"></a><span data-ttu-id="ab2a9-183">**Get-AzureRmEventHubNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-183">**Get-AzureRmEventHubNamespaceKey**</span></span>
- <span data-ttu-id="ab2a9-184">“Get-AzureRmEventHubNamespaceKey”cmdlet 已删除。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-184">The 'Get-AzureRmEventHubNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="ab2a9-185">请使用“Get-AzureRmEventHubKey”cmdlet</span><span class="sxs-lookup"><span data-stu-id="ab2a9-185">Please use the 'Get-AzureRmEventHubKey' cmdlet</span></span>
    
### <a name="new-azurermeventhubnamespace"></a><span data-ttu-id="ab2a9-186">**New-AzureRmEventHubNamespace**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-186">**New-AzureRmEventHubNamespace**</span></span>
- <span data-ttu-id="ab2a9-187">NamespceAttributes 的属性“Status”和“Enabled”将删除。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-187">The property 'Status' and 'Enabled' from the NamespceAttributes will be removed.</span></span> 

```powershell
# Old
# The $namespace has Status and Enabled property  
$namespace = New-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property    
$namespace = Get-AzureRmEventHubNamespace <parameters>
```
    
### <a name="get-azurermeventhubnamespace"></a><span data-ttu-id="ab2a9-188">**Get-AzureRmEventHubNamespace**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-188">**Get-AzureRmEventHubNamespace**</span></span>
- <span data-ttu-id="ab2a9-189">NamespceAttributes 的属性“Status”和“Enabled”将删除。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-189">The property 'Status' and 'Enabled' from the NamespceAttributes will be removed.</span></span> 

```powershell
# Old
# The $namespace has Status and Enabled property 
$namespace = Get-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property    
$namespace = Get-AzureRmEventHubNamespace <parameters>
```
    
### <a name="set-azurermeventhubnamespace"></a><span data-ttu-id="ab2a9-190">**Set-AzureRmEventHubNamespace**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-190">**Set-AzureRmEventHubNamespace**</span></span>
- <span data-ttu-id="ab2a9-191">NamespceAttributes 的属性“Status”和“Enabled”将删除。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-191">The property 'Status' and 'Enabled' from the NamespceAttributes will be removed.</span></span> 

```powershell
# Old
# The $namespace has Status and Enabled property 
$namespace = Set-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property    
$namespace = Set-AzureRmEventHubNamespace <parameters>
``` 
  
### <a name="new-azurermeventhubconsumergroup"></a><span data-ttu-id="ab2a9-192">**New-AzureRmEventHubConsumerGroup**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-192">**New-AzureRmEventHubConsumerGroup**</span></span>
- <span data-ttu-id="ab2a9-193">ConsumerGroupAttributes 的属性“EventHubPath”将删除。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-193">The property 'EventHubPath' from the ConsumerGroupAttributes will be removed.</span></span>

```powershell
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = New-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = New-AzureRmEventHubConsumerGroup <parameters>
```
    
### <a name="set-azurermeventhubconsumergroup"></a><span data-ttu-id="ab2a9-194">**Set-AzureRmEventHubConsumerGroup**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-194">**Set-AzureRmEventHubConsumerGroup**</span></span>
- <span data-ttu-id="ab2a9-195">ConsumerGroupAttributes 的属性“EventHubPath”将删除。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-195">The property 'EventHubPath' from the ConsumerGroupAttributes will be removed.</span></span>

```powershell
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = Set-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = Set-AzureRmEventHubConsumerGroup <parameters>
```
    
### <a name="get-azurermeventhubconsumergroup"></a><span data-ttu-id="ab2a9-196">**Get-AzureRmEventHubConsumerGroup**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-196">**Get-AzureRmEventHubConsumerGroup**</span></span>
- <span data-ttu-id="ab2a9-197">ConsumerGroupAttributes 的属性“EventHubPath”将删除。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-197">The property 'EventHubPath' from the ConsumerGroupAttributes will be removed.</span></span>

```powershell
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = Get-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = Get-AzureRmEventHubConsumerGroup <parameters>
```

## <a name="breaking-changes-to-insights-cmdlets"></a><span data-ttu-id="ab2a9-198">见解 cmdlet 的重大更改</span><span class="sxs-lookup"><span data-stu-id="ab2a9-198">Breaking changes to Insights cmdlets</span></span>

### <a name="add-azurermlogalertrule"></a><span data-ttu-id="ab2a9-199">**Add-AzureRMLogAlertRule**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-199">**Add-AzureRMLogAlertRule**</span></span>
- <span data-ttu-id="ab2a9-200">**Add-AzureRMLogAlertRule** cmdlet 已弃用</span><span class="sxs-lookup"><span data-stu-id="ab2a9-200">The **Add-AzureRMLogAlertRule** cmdlet has been deprecated</span></span>
- <span data-ttu-id="ab2a9-201">在 10 月 1 日之后，使用此 cmdlet 将不再有任何效果，因为此功能正在迁移到活动日志警报。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-201">After October 1st using this cmdlet will no longer have any effect as this functionality is being transitioned to Activity Log Alerts.</span></span> <span data-ttu-id="ab2a9-202">有关详细信息，请参阅 https://aka.ms/migratemealerts。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-202">Please see https://aka.ms/migratemealerts for more information.</span></span>

### <a name="get-azurermusage"></a><span data-ttu-id="ab2a9-203">**Get-AzureRMUsage**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-203">**Get-AzureRMUsage**</span></span>
- <span data-ttu-id="ab2a9-204">**Get-AzureRMUsage** cmdlet 已弃用</span><span class="sxs-lookup"><span data-stu-id="ab2a9-204">The **Get-AzureRMUsage** cmdlet has been deprecated</span></span>

### <a name="get-azurermalerthistory--get-azurermautoscalehistory--get-azurermlogs"></a><span data-ttu-id="ab2a9-205">**Get-AzureRmAlertHistory** / **Get-AzureRmAutoscaleHistory** / **Get-AzureRmLogs**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-205">**Get-AzureRmAlertHistory** / **Get-AzureRmAutoscaleHistory** / **Get-AzureRmLogs**</span></span>
- <span data-ttu-id="ab2a9-206">输出更改：（由这些 cmdlet 返回的）EventData 对象的字段 EventChannels 将被弃用，因为它现在返回一个常量值 (Admin,Operation)。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-206">Output change: The field EventChannels from the EventData object (returned by these cmdlets) is being deprecated since it now returns a constant value (Admin,Operation.)</span></span>

### <a name="get-azurermalertrule"></a><span data-ttu-id="ab2a9-207">**Get-AzureRmAlertRule**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-207">**Get-AzureRmAlertRule**</span></span>
- <span data-ttu-id="ab2a9-208">输出更改：此 cmdlet 的输出将平展（即取消 properties 字段）以改善用户体验。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-208">Output change: The output of this cmdlet will be flattened, i.e. elimination of the properties field, to improve the user experience.</span></span>

```powershell
# Old
$rules = Get-AzureRmAlertRule -ResourceGroup $resourceGroup
if ($rules -and $rules.count -ge 1)
{
    Write-Host -Foreground Red "Error updating alert rule"
    Write-Host $rules[0].Id
    Write-Host $rules[0].Properties.IsEnabled
    Write-Host $rules[0].Properties.Condition
}

# New
$rules = Get-AzureRmAlertRule -ResourceGroup $resourceGroup
if ($rules -and $rules.count -ge 1)
{
    Write-Host -Foreground red "Error updating alert rule"
    Write-Host $rules[0].Id

    # Properties will remain for a while
    Write-Host $rules[0].Properties.IsEnabled
      
    # But the properties will be at the top level too. Later Properties will be removed
    Write-Host $rules[0].IsEnabled
    Write-Host $rules[0].Condition
}
```

### <a name="get-azurermautoscalesetting"></a><span data-ttu-id="ab2a9-209">**Get-AzureRmAutoscaleSetting**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-209">**Get-AzureRmAutoscaleSetting**</span></span>
- <span data-ttu-id="ab2a9-210">输出更改：AutoscaleSettingResourceName 字段将弃用，因为它始终等于 Name 字段。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-210">Output change: The AutoscaleSettingResourceName field will be deprecated since it always equals the Name field.</span></span>

```powershell
# Old
$s1 = Get-AzureRmAutoscaleSetting -ResourceGroup $resourceGroup -Name MySetting
if ($s1.AutoscaleSettingResourceName -ne $s1.Name)
{
    Write-Host "There is something wrong with the name"
}

# New
$s1 = Get-AzureRmAutoscaleSetting -ResourceGroup $resourceGroup -Name MySetting
    
# there won't be a AutoscaleSettingResourceName
Write-Host $s1.Name    
```

### <a name="remove-azurermalertrule--remove-azurermlogprofile"></a><span data-ttu-id="ab2a9-211">**Remove-AzureRmAlertRule** / **Remove-AzureRmLogProfile**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-211">**Remove-AzureRmAlertRule** / **Remove-AzureRmLogProfile**</span></span>
- <span data-ttu-id="ab2a9-212">输出更改：输出类型将更改为返回内含请求 Id 和状态代码的单个对象。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-212">Output change: The type of the output will change to return a single object containing the request Id and the status code.</span></span>

```powershell
# Old
$s1 = Remove-AzureRmAlertRule -ResourceGroup $resourceGroup -name $ruleName
if ($s1 -ne $null)
{
    $r = $s1[0].RequestId
    $s = $s1[0].StatusCode
}

# New
$s1 = Remove-AzureRmAlertRule -ResourceGroup $resourceGroup -name $ruleName
$r = $s1.RequestId
$s = $s1.StatusCode
```

## <a name="breaking-changes-to-network-cmdlets"></a><span data-ttu-id="ab2a9-213">网络 cmdlet 的重大更改</span><span class="sxs-lookup"><span data-stu-id="ab2a9-213">Breaking changes to Network cmdlets</span></span>

### <a name="add-azurermapplicationgatewaysslcertificate"></a><span data-ttu-id="ab2a9-214">**Add-AzureRmApplicationGatewaySslCertificate**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-214">**Add-AzureRmApplicationGatewaySslCertificate**</span></span>
- <span data-ttu-id="ab2a9-215">参数“Password”被替换为 SecureString</span><span class="sxs-lookup"><span data-stu-id="ab2a9-215">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
Add-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
Add-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermapplicationgatewaysslcertificate"></a><span data-ttu-id="ab2a9-216">**New-AzureRmApplicationGatewaySslCertificate**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-216">**New-AzureRmApplicationGatewaySslCertificate**</span></span>
- <span data-ttu-id="ab2a9-217">参数“Password”被替换为 SecureString</span><span class="sxs-lookup"><span data-stu-id="ab2a9-217">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
New-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermapplicationgatewaysslcertificate"></a><span data-ttu-id="ab2a9-218">**Set-AzureRmApplicationGatewaySslCertificate**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-218">**Set-AzureRmApplicationGatewaySslCertificate**</span></span>
- <span data-ttu-id="ab2a9-219">参数“Password”被替换为 SecureString</span><span class="sxs-lookup"><span data-stu-id="ab2a9-219">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
Set-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
Set-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-resources-cmdlets"></a><span data-ttu-id="ab2a9-220">资源 cmdlet 的重大更改</span><span class="sxs-lookup"><span data-stu-id="ab2a9-220">Breaking changes to Resources cmdlets</span></span>

### <a name="new-azurermadappcredential"></a><span data-ttu-id="ab2a9-221">**New-AzureRmADAppCredential**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-221">**New-AzureRmADAppCredential**</span></span>
- <span data-ttu-id="ab2a9-222">参数“Password”被替换为 SecureString</span><span class="sxs-lookup"><span data-stu-id="ab2a9-222">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmADAppCredential [other required parameters] -Password "plain-text string"

# New
New-AzureRmADAppCredential [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadapplication"></a><span data-ttu-id="ab2a9-223">**New-AzureRmADApplication**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-223">**New-AzureRmADApplication**</span></span>
- <span data-ttu-id="ab2a9-224">参数“Password”被替换为 SecureString</span><span class="sxs-lookup"><span data-stu-id="ab2a9-224">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmADApplication [other required parameters] -Password "plain-text string"

# New
New-AzureRmADApplication [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadserviceprincipal"></a><span data-ttu-id="ab2a9-225">**New-AzureRmADServicePrincipal**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-225">**New-AzureRmADServicePrincipal**</span></span>
- <span data-ttu-id="ab2a9-226">参数“Password”被替换为 SecureString</span><span class="sxs-lookup"><span data-stu-id="ab2a9-226">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmADServicePrincipal [other required parameters] -Password "plain-text string"

# New
New-AzureRmADServicePrincipal [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadspcredential"></a><span data-ttu-id="ab2a9-227">**New-AzureRmADSpCredential**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-227">**New-AzureRmADSpCredential**</span></span>
- <span data-ttu-id="ab2a9-228">参数“Password”被替换为 SecureString</span><span class="sxs-lookup"><span data-stu-id="ab2a9-228">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmADSpCredential [other required parameters] -Password "plain-text string"

# New
New-AzureRmADSpCredential [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermaduser"></a><span data-ttu-id="ab2a9-229">**New-AzureRmADUser**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-229">**New-AzureRmADUser**</span></span>
- <span data-ttu-id="ab2a9-230">参数“Password”被替换为 SecureString</span><span class="sxs-lookup"><span data-stu-id="ab2a9-230">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmADUser [other required parameters] -Password "plain-text string"

# New
New-AzureRmADUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermaduser"></a><span data-ttu-id="ab2a9-231">**Set-AzureRmADUser**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-231">**Set-AzureRmADUser**</span></span>
- <span data-ttu-id="ab2a9-232">参数“Password”被替换为 SecureString</span><span class="sxs-lookup"><span data-stu-id="ab2a9-232">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
Set-AzureRmADUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmADUser [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-servicebus-cmdlets"></a><span data-ttu-id="ab2a9-233">ServiceBus cmdlet 的重大更改</span><span class="sxs-lookup"><span data-stu-id="ab2a9-233">Breaking changes to ServiceBus cmdlets</span></span>

### <a name="get-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="ab2a9-234">**Get-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-234">**Get-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="ab2a9-235">“Get-AzureRmServiceBusTopicAuthorizationRule”cmdlet 已删除。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-235">The 'Get-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="ab2a9-236">请使用“Get-AzureRmServiceBusAuthorizationRule”cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-236">Please use the 'Get-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>    

### <a name="get-azurermservicebustopickey"></a><span data-ttu-id="ab2a9-237">**Get-AzureRmServiceBusTopicKey**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-237">**Get-AzureRmServiceBusTopicKey**</span></span>
- <span data-ttu-id="ab2a9-238">“Get-AzureRmServiceBusTopicKey”cmdlet 已删除。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-238">The 'Get-AzureRmServiceBusTopicKey' cmdlet has been removed.</span></span> <span data-ttu-id="ab2a9-239">请使用“Get-AzureRmServiceBusKey”cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-239">Please use the 'Get-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="new-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="ab2a9-240">**New-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-240">**New-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="ab2a9-241">“New-AzureRmServiceBusTopicAuthorizationRule”cmdlet 已删除。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-241">The 'New-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="ab2a9-242">请使用“New-AzureRmServiceBusAuthorizationRule”cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-242">Please use the 'New-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="new-azurermservicebustopickey"></a><span data-ttu-id="ab2a9-243">**New-AzureRmServiceBusTopicKey**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-243">**New-AzureRmServiceBusTopicKey**</span></span>
- <span data-ttu-id="ab2a9-244">“New-AzureRmServiceBusTopicKey”cmdlet 已删除。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-244">The 'New-AzureRmServiceBusTopicKey' cmdlet has been removed.</span></span> <span data-ttu-id="ab2a9-245">请使用“New-AzureRmServiceBusKey”cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-245">Please use the 'New-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="remove-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="ab2a9-246">**Remove-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-246">**Remove-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="ab2a9-247">“Remove-AzureRmServiceBusTopicAuthorizationRule”cmdlet 已删除。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-247">The 'Remove-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="ab2a9-248">请使用“Remove-AzureRmServiceBusAuthorizationRule”cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-248">Please use the 'Remove-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="set-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="ab2a9-249">**Set-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-249">**Set-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="ab2a9-250">“Set-AzureRmServiceBusTopicAuthorizationRule”cmdlet 已删除。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-250">The 'Set-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="ab2a9-251">请使用“Set-AzureRmServiceBusAuthorizationRule”cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-251">Please use the 'Set-AzureRmServiceBusAuthorizationRule'cmdlet.</span></span>

### <a name="new-azurermservicebusnamespacekey"></a><span data-ttu-id="ab2a9-252">**New-AzureRmServiceBusNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-252">**New-AzureRmServiceBusNamespaceKey**</span></span>
- <span data-ttu-id="ab2a9-253">“New-AzureRmServiceBusNamespaceKey”cmdlet 已删除。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-253">The 'New-AzureRmServiceBusNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="ab2a9-254">请使用“New-AzureRmServiceBusKey”cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-254">Please use the 'New-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="get-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="ab2a9-255">**Get-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-255">**Get-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="ab2a9-256">“Get-AzureRmServiceBusQueueAuthorizationRule”cmdlet 已删除。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-256">The 'Get-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="ab2a9-257">请使用“Get-AzureRmServiceBusAuthorizationRule”cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-257">Please use the 'Get-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="get-azurermservicebusqueuekey"></a><span data-ttu-id="ab2a9-258">**Get-AzureRmServiceBusQueueKey**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-258">**Get-AzureRmServiceBusQueueKey**</span></span>
- <span data-ttu-id="ab2a9-259">“Get-AzureRmServiceBusQueueKey”cmdlet 已删除。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-259">The 'Get-AzureRmServiceBusQueueKey' cmdlet has been removed.</span></span> <span data-ttu-id="ab2a9-260">请使用“Get-AzureRmServiceBusKey”cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-260">Please use the 'Get-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="new-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="ab2a9-261">**New-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-261">**New-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="ab2a9-262">“New-AzureRmServiceBusQueueAuthorizationRule”cmdlet 已删除。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-262">The 'New-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="ab2a9-263">请使用“New-AzureRmServiceBusAuthorizationRule”cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-263">Please use the 'New-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="new-azurermservicebusqueuekey"></a><span data-ttu-id="ab2a9-264">**New-AzureRmServiceBusQueueKey**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-264">**New-AzureRmServiceBusQueueKey**</span></span>
- <span data-ttu-id="ab2a9-265">“New-AzureRmServiceBusQueueKey”cmdlet 已删除。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-265">The 'New-AzureRmServiceBusQueueKey' cmdlet has been removed.</span></span> <span data-ttu-id="ab2a9-266">请使用“New-AzureRmServiceBusKey”cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-266">Please use the 'New-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="remove-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="ab2a9-267">**Remove-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-267">**Remove-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="ab2a9-268">“Remove-AzureRmServiceBusQueueAuthorizationRule”cmdlet 已删除。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-268">The 'Remove-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="ab2a9-269">请使用“GRemove-AzureRmServiceBusAuthorizationRule”cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-269">Please use the 'GRemove-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="set-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="ab2a9-270">**Set-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-270">**Set-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="ab2a9-271">“Set-AzureRmServiceBusQueueAuthorizationRule”cmdlet 已删除。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-271">The 'Set-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="ab2a9-272">请使用“Set-AzureRmServiceBusAuthorizationRule”cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-272">Please use the 'Set-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="get-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="ab2a9-273">**Get-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-273">**Get-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="ab2a9-274">“Get-AzureRmServiceBusNamespaceAuthorizationRule”cmdlet 已删除。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-274">The 'Get-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="ab2a9-275">请使用“Get-AzureRmServiceBusAuthorizationRule”cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-275">Please use the 'Get-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="get-azurermservicebusnamespacekey"></a><span data-ttu-id="ab2a9-276">**Get-AzureRmServiceBusNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-276">**Get-AzureRmServiceBusNamespaceKey**</span></span>
- <span data-ttu-id="ab2a9-277">“Get-AzureRmServiceBusNamespaceKey”cmdlet 已删除。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-277">The 'Get-AzureRmServiceBusNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="ab2a9-278">请使用“Get-AzureRmServiceBusKey”cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-278">Please use the 'Get-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="new-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="ab2a9-279">**New-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-279">**New-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="ab2a9-280">“New-AzureRmServiceBusNamespaceAuthorizationRule”cmdlet 已删除。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-280">The 'New-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="ab2a9-281">请使用“New-AzureRmServiceBusAuthorizationRule”cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-281">Please use the 'New-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="remove-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="ab2a9-282">**Remove-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-282">**Remove-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="ab2a9-283">“Remove-AzureRmServiceBusNamespaceAuthorizationRule”cmdlet 已删除。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-283">The 'Remove-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="ab2a9-284">请使用“Remove-AzureRmServiceBusAuthorizationRule”cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-284">Please use the 'Remove-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="set-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="ab2a9-285">**Set-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-285">**Set-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="ab2a9-286">“Set-AzureRmServiceBusNamespaceAuthorizationRule”cmdlet 已删除。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-286">The 'Set-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="ab2a9-287">请使用“Set-AzureRmServiceBusAuthorizationRule”cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ab2a9-287">Please use the 'Set-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="type-namespaceattributes"></a><span data-ttu-id="ab2a9-288">**类型 NamespaceAttributes**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-288">**Type NamespaceAttributes**</span></span>
- <span data-ttu-id="ab2a9-289">以下属性已删除</span><span class="sxs-lookup"><span data-stu-id="ab2a9-289">The following properties have been removed</span></span>
    - <span data-ttu-id="ab2a9-290">已启用</span><span class="sxs-lookup"><span data-stu-id="ab2a9-290">Enabled</span></span>
    - <span data-ttu-id="ab2a9-291">状态</span><span class="sxs-lookup"><span data-stu-id="ab2a9-291">Status</span></span>
   
```powershell
# Old
# The $namespace has Status and Enabled property 
$namespace = Get-AzureRmServiceBusNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Enabled and Status properties    
$namespace = Get-AzureRmServiceBusNamespace <parameters>
```

### <a name="type-queueattribute"></a><span data-ttu-id="ab2a9-292">**类型 QueueAttribute**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-292">**Type QueueAttribute**</span></span>
- <span data-ttu-id="ab2a9-293">以下属性标记为已过时：</span><span class="sxs-lookup"><span data-stu-id="ab2a9-293">The following properties are marked as obsolete:</span></span>
    - <span data-ttu-id="ab2a9-294">EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="ab2a9-294">EnableBatchedOperations</span></span>
    - <span data-ttu-id="ab2a9-295">EntityAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="ab2a9-295">EntityAvailabilityStatus</span></span>
    - <span data-ttu-id="ab2a9-296">IsAnonymousAccessible</span><span class="sxs-lookup"><span data-stu-id="ab2a9-296">IsAnonymousAccessible</span></span>
    - <span data-ttu-id="ab2a9-297">SupportOrdering</span><span class="sxs-lookup"><span data-stu-id="ab2a9-297">SupportOrdering</span></span>

```powershell
# Old
# The $queue has EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties
$queue = Get-AzureRmServiceBusQueue <parameters>
$queue.EntityAvailabilityStatus
$queue.EnableBatchedOperations
$queue.IsAnonymousAccessible
$queue.SupportOrdering  

# New
# The call remains the same, but the returned values Queue object will not have the EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties    
$queue = Get-AzureRmServiceBusQueue <parameters>
```
   
### <a name="type-topicattribute"></a><span data-ttu-id="ab2a9-298">**类型 TopicAttribute**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-298">**Type TopicAttribute**</span></span>
- <span data-ttu-id="ab2a9-299">以下属性标记为已过时：</span><span class="sxs-lookup"><span data-stu-id="ab2a9-299">The following properties are marked as obsolete:</span></span>
    - <span data-ttu-id="ab2a9-300">Location</span><span class="sxs-lookup"><span data-stu-id="ab2a9-300">Location</span></span>
    - <span data-ttu-id="ab2a9-301">IsExpress</span><span class="sxs-lookup"><span data-stu-id="ab2a9-301">IsExpress</span></span>
    - <span data-ttu-id="ab2a9-302">IsAnonymousAccessible</span><span class="sxs-lookup"><span data-stu-id="ab2a9-302">IsAnonymousAccessible</span></span>
    - <span data-ttu-id="ab2a9-303">FilteringMessagesBeforePublishing</span><span class="sxs-lookup"><span data-stu-id="ab2a9-303">FilteringMessagesBeforePublishing</span></span>
    - <span data-ttu-id="ab2a9-304">EnableSubscriptionPartitioning</span><span class="sxs-lookup"><span data-stu-id="ab2a9-304">EnableSubscriptionPartitioning</span></span>
    - <span data-ttu-id="ab2a9-305">EntityAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="ab2a9-305">EntityAvailabilityStatus</span></span>

```powershell
# Old
# The $topic has EntityAvailabilityStatus, EnableSubscriptionPartitioning, IsAnonymousAccessible, IsExpress, Location and FilteringMessagesBeforePublishing properties
$topic = Get-AzureRmServiceBusTopic <parameters>
$topic.EntityAvailabilityStatus
$topic.EnableSubscriptionPartitioning
$topic.IsAnonymousAccessible
$topic.IsExpress
$topic.FilteringMessagesBeforePublishing
$topic.Location

# New
# The call remains the same, but the returned values Topic object will not have the EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties    
$topic = Get-AzureRmServiceBusTopic <parameters>
```
   
### <a name="type-subscriptionattribute"></a><span data-ttu-id="ab2a9-306">**类型 SubscriptionAttribute**</span><span class="sxs-lookup"><span data-stu-id="ab2a9-306">**Type SubscriptionAttribute**</span></span>
- <span data-ttu-id="ab2a9-307">以下属性标记为已过时</span><span class="sxs-lookup"><span data-stu-id="ab2a9-307">The following properties are marked as obsolete</span></span>
    - <span data-ttu-id="ab2a9-308">DeadLetteringOnFilterEvaluationExceptions</span><span class="sxs-lookup"><span data-stu-id="ab2a9-308">DeadLetteringOnFilterEvaluationExceptions</span></span>
    - <span data-ttu-id="ab2a9-309">EntityAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="ab2a9-309">EntityAvailabilityStatus</span></span>
    - <span data-ttu-id="ab2a9-310">IsReadOnly</span><span class="sxs-lookup"><span data-stu-id="ab2a9-310">IsReadOnly</span></span>
    - <span data-ttu-id="ab2a9-311">Location</span><span class="sxs-lookup"><span data-stu-id="ab2a9-311">Location</span></span>
   
```powershell
# Old
# The $subscription has EntityAvailabilityStatus, EnableSubscriptionPartitioning, IsAnonymousAccessible, IsExpress, Location and FilteringMessagesBeforePublishing properties
$subscription = Get-AzureRmServiceBussubscription <parameters>
$subscription.EntityAvailabilityStatus
$subscription.EnableSubscriptionPartitioning
$subscription.IsAnonymousAccessible
$subscription.IsExpress
$subscription.FilteringMessagesBeforePublishing
$subscription.Location

# New
# The call remains the same, but the returned values Topic object will not have the EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties    
$subscription = Get-AzureRmServiceBussubscription <parameters>
```