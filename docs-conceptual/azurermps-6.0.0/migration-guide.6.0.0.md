---
title: Microsoft Azure PowerShell 6.0.0 的重大更改
description: 本迁移指南包含一个列表，列出了在发行的第 6 版中对 Azure PowerShell 所做的重大更改。
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 5/1/2018
ms.openlocfilehash: dc88ba8a2359e92cb3aa9c3e891463e70143ddb4
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/08/2018
ms.locfileid: "33912099"
---
# <a name="breaking-changes-for-microsoft-azure-powershell-600"></a>Microsoft Azure PowerShell 6.0.0 的重大更改

本文档是面向 Microsoft Azure PowerShell cmdlet 的使用者的重大更改通知和迁移指南。 每部分都介绍了重大更改的影响和最简便的迁移路径。 有关深入的上下文，请参考与每个更改关联的拉取请求。

## <a name="table-of-contents"></a>目录

- [常规重大更改](#general-breaking-changes)
    - [PowerShell 最低版本要求升至 5.0](#minimum-powershell-version-required-bumped-to-50)
    - [默认启用上下文自动保存功能](#context-autosaved-enabled-by-default)
    - [删除标记别名](#removal-of-tags-alias)
- [AzureRM.Compute cmdlet 的重大更改](#breaking-changes-to-azurermcompute-cmdlets)
- [AzureRM.DataLakeStore cmdlet 的重大更改](#breaking-changes-to-azurermdatalakestore-cmdlets)
- [AzureRM.Dns cmdlet 的重大更改](#breaking-changes-to-azurermdns-cmdlets)
- [AzureRM.Insights cmdlet 的重大更改](#breaking-changes-to-azurerminsights-cmdlets)
- [AzureRM.KeyVault cmdlet 的重大更改](#breaking-changes-to-azurermkeyvault-cmdlets)
- [AzureRM.Network cmdlet 的重大更改](#breaking-changes-to-azurermnetwork-cmdlets)
- [AzureRM.RedisCache cmdlet 的重大更改](#breaking-changes-to-azurermrediscache-cmdlets)
- [AzureRM.Resources cmdlet 的重大更改](#breaking-changes-to-azurermresources-cmdlets)
- [AzureRM.Storage cmdlet 的重大更改](#breaking-changes-to-azurermstorage-cmdlets)
- [删除的模块](#removed-modules)
    - [`AzureRM.ServerManagement`](#azurermservermanagement)
    - [`AzureRM.SiteRecovery`](#azurermsiterecovery)

## <a name="general-breaking-changes"></a>常规重大更改

### <a name="minimum-powershell-version-required-bumped-to-50"></a>PowerShell 最低版本要求升至 5.0

Azure PowerShell 以前要求使用至少 3.0 版的 PowerShell 来运行 cmdlet。 此要求以后会提高到 5.0 版的 PowerShell。 若要了解如何升级到 PowerShell 5.0，请查看[此表](https://docs.microsoft.com/en-us/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell)。

### <a name="context-autosave-enabled-by-default"></a>默认启用上下文自动保存功能

上下文自动保存是指存储可以在新的和不同的 PowerShell 会话之间使用的 Azure 登录信息。 有关上下文自动保存的详细信息，请参阅[此文档](https://docs.microsoft.com/en-us/powershell/azure/context-persistence)。

在以前，上下文自动保存功能是禁用的，这意味着在两次会话之间不会存储用户的 Azure 登录信息，除非用户通过运行 `Enable-AzureRmContextAutosave` cmdlet 启用了上下文保存功能。 在以后，上下文自动保存功能会默认启用，这意味着即使用户的自动保存设置是不保存上下文，他们在下次登录时系统也会存储其上下文。 用户可以选择使用 `Disable-AzureRmContextAutosave` cmdlet 来退出此功能。

_注意_：如果用户以前禁用了上下文自动保存，或者在启用上下文自动保存后使用的是现有的上下文，则不受此更改的影响

### <a name="removal-of-tags-alias"></a>删除标记别名

`Tag` 参数的别名 `Tags` 已在多个 cmdlet 中删除。 下面是受此影响的模块（以及相应的 cmdlet）的列表：

#### `AzureRM.ApiManagement`

- `New-AzureRmApiManagement`
- `New-AzureRmApiManagementProperty`
- `Set-AzureRmApiManagementProperty`

#### `AzureRM.Automation`
- `Set-AzureRmAutomationRunbook`

#### `AzureRM.Cdn`
- `New-AzureRmCdnEndpoint`
- `New-AzureRmCdnProfile`

#### `AzureRM.Compute`
- `New-AzureRmVM`
- `Update-AzureRmVM`

#### `AzureRM.DataFactories`
- `New-AzureRmDataFactories`

#### `AzureRM.DataLakeAnalytics`
- `New-AzureRmDataLakeAnalyticsAccount`

#### `AzureRM.DataLakeStore`
- `New-AzureRmDataLakeStoreAccount`
- `Set-AzureRmDataLakeStoreAccount`

#### `AzureRM.MachineLearning`
- `Update-AzureRmMlCommitmentPlan`

#### `AzureRM.Media`
- `Set-AzureRmMediaService`

#### `AzureRM.OperationalInsights`
- `New-AzureRmOperationalInsightsSavedSearch`
- `New-AzureRmOperationalInsightsWorkspace`
- `Set-AzureRmOperationalInsightsSavedSearch`
- `Set-AzureRmOperationalInsightsWorkspace`

## <a name="breaking-changes-to-azurermcompute-cmdlets"></a>AzureRM.Compute cmdlet 的重大更改

**其他**
- 嵌套在类型 `PSDisk` 和 `PSSnapshot` 中的 SKU 名称属性已分别从 `StandardLRS` 和 `PremiumLRS` 更改为 `Standard_LRS` 和 `Premium_LRS`

```powershell
$disk = Get-AzureRmDisk -ResourceGroupName "MyResourceGroup" -DiskName "MyDiskName"
$disk.Sku.Name       # This will now return Standard_LRS or Premium_LRS

$snapshot = Get-AzureRmSnapshot -ResourceGroupName "MyResourceGroup" -SnapshotName "MySnapshotName"
$snapshot.Sku.Name   # This will now return Standard_LRS or Premium_LRS
```

- 嵌套在类型 `PSVirtualMachine`、`PSVirtualMachineScaleSet`、`PSImage` 中的存储帐户类型属性已分别从 `StandardLRS` 和 `PremiumLRS` 更改为 `Standard_LRS` 和 `Premium_LRS`

```powershell
$vm = Get-AzureRmVM -ResourceGroupName "MyResourceGroup" -Name "MyVM"
$vm.StorageProfile.DataDisks[0].ManagedDisk.StorageAccountType   # This will now return Standard_LRS or Premium_LRS
```

**Add-AzureRmImageDataDisk**
- 参数 `StorageAccountType` 接受的值已分别从 `StandardLRS` 和 `PremiumLRS` 更改为 `Standard_LRS` 和 `Premium_LRS`

**Add-AzureRmVMDataDisk**
- 参数 `StorageAccountType` 接受的值已分别从 `StandardLRS` 和 `PremiumLRS` 更改为 `Standard_LRS` 和 `Premium_LRS`

**Add-AzureRmVmssDataDisk**
- 参数 `StorageAccountType` 接受的值已分别从 `StandardLRS` 和 `PremiumLRS` 更改为 `Standard_LRS` 和 `Premium_LRS`

**New-AzureRmAvailabilitySet**
- 参数 `Managed` 已删除，改用 `Sku`

```powershell
# Old
New-AzureRmAvailabilitySet -ResourceGroupName "MyRG" -Name "MyAvailabilitySet" -Location "West US" -Managed

# New
New-AzureRmAvailabilitySet -ResourceGroupName "MyRG" -Name "MyAvailabilitySet" -Location "West US" -Sku "Aligned"
```

**New-AzureRmDiskConfig**
- 参数 `SkuName` 接受的值已分别从 `StandardLRS` 和 `PremiumLRS` 更改为 `Standard_LRS` 和 `Premium_LRS`

**New-AzureRmDiskUpdateConfig**
- 参数 `SkuName` 接受的值已分别从 `StandardLRS` 和 `PremiumLRS` 更改为 `Standard_LRS` 和 `Premium_LRS`

**New-AzureRmSnapshotConfig**
- 参数 `SkuName` 接受的值已分别从 `StandardLRS` 和 `PremiumLRS` 更改为 `Standard_LRS` 和 `Premium_LRS`

**New-AzureRmSnapshotUpdateConfig**
- 参数 `SkuName` 接受的值已分别从 `StandardLRS` 和 `PremiumLRS` 更改为 `Standard_LRS` 和 `Premium_LRS`

**Set-AzureRmImageOsDisk**
- 参数 `StorageAccountType` 接受的值已分别从 `StandardLRS` 和 `PremiumLRS` 更改为 `Standard_LRS` 和 `Premium_LRS`

**Set-AzureRmVMAEMExtension**
- 参数 `DisableWAD` 已删除
    -  默认禁用 Windows Azure 诊断

**Set-AzureRmVMDataDisk**
- 参数 `StorageAccountType` 接受的值已分别从 `StandardLRS` 和 `PremiumLRS` 更改为 `Standard_LRS` 和 `Premium_LRS`

**Set-AzureRmVMOSDisk**
- 参数 `StorageAccountType` 接受的值已分别从 `StandardLRS` 和 `PremiumLRS` 更改为 `Standard_LRS` 和 `Premium_LRS`

**Set-AzureRmVmssStorageProfile**
- 参数 `ManagedDisk` 接受的值已分别从 `StandardLRS` 和 `PremiumLRS` 更改为 `Standard_LRS` 和 `Premium_LRS`

**Update-AzureRmVmss**
- 参数 `ManagedDiskStorageAccountType` 接受的值已分别从 `StandardLRS` 和 `PremiumLRS` 更改为 `Standard_LRS` 和 `Premium_LRS`

## <a name="breaking-changes-to-azurermdatalakestore-cmdlets"></a>AzureRM.DataLakeStore cmdlet 的重大更改

**Export-AzureRmDataLakeStoreItem**
- 参数 `PerFileThreadCount` 和 `ConcurrentFileCount` 已删除。 以后请使用 `Concurrency` 参数

```powershell
# Old
Export-AzureRmDataLakeStoreItem -Account contoso -Path /test -Destination C:\test -Recurse -Resume -PerFileThreadCount 2 -ConcurrentFileCount 80

# New
Export-AzureRmDataLakeStoreItem -Account contoso -Path /test -Destination C:\test -Recurse -Resume -Concurrency 160
```

**Import-AzureRmDataLakeStoreItem**
- 参数 `PerFileThreadCount` 和 `ConcurrentFileCount` 已删除。 以后请使用 `Concurrency` 参数

```powershell
# Old
Import-AzureRmDataLakeStoreItem -Account contoso -Path C:\test -Destination /test -Recurse -Resume -ForceBinary -PerFileThreadCount 2 -ConcurrentFileCount 80

# New
Import-AzureRmDataLakeStoreItem -Account contoso -Path C:\test -Destination /test -Recurse -Resume -ForceBinary -Concurrency 160
```

**Remove-AzureRmDataLakeStoreItem**
- 参数 `Clean` 已删除

```powershell
# Old
Remove-AzureRmDataLakeStoreItem -Account "ContosoADL" -path /myFolder -Recurse -Clean

# New
Remove-AzureRmDataLakeStoreItem -Account "ContosoADL" -path /myFolder -Recurse
```

## <a name="breaking-changes-to-azurermdns-cmdlets"></a>AzureRM.Dns cmdlet 的重大更改

**New-AzureRmDnsRecordSet**
- 参数 `Force` 已删除

**Remove-AzureRmDnsRecordSet**
- 参数 `Force` 已删除

**Remove-AzureRmDnsZone**
- 参数 `Force` 已删除

## <a name="breaking-changes-to-azurerminsights-cmdlets"></a>AzureRM.Insights cmdlet 的重大更改

**Add-AzureRmAutoscaleSetting**
- 参数别名 `AutoscaleProfiles` 和 `Notifications` 已删除

**Add-AzureRmLogProfile**
- 参数别名 `Categories` 和 `Locations` 已删除

**Add-AzureRmMetricAlertRule**
- 参数别名 `Actions` 已删除

**Add-AzureRmWebtestAlertRule**
- 参数别名 `Actions` 已删除

**Get-AzureRmLog**
- 参数别名 `MaxRecords` 和 `MaxEvents` 已删除

**Get-AzureRmMetricDefinition**
- 参数别名 `MetricNames` 已删除

**New-AzureRmAlertRuleEmail**
- 参数别名 `CustomEmails` 和 `SendToServiceOwners` 已删除

**New-AzureRmAlertRuleWebhook**
- 参数别名 `Properties` 已删除

**New-AzureRmAutoscaleNotification**
- 参数别名 `CustomEmails`、`SendEmailToSubscriptionCoAdministrators`、`Webhooks` 已删除

**New-AzureRmAutoscaleProfile**
- 参数别名 `Rules`、`ScheduleDays`、`ScheduleHours`、`ScheduleMinutes` 已删除

**New-AzureRmAutoscaleWebhook**
- 参数别名 `Properties` 已删除

## <a name="breaking-changes-to-azurermkeyvault-cmdlets"></a>AzureRM.KeyVault cmdlet 的重大更改

**Add-AzureKeyVaultCertificate**
- `Certificate` 参数已变为必选。

**Set-AzureKeyVaultManagedStorageSasDefinition**
- 此 cmdlet 不再接受组成访问令牌的单个参数，而是将显式令牌参数（例如 `Service` 或 `Permissions`）替换为泛型 `TemplateUri` 参数，后者对应于在其他位置定义的示例访问令牌（假定使用存储 PowerShell cmdlet，或者根据存储文档手动进行组合）。此 cmdlet 保留 `ValidityPeriod` 参数。

若要详细了解如何为 Azure 存储组合共享访问令牌，请参阅相应的文档页：
- [Constructing a Service SAS] (https://docs.microsoft.com/en-us/rest/api/storageservices/Constructing-a-Service-SAS)（构造服务 SAS）
- [Constructing an Account SAS] (https://docs.microsoft.com/en-us/rest/api/storageservices/constructing-an-account-sas)（构造帐户 SAS）

```powershell
# Old
$sas = Set-AzureKeyVaultManagedStorageSasDefinition -VaultName myVault -Name myKey -Service Blob -Permissions 'rcw' -ValidityPeriod 180d

# New
$sctx=New-AzureStorageContext -StorageAccountName $sa.StorageAccountName -Protocol Https -StorageAccountKey Key1
$start=[System.DateTime]::Now.AddDays(-1)
$end=[System.DateTime]::Now.AddMonths(1)
$at=New-AzureStorageAccountSasToken -Service blob -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -StartTime $start -ExpiryTime $end -Context $sctx
$sas=Set-AzureKeyVaultManagedStorageSasDefinition -AccountName $sa.StorageAccountName -VaultName $kv.VaultName -Name accountsas -TemplateUri $at -SasType 'account' -ValidityPeriod ([System.Timespan]::FromDays(30))
```

**Set-AzureKeyVaultCertificateIssuer**
- `IssuerProvider` 参数已变为必选。

**Undo-AzureKeyVaultCertificateRemoval**
- 此 cmdlet 的输出已从 `CertificateBundle` 更改为 `PSKeyVaultCertificate`。

**Undo-AzureRmKeyVaultRemoval**
- `ResourceGroupName` 已从 `InputObject` 参数集中删除，改为从 `InputObject` 参数的 `ResourceId` 属性中获取。

**Set-AzureRmKeyVaultAccessPolicy**
- `all` 权限已从 `PermissionsToKeys`、`PermissionsToSecrets`、`PermissionsToCertificates` 中删除。

**常规**
- `ValueFromPipelineByPropertyName` 属性已从所有允许通过 `InputObject` 进行管道操作的 cmdlet 中删除。  受影响的 cmdlet 包括：
    - `Add-AzureKeyVaultCertificate`
    - `Add-AzureKeyVaultCertificateContact`
    - `Add-AzureKeyVaultKey`
    - `Backup-AzureKeyVaultKey`
    - `Backup-AzureKeyVaultSecret`
    - `Get-AzureKeyVaultCertficate`
    - `Get-AzureKeyVaultCertificateContact`
    - `Get-AzureKeyVaultCertificateIssuer`
    - `Get-AzureKeyVaultCertificateOperation`
    - `Get-AzureKeyVaultCertificatePolicy`
    - `Get-AzureKeyVaultKey`
    - `Get-AzureKeyVaultManagedStorageAccount`
    - `Get-AzureKeyVaultManagedStorageSasDefinition`
    - `Get-AzureKeyVaultSecret`
    - `Remove-AzureRmKeyVault`
    - `Remove-AzureRmKeyVaultAccessPolicy`
    - `Remove-AzureKeyVaultCertificate`
    - `Remove-AzureKeyVaultCertificateContact`
    - `Remove-AzureKeyVaultCertificateIssuer`
    - `Remove-AzureKeyVaultCertificateOperation`
    - `Remove-AzureKeyVaultKey`
    - `Remove-AzureKeyVaultManagedStorageAccount`
    - `Remove-AzureKeyVaultManagedStorageSasDefinition`
    - `Remove-AzureKeyVaultSecret`
    - `Restore-AzureKeyVaultKey`
    - `Restore-AzureKeyVaultSecret`
    - `Set-AzureRmKeyVaultAccessPolicy`
    - `Set-AzureKeyVaultCertificateAttribute`
    - `Set-AzureKeyVaultCertificateIssuer`
    - `Set-AzureKeyVaultCertificatePolicy`
    - `Set-AzureKeyVaultKeyAttribute`
    - `Set-AzureKeyVaultManagedStorageSasDefinition`
    - `Set-AzureKeyVaultSecret`
    - `Set-AzureKeyVaultSecretAttribute`
    - `Stop-AzureKeyVaultCertificateOperation`
    - `Undo-AzureKeyVaultCertificateRemoval`
    - `Undo-AzureKeyVaultKeyRemoval`
    - `Undo-AzureRmKeyVaultRemoval`
    - `Undo-AzureKeyVaultSecretRemoval`
    - `Update-AzureKeyVaultManagedStorageAccount`
    - `Update-AzureKeyVaultManagedStorageAccountKey`

- `ConfirmImpact` 级别已从所有 cmdlet 中删除。  受影响的 cmdlet 包括：
    - `Remove-AzureRmKeyVault`
    - `Remove-AzureKeyVaultCertificate`
    - `Remove-AzureKeyVaultCertificateIssuer`
    - `Remove-AzureKeyVaultCertificateOperation`
    - `Remove-AzureKeyVaultKey`
    - `Remove-AzureKeyVaultManagedStorageAccount`
    - `Remove-AzureKeyVaultManagedStorageSasDefinition`
    - `Remove-AzureKeyVaultSecret`
    - `Stop-AzureKeyVaultCertificateOperation`
    - `Update-AzureKeyVaultManagedStorageAccountKey`

- 对 `IKeyVaultDataServiceClient` 进行了更新，因此所有证书操作返回 PSTypes 而不是 SDK 类型。 这包括：
    - `SetCertificateContacts`
    - `GetCertificateContacts`
    - `GetCertificate`
    - `GetDeletedCertificate`
    - `MergeCertificate`
    - `ImportCertificate`
    - `DeleteCertificate`
    - `RecoverCertificate`
    - `EnrollCertificate`
    - `UpdateCertificate`
    - `GetCertificateOperation`
    - `DeleteCertificateOperation`
    - `CancelCertificateOperation`
    - `GetCertificatePolicy`
    - `UpdateCertificatePolicy`
    - `GetCertificateIssuer`
    - `SetCertificateIssuer`
    - `DeleteCertificateIssuer`

## <a name="breaking-changes-to-azurermnetwork-cmdlets"></a>AzureRM.Network cmdlet 的重大更改


**Add-AzureRmApplicationGatewayBackendHttpSettings**
- 参数 `ProbeEnabled` 已删除

**Add-AzureRmVirtualNetworkPeering**
- 参数别名 `AlloowGatewayTransit` 已删除

**New-AzureRmApplicationGatewayBackendHttpSettings**
- 参数 `ProbeEnabled` 已删除

**Set-AzureRmApplicationGatewayBackendHttpSettings**
- 参数 `ProbeEnabled` 已删除

## <a name="breaking-changes-to-azurermrediscache-cmdlets"></a>AzureRM.RedisCache cmdlet 的重大更改

**New-AzureRmRedisCache**
- 参数 `Subnet` 和 `VirtualNetwork` 已删除，改用 `SubnetId`
- 参数 `RedisVersion` 已删除
- 参数 `MaxMemoryPolicy` 已删除，改用 `RedisConfiguration`

```powershell
# Old
New-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -Location "North Central US" -MaxMemoryPolicy "allkeys-lru"

# New
New-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -Location "North Central US" -RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}
```

**Set-AzureRmRedisCache**
- 参数 `MaxMemoryPolicy` 已删除，改用 `RedisConfiguration`

```powershell
# Old
Set-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -MaxMemoryPolicy "allkeys-lru"

# New
Set-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}
```

## <a name="breaking-changes-to-azurermresources-cmdlets"></a>AzureRM.Resources cmdlet 的重大更改

**Find-AzureRmResource**
- 此 cmdlet 已删除，相关功能已移到 `Get-AzureRmResource` 中

```powershell
# Old
Find-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceGroupNameContains "ResourceGroup"
Find-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceNameContains "test"

# New
Get-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceGroupName "*ResourceGroup*"
Get-AzureRmResource -ResourceType "Microsoft.Web/sites" -Name "*test*"
```

**Find-AzureRmResourceGroup**
- 此 cmdlet 已删除，相关功能已移到 `Get-AzureRmResourceGroup` 中

```powershell
# Old
Find-AzureRmResourceGroup
Find-AzureRmResourceGroup -Tag @{ "testtag" = $null }
Find-AzureRmResourceGroup -Tag @{ "testtag" = "testval" }

# New
Get-AzureRmResourceGroup
Get-AzureRmResourceGroup -Tag @{ "testtag" = $null }
Get-AzureRmResourceGroup -Tag @{ "testtag" = "testval" }
```

**Get-AzureRmRoleDefinition**
- 参数 `AtScopeAndBelow` 已删除

```powershell

# Old
Get-AzureRmRoleDefinition [other required parameters] -AtScopeAndBelow

# New
Get-AzureRmRoleDefinition [other required parameters]
```

## <a name="breaking-changes-to-azurermstorage-cmdlets"></a>AzureRM.Storage cmdlet 的重大更改

**New-AzureRmStorageAccount**
- 参数 `EnableEncryptionService` 已删除

**Set-AzureRmStorageAccount**
- 参数 `EnableEncryptionService` 和 `DisableEncryptionService` 已删除

## <a name="removed-modules"></a>删除的模块

### `AzureRM.ServerManagement`

服务器管理工具服务[去年停用](https://blogs.technet.microsoft.com/servermanagement/2017/05/17/smt-preview-service-is-being-retired-on-june-30-2017/)，因此，SMT 的相应模块 `AzureRM.ServerManagement` 已从 `AzureRM` 中删除，以后将停止寄送。

### `AzureRM.SiteRecovery`

`AzureRM.SiteRecovery` 模块将被 `AzureRM.RecoveryServices.SiteRecovery` 取代，后者是 `AzureRM.SiteRecovery` 模块在功能上的超级组合，包括新的等效 cmdlet 组合。 下面是从旧 cmdlet 到新 cmdlet 的映射的完整列表：

| 已弃用的 cmdlet                                        | 等效 cmdlet                                                | 别名                                  |
|----------------------------------------------------------|------------------------------------------------------------------|------------------------------------------|
| `Edit-AzureRmSiteRecoveryRecoveryPlan`                   | `Edit-AzureRmRecoveryServicesAsrRecoveryPlan`                    | `Edit-ASRRecoveryPlan`                   |
| `Get-AzureRmSiteRecoveryFabric`                          | `Get-AzureRmRecoveryServicesAsrFabric`                           | `Get-ASRFabric`                          |
| `Get-AzureRmSiteRecoveryJob`                             | `Get-AzureRmRecoveryServicesAsrJob`                              | `Get-ASRJob`                             |
| `Get-AzureRmSiteRecoveryNetwork`                         | `Get-AzureRmRecoveryServicesAsrNetwork`                          | `Get-ASRNetwork`                         |
| `Get-AzureRmSiteRecoveryNetworkMapping`                  | `Get-AzureRmRecoveryServicesAsrNetworkMapping`                   | `Get-ASRNetworkMapping`                  |
| `Get-AzureRmSiteRecoveryPolicy`                          | `Get-AzureRmRecoveryServicesAsrPolicy`                           | `Get-ASRPolicy`                          |
| `Get-AzureRmSiteRecoveryProtectableItem`                 | `Get-AzureRmRecoveryServicesAsrProtectableItem`                  | `Get-ASRProtectableItem`                 |
| `Get-AzureRmSiteRecoveryProtectionContainer`             | `Get-AzureRmRecoveryServicesAsrProtectionContainer`              | `Get-ASRProtectionContainer`             |
| `Get-AzureRmSiteRecoveryProtectionContainerMapping`      | `Get-AzureRmRecoveryServicesAsrProtectionContainerMapping`       | `Get-ASRProtectionContainerMapping`      |
| `Get-AzureRmSiteRecoveryProtectionEntity`                | `Get-AzureRmRecoveryServicesAsrProtectableItem`                  | `Get-ASRProtectableItem`                 |
| `Get-AzureRmSiteRecoveryRecoveryPlan`                    | `Get-AzureRmRecoveryServicesAsrRecoveryPlan`                     | `Get-ASRRecoveryPlan`                    |
| `Get-AzureRmSiteRecoveryRecoveryPoint`                   | `Get-AzureRmRecoveryServicesAsrRecoveryPoint`                    | `Get-ASRRecoveryPoint`                   |
| `Get-AzureRmSiteRecoveryReplicationProtectedItem`        | `Get-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Get-ASRReplicationProtectedItem`        |
| `Get-AzureRmSiteRecoveryServer`                          | `Get-AzureRmRecoveryServicesAsrServicesProvider`                 | `Get-ASRServicesProvider`                |
| `Get-AzureRmSiteRecoveryServicesProvider`                | `Get-AzureRmRecoveryServicesAsrServicesProvider`                 | `Get-ASRServicesProvider`                |
| `Get-AzureRmSiteRecoverySite`                            | `Get-AzureRmRecoveryServicesAsrFabric`                           | `Get-ASRFabric`                          |
| `Get-AzureRmSiteRecoveryStorageClassification`           | `Get-AzureRmRecoveryServicesAsrStorageClassification`            | `Get-ASRStorageClassification`           |
| `Get-AzureRmSiteRecoveryStorageClassificationMapping`    | `Get-AzureRmRecoveryServicesAsrStorageClassificationMapping`     | `Get-ASRStorageClassificationMapping`    |
| `Get-AzureRmSiteRecoveryVault`                           | `Get-AzureRmRecoveryServicesVault`                               |                                          |
| `Get-AzureRmSiteRecoveryVaultSettings`                   | `Get-AzureRmRecoveryServicesAsrVaultContext`                     |                                          |
| `Get-AzureRmSiteRecoveryVaultSettingsFile`               | `Get-AzureRmRecoveryServicesVaultSettingsFile`                   |                                          |
| `Get-AzureRmSiteRecoveryVM`                              | `Get-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Get-ASRReplicationProtectedItem`        |
| `Import-AzureRmSiteRecoveryVaultSettingsFile`            | `Import-AzureRmRecoveryServicesAsrVaultSettingsFile`             |                                          |
| `New-AzureRmSiteRecoveryFabric`                          | `New-AzureRmRecoveryServicesAsrFabric`                           | `New-ASRFabric`                          |
| `New-AzureRmSiteRecoveryNetworkMapping`                  | `New-AzureRmRecoveryServicesAsrNetworkMapping`                   | `New-ASRNetworkMapping`                  |
| `New-AzureRmSiteRecoveryPolicy`                          | `New-AzureRmRecoveryServicesAsrPolicy`                           | `New-ASRPolicy`                          |
| `New-AzureRmSiteRecoveryProtectionContainerMapping`      | `New-AzureRmRecoveryServicesAsrProtectionContainerMapping`       | `New-ASRProtectionContainerMapping`      |
| `New-AzureRmSiteRecoveryRecoveryPlan`                    | `New-AzureRmRecoveryServicesAsrRecoveryPlan`                     | `New-ASRRecoveryPlan`                    |
| `New-AzureRmSiteRecoveryReplicationProtectedItem`        | `New-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `New-ASRReplicationProtectedItem`        |
| `New-AzureRmSiteRecoverySite`                            | `New-AzureRmRecoveryServicesAsrFabric`                           | `New-ASRFabric`                          |
| `New-AzureRmSiteRecoveryStorageClassificationMapping`    | `New-AzureRmRecoveryServicesAsrStorageClassificationMapping`     | `New-ASRStorageClassificationMapping`    |
| `New-AzureRmSiteRecoveryVault`                           | `New-AzureRmRecoveryServicesVault`                               |                                          |
| `Remove-AzureRmSiteRecoveryFabric`                       | `Remove-AzureRmRecoveryServicesAsrFabric`                        | `Remove-ASRFabric`                       |
| `Remove-AzureRmSiteRecoveryNetworkMapping`               | `Remove-AzureRmRecoveryServicesAsrNetworkMapping`                | `Remove-ASRNetworkMapping`               |
| `Remove-AzureRmSiteRecoveryPolicy`                       | `Remove-AzureRmRecoveryServicesAsrPolicy`                        | `Remove-ASRPolicy`                       |
| `Remove-AzureRmSiteRecoveryProtectionContainerMapping`   | `Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping`    | `Remove-ASRProtectionContainerMapping`   |
| `Remove-AzureRmSiteRecoveryRecoveryPlan`                 | `Remove-AzureRmRecoveryServicesAsrRecoveryPlan`                  | `Remove-ASRRecoveryPlan`                 |
| `Remove-AzureRmSiteRecoveryReplicationProtectedItem`     | `Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem`      | `Remove-ASRReplicationProtectedItem`     |
| `Remove-AzureRmSiteRecoveryServer`                       | `Remove-AzureRmRecoveryServicesAsrServicesProvider`              |                                          |
| `Remove-AzureRmSiteRecoveryServicesProvider`             | `Remove-AzureRmRecoveryServicesAsrServicesProvider`              | `Remove-ASRServicesProvider`             |
| `Remove-AzureRmSiteRecoverySite`                         | `Remove-AzureRmRecoveryServicesAsrFabric`                        | `Remove-ASRFabric`                       |
| `Remove-AzureRmSiteRecoveryStorageClassificationMapping` | `Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping`  | `Remove-ASRStorageClassificationMapping` |
| `Remove-AzureRmSiteRecoveryVault`                        | `Remove-AzureRmRecoveryServicesVault`                            |                                          |
| `Restart-AzureRmSiteRecoveryJob`                         | `Restart-AzureRmRecoveryServicesAsrJob`                          | `Restart-ASRJob`                         |
| `Resume-AzureRmSiteRecoveryJob`                          | `Resume-AzureRmRecoveryServicesAsrJob`                           | `Resume-ASRJob`                          |
| `Set-AzureRmSiteRecoveryProtectionEntity`                | `New-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `New-ASRReplicationProtectedItem`        |
| `Set-AzureRmSiteRecoveryReplicationProtectedItem`        | `Set-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Set-ASRReplicationProtectedItem`        |
| `Set-AzureRmSiteRecoveryVaultSettings`                   | `Set-AzureRmRecoveryServicesAsrVaultContext`                     | `Set-ASRVaultContext`                    |
| `Set-AzureRmSiteRecoveryVM`                              | `Set-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Set-ASRReplicationProtectedItem`        |
| `Start-AzureRmSiteRecoveryApplyRecoveryPoint`            | `Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint`             | `Start-ASRApplyRecoveryPoint`            |
| `Start-AzureRmSiteRecoveryCommitFailoverJob`             | `Start-AzureRmRecoveryServicesAsrCommitFailoverJob`              | `Start-ASRCommitFailoverJob`             |
| `Start-AzureRmSiteRecoveryPlannedFailoverJob`            | `Start-AzureRmRecoveryServicesAsrPlannedFailoverJob`             | `Start-ASRPlannedFailoverJob`            |
| `Start-AzureRmSiteRecoveryPolicyAssociationJob`          | `New-AzureRmRecoveryServicesAsrProtectionContainerMapping`       | `New-ASRProtectionContainerMapping`      |
| `Start-AzureRmSiteRecoveryPolicyDissociationJob`         | `Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping`    | `Remove-ASRProtectionContainerMapping`   |
| `Start-AzureRmSiteRecoveryTestFailoverJob`               | `Start-AzureRmRecoveryServicesAsrTestFailoverJob`                | `Start-ASRTestFailoverJob`               |
| `Start-AzureRmSiteRecoveryUnplannedFailoverJob`          | `Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob`           | `Start-ASRUnplannedFailoverJob`          |
| `Stop-AzureRmSiteRecoveryJob`                            | `Stop-AzureRmRecoveryServicesAsrJob`                             | `Stop-ASRJob`                            |
| `Update-AzureRmSiteRecoveryPolicy`                       | `Update-AzureRmRecoveryServicesAsrPolicy`                        | `Update-ASRPolicy`                       |
| `Update-AzureRmSiteRecoveryProtectionDirection`          | `Update-AzureRmRecoveryServicesAsrProtectionDirection`           | `Update-ASRProtectionDirection`          |
| `Update-AzureRmSiteRecoveryRecoveryPlan`                 | `Update-AzureRmRecoveryServicesAsrRecoveryPlan`                  | `Update-ASRRecoveryPlan`                 |
| `Update-AzureRmSiteRecoveryServer`                       | `Update-AzureRmRecoveryServicesAsrServicesProvider`              | `Update-ASRServicesProvider`             |
| `Update-AzureRmSiteRecoveryServicesProvider`             | `Update-AzureRmRecoveryServicesAsrvCenter`                       | `Update-ASRvCenter`                      |