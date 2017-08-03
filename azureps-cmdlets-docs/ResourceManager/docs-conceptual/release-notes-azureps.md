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
ms.date: 07/26/2017
ms.openlocfilehash: cc2fe75f498f9043e5a4b632c144877af0143173
ms.sourcegitcommit: 20bcef86db4e4869125bb63085fcffd009c19280
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/27/2017
---
# <a name="release-notes"></a>发行说明

下面是此版本中对 Azure PowerShell 所做的更改列表。

## <a name="20170717---version-421"></a>2017.07.17 - 版本 4.2.1
* 计算
    - 修复 VM 磁盘和 VM 磁盘快照创建和更新 cmdlet 的问题，（链接）[https://github.com/azure/azure-powershell/issues/4309]
      - New-AzureRmDisk
      - New-AzureRmSnapshot
      - Update-AzureRmDisk
      - Update-AzureRmSnapshot
* 配置文件
    - 修复 RDFE 中非交互用户身份验证的问题（链接）[https://github.com/Azure/azure-powershell/issues/4299]
* ServiceManagement
    - 修复非交互用户身份验证的问题（链接）[https://github.com/Azure/azure-powershell/issues/4299]

## <a name="2017711---version-420"></a>2017.7.11 - 版本 4.2.0
* AnalysisServices
    * 添加新的 dataplane API
        - 引入了 API，提取 AS 服务器日志 Export-AzureAnalysisServicesInstanceLog
* 自动化
    * 正确设置 New-AzureRmAutomationSchedule“每周”和“每月”计划的时区值
        - 此问题中提供详细信息：https://github.com/Azure/azure-powershell/issues/3043
* AzureBatch
    - 添加了新的 Get-AzureBatchJobPreparationAndReleaseTaskStatus cmdlet。
    - 向 Get-AzureBatchNodeFileContent 参数添加了字节范围开始和结束。
* 认知服务
    * 与认知服务管理 SDK 版本 1.0.0 集成。
    * 修复帐户名称长度检查 bug。
* 计算
    * 映像磁盘的存储帐户类型支持：
        - 已将“StorageAccountType”参数添加到 Set-AzureRmImageOsDisk 和 Add-AzureRmImageDataDisk
    * Vmss Ip 配置中的 PrivateIP 和 PublicIP 功能：
        - 已将“PrivateIPAddressVersion”、“PublicIPAddressConfigurationName”、“PublicIPAddressConfigurationIdleTimeoutInMinutes”、“DnsSetting”名称添加到 New-AzureRmVmssIpConfig
        - 已将用于指定 IPv4 或 IPv6 的“PrivateIPAddressVersion”参数添加到 New-AzureRmVmssIpConfig
    * 性能维护功能：
        - 已将“PerformMaintenance”开关参数添加到 Restart-AzureRmVM。
        - Get-AzureRmVM -Status 显示给定 VM 性能维护的信息
    * 虚拟机标识功能：
        - 已将“IdentityType”参数添加到 New-AzureRmVMConfig 和 UpdateAzureRmVM
        - Get AzureRmVM 显示给定 VM 的标识信息
    * Vmss 标识功能：
        - 已将“IdentityType”参数添加到 New-AzureRmVmssConfig
        - Get-AzureRmVmss 显示给定 Vmss 的标识信息
    * Vmss 启动诊断功能：
        - 用于设置 Vmss 对象的启动诊断的新 cmdlet：Set-AzureRmVmssBootDiagnostics
        - 已将“BootDiagnostic”参数添加到 New-AzureRmVmssConfig
    * Vmss LicenseType 功能：
        - 已将“LicenseType”参数添加到 New-AzureRmVmssConfig
    * RecoveryPolicyMode 支持：
        - 已将“RecoveryPolicyMode”参数添加到 New-AzureRmVmssConfig
    * 计算资源 Sku 功能：
        - 新的 cmdlet“Get AzureRmComputeResourceSku”列出所有计算资源 sku
* 数据工厂
    * 弃用 New-AzureRmDataFactoryGatewayKey
    * 通过添加 New-AzureRmDataFactoryGatewayAuthKey 和 Get-AzureRmDataFactoryGatewayAuthKey 引入网关身份验证密钥功能
* DataLakeAnalytics
    * 通过以下命令添加对计算策略 CRUD 的支持：
        - New-AzureRMDataLakeAnalyticsComputePolicy
        - Get-AzureRMDataLakeAnalyticsComputePolicy
        - Remove-AzureRMDataLakeAnalyticsComputePolicy
        - Update-AzureRMDataLakeAnalyticsComputePolicy
    * 添加对作业关系元数据的支持，为定期作业和作业管道提供帮助。 已更新或已添加以下命令：
        - Submit-AzureRMDataLakeAnalyticsJob
        - Get-AzureRMDataLakeAnalyticsJob
        - Get-AzureRMDataLakeAnalyticsJobRecurrence
        - Get-AzureRMDataLakeAnalyticsJobPipeline
    * 已更新作业和目录 API 的令牌受众，使用正确的 Data Lake 特定受众而不是 Azure 资源受众。
* DataLakeStore
    * 在 Set-AzureRMDataLakeStoreAccount cmdlet 中添加了对用户托管 KeyVault 密钥轮换的支持
    * 添加了生命周期质量更新，在添加用户托管 KeyVault 或轮换密钥时自动触发 `enableKeyVault` 调用。
    * 已更新作业和目录 API 的令牌受众，使用正确的 Data Lake 特定受众而不是 Azure 资源受众。
    * 使用以下 cmdlet 修复了限制已创建/追加文件的大小 bug：
        - New-AzureRmDataLakeStoreItem
        - Add-AzureRmDataLakeStoreItemContent
* Dns
    * 修复 Get AzureRmDnsZone 的管道方案中的 bug
        - 此处提供详细信息：https://github.com/Azure/azure-powershell/issues/4203
* HDInsight
    * 添加了支持以启用/禁用 Operations Management Suite (OMS)
    * 新 cmdlet
        - Enable-AzureRmHDInsightOperationsManagementSuite
        - Disable-AzureRmHDInsightOperationsManagementSuite
        - Get-AzureRmHDInsightOperationsManagementSuite
    * 添加新参数，将 Spark 自定义配置设置为 Add-AzureRmHDInsightConfigValues
        - 适用于 Spark 1.6 的参数 SparkDefaults 和 SparkThriftConf
        - 适用于 Spark 2.0 的参数 Spark2Defaults 和 Spark2ThriftConf
* 洞察力
    * 问题 #4215（更改请求）删除了 Get-AzureRmLog cmdlet 时间范围中的 15 天限制。 此外还对单元测试名称进行了细微的更改。
    * 已为 Get-AzureRmLog 修复了问题 #3957
        - 问题 #1：后端以每页 200 条记录的形式返回记录，由继续标记链接到下一页。 客户看到该 cmdlet 仅返回 200 条记录，但他们知道还有更多记录。 无论对 MaxEvents 设置何值（除非该值小于 200）都会出现这种情况。
        - 问题 2：文档包含此 cmdlet 相关的错误数据，例如：默认时间范围为 1 小时。
        - 修复 #1：cmdlet 现遵循后端返回的继续标记，直到它达到 MaxEvents 值或该组的末尾。<br>MaxEvents 的默认值为 1000，其最大值为 100000。 将忽略小于 1 的任何 MaxEvents 值，改用默认值。 这些值和行为没有更改，现在可以正确记录它们。<br>已添加 MaxEvents 的别名 - MaxRecords，因为该 cmdlet 的名称没有再提及事件，只提及日志。
        - 修复 #2：文档包含正确信息以及更多详细信息：新别名、正确的时间范围、正确的默认值、最小值和最大值。
* KeyVault
    * 将 -UserPrincipalName 指定为 Set-AzureRMKeyVaultAccessPolicy 和 Remove-AzureRMKeyVaultAccessPolicy cmdlet 时，从目录查询中删除电子邮件地址。
      - 这两个 Cmdlet 现拥有在适合查询电子邮件地址时，可使用的 -EmailAddress 参数（而不是 -UserPrincipalName 参数）。  如果目录中存在多个匹配的电子邮件地址，Cmdlet 将失败。
* 网络
    * New-AzureRmIpsecPolicy：SALifeTimeSeconds 和 SADataSizeKilobytes 不再是必需参数
        - SALifeTimeSeconds 默认值为 27000 秒
        - SADataSizeKilobytes 默认值为 102400000 KB
    * 通过使用 ssl 策略并列出应用程序网关中的所有 ssl 选项 api，添加了对自定义密码套件配置的支持
        - 添加了可选参数 -PolicyType、-PolicyName、-MinProtocolVersion、-Ciphersuite
            - Add-AzureRmApplicationGatewaySslPolicy
            - New-AzureRmApplicationGatewaySslPolicy
            - Set-AzureRmApplicationGatewaySslPolicy
        - 添加了 Get-AzureRmApplicationGatewayAvailableSslOptions（别名：List-AzureRmApplicationGatewayAvailableSslOptions）
        - 添加了 Get AzureRmApplicationGatewaySslPredefinedPolicy（别名：List-AzureRmApplicationGatewaySslPredefinedPolicy）
    * 在应用程序网关中添加了重定向支持
        - 添加了 Add-AzureRmApplicationGatewayRedirectConfiguration
        - 添加了 Get-AzureRmApplicationGatewayRedirectConfiguration
        - 添加了 New-AzureRmApplicationGatewayRedirectConfiguration
        - 添加了 Remove-AzureRmApplicationGatewayRedirectConfiguration
        - 添加了 Set-AzureRmApplicationGatewayRedirectConfiguration
        - 添加了可选参数 -RedirectConfiguration
            - Add-AzureRmApplicationGatewayRequestRoutingRule
            - New-AzureRmApplicationGatewayRequestRoutingRule
            - Set-AzureRmApplicationGatewayRequestRoutingRule
        - 添加了可选参数 -DefaultRedirectConfiguration
            - Add-AzureRmApplicationGatewayUrlPathMapConfig
            - New-AzureRmApplicationGatewayUrlPathMapConfig
            - Set-AzureRmApplicationGatewayUrlPathMapConfig
        - 添加了可选参数 -RedirectConfiguration
            - Add-AzureRmApplicationGatewayPathRuleConfig
            - New-AzureRmApplicationGatewayPathRuleConfig
            - Set-AzureRmApplicationGatewayPathRuleConfig
        - 添加了可选参数 -RedirectConfigurations
            - New-AzureRmApplicationGateway
            - Set-AzureRmApplicationGateway
    * 添加了在应用程序网关中对 Azure 网站的支持
        - 添加了 New-AzureRmApplicationGatewayProbeHealthResponseMatch
        - 添加了可选参数 -PickHostNameFromBackendHttpSettings、-MinServers、-Match
            - Add-AzureRmApplicationGatewayProbeConfig
            - New-AzureRmApplicationGatewayProbeConfig
            - Set-AzureRmApplicationGatewayProbeConfig
        - 添加了可选参数 -PickHostNameFromBackendAddress、-AffinityCookieName、-ProbeEnabled、-Path
            - Add-AzureRmApplicationGatewayBackendHttpSettings
            - New-AzureRmApplicationGatewayBackendHttpSettings
            - Set-AzureRmApplicationGatewayBackendHttpSettings
    * 更新 Get-AzureRmPublicIPaddress，检索通过 VM 规模集创建的 publicipaddress 资源
    * 添加了 cmdlet 来获取虚拟网络当前的使用情况
        - Get-AzureRmVirtualNetworkUsageList
* 配置文件
    * 修复了使用 Import-AzureRmContext 或 Save-AzureRmContext 时的错误
        - 此问题中提供详细信息：https://github.com/Azure/azure-powershell/issues/3954
* RecoveryServices.SiteRecovery
    * 为 Azure Site Recovery 操作引入新模块。
        - 所有 cmdlet 都以 AzureRmRecoveryServicesAsr* 开头
* Sql
    * 将数据同步 PowerShell Cmdlet 添加到 AzureRM.Sql
    * 更新了 AzureRmSqlServer cmdlet，使用创建服务器时可避免超时的 REST API 新版本。
    * 已弃用服务器升级 cmdlet，因为旧版服务器 (2.0) 不再存在。
    * 将新的可选开关参数“AssignIdentity”添加到 New-AzureRmSqlServer 和 Set-AzureRmSqlServer cmdlet 中，支持预配 SQL Server 资源的资源标识
    * 参数 ResourceGroupName 现对于 Get AzureRmSqlServer 来说可选
        - 以下问题中提供详细信息：https://github.com/Azure/azure-powershell/issues/635
* ExpressRoute 的 ServiceManagement：
    * 更新了 New-AzureBgpPeering cmdlet 以添加以下选项：
        - PeerAddressType：可指定值“IPv4”或“IPv6”，创建相应地址系列类型的 BGP 对等互连
    * 更新了 Set-AzureBgpPeering cmdlet 以添加以下选项：
        - PeerAddressType：可指定值“IPv4”或“IPv6”，以更新相应地址系列类型的 BGP 对等互连
    * 更新了 Remove-AzureBgpPeering cmdlet 以添加以下选项：
        - PeerAddressType：可指定值“IPv4”、“IPv6”或“全部”，以删除相应地址或全部地址系列类型的 BGP 对等互连

## <a name="20170607---version-410"></a>2017.06.07 - 版本 4.1.0
* AnalysisServices
    * 新增 SKU：B1、B2、S0
    * 添加了增加/减少支持
* 认知服务
    * 更新创建认知服务资源时许可协议的详细显示
* 计算
    * 为含多个托管磁盘的虚拟机修复 Test-AzureRmVMAEMExtension
    * 更新了 Set-AzureRmVMAEMExtension：添加高级托管磁盘的缓存信息
    * Add-AzureRmVhd：对 vhd 的大小限制增加到了 4 TB。
    * Stop-AzureRmVM：阐明 STayProvisioned 参数的文档
    * New-AzureRmDiskUpdateConfig
      * 已弃用参数 CreateOption、StorageAccountId、ImageReference、SourceUri、SourceResourceId
    * Set-AzureRmDiskUpdateImageReference：已弃用 cmdlet
    * New-AzureRmSnapshotUpdateConfig
      * 已弃用参数 CreateOption、StorageAccountId、ImageReference、SourceUri、SourceResourceId
    * Set-AzureRmSnapshotUpdateImageReference：已弃用 cmdlet
* DataLakeStore
    * Enable-AzureRmDataLakeStoreKeyVault (Enable-AdlStoreKeyVault)
      * 为 DataLake Store 启用 KeyVault 托管加密
* DevTestLabs
    * 更新 cmdlet，使其与当前版本和更新的开发测试实验室 API 版本一起使用。
* IotHub
    * 添加对 IoTHub cmdlet 的路由支持
* KeyVault
  * 支持 KeyVault 托管存储帐户密钥的新 Cmdlet
    * Get-AzureKeyVaultManagedStorageAccount
    * Add-AzureKeyVaultManagedStorageAccount
    * Remove-AzureKeyVaultManagedStorageAccount
    * Update-AzureKeyVaultManagedStorageAccount
    * Update-AzureKeyVaultManagedStorageAccountKey
    * Get-AzureKeyVaultManagedStorageSasDefinition
    * Set-AzureKeyVaultManagedStorageSasDefinition
    * Remove-AzureKeyVaultManagedStorageSasDefinition
* 网络
    * Get AzureRmNetworkUsage：显示网络使用情况和容量详细信息的新 cmdlet
    * 为 VirtualNetworkGateways 添加了新的 GatewaySku 选项
        * VpnGw1、VpnGw2、VpnGw3 是为 Vpn 网关添加的新 Sku
    * Set-AzureRmNetworkWatcherConfigFlowLog
      * 已修复的帮助示例
* 通知中心
    * 新 API 的 NotificationHubs cmdlet 的透明更新
* 配置文件
    * Resolve-AzureRmError
      * 显示 cmdlet 引发的错误和异常的详细信息（包括服务器请求/响应数据）的新 cmdlet
    * Send-Feedback
      * 已启用在不登录的情况下发送反馈的功能
    * Get-AzureRmSubscription
      * 修复检索 CSP 订阅时的 bug
* 资源
    * 已修复以下问题：如果 roleassignments 数大于 1000，Get-AzureRMRoleAssignment 将导致错误请求
        * 现在，即使要返回的 roleassignments 数大于 1000，用户也可使用 Get-AzureRMRoleAssignment
* Sql
    * Restore-AzureRmSqlDatabase：更新文档示例
* 存储
    * 将 AssignIdentity 设置支持添加到资源模式存储帐户 cmdlet
        * New-AzureRmStorageAccount
        * Set-AzureRmStorageAccount
    * 将客户密钥支持添加到资源模式存储帐户 cmdlet
        * Set-AzureRmStorageAccount
        * New-AzureRmStorageAccountEncryptionKeySource
* TrafficManager

    * 新的监视设置“MonitorIntervalInSeconds”、“MonitorTimeoutInSeconds”、“MonitorToleratedNumberOfFailures”
    * 新监视协议“TCP”
* ServiceManagement
    * Add-AzureVhd：对 vhd 的大小限制增加到了 4 TB。
    * New-AzureBGPPeering：支持 LegacyMode
* Azure.Storage
    * 更新针对接受通配符的参数的帮助并更新 StorageContext 类型

## <a name="20170523---version-402"></a>2017.05.23 - 版本 4.0.2
* 配置文件
    * Add-AzureRmAccount
      * 添加了 `-EnvironmentName` 参数别名，实现与 AzureRM.profile 2.x 版的后向兼容性

## <a name="20170512---version-401"></a>2017.05.12 - 版本 4.0.1
 * 修复了 New-AzureStorageContext 在脱机情况下的问题：https://github.com/Azure/azure-powershell/issues/3939

## <a name="20170510---version-400"></a>2017.05.10 - 版本 4.0.0


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
