---
title: Azure PowerShell 更改日志 | Microsoft Docs
description: 下面提供了对 Azure PowerShell 最新版本所做更改的历史记录。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 5/1/2018
ms.openlocfilehash: 5bc3c9079cb4019bdb2255ab1f947e8ad35ae4cc
ms.sourcegitcommit: c98e3a21037ebd82936828bcb544eed902b24212
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/08/2018
ms.locfileid: "34853451"
---
# <a name="release-notes"></a>发行说明

下面是此版本中对 Azure PowerShell 所做的更改列表。

---
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