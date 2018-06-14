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
# <a name="release-notes"></a><span data-ttu-id="46617-103">发行说明</span><span class="sxs-lookup"><span data-stu-id="46617-103">Release notes</span></span>

<span data-ttu-id="46617-104">下面是此版本中对 Azure PowerShell 所做的更改列表。</span><span class="sxs-lookup"><span data-stu-id="46617-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

## <a name="version-380"></a><span data-ttu-id="46617-105">版本 3.8.0</span><span class="sxs-lookup"><span data-stu-id="46617-105">Version 3.8.0</span></span>
* <span data-ttu-id="46617-106">计算</span><span class="sxs-lookup"><span data-stu-id="46617-106">Compute</span></span>
  - <span data-ttu-id="46617-107">修复了 Get-\* cmdlet 中的 bug，以便能够检索多个数据页面（超过 120 项）</span><span class="sxs-lookup"><span data-stu-id="46617-107">Fix bug in Get-\* cmdlets, to allow retrieving multiple pages of data (more than 120 items)</span></span>
* <span data-ttu-id="46617-108">DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="46617-108">DataLakeAnalytics</span></span>
  - <span data-ttu-id="46617-109">修复了某些命令的帮助信息，提供了适当的措辞和示例。</span><span class="sxs-lookup"><span data-stu-id="46617-109">Fix help for some commands to have the proper verbage and examples.</span></span>
* <span data-ttu-id="46617-110">DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="46617-110">DataLakeStore</span></span>
  - <span data-ttu-id="46617-111">为 `Get-AzureRMDataLakeStoreItemContent` cmdlet 添加了头部和尾部支持。</span><span class="sxs-lookup"><span data-stu-id="46617-111">Add support for head and tail to the `Get-AzureRMDataLakeStoreItemContent` cmdlet.</span></span> <span data-ttu-id="46617-112">这样，便可以显示“前 N 个”或“后 N 个”换行符分隔的行。</span><span class="sxs-lookup"><span data-stu-id="46617-112">This enables returning the top N or last N new line delimited rows to be displayed.</span></span>
* <span data-ttu-id="46617-113">HDInsight</span><span class="sxs-lookup"><span data-stu-id="46617-113">HDInsight</span></span>
  - <span data-ttu-id="46617-114">添加了对 RServer 群集类型的支持</span><span class="sxs-lookup"><span data-stu-id="46617-114">Added support for RServer cluster type</span></span>
    + <span data-ttu-id="46617-115">可以在 New-AzureRmHDInsightCluster 或 New-AzureRmHDInsightClusterConfig 中为 RServer 群集指定边缘节点 VM 大小</span><span class="sxs-lookup"><span data-stu-id="46617-115">Edgenode VM size can be specified for RServer cluster in New-AzureRmHDInsightCluster or New-AzureRmHDInsightClusterConfig</span></span>
    + <span data-ttu-id="46617-116">现在，RServer 是 Add-AzureRmHDInsightConfigValues 中的一个配置选项。</span><span class="sxs-lookup"><span data-stu-id="46617-116">RServer is now a configuration option in Add-AzureRmHDInsightConfigValues.</span></span> <span data-ttu-id="46617-117">它允许设置 RStudio 标志来指示应执行 R Studio 安装。</span><span class="sxs-lookup"><span data-stu-id="46617-117">It allows for RStudio flag to be set to indicate that R Studio installation should be done.</span></span>
* <span data-ttu-id="46617-118">LogicApp</span><span class="sxs-lookup"><span data-stu-id="46617-118">LogicApp</span></span>
  - <span data-ttu-id="46617-119">修复了 Set-AzureRmIntegrationAccountSchema 和 Set-AzureRmIntegrationAccountMap cmdlet，解决了内容链接问题（同时设置内容和内容链接导致更新失败）。</span><span class="sxs-lookup"><span data-stu-id="46617-119">Set-AzureRmIntegrationAccountSchema and Set-AzureRmIntegrationAccountMap cmdlets are fixed for the contentlink issue(Both content and contentlink were set resulting in update failure).</span></span>
* <span data-ttu-id="46617-120">网络</span><span class="sxs-lookup"><span data-stu-id="46617-120">Network</span></span>
  - <span data-ttu-id="46617-121">在应用程序网关中添加了对新 Web 应用程序防火墙功能的支持</span><span class="sxs-lookup"><span data-stu-id="46617-121">Added support for new web application firewall features to Application Gateways</span></span>
    + <span data-ttu-id="46617-122">添加了 New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig</span><span class="sxs-lookup"><span data-stu-id="46617-122">Added New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig</span></span>
    + <span data-ttu-id="46617-123">添加了 Get-AzureRmApplicationGatewayAvailableWafRuleSets（别名：List-AzureRmApplicationGatewayAvailableWafRuleSets）</span><span class="sxs-lookup"><span data-stu-id="46617-123">Added Get-AzureRmApplicationGatewayAvailableWafRuleSets (Alias: List-AzureRmApplicationGatewayAvailableWafRuleSets)</span></span>
    + <span data-ttu-id="46617-124">更新了 New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration：添加了参数 -RuleSetType -RuleSetVersion 和 -DisabledRuleGroups</span><span class="sxs-lookup"><span data-stu-id="46617-124">Updated New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration: Added parameter -RuleSetType -RuleSetVersion and -DisabledRuleGroups</span></span>
    + <span data-ttu-id="46617-125">更新了 Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration：添加了参数 -RuleSetType -RuleSetVersion 和 -DisabledRuleGroups</span><span class="sxs-lookup"><span data-stu-id="46617-125">Updated Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration: Added parameter -RuleSetType -RuleSetVersion and -DisabledRuleGroups</span></span>
  - <span data-ttu-id="46617-126">在虚拟网络网关连接中添加了对 IPSec 策略的支持</span><span class="sxs-lookup"><span data-stu-id="46617-126">Added support for IPSec policies to Virtual Network Gateway Connections</span></span>
  - <span data-ttu-id="46617-127">添加了 New-AzureRmIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="46617-127">Added New-AzureRmIpsecPolicy</span></span>
  - <span data-ttu-id="46617-128">更新了 New-AzureRmVirtualNetworkGatewayConnection：添加了参数 -IpsecPolicies 和 -UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="46617-128">Updated New-AzureRmVirtualNetworkGatewayConnection: Added parameter -IpsecPolicies and -UsePolicyBasedTrafficSelectors</span></span>
* <span data-ttu-id="46617-129">配置文件</span><span class="sxs-lookup"><span data-stu-id="46617-129">Profile</span></span>
  - <span data-ttu-id="46617-130">*已弃用*：Save-AzureRmProfile 已重命名为 Save-AzureRmContext，旧 cmdlet 名称有一个别名，下一版本将删除该别名。</span><span class="sxs-lookup"><span data-stu-id="46617-130">*Obsolete*: Save-AzureRmProfile is renamed to Save-AzureRmContext, there is an alias to the old cmdlet name, the alias will be removed in the next release.</span></span>
  - <span data-ttu-id="46617-131">*已弃用*：Select-AzureRmProfile 已重命名为 Import-AzureRmContext，旧 cmdlet 名称有一个别名，下一版本将删除该别名。</span><span class="sxs-lookup"><span data-stu-id="46617-131">*Obsolete*: Select-AzureRmProfile is renamed to Import-AzureRmContext, there is an alias to the old cmdlet name, the alias will be removed in the next release.</span></span>
  - <span data-ttu-id="46617-132">下一版本会更改配置文件 cmdlet 的 PSAzureContext 和 PSAzureProfile 输出类型。</span><span class="sxs-lookup"><span data-stu-id="46617-132">The PSAzureContext and PSAzureProfile output types of profile cmdlets will be changed in the next release.</span></span>
  - <span data-ttu-id="46617-133">在下一版本中，Save-AzureRmContext cmdlet 将没有 OutputType。</span><span class="sxs-lookup"><span data-stu-id="46617-133">The Save-AzureRmContext cmdlet will have no OutputType in the next release.</span></span>
  - <span data-ttu-id="46617-134">修复了 cmdlet 通用代码中的 Bug，现在对数据哈希使用符合 FIPS 规范的算法：https://github.com/Azure/azure-powershell/issues/3651</span><span class="sxs-lookup"><span data-stu-id="46617-134">Fix bug in cmdlet common code to use FIPS-compliant algorithm for data hashes: https://github.com/Azure/azure-powershell/issues/3651</span></span>
* <span data-ttu-id="46617-135">Sql</span><span class="sxs-lookup"><span data-stu-id="46617-135">Sql</span></span>
  - <span data-ttu-id="46617-136">修复了 Azure 故障转移组 Cmdlet 中的 Bug</span><span class="sxs-lookup"><span data-stu-id="46617-136">Bug fixes on Azure Failover Group Cmdlets</span></span>
  - <span data-ttu-id="46617-137">修复操作轮询</span><span class="sxs-lookup"><span data-stu-id="46617-137">Fix for operation polling</span></span>
  - <span data-ttu-id="46617-138">修复了将 FailoverPolicy 设置为 Manual 时的 GracePeriodWithDataLossHour 值</span><span class="sxs-lookup"><span data-stu-id="46617-138">Fix GracePeriodWithDataLossHour value when setting FailoverPolicy to Manual</span></span>
* <span data-ttu-id="46617-139">TrafficManager</span><span class="sxs-lookup"><span data-stu-id="46617-139">TrafficManager</span></span>
  - <span data-ttu-id="46617-140">支持“地理”流量路由方法</span><span class="sxs-lookup"><span data-stu-id="46617-140">Support for the Geographic traffic routing method</span></span>
    + <span data-ttu-id="46617-141">为 New-AzureRmTrafficManagerProfile 的 TrafficRoutingMethod 参数新增了值“Geographic”</span><span class="sxs-lookup"><span data-stu-id="46617-141">New value 'Geographic' for the TrafficRoutingMethod parameter of New-AzureRmTrafficManagerProfile</span></span>
    + <span data-ttu-id="46617-142">为 New-AzureRmTrafficManagerEndpoint 和 Add-AzureRmTrafficManagerEndpointConfig 新增了参数“GeoMapping”</span><span class="sxs-lookup"><span data-stu-id="46617-142">New parameter 'GeoMapping' for the New-AzureRmTrafficManagerEndpoint and Add-AzureRmTrafficManagerEndpointConfig</span></span>
    + <span data-ttu-id="46617-143">修复了 Get-AzureRmTrafficManagerProfile 在返回配置文件集合时的管道</span><span class="sxs-lookup"><span data-stu-id="46617-143">Fix piping for Get-AzureRmTrafficManagerProfile when it returns a collection of profiles</span></span>
* <span data-ttu-id="46617-144">ServiceManagement</span><span class="sxs-lookup"><span data-stu-id="46617-144">ServiceManagement</span></span>
  - <span data-ttu-id="46617-145">Restart-AzureVM：添加了 InitiateMaintenance 参数用于在 VM 重新启动期间执行维护。</span><span class="sxs-lookup"><span data-stu-id="46617-145">Restart-AzureVM: Added InitiateMaintenance parameter for performing maintenance during VM restart.</span></span>
  - <span data-ttu-id="46617-146">Get-AzureVM：添加了“维护状态”字段。</span><span class="sxs-lookup"><span data-stu-id="46617-146">Get-AzureVM: Added Maintenance Status field.</span></span>
  - <span data-ttu-id="46617-147">添加了新的 cmdlet 用于支持恢复服务保管库升级</span><span class="sxs-lookup"><span data-stu-id="46617-147">Added new cmdlets to support Recovery Services vault upgrade</span></span>
    + <span data-ttu-id="46617-148">Test-AzureRecoveryServicesVaultUpgrade</span><span class="sxs-lookup"><span data-stu-id="46617-148">Test-AzureRecoveryServicesVaultUpgrade</span></span>
    + <span data-ttu-id="46617-149">Invoke-AzureRecoveryServicesVaultUpgrade</span><span class="sxs-lookup"><span data-stu-id="46617-149">Invoke-AzureRecoveryServicesVaultUpgrade</span></span>
