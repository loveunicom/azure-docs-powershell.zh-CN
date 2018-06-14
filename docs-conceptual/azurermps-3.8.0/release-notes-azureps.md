---
title: Azure PowerShell 更改日志 | Microsoft Docs
description: 下面提供了对 Azure PowerShell 最新版本所做更改的历史记录。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: b777a5fe036cda58a930ac0f5aaef3b9a7c2b420
ms.sourcegitcommit: c98e3a21037ebd82936828bcb544eed902b24212
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/08/2018
ms.locfileid: "34853434"
---
# <a name="release-notes"></a>发行说明

下面是此版本中对 Azure PowerShell 所做的更改列表。

## <a name="version-380"></a>版本 3.8.0
* 计算
  - 修复了 Get-* cmdlet 中的 bug，以便能够检索多个数据页面（超过 120 项）
* DataLakeAnalytics
  - 修复了某些命令的帮助信息，提供了适当的措辞和示例。
* DataLakeStore
  - 为 `Get-AzureRMDataLakeStoreItemContent` cmdlet 添加了头部和尾部支持。 这样，便可以显示“前 N 个”或“后 N 个”换行符分隔的行。
* HDInsight
  - 添加了对 RServer 群集类型的支持
    + 可以在 New-AzureRmHDInsightCluster 或 New-AzureRmHDInsightClusterConfig 中为 RServer 群集指定边缘节点 VM 大小
    + 现在，RServer 是 Add-AzureRmHDInsightConfigValues 中的一个配置选项。 它允许设置 RStudio 标志来指示应执行 R Studio 安装。
* LogicApp
  - 修复了 Set-AzureRmIntegrationAccountSchema 和 Set-AzureRmIntegrationAccountMap cmdlet，解决了内容链接问题（同时设置内容和内容链接导致更新失败）。
* 网络
  - 在应用程序网关中添加了对新 Web 应用程序防火墙功能的支持
    + 添加了 New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig
    + 添加了 Get-AzureRmApplicationGatewayAvailableWafRuleSets（别名：List-AzureRmApplicationGatewayAvailableWafRuleSets）
    + 更新了 New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration：添加了参数 -RuleSetType -RuleSetVersion 和 -DisabledRuleGroups
    + 更新了 Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration：添加了参数 -RuleSetType -RuleSetVersion 和 -DisabledRuleGroups
  - 在虚拟网络网关连接中添加了对 IPSec 策略的支持
  - 添加了 New-AzureRmIpsecPolicy
  - 更新了 New-AzureRmVirtualNetworkGatewayConnection：添加了参数 -IpsecPolicies 和 -UsePolicyBasedTrafficSelectors
* 配置文件
  - *已弃用*：Save-AzureRmProfile 已重命名为 Save-AzureRmContext，旧 cmdlet 名称有一个别名，下一版本将删除该别名。
  - *已弃用*：Select-AzureRmProfile 已重命名为 Import-AzureRmContext，旧 cmdlet 名称有一个别名，下一版本将删除该别名。
  - 下一版本会更改配置文件 cmdlet 的 PSAzureContext 和 PSAzureProfile 输出类型。
  - 在下一版本中，Save-AzureRmContext cmdlet 将没有 OutputType。
  - 修复了 cmdlet 通用代码中的 Bug，现在对数据哈希使用符合 FIPS 规范的算法：https://github.com/Azure/azure-powershell/issues/3651
* Sql
  - 修复了 Azure 故障转移组 Cmdlet 中的 Bug
  - 修复操作轮询
  - 修复了将 FailoverPolicy 设置为 Manual 时的 GracePeriodWithDataLossHour 值
* TrafficManager
  - 支持“地理”流量路由方法
    + 为 New-AzureRmTrafficManagerProfile 的 TrafficRoutingMethod 参数新增了值“Geographic”
    + 为 New-AzureRmTrafficManagerEndpoint 和 Add-AzureRmTrafficManagerEndpointConfig 新增了参数“GeoMapping”
    + 修复了 Get-AzureRmTrafficManagerProfile 在返回配置文件集合时的管道
* ServiceManagement
  - Restart-AzureVM：添加了 InitiateMaintenance 参数用于在 VM 重新启动期间执行维护。
  - Get-AzureVM：添加了“维护状态”字段。
  - 添加了新的 cmdlet 用于支持恢复服务保管库升级
    + Test-AzureRecoveryServicesVaultUpgrade
    + Invoke-AzureRecoveryServicesVaultUpgrade
