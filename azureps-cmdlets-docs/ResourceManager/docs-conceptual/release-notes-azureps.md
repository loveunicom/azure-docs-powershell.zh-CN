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
ms.date: 05/18/2017
ms.openlocfilehash: 97a23180a1fc65d96fdc9dbdffcbe3501a4c4c2a
ms.sourcegitcommit: 226527be7cb647acfe2ea9ab151185053ab3c6db
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/29/2017
---
# <a name="release-notes"></a>发行说明

下面是此版本中对 Azure PowerShell 所做的更改列表。

## <a name="version-400"></a>版本 4.0.0

* 此版本包含重大更改。 请参阅[迁移指南](https://aka.ms/azps-migration-guide)，了解有关更改的详细信息及其对现有脚本的影响。
* ApiManagement
  - 添加了在 New-AzureRmApiManagementGroup 中配置外部组的支持。
* 计费
  - 全新 Cmdlet Get-AzureRmBillingPeriod
    + 用于检索订阅的 Azure 计费周期的 cmdlet。
  - 更新 Cmdlet Get-AzureRmBillingInvoice
  - 新属性 BillingPeriodNames
  - 列表视图中的输出
* 计算
  - 更新了 Set-AzureRmVMAEMExtension 和 Test-AzureRmVMAEMExtension cmdlet，以支持高级托管磁盘
  - 用于 IaaS VM 和故障还原的备份加密设置
  - ChefServiceInterval 选项现已重命名为 ChefDaemonInterval。 但旧名称仍可继续使用。
  - 从 PS VM 对象中删除重复的 DataDiskNames 和 NetworkInterfaceIDs 属性。
  - 让 DataDiskNames 参数在 Remove-AzureRmVMDataDisk 中、NetworkInterfaceIDs 参数在 Remove-AzureRmVMNetworkInterface 中变为可选。
  - 修复 Get cmdlet 返回列表对象时的 Get cmdlet 管道问题。
  - 已重命名与 RDFE cmdlet 冲突的 cmdlet。 有关详细信息，请参阅“问题”https://github.com/Azure/azure-powershell/issues/2917
    + `New-AzureVMSqlServerAutoBackupConfig` 已重名为 `New-AzureRmVMSqlServerAutoBackupConfig`
    + `New-AzureVMSqlServerAutoPatchingConfig` 已重名为 `New-AzureRmVMSqlServerAutoPatchingConfig`
    + `New-AzureVMSqlServerKeyVaultCredentialConfig` 已重名为 `New-AzureRmVMSqlServerKeyVaultCredentialConfig`
* 消耗
  - 新 Cmdlet Get-AzureRmConsumptionUsageDetail
    + 用于检索订阅详细使用情况的 cmdlet。
* ContainerRegistry
  - 为 Azure 容器注册表添加 PowerShell cmdlet
    + New-AzureRmContainerRegistry
    + Get-AzureRmContainerRegistry
    + Update-AzureRmContainerRegistry
    + Remove-AzureRmContainerRegistry
    + Get-AzureRmContainerRegistryCredential
    + Update-AzureRmContainerRegistryCredential
    + Test-AzureRmContainerRegistryNameAvailability
* DataLakeAnalytics
  - 添加对获取和列出目录包的支持
  - 添加了从更深上级列出以下目录项的支持：
    + 表
    + TVF
    + 查看
    + 统计信息
* DataLakeStore
  - 对于 `Import-AzureRMDataLakeStoreItem` 和 `Export-AzureRMDataLakeStoreItem`，默认情况下禁用跟踪日志记录功能以提高性能。 如果需要跟踪日志记录，请使用 `-DiagnosticLogLevel` 和 `-DiagnosticLogPath` 参数
  - 修复了向 ADLS 上传大量小文件时可能导致 PowerShell 崩溃的 bug。
* EventHub
  - Bug 修复：
    + 修复 Set-AzureRmEventHubNamespace cmdlet 错误 -“层”不能为 null，应为“SkuName”
    + Set-AzureRmEventHub - 修复更新 EventHub 时出现的“未将对象引用设置为对象的实例”错误
* 洞察力
  - Add-AzureRm*AlertRule
    + 返回单个对象：newResource、statusCode、requestId
  - Get-AzureRmAlertRule
    + 现会枚举输出，而不是将其视作单个对象。 其类型未发生更改，仍为列表。
  - Remove-AzureRmAlertRule
    + statusCode 遵循请求返回的状态代码，而之前其状态始终为“确定”。
  - Add-AzureRmAutoscaleSetting
    + 现在返回单个对象（以前返回列表），其中包含 statusCode、requestId 和新创建/更新的资源。
    + 状态代码遵循请求返回的状态，之前其状态始终为“确定”。
  - New-AzureRmAutoscaleRule
    + 已扩展参数 ScaleActionType，该参数现接收以下值：ChangeCount、PercentChangeCount、ExactCount。
  - Remove-AzureRmAutoscaleSetting
    + 输出中的 statusCode 遵循请求返回的状态代码。 之前其状态始终为“确定”。
  - Get-AzureRMLogProfile
    + 现会枚举输出。 以前将其视作单个对象。 和以前一样，输出类型仍为列表。
  - Remove-AzureRmLogProfile
    + 已实现 PassThru 参数。
  - 指标 API
    + SDK 现从 MDM 检索指标。
  - Get-AzureRmMetricDefinition
    + 输出仍为列表，但列表的结构有所更改。
  - Get-AzureRmMetric
    + 已更改调用。 新语法为： Get-AzureRmMetric ResourceId [MetricNames [TimeGrain] [AggregationType] [StartTime] [EndTime]] [DetailedOutput]
    + 输出为列表，其元素的结构有所更改。
* KeyVault
  - 添加对 KeyVault 机密的备份/还原支持
    + 可备份和还原机密，这与当前支持的密钥功能相符

  - 密钥和机密的备份 cmdlet 现在接受相应对象作为输入参数
    + 调用方可能捆绑检索和备份操作：Get-AzureKeyVaultKey -VaultName myVault -Name myKey | Backup-AzureKeyVaultKey

  - 备份 cmdlet 现支持 -Force 开关以覆盖现有文件
    + 请注意：尝试覆盖现有文件这一操作不再引发，而是提示用户选择继续操作的方式。
* LogicApp
  - 交换控制编号灾难恢复 cmdlet 的新参数：
    + 可选 - 用于指定相关控制编号的 AgreementType 参数（“X12”或“Edifact”）
* MachineLearning
  - 使用新版 Azure 机器学习 .Net SDK 并添加新 cmdlet
    + Add-AzureRmMlWebServiceRegionalProperty
  - 帮助文本中的措词小修复。
* 网络
  - 添加了 Test-AzureRmNetworkWatcherConnectivity cmdlet
    + 返回有关指定源 VM 和目标的连接信息
    + 如果源和目标之间无法建立连接，则该 cmdlet 返回问题相关详细信息
* 配置文件
  - 添加了 `Send-Feedback' cmdlet：允许用户启动一组会向 Azure PowerShell 团队发送反馈的提示。
  - 已删除以下别名，因为它们与 Azure 模块中的现有 cmdlet 名称冲突：
    + `Enable-AzureDataCollection`（由 `Enable-AzureRmDataCollection` 支持）
    + `Disable-AzureDataCollection`（由 `Disable-AzureRmDataCollection` 支持）
* 中继
  - 为 Azure 中继添加 cmdlet，让用户能够创建和管理所有 Azure 中继资源。
    + `New-AzureRmRelayNamespace`
    + `Get-AzureRmRelayNamespace`
    + `Set-AzureRmRelayNamespace`
    + `Remove-AzureRmRelayNamespace`
    + `New-AzureRmWcfRelay`
    + `Get-AzureRmWcfRelay`
    + `Set-AzureRmWcfRelay`
    + `Remove-AzureRmWcfRelay`
    + `New-AzureRmRelayHybridConnection`
    + `Get-AzureRmRelayHybridConnection`
    + `Set-AzureRmRelayHybridConnection`
    + `Remove-AzureRmRelayHybridConnection`
    + `Test-AzureRmRelayName`
    + `Get-AzureRmRelayOperation`
    + `New-AzureRmRelayKey`
    + `Get-AzureRmRelayKey`
    + `New-AzureRmRelayAuthorizationRule`
    + `Get-AzureRmRelayAuthorizationRule`
    + `Set-AzureRmRelayAuthorizationRule`
    + `Remove-AzureRmRelayAuthorizationRule`
* 资源
  - 支持 New-AzureRmResourceGroupDeployment 的跨资源组部署
    + 现在，用户可使用嵌套部署在不同资源组之间进行部署。
* ServiceBus

  - Bug 修复：ServiceBus 队列对象属性值设置为 null，该对象用作 Set-AzureRmServiceBusQueue cmdlet 中的输入参数，用于更新队列。
   - 受影响的属性为 LockDuration、EntityAvailabilityStatus、DuplicateDetectionHistoryTimeWindow、MaxDeliveryCount and MessageCount
* ServiceFabric

  - 添加了适用于 Service Fabric 的 cmdlet
    + Add-AzureRmServiceFabricApplicationCertificate 添加将用作应用程序证书的证书
    + Add-AzureRmServiceFabricClientCertificate 向群集设置添加公用名或指纹，以便进行客户端身份验证
    + Add-AzureRmServiceFabricClusterCertificate 向群集添加辅助群集证书，以便滚动显示现有证书
    + Add-AzureRmServiceFabricNodes 向群集添加特定节点类型的节点/VM
    + Add-AzureRmServiceFabricNodeType 向现有群集添加节点类型/VM
    + Get-AzureRmServiceFabricCluster 获取群集资源的详细信息
    + New-AzureRmServiceFabricCluster 新建 ServiceFabric 群集。 此命令包含许多重载，适用于各种方案
    + Remove-AzureRmServiceFabricClientCertificate 删除用于访问群集的客户端证书
    + Remove-AzureRmServiceFabricClusterCertificate 删除用于确保群集安全性的群集证书
    + Remove-AzureRmServiceFabricNodes 从群集中删除特定节点类型的节点
    + Remove-AzureRmServiceFabricNodeType 从群集中删除节点类型
    + Remove-AzureRmServiceFabricSettings 从群集中删除一个或多个 ServiceFabric 设置
    + Set-AzureRmServiceFabricSettings 添加或更新群集的一个或多个 ServiceFabric 设置
    + Set-AzureRmServiceFabricUpgradeType 更改群集的 ServiceFabric 升级类型
    + Update-AzureRmServiceFabricDurability 更改群集的持久性层
    + Update-AzureRmServiceFabricReliability 更改群集的可靠性层
* Sql
  - 向 New-AzureRmSqlDatabase 添加了 -SampleName 参数
  - 更新了故障转移组 cmdlet
  - 删除“Tag”参数
  - 从 Remove-AzureRmSqlDatabaseFailoverGroup cmdlet 中删除“PartnerResourceGroupName”和“PartnerServerName”参数
  - 向 New-cmdlet 和 Set- cmdlet 添加“GracePeriodWithDataLossHours”参数，此参数最终将取代“GracePeriodWithDataLossHour”
  - 已完善并更新文档
  - 更改返回对象的格式，并修复一些有关漏填字段的 Bug
  - 向故障转移组对象添加“DatabaseNames”和“PartnerLocation”属性
  - 修复导致 Switch- cmdlet 立即返回而不是等待操作完成的 bug
  - 修复使用高宽限期值时出现的整数溢出 bug
  - 如果提供的宽限期低于最小值 1 小时，则将其调整为最小值 1 小时
  - 从 Set-AzureRmSqlDatabaseThreatDetectionPolicy cmdlet 和 Set-AzureRmSqlServerThreatDetectionPolicy cmdlet 的“ExcludedDetectionType”参数的接受值中删除“Usage_Anomaly”。
* 存储
  - 将 SRP SDK 升级到 6.3.0
  - New/Set-AzureRmStorageAccount：添加新参数，用于支持 EnableHttpsTrafficOnly
  - New/Set/Get-AzureRmStorageAccount：返回的存储帐户包含新属性 EnableHttpsTrafficOnly
* Azure.Storage
  - 升级到 Azure 存储客户端库 8.1.1 和 Azure 存储 DataMovement 库 0.5.1
  - 添加一个新 cmdlet，用于支持 blob 增量复制功能
