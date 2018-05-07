# <a name="breaking-changes-for-microsoft-azure-powershell-400"></a>Microsoft Azure PowerShell 4.0.0 的重大更改

本文档是面向 Microsoft Azure PowerShell cmdlet 的使用者的重大更改通知和迁移指南。 每部分都介绍了重大更改的影响和最简便的迁移路径。 有关深入的上下文，请参考与每个更改关联的拉取请求。

## <a name="table-of-contents"></a>目录

- [计算 cmdlet 的重大更改](#breaking-changes-to-compute-cmdlets)
- [EventHub cmdlet 的重大更改](#breaking-changes-to-eventhub-cmdlets)
- [见解 cmdlet 的重大更改](#breaking-changes-to-insights-cmdlets)
- [网络 cmdlet 的重大更改](#breaking-changes-to-network-cmdlets)
- [ServiceBus cmdlet 的重大更改](#breaking-changes-to-servicebus-cmdlets)
- [Sql cmdlet 的重大更改](#breaking-changes-to-sql-cmdlets)
- [存储 cmdlet 的重大更改](#breaking-changes-to-storage-cmdlets)
- [配置文件 cmdlet 的重大更改](#breaking-changes-to-profile-cmdlets)
## <a name="breaking-changes-to-compute-cmdlets"></a>计算 cmdlet 的重大更改

此版本影响以下输出类型：

### <a name="psvirtualmachine"></a>PSVirtualMachine
- `PSVirtualMachine` 对象的顶级属性 `DataDiskNames` 和 `NetworkInterfaceIDs` 已从输出类型中删除。 这些属性始终在 `PSVirtualMachine` 对象的 `StorageProfile` 和 `NetworkProfile` 属性中提供，并且以后这将是访问它们时需要使用的方式。
- 此更改影响以下 cmdlet:
    - `Add-AzureRmVMDataDisk`
    - `Add-AzureRmVMNetworkInterface`
    - `Get-AzureRmVM`
    - `Remove-AzureRmVMDataDisk`
    - `Remove-AzureRmVMNetworkInterface`
    - `Set-AzureRmVMDataDisk`

```powershell
# Old
$vm.DataDiskNames
$vm.NetworkInterfaceIDs

# New
$vm.StorageProfile.DataDisks | Select -Property Name
$vm.NetworkProfile.NetworkInterfaces | Select -Property Id
```

## <a name="breaking-changes-to-eventhub-cmdlets"></a>EventHub cmdlet 的重大更改

此版本影响以下 cmdlet：

### <a name="get-azurermeventhubnamespace"></a>Get-AzureRmEventHubNamespace
- 属性 `ResourceGroupName` 已从输出类型 `NamespaceAttributes` 中删除

### <a name="new-azurermeventhubnamespace"></a>New-AzureRmEventHubNamespace
- 属性 `ResourceGroupName` 已从输出类型 `NamespaceAttributes` 中删除

## <a name="breaking-changes-to-insights-cmdlets"></a>见解 cmdlet 的重大更改

此版本影响以下 cmdlet：
    
### <a name="get-azurermusage"></a>Get-AzureRmUsage
- 此 cmdLet 已弃用。

### <a name="remove-azurermalertrule"></a>Remove-AzureRmAlertRule
- 此 cmdlet 的输出已从内含单个对象的列表更改为单个对象；此对象包括 requestId 和状态代码。
    
```powershell
# Old  
$s1 = Remove-AzureRmAlertRule -ResourceGroup $resourceGroup -name chiricutin
if ($s1 -ne $null)
{
    $r = $s1(0).RequestId
    $s = $s1(0).StatusCode
}

# New
$s1 = Remove-AzureRmAlertRule -ResourceGroup $resourceGroup -name chiricutin
$r = $s1.RequestId
$s = $s1.StatusCode
```
    
### <a name="add-azurermlogalertrule"></a>Add-AzureRmLogAlertRule
- 此 cmdLet 已弃用。
    
### <a name="get-azurermalertrule"></a>Get-AzureRmAlertRule
- 此 cmdlet 的输出（一个对象列表）的每个元素都是平展的，也就是说，它不采用结构 `{ Id, Location, Name, Tags, Properties }` 返回对象，而是将采用结构 `{ Id, Location, Name, Tags, Type, Description, IsEnabled, Condition, Actions, LastUpdatedTime, ...}` 返回对象，这是 Azure 资源的所有属性外加 AlertRuleResource 顶层的所有属性。
    
```powershell
# Old
$rules = Get-AzureRmAlertRule -ResourceGroup $resourceGroup
if ($rules -and $rules.count -ge 1)
{
    Write-Host -fore red "Error updating alert rule"
      
    Write-Host $rules(0).Id
    Write-Host $rules(0).Properties.IsEnabled
    Write-Host $rules(0).Properties.Condition
}

# New
$rules = Get-AzureRmAlertRule -ResourceGroup $resourceGroup
if ($rules -and $rules.count -ge 1)
{
    Write-Host -fore red "Error updating alert rule"
 
    Write-Host $rules(0).Id
      
    # Properties will remain for a while
    Write-Host $rules(0).Properties.IsEnabled
      
    # But the properties will be at the top level too. Later Properties will be removed
    Write-Host $rules(0).IsEnabled
    Write-Host $rules(0).Condition
}
```
    
### <a name="get-azurermautoscalesetting"></a>Get-AzureRmAutoscaleSetting
- `AutoscaleSettingResourceName` 字段已弃用，因为它始终具有与 `Name` 字段相同的值。

```powershell
# Old  
$s1 = Get-AzureRmAutoscaleSetting -ResourceGroup $resourceGroup -Name MySetting
if ($s1.AutoscaleSettingResourceName -ne $s1.Name)
{
    Write-Host "There is something wrong with the name"
}

# New
$s1 = Get-AzureRmAutoscaleSetting -ResourceGroup $resourceGroup -Name MySetting
    
# There won't be a AutoscaleSettingResourceName
Write-Host $s1.Name
```
    
### <a name="remove-azurermlogprofile"></a>Remove-AzureRmLogProfile
- 此 cmdlet 的输出将从 `Boolean` 更改为包含 `RequestId` 和 `StatusCode` 的对象

```powershell
# Old  
$s1 = Remove-AzureRmLogProfile -Name myLogProfile
if ($s1 -eq $true)
{
    Write-Host "Removed"
}
else
{
    Write-Host "Failed"
}

# New
$s1 = Remove-AzureRmLogProfile -Name myLogProfile
$r = $s1.RequestId
$s = $s1.StatusCode
```
    
### <a name="add-azurermlogprofile"></a>Add-AzureRmLogProfile
- 此 cmdlet 的输出将从包含 requestId 的对象更改为包含 requestId、状态代码以及更新的或新建的资源的对象
    
```powershell
# Old  
$s1 = Add-AzureRmLogProfile -Name default -StorageAccountId /subscriptions/df602c9c-7aa0-407d-a6fb-eb20c8bd1192/resourceGroups/JohnKemTest/providers/Microsoft.Storage/storageAccounts/johnkemtest8162 -Locations Global -categ Delete, Write, Action -retention 3
$r = $s1.ServiceBusRuleId

# New
$s1 = Add-AzureRmLogProfile -Name default -StorageAccountId /subscriptions/df602c9c-7aa0-407d-a6fb-eb20c8bd1192/resourceGroups/JohnKemTest/providers/Microsoft.Storage/storageAccounts/johnkemtest8162 -Locations Global -categ Delete, Write, Action -retention 3
$r = $s1.RequestId
$s = $s1.StatusCode
$a = $s1.NewResource.ServiceBusRuleId
    
```
    
### <a name="set-azurermdiagnosticsettings"></a>Set-AzureRmDiagnosticSettings
- 此命令将重命名为 `Update-AzureRmDiagnsoticSettings`

```powershell
# Old
Set-AzureRmDiagnosticSettings

# New
Update-AzureRmDiagnosticSettings
```

## <a name="breaking-changes-to-network-cmdlets"></a>网络 cmdlet 的重大更改

此版本影响以下 cmdlet：

### <a name="new-azurermvirtualnetworkgatewayconnection"></a>New-AzureRmVirtualNetworkGatewayConnection
- `EnableBgp` 参数已更改为采用 `boolean` 而非 `string`

```powershell
# Old
New-AzureRmVirtualNetworkGatewayConnection -ResourceGroupName "RG" -name "conn1" -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -SharedKey "key" -EnableBgp "true"

# New
New-AzureRmVirtualNetworkGatewayConnection -ResourceGroupName "RG" -name "conn1" -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -SharedKey "key" -EnableBgp $true
```

## <a name="breaking-changes-to-servicebus-cmdlets"></a>ServiceBus cmdlet 的重大更改

此版本影响以下 cmdlet：

### <a name="get-azurermservicebusnamespace"></a>Get-AzureRmServiceBusNamespace
- 属性 `ResourceGroupName` 已从输出类型 `NamespaceAttributes` 中删除

### <a name="new-azurermservicebusnamespace"></a>New-AzureRmServiceBusNamespace

- 属性 `ResourceGroupName` 已从输出类型 `NamespaceAttributes` 中删除

## <a name="breaking-changes-to-sql-cmdlets"></a>Sql cmdlet 的重大更改

此版本影响以下 cmdlet：

### <a name="new-azurermsqldatabasefailovergroup"></a>New-AzureRmSqlDatabaseFailoverGroup
- `Tag` 参数已删除
- `GracePeriodWithDataLossHour` 参数已重命名为 `GracePeriodWithDataLossHours`

```powershell
# Old
New-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -FailoverPolicy Automatic -GracePeriodWithDataLossHour 1 -Tag @{ Environment="Test" }

# New
New-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

### <a name="set-azurermsqldatabasefailovergroup"></a>Set-AzureRmSqlDatabaseFailoverGroup
- `Tag` 参数已删除
- `GracePeriodWithDataLossHour` 参数已重命名为 `GracePeriodWithDataLossHours`

```powershell
# Old
Set-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHour 1 -Tag @{ Environment="Test" }

# New
Set-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

### <a name="add-azurermsqldatabasetofailovergroup"></a>Add-AzureRmSqlDatabaseToFailoverGroup
- `Tag` 参数已删除

```powershell
# Old
Add-AzureRmSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1 -Tag @{ Environment="Test" }

# New
Add-AzureRmSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1
```

###  <a name="remove-azurermsqldatabasefromfailovergroup"></a>Remove-AzureRmSqlDatabaseFromFailoverGroup
- `Tag` 参数已删除

```powershell
# Old
Remove-AzureRmSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1 -Tag @{ Environment="Test" }

# New
Remove-AzureRmSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1
```

### <a name="remove-azurermsqldatabasefailovergroup"></a>Remove-AzureRmSqlDatabaseFailoverGroup
- `PartnerResourceGroupName` 参数已删除
- `PartnerServerName` 参数已删除

```powershell
# Old
Remove-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -PartnerResourceGroupName rg

# New
Remove-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg
```

### <a name="set-azurermsqldatabasethreatdetectionpolicy"></a>Set-AzureRmSqlDatabaseThreatDetectionPolicy
- 值 `Usage_Anomaly` 对参数 `ExcludedDetectionType` 不再有效

### <a name="set-azurermsqlserverthreatdetectionpolicy"></a>Set-AzureRmSqlServerThreatDetectionPolicy
- 值 `Usage_Anomaly` 对参数 `ExcludedDetectionType` 不再有效

## <a name="breaking-changes-to-storage-cmdlets"></a>存储 cmdlet 的重大更改

此版本影响以下输出类型属性：

### <a name="azurestorageblobicloudblobserviceclient"></a>AzureStorageBlob.ICloudBlob.ServiceClient
- 以下属性已从此类型中删除（_注意_：它们仍然存在于 `DefaultRequestOptions` 属性中）：
    - `LocationMode`
    - `MaximumExecutionTime`
    - `ServerTimeout`
    - `ParallelOperationThreadCount`
    - `SingleBlobUploadThresholdInBytes`
- 此更改影响以下 cmdlet:
    - `Get-AzureStorageBlob`
    - `Get-AzureStorageBlobContent`
    - `Get-AzureStorageBlobCopyState`
    - `Set-AzureStorageBlobContent`
    - `Start-AzureStorageBlobCopy`
    - `Stop-AzureStorageBlobCopy`
    
### <a name="azurestoragecontainercloudblobcontainerserviceclient"></a>AzureStorageContainer.CloudBlobContainer.ServiceClient
- 以下属性已从此类型中删除（_注意_：它们仍然存在于 `DefaultRequestOptions` 属性中）：
    - `LocationMode`
    - `MaximumExecutionTime`
    - `ServerTimeout`
    - `ParallelOperationThreadCount`
    - `SingleBlobUploadThresholdInBytes`
- 此更改影响以下 cmdlet:
    - `Get-AzureStorageContainer`
    - `New-AzureStorageContainer`
    - `Set-AzureStorageContainerAcl`
    
### <a name="azurestoragequeuecloudqueueserviceclient"></a>AzureStorageQueue.CloudQueue.ServiceClient
- 以下属性已从此类型中删除（_注意_：它们仍然存在于 `DefaultRequestOptions` 属性中）：
    - `LocationMode`
    - `MaximumExecutionTime`
    - `RetryPolicy`
    - `ServerTimeout`
- 此更改影响以下 cmdlet:
    - `Get-AzureStorageQueue`
    - `New-AzureStorageQueue`
    
### <a name="azurestoragetablecloudtableserviceclient"></a>AzureStorageTable.CloudTable.ServiceClient
- 以下属性已从此类型中删除（_注意_：它们仍然存在于 `DefaultRequestOptions` 属性中）：
    - `LocationMode`
    - `MaximumExecutionTime`
    - `PayloadFormat`
    - `RetryPolicy`
    - `ServerTimeout`
- 此更改影响以下 cmdlet:
    - `Get-AzureStorageTable`
    - `New-AzureStorageTable`
    
```powershell
# Old
$LocationMode = (Get-AzureStorageBlob -Container $containername)[0].ICloudBlob.ServiceClient.LocationMode       
$ParallelOperationThreadCount = (Get-AzureStorageContainer -Container $containername).CloudBlobContainer.ServiceClient.ParallelOperationThreadCount
$PayloadFormat = (Get-AzureStorageTable -Name $tablename).CloudTable.ServiceClient.PayloadFormat
$RetryPolicy = (Get-AzureStorageQueue -Name $queuename).CloudQueue.ServiceClient.RetryPolicy

# New
$LocationMode = (Get-AzureStorageBlob -Container $containername)[0].ICloudBlob.ServiceClient.DefaultRequestOptions.LocationMode     
$ParallelOperationThreadCount = (Get-AzureStorageContainer -Container $containername).CloudBlobContainer.ServiceClient.DefaultRequestOptions.ParallelOperationThreadCount
$PayloadFormat = (Get-AzureStorageTable -Name $tablename).CloudTable.ServiceClient.DefaultRequestOptions.PayloadFormat
$RetryPolicy = (Get-AzureStorageQueue -Name $queuename).CloudQueue.ServiceClient.DefaultRequestOptions.RetryPolicy
```

## <a name="breaking-changes-to-profile-cmdlets"></a>配置文件 cmdlet 的重大更改

以下 cmdlet 和 cmdlet 输出类型在此版本中已更改。

### <a name="add-azurermaccount-breaking-changes"></a>Add-AzureRmAccount 重大更改

- ```EnvironmentName``` 参数已删除并替换为 ```Environment```，```Environment``` 现在采用字符串而非 ```AzureEnvironment``` 对象

```powershell
# Old
Add-AzureRmAccount -EnvironmentName AzureChinaCloud

# New
Add-AzureRmAccount -Environment AzureChinaCloud
```

### <a name="select-azurermprofile-was-renamed-to-import-azurermcontext"></a>Select-AzureRmProfile 已重命名为 Import-AzureRmContext

```Select-AzureRmProfile``` 已重命名为 ```Import-AzureRmContext```

```powershell
# Old
Select-AzureRmProfile -Path c:\mydir\myprofile.json

# New
Import-AzureRmContext -Path c:\mydir\myprofile.json
```

### <a name="save-azurermprofile-was-renamed-to-save-azurermcontext"></a>Save-AzureRmProfile 已重命名为 Save-AzureRmContext

```Save-AzureRmProfile``` 已重命名为 ```Save-AzureRmContext```

```powershell
# Old
Save-AzureRmProfile -Path c:\mydir\myprofile.json

# New
Save-AzureRmContext -Path c:\mydir\myprofile.json
```
### <a name="breaking-changes-to-output-psazurecontext-type"></a>输出 PSAzureContext 类型的重大更改

- ```TokenCache``` 属性已更改为实现 ```IAzureTokenCache``` 而非 ```byte[]``` 的类型

```powershell
# Old
$bytes = (Get-AzureRmContext).TokenCache
$bytes = (Set-AzureRmContext -SubscriptionId xxx-xxx-xxx-xxx).TokenCache
$bytes = (Add-AzureRmAccount).Context.TokenCache

# New
$bytes = (Get-AzureRmContext).TokenCache.CacheData
$bytes = (Set-AzureRmContext -SubscriptionId xxx-xxx-xxx-xxx).TokenCache.CacheData
$bytes = (Add-AzureRmAccount).Context.TokenCache.CacheData
```

### <a name="breaking-changes-to-the-output-psazureaccount-type"></a>输出 PSAzureAccount 类型的重大更改

- ```AccountType``` 属性已更改为 ```Type```

```powershell
# Old
$type = (Get-AzureRmContext).Account.AccountType
$type = (Set-AzureRmContext -SubscriptionId xxx-xxx-xxx-xxx).Account.AccountType
$type = (Add-AzureRmAccount).Context.Account.AccountType

# New 
$type = (Get-AzureRmContext).Account.Type
$type = (Set-AzureRmContext -SubscriptionId xxx-xxx-xxx-xxx).Account.Type
$type = (Add-AzureRmAccount).Context.Account.Type
```

### <a name="breaking-changes-to-the-output-psazuresubscription-type"></a>输出 PSAzureSubscription 类型的重大更改
- ```SubscriptionId``` 属性已更改为 ```Id```

```powershell
# Old
$id =(Get-AzureRmSubscription -SubscriptionId xxxx-xxxx-xxxx-xxxx).SubscriptionId
$id =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Subscription.SubscriptionId
$id =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.SubscriptionId
$id =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.SubscriptionId

# New
$id =(Get-AzureRmSubscription -SubscriptionId xxxx-xxxx-xxxx-xxxx).Id
$id =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Subscription.Id
$id =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.Id
$id =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.Id
```

- ```SubscriptionName``` 属性已更改为 ```Name```

```powershell
# Old
$name =(Get-AzureRmSubscription -SubscriptionId xxxx-xxxx-xxxx-xxxx).SubscriptionName
$name =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Subscription.SubscriptionName
$name =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.SubscriptionName
$name =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.SubscriptionName

# New
$name =(Get-AzureRmSubscription -SubscriptionId xxxx-xxxx-xxxx-xxxx).Name
$name =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Subscription.Name
$name =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.Name
$name =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.Name
```

### <a name="breaking-changes-to-the-output-psazuretenant-type"></a>输出 PSAzureTenant 类型的重大更改

- ```TenantId``` 属性已更改为 ```Id```

```powershell
# Old
$id =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).TenantId
$id =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Tenant.TenantId
$id =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Tenant.TenantId
$id =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Tenant.TenantId

# New
$id =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).Id
$id =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Tenant.Id
$id =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Tenant.Id
$id =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Tenant.Id
```

- ```Domain``` 属性已更改为 ```Directory```

```powershell
# Old
$tenantName =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).Domain

# New
$tenantName =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).Directory
```
