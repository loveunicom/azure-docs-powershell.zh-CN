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
ms.openlocfilehash: cf58789ba69fd2fc157e37d0b052827b361246e5
ms.sourcegitcommit: c42c7176276ec4e1cc3360a93e6b15d32083bf9f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/14/2017
---
# <a name="release-notes"></a>发行说明

下面是此版本中对 Azure PowerShell 所做的更改列表。

## <a name="20171208-version-511"></a>2017.12.08 - 版本 5.1.1
* AnalysisServices
    - 将位置的验证集更改为动态查找，以便支持所有云。
* 自动化
    - 更新为 Import-AzureRMAutomationRunbook
        - 现在为 Python2 Runbook 提供支持
* 批处理
    - 修复了没有资源组时帐户操作无法自动检测资源组这一 Bug
* 计算
    - Get-AzureRmComputeResourceSku 显示区域信息。
    - 更新了 Disable-AzureRmVmssDiskEncryption 以修复问题 https://github.com/Azure/azure-powershell/issues/5038
    - 添加了对长时间运行的计算 cmdlet 的 -AsJob 支持。 允许选定的 cmdlet 在后台运行并返回可跟踪和控制进度的作业。
        - 受影响的 cmdlet 包括适用于虚拟机和虚拟机规模集的 New-、Update-、Set-、Remove-、Start-、Restart-、Stop- cmdlet
    - 向 New-AzureRmVM（可使用智能默认设置创建虚拟机和所有必需的资源）添加了简化的参数集
* ContainerInstance
    - 应用 Azure 容器实例 SDK 2017-10-01
        - 支持容器 run-to-completion
        - 支持 Azure 文件卷装载
        - 支持为公共 IP 打开多个端口
* ContainerRegistry
    - 用于异地复制和 Webhook 的新 cmdlet
        - Get/New/Remove-AzureRmContainerRegistryReplication
        - Get/New/Remove/Test/Update-AzureRmContainerRegistryWebhook
* 数据工厂
    - 凭据加密功能现在适用于启用了“远程访问”的操作（通过网络的操作）和禁用了“远程访问”的操作（本地计算机操作）。
* DataFactoryV2
    - 添加了两个新的 cmdlet：Update-AzureRmDataFactoryV2 和 Stop-AzureRmDataFactoryV2PipelineRun
* DataLakeAnalytics
    - 向 Submit-AzureRmDataLakeAnalyticsJob 添加了名为 ScriptParameter 的参数
        - 可以对 Submit-AzureRmDataLakeAnalyticsJob 使用 Get-Help 来查找有关 ScriptParameter 的详细信息
    - 已将 New-AzureRmDataLakeAnalyticsAccount 的参数 MaxDegreeOfParallelism 更改为 MaxAnalyticsUnits
        - 为参数 MaxAnalyticsUnits 添加了别名 MaxDegreeOfParallelism
    - 已将 New-AzureRmDataLakeAnalyticsComputePolicy 的参数 MaxDegreeOfParallelismPerJob 更改为 MaxAnalyticsUnitsPerJob
        - 为参数 MaxAnalyticsUnitsPerJob 添加了别名 MaxDegreeOfParallelismPerJob
    - 已将 Set-AzureRmDataLakeAnalyticsAccount 的参数 MaxDegreeOfParallelism 更改为 MaxAnalyticsUnits
        - 为参数 MaxAnalyticsUnits 添加了别名 MaxDegreeOfParallelism
    - 已将 Submit-AzureRmDataLakeAnalyticsJob 的参数 DegreeOfParallelism 更改为 AnalyticsUnits
        - 为参数 AnalyticsUnits 添加了别名 DegreeOfParallelism
    - 已将 Update-AzureRmDataLakeAnalyticsComputePolicy 的参数 MaxDegreeOfParallelismPerJob 更改为 MaxAnalyticsUnitsPerJob
        - 为参数 MaxAnalyticsUnitsPerJob 添加了别名 MaxDegreeOfParallelismPerJob
* MachineLearningCompute
    - 添加 Set-AzureRmMlOpCluster
        - 更新群集的代理计数或 SSL 配置
    - 业务流程协调程序属性为可选
        - 此服务会创建服务主体（如果未提供），因此业务流程协调程序属性现在为可选
* PowerBIEmbedded
    - 添加对 Power BI Embedded 容量 cmdlet 的支持
    - 全新 Cmdlet Get-AzureRmPowerBIEmbeddedCapacity - 获取 PowerBI Embedded 容量的详细信息。
    - 全新 Cmdlet New-AzureRmPowerBIEmbeddedCapacity - 创建新的 PowerBI Embedded 容量
    - 全新 Cmdlet Remove-AzureRmPowerBIEmbeddedCapacity - 删除 PowerBI Embedded 容量的实例
    - 全新 Cmdlet Resume-AzureRmPowerBIEmbeddedCapacity - 恢复 PowerBI Embedded 容量的实例
    - 全新 Cmdlet Suspend-AzureRmPowerBIEmbeddedCapacity - 暂停 PowerBI Embedded 容量的实例
    - 全新 Cmdlet Test-AzureRmPowerBIEmbeddedCapacity - 测试 PowerBI Embedded 容量的实例是否存在
    - 全新 Cmdlet Update-AzureRmPowerBIEmbeddedCapacity - 修改 PowerBI Embedded 容量的实例
* 配置文件
    - 已将 USGovernmentActiveDirectoryEndpoint 更新为 https://login.microsoftonline.us/
        - 有关 Azure 政府终结点映射的详细信息，请查看以下链接：https://docs.microsoft.com/en-us/azure/azure-government/documentation-government-developer-guide#endpoint-mapping
    - 添加了对 cmdlet 的 -AsJob 支持，允许所选 cmdlet 在后台执行并返回可跟踪和控制进度的作业
    - 向 Get-AzureRmSubscription cmdlet 添加了 -AsJob 参数
* RecoveryServices.Backup
    - 修复了 Bug - Get-AzureRmRecoveryServicesBackupItem 应该为容器名称筛选器执行不区分大小写的比较。
    - 修复了 Bug - AzureVmItem 现在有一个可显示上次进行备份操作的时间的属性 - LastBackupTime.
* 资源
    - 修复了 Get-AzureRMRoleAssignment 所进行的分配没有为自定义角色提供 roledefiniton 名称的问题
        - 用户现在可以对具有 roledefinition 名称的分配使用 Get-AzureRMRoleAssignment，不管角色类型如何
    - 修复了在 assignablescopes 中存在新作用域时使用 Set-AzureRMRoleRoleDefinition 引发“找不到 RD”错误的问题
        - 用户现在可以将 Set-AzureRMRoleRoleDefinition 与包括新作用域在内的可分配作用域配合使用，不管作用域的位置如何
    - 允许作用域以“/”结尾
        - 用户现在可以使用作用域以“/”结尾的 RoleDefinition 和 RoleAssignment cmdlet，与 API 和 CLI 保持一致
    - 允许用户使用委派标志创建 RoleAssignment
        - 用户现在可以使用 New-AzureRMRoleAssignment，其中的一个选项是添加委派标志
    - 修复了可接受作用域参数的 RoleAssignment get 的问题
    - 在 New-AzureRmRoleAssignment cmdlet 中添加了 ServicePrincipalName 的别名
        - 在使用 New-AzureRmRoleAssignment cmdlet 时，用户现在可以使用 ApplicationId 而非 ServicePrincipalName
* SiteRecovery
    - 在此模块中添加了针对所有 cmdlet 的弃用警告，为下一次发布重大更改做准备。
        - 请参阅即将发布的重大更改指南，详细了解如何从 AzureRM 迁移 cmdlet。
* Sql
    - 添加了使用 Set-AzureRmSqlDatabase 重命名数据库的功能
    - 修复了 https://github.com/Azure/azure-powershell/issues/4974 中提到的问题
        - 为审核 cmdlet 提供无效的 AUDIT_CHANGED_GROUP 值时，不再引发错误。此项将在即将发布的版本中删除。
    - 修复了 https://github.com/Azure/azure-powershell/issues/5046 中提到的问题
        - 不再忽略审核 cmdlet 中的 AuditAction 参数
    - 修复了提供的 StorageKeyType 为“Secondary”时审核 cmdlet 中存在的问题
        - 以前在设置 Blob 审核时，如果为 StorageKeyType 参数提供的值为“Secondary”，会使用主存储帐户密钥而非辅助密钥。
    - 更改 Set-AzureRmSqlServerTransparentDataEncryptionProtector 中确认消息的措辞
* Azure (RDFE)
    - 删除了所有 RemoteApp cmdlet
* Azure.存储
    - 升级到 Azure 存储客户端库 8.6.0 和 Azure 存储 DataMovement 库 0.6.5

自上一版本以来所做的更改：https://github.com/azure/azure-powershell/compare/v5.0.1-November2017...v5.1.1-December2017

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
