# <a name="breaking-changes-for-microsoft-azure-powershell-500"></a>Microsoft Azure PowerShell 5.0.0 的重大更改

本文档是面向 Microsoft Azure PowerShell cmdlet 的使用者的重大更改通知和迁移指南。 每部分都介绍了重大更改的影响和最简便的迁移路径。 有关深入的上下文，请参考与每个更改关联的拉取请求。

## <a name="table-of-contents"></a>目录

- [ApiManagement cmdlet 的重大更改](#breaking-changes-to-apimanagement-cmdlets)
- [Batch cmdlet 的重大更改](#breaking-changes-to-batch-cmdlets)
- [计算 cmdlet 的重大更改](#breaking-changes-to-compute-cmdlets)
- [EventHub cmdlet 的重大更改](#breaking-changes-to-eventhub-cmdlets)
- [见解 cmdlet 的重大更改](#breaking-changes-to-insights-cmdlets)
- [网络 cmdlet 的重大更改](#breaking-changes-to-network-cmdlets)
- [资源 cmdlet 的重大更改](#breaking-changes-to-resources-cmdlets)
- [ServiceBus cmdlet 的重大更改](#breaking-changes-to-servicebus-cmdlets)

## <a name="breaking-changes-to-apimanagement-cmdlets"></a>ApiManagement cmdlet 的重大更改

### <a name="new-azurermapimanagementbackendproxy"></a>**New-AzureRmApiManagementBackendProxy**
- 参数“UserName”和“Password”被替换为 PSCredential

```powershell
# Old
New-AzureRmApiManagementBackendProxy [other required parameters] -UserName "plain-text string" -Password "plain-text string"

# New
New-AzureRmApiManagementBackendProxy [other required parameters] -Credential $PSCredentialVariable
```

### <a name="new-azurermapimanagementuser"></a>**New-AzureRmApiManagementUser**
- 参数“Password”被替换为 SecureString

```powershell
# Old
New-AzureRmApiManagementUser [other required parameters] -Password "plain-text string"

# New
New-AzureRmApiManagementUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermapimanagementuser"></a>**Set-AzureRmApiManagementUser**
- 参数“Password”被替换为 SecureString

```powershell
# Old
Set-AzureRmApiManagementUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmApiManagementUser [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-batch-cmdlets"></a>Batch cmdlet 的重大更改

### <a name="new-azurebatchcertificate"></a>**New-AzureBatchCertificate**
- 参数 `Password` 被替换为 SecureString

```powershell
# Old
New-AzureBatchCertificate [other required parameters] -Password "plain-text string"

# New
New-AzureBatchCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurebatchcomputenodeuser"></a>**New-AzureBatchComputeNodeUser**
- 参数 `Password` 被替换为 SecureString

```powershell
# Old
New-AzureBatchComputeNodeUser [other required parameters] -Password "plain-text string"

# New
New-AzureBatchComputeNodeUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermbatchcomputenodeuser"></a>**Set-AzureRmBatchComputeNodeUser**
- 参数 `Password` 被替换为 SecureString

```powershell
# Old
Set-AzureRmBatchComputeNodeUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmBatchComputeNodeUser [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurebatchtask"></a>**New-AzureBatchTask**
 - 删除了 `RunElevated` 开关并已将其替换为 `UserIdentity`。

```powershell
# Old
New-AzureBatchTask -Id $taskId1 -JobId $jobId -CommandLine "cmd /c echo hello" -RunElevated $TRUE

# New
$autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")
$userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser
New-AzureBatchTask -Id $taskId1 -JobId $jobId -CommandLine "cmd /c echo hello" -UserIdentity $userIdentity
```

这还会影响 `PSCloudTask`、`PSStartTask`、`PSJobManagerTask`、`PSJobPreparationTask` 和 `PSJobReleaseTask` 的 `RunElevated` 属性。

### <a name="psmultiinstancesettings"></a>**PSMultiInstanceSettings**

- `PSMultiInstanceSettings` 构造函数不再采用必需的 `numberOfInstances` 参数，而是采用必需的 `coordinationCommandLine` 参数。

```powershell
# Old
$settings = New-Object Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings -ArgumentList @(2)
$settings.CoordinationCommandLine = "cmd /c echo hello"
New-AzureBatchTask [other parameters] -MultiInstanceSettings $settings

# New
$settings = New-Object Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings -ArgumentList @("cmd /c echo hello", 2)
New-AzureBatchTask [other parameters] -MultiInstanceSettings $settings
```

### <a name="get-azurebatchtask"></a>**Get-AzureBatchTask**
 - 删除了 `PSCloudTask` 的 `RunElevated` 属性。 添加了 `UserIdentity` 属性来替换 `RunElevated`。

```powershell
# Old
$task = Get-AzureBatchTask [parameters]
$task.RunElevated

# New
$task = Get-AzureBatchTask [parameters]
$task.UserIdentity.AutoUser.ElevationLevel
```

这还会影响 `PSCloudTask`、`PSStartTask`、`PSJobManagerTask`、`PSJobPreparationTask` 和 `PSJobReleaseTask` 的 `RunElevated` 属性。

### <a name="multiple-types"></a>**多个类型**

- 已将 `PSExitConditions` 的 `SchedulingError` 属性重命名为 `PreProcessingError`。

```powershell
# Old
$task = Get-AzureBatchTask [parameters]
$task.ExitConditions.SchedulingError

# New
$task = Get-AzureBatchTask [parameters]
$task.ExitConditions.PreProcessingError
```

### <a name="multiple-types"></a>**多个类型**

- 已将 `PSJobPreparationTaskExecutionInformation`、`PSJobReleaseTaskExecutionInformation`、`PSStartTaskInformation`、`PSSubtaskInformation` 和 `PSTaskExecutionInformation` 的 `SchedulingError` 属性重命名为 `FailureInformation`。
  - 每次出现任务故障时都将返回 `FailureInformation`。 这包括所有以前的计划错误情况以及非零任务退出代码和来自新的输出文件功能的文件上传故障。
  - 它的结构与之前一样，因此使用此类型时不需要更改任何代码。

```powershell
# Old
$task = Get-AzureBatchTask [parameters]
$task.ExecutionInformation.SchedulingError

# New
$task = Get-AzureBatchTask [parameters]
$task.ExecutionInformation.FailureInformation
```

这还会影响：Get-AzureBatchPool、Get-AzureBatchSubtask 和 Get-AzureBatchJobPreparationAndReleaseTaskStatus

### <a name="new-azurebatchpool"></a>**New-AzureBatchPool**
 - 删除了 `TargetDedicated` 并将其替换为 `TargetDedicatedComputeNodes` 和 `TargetLowPriorityComputeNodes`。
 - `TargetDedicatedComputeNodes` 具有别名 `TargetDedicated`。

```powershell
# Old
New-AzureBatchPool [other parameters] [-TargetDedicated <Int32>]

# New
New-AzureBatchPool [other parameters] [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
```

这还会影响：Start-AzureBatchPoolResize

### <a name="get-azurebatchpool"></a>**Get-AzureBatchPool**
 - 已将 `PSCloudPool` 的 `TargetDedicated` 和 `CurrentDedicated` 属性重命名为 `TargetDedicatedComputeNodes` 和 `CurrentDedicatedComputeNodes`。

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

### <a name="type-pscloudpool"></a>**Type PSCloudPool**

- 已将 `PSCloudPool` 的 `ResizeError` 重命名为 `ResizeErrors`，它现在是一个集合。

```powershell
# Old
$pool = Get-AzureBatchPool [parameters]
$pool.ResizeError

# New
$pool = Get-AzureBatchPool [parameters]
$pool.ResizeErrors[0]
```

### <a name="new-azurebatchjob"></a>**New-AzureBatchJob**
- 已将 `PSPoolSpecification` 的 `TargetDedicated` 属性重命名为 `TargetDedicatedComputeNodes`。

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

### <a name="get-azurebatchnodefile"></a>**Get-AzureBatchNodeFile**
 - 删除了 `Name` 并将其替换为 `Path`。
 - `Path` 具有别名 `Name`。

```powershell
# Old
Get-AzureBatchNodeFile [other parameters] [[-Name] <String>]

# New
Get-AzureBatchNodeFile [other parameters] [[-Path] <String>]
```

这还会影响：Get-AzureBatchNodeFileContent、Remove-AzureBatchNodeFile

### <a name="type-psnodefile"></a>类型 **PSNodeFile**

 - 已将 `PSNodeFile` 的 `Name` 属性重命名为 `Path`。

```powershell
# Old
$file = Get-AzureBatchNodeFile [parameters]
$file.Name

# New
$file = Get-AzureBatchNodeFile [parameters]
$file.Path
```

### <a name="get-azurebatchsubtask"></a>**Get-AzureBatchSubtask**
- `PSSubtaskInformation` 的 `PreviousState` 和 `State` 属性不再是 `TaskState` 类型的，而是 `SubtaskState` 类型的。
  - 与 `TaskState` 不同，`SubtaskState` 没有 `Active` 值，因为子任务不可能处于 `Active` 状态。

```powershell
# Old
$subtask = Get-AzureBatchSubtask [parameters]
if ($subtask.State -eq Microsoft.Azure.Batch.Common.TaskState.Running) { }

# New
$subtask = Get-AzureBatchSubtask [parameters]
if ($subtask.State -eq Microsoft.Azure.Batch.Common.SubtaskState.Running) { }
```

## <a name="breaking-changes-to-compute-cmdlets"></a>计算 cmdlet 的重大更改

### <a name="set-azurermvmaccessextension"></a>**Set-AzureRmVMAccessExtension**
- 参数“UserName”和“Password”被替换为 PSCredential

```powershell
# Old
Set-AzureRmVMAccessExtension [other required parameters] -UserName "plain-text string" -Password "plain-text string"

# New
Set-AzureRmVMAccessExtension [other required parameters] -Credential $PSCredential
```

## <a name="breaking-changes-to-eventhub-cmdlets"></a>EventHub cmdlet 的重大更改

### <a name="new-azurermeventhubnamespaceauthorizationrule"></a>**New-AzureRmEventHubNamespaceAuthorizationRule**
- “New-AzureRmEventHubNamespaceAuthorizationRule”cmdlet 已删除。 请使用“New-AzureRmEventHubAuthorizationRule”cmdlet
    
### <a name="get-azurermeventhubnamespaceauthorizationrule"></a>**Get-AzureRmEventHubNamespaceAuthorizationRule**
- “Get-AzureRmEventHubNamespaceAuthorizationRule”cmdlet 已删除。 请使用“Get-AzureRmEventHubAuthorizationRule”cmdlet
    
### <a name="set-azurermeventhubnamespaceauthorizationrule"></a>**Set-AzureRmEventHubNamespaceAuthorizationRule**
- “Set-AzureRmEventHubNamespaceAuthorizationRule”cmdlet 已删除。 请使用“Set-AzureRmEventHubAuthorizationRule”cmdlet
    
### <a name="remove-azurermeventhubnamespaceauthorizationrule"></a>**Remove-AzureRmEventHubNamespaceAuthorizationRule**
- “Remove-AzureRmEventHubNamespaceAuthorizationRule”cmdlet 已删除。 请使用“Remove-AzureRmEventHubAuthorizationRule”cmdlet
    
### <a name="new-azurermeventhubnamespacekey"></a>**New-AzureRmEventHubNamespaceKey**
- “New-AzureRmEventHubNamespaceKey”cmdlet 已删除。 请使用“New-AzureRmEventHubKey”cmdlet
    
### <a name="get-azurermeventhubnamespacekey"></a>**Get-AzureRmEventHubNamespaceKey**
- “Get-AzureRmEventHubNamespaceKey”cmdlet 已删除。 请使用“Get-AzureRmEventHubKey”cmdlet
    
### <a name="new-azurermeventhubnamespace"></a>**New-AzureRmEventHubNamespace**
- NamespceAttributes 的属性“Status”和“Enabled”将删除。 

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
    
### <a name="get-azurermeventhubnamespace"></a>**Get-AzureRmEventHubNamespace**
- NamespceAttributes 的属性“Status”和“Enabled”将删除。 

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
    
### <a name="set-azurermeventhubnamespace"></a>**Set-AzureRmEventHubNamespace**
- NamespceAttributes 的属性“Status”和“Enabled”将删除。 

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
  
### <a name="new-azurermeventhubconsumergroup"></a>**New-AzureRmEventHubConsumerGroup**
- ConsumerGroupAttributes 的属性“EventHubPath”将删除。

```powershell
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = New-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = New-AzureRmEventHubConsumerGroup <parameters>
```
    
### <a name="set-azurermeventhubconsumergroup"></a>**Set-AzureRmEventHubConsumerGroup**
- ConsumerGroupAttributes 的属性“EventHubPath”将删除。

```powershell
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = Set-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = Set-AzureRmEventHubConsumerGroup <parameters>
```
    
### <a name="get-azurermeventhubconsumergroup"></a>**Get-AzureRmEventHubConsumerGroup**
- ConsumerGroupAttributes 的属性“EventHubPath”将删除。

```powershell
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = Get-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = Get-AzureRmEventHubConsumerGroup <parameters>
```

## <a name="breaking-changes-to-insights-cmdlets"></a>见解 cmdlet 的重大更改

### <a name="add-azurermlogalertrule"></a>**Add-AzureRMLogAlertRule**
- **Add-AzureRMLogAlertRule** cmdlet 已弃用
- 在 10 月 1 日之后，使用此 cmdlet 将不再有任何效果，因为此功能正在迁移到活动日志警报。 有关详细信息，请参阅 https://aka.ms/migratemealerts。

### <a name="get-azurermusage"></a>**Get-AzureRMUsage**
- **Get-AzureRMUsage** cmdlet 已弃用

### <a name="get-azurermalerthistory--get-azurermautoscalehistory--get-azurermlogs"></a>**Get-AzureRmAlertHistory** / **Get-AzureRmAutoscaleHistory** / **Get-AzureRmLogs**
- 输出更改：（由这些 cmdlet 返回的）EventData 对象的字段 EventChannels 将被弃用，因为它现在返回一个常量值 (Admin,Operation)。

### <a name="get-azurermalertrule"></a>**Get-AzureRmAlertRule**
- 输出更改：此 cmdlet 的输出将平展（即取消 properties 字段）以改善用户体验。

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

### <a name="get-azurermautoscalesetting"></a>**Get-AzureRmAutoscaleSetting**
- 输出更改：AutoscaleSettingResourceName 字段将弃用，因为它始终等于 Name 字段。

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

### <a name="remove-azurermalertrule--remove-azurermlogprofile"></a>**Remove-AzureRmAlertRule** / **Remove-AzureRmLogProfile**
- 输出更改：输出类型将更改为返回内含请求 Id 和状态代码的单个对象。

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

## <a name="breaking-changes-to-network-cmdlets"></a>网络 cmdlet 的重大更改

### <a name="add-azurermapplicationgatewaysslcertificate"></a>**Add-AzureRmApplicationGatewaySslCertificate**
- 参数“Password”被替换为 SecureString

```powershell
# Old
Add-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
Add-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermapplicationgatewaysslcertificate"></a>**New-AzureRmApplicationGatewaySslCertificate**
- 参数“Password”被替换为 SecureString

```powershell
# Old
New-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
New-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermapplicationgatewaysslcertificate"></a>**Set-AzureRmApplicationGatewaySslCertificate**
- 参数“Password”被替换为 SecureString

```powershell
# Old
Set-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
Set-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-resources-cmdlets"></a>资源 cmdlet 的重大更改

### <a name="new-azurermadappcredential"></a>**New-AzureRmADAppCredential**
- 参数“Password”被替换为 SecureString

```powershell
# Old
New-AzureRmADAppCredential [other required parameters] -Password "plain-text string"

# New
New-AzureRmADAppCredential [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadapplication"></a>**New-AzureRmADApplication**
- 参数“Password”被替换为 SecureString

```powershell
# Old
New-AzureRmADApplication [other required parameters] -Password "plain-text string"

# New
New-AzureRmADApplication [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadserviceprincipal"></a>**New-AzureRmADServicePrincipal**
- 参数“Password”被替换为 SecureString

```powershell
# Old
New-AzureRmADServicePrincipal [other required parameters] -Password "plain-text string"

# New
New-AzureRmADServicePrincipal [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadspcredential"></a>**New-AzureRmADSpCredential**
- 参数“Password”被替换为 SecureString

```powershell
# Old
New-AzureRmADSpCredential [other required parameters] -Password "plain-text string"

# New
New-AzureRmADSpCredential [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermaduser"></a>**New-AzureRmADUser**
- 参数“Password”被替换为 SecureString

```powershell
# Old
New-AzureRmADUser [other required parameters] -Password "plain-text string"

# New
New-AzureRmADUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermaduser"></a>**Set-AzureRmADUser**
- 参数“Password”被替换为 SecureString

```powershell
# Old
Set-AzureRmADUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmADUser [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-servicebus-cmdlets"></a>ServiceBus cmdlet 的重大更改

### <a name="get-azurermservicebustopicauthorizationrule"></a>**Get-AzureRmServiceBusTopicAuthorizationRule**
- “Get-AzureRmServiceBusTopicAuthorizationRule”cmdlet 已删除。 请使用“Get-AzureRmServiceBusAuthorizationRule”cmdlet。    

### <a name="get-azurermservicebustopickey"></a>**Get-AzureRmServiceBusTopicKey**
- “Get-AzureRmServiceBusTopicKey”cmdlet 已删除。 请使用“Get-AzureRmServiceBusKey”cmdlet。

### <a name="new-azurermservicebustopicauthorizationrule"></a>**New-AzureRmServiceBusTopicAuthorizationRule**
- “New-AzureRmServiceBusTopicAuthorizationRule”cmdlet 已删除。 请使用“New-AzureRmServiceBusAuthorizationRule”cmdlet。

### <a name="new-azurermservicebustopickey"></a>**New-AzureRmServiceBusTopicKey**
- “New-AzureRmServiceBusTopicKey”cmdlet 已删除。 请使用“New-AzureRmServiceBusKey”cmdlet。

### <a name="remove-azurermservicebustopicauthorizationrule"></a>**Remove-AzureRmServiceBusTopicAuthorizationRule**
- “Remove-AzureRmServiceBusTopicAuthorizationRule”cmdlet 已删除。 请使用“Remove-AzureRmServiceBusAuthorizationRule”cmdlet。

### <a name="set-azurermservicebustopicauthorizationrule"></a>**Set-AzureRmServiceBusTopicAuthorizationRule**
- “Set-AzureRmServiceBusTopicAuthorizationRule”cmdlet 已删除。 请使用“Set-AzureRmServiceBusAuthorizationRule”cmdlet。

### <a name="new-azurermservicebusnamespacekey"></a>**New-AzureRmServiceBusNamespaceKey**
- “New-AzureRmServiceBusNamespaceKey”cmdlet 已删除。 请使用“New-AzureRmServiceBusKey”cmdlet。

### <a name="get-azurermservicebusqueueauthorizationrule"></a>**Get-AzureRmServiceBusQueueAuthorizationRule**
- “Get-AzureRmServiceBusQueueAuthorizationRule”cmdlet 已删除。 请使用“Get-AzureRmServiceBusAuthorizationRule”cmdlet。

### <a name="get-azurermservicebusqueuekey"></a>**Get-AzureRmServiceBusQueueKey**
- “Get-AzureRmServiceBusQueueKey”cmdlet 已删除。 请使用“Get-AzureRmServiceBusKey”cmdlet。

### <a name="new-azurermservicebusqueueauthorizationrule"></a>**New-AzureRmServiceBusQueueAuthorizationRule**
- “New-AzureRmServiceBusQueueAuthorizationRule”cmdlet 已删除。 请使用“New-AzureRmServiceBusAuthorizationRule”cmdlet。

### <a name="new-azurermservicebusqueuekey"></a>**New-AzureRmServiceBusQueueKey**
- “New-AzureRmServiceBusQueueKey”cmdlet 已删除。 请使用“New-AzureRmServiceBusKey”cmdlet。

### <a name="remove-azurermservicebusqueueauthorizationrule"></a>**Remove-AzureRmServiceBusQueueAuthorizationRule**
- “Remove-AzureRmServiceBusQueueAuthorizationRule”cmdlet 已删除。 请使用“GRemove-AzureRmServiceBusAuthorizationRule”cmdlet。

### <a name="set-azurermservicebusqueueauthorizationrule"></a>**Set-AzureRmServiceBusQueueAuthorizationRule**
- “Set-AzureRmServiceBusQueueAuthorizationRule”cmdlet 已删除。 请使用“Set-AzureRmServiceBusAuthorizationRule”cmdlet。

### <a name="get-azurermservicebusnamespaceauthorizationrule"></a>**Get-AzureRmServiceBusNamespaceAuthorizationRule**
- “Get-AzureRmServiceBusNamespaceAuthorizationRule”cmdlet 已删除。 请使用“Get-AzureRmServiceBusAuthorizationRule”cmdlet。

### <a name="get-azurermservicebusnamespacekey"></a>**Get-AzureRmServiceBusNamespaceKey**
- “Get-AzureRmServiceBusNamespaceKey”cmdlet 已删除。 请使用“Get-AzureRmServiceBusKey”cmdlet。

### <a name="new-azurermservicebusnamespaceauthorizationrule"></a>**New-AzureRmServiceBusNamespaceAuthorizationRule**
- “New-AzureRmServiceBusNamespaceAuthorizationRule”cmdlet 已删除。 请使用“New-AzureRmServiceBusAuthorizationRule”cmdlet。

### <a name="remove-azurermservicebusnamespaceauthorizationrule"></a>**Remove-AzureRmServiceBusNamespaceAuthorizationRule**
- “Remove-AzureRmServiceBusNamespaceAuthorizationRule”cmdlet 已删除。 请使用“Remove-AzureRmServiceBusAuthorizationRule”cmdlet。

### <a name="set-azurermservicebusnamespaceauthorizationrule"></a>**Set-AzureRmServiceBusNamespaceAuthorizationRule**
- “Set-AzureRmServiceBusNamespaceAuthorizationRule”cmdlet 已删除。 请使用“Set-AzureRmServiceBusAuthorizationRule”cmdlet。

### <a name="type-namespaceattributes"></a>**类型 NamespaceAttributes**
- 以下属性已删除
    - Enabled
    - Status
   
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

### <a name="type-queueattribute"></a>**类型 QueueAttribute**
- 以下属性标记为已过时：
    - EnableBatchedOperations
    - EntityAvailabilityStatus
    - IsAnonymousAccessible
    - SupportOrdering

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
   
### <a name="type-topicattribute"></a>**类型 TopicAttribute**
- 以下属性标记为已过时：
    - Location
    - IsExpress
    - IsAnonymousAccessible
    - FilteringMessagesBeforePublishing
    - EnableSubscriptionPartitioning
    - EntityAvailabilityStatus

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
   
### <a name="type-subscriptionattribute"></a>**类型 SubscriptionAttribute**
- 以下属性标记为已过时
    - DeadLetteringOnFilterEvaluationExceptions
    - EntityAvailabilityStatus
    - IsReadOnly
    - Location
   
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