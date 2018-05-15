---
title: Azure PowerShell 更改日志 | Microsoft Docs
description: 下面提供了对 Azure PowerShell 最新版本所做更改的历史记录。
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
ms.openlocfilehash: 8515a267e80e5d1f7bb97557efa72b9e86b7b45d
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/08/2018
---
# <a name="release-notes"></a>发行说明

下面是此版本中对 Azure PowerShell 所做的更改列表。

---

## <a name="600---may-2018"></a>6.0.0 - 2018 年 5 月

### <a name="general"></a>常规
* 将模块的最低依赖项设置为 PowerShell 5.0

### <a name="azurestorage"></a>Azure.存储
* 支持用作存储 Blob 容器名称
    - New-AzureStorageBlobContainer
    - Remove-AzureStorageBlobContainer
    - Set-AzureStorageBlobContent
    - Get-AzureStorageBlobContent
* 修复了某些存储 cmdlet 故障输出不包含详细故障信息的问题

### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* 引入多项重大更改
    - 有关详细信息，请参阅迁移指南

### <a name="azurermautomation"></a>AzureRM.Automation
* 从 cmdlet 中删除已弃用的“Tags”别名
    - 'Set-AzureRmAutomationRunbook'

### <a name="azurermbatch"></a>AzureRM.Batch
* 更新了 New-AzureBatchPool 文档，删除了已弃用的示例

### <a name="azurermcdn"></a>AzureRM.Cdn
* 引入多项重大更改
    - 有关详细信息，请参阅迁移指南

### <a name="azurermcompute"></a>AzureRM.Compute
* “New-AzureRmVm”和“New-AzureRmVmss”支持参数的详细输出。
* “New-AzureRmVm”和“New-AzureRmVmss”（简单参数集）支持向 VM 分配用户定义的和（或）系统定义的标识。
* VMSS Redeploy 和 PerformMaintenance 功能
    -  向“Set-AzureRmVmss”和“Set-AzureRmVmssVM”添加新的开关参数 -Redeploy 和 -PerformMaintenance
* 向“Set-AzureRmVMOperatingSystem”cmdlet 添加 DisableVMAgent 开关参数
* “New-AzureRmVm”和“New-AzureRmVmss”（简单参数集）支持“Win10”映像。
* 添加了“Repair-AzureRmVmssServiceFabricUpdateDomain”cmdlet。
* 引入多项重大更改
    - 如需更多详细信息，请参阅迁移指南
* “Set-AzureRmVmDiskEncryptionExtension”使 AAD 参数变为可选

### <a name="azurermdatafactories"></a>AzureRM.DataFactories
* 从 cmdlet 中删除已弃用的“Tags”别名
    - New-AzureRmDataFactory

### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* 将 ADF.Net SDK 版本更新到了 0.7.0-preview，其中包含以下更改：
    - 在 ExecuteSSISPackage 活动上添加了执行参数和连接管理器属性
    - 更新了 PostgreSql 和 MySql 链接服务，使用完整的连接字符串而不是服务器、数据库、架构、用户名和密码
    - 从 DB2 链接服务中删除了架构
    - 从 Teradata 链接服务中删除了架构属性
    - 为 Responsys 添加了 LinkedService、Dataset、CopySource

### <a name="azurermdatalakeanalytics"></a>AzureRM.DataLakeAnalytics
* 从 cmdlet 中删除已弃用的“Tags”别名
    - 'New-AzureRmDataLakeAnalyticsAccount'
    - 'Set-AzureRmDataLakeAnalyticsAccount'

### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* 向 Remove-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAcl 添加递归 Acl 更改这一新功能
* 添加用于在目录下检索内容摘要的新 cmdlet
* 添加用于检索磁盘使用情况和 Acl 转储的新 cmdlet
* 将返回类型 Set-AzureRmDataLakeStoreItemAcl bool 更正为 IEnumerable<DataLakeStoreItemAce>
* 将返回类型 Set-AzureRmDataLakeStoreItemAclEntry bool 更正为 IEnumerable<DataLakeStoreItemAce>
* Export-AzureRmDataLakeStoreItem、Import-AzureRmDataLakeStoreItem、Remove-AzureRmDataLakeStoreItem 中的重大更改

### <a name="azurermdns"></a>AzureRM.Dns
* 引入多项重大更改
    - 有关详细信息，请参阅迁移指南

### <a name="azurermeventhub"></a>AzureRM.EventHub
* 更新了 cmdlet 的帮助文档，增加了缺失的示例

### <a name="azurerminsights"></a>AzureRM.Insights
* 引入了多项重大更改
    - 有关详细信息，请参阅迁移指南

### <a name="azurermiothub"></a>AzureRM.IotHub
* 启用 IotHub 的标记和基本 SKU

### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* 管道方案支持方面的重大更改
* 添加了新 cmdlet：Backup/Restore-AzureKeyVaultManagedStorageAccount、Backup/Restore-AzureKeyVaultCertificate、Undo-AzureKeyVaultManagedStorageSasDefinitionRemoval、Undo-AzureKeyVaultManagedStorageAccountRemoval

### <a name="azurermmachinelearning"></a>AzureRM.MachineLearning
* 从 cmdlet 中删除已弃用的“Tags”别名
    - Update-AzureRmMlCommitmentPlan

### <a name="azurermmedia"></a>AzureRM.Media
* 从 cmdlet 中删除已弃用的“Tags”别名
    - 'Set-AzureRmMediaService'

### <a name="azurermnetwork"></a>AzureRM.Network
* 增加对 DDoS 防护计划资源的支持
* 引入了多项重大更改
    - 有关详细信息，请参阅迁移指南

### <a name="azurermnotificationhubs"></a>AzureRM.NotificationHubs
* 引入多项重大更改
    - 有关详细信息，请参阅迁移指南

### <a name="azurermoperationalinsights"></a>AzureRM.OperationalInsights
* 引入多项重大更改
    - 有关详细信息，请参阅迁移指南

### <a name="azurermprofile"></a>AzureRM.Profile
* 默认启用上下文自动保存功能
* 向 Azure 环境美国政府版添加 USGovernmentOperationalInsightsEndpoint 和 USGovernmentOperationalInsightsEndpointResourceId 属性。

### <a name="azurermrecoveryservicessiterecovery"></a>AzureRM.RecoveryServices.SiteRecovery
* 修复了 SiteRecovery 方案中的身份验证标头

### <a name="azurermrediscache"></a>AzureRM.RedisCache
* 引入了多项重大更改
    - 有关详细信息，请参阅迁移指南

### <a name="azurermresources"></a>AzureRM.Resources
* 从 Get-AzureRmRoledefinition 调用中删除过时的参数 -AtScopeAndBelow
* 在 Get-AzureRmRoleAssignment 结果中包括针对已删除的 USers/Groups/ServicePrincipals 的分配
* 为 Scope 和 ResourceType 添加了 Tab 补全选项
* 添加用于创建 ServicePrincipals 的便捷 cmdlet
* 在 Get-AzureRmResource 中合并 Get- 和 Find- 功能
* 添加 AD Cmdlet：
  - Remove-AzureRmADGroupMember
  - Get-AzureRmADGroup
  - New-AzureRmADGroup
  - Remove-AzureRmADGroup
  - Remove-AzureRmADUser
  - Update-AzureRmADApplication
  - Update-AzureRmADServicePrincipal
  - Update-AzureRmADUser

### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* 更新默认的 Linux 映像版本 SKU
  - NewAzureServiceFabricCluster.cs 默认 UbuntuServer1604 SKU 更新

### <a name="azurermstorage"></a>AzureRM.Storage
* 引入了多项重大更改
    - 有关详细信息，请参阅迁移指南

### <a name="azurermwebsites"></a>AzureRM.Websites
* 升级到最新版本的网站 SDK
* 为 Set-AzureRmWebApp 和 Set-AzureRmWebAppSlot 增加了 -AssignIdentity 和 -Httpsonly 属性
* 增加了两个新的 cmdlet：Get-AzureRmWebAppSnapshots 和 Restore-AzureRmWebAppSnapshot
