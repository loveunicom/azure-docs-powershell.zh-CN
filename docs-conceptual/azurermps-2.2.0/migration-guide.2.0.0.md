# <a name="table-of-contents"></a>目录
1. [Force 参数的删除](#removal-of-force-parameters)
2. [Tag 参数的更改](#change-of-tag-parameters)
3. [存储 cmdlet 的重大更改](#breaking-changes-to-storage-cmdlets)
4. [AD cmdlet 的重大更改](#breaking-changes-to-ad-cmdlets)

## <a name="removal-of-force-parameters"></a>Force 参数的删除

在此版本中，我们从 cmdlet 中删除了所有已过时的 `Force` 参数，并且在将来的版本中将删除与此参数相关的相应警告。

此更改影响以下 cmdlet:

**ApiManagement**
- Remove-AzureRmApiManagement
- Remove-AzureRmApiManagementApi
- Remove-AzureRmApiManagementGroup
- Remove-AzureRmApiManagementLogger
- Remove-AzureRmApiManagementOpenIdConnectProvider
- Remove-AzureRmApiManagementOperation
- Remove-AzureRmApiManagementPolicy
- Remove-AzureRmApiManagementProduct
- Remove-AzureRmApiManagementProperty
- Remove-AzureRmApiManagementSubscription
- Remove-AzureRmApiManagementUser

**自动化**
- Remove-AzureRmAutomationCertificate
- Remove-AzureRmAutomationCredential
- Remove-AzureRmAutomationVariable
- Remove-AzureRmAutomationWebhook

**批处理**
- Remove-AzureBatchCertificate
- Remove-AzureBatchComputeNode
- Remove-AzureBatchComputeNodeUser

**DataFactories**
- Resume-AzureRmDataFactoryPipeline
- Set-AzureRmDataFactoryPipelineActivePeriod
- Suspend-AzureRmDataFactoryPipeline

**DataLakeStore**
- Remove-AzureRmDataLakeStoreItemAclEntry
- Set-AzureRmDataLakeStoreItemAcl
- Set-AzureRmDataLakeStoreItemAclEntry
- Set-AzureRmDataLakeStoreItemOwner

**OperationalInsights**
- Remove-AzureRmOperationalInsightsSavedSearch

**配置文件**
- Remove-AzureRmEnvironment

**RedisCache**
- Remove-AzureRmRedisCacheDiagnostics

**资源**
- Register-AzureRmProviderFeature
- Register-AzureRmResourceProvider
- Remove-AzureRmADServicePrincipal
- Remove-AzureRmPolicyAssignment
- Remove-AzureRmResourceGroupDeployment
- Remove-AzureRmRoleAssignment
- Stop-AzureRmResourceGroupDeployment
- Unregister-AzureRmResourceProvider

**存储**
- Remove-AzureStorageContainerStoredAccessPolicy
- Remove-AzureStorageQueueStoredAccessPolicy
- Remove-AzureStorageShareStoredAccessPolicy
- Remove-AzureStorageTableStoredAccessPolicy

**StreamAnalytics**
- Remove-AzureRmStreamAnalyticsFunction
- Remove-AzureRmStreamAnalyticsInput
- Remove-AzureRmStreamAnalyticsJob
- Remove-AzureRmStreamAnalyticsOutput

**标记**
- Remove-AzureRmTag

<br>

如果具有使用以上任一 cmdlet 的脚本，则只需删除 `Force` 参数便可适应此重大更改。

```powershell
# Old
New-AzureRmResourceGroup -Name $resourceGroupName -Location $location -Force

# New
New-AzureRmResourceGroup -Name $resourceGroupName -Location $location
```

<br>

## <a name="change-of-tag-parameters"></a>Tag 参数的更改

在此版本中，`Tags` 参数名称已更改为 `Tag`，并且类型已从 `Hashtable[]` 更改为 `Hashtable`，更改了键-值对的格式。

以前，`Hashtable[]` 中的每个条目表示单个键-值对：

```powershell
$tags = @{ Name = "test1"; Value = "testval1" }, @{ Name = "test2", Value = "testval2" }
$tags[0].Name  # Key for the first entry, "test1"
$tags[0].Value # Value for the first entry, "testval1"
$tags[1].Name  # Key for the second entry, "test2"
$tags[1].Value # Value for the second entry, "testval2"
```

现在，`Name` 和 `Value` 不再是必需的，允许通过在 `Hashtable` 中分配 `Key = "Value"` 来创建键-值对：

```powershell
$tag = @{ test1 = "testval1"; test2 = "testval2" }
$tag["test1"] # Gets the value associated with the key "test1"
$tag["test2"] # Gets the value associated with the key "test2"
```

此更改影响以下 cmdlet:

**批处理**
- Get-AzureRmBatchAccount
- New-AzureRmBatchAccount
- Set-AzureRmBatchAccount

**计算**
- New-AzureRmVM
- Update-AzureRmVM

**DataLakeAnalytics**
- New-AzureRmDataLakeAnalyticsAccount
- Set-AzureRmDataLakeAnalyticsAccount

**DataLakeStore**
- New-AzureRmDataLakeStoreAccount
- Set-AzureRmDataLakeStoreAccount

**Dns**
- New-AzureRmDnsZone
- Set-AzureRmDnsZone

**KeyVault**
- Get-AzureRmKeyVault
- New-AzureRmKeyVault

**网络**
- New-AzureRmApplicationGateway
- New-AzureRmExpressRouteCircuit
- New-AzureRmLoadBalancer
- New-AzureRmLocalNetworkGateway
- New-AzureRmNetworkInterface
- New-AzureRmNetworkSecurityGroup
- New-AzureRmPublicIpAddress
- New-AzureRmRouteTable
- New-AzureRmVirtualNetwork
- New-AzureRmVirtualNetworkGateway
- New-AzureRmVirtualNetworkGatewayConnection
- New-AzureRmVirtualNetworkPeering

**资源**
- Find-AzureRmResource
- Find-AzureRmResourceGroup
- New-AzureRmResource
- New-AzureRmResourceGroup
- Set-AzureRmResource
- Set-AzureRmResourceGroup

**SQL**
- New-AzureRmSqlDatabase
- New-AzureRmSqlDatabaseCopy
- New-AzureRmSqlDatabaseSecondary
- New-AzureRmSqlElasticPool
- New-AzureRmSqlServer
- Set-AzureRmSqlDatabase
- Set-AzureRmSqlElasticPool
- Set-AzureRmSqlServer

**存储**
- New-AzureRmStorageAccount
- Set-AzureRmStorageAccount

**TrafficManager**
- New-AzureRmTrafficManagerProfile

<br>

如果具有使用以上任一 cmdlet 的脚本，则可以通过将 `Tags` 参数更改为 `Tag` 以及将 `Tag` 更改为新格式来适应此重大更改。

```powershell
# Old
New-AzureRmResourceGroup -Name $resourceGroupName -Location -location -Tags @{ Name = "testtag"; Value = "testval" }

# New
New-AzureRmResourceGroup -Name $resourceGroupName -Location -location -Tag @{ testtag = "testval" }
```

<br>

## <a name="breaking-changes-to-storage-cmdlets"></a>存储 cmdlet 的重大更改

此版本影响以下 cmdlet：

**Get-AzureRmStorageAccountKey**
- 此 cmdlet 现在返回一个键列表，而非包含每个键的属性的对象

```powershell
# Old
$key = (Get-AzureRmStorageAccountKey -ResourceGroupName $resourceGroupName -Name $accountName).Key1

# New
$key = (Get-AzureRmStorageAccountKey -ResourceGroupName $resourceGroupName -Name $accountName)[0].Value
```

**New-AzureRmStorageAccountKey**
- 此 cmdlet 的输出中的 `StorageAccountRegenerateKeyResponse` 字段已重命名为 `StorageAccountListKeysResults`，它现在是一个键列表而非包含每个键的属性的对象

```powershell
# Old
$key = (New-AzureRmStorageAccountKey -ResourceGroupName $resourceGroupName -Name $accountName).StorageAccountKeys.Key1

# New
$key = (New-AzureRmStorageAccountKey -ResourceGroupName $resourceGroupName -Name $accountName).Keys[0].Value
```

**New/Get/Set-AzureRmStorageAccount**
- 此 cmdlet 的输出中的 `AccountType` 字段已重名为 `Sku.Name`
- PrimaryEndpoints/Secondary 终结点 blob/table/queue/file 的输出类型已从 `Uri` 更改为 `String`

```powershell
# Old
$accountType = (Get-AzureRmStorageAccount -ResourceGroupName $resourceGroupName -Name $accountName).AccountType

# New
$accountType = (Get-AzureRmStorageAccount -ResourceGroupName $resourceGroupName -Name $accountName).Sku.Name
```

```powershell
# Old 
$blobEndpoint = (Get-AzureRmStorageAccount -ResourceGroupName $resourceGroupName -Name $accountName).PrimaryEndpoints.Blob.ToString()
$blobEndpoint = (Get-AzureRmStorageAccount -ResourceGroupName $resourceGroupName -Name $accountName).PrimaryEndpoints.Blob.AbsolutePath

# New
$blobEndpoint = (Get-AzureRmStorageAccount -ResourceGroupName $resourceGroupName -Name $accountName).PrimaryEndpoints.Blob.ToString()
$blobEndpoint = (Get-AzureRmStorageAccount -ResourceGroupName $resourceGroupName -Name $accountName).PrimaryEndpoints.Blob
```

<br>

## <a name="breaking-changes-to-ad-cmdlets"></a>AD cmdlet 的重大更改

此版本影响以下 cmdlet：

**Get-AzureRMADServicePrincipal**
- 此 cmdlet 的输出中的 `ServicePrincipalName` 字段已重名为 `ServicePrincipalNames`，并且现在是一个集合。 它现在还将 `ApplicationId` 显示为 SPN 和 identifierUri 之一。

```powershell
# Old
$servicePrincipals = Get-AzureRmADServicePrincipal -SearchString $displayName
$spn = $servicePrincipals[0].ServicePrincipalName

# New
$servicePrincipals = Get-AzureRmADServicePrincipal -SearchString $displayName
$spn = $servicePrincipals[0].ServicePrincipalNames[0]
```

**Get-AzureRmADApplication**
- 参数 `ApplicationObjectId` 已重命名为 `ObjectId`。
- 在此 cmdlet 的输出中，`ApplicationObjectId` 已重名为 `ObjectId`。

```powershell
# Old
$app = Get-AzureRmADApplication -ApplicationObjectId $applicationObjectId
$objectId = $app.ApplicationObjectId

# New
$app = Get-AzureRmADApplication -ObjectId $objectId
$objectId = $app.ObjectId
```

**Remove-AzureRmADApplication**
- 参数 `ApplicationObjectId` 已重命名为 `ObjectId`。

```powershell
# Old
$app = Remove-AzureRmADApplication -ApplicationObjectId $applicationObjectId -Force

# New
$app = Remove-AzureRmADApplication -ObjectId $objectId -Force
```

**New-AzureRmADApplication**
- 在此 cmdlet 的输出中，`ApplicationObjectId` 已重名为 `ObjectId`。
- `KeyValue`、`KeyUsage`、`KeyType` 参数已删除。

```powershell
# Old
$app = New-AzureRmADApplication -DisplayName $displayName -HomePage $homePage -IdentifierUris $identifierUris -KeyValue $kv -KeyType $kt -KeyUsage $ku
$id = $app.ApplicationObjectId

# New
$app = New-AzureRmADApplication -DisplayName $displayName -HomePage $homePage -IdentifierUris $identifierUris
$id = $app.ObjectId
New-AzureRmADAppCredential -ObjectId $id -Password $kv
```

**Get-AzureRmADGroup**
- `Mail` 字段已从输出中删除。

**Get-AzureRmADUser**
- `Mail` 字段已从输出中删除。

**New-AzureRmADServicePrincipal**
- 删除了 `DisableAccount` 参数。

```powershell
# Old
$servicePrincipal = New-AzureRmADServicePrincipal -DisplayName $displayName -Password $password -DisableAccount true

# New
$servicePrincipal = New-AzureRmADServicePrincipal -DisplayName $displayName -Password $password
Remove-AzureRmADServicePrincipal -ObjectId $servicePrincipal.ObjectId
```