---
title: Azure PowerShell 更改日志 | Microsoft Docs
description: 下面提供了对 Azure PowerShell 最新版本所做更改的历史记录。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 08/28/2018
ms.openlocfilehash: c60bc9197266cc1da37cc9af7baf03e7ba8fb7ac
ms.sourcegitcommit: 06f9206e025afa7207d4657c8f57c94ddb74817a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/07/2018
ms.locfileid: "51212583"
---
# <a name="release-notes"></a>发行说明

下面是此版本中对 Azure PowerShell 所做的更改列表。

---
## <a name="6120---november-2018"></a>6.12.0 - 2018 年 11 月
#### <a name="azurermprofile"></a>AzureRM.Profile
* 更新通用代码以使用最新版本的 ClientRuntime
* 将 Connect-AzureRmAccount cmdlet 中的 TenantId 参数重命名为 Tenant，并为 TenantId 添加别名
* 更新了 Connect-AzureRmAccount 的 TenantId 说明
* 修复了在提供租户域时失败的登录的错误消息
    - https://github.com/Azure/azure-powershell/issues/6936
* 为租户中没有订阅的帐户修复了上下文名称冲突的问题
    - https://github.com/Azure/azure-powershell/issues/7453
* 修复了在使用 MSI 时的 DataLake 终结点问题
    - https://github.com/Azure/azure-powershell/issues/7462
* 修复了在未连接时会引发“Disconnect-AzureRmAccount”的问题
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azurermautomation"></a>AzureRM.Automation
* 已将 cmdlet DLL 文件名重命名为 Microsoft.Azure.Commands.Automation.dll

#### <a name="azurermcognitiveservices"></a>AzureRM.CognitiveServices
* 添加了 Get-AzureRmCognitiveServicesAccountSkus 操作。

#### <a name="azurermcompute"></a>AzureRM.Compute
* 添加了 Add-AzureRmVmssVMDataDisk 和 Remove-AzureRmVmssVMDataDisk cmdlet
* Get-AzureRmVMImage 显示 AutomaticOSUpgradeProperties
* 修复了 SetAzureRmVMChefExtension BootstrapOptions 和 -JsonAttribute 选项值未以 json 格式设置的问题。

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* 将 DataLake 程序包更新至 1.1.10。
* 将默认并发添加到多线程操作。

#### <a name="azurerminsights"></a>AzureRM.Insights
* 修复了问题 #7267（自动缩放区域）
    - 创建新的自动缩放规则时未正确设置枚举的参数（始终将它们设置为默认值）的问题。
* 修复了问题 #7513 [见解] Set-AzureRMDiagnosticSetting 在创建设置期间需要显式指定类别
    - 现在该 cmdlet 不需要在创建期间显式指示要启用的类别，即它会按记录工作

#### <a name="azurermnetwork"></a>AzureRM.Network
* 已将 PeeringType 更改为以下 cmdlet 的必需参数：
    - Get-AzureRmExpressRouteCircuitRouteTable
    - Get-AzureRmExpressRouteCircuitARPTable
    - Get-AzureRmExpressRouteCircuitRouteTableSummary
    - Get-AzureRMExpressRouteCrossConnectionArpTable
    - Get-AzureRMExpressRouteCrossConnectionRouteTable
    - Get-AzureRMExpressRouteCrossConnectionRouteTableSummary

#### <a name="azurermpolicyinsights"></a>AzureRM.PolicyInsights
* 添加了策略修正 cmdlet

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices.Backup
* 添加了对恢复服务中 azure 文件共享的支持。

#### <a name="azurermresources"></a>AzureRM.Resources
* https://github.com/Azure/azure-powershell/issues/7402 的修复
    - 允许对“Get-AzureRmResource”使用“-ResourceId”参数来列出资源

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* 为 PSServiceBusMigrationConfigurationAttributes 添加了 MigrationState 只读属性，这将有助于了解迁移状态。

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* 修复了将证书添加到 Linux Vmss 的问题。
* 修复了“Add-AzureRmServiceFabricClusterCertificate”
    - 使用来自新证书的正确指纹 (Azure/service-fabric-issues#932)。
    - 正确显示异常 (Azure/service-fabric-issues#1054)。
* 修复了“Update-AzureRmServiceFabricDurability”以在开始 Vmss CreateOrUpdate 操作之前更新群集配置。

## <a name="6110---october-2018"></a>6.11.0 - 2018 年 10 月
#### <a name="azurermprofile"></a>AzureRM.Profile
* 修复了 CloudShell 中 Get-AzureRmSubscription 的问题
* 更新通用代码以使用最新版本的 ClientRuntime

#### <a name="azurermbackup"></a>AzureRM.Backup
* 已弃用 Azure 备份 cmdlet。

#### <a name="azurermcompute"></a>AzureRM.Compute
* 向 VM 大小的允许列表添加了新的大小，这样就可以在将简单的参数集用于“New-AzureRmVm”时为这些大小启用加速网络
* 向所有 cmdlet 添加了 ResourceName 参数补全选项。

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* 添加虚拟网络规则的支持
    - Get-AzureRmDataLakeStoreVirtualNetworkRule：获取或列出 Azure Data Lake Store 虚拟网络规则。
    - Add-AzureRmDataLakeStoreVirtualNetworkRule：向指定的 Data Lake Store 帐户添加虚拟网络规则。
    - Set-AzureRmDataLakeStoreVirtualNetworkRule：在指定的 Data Lake Store 帐户中修改指定的虚拟网络规则。
    - Remove-AzureRmDataLakeStoreVirtualNetworkRule：删除 Azure Data Lake Store 虚拟网络规则。

#### <a name="azurermnetwork"></a>AzureRM.Network
* 更新 cmdlet Test-AzureRmNetworkWatcherConnectivity，向后端传递协议值。
* 向所有 cmdlet 添加了 ResourceName 参数补全选项。

#### <a name="azurermresources"></a>AzureRM.Resources
* 通过在方案中添加一个有意义的异常，修复了 Get-AzureRMRoleDefinition 在默认配置文件中没有订阅且未指定范围的情况下引发难以理解异常的问题。 另外，已将默认参数集设置为“RoleDefinitionNameParameterSet”。

## <a name="6100---october-2018"></a>6.10.0 - 2018 年 10 月
#### <a name="azurestorage"></a>Azure.存储
* 修复了 Copy Blob/File 在目标有元数据问题时不会复制元数据的问题
    - Start-AzureStorageBlobCopy
    - Start-AzureStorageFileCopy

#### <a name="azurermcognitiveservices"></a>AzureRM.CognitiveServices
* 在没有现有帐户的情况下支持 Get-AzureRmCognitiveServicesAccountSkus。

#### <a name="azurermcompute"></a>AzureRM.Compute
* 修复了 Get-AzureRmVM -ResourceGroupName <rg>，以在需要时返回超过 50 个结果
* 在 New-AzureRmVmss cmdlet 帮助中添加了“SimpleParameterSet”的示例。
* 修复了 Azure 磁盘加密进度消息中的拼写错误

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* 将 ADF .Net SDK 版本更新为 2.3.0。

#### <a name="azurermnetwork"></a>AzureRM.Network
* 添加了 NetworkProfile 功能。 添加了新 cmdlet
    - Get-AzureRMNetworkProfile
    - New-AzureRMNetworkProfile
    - Remove-AzureRMNetworkProfile
    - Set-AzureRMNetworkProfile
    - New-AzureRMContainerNicConfig
    - New-AzureRmContainerNicConfigIpConfig
* 在子网模型上添加了服务关联链接
* 添加了 cmdlet New-AzureRmVirtualNetworkTap、Get-AzureRmVirtualNetworkTap、Set-AzureRmVirtualNetworkTap、Remove-AzureRmVirtualNetworkTap
* 添加了 cmdlet Set-AzureRmNEtworkInterfaceTapConfig、Get-AzureRmNEtworkInterfaceTapConfig、Remove-AzureRmNEtworkInterfaceTapConfig

#### <a name="azurermrediscache"></a>AzureRM.RedisCache
* 今后允许任何字符串作为 Size 参数。 在 PSArgumentCompleter 弹出窗口中添加了 P5

#### <a name="azurermresources"></a>AzureRM.Resources
* 将缺少的 -Mode 参数添加到 Set-AzureRmPolicyDefinition
* 对于使用包含用户的源的操作，修复了 Get-AzureRmProviderOperation commandlet bug

#### <a name="azurermsql"></a>AzureRM.Sql
* 修复了某些备份 cmdlet 无法识别当前 azure 订阅的问题

#### <a name="azurermstorage"></a>AzureRM.Storage
* 支持获取特定位置的存储资源使用情况，并对于获取的全局存储资源使用情况已过时添加警告消息。
    - Get-AzureRmStorageUsage

#### <a name="azurermwebsites"></a>AzureRM.Websites
* 新 Cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl - 获取容器持续部署 Webhook URL
* 新 Cmdlet New-AzureRMWebAppContainerPSSession 和 Enter-WebAppContainerPSSession - 在 Windows 容器应用中启动 PowerShell 远程会话

## <a name="690---september-2018"></a>6.9.0 - 2018 年 9 月
#### <a name="general"></a>常规
* AzureRM.SignalR 已添加到 AzureRM 汇总模块

#### <a name="azurermprofile"></a>AzureRM.Profile
* 对存储常用代码进行了细微的更改
* 更新了帮助文件，使之包括完整参数类型。
- 已在 ServicePrincipalCertificateWithSubscriptionId 参数集中将 -ServicePrincipal 更改为非强制性项 

#### <a name="azurestorage"></a>Azure.存储
* 支持使用 OAuth 创建存储上下文。 
    - New-AzureStorageContext

#### <a name="azurermcdn"></a>AzureRM.Cdn
* 在 Cdn 定价 sku 中增加了 Standard_Microsoft。 

#### <a name="azurermcompute"></a>AzureRM.Compute
* 将 Keyvault 和存储的依赖项移到了常用依赖项中
* 增加了对 AEM cmdlet 的支持，可以使用更多的虚拟机大小
* 为 New-AzureRmVmssIpConfig 增加了 PublicIPPrefix 参数
* 为 Invoke-AzureRmVMRunCommand cmdelt 增加了 ResourceId 参数
* 增加了 Invoke-AzureRmVmssVMRunCommand cmdlet

#### <a name="azurermdns"></a>AzureRM.Dns
* 增加了在创建 dns 记录期间对别名记录的支持

#### <a name="azurerminsights"></a>AzureRM.Insights
* 修复了问题 #6833 和 #7102（诊断设置方面）
    - 在创建和列出/获取诊断设置期间出现的默认名称（即“service”）的问题
    - 通过类别创建诊断设置的问题
* 为指标时间粒度参数添加了弃用消息
    - Timegrains 参数仍然会被接受（这是非重大变更），但在后端会被忽略，因为仅 PT1M 有效

#### <a name="azurermnetwork"></a>AzureRM.Network
* 更改了 LoadBalancer cmdlet
  - LoadBalancerInboundNatPoolConfig：增加了 IdleTimeoutInMinutes、EnableFloatingIp 和 EnableTcpReset 参数
  - LoadBalancerInboundNatRuleConfig：增加了 EnableTcpReset 参数
  - LoadBalancerRuleConfig：增加了 EnableTcpReset 参数
  - LoadBalancerProbeConfig：增加了对参数 Protocol 的“Https”值的支持
* 为新 LoadBalancer 的子资源 OutboundRule 增加了新命令
  - Add-AzureRmLoadBalancerOutboundRuleConfig
  - Get-AzureRmLoadBalancerOutboundRuleConfig
  - New-AzureRmLoadBalancerOutboundRuleConfig
  - Set-AzureRmLoadBalancerOutboundRuleConfig
  - Remove-AzureRmLoadBalancerOutboundRuleConfig
* 为 PSNetworkInterface 增加了新的 HostedWorkloads 属性
* 通过 ARM 为 Azure 防火墙功能增加了新的 cmdlet
  - 增加了 Get-AzureRmFirewall
  - 增加了 Set-AzureRmFirewall
  - 增加了 New-AzureRmFirewall
  - 增加了 Remove-AzureRmFirewall
  - 增加了 New-AzureRmFirewallApplicationRuleCollection
  - 增加了 New-AzureRmFirewallApplicationRule
  - 增加了 New-AzureRmFirewallNatRuleCollection
  - 增加了 New-AzureRmFirewallNatRule
  - 增加了 New-AzureRmFirewallNetworkRuleCollection
  - 增加了 New-AzureRmFirewallNetworkRule
* 在应用程序网关中增加了对受信任根证书和自动缩放配置的支持
  - 增加了新的 Cmdlet：
      - Add-AzureRmApplicationGatewayTrustedRootCertificate
      - Get-AzureRmApplicationGatewayTrustedRootCertificate
      - New-AzureRmApplicationGatewayTrustedRootCertificate
      - Remove-AzureRmApplicationGatewayTrustedRootCertificate
      - Set-AzureRmApplicationGatewayTrustedRootCertificate
      - Get-AzureRmApplicationGatewayAutoscaleConfiguration
      - New-AzureRmApplicationGatewayAutoscaleConfiguration
      - Remove-AzureRmApplicationGatewayAutoscaleConfiguration
      - Set-AzureRmApplicationGatewayAutoscaleConfiguration
  - 使用可选参数 -TrustedRootCertificate 更新了 Cmdlet
      - New-AzureRmApplicationGateway
      - Set-AzureRmApplicationGateway
      - New-AzureRmApplicationGatewayBackendHttpSetting
      - Set-AzureRmApplicationGatewayBackendHttpSetting
  - 使用可选参数 -AutoscaleConfiguration 更新了 Cmdlet
      - New-AzureRmApplicationGateway
      - Set-AzureRmApplicationGateway
* 为接口终结点增加了 cmdlet Get-AzureInterfaceEndpoint
* 在子网中增加了对多个地址前缀的支持。 更新了 cmdlet：
  - New-AzureRmVirtualNetworkSubnetConfig
  - Set-AzureRmVirtualNetworkSubnetConfig
  - Add-AzureRmVirtualNetworkSubnetConfig
  - Get-AzureRmVirtualNetworkSubnetConfig
  - Add-AzureRmApplicationGatewayAuthenticationCertificate
  - Add-AzureRmApplicationGatewayFrontendIPConfig
  - New-AzureRmApplicationGatewayFrontendIPConfig
  - Set-AzureRmApplicationGatewayFrontendIPConfig
  - Add-AzureRmApplicationGatewayIPConfiguration
  - New-AzureRmApplicationGatewayIPConfiguration
  - Set-AzureRmApplicationGatewayIPConfiguration
  - Add-AzureRmNetworkInterfaceIpConfig
  - New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig
  - New-AzureRmVirtualNetworkGatewayIpConfig
  - Add-AzureRmVirtualNetworkGatewayIpConfig
  - Set-AzureRmLoadBalancerFrontendIpConfig
  - Add-AzureRmLoadBalancerFrontendIpConfig
  - New-AzureRmLoadBalancerFrontendIpConfig
  - New-AzureRmNetworkInterface
* 增加了用于子网委派的 cmdlet。
  - New-AzureRmDelegation：创建一个可以添加到子网的新委派
  - Remove-AzureRmDelegation：获取一个子网，然后从该子网中删除提供的委派名称
  - Add-AzureRmDelegation：获取一个子网，然后向该子网添加提供的服务名称作为委派
  - Get-AzureRmDelegation
  - Get-AzureRmAvailableServiceDelegations

#### <a name="azurermrecoveryservicessiterecovery"></a>AzureRM.RecoveryServices.SiteRecovery
* 支持托管磁盘

#### <a name="azurermrediscache"></a>AzureRM.RedisCache
* 更新了 Insights 依赖项。

#### <a name="azurermresources"></a>AzureRM.Resources
* 使用新参数 RollbackAction 更新了 New-AzureRmResourceGroupDeployment
    - 使用新参数增加了对 OnErrorDeployment 的支持。
* 在策略分配方面支持托管标识。
* 使用“New-AzureRmPolicyAssignment”来分配策略时，不再需要带默认值的参数
* 增加了新的 cmdlet Get-AzureRmPolicyAlias，用于检索策略别名

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* 修复了问题 #7161

#### <a name="azurermsignalr"></a>AzureRM.SignalR
* 将 SKU 名称更新为 Free_F1 和 Standard_S1
* 为 PSSignalRResource 对象增加了版本字段，为 PSSignalRKeys 对象增加了字符串。

#### <a name="azurermstorage"></a>AzureRM.Storage
* 在 AzureRm.Storage 中支持不可变性策略 
    - Remove-AzureRmStorageAccountNetworkRule
    - Get-AzureRmStorageContainer
    - Update-AzureRmStorageContainer
    - New-AzureRmStorageContainer
    - Remove-AzureRmStorageContainer
    - Add-AzureRmStorageContainerLegalHold
    - Remove-AzureRmStorageContainerLegalHold
    - Set-AzureRmStorageContainerImmutabilityPolicy
    - Get-AzureRmStorageContainerImmutabilityPolicy
    - Remove-AzureRmStorageContainerImmutabilityPolicy
    - Lock-AzureRmStorageContainerImmutabilityPolicy

#### <a name="azurermwebsites"></a>AzureRM.Websites
* 增加了两个新的 cmdlet：Get-AzureRmDeletedWebApp 和 Restore-AzureRmDeletedWebApp
* 增加了 New-AzureRmAppServicePlan -HyperV 开关，用于通过 Windows 容器创建应用服务计划
* New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - 增加了新参数 (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment)，用于创建和管理 Windows 容器应用

## <a name="681---august-2018"></a>6.8.1 - 2018 年 8 月
#### <a name="general"></a>常规
* 解决了未设置默认资源组的问题。
* 更新了公共运行时程序集

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* 解决了未设置默认资源组的问题。
* 修复了问题 https://github.com/Azure/azure-powershell/issues/6603
    - Import-AzureRmApiManagementApi 和 *-AzureRmApiManagementCertificate cmdlet 现在处理相对路径
* 修复了问题 https://github.com/Azure/azure-powershell/issues/6879
    - CertificateInformation 是使 Set-AzureRmApiManagement cmdlet 可以正常工作的可设置属性。 通过升级到 4.0.4-preview nuget 进行了修复
* 修复了问题 https://github.com/Azure/azure-powershell/issues/6853
    - 针对按产品名称进行的搜索修复了 Odata 筛选器
* 修复了问题 https://github.com/Azure/azure-powershell/issues/6814
    - 针对按 API 名称进行的搜索修复了 Odata 筛选器
* 添加了对 AzureMonitor 记录器的支持


#### <a name="azurermcompute"></a>AzureRM.Compute
* 解决了错误输出中缺少目标的问题。
* 解决了带有托管磁盘的 VM 的存储帐户类型问题
* 解决了未设置默认资源组的问题。
* 解决了在其他环境（例如 Azure 中国）中使用 AEM 扩展 cmdlet 的问题

#### <a name="azurermnetwork"></a>AzureRM.Network
* 将默认 cmdlet 输出表示形式更改为表视图

#### <a name="azurermpowerbiembedded"></a>AzureRM.PowerBIEmbedded
* 修复了在尝试扩展停用的容量时 Update-AzureRmPowerBIEmbeddedCapacity 中出现的故障


#### <a name="azurermresources"></a>AzureRM.Resources
* 解决了从市场创建托管应用程序的问题。

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* 修复的问题
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* 添加了对 MultiValue 路由方法的支持
    - MultiValue 路由的新参数“MaxReturn”
* 添加了对 Subnet 路由方法的支持
    - 对终结点中的 IP 地址范围（子网）的支持
* 添加了对配置文件中的自定义标头的支持
* 添加了对配置文件中的预期状态代码范围的支持
* 添加了对终结点中的自定义标头的支持

## <a name="680---august-2018"></a>6.8.0 - 2018 年 8 月
#### <a name="general"></a>常规
* 解决了未设置默认资源组的问题。

#### <a name="azurermprofile"></a>AzureRM.Profile
* 为在执行 Connect-AzureRmAccount 期间返回的令牌添加了“过期”属性

#### <a name="azurermcompute"></a>AzureRM.Compute
* 解决了错误输出中缺少目标的问题。
* 解决了带有托管磁盘的 VM 的存储帐户类型问题
* 解决了在其他环境（例如 Azure 中国）中使用 AEM 扩展 cmdlet 的问题

#### <a name="azurermiothub"></a>AzureRM.IotHub
* 修复了 New-AzureRmIotHubExportDevices 和 New-AzureRmIotHubImportDevices的示例

#### <a name="azurermnetwork"></a>AzureRM.Network
* 将默认模型表示形式更改为表视图

#### <a name="azurermpowerbiembedded"></a>AzureRM.PowerBIEmbedded
* 修复了在尝试扩展停用的容量时 Update-AzureRmPowerBIEmbeddedCapacity 中出现的故障

#### <a name="azurermresources"></a>AzureRM.Resources
* 解决了从市场创建托管应用程序的问题。

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* 解决了以下问题
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* 对 MultiValue 路由方法的支持
    - MultiValue 路由的新参数“MaxReturn”
* 对 Subnet 路由方法的支持
    - 对终结点中的 IP 地址范围（子网）的支持
* 对配置文件中的自定义标头的支持
* 对配置文件中的预期状态代码范围的支持
* 对终结点中的自定义标头的支持

#### <a name="azurermwebsites"></a>AzureRM.Websites
* 解决了错误地设置默认资源组的问题。

## <a name="670---august-2018"></a>6.7.0 - 2018 年 8 月
#### <a name="azurermprofile"></a>AzureRM.Profile
* 已更新到最新版本的 Azure ClientRuntime。
* 向默认的上下文名称添加用户 ID，避免上下文冲突
    - https://github.com/Azure/azure-powershell/issues/6489
* 修复了 Clear-AzureRmContext 在选择上下文 #6398 时出现的问题
* 允许将租户域传递给“Connect-AzureRmAccount”的“-TenantId”参数
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a>Azure.存储
* 去除了 Azure 文件共享配额的 5TB 限制
- Set-AzureStorageShareQuota

#### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* 已更新到最新版本的 Azure ClientRuntime。

#### <a name="azureanalysisservices"></a>Azure.AnalysisServices
* 已更新到最新版本的 Azure ClientRuntime。

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* 已更新到最新版本的 Azure ClientRuntime。

#### <a name="azurermapplicationinsights"></a>AzureRM.ApplicationInsights
* 已更新到最新版本的 Azure ClientRuntime。

#### <a name="azurermautomation"></a>AzureRM.Automation
* 已更新到最新版本的 Azure ClientRuntime。

#### <a name="azurermbackup"></a>AzureRM.Backup
* 已更新到最新版本的 Azure ClientRuntime。

#### <a name="azurermbatch"></a>AzureRM.Batch
* 已更新到最新版本的 Azure ClientRuntime。

#### <a name="azurermbilling"></a>AzureRM.Billing
* 已更新到最新版本的 Azure ClientRuntime。

#### <a name="azurermcdn"></a>AzureRM.Cdn
* 已更新到最新版本的 Azure ClientRuntime。

#### <a name="azurermcognitiveservices"></a>AzureRM.CognitiveServices
* 已更新到最新版本的 Azure ClientRuntime。

#### <a name="azurermcompute"></a>AzureRM.Compute
* 已更新到最新版本的 Azure ClientRuntime。
* 为 New-AzureRmVmssConfig 增加了 EvictionPolicy 参数
* 在 New-AzureRmVm 的 DiskFileParameterSet 中使用默认位置（如果未指定 Location）
* 修复了 Save-AzureRmVMImage 中的参数说明
* 修复了某些单次传递相关方案的 Get-AzureRmVMDiskEncryptionStatus cmdlet

#### <a name="azurermconsumption"></a>AzureRM.Consumption
* 已更新到最新版本的 Azure ClientRuntime。

#### <a name="azurermcontainerinstance"></a>AzureRM.ContainerInstance
* 已更新到最新版本的 Azure ClientRuntime。

#### <a name="azurermcontainerregistry"></a>AzureRM.ContainerRegistry
* 已更新到最新版本的 Azure ClientRuntime。

#### <a name="azurermdatafactories"></a>AzureRM.DataFactories
* 已更新到最新版本的 Azure ClientRuntime。

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* 已更新到最新版本的 Azure ClientRuntime。

#### <a name="azurermdatalakeanalytics"></a>AzureRM.DataLakeAnalytics
* 已更新到最新版本的 Azure ClientRuntime。

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* 修复了从 PowerShell 命令行设置 DebugPreference 时的调试问题
* 更新了 Set-AzureRmDataLakeStoreItemAcl 的示例
* 已更新到最新版本的 Azure ClientRuntime。
* 更新了 Set-AzureRmDataLakeStoreItemAclEntry 的示例

#### <a name="azurermdevtestlabs"></a>AzureRM.DevTestLabs
* 已更新到最新版本的 Azure ClientRuntime。

#### <a name="azurermdns"></a>AzureRM.Dns
* 已更新到最新版本的 Azure ClientRuntime。

#### <a name="azurermeventgrid"></a>AzureRM.EventGrid
* 已更新到最新版本的 Azure ClientRuntime。

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* 已更新到最新版本的 Azure ClientRuntime。

#### <a name="azurermhdinsight"></a>AzureRM.HDInsight
* 已更新到最新版本的 Azure ClientRuntime。

#### <a name="azurerminsights"></a>AzureRM.Insights
* 已更新到最新版本的 Azure ClientRuntime。

#### <a name="azurermiothub"></a>AzureRM.IotHub
* 已更新到最新版本的 Azure ClientRuntime。

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* 已更新到最新版本的 Azure ClientRuntime。

#### <a name="azurermlogicapp"></a>AzureRM.LogicApp
* 已更新到最新版本的 Azure ClientRuntime。

#### <a name="azurermmachinelearning"></a>AzureRM.MachineLearning
* 已更新到最新版本的 Azure ClientRuntime。

#### <a name="azurermmachinelearningcompute"></a>AzureRM.MachineLearningCompute
* 已更新到最新版本的 Azure ClientRuntime。

#### <a name="azurermmarketplaceordering"></a>AzureRM.MarketplaceOrdering
* 已更新到最新版本的 Azure ClientRuntime。

#### <a name="azurermmedia"></a>AzureRM.Media
* 已更新到最新版本的 Azure ClientRuntime。

#### <a name="azurermnetwork"></a>AzureRM.Network
* 增加了 Set-AzureRmLocalNetworkGateway 的示例
* 增加了 Add-AzureRmVirtualNetworkGatewayIpConfig、Get-AzureRmVirtualNetworkGatewayConnectionSharedKey 和 New-AzureRmVirtualNetworkGatewayConnection 的示例和说明
* 增加了 Remove-AzureRmVirtualNetworkGatewayIpConfig 和 Reset-AzureRmVirtualNetworkGateway 的示例
* 增加了 Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey 的示例
* 增加了 Set-AzureRmVirtualNetworkGatewayConnectionSharedKey 的示例
* 增加了 Set-AzureRmVirtualNetworkGatewayConnection 的示例
* 使用最新的代码生成器重新生成了 ApplicationSecurityGroup、RouteTable 和 Usage 的 cmdlet
* 阐明了在尝试获取的子网不存在时 Get-AzureRmVirtualNetworkSubnetConfig 的错误消息

#### <a name="azurermnotificationhubs"></a>AzureRM.NotificationHubs
* 已更新到最新版本的 Azure ClientRuntime。

#### <a name="azurermoperationalinsights"></a>AzureRM.OperationalInsights
* 已更新到最新版本的 Azure ClientRuntime。

#### <a name="azurermpolicyinsights"></a>AzureRM.PolicyInsights
* 已更新到最新版本的 Azure ClientRuntime。

#### <a name="azurermpowerbiembedded"></a>AzureRM.PowerBIEmbedded
* 已更新到最新版本的 Azure ClientRuntime。

#### <a name="azurermrecoveryservices"></a>AzureRM.RecoveryServices
* 已更新到最新版本的 Azure ClientRuntime。

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices.Backup
* 为 Get-AzureRmRecoveryServicesBackItem cmdlet 增加了策略筛选器。 此命令返回受给定策略 ID 保护的备份项的列表。
* 已将 Microsoft.Azure.Management.RecoveryServices.Backup 更新到 3.0.0-preview 版本。
* 已更新到最新版本的 Azure ClientRuntime。
* 为 Restore-AzureRmRecoveryServicesBackupItem 增加了 TargetResourceGroupName 参数。 托管磁盘还原到的资源组。 适用于包含托管磁盘的 VM 的备份。

#### <a name="azurermrecoveryservicessiterecovery"></a>AzureRM.RecoveryServices.SiteRecovery
* 已更新到最新版本的 Azure ClientRuntime。

#### <a name="azurermrediscache"></a>AzureRM.RedisCache
* 已更新到最新版本的 Azure ClientRuntime。

#### <a name="azurermrelay"></a>AzureRM.Relay
* 已更新到最新版本的 Azure ClientRuntime。

#### <a name="azurermresources"></a>AzureRM.Resources
* 支持在订阅范围部署模板。 增加了新 cmdlet：
    - New-AzureRmDeployment
    - Get-AzureRmDeployment
    - Test-AzureRmDeployment
    - Remove-AzureRmDeployment
    - Stop-AzureRmDeployment
    - Save-AzureRmDeploymentTemplate
    - Get-AzureRmDeploymentOperation
* 修复了在将上下文传递给 Set-AzureRmResource 时引发错误的问题
    - https://github.com/Azure/azure-powershell/issues/5705
* 修复了 New-AzureRmResourceGroupDeployment 中的示例
* 已更新到最新版本的 Azure ClientRuntime。

#### <a name="azurermscheduler"></a>AzureRM.Scheduler
* 已更新到最新版本的 Azure ClientRuntime。

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* 已更新到最新版本的 Azure ClientRuntime。

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* 已更新到最新版本的 Azure ClientRuntime。

#### <a name="azurermsql"></a>AzureRM.Sql
* 已更新到最新版本的 Azure ClientRuntime。

#### <a name="azurermstorage"></a>AzureRM.Storage
* 已更新到最新版本的 Azure ClientRuntime。

#### <a name="azurermstreamanalytics"></a>AzureRM.StreamAnalytics
* 已更新到最新版本的 Azure ClientRuntime。

#### <a name="azurermtags"></a>AzureRM.Tags
* 已更新到最新版本的 Azure ClientRuntime。

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* 已更新到最新版本的 Azure ClientRuntime。

#### <a name="azurermusageaggregates"></a>AzureRM.UsageAggregates
* 已更新到最新版本的 Azure ClientRuntime。

#### <a name="azurermwebsites"></a>AzureRM.Websites
* 已更新到最新版本的 Azure ClientRuntime。

## <a name="660---july-2018"></a>6.6.0 - 2018 年 7 月
#### <a name="general"></a>常规
* 更新了所有帮助文件，以包括完整参数类型和正确的输入/输出类型。

#### <a name="azurermprofile"></a>AzureRM.Profile
* 更新了 Common.Strategy 库，以便能够验证资源的当前配置是否与目标资源兼容。
* 在 Common.Storage 中添加了 ps1xml 类型

#### <a name="azurestorage"></a>Azure.存储
* 增加了从 DefaultProfile 获取存储上下文的支持
* 为 cmdlet 输出类型属性增加了 Ps1XmlAttribute。

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* 修复了问题 https://github.com/Azure/azure-powershell/issues/6370
    - 修复了 Automapper 中将 PsApiManagementApi 转换为 ApiContract 的 bug
* 修复了问题 https://github.com/Azure/azure-powershell/issues/6515
    - 修复了 File.Save 中没有使用编码类型重载的 bug
* 修复了问题 https://github.com/Azure/azure-powershell/issues/6560
    - 升级到了 4.0.3 Nuget版本，该版本修复了 apiId 上的模式异常

#### <a name="azurermcompute"></a>AzureRM.Compute
* 修复因使用 PremiumLRS 存储帐户类型重命名而在 New-AzureRmVm 中使用 DiskFileParameterSet 创建 VM 失败的问题。
* 修复 Invoke-AzureRmVMRunCommand cmdlet
* 更新 Get-AzureRmAvailabilitySet 以启用列出订阅中的所有可用性集。  （ResouceGroupName 参数现在是可选的。）
* 更新“New-AzureRmVm”的 SimpleParameterSet 以在符合条件的 VM 上启用加速网络。
* 将 New-AzureRmVmss 简单参数集更新为在用户指定的 LB 已存在时创建 vmss 失败。
* 更新 New-AzureRmDisk 的示例
* 添加“New-AzureRmVM”的示例
* 更新 Set-AzureRmVMOSDisk 的说明
* 更新 Set-AzureRmVMBginfoExtension 的示例 1 以更正拼写和前缀。 

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* 将 ADF .Net SDK 版本更新为 1.1.0。
* 支持跨数据工厂的自承载集成运行时共享。
     - 将新参数 -SharedIntegrationRuntimeResourceId 添加到 Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet。
     - 将新的可选参数 -LinkedDataFactoryName 添加到 Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet。

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* 将数据平面 SDK (Microsoft.Azure.DataLake.Store) 版本更新为 1.1.9

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* 在删除 cmdlet 中更新了 InputObject 和 ResourceId 的管道

#### <a name="azurerminsights"></a>AzureRM.Insights
* 修复了帮助文件中 OutputType 的格式问题
* 使用 Microsoft.Azure.Management.Monitor SDK 0.19.1-preview

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* 修复了 Set-AzureRmKeyVaultAccessPolicy 中的管道问题

#### <a name="azurermnetwork"></a>AzureRM.Network
* 添加了 LoadBalancerInboundNatPoolConfig cmdlet 的示例。

#### <a name="azurermresources"></a>AzureRM.Resources
* 修复了为“Get-AzureRmResource”同时提供标记名称和值时出现的问题
    - https://github.com/Azure/azure-powershell/issues/6765
* 使用“Set-AzureRmResource”修复管道方案

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* 在删除 cmdlet 中更新了 InputObject 和 ResourceId 的管道
* 修复了几个问题
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a>AzureRM.Sql
* 使用以下 cmdlet 添加服务器高级威胁防护支持：
    - Enable-AzureRmSqlServerAdvancedThreatProtection；Disable-AzureRmSqlServerAdvancedThreatProtection；Get-AzureRmSqlServerAdvancedThreatProtectionPolicy
* 使用以下 cmdlet 添加漏洞评估支持：
    - Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings；Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings；Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings
    - Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline；Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline；Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline
    - Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan；Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord；Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan
* 修复了 Remove-AzureRmSqlServerFirewallRule 中的示例
* 修复了 Get-AzureSqlSyncGroupLog 中非美国基础文化的日期时间处理错误

#### <a name="azurermstorage"></a>AzureRM.Storage
* 将 Ps1XmlAttribute 添加到 cmdlet 输出类型属性
* 在表视图中显示 StorageAccount cmdlet 输出
    - Get-AzureRmStorageAccount
    - New-AzureRmStorageAccount
    - Set-AzureRmStorageAccount

#### <a name="azurermtags"></a>AzureRM.Tags
* 从 Tag cmdlet 帮助中删除不正确的语句
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a>6.5.0 - 2018 年 7 月
#### <a name="azurermprofile"></a>AzureRM.Profile
* 更新了“Get-AzureRmContextAutosaveSetting”的帮助

#### <a name="azurestorage"></a>Azure.存储
* 支持使用只写 Sas 令牌上传 Blob 或文件
- Set-AzureStorageBlobContent
- Set-AzureStorageFileContent

#### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* 将所需属性 ResourceGroupName 添加到 AS。

#### <a name="azurermautomation"></a>AzureRM.Automation
* 更新帮助并添加“New-AzureRMAutomationSchedule”的示例

#### <a name="azurermcompute"></a>AzureRM.Compute
* 将 -Tag 参数添加到 Update/New-AzureRmAvailabilitySet
* 添加“Add-AzureRmVmssExtension”的示例
* 添加“Remove-AzureRmVmssExtension”的示例
* 更新“Set-AzureRmVMAccessExtension”的帮助
* 更新 New-AzureRmVmss 的 SimpleParameterSet，以默认情况下将 SinglePlacementGroup 设置为false，并添加开关参数“SinglePlacementGroup”，使用户能够在单个放置组中创建 VMSS。

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* 向 PSEventHubDRConfigurationAttributes 类添加了一个只读属性“PendingReplicationOperationsCount”，该属性在复制过程中为挂起的复制操作计数

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* 更新了 Set-AzureRmKeyVaultAccessPolicy 的错误消息

#### <a name="azurermlogicapp"></a>AzureRM.LogicApp
* 修复了 New-AzureRmLogicApp 中的“无法解析参数集”错误

#### <a name="azurermnetwork"></a>AzureRM.Network
* 在多个租户中为 Set/Add-AzureRmVirtualNetworkPeering 启用跨虚拟网络对等互连
* 针对应用程序网关更新了以下 cmdlet
    - New-AzureRmApplicationGateway：添加了 EnableFIPS 标志和区域支持
    - New-AzureRmApplicationGatewaySku：添加了新的 sku Standard_v2 和 WAF_v2
    - Set-AzureRmApplicationGatewaySku：添加了新的 sku Standard_v2 和 WAF_v2
* 使用最新的生成器版本重新生成了 RouteTable cmdlet

#### <a name="azurermrelay"></a>AzureRM.Relay
* 更新了 Markdown 文件，其中修复了示例中的参数名称问题

#### <a name="azurermresources"></a>AzureRM.Resources
* 更新了 Roleassignment 和 roledefinition cmdlet：
    - 删除了作为分页的一部分完成的额外 roledefinition 调用。
* 修复了 Get-AzureRmRoleAssignment cmdlet
    - 修复了 -ExpandPrincipalGroups 命令参数功能
* 修复了“Get-AzureRmResource”的问题，其中“-ResourceType”参数区分大小写

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* 向列表 cmdlet 添加了 top 和 skip 参数
* 添加了标准到高级命名空间迁移 cmdlet：
    - Start-AzureRmServiceBusMigration
    - Get-AzureRmServiceBusMigration
    - Complete-AzureRmServiceBusMigration
    - Stop-AzureRmServiceBusMigration
    - Remove-AzureRmServiceBusMigration
* 向 PSServiceBusDRConfigurationAttributes 类添加了一个只读属性“PendingReplicationOperationsCount”，该属性在复制过程中为挂起的复制操作计数

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* 更新了“New-AzureRmServiceFabricCluster”的示例

#### <a name="azurermsql"></a>AzureRM.Sql
* 为 Management.Sql 添加新的 Cmdlet，以允许客户将 TDE 证书添加到 Sql Server 实例或托管实例
    - Add-AzureRmSqlServerTransparentDataEncryptionCertificate
    - Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate

#### <a name="azurermwebsites"></a>AzureRM.Websites
* 设置为 false 时，`Set-AzureRmWebApp -AssignIdentity` 和 `Set-AzureRmWebAppSlot -AssignIdentity` 现在将从站点对象中删除 Identity 属性。同时移除预览标记。
* `Get-AzureRmWebAppMetrics`、`Get-AzureRmAppServicePlanMetrics` 示例已更新
* `Set-AzureRmWebApp -PhpVersion` 支持 off 作为有效的 php 版本

## <a name="640---july-2018"></a>6.4.0 - 2018 年 7 月
#### <a name="general"></a>常规
* 修复了大多数模块的帮助文件中的 OutputType 格式问题

#### <a name="azurermprofile"></a>AzureRM.Profile
* 已将 Ps1Xml 属性添加到基本输出类型

#### <a name="azurermcompute"></a>AzureRM.Compute
* VMSS 的 IP 标记功能
    - 已添加“New-AzureRmVmssIpTagConfig”cmdlet
    - 已将 IpTag 参数添加到 New-AzureRmVmssIpConfig
* VMSS 的自动 OS 回滚功能
    - 已将 DisableAutoRollback 参数添加到 New-AzureRmVmssConfig 和 Update-AzureRmVmss
* VMSS 的 OS 升级历史记录功能
    - 已将 OSUpgradeHistory 开关参数添加到 Get-AzureRmVmss

#### <a name="azurermdatalakeanalytics"></a>AzureRM.DataLakeAnalytics
* 通过以下命令添加目录 ACL 的支持：
    - Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry
    - Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry
    - Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* 为 Set-AzureRmDataLakeStoreItemAclEntry、Remove-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAcl 添加了取消支持和进度跟踪
* 为 Export-AzureRmDataLakeStoreChildItemProperties 添加了取消支持
* 修复了执行递归操作的 cmdlet 的调试消息刷新
* 修复了 DataLake cmdlet 的测试位置

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* 已将可选的 MaxCount 参数添加到“列出操作”cmdlet Get-AzureRmEventHub 和 Get-AzureRmEventHubConsumerGroup
* 修复了 New-AzureRmEventHub cmdlet 的问题：创建新事件中心时至少需要一个参数。 提供了默认参数集。
* 已将可选参数 -KeyValue 添加到 New-AzureRmEventHubKey cmdlet，该参数可让用户提供 KeyValue。

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* 修复了 Get-AzureRmKeyVault -Tag 返回所有资源的问题

#### <a name="azurermnetwork"></a>AzureRM.Network
* 为区域冗余的 VirtualNetworkGateways 公开新 SKU
* 通过 ARM 为以下功能添加了新命令：ExpressRoute 合作伙伴 API
    - 添加了 Get-AzureRmExpressRouteCrossConnection
    - 添加了 Set-AzureRmExpressRouteCrossConnection
    - 添加了 Add-AzureRmExpressRouteCrossConnectionPeering
    - 添加了 Get-AzureRmExpressRouteCrossConnectionPeering
    - 添加了 Remove-AzureRmExpressRouteCrossConnectionPeering
    - 添加了 Get-AzureRMExpressRouteCrossConnectionArpTable
    - 添加了 Get-AzureRMExpressRouteCrossConnectionRouteTable
    - 添加了 Get-AzureRMExpressRouteCrossConnectionRouteTableSummary

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices.Backup
* 添加了 Get-AzureRmRecoveryServicesBackupStatus cmdlet。 此 cmdlet 采用 VM ID，并检查 VM 是否受订阅中的某个保管库保护。 如果存在此类保管库，该 cmdlet 会输出该保管库的详细信息。

#### <a name="azurermresources"></a>AzureRM.Resources
* 更新了 Get-AzureRmPolicyAssignment cmdlet：
    - 添加了在管理组级别列出 -Scope 值的支持
    - 添加了在管理组级别使用 -Scope 值检索单个分配的支持
    - 已将 -Effective 和 -All 开关添加到 control 参数
* 更新了 Get/New/Remove/Set-AzureRmPolicyDefinition cmdlet
    - 添加了 -ManagementGroupName 参数，以将操作应用到给定的管理组
    - 添加了 -SubscriptionId 参数，以将操作应用到给定的订阅
* 更新了 Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlet
    - 添加了 -ManagementGroupName 参数，以将操作应用到给定的管理组
    - 添加了 -SubscriptionId 参数，以将操作应用到给定的订阅
* 添加了使用 TemplateParameterObject 时在参数中指定 KeyVault 机密引用的支持
* 修复了忽略“New-AzureRmADAppCredential”的“-EndDate”参数的问题
    - https://github.com/Azure/azure-powershell/issues/6505
* 修复了“Add-AzureRmADGroupMember”使用错误的 URL 发出请求的问题
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* 已将可选参数 -KeyValue 添加到 New-AzureRmServiceBusKey cmdlet，该参数可让用户提供 KeyValue。

#### <a name="azurermsql"></a>AzureRM.Sql
* 在 AzureRmSqlDatabaseRestorePoint 帮助中澄清了 SQLDW 的用户定义还原点
* 更新了多个 cmdlet 中 -ComputeGeneration 参数的文档

## <a name="630---june-2018"></a>6.3.0 - 2018 年 6 月
#### <a name="azurermprofile"></a>AzureRM.Profile
* 更新了 Enable-AzureRmContextAutoSave 的错误消息
* 在运行没有旧上下文的“Connect-AzureRmAccount”时为每个订阅创建一个上下文

#### <a name="azurestorage"></a>Azure.存储
* 在帮助文件中增加了关于 -Permissions 参数的其他信息。

#### <a name="azurermcompute"></a>AzureRM.Compute
* “Get-AzureRmVmDiskEncryptionStatus”修复了一个针对没有数据磁盘的 VM 观察到的问题 
* 更新计算客户端库版本以修复以下 cmdlet
    - Grant-AzureRmDiskAccess
    - Grant-AzureRmSnapshotAccess
    - Save-AzureRmVMImage
* 修复了以下 cmdlet，因此可以正确地显示“操作 ID”和“操作状态”：
    - Start-AzureRmVM
    - Stop-AzureRmVM
    - Restart-AzureRmVM
    - Set-AzureRmVM
    - Remove-AzuerRmVM
    - Set-AzureRmVmss
    - Start-AzureRmVmssRollingOSUpgrade
    - Stop-AzureRmVmssRollingUpgrade
    - Start-AzureRmVmss
    - Restart-AzureRmVmss
    - Stop-AzureRmVmss
    - Remove-AzureRmVmss
    - ConvertTo-AzureRmVMManagedDisk
    - Revoke-AzureRmSnapshotAccess
    - Remove-AzureRmSnapshot
    - Revoke-AzureRmDiskAccess
    - Remove-AzureRmDisk
    - Remove-AzureRmContainerService
    - Remove-AzureRmAvailabilitySet

#### <a name="azurermeventgrid"></a>AzureRM.EventGrid
* 在 Update-AzureRmEventGridSubscription cmdlet 中删除 SubjectBeginsWith/SubjectEndsWith 的 ValidateNotNullOrEmpty 验证条件，允许根据需要将这些参数更改为空字符串。

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* 修复运行 Get-AzureRmKeyVault -Tag 时不返回任何标记的问题

#### <a name="azurermpolicyinsights"></a>AzureRM.PolicyInsights
* 策略见解 cmdlet 的公开发行版
    - 使用 API 版本 2018-04-04
    - 向 Get-AzureRmPolicyStateSummary 的结果添加了 PolicyDefinitionReferenceId

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices.Backup
* 向 RecoveryServices.Backup cmdlet 添加了 -Vault 参数。 传递时，此项会替代 Set-AzureRmRecoveryServicesContext cmdlet。

#### <a name="azurermsql"></a>AzureRM.Sql
* 更新了 Get-AzureRmSqlDatabaseExpanded 的帮助文件中的示例

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* 更新了 Add-AzureRmTrafficManagerEndpointConfig 的帮助文件

#### <a name="azurermwebsites"></a>AzureRM.Websites
* 更新了“Set-AzureRmWebApp”，在使用 -AssignIdentity 时不覆盖 AppSettings
* 更新了“New-AzureRmWebAppSlot”，允许使用 AppServicePlan 作为可选参数

## <a name="621---june-2018"></a>6.2.1 - 2018 年 6 月
### <a name="azurermoperationalinsights"></a>AzureRM.OperationalInsights
* 更新了 PSWorkspace 模型，允许 Network 使用 type 作为参数

## <a name="620---june-2018"></a>6.2.0 - 2018 年 6 月
#### <a name="azurermprofile"></a>AzureRM.Profile
* 修复了 Newtonsoft.Json 的版本 10.0.3 在模块导入时无法加载的问题

#### <a name="azurermcompute"></a>AzureRM.Compute
* VMSS VM 更新功能
    - 增加了“Update-AzureRmVmssVM”和“New-AzureRmVMDataDisk”cmdlet
    - 为“Add-AzureRmVMDataDisk”cmdlet 增加了 VirtualMachineScaleSetVM 参数，支持向 Vmss VM 添加数据磁盘。

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* 将 ADF.Net SDK 版本更新到了 0.8.0-preview，其中包含以下更改：
    - 增加了“配置工厂存储库”操作
    - 更新了 QuickBooks LinkedService，可以公开 consumerKey 和 consumerSecret 属性
    - 已将多个模型类型从 SecretBase 更新为 Object
    - 增加了 Blob 事件触发器

### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* 使用示例输出更新了文档

### <a name="azurermnetwork"></a>AzureRM.Network
* 在网络观察程序 cmdlet 上启用了流量分析参数

#### <a name="azurermresources"></a>AzureRM.Resources
* 修复了从“Get-AzureRmResource”返回的“PSResource”对象的“Properties”属性问题

#### <a name="azurermscheduler"></a>AzureRM.Scheduler
* 修复了更新 ServiceBusQueueJob 无法设置新 Auth 值的问题

### <a name="azurermsql"></a>AzureRM.Sql
* 使用可选的 LicenseType 参数更新了以下 cmdlet
    - New-AzureRmSqlDatabase；Set-AzureRmSqlDatabase
    - New-AzureRmSqlElasticPool；Set-AzureRmSqlElasticPool
    - New-AzureRmSqlDatabaseCopy
    - New-AzureRmSqlDatabaseSecondary
    - Restore-AzureRmSqlDatabase

#### <a name="azurermwebsites"></a>AzureRM.Websites
* 更新了“New-AzureRMWebApp”，可以使用策略库中的常用算法。

## <a name="610---may-2018"></a>6.1.0 - 2018 年 5 月
#### <a name="azurermprofile"></a>AzureRM.Profile
* 修复了运行“Clear-AzureRmContext”时会保留空上下文的问题，该上下文使用旧的默认上下文的名称，导致用户无法使用旧名称创建新的上下文

#### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* 允许在 AS 上执行网关的关联/取消关联操作。

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* 增加了对 ApiVersions、ApiReleases 和 ApiRevisions 的支持
* 增加了对 ServiceFabric 后端的支持
* 增加了对 Application Insights Logger 的支持
* 增加的支持包括认可“基本”SKU 是 API 管理服务的有效 SKU
* 增加的支持包括允许将专用 CA 颁发的证书作为根证书或 CA 证书安装
* 增加的支持包括通过 KeyVault 和多个代理主机名接受自定义 SSL 证书
* 增加了对 MSI 标识的支持
* 增加的支持包括通过 URL 接受策略 注意：以下 cmdlet 将在未来版本中弃用
   - Import-AzureRmApiManagementHostnameCertificate
   - New-AzureRmApiManagementHostnameConfiguration
   - Set-AzureRmApiManagementHostnames
   - Update-AzureRmApiManagementDeployment

#### <a name="azurermbatch"></a>AzureRM.Batch
* 发布新 cmdlet Get-AzureBatchPoolNodeCounts
* 发布新 cmdlet Start-AzureBatchComputeNodeServiceLogUpload

#### <a name="azurermconsumption"></a>AzureRM.Consumption
* 在 Cmdlet Get-AzureRmConsumptionUsageDetail 中增加了新参数 Expand、ResourceGroup、InstanceName、InstanceId、Tags、Top

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* 修复了 Export-AzureRmDataLakeStoreChildItemProperties 的示例
* 修复了 Set-AzureRmDataLakeStoreItemAclEntry 中 Recurse 用例的 null 参数异常 
* 修复了 Set-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAcl、Remove-AzureRmDataLakeStoreItemAclEntry 的帮助文件 

#### <a name="azurermnetwork"></a>AzureRM.Network
* 将网络 SDK 版本从 18.0.0-preview 升至 19.0.0-preview
* 增加了用于创建协议配置的 cmdlet
    - New-AzureRmNetworkWatcherProtocolConfiguration
* 增加了用于向现有的快速路由线路添加新的线路连接的 cmdlet。
    - Add-AzureRmExpressRouteCircuitConnectionConfig
* 增加了用于从现有的快速路由线路删除线路连接的 cmdlet。
    - Remove-AzureRmExpressRouteCircuitConnectionConfig
* 增加了用于检索线路连接的 cmdlet
    - Get-AzureRmExpressRouteCircuitConnectionConfig

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* 修复了使用生成的证书进行服务器身份验证的问题（问题 5998）

#### <a name="azurermsql"></a>AzureRM.Sql
* 更新了审核 cmdlet，允许删除 AuditActions 或 AuditActionGroups
* 修复了设置新的灵活保留策略时使用 Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy 出现的问题。该问题的具体表现是：在命令失败的同时，出现“不再支持使用 Azure 恢复服务保管库和策略配置长期保留策略。 请使用新的灵活保留策略提交请求”错误消息。
* 更新了与 Azure SQL 数据库/ElasticPool 的创建/更新相关的所有 cmdlet，允许使用新的数据库 API，而这些 cmdlet 支持的 SKU 属性则适用于规模和层相关属性。
* 更新的 cmdlet 包括： 
    - New-AzureRmSqlDatabase；Set-AzureRmSqlDatabase
    - New-AzureRmSqlElasticPool；Set-AzureRmSqlElasticPool
    - New-AzureRmSqlDatabaseCopy
    - New-AzureRmSqlDatabaseSecondary
    - Restore-AzureRmSqlDatabase

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* 更新了“Get-AzureRmTrafficManagerProfile”的参数，要求在使用 -Name 参数时使用 -ResourceGroupName 参数。
