---
title: Azure PowerShell 更改日志 | Microsoft Docs
description: 下面提供了对 Azure PowerShell 最新版本所做更改的历史记录。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 07/26/2017
ms.openlocfilehash: 6f0e304c499fc8bf4909e2825d52cd63b1fcbf5d
ms.sourcegitcommit: 990f82648b0aa2e970f96c02466a7134077c8c56
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/11/2018
ms.locfileid: "38100485"
---
# <a name="release-notes"></a>发行说明

下面是此版本中对 Azure PowerShell 所做的更改列表。

## <a name="20170925---version-440"></a>2017.09.25 - 版本 4.4.0
* AnalysisServices
  * 添加了新的数据平面 cmdlet，用于将数据库从读写实例同步到只读实例
    - 包含了 cmdlet 的帮助文件
    - 添加了内存中测试和方案测试（仅限实时）
  * 修复了 Add-AzureAsAccount cmdlet 中的 bug
* 自动化
  * 纠正了前一版本中修复的 cmdlet 的帮助文档。
  * 添加了 4 个新 cmdlet 用于支持 DSC 节点配置的分阶段实施。
    - Start-AzureRmAutomationDscNodeConfigurationDeployment
    - Stop-AzureRmAutomationDscNodeConfigurationDeployment
    - Get-AzureRmAutomationDscNodeConfigurationDeployment
    - Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule
* 认知服务
  * 与认知服务管理 SDK 版本 2.0.0 集成。
  * Get-AzureRmCognitiveServicesAccount 现在可以正确支持分页。
* 计算
  * Run 命令功能：
    - 新 cmdlet“Invoke-AzureRmVMRunCommand”在 VM 上调用 run 命令
    - 新 cmdlet“Get-AzureRmVMRunCommandDocument”显示可用的 run 命令文档
  * 将“StorageAccountType”参数添加到 Set-AzureRmDataDisk
  * 虚拟机、VM 规模集和磁盘的可用性区域支持
    - 已将新参数“Zone”添加到 New-AzureRmVM、New-AzureRmVMConfig、New-AzureRmVmssConfig、New-AzureRmDiskConfig
  * VM 规模集滚动升级功能：
    - 新 cmdlet“Start-AzureRmVmssRollingOSUpgrade”调用 VM 规模集的 OS 滚动升级
    - 新 cmdlet“Set-AzureRmVmssRollingUpgradePolicy”为 VM 规模集滚动升级设置升级策略。
    - 新 cmdlet“Stop-AzureRmVmssRollingUpgrade”取消 VM 规模集的滚动升级
    - 新 cmdlet“Get-AzureRmVmssRollingUpgrade”显示 VM 规模集滚动升级的状态。
  * 为系统分配的标识引入了 AssignIdentity 开关参数。
    - 已将新参数“AssignIdentity”添加到 New-AzureRmVMConfig、New-AzureRmVmssConfig 和 Update-AzureRmVM
  * VMSS 磁盘加密功能：
    - 新 cmdlet“Set-AzureRmVmssDiskEncryptionExtension”在 VM 规模集上启用磁盘加密
    - 新 cmdlet“Disable-AzureRmVmssDiskEncryption”在 VM 规模集上禁用磁盘加密
    - 新 cmdlet“Get-AzureRmVmssDiskEncryptionStatus”显示 VM 规模集的磁盘加密状态
    - 新 cmdlet“Get-AzureRmVmssVMDiskEncryptionStatus”显示 VM 规模集中 VM 的磁盘加密状态
* ContainerInstance
  * 为 Azure 容器实例添加 PowerShell cmdlet
    - New-AzureRmContainerGroup
    - Get-AzureRmContainerGroup
    - Remove-AzureRmContainerGroup
    - Get-AzureRmContainerInstanceLog
* 洞察力
  * 新 cmdlet Disable-AzureRmActivityLogAlert
    - 用于禁用现有活动日志警报的新 cmdlet。
    - 也可以选择性地为此 cmdlet 设置标记。
  * 新 cmdlet Enable-AzureRmActivityLogAlert
    - 用于启用现有活动日志警报的新 cmdlet。
    - 也可以选择性地为此 cmdlet 设置标记。
  * 新 cmdlet Get-AzureRmActivityLogAlert
    - 用于检索一个或多个活动日志警报的新 cmdlet。
    - 可按名称、资源组或订阅检索警报。
  * 新 cmdlet New-AzureRmActionGroup
    - 用于在内存中创建 ActionGroup 对象的新 cmdlet（不涉及请求。）
  * 新 cmdlet New-AzureRmActivityLogAlertCondition
    - 用于在内存中创建活动日志警报叶条件对象的新 cmdlet（不涉及请求。）
  * 新 cmdlet Set-AzureRmActivityLogAlert
    - 用于创建或更新活动日志警报的新 cmdlet。
  * 新 cmdlet Remove-AzureRmActivityLogAlert
    - 用于删除一个活动日志警报的新 cmdlet。
  * 新 cmdlet Set-AzureRmActionGroup
    - 用于新建或更新现有操作组的新 cmdlet。
  * 新 cmdlet Get-AzureRmActionGroup
    - 用于检索一个或多个操作组的新 cmdlet。
    - 可按名称、资源组或订阅检索操作组。
  * 新 cmdlet Remove-AzureRmActionGroup
    - 用于检索一个操作组的新 cmdlet。
  * 新 cmdlet New-AzureRmActionGroupReceiver
    - 用于在内存中新建操作组接收器的新 cmdlet。
* KeyVault
  * 用于支持软删除 KeyVault 证书的新/更新 Cmdlet
    * Get-AzureKeyVaultCertificate
    * Remove-AzureKeyVaultCertificate
    * Undo-AzureKeyVaultCertificateRemoval
* 网络
  * 为虚拟网络子网添加了终结点服务支持
    - 更新了 Add-AzureRmVirtualSubnetConfig：添加了可选参数 -ServiceEndpoint
    - 更新了 New-AzureRmVirtualSubnetConfig：添加了可选参数 -ServiceEndpoint
    - 更新了 Set-AzureRmVirtualSubnetConfig：添加了可选参数 -ServiceEndpoint
  * 添加了 cmdlet 用于列出位置中的可用终结点服务
    - Get-AzureRmVirtualNetworkAvailableEndpointService
  * 为以下 cmdlet 添加了配置基于外部 Radius 的 P2S 身份验证的功能
    - New-AzureVirtualNetworkGateway
    - Set-AzureVirtualNetworkGateway
    - Set-AzureRmVirtualNetworkGatewayVpnClientConfig
  * 添加了 cmdlet 用于生成基于外部 Radius 的 P2S 的 VpnProfiles
    - New-AzureRmVpnClientConfiguration
    - Get-AzureRmVpnClientConfiguration
  * 添加了针对公共 IP 地址和负载均衡器的 SKU 参数支持
    - 更新了 New-AzureRMLoadBalancer：添加了可选参数 -Sku
    - 更新了 New-AzureRMPublicIpAddress：添加了可选参数 -Sku
  * 为负载均衡器规则添加了 DisableOutboundSNAT 支持
    - 更新了 New-AzureRMLoadBalancerRuleConfig：添加了可选参数 DisableOutboundSNAT
    - 更新了 Add-AzureRMLoadBalancerRuleConfig：添加了可选参数 DisableOutboundSNAT
    - 更新了 Set-AzureRMLoadBalancerRuleConfig：添加了可选参数 DisableOutboundSNAT
  * 添加了对 IkeV2 P2S 的支持
    - 更新了 New-AzureRmVirtualNetworkGateway：添加了可选参数 -VpnClientProtocol，默认为 [ "SSTP", "IkeV2" ]
    - 更新了 Set-AzureRmVirtualNetworkGateway：添加了可选参数 -VpnClientProtocol
  * 在网络安全规则和有效网络安全规则中添加了多值规则支持
    - 更新了 Add-AzureRmNetworkSecurityRuleConfig：更新了 SourcePortRange、DestinationPortRange、SourceAddressPrefix 参数以接受字符串列表
    - 更新了 New-AzureRmNetworkSecurityRuleConfig：更新了 SourcePortRange、DestinationPortRange、SourceAddressPrefix 参数以接受字符串列表
    - 更新了 Set-AzureRmNetworkSecurityRuleConfig：更新了 SourcePortRange、DestinationPortRange、SourceAddressPrefix 参数以接受字符串列表
    - 更新了 Add-AzureRmNetworkSecurityRuleConfig：更新了 SourcePortRange、DestinationPortRange、SourceAddressPrefix 参数以接受字符串列表
    - 更新了 New-AzureRmNetworkSecurityGroup：更新了 SecurityRules 参数以接受 SourcePortRange、DestinationPortRange 和 SourceAddressPrefix 参数（PSSecurityRule 对象中的字符串列表）
    - 更新了 Get-AzureRmEffectiveNetworkSecurityGroup：添加了参数 TagMap
    - 更新了 Get-AzureRmEffectiveNetworkSecurityGroup：更新了包含 SourcePortRange、DestinationPortRange 和 SourceAddressPrefix 参数（字符串列表）的 PSEffectiveSecurityRule 返回对象。
  * 添加了虚拟网络的 DDoS 保护支持
    - 更新了 New-azurermvirtualnetwork：添加了开关参数 EnableDDoSProtection 和 EnableVmProtection
    - 在 PSVirtualNetwork 对象中添加了属性 EnableDDoSProtection 和 EnableVmProtection
  * 添加了对高可用性内部负载均衡器的支持
    - 更新了 Add-AzureRmLoadBalancerRuleConfig：添加了 All 作为 Protocol 参数的可接受值
    - 更新了 New-AzureRmLoadBalancerRuleConfig：添加了 All 作为 Protocol 参数的可接受值
    - 更新了 Set-AzureRmLoadBalancerRuleConfig：添加了 All 作为 Protocol 参数的可接受值
  * 添加了对应用程序安全组的支持
    - 添加了 New-AzureRmApplicationSecurityGroup
    - 添加了 Get-AzureRmApplicationSecurityGroup
    - 添加了 Remove-AzureRmApplicationSecurityGroup
    - 更新了 New-AzureRmNetworkInterface：添加了可选参数 ApplicationSecurityGroup 和 ApplicationSecurityGroupId
    - 更新了 New-AzureRmNetworkInterfaceIpConfig：添加了可选参数 ApplicationSecurityGroup 和 ApplicationSecurityGroupId
    - 更新了 Add-AzureRmNetworkInterfaceIpConfig：添加了可选参数 ApplicationSecurityGroup 和 ApplicationSecurityGroupId
    - 更新了 Set-AzureRmNetworkInterfaceIpConfig：添加了可选参数 ApplicationSecurityGroup 和 ApplicationSecurityGroupId
    - 更新了 New-AzureRmNetworkSecurityRuleConfig：添加了可选参数 SourceApplicationSecurityGroup、SourceApplicationSecurityGroupId、DestinationApplicationSecurityGroup 和 DestinationApplicationSecurityGroupId
    - 更新了 Add-AzureRmNetworkSecurityRuleConfig：添加了可选参数 SourceApplicationSecurityGroup、SourceApplicationSecurityGroupId、DestinationApplicationSecurityGroup 和 DestinationApplicationSecurityGroupId
    - 更新了 Set-AzureRmNetworkSecurityRuleConfig：添加了可选参数 SourceApplicationSecurityGroup、SourceApplicationSecurityGroupId、DestinationApplicationSecurityGroup 和 DestinationApplicationSecurityGroupId
  * 为 VpnDeviceConfiguration 脚本添加了新命令
    - Get-AzureRmVirtualNetworkGatewaySupportedVpnDevices
    - Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript
* 配置文件
  * AzureRm cmdlet 的 Start-Job 支持。
    * 所有 AzureRm cmdlet 都添加了可接受上下文（Context cmdlet 的输出）的 -AzureRmContext 参数。
      - 具有 DISABLED 上下文持久性的作业的通用模式：`Start-Job {param ($context) New-AzureRmVM -AzureRmContext $context [... other parameters]} -ArgumentList (Get-AzureRmContext)`
      - 具有 ENABLED 上下文持久性的作业的通用模式：`Start-Job {New-AzureRmVM [... other parameters]}`
  * 在不同会话之间持久保留登录信息，新 cmdlet：
    - Enable-AzureRmContextAutosave - 在不同的会话之间启用凭据持久性。
    - Disable-AzureRmContextAutosave - 在不同的会话之间禁用凭据持久性。
  * 管理上下文信息，新 cmdlet
    - Select-AzureRmContext - 选择处于活动状态的命名上下文。
    - Rename-AzureRmContext - 重命名现有上下文以方便引用。
    - Remove-AzureRmContext - 删除现有上下文。
    - Remove-AzureRmAccount - 删除与帐户关联的所有凭据、订阅和租户。
  * 管理上下文信息，cmdlet 更改：
    - 为更改凭据的所有 cmdlet 添加了 Scope = (Process | CurrentUser)
    - Get-AzureRmContext - 添加了 ListAvailable 参数用于列出所有已保存的上下文
* 资源
  * 添加 PolicySetDefinition cmdlet
    - 用于创建策略集定义的 New-AzureRmPolicySetDefinition cmdlet
    - 用于列出所有策略集定义或获取特定策略集定义的 Get-AzureRmPolicySetDefinition cmdlet
    - 用于删除策略集定义的 Remove-AzureRmPolicySetDefinition cmdlet
    - 用于更新现有策略集定义的 Set-AzureRmPolicySetDefinition cmdlet
  * 将 -PolicySetDefinition、-Sku 和 -NotScope 参数添加到 New-AzureRmPolicyAssignment 和 Set-AzureRmPolicyAssignment cmdlet
  * 在 New-AzureRmPolicyDefinition 和 Set-AzureRmPolicyDefinition cmdlet 中添加传入策略 URL 的支持
  * 将 -Mode 参数添加到 New-AzureRmPolicyDefinition cmdlet
  * 添加使用 PSRoleAssignment 对象删除角色分配的支持
    - 用户现在可以结合 Remove-AzureRMRoleAssignment cmdlet 使用 PSRoleassignmnet 输入对象来删除角色分配。
  * 添加 ManagedApplication cmdlet
    - 用于创建托管应用程序的 New-AzureRmManagedApplication cmdlet
    - 用于列出订阅下的所有托管应用程序或获取特定托管应用程序的 Get-AzureRmManagedApplication cmdlet
    - 用于删除托管应用程序的 Remove-AzureRmManagedApplication cmdlet
    - 用于更新现有托管应用程序的 Set-AzureRmManagedApplication cmdlet
  * 添加 ManagedApplicationDefinition cmdlet
    - 用于通过 zip 文件 URI 或通过 mainTemplate 和 createUiDefinition json 文件创建托管应用程序定义的 New-AzureRmManagedApplicationDefinition cmdlet
    - 用于列出资源组下的所有托管应用程序定义或获取特定托管应用程序定义的 Get-AzureRmManagedApplicationDefinition cmdlet
    - 用于删除托管应用程序定义的 Remove-AzureRmManagedApplicationDefinition cmdlet
    - 用于更新现有托管应用程序定义的 Set-AzureRmManagedApplicationDefinition cmdlet
* Sql
  * 添加虚拟网络规则的支持
    - 添加 Get-AzureRmSqlServerVirtualNetworkRule cmdlet，用于按特定规则名称获取虚拟网络规则，或获取 Azure SQL 服务器中的虚拟网络规则列表。
    - 添加 Set-AzureRmSqlServerVirtualNetworkRule cmdlet，用于更改规则指向的虚拟网络。
    - 添加 Remove-AzureRmSqlServerVirtualNetworkRule cmdlet，用于删除 Azure SQL 服务器的虚拟网络规则。
    - 添加 New-AzureRmSqlServerVirtualNetworkRule cmdlet，用于新建 Azure SQL 服务器的虚拟网络规则。
* 网站
  * 为应用服务计划添加 PremiumV2 层
* Azure.存储
  * 升级到 Azure 存储客户端库 8.4.0 和 Azure 存储 DataMovement 库 0.6.1
  * 在上传和复制 Blob API 中添加 PremiumPageBlobTier 支持
    - Set-AzureStorageBlobContent
    - Start-AzureStorageBlobCopy
  * 优化 AzureStorageContainer、AzureStorageBlob、AzureStorageQueue 和 AzureStorageTable 的控制台输出格式
    - Get-AzureStorageContainer
    - Get-AzureStorageBlob
    - Get-AzureStorageQueue
    - Get-AzureStorageTable

## <a name="20170810---version-431"></a>2017.08.10 - 版本 4.3.1
  * 修复程序集签名问题的更新

## <a name="20170807---version-430"></a>2017.08.07 - 版本 4.3.0
* AnalysisServices
  * 修复了 Set-AzureRmAnalysisServciesServer 中的 bug
    - 如果未提供管理员，将删除该管理员。
  * New-AzureRmAnalysisServicesServer 和 Set-AzureRmAnalysisServicesServer 中添加了 BackupBlobContainerUri
    - 启用可设置/禁用用于备份/还原 Azure Analysis Services 服务器的备份 blob 容器
  * 更新了 New-AzureRmAnalysisServicesServer 和 Set-AzureRmAnalysisServicesServer 中的 SKU 查找
    - 将硬编码 SKU 改为动态查找。
  * Add-AzureAnalysisServicesAccount 支持通过服务主体登录
* 自动化
  * 对 AutomationDSC* cmdlet 进行了修改，可拉取超过 100 条记录
  * 解决了调用某些自动化 cmdlet（如 Get-AzureRmAutomationVariable、Get-AzureRmAutomationJob）之后，详细流停止工作的问题。
  * StartAzureAutomationDscCompilationJob 和 ImportAzureAutomationDscNodeConfiguration 中添加了对 NodeConfiguration 生成版本控制的支持
  * 针对现有问题进行了 bug 修复 - 修复了 #3775 别名问题、 runOn 别名以及对 HybridWorkers 的支持。
* 计算
  * Set-AzureRmVMAEMExtension：添加对新高级磁盘大小的支持
  * Set-AzureRmVMAEMExtension：添加对 M 系列的支持
  * 向 Add-AzureRmVmssExtension 添加 ForceUpdateTag 参数
  * 向 New-AzureRmVmssIpConfig 添加 Primary 参数
  * 向 Add-AzureRmVmssNetworkInterfaceConfig 添加 EnableAcceleratedNetworking 参数
  * 向 Set-AzureRmVmss 添加 InstanceId
  * 向 Get-AzureRmVM -Status 输出公开 MaintenanceRedeployStatus
  * 向 Get-AzureRmComputeResourceSku 的表格格式公开限制和功能
* DataLakeStore
  * 修复问题：https://github.com/Azure/azure-powershell/issues/4323
* EventHub
  * 向 NamespaceAttributes 添加了 ResourceGroup 属性
    - “ResourceGroup”获取命名空间所在资源组的名称
  * cmdlet 已使用 Namespace 的 Parameterset 和 AuthorizationRule 操作的 EventHub 更新
    - New-AzureRmEventHubAuthorizationRule - 向现有 NameSpace 或 EventHub 添加新的 AuthorizationRule。
    - Get-AzureRmEventHubAuthorizationRule - 获取现有 NameSpace 或 EventHub 的 AuthorizationRule 或 AuthorizationRule 列表。
    - Set-AzureRmEventHubAuthorizationRule - 更新 EventHub NameSpace 的现有 AuthorizationRule 属性。
    - Remove-AzureRmEventHubAuthorizationRule - 删除现有 NameSpace 或 EventHub 的现有 AuthorizationRule。
    - New-AzureRmEventHubKey - 为现有 NameSpace 或 EventHub 的 AuthorizationRule 生成新的主密钥或辅助密钥。
    - Get-AzureRmEventHubKey - 获取现有 NameSpace 或 EventHub 的 AuthorizationRule 主密钥或辅助密钥。
* 网络
    * 添加了 IPv6 支持和新的可选参数 -PeerAddressType
      * New-AzureRmExpressRouteCircuitPeeringConfig：
      * Set-AzureRmExpressRouteCircuitPeeringConfig：添加了 IPv6 支持。 添加了新的可选参数
      * Remove-AzureRmExpressRouteCircuitPeeringConfig：添加了 IPv6 支持。 添加了新的可选参数
    * 参数 -ProbeEnabled 标记为“已过时”
      - Add-AzureRmApplicationGatewayBackendHttpSettings
      - New-AzureRmApplicationGatewayBackendHttpSettings
      - Set-AzureRmApplicationGatewayBackendHttpSettings
* 配置文件
    * 数据收集在默认情况下处于启用状态。 Microsoft 收集使用情况数据以改进用户体验。 数据是匿名的，不会包括命令行参数值。
      - 使用 Disable-AzureRmDataCollection cmdlet 可关闭此功能
      - 使用 Enable-AzureRmDataCollection cmdlet 可打开此功能
* 资源
    * 支持将请求发送到 ARM 之前对以下 roledefinition 和 roleassignment commandlet 范围进行验证
      - Get-AzureRMRoleAssignment
      - New-AzureRMRoleAssignment
      - Remove-AzureRMRoleAssignment
      - Get-AzureRMRoleDefinition
      - New-AzureRMRoleDefinition
      - Remove-AzureRMRoleDefinition
      - Set-AzureRMRoleDefinition
* ServiceBus
    * 为 NameSpace、 Queue 和 Topic 的 AuthorizationRule 添加了以下新 commandlet。 根据参数集执行授权规则操作。
     - New-AzureRmServiceBusAuthorizationRule - 向现有 ServiceBus NameSpace/Queue/Topic 添加新的 AuthorizationRule。
     - Get-AzureRmServiceBusAuthorizationRule - 获取现有 ServiceBus NameSpace/Queue/Topic 的 AuthorizationRule 或 AuthorizationRule 列表。
     - Set-AzureRmServiceBusAuthorizationRule - 更新 Servicebus NameSpace/Queue/Topic 的现有 AuthorizationRule 属性。
     - New-AzureRmServiceBusKey - 为现有 ServiceBus NameSpace/Queue/Topic 的 AuthorizationRule 生成新的主密钥或辅助密钥。
     - Get-AzureRmServiceBusKey - 获取现有 ServiceBus NameSpace/Queue/Topic 的 AuthorizationRule 主密钥或辅助密钥。
     - Remove-AzureRmServiceBusNamespaceAuthorizationRule - 删除 ServiceBus NameSpace/Queue/Topic 的现有 AuthorizationRule 属性。
    * 向 NamespceAttributes 添加了 Resource Group 属性
* Sql
    * 更新 Set-AzureRmSqlServerTransparentDataEncryptionProtector，如果加密保护程序类型设置为 AzureKeyVault，则会显示警告并要求确认
    * 为审核设置添加新的已更新 cmdlet
      - Get-AzureRmSqlDatabaseAuditing cmdlet，它可获取 Azure SQL 数据库的审核设置。
      - Get-AzureRmSqlServerAuditing cmdlet，它可获取 Azure SQL Server 的审核设置。
      - Set-AzureRmSqlDatabaseAuditing cmdlet 可更改 Azure SQL 数据库的审核设置。
      - Set-AzureRmSqlServerAuditing cmdlet，它可更改 Azure SQL Server 的审核设置。
    * 弃用现有审核策略 cmdlet
      - Get-AzureRmSqlDatabaseAuditingPolicy
      - Get-AzureRmSqlServerAuditingPolicy
      - Set-AzureRmSqlDatabaseAuditingPolicy
      - Set-AzureRmSqlServerAuditingPolicy
      - Use-AzureRmSqlServerAuditingPolicy
      - Remove-AzureRmSqlDatabaseAuditing
      - Remove-AzureRmSqlServerAuditing
    * Update-AzureRmSqlSyncGroup 的架构文件分析现可区分大小写。
* 存储
    * 向资源模式存储帐户 cmdlet 添加 NeworkRule 支持
      - New-AzureRmStorageAccount
      - Set-AzureRmStorageAccount
      - Get-AzureRmStorageAccountNetworkRuleSet
      - Update-AzureRmStorageAccountNetworkRuleSet
      - Add-AzureRmStorageAccountNetworkRule
      - Remove-AzureRmStorageAccountNetworkRule

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
        - 详情可参阅此问题：https://github.com/Azure/azure-powershell/issues/3043
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
        - 可在此处 https://github.com/Azure/azure-powershell/issues/4203 找到更多信息
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
        - 详情可参阅此问题：https://github.com/Azure/azure-powershell/issues/3954
* RecoveryServices.SiteRecovery
    * 为 Azure Site Recovery 操作引入新模块。
        - 所有 cmdlet 都以 AzureRmRecoveryServicesAsr* 开头
* Sql
    * 将数据同步 PowerShell Cmdlet 添加到 AzureRM.Sql
    * 更新了 AzureRmSqlServer cmdlet，使用创建服务器时可避免超时的 REST API 新版本。
    * 已弃用服务器升级 cmdlet，因为旧版服务器 (2.0) 不再存在。
    * 将新的可选开关参数“AssignIdentity”添加到 New-AzureRmSqlServer 和 Set-AzureRmSqlServer cmdlet 中，支持预配 SQL Server 资源的资源标识
    * 参数 ResourceGroupName 现对于 Get AzureRmSqlServer 来说可选
        - 详情可参阅以下问题：https://github.com/Azure/azure-powershell/issues/635
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
  - 已重命名与 RDFE cmdlet 冲突的 cmdlet。 如需更多详细信息，请参阅 https://github.com/Azure/azure-powershell/issues/2917 中的问题
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
* Azure.存储
  - 升级到 Azure 存储客户端库 8.1.1 和 Azure 存储 DataMovement 库 0.5.1
  - 添加一个新 cmdlet，用于支持 blob 增量复制功能
