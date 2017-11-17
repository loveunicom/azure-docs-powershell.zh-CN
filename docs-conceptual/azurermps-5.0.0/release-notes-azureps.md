---
title: "Azure PowerShell 更改日志 | Microsoft Docs"
description: "下面提供了对 Azure PowerShell 最新版本所做更改的历史记录。"
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: 
ms.date: 11/14/2017
ms.openlocfilehash: ab35cbc4ec1a0bd4e7ee40e1864bd7941f5bca87
ms.sourcegitcommit: 79dd3700b5cb4cb90b268778b482082052160093
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/14/2017
---
# <a name="release-notes"></a>发行说明

下面是此版本中对 Azure PowerShell 所做的更改列表。

## <a name="20171110-version-501"></a>2017.11.10 版本 5.0.1
* 修复了在以下模块中执行时会导致某些 cmdlet 失败的程序集加载问题：
    - AzureRM.ApiManagement
    - AzureRM.Backup
    - AzureRM.Batch
    - AzureRM.Compute
    - AzureRM.DataFactories
    - AzureRM.HDInsight
    - AzureRM.KeyVault
    - AzureRM.RecoveryServices
    - AzureRM.RecoveryServices.Backup
    - AzureRM.RecoveryServices.SiteRecovery
    - AzureRM.RedisCache
    - AzureRM.SiteRecovery
    - AzureRM.Sql
    - AzureRM.Storage
    - AzureRM.StreamAnalytics

## <a name="2017118---version-500"></a>2017.11.8 - 版本 5.0.0
* 注意：这是一个有重大更改的版本。 有关引入的重大更改的完整列表，请参阅迁移指南 (https://aka.ms/azps-migration-guide)。
* AzureRM 中的所有 cmdlet 现在支持联机帮助
    - 结合 -Online 参数运行 Get-Help 可在默认 Internet 浏览器中打开联机帮助
* AnalysisServices
    * 修复了 Synchronize-AzureAsInstance 命令，现在它可以配合新的 AsAzure REST API 进行同步
* ApiManagement
    * 有关此版本中对 ApiManagement 所做的重大更改，参阅迁移指南
    * 更新了 Cmdlet Get-AzureRmApiManagementUser 以修复问题 https://github.com/Azure/azure-powershell/issues/4510
    * 更新了 Cmdlet New-AzureRmApiManagementApi 以创建包含空路径的 API (https://github.com/Azure/azure-powershell/issues/4069)
* ApplicationInsights
    * 添加用于获取/创建/删除 Applicaiton Insights 资源的命令
        - Get-AzureRmApplicationInsights
        - New-AzureRmApplicationInsights
        - Remove-AzureRmApplicationInsights
    * 添加用于获取/更新 Applicaiton Insights 资源定价/每日上限的命令
        - Get-AzureRmApplicationInsights -IncludeDailyCap
        - Set-AzureRmApplicationInsightsPricingPlan
        - Set-AzureRmApplicationInsightsDailyCap
    * 添加用于获取/创建/更新/删除 Applicaiton Insights 资源连续导出的命令
        - Get-AzureRmApplicationInsightsContinuousExport
        - Set-AzureRmApplicationInsightsContinuousExport
        - New-AzureRmApplicationInsightsContinuousExport
        - Remove-AzureRmApplicationInsightsContinuousExport
    * 添加用于获取/创建/删除 Applicaiton Insights 资源 API 密钥的命令
        - Get-AzureRmApplicationInsightsApiKey
        - New-AzureRmApplicationInsightsApiKey
        - Remove-AzureRmApplicationInsightsApiKey
* AzureBatch
    * 为 `New-AzureRmBatchAccount` 添加了新参数。
        - `PoolAllocationMode`：用于在 Batch 帐户中创建池的分配模式。 若要创建一个可在用户订阅中分配池节点的 Batch 帐户，请将此参数设置为 `UserSubscription`。
        - `KeyVaultId`：与 Batch 帐户关联的 Azure Key Vault 的资源 ID。
        - `KeyVaultUrl`：与 Batch 帐户关联的 Azure Key Vault 的 URL。
    * 更新了 `New-AzureBatchTask` 的参数。
        - 删除了 `RunElevated` 开关。 已添加 `UserIdentity` 参数来取代 `RunElevated`，可按如下所示，通过构造 `PSUserIdentity` 来实现等效的行为：
            - $autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")
            - $userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser
        - 添加了 `AuthenticationTokenSettings` 参数。 使用此参数可以请求 Batch 服务向运行的任务提供身份验证令牌，从而无需向该任务传递 Batch 帐户密钥来向 Batch 服务发出请求。
        - 添加了 `ContainerSettings` 参数。
            - 使用此参数可以请求 Batch 服务在容器内部运行任务。
        - 添加了 `OutputFiles` 参数。
            - 使用此参数可以配置任务，以便在完成任务之后将文件上传到 Azure 存储。
    * 更新了 `New-AzureBatchPool` 的参数。
        - 添加了 `UserAccounts` 参数。
            - 此参数定义在池中每个节点上创建的用户帐户。
        - 添加了 `TargetLowPriorityComputeNodes`，并已将 `TargetDedicated` 重命名为 `TargetDedicatedComputeNodes`。
            - 为 `TargetDedicatedComputeNodes` 参数创建了 `TargetDedicated` 别名。
        - 添加了 `NetworkConfiguration` 参数。
            - 使用此参数可以配置池的网络设置。
    * 更新了 `New-AzureBatchCertificate` 的参数。
        - `Password` 参数现在是 `SecureString`。
    * 更新了 `New-AzureBatchComputeNodeUser` 的参数。
        - `Password` 参数现在是 `SecureString`。
    * 更新了 `Set-AzureBatchComputeNodeUser` 的参数。
        - `Password` 参数现在是 `SecureString`。
    * 已将 `Get-AzureBatchNodeFile`、`Get-AzureBatchNodeFileContent` 和 `Remove-AzureBatchNodeFile` 的 `Name` 参数重命名为 `Path`。
        - 为 `Path` 参数创建了 `Name` 别名。
    * 对象更改
        - 有关完整列表，参阅 Batch 更改日志
    * 添加了对基于 Azure Active Directory 的身份验证的支持。
        - 若要使用 Azure Active Directory 身份验证，请使用 `Get-AzureRmBatchAccount` cmdlet 检索 `BatchAccountContext` 对象，并将此 `BatchAccountContext` 提供给 Batch 服务 cmdlet 的 `-BatchContext` 参数。 采用 `PoolAllocationMode = UserSubscription` 设置的帐户必须使用 Azure Active Directory 身份验证。
        - 对于现有帐户或使用 `PoolAllocationMode = BatchService` 创建的新帐户，可通过使用 `Get-AzureRmBatchAccoutKeys` cmdlet 检索 `BatchAccountContext` 对象，来继续使用共享密钥身份验证。
* 计算
    * Azure 磁盘加密扩展命令
        - “Set-AzureRmVmDiskEncryptionExtension”的新参数“-EncryptFormatAll”可以加密形式格式化数据磁盘
        - “Set-AzureRmVmDiskEncryptionExtension”的新参数“-ExtensionPublisherName”和“-ExtensionType”可用于切换到扩展的其他版本
        - “Disable-AzureRmVmDiskEncryption”的新参数“-ExtensionPublisherName”和“-ExtensionType”可用于切换到扩展的其他版本
        - “Get-AzureRmVmDiskEncryptionStatus”的新参数“-ExtensionPublisherName”和“-ExtensionType”可用于切换到扩展的其他版本
* DataLakeAnalytics
    * 有关此版本中对 DataLakeAnalytics 所做的重大更改，参阅迁移指南
    * 更改了 Get-AzureRmDataLakeAnalyticsAccount 的两个 OutputType 中的一个
        - List\<DataLakeAnalyticsAccount> 已更改为 List\<PSDataLakeAnalyticsAccountBasic>
        - PSDataLakeAnalyticsAccountBasic 的属性是 DataLakeAnalyticsAccount 的属性的严格子集
        - DataLakeAnalyticsAccount 中的附加属性不会由服务返回。  因此，此项更改旨在准确反映这种情况。 这些附加属性仍在 PSDataLakeAnalyticsAccountBasic 中，但已标记为“已过时”。
    * 更改了 Get-AzureRmDataLakeAnalyticsJob 的两个 OutputType 中的一个
        - List\<JobInformation> 已更改为 List\<PSJobInformationBasic>
        - PSJobInformationBasic 的属性是 JobInformation 的属性的严格子集
        - JobInformation 中的附加属性不会由服务返回。  因此，此项更改旨在准确反映这种情况。 这些附加属性仍在 PSJobInformationBasic 中，但已标记为“已过时”。
* DataLakeStore
    * 有关此版本中对 DataLakeStore 所做的重大更改，参阅迁移指南
    * 更改了 Get-AzureRmDataLakeStoreAccount 的两个 OutputType 中的一个
        - List\<PSDataLakeStoreAccount> 已更改为 List\<PSDataLakeStoreAccountBasic>
        - PSDataLakeStoreAccountBasic 的属性是 PSDataLakeStoreAccount 的属性的严格子集
        - PSDataLakeStoreAccount 中的附加属性不会由服务返回。  因此，此项更改旨在准确反映这种情况。 这些附加属性仍在 PSDataLakeStoreAccountBasic 中，但已标记为“已过时”。
* Dns
    * 对 Azure DNS 中 CAA 记录类型的支持
       - 支持对 CAA 记录类型执行所有操作
* EventHub
    * 有关此版本中对 EventHub 所做的重大更改，参阅迁移指南
* 洞察力
    * 有关此版本中对 Insights 所做的重大更改，参阅迁移指南
* 网络
    * 有关此版本中对 Network 所做的重大更改，参阅迁移指南
    * 添加了 cmdlet 用于列出指定 Azure 区域的可用 Internet 服务提供商
        - Get-AzureRmNetworkWatcherReachabilityProvidersList
    * 添加了 cmdlet 用于获取 Internet 服务提供商从指定位置到 Azure 区域的相对延迟评分
        - Get-AzureRmNetworkWatcherReachabilityReport
* 配置文件
    - Set-AzureRmDefault
        - 使用此 cmdlet 可设置默认资源组。  因此，对于某些 cmdlet 可以选择性地使用 -ResourceGroup 参数；如果未指定资源组，将使用默认值
        - ```Set-AzureRmDefault -ResourceGroupName "ExampleResourceGroup"```
        - 如果订阅中存在指定的资源组，此资源组将设置为默认值。  否则，将创建资源组并将其设置为默认值。
    - Get-AzureRmDefault
        - 使用此 cmdlet 可获取当前的默认资源组（和将来的其他默认资源组）。
        - ```Get-AzureRmDefault -ResourceGroup```
    - Clear-AzureRmDefault
        - 使用此 cmdlet 可删除当前的默认资源组
        - ```Clear-AzureRmDefault -ResourceGroup```
    - Add-AzureRmEnvironment 和 Set-AzureRmEnvironment
        - 添加 BatchAudience 参数，以便指定在获取 Batch 服务的身份验证令牌时要使用的 Azure Batch Active Directory 受众。
* RecoveryServices.Backup
    * 添加了 cmdlet 用于执行即时文件恢复。
        - Get-AzureRmRecoveryServicesBackupRPMountScript
        - Disable-AzureRmRecoveryServicesBackupRPMountScript
    * 已 RecoveryServices.Backup SDK 版本更新到最新版
    * 更新了 Azure VM 工作负荷的测试，以便测试运行所需的所有设置由测试本身完成。
    * 修复了 https://github.com/Azure/azure-powershell/issues/3164
* RecoveryServices.SiteRecovery
    * 对 ASR VMware 到 Azure Site Recovery 的迁移所做的更改（cmdlet 目前支持企业到企业、企业到 Azure 以及 HyperV 到 Azure 的操作）
        - New-AzureRmRecoveryServicesAsrPolicy
        - New-AzureRmRecoveryServicesAsrProtectedItem
        - Update-AzureRmRecoveryServicesAsrPolicy
        - Update-AzureRmRecoveryServicesAsrProtectionDirection
    * 添加了对基于 AAD 的保管库的支持
    * 添加了 cmdlet 用于管理 VCenter 资源
        - Get-AzureRmRecoveryServicesAsrVCenter
        - New-AzureRmRecoveryServicesAsrVCenter
        - Remove-AzureRmRecoveryServicesAsrVCenter
        - Update-AzureRmRecoveryServicesAsrVCenter
    * 添加了其他 cmdlet
        - Get-AzureRmRecoveryServicesAsrAlertSetting
        - Get-AzureRmRecoveryServicesAsrEvent
        - New-AzureRmRecoveryServicesAsrProtectableItem
        - Set-AzureRmRecoveryServicesAsrAlertSetting
        - Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob
        - Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob
        - Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob
        - Update-AzureRmRecoveryServicesAsrMobilityService
* ServiceBus
    - 有关此版本中对 ServiceBus 所做的重大更改，参阅迁移指南
* Sql
    * 添加列出和取消对数据库执行的异步 updateslo 操作的支持
        - 更新现有的 cmdlet Get-AzureRmSqlDatabaseActivity 以返回 DB updateslo 操作状态。
        - 添加新的 cmdlet Stop-AzureRmSqlDatabaseActivity，以取消对数据库执行的 updateslo 异步操作。
    * 添加数据库和弹性池区域冗余的支持
        - 添加 New-AzureRmSqlDatabase 的 ZoneRedundant 开关参数
        - 添加 Set-AzureRmSqlDatabase 的 ZoneRedundant 开关参数
        - 添加 New-AzureRmSqlElasticPool 的 ZoneRedundant 开关参数
        - 添加 Set-AzureRmSqlElasticPool 的 ZoneRedundant 开关参数
    * 添加对服务器 DNS 别名的支持
        - 添加 Get-AzureRmSqlServerDnsAlias cmdlet，用于根据服务器和别名获取服务器 DNS 别名，或 Azure SQL Server 的一系列服务器 DNS 别名。
        - 添加 New-AzureRmSqlServerDnsAlias cmdlet，用于新建给定 Azure SQL Server 的服务器 DNS 别名
        - 添加 Set-AzurermSqlServerDnsAlias cmlet，用于更新服务器 DNS 别名所指向的 Azure SQL Server
        - 添加 Remove-AzureRmSqlServerDnsAlias cmdlet，用于删除 Azure SQL Server 的服务器 DNS 别名
* Azure.存储
    * 升级到 Azure 存储客户端库 8.5.0 和 Azure 存储 DataMovement 库 0.6.3
    * 添加文件共享支持快照
        - 为 Get-AzureStorageShare 添加“SnapshotTime”参数
        - 为 Remove-AzureStorageShare 添加“IncludeAllSnapshot”参数