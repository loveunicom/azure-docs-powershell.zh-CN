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
ms.openlocfilehash: 7f517f0b3768a2075557b131158ee1264ea9ab3f
ms.sourcegitcommit: 80a3da199954d0ab78765715fb49793e89a30f12
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/22/2018
ms.locfileid: "52259449"
---
# <a name="release-notes"></a><span data-ttu-id="368d1-103">发行说明</span><span class="sxs-lookup"><span data-stu-id="368d1-103">Release notes</span></span>

<span data-ttu-id="368d1-104">下面是此版本中对 Azure PowerShell 所做的更改列表。</span><span class="sxs-lookup"><span data-stu-id="368d1-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="6130---november-2018"></a><span data-ttu-id="368d1-105">6.13.0 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="368d1-105">6.13.0 - November 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="368d1-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="368d1-106">AzureRM.Profile</span></span>
* <span data-ttu-id="368d1-107">更新通用代码以使用最新版本的 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="368d1-107">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="368d1-108">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="368d1-108">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="368d1-109">更新类型映射问题的依赖项</span><span class="sxs-lookup"><span data-stu-id="368d1-109">Update dependencies for type mapping issue</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="368d1-110">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="368d1-110">AzureRM.Automation</span></span>
* <span data-ttu-id="368d1-111">基于 Swagger 的 Azure 自动化 cmdlet</span><span class="sxs-lookup"><span data-stu-id="368d1-111">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="368d1-112">增加了更新管理 cmdlet</span><span class="sxs-lookup"><span data-stu-id="368d1-112">Added Update Management cmdlets</span></span>
* <span data-ttu-id="368d1-113">增加了源代码管理 cmdlet</span><span class="sxs-lookup"><span data-stu-id="368d1-113">Added Source Control cmdlets</span></span>
* <span data-ttu-id="368d1-114">增加了 Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span><span class="sxs-lookup"><span data-stu-id="368d1-114">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="368d1-115">修复了 DSC Register Node 命令</span><span class="sxs-lookup"><span data-stu-id="368d1-115">Fixed the DSC Register Node command</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="368d1-116">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="368d1-116">AzureRM.Compute</span></span>
* <span data-ttu-id="368d1-117">修复了 SystemAssigned 标识的标识问题</span><span class="sxs-lookup"><span data-stu-id="368d1-117">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="368d1-118">更新类型映射问题的依赖项</span><span class="sxs-lookup"><span data-stu-id="368d1-118">Update dependencies for type mapping issue</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="368d1-119">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="368d1-119">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="368d1-120">更新类型映射问题的依赖项</span><span class="sxs-lookup"><span data-stu-id="368d1-120">Update dependencies for type mapping issue</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="368d1-121">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="368d1-121">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="368d1-122">更新市场 cmdlet 的示例说明</span><span class="sxs-lookup"><span data-stu-id="368d1-122">update the examples description for marketplace cmdlets</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="368d1-123">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="368d1-123">AzureRM.Network</span></span>
* <span data-ttu-id="368d1-124">增加了 cmdlet New-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayCustomError、Get-AzureRmApplicationGatewayCustomError、Set-AzureRmApplicationGatewayCustomError、Remove-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayHttpListenerCustomError、Get-AzureRmApplicationGatewayHttpListenerCustomError、Set-AzureRmApplicationGatewayHttpListenerCustomError、Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="368d1-124">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="368d1-125">将 ICMP 重新添加到受支持的 AzureFirewall 网络协议</span><span class="sxs-lookup"><span data-stu-id="368d1-125">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="368d1-126">更新 cmdlet Test-AzureRmNetworkWatcherConnectivity，在目标 ID、地址和端口上添加验证。</span><span class="sxs-lookup"><span data-stu-id="368d1-126">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="368d1-127">修复 VirtualNetwork 映射中内存使用的问题</span><span class="sxs-lookup"><span data-stu-id="368d1-127">Fix issues with memory usage in VirtualNetwork map</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="368d1-128">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="368d1-128">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="368d1-129">修复受保护文件共享的策略修改问题。</span><span class="sxs-lookup"><span data-stu-id="368d1-129">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="368d1-130">将策略时区转换成了大写形式。</span><span class="sxs-lookup"><span data-stu-id="368d1-130">Converted policy timezone to uppercase.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="368d1-131">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="368d1-131">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="368d1-132">更正了 New-AzureRmRecoveryServicesAsrProtectableItem 中的示例</span><span class="sxs-lookup"><span data-stu-id="368d1-132">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="368d1-133">更新类型映射问题的依赖项</span><span class="sxs-lookup"><span data-stu-id="368d1-133">Update dependencies for type mapping issue</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="368d1-134">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="368d1-134">AzureRM.Relay</span></span>
* <span data-ttu-id="368d1-135">已将可选参数 -KeyValue 添加到 New-AzureRmRelayKey cmdlet，该参数允许用户提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="368d1-135">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="368d1-136">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="368d1-136">AzureRM.Resources</span></span>
* <span data-ttu-id="368d1-137">更新 `New-AzureRmPolicyAssignment` 和 `Set-AzureRmPolicyAssignment` 中资源标识相关参数的帮助文档</span><span class="sxs-lookup"><span data-stu-id="368d1-137">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="368d1-138">为使用 -Metadata 的 New-AzureRmPolicyDefinition 添加一个示例</span><span class="sxs-lookup"><span data-stu-id="368d1-138">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="368d1-139">修复后允许在 NetStandard 的 Tag 键中保留大小写：#7678 #7703</span><span class="sxs-lookup"><span data-stu-id="368d1-139">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="368d1-140">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="368d1-140">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="368d1-141">在即将发布的重大更改中添加弃用消息</span><span class="sxs-lookup"><span data-stu-id="368d1-141">Add deprecation messages for upcoming breaking changes</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="368d1-142">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="368d1-142">AzureRM.Sql</span></span>
* <span data-ttu-id="368d1-143">为 Azure SQL 数据库托管实例和 Azure SQL 托管数据库上的 CRUD 操作添加了新的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="368d1-143">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="368d1-144">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="368d1-144">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="368d1-145">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="368d1-145">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="368d1-146">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="368d1-146">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="368d1-147">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="368d1-147">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="368d1-148">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="368d1-148">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="368d1-149">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="368d1-149">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="368d1-150">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="368d1-150">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="368d1-151">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="368d1-151">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="368d1-152">允许在服务器或数据库上进行扩展的审核策略管理。</span><span class="sxs-lookup"><span data-stu-id="368d1-152">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="368d1-153">添加了新的参数 (PredicateExpression)，用于筛选审核日志。</span><span class="sxs-lookup"><span data-stu-id="368d1-153">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="368d1-154">修改了 Cmdlet，以便使用 SQL 客户端而不是旧客户端。</span><span class="sxs-lookup"><span data-stu-id="368d1-154">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="368d1-155">Set-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="368d1-155">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="368d1-156">Get-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="368d1-156">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="368d1-157">Set-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="368d1-157">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="368d1-158">Get-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="368d1-158">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="368d1-159">修复了将 Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings 与存储帐户名称参数集配合使用时出现的问题</span><span class="sxs-lookup"><span data-stu-id="368d1-159">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="6120---november-2018"></a><span data-ttu-id="368d1-160">6.12.0 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="368d1-160">6.12.0 - November 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="368d1-161">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="368d1-161">AzureRM.Profile</span></span>
* <span data-ttu-id="368d1-162">更新通用代码以使用最新版本的 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="368d1-162">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="368d1-163">将 Connect-AzureRmAccount cmdlet 中的 TenantId 参数重命名为 Tenant，并为 TenantId 添加别名</span><span class="sxs-lookup"><span data-stu-id="368d1-163">Rename param TenantId in cmdlet Connect-AzureRmAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="368d1-164">更新了 Connect-AzureRmAccount 的 TenantId 说明</span><span class="sxs-lookup"><span data-stu-id="368d1-164">Updated TenantId description for Connect-AzureRmAccount</span></span>
* <span data-ttu-id="368d1-165">修复了在提供租户域时失败的登录的错误消息</span><span class="sxs-lookup"><span data-stu-id="368d1-165">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="368d1-166">为租户中没有订阅的帐户修复了上下文名称冲突的问题</span><span class="sxs-lookup"><span data-stu-id="368d1-166">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="368d1-167">修复了在使用 MSI 时的 DataLake 终结点问题</span><span class="sxs-lookup"><span data-stu-id="368d1-167">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="368d1-168">修复了在未连接时会引发“Disconnect-AzureRmAccount”的问题</span><span class="sxs-lookup"><span data-stu-id="368d1-168">Fix issue where 'Disconnect-AzureRmAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azurermautomation"></a><span data-ttu-id="368d1-169">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="368d1-169">AzureRM.Automation</span></span>
* <span data-ttu-id="368d1-170">已将 cmdlet DLL 文件名重命名为 Microsoft.Azure.Commands.Automation.dll</span><span class="sxs-lookup"><span data-stu-id="368d1-170">Renamed cmdlet DLL filename to Microsoft.Azure.Commands.Automation.dll</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="368d1-171">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="368d1-171">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="368d1-172">添加了 Get-AzureRmCognitiveServicesAccountSkus 操作。</span><span class="sxs-lookup"><span data-stu-id="368d1-172">Add Get-AzureRmCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="368d1-173">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="368d1-173">AzureRM.Compute</span></span>
* <span data-ttu-id="368d1-174">添加了 Add-AzureRmVmssVMDataDisk 和 Remove-AzureRmVmssVMDataDisk cmdlet</span><span class="sxs-lookup"><span data-stu-id="368d1-174">Add Add-AzureRmVmssVMDataDisk and Remove-AzureRmVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="368d1-175">Get-AzureRmVMImage 显示 AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="368d1-175">Get-AzureRmVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="368d1-176">修复了 SetAzureRmVMChefExtension BootstrapOptions 和 -JsonAttribute 选项值未以 json 格式设置的问题。</span><span class="sxs-lookup"><span data-stu-id="368d1-176">Fixed SetAzureRmVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="368d1-177">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="368d1-177">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="368d1-178">将 DataLake 程序包更新至 1.1.10。</span><span class="sxs-lookup"><span data-stu-id="368d1-178">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="368d1-179">将默认并发添加到多线程操作。</span><span class="sxs-lookup"><span data-stu-id="368d1-179">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="368d1-180">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="368d1-180">AzureRM.Insights</span></span>
* <span data-ttu-id="368d1-181">修复了问题 #7267（自动缩放区域）</span><span class="sxs-lookup"><span data-stu-id="368d1-181">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="368d1-182">创建新的自动缩放规则时未正确设置枚举的参数（始终将它们设置为默认值）的问题。</span><span class="sxs-lookup"><span data-stu-id="368d1-182">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="368d1-183">修复了问题 #7513 [见解] Set-AzureRMDiagnosticSetting 在创建设置期间需要显式指定类别</span><span class="sxs-lookup"><span data-stu-id="368d1-183">Fixed issue #7513 [Insights] Set-AzureRMDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="368d1-184">现在该 cmdlet 不需要在创建期间显式指示要启用的类别，即它会按记录工作</span><span class="sxs-lookup"><span data-stu-id="368d1-184">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="368d1-185">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="368d1-185">AzureRM.Network</span></span>
* <span data-ttu-id="368d1-186">已将 PeeringType 更改为以下 cmdlet 的必需参数：</span><span class="sxs-lookup"><span data-stu-id="368d1-186">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="368d1-187">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="368d1-187">Get-AzureRmExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="368d1-188">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="368d1-188">Get-AzureRmExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="368d1-189">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="368d1-189">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="368d1-190">Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="368d1-190">Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="368d1-191">Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="368d1-191">Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="368d1-192">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="368d1-192">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="368d1-193">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="368d1-193">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="368d1-194">添加了策略修正 cmdlet</span><span class="sxs-lookup"><span data-stu-id="368d1-194">Added policy remediation cmdlets</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="368d1-195">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="368d1-195">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="368d1-196">添加了对恢复服务中 azure 文件共享的支持。</span><span class="sxs-lookup"><span data-stu-id="368d1-196">Added support for azure file shares in recovery services.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="368d1-197">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="368d1-197">AzureRM.Resources</span></span>
* <span data-ttu-id="368d1-198">https://github.com/Azure/azure-powershell/issues/7402 的修复</span><span class="sxs-lookup"><span data-stu-id="368d1-198">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="368d1-199">允许对“Get-AzureRmResource”使用“-ResourceId”参数来列出资源</span><span class="sxs-lookup"><span data-stu-id="368d1-199">Allow listing resources using the '-ResourceId' parameter for 'Get-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="368d1-200">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="368d1-200">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="368d1-201">为 PSServiceBusMigrationConfigurationAttributes 添加了 MigrationState 只读属性，这将有助于了解迁移状态。</span><span class="sxs-lookup"><span data-stu-id="368d1-201">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="368d1-202">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="368d1-202">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="368d1-203">修复了将证书添加到 Linux Vmss 的问题。</span><span class="sxs-lookup"><span data-stu-id="368d1-203">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="368d1-204">修复了“Add-AzureRmServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="368d1-204">Fix 'Add-AzureRmServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="368d1-205">使用来自新证书的正确指纹 (Azure/service-fabric-issues#932)。</span><span class="sxs-lookup"><span data-stu-id="368d1-205">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="368d1-206">正确显示异常 (Azure/service-fabric-issues#1054)。</span><span class="sxs-lookup"><span data-stu-id="368d1-206">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="368d1-207">修复了“Update-AzureRmServiceFabricDurability”以在开始 Vmss CreateOrUpdate 操作之前更新群集配置。</span><span class="sxs-lookup"><span data-stu-id="368d1-207">Fix 'Update-AzureRmServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="6110---october-2018"></a><span data-ttu-id="368d1-208">6.11.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="368d1-208">6.11.0 - October 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="368d1-209">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="368d1-209">AzureRM.Profile</span></span>
* <span data-ttu-id="368d1-210">修复了 CloudShell 中 Get-AzureRmSubscription 的问题</span><span class="sxs-lookup"><span data-stu-id="368d1-210">Fix issue with Get-AzureRmSubscription in CloudShell</span></span>
* <span data-ttu-id="368d1-211">更新通用代码以使用最新版本的 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="368d1-211">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="368d1-212">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="368d1-212">AzureRM.Backup</span></span>
* <span data-ttu-id="368d1-213">已弃用 Azure 备份 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="368d1-213">Deprecated Azure Backup cmdlets.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="368d1-214">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="368d1-214">AzureRM.Compute</span></span>
* <span data-ttu-id="368d1-215">向 VM 大小的允许列表添加了新的大小，这样就可以在将简单的参数集用于“New-AzureRmVm”时为这些大小启用加速网络</span><span class="sxs-lookup"><span data-stu-id="368d1-215">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzureRmVm'</span></span>
* <span data-ttu-id="368d1-216">向所有 cmdlet 添加了 ResourceName 参数补全选项。</span><span class="sxs-lookup"><span data-stu-id="368d1-216">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="368d1-217">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="368d1-217">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="368d1-218">添加虚拟网络规则的支持</span><span class="sxs-lookup"><span data-stu-id="368d1-218">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="368d1-219">Get-AzureRmDataLakeStoreVirtualNetworkRule：获取或列出 Azure Data Lake Store 虚拟网络规则。</span><span class="sxs-lookup"><span data-stu-id="368d1-219">Get-AzureRmDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="368d1-220">Add-AzureRmDataLakeStoreVirtualNetworkRule：向指定的 Data Lake Store 帐户添加虚拟网络规则。</span><span class="sxs-lookup"><span data-stu-id="368d1-220">Add-AzureRmDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="368d1-221">Set-AzureRmDataLakeStoreVirtualNetworkRule：在指定的 Data Lake Store 帐户中修改指定的虚拟网络规则。</span><span class="sxs-lookup"><span data-stu-id="368d1-221">Set-AzureRmDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="368d1-222">Remove-AzureRmDataLakeStoreVirtualNetworkRule：删除 Azure Data Lake Store 虚拟网络规则。</span><span class="sxs-lookup"><span data-stu-id="368d1-222">Remove-AzureRmDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="368d1-223">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="368d1-223">AzureRM.Network</span></span>
* <span data-ttu-id="368d1-224">更新 cmdlet Test-AzureRmNetworkWatcherConnectivity，向后端传递协议值。</span><span class="sxs-lookup"><span data-stu-id="368d1-224">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="368d1-225">向所有 cmdlet 添加了 ResourceName 参数补全选项。</span><span class="sxs-lookup"><span data-stu-id="368d1-225">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="368d1-226">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="368d1-226">AzureRM.Resources</span></span>
* <span data-ttu-id="368d1-227">通过在方案中添加一个有意义的异常，修复了 Get-AzureRMRoleDefinition 在默认配置文件中没有订阅且未指定范围的情况下引发难以理解异常的问题。</span><span class="sxs-lookup"><span data-stu-id="368d1-227">Fix isssue where Get-AzureRMRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="368d1-228">另外，已将默认参数集设置为“RoleDefinitionNameParameterSet”。</span><span class="sxs-lookup"><span data-stu-id="368d1-228">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="6100---october-2018"></a><span data-ttu-id="368d1-229">6.10.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="368d1-229">6.10.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="368d1-230">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="368d1-230">Azure.Storage</span></span>
* <span data-ttu-id="368d1-231">修复了 Copy Blob/File 在目标有元数据问题时不会复制元数据的问题</span><span class="sxs-lookup"><span data-stu-id="368d1-231">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="368d1-232">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="368d1-232">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="368d1-233">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="368d1-233">Start-AzureStorageFileCopy</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="368d1-234">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="368d1-234">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="368d1-235">在没有现有帐户的情况下支持 Get-AzureRmCognitiveServicesAccountSkus。</span><span class="sxs-lookup"><span data-stu-id="368d1-235">Support Get-AzureRmCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="368d1-236">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="368d1-236">AzureRM.Compute</span></span>
* <span data-ttu-id="368d1-237">修复了 Get-AzureRmVM -ResourceGroupName <rg>，以在需要时返回超过 50 个结果</span><span class="sxs-lookup"><span data-stu-id="368d1-237">Fix Get-AzureRmVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="368d1-238">在 New-AzureRmVmss cmdlet 帮助中添加了“SimpleParameterSet”的示例。</span><span class="sxs-lookup"><span data-stu-id="368d1-238">Added an example of the 'SimpleParameterSet' to New-AzureRmVmss cmdlet help.</span></span>
* <span data-ttu-id="368d1-239">修复了 Azure 磁盘加密进度消息中的拼写错误</span><span class="sxs-lookup"><span data-stu-id="368d1-239">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="368d1-240">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="368d1-240">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="368d1-241">将 ADF .Net SDK 版本更新为 2.3.0。</span><span class="sxs-lookup"><span data-stu-id="368d1-241">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="368d1-242">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="368d1-242">AzureRM.Network</span></span>
* <span data-ttu-id="368d1-243">添加了 NetworkProfile 功能。</span><span class="sxs-lookup"><span data-stu-id="368d1-243">Added NetworkProfile functionality.</span></span> <span data-ttu-id="368d1-244">添加了新 cmdlet</span><span class="sxs-lookup"><span data-stu-id="368d1-244">new cmdlets added</span></span>
    - <span data-ttu-id="368d1-245">Get-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="368d1-245">Get-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="368d1-246">New-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="368d1-246">New-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="368d1-247">Remove-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="368d1-247">Remove-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="368d1-248">Set-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="368d1-248">Set-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="368d1-249">New-AzureRMContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="368d1-249">New-AzureRMContainerNicConfig</span></span>
    - <span data-ttu-id="368d1-250">New-AzureRmContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="368d1-250">New-AzureRmContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="368d1-251">在子网模型上添加了服务关联链接</span><span class="sxs-lookup"><span data-stu-id="368d1-251">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="368d1-252">添加了 cmdlet New-AzureRmVirtualNetworkTap、Get-AzureRmVirtualNetworkTap、Set-AzureRmVirtualNetworkTap、Remove-AzureRmVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="368d1-252">Added cmdlet New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap</span></span>
* <span data-ttu-id="368d1-253">添加了 cmdlet Set-AzureRmNEtworkInterfaceTapConfig、Get-AzureRmNEtworkInterfaceTapConfig、Remove-AzureRmNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="368d1-253">Added cmdlet Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="368d1-254">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="368d1-254">AzureRM.RedisCache</span></span>
* <span data-ttu-id="368d1-255">今后允许任何字符串作为 Size 参数。</span><span class="sxs-lookup"><span data-stu-id="368d1-255">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="368d1-256">在 PSArgumentCompleter 弹出窗口中添加了 P5</span><span class="sxs-lookup"><span data-stu-id="368d1-256">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="368d1-257">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="368d1-257">AzureRM.Resources</span></span>
* <span data-ttu-id="368d1-258">将缺少的 -Mode 参数添加到 Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="368d1-258">Add missing -Mode parameter to Set-AzureRmPolicyDefinition</span></span>
* <span data-ttu-id="368d1-259">对于使用包含用户的源的操作，修复了 Get-AzureRmProviderOperation commandlet bug</span><span class="sxs-lookup"><span data-stu-id="368d1-259">Fix Get-AzureRmProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="368d1-260">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="368d1-260">AzureRM.Sql</span></span>
* <span data-ttu-id="368d1-261">修复了某些备份 cmdlet 无法识别当前 azure 订阅的问题</span><span class="sxs-lookup"><span data-stu-id="368d1-261">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="368d1-262">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="368d1-262">AzureRM.Storage</span></span>
* <span data-ttu-id="368d1-263">支持获取特定位置的存储资源使用情况，并对于获取的全局存储资源使用情况已过时添加警告消息。</span><span class="sxs-lookup"><span data-stu-id="368d1-263">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="368d1-264">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="368d1-264">Get-AzureRmStorageUsage</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="368d1-265">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="368d1-265">AzureRM.Websites</span></span>
* <span data-ttu-id="368d1-266">新 Cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl - 获取容器持续部署 Webhook URL</span><span class="sxs-lookup"><span data-stu-id="368d1-266">New Cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="368d1-267">新 Cmdlet New-AzureRMWebAppContainerPSSession 和 Enter-WebAppContainerPSSession - 在 Windows 容器应用中启动 PowerShell 远程会话</span><span class="sxs-lookup"><span data-stu-id="368d1-267">New Cmdlets New-AzureRMWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="690---september-2018"></a><span data-ttu-id="368d1-268">6.9.0 - 2018 年 9 月</span><span class="sxs-lookup"><span data-stu-id="368d1-268">6.9.0 - September 2018</span></span>
#### <a name="general"></a><span data-ttu-id="368d1-269">常规</span><span class="sxs-lookup"><span data-stu-id="368d1-269">General</span></span>
* <span data-ttu-id="368d1-270">AzureRM.SignalR 已添加到 AzureRM 汇总模块</span><span class="sxs-lookup"><span data-stu-id="368d1-270">AzureRM.SignalR was added to the AzureRM rollup module</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="368d1-271">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="368d1-271">AzureRM.Profile</span></span>
* <span data-ttu-id="368d1-272">对存储常用代码进行了细微的更改</span><span class="sxs-lookup"><span data-stu-id="368d1-272">Minor changes to the storage common code</span></span>
* <span data-ttu-id="368d1-273">更新了帮助文件，使之包括完整参数类型。</span><span class="sxs-lookup"><span data-stu-id="368d1-273">Updated help files to include full parameter types.</span></span>
* <span data-ttu-id="368d1-274">已在 ServicePrincipalCertificateWithSubscriptionId 参数集中将 -ServicePrincipal 更改为非强制性项</span><span class="sxs-lookup"><span data-stu-id="368d1-274">Changed -ServicePrincipal to non-mandatory in the ServicePrincipalCertificateWithSubscriptionId parameter set</span></span> 

#### <a name="azurestorage"></a><span data-ttu-id="368d1-275">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="368d1-275">Azure.Storage</span></span>
* <span data-ttu-id="368d1-276">支持使用 OAuth 创建存储上下文。</span><span class="sxs-lookup"><span data-stu-id="368d1-276">Support create Storage Context with OAuth.</span></span> 
    - <span data-ttu-id="368d1-277">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="368d1-277">New-AzureStorageContext</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="368d1-278">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="368d1-278">AzureRM.Cdn</span></span>
* <span data-ttu-id="368d1-279">在 Cdn 定价 sku 中增加了 Standard_Microsoft。</span><span class="sxs-lookup"><span data-stu-id="368d1-279">Added Standard_Microsoft in Cdn pricing sku.</span></span> 

#### <a name="azurermcompute"></a><span data-ttu-id="368d1-280">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="368d1-280">AzureRM.Compute</span></span>
* <span data-ttu-id="368d1-281">将 Keyvault 和存储的依赖项移到了常用依赖项中</span><span class="sxs-lookup"><span data-stu-id="368d1-281">Move dependencies on Keyvault and Storage to the common dependencies</span></span>
* <span data-ttu-id="368d1-282">增加了对 AEM cmdlet 的支持，可以使用更多的虚拟机大小</span><span class="sxs-lookup"><span data-stu-id="368d1-282">Add support for more virutal machine sizes to AEM cmdlets</span></span>
* <span data-ttu-id="368d1-283">为 New-AzureRmVmssIpConfig 增加了 PublicIPPrefix 参数</span><span class="sxs-lookup"><span data-stu-id="368d1-283">Add PublicIPPrefix parameter to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="368d1-284">为 Invoke-AzureRmVMRunCommand cmdelt 增加了 ResourceId 参数</span><span class="sxs-lookup"><span data-stu-id="368d1-284">Add ResourceId parameter to Invoke-AzureRmVMRunCommand cmdelt</span></span>
* <span data-ttu-id="368d1-285">增加了 Invoke-AzureRmVmssVMRunCommand cmdlet</span><span class="sxs-lookup"><span data-stu-id="368d1-285">Add Invoke-AzureRmVmssVMRunCommand cmdlet</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="368d1-286">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="368d1-286">AzureRM.Dns</span></span>
* <span data-ttu-id="368d1-287">增加了在创建 dns 记录期间对别名记录的支持</span><span class="sxs-lookup"><span data-stu-id="368d1-287">Added support for alias record during dns record creation</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="368d1-288">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="368d1-288">AzureRM.Insights</span></span>
* <span data-ttu-id="368d1-289">修复了问题 #6833 和 #7102（诊断设置方面）</span><span class="sxs-lookup"><span data-stu-id="368d1-289">Fixed issues #6833 and #7102 (Diagnostic Settings area)</span></span>
    - <span data-ttu-id="368d1-290">在创建和列出/获取诊断设置期间出现的默认名称（即“service”）的问题</span><span class="sxs-lookup"><span data-stu-id="368d1-290">Issues with the default name, i.e. 'service', during creation and listing/getting of diagnostic settings</span></span>
    - <span data-ttu-id="368d1-291">通过类别创建诊断设置的问题</span><span class="sxs-lookup"><span data-stu-id="368d1-291">Issues creating diagnostic settings with categories</span></span>
* <span data-ttu-id="368d1-292">为指标时间粒度参数添加了弃用消息</span><span class="sxs-lookup"><span data-stu-id="368d1-292">Added deprecation message for metrics time grains parameters</span></span>
    - <span data-ttu-id="368d1-293">Timegrains 参数仍然会被接受（这是非重大变更），但在后端会被忽略，因为仅 PT1M 有效</span><span class="sxs-lookup"><span data-stu-id="368d1-293">Timegrains parameters are still being accepted (this is a non-breaking change,) but they are ignored in the backend since only PT1M is valid</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="368d1-294">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="368d1-294">AzureRM.Network</span></span>
* <span data-ttu-id="368d1-295">更改了 LoadBalancer cmdlet</span><span class="sxs-lookup"><span data-stu-id="368d1-295">Changes to LoadBalancer cmdlets</span></span>
  - <span data-ttu-id="368d1-296">LoadBalancerInboundNatPoolConfig：增加了 IdleTimeoutInMinutes、EnableFloatingIp 和 EnableTcpReset 参数</span><span class="sxs-lookup"><span data-stu-id="368d1-296">LoadBalancerInboundNatPoolConfig: added parameters IdleTimeoutInMinutes, EnableFloatingIp and EnableTcpReset</span></span>
  - <span data-ttu-id="368d1-297">LoadBalancerInboundNatRuleConfig：增加了 EnableTcpReset 参数</span><span class="sxs-lookup"><span data-stu-id="368d1-297">LoadBalancerInboundNatRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="368d1-298">LoadBalancerRuleConfig：增加了 EnableTcpReset 参数</span><span class="sxs-lookup"><span data-stu-id="368d1-298">LoadBalancerRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="368d1-299">LoadBalancerProbeConfig：增加了对参数 Protocol 的“Https”值的支持</span><span class="sxs-lookup"><span data-stu-id="368d1-299">LoadBalancerProbeConfig: added support for value "Https" for parameter Protocol</span></span>
* <span data-ttu-id="368d1-300">为新 LoadBalancer 的子资源 OutboundRule 增加了新命令</span><span class="sxs-lookup"><span data-stu-id="368d1-300">Added new commands for new LoadBalancer's subresource OutboundRule</span></span>
  - <span data-ttu-id="368d1-301">Add-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="368d1-301">Add-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="368d1-302">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="368d1-302">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="368d1-303">New-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="368d1-303">New-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="368d1-304">Set-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="368d1-304">Set-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="368d1-305">Remove-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="368d1-305">Remove-AzureRmLoadBalancerOutboundRuleConfig</span></span>
* <span data-ttu-id="368d1-306">为 PSNetworkInterface 增加了新的 HostedWorkloads 属性</span><span class="sxs-lookup"><span data-stu-id="368d1-306">Added new HostedWorkloads property for PSNetworkInterface</span></span>
* <span data-ttu-id="368d1-307">通过 ARM 为 Azure 防火墙功能增加了新的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="368d1-307">Added new cmdlets for feature: Azure Firewall via ARM</span></span>
  - <span data-ttu-id="368d1-308">增加了 Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="368d1-308">Added Get-AzureRmFirewall</span></span>
  - <span data-ttu-id="368d1-309">增加了 Set-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="368d1-309">Added Set-AzureRmFirewall</span></span>
  - <span data-ttu-id="368d1-310">增加了 New-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="368d1-310">Added New-AzureRmFirewall</span></span>
  - <span data-ttu-id="368d1-311">增加了 Remove-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="368d1-311">Added Remove-AzureRmFirewall</span></span>
  - <span data-ttu-id="368d1-312">增加了 New-AzureRmFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="368d1-312">Added New-AzureRmFirewallApplicationRuleCollection</span></span>
  - <span data-ttu-id="368d1-313">增加了 New-AzureRmFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="368d1-313">Added New-AzureRmFirewallApplicationRule</span></span>
  - <span data-ttu-id="368d1-314">增加了 New-AzureRmFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="368d1-314">Added New-AzureRmFirewallNatRuleCollection</span></span>
  - <span data-ttu-id="368d1-315">增加了 New-AzureRmFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="368d1-315">Added New-AzureRmFirewallNatRule</span></span>
  - <span data-ttu-id="368d1-316">增加了 New-AzureRmFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="368d1-316">Added New-AzureRmFirewallNetworkRuleCollection</span></span>
  - <span data-ttu-id="368d1-317">增加了 New-AzureRmFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="368d1-317">Added New-AzureRmFirewallNetworkRule</span></span>
* <span data-ttu-id="368d1-318">在应用程序网关中增加了对受信任根证书和自动缩放配置的支持</span><span class="sxs-lookup"><span data-stu-id="368d1-318">Added support for Trusted Root certificate and Autoscale configuration in Application Gateway</span></span>
  - <span data-ttu-id="368d1-319">增加了新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="368d1-319">New Cmdlets added:</span></span>
      - <span data-ttu-id="368d1-320">Add-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="368d1-320">Add-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="368d1-321">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="368d1-321">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="368d1-322">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="368d1-322">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="368d1-323">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="368d1-323">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="368d1-324">Set-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="368d1-324">Set-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="368d1-325">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="368d1-325">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="368d1-326">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="368d1-326">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="368d1-327">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="368d1-327">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="368d1-328">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="368d1-328">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
  - <span data-ttu-id="368d1-329">使用可选参数 -TrustedRootCertificate 更新了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="368d1-329">Cmdlets updated with optonal parameter -TrustedRootCertificate</span></span>
      - <span data-ttu-id="368d1-330">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="368d1-330">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="368d1-331">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="368d1-331">Set-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="368d1-332">New-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="368d1-332">New-AzureRmApplicationGatewayBackendHttpSetting</span></span>
      - <span data-ttu-id="368d1-333">Set-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="368d1-333">Set-AzureRmApplicationGatewayBackendHttpSetting</span></span>
  - <span data-ttu-id="368d1-334">使用可选参数 -AutoscaleConfiguration 更新了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="368d1-334">Cmdlets updated with optonal parameter -AutoscaleConfiguration</span></span>
      - <span data-ttu-id="368d1-335">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="368d1-335">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="368d1-336">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="368d1-336">Set-AzureRmApplicationGateway</span></span>
* <span data-ttu-id="368d1-337">为接口终结点增加了 cmdlet Get-AzureInterfaceEndpoint</span><span class="sxs-lookup"><span data-stu-id="368d1-337">Add cmdlet for Interface Endpoint Get-AzureInterfaceEndpoint</span></span>
* <span data-ttu-id="368d1-338">在子网中增加了对多个地址前缀的支持。</span><span class="sxs-lookup"><span data-stu-id="368d1-338">Added support for multiple address prefixes in a subnet.</span></span> <span data-ttu-id="368d1-339">更新了 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="368d1-339">Updated cmdlets:</span></span>
  - <span data-ttu-id="368d1-340">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="368d1-340">New-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="368d1-341">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="368d1-341">Set-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="368d1-342">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="368d1-342">Add-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="368d1-343">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="368d1-343">Get-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="368d1-344">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="368d1-344">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>
  - <span data-ttu-id="368d1-345">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="368d1-345">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="368d1-346">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="368d1-346">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="368d1-347">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="368d1-347">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="368d1-348">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="368d1-348">Add-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="368d1-349">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="368d1-349">New-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="368d1-350">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="368d1-350">Set-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="368d1-351">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="368d1-351">Add-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="368d1-352">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="368d1-352">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="368d1-353">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="368d1-353">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="368d1-354">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="368d1-354">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="368d1-355">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="368d1-355">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="368d1-356">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="368d1-356">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="368d1-357">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="368d1-357">New-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="368d1-358">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="368d1-358">New-AzureRmNetworkInterface</span></span>
* <span data-ttu-id="368d1-359">增加了用于子网委派的 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="368d1-359">Adding cmdlets for subnet delegation.</span></span>
  - <span data-ttu-id="368d1-360">New-AzureRmDelegation：创建一个可以添加到子网的新委派</span><span class="sxs-lookup"><span data-stu-id="368d1-360">New-AzureRmDelegation: Creates a new delegation, which can be added to a subnet</span></span>
  - <span data-ttu-id="368d1-361">Remove-AzureRmDelegation：获取一个子网，然后从该子网中删除提供的委派名称</span><span class="sxs-lookup"><span data-stu-id="368d1-361">Remove-AzureRmDelegation: Takes in a subnet and removes the provided delegation name from that subnet</span></span>
  - <span data-ttu-id="368d1-362">Add-AzureRmDelegation：获取一个子网，然后向该子网添加提供的服务名称作为委派</span><span class="sxs-lookup"><span data-stu-id="368d1-362">Add-AzureRmDelegation: Takes in a subnet and adds the provided service name as a delegation to that subnet</span></span>
  - <span data-ttu-id="368d1-363">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="368d1-363">Get-AzureRmDelegation</span></span>
  - <span data-ttu-id="368d1-364">Get-AzureRmAvailableServiceDelegations</span><span class="sxs-lookup"><span data-stu-id="368d1-364">Get-AzureRmAvailableServiceDelegations</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="368d1-365">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="368d1-365">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="368d1-366">支持托管磁盘</span><span class="sxs-lookup"><span data-stu-id="368d1-366">Support for managed Managed disk</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="368d1-367">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="368d1-367">AzureRM.RedisCache</span></span>
* <span data-ttu-id="368d1-368">更新了 Insights 依赖项。</span><span class="sxs-lookup"><span data-stu-id="368d1-368">Updated Insights dependency.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="368d1-369">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="368d1-369">AzureRM.Resources</span></span>
* <span data-ttu-id="368d1-370">使用新参数 RollbackAction 更新了 New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="368d1-370">Update New-AzureRmResourceGroupDeployment with new parameter RollbackAction</span></span>
    - <span data-ttu-id="368d1-371">使用新参数增加了对 OnErrorDeployment 的支持。</span><span class="sxs-lookup"><span data-stu-id="368d1-371">Add support for OnErrorDeployment with the new parameter.</span></span>
* <span data-ttu-id="368d1-372">在策略分配方面支持托管标识。</span><span class="sxs-lookup"><span data-stu-id="368d1-372">Support managed identity on policy assignments.</span></span>
* <span data-ttu-id="368d1-373">使用“New-AzureRmPolicyAssignment”来分配策略时，不再需要带默认值的参数</span><span class="sxs-lookup"><span data-stu-id="368d1-373">Parameters with default values are no longer requred when assigning a policy with 'New-AzureRmPolicyAssignment'</span></span>
* <span data-ttu-id="368d1-374">增加了新的 cmdlet Get-AzureRmPolicyAlias，用于检索策略别名</span><span class="sxs-lookup"><span data-stu-id="368d1-374">Add new cmdlet Get-AzureRmPolicyAlias for retrieving policy aliases</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="368d1-375">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="368d1-375">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="368d1-376">修复了问题 #7161</span><span class="sxs-lookup"><span data-stu-id="368d1-376">Fixed issue #7161</span></span>

#### <a name="azurermsignalr"></a><span data-ttu-id="368d1-377">AzureRM.SignalR</span><span class="sxs-lookup"><span data-stu-id="368d1-377">AzureRM.SignalR</span></span>
* <span data-ttu-id="368d1-378">将 SKU 名称更新为 Free_F1 和 Standard_S1</span><span class="sxs-lookup"><span data-stu-id="368d1-378">Update SKU names to Free_F1 and Standard_S1</span></span>
* <span data-ttu-id="368d1-379">为 PSSignalRResource 对象增加了版本字段，为 PSSignalRKeys 对象增加了字符串。</span><span class="sxs-lookup"><span data-stu-id="368d1-379">Add version field to the PSSignalRResource object and connection string to the PSSignalRKeys object.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="368d1-380">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="368d1-380">AzureRM.Storage</span></span>
* <span data-ttu-id="368d1-381">在 AzureRm.Storage 中支持不可变性策略</span><span class="sxs-lookup"><span data-stu-id="368d1-381">Support Immutability Policy in AzureRm.Storage</span></span> 
    - <span data-ttu-id="368d1-382">Remove-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="368d1-382">Remove-AzureRmStorageAccountNetworkRule</span></span>
    - <span data-ttu-id="368d1-383">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="368d1-383">Get-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="368d1-384">Update-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="368d1-384">Update-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="368d1-385">New-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="368d1-385">New-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="368d1-386">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="368d1-386">Remove-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="368d1-387">Add-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="368d1-387">Add-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="368d1-388">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="368d1-388">Remove-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="368d1-389">Set-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="368d1-389">Set-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="368d1-390">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="368d1-390">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="368d1-391">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="368d1-391">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="368d1-392">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="368d1-392">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="368d1-393">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="368d1-393">AzureRM.Websites</span></span>
* <span data-ttu-id="368d1-394">增加了两个新的 cmdlet：Get-AzureRmDeletedWebApp 和 Restore-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="368d1-394">Added two new cmdlets: Get-AzureRmDeletedWebApp and Restore-AzureRmDeletedWebApp</span></span>
* <span data-ttu-id="368d1-395">增加了 New-AzureRmAppServicePlan -HyperV 开关，用于通过 Windows 容器创建应用服务计划</span><span class="sxs-lookup"><span data-stu-id="368d1-395">New-AzureRmAppServicePlan -HyperV switch is added for create app service plan with windows container</span></span>
* <span data-ttu-id="368d1-396">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - 增加了新参数 (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment)，用于创建和管理 Windows 容器应用</span><span class="sxs-lookup"><span data-stu-id="368d1-396">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - New parameters (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) added for creating and managing windows container app</span></span>

## <a name="681---august-2018"></a><span data-ttu-id="368d1-397">6.8.1 - 2018 年 8 月</span><span class="sxs-lookup"><span data-stu-id="368d1-397">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="368d1-398">常规</span><span class="sxs-lookup"><span data-stu-id="368d1-398">General</span></span>
* <span data-ttu-id="368d1-399">解决了未设置默认资源组的问题。</span><span class="sxs-lookup"><span data-stu-id="368d1-399">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="368d1-400">更新了公共运行时程序集</span><span class="sxs-lookup"><span data-stu-id="368d1-400">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="368d1-401">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="368d1-401">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="368d1-402">解决了未设置默认资源组的问题。</span><span class="sxs-lookup"><span data-stu-id="368d1-402">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="368d1-403">修复了问题 https://github.com/Azure/azure-powershell/issues/6603</span><span class="sxs-lookup"><span data-stu-id="368d1-403">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="368d1-404">Import-AzureRmApiManagementApi 和 \*-AzureRmApiManagementCertificate cmdlet 现在处理相对路径</span><span class="sxs-lookup"><span data-stu-id="368d1-404">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="368d1-405">修复了问题 https://github.com/Azure/azure-powershell/issues/6879</span><span class="sxs-lookup"><span data-stu-id="368d1-405">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="368d1-406">CertificateInformation 是使 Set-AzureRmApiManagement cmdlet 可以正常工作的可设置属性。</span><span class="sxs-lookup"><span data-stu-id="368d1-406">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="368d1-407">通过升级到 4.0.4-preview nuget 进行了修复</span><span class="sxs-lookup"><span data-stu-id="368d1-407">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="368d1-408">修复了问题 https://github.com/Azure/azure-powershell/issues/6853</span><span class="sxs-lookup"><span data-stu-id="368d1-408">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="368d1-409">针对按产品名称进行的搜索修复了 Odata 筛选器</span><span class="sxs-lookup"><span data-stu-id="368d1-409">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="368d1-410">修复了问题 https://github.com/Azure/azure-powershell/issues/6814</span><span class="sxs-lookup"><span data-stu-id="368d1-410">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="368d1-411">针对按 API 名称进行的搜索修复了 Odata 筛选器</span><span class="sxs-lookup"><span data-stu-id="368d1-411">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="368d1-412">添加了对 AzureMonitor 记录器的支持</span><span class="sxs-lookup"><span data-stu-id="368d1-412">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="368d1-413">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="368d1-413">AzureRM.Compute</span></span>
* <span data-ttu-id="368d1-414">解决了错误输出中缺少目标的问题。</span><span class="sxs-lookup"><span data-stu-id="368d1-414">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="368d1-415">解决了带有托管磁盘的 VM 的存储帐户类型问题</span><span class="sxs-lookup"><span data-stu-id="368d1-415">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="368d1-416">解决了未设置默认资源组的问题。</span><span class="sxs-lookup"><span data-stu-id="368d1-416">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="368d1-417">解决了在其他环境（例如 Azure 中国）中使用 AEM 扩展 cmdlet 的问题</span><span class="sxs-lookup"><span data-stu-id="368d1-417">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="368d1-418">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="368d1-418">AzureRM.Network</span></span>
* <span data-ttu-id="368d1-419">将默认 cmdlet 输出表示形式更改为表视图</span><span class="sxs-lookup"><span data-stu-id="368d1-419">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="368d1-420">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="368d1-420">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="368d1-421">修复了在尝试扩展停用的容量时 Update-AzureRmPowerBIEmbeddedCapacity 中出现的故障</span><span class="sxs-lookup"><span data-stu-id="368d1-421">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="368d1-422">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="368d1-422">AzureRM.Resources</span></span>
* <span data-ttu-id="368d1-423">解决了从市场创建托管应用程序的问题。</span><span class="sxs-lookup"><span data-stu-id="368d1-423">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="368d1-424">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="368d1-424">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="368d1-425">修复的问题</span><span class="sxs-lookup"><span data-stu-id="368d1-425">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="368d1-426">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="368d1-426">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="368d1-427">添加了对 MultiValue 路由方法的支持</span><span class="sxs-lookup"><span data-stu-id="368d1-427">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="368d1-428">MultiValue 路由的新参数“MaxReturn”</span><span class="sxs-lookup"><span data-stu-id="368d1-428">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="368d1-429">添加了对 Subnet 路由方法的支持</span><span class="sxs-lookup"><span data-stu-id="368d1-429">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="368d1-430">对终结点中的 IP 地址范围（子网）的支持</span><span class="sxs-lookup"><span data-stu-id="368d1-430">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="368d1-431">添加了对配置文件中的自定义标头的支持</span><span class="sxs-lookup"><span data-stu-id="368d1-431">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="368d1-432">添加了对配置文件中的预期状态代码范围的支持</span><span class="sxs-lookup"><span data-stu-id="368d1-432">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="368d1-433">添加了对终结点中的自定义标头的支持</span><span class="sxs-lookup"><span data-stu-id="368d1-433">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="368d1-434">6.8.0 - 2018 年 8 月</span><span class="sxs-lookup"><span data-stu-id="368d1-434">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="368d1-435">常规</span><span class="sxs-lookup"><span data-stu-id="368d1-435">General</span></span>
* <span data-ttu-id="368d1-436">解决了未设置默认资源组的问题。</span><span class="sxs-lookup"><span data-stu-id="368d1-436">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="368d1-437">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="368d1-437">AzureRM.Profile</span></span>
* <span data-ttu-id="368d1-438">为在执行 Connect-AzureRmAccount 期间返回的令牌添加了“过期”属性</span><span class="sxs-lookup"><span data-stu-id="368d1-438">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="368d1-439">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="368d1-439">AzureRM.Compute</span></span>
* <span data-ttu-id="368d1-440">解决了错误输出中缺少目标的问题。</span><span class="sxs-lookup"><span data-stu-id="368d1-440">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="368d1-441">解决了带有托管磁盘的 VM 的存储帐户类型问题</span><span class="sxs-lookup"><span data-stu-id="368d1-441">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="368d1-442">解决了在其他环境（例如 Azure 中国）中使用 AEM 扩展 cmdlet 的问题</span><span class="sxs-lookup"><span data-stu-id="368d1-442">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="368d1-443">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="368d1-443">AzureRM.IotHub</span></span>
* <span data-ttu-id="368d1-444">修复了 New-AzureRmIotHubExportDevices 和 New-AzureRmIotHubImportDevices的示例</span><span class="sxs-lookup"><span data-stu-id="368d1-444">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="368d1-445">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="368d1-445">AzureRM.Network</span></span>
* <span data-ttu-id="368d1-446">将默认模型表示形式更改为表视图</span><span class="sxs-lookup"><span data-stu-id="368d1-446">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="368d1-447">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="368d1-447">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="368d1-448">修复了在尝试扩展停用的容量时 Update-AzureRmPowerBIEmbeddedCapacity 中出现的故障</span><span class="sxs-lookup"><span data-stu-id="368d1-448">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="368d1-449">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="368d1-449">AzureRM.Resources</span></span>
* <span data-ttu-id="368d1-450">解决了从市场创建托管应用程序的问题。</span><span class="sxs-lookup"><span data-stu-id="368d1-450">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="368d1-451">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="368d1-451">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="368d1-452">解决了以下问题</span><span class="sxs-lookup"><span data-stu-id="368d1-452">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="368d1-453">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="368d1-453">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="368d1-454">对 MultiValue 路由方法的支持</span><span class="sxs-lookup"><span data-stu-id="368d1-454">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="368d1-455">MultiValue 路由的新参数“MaxReturn”</span><span class="sxs-lookup"><span data-stu-id="368d1-455">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="368d1-456">对 Subnet 路由方法的支持</span><span class="sxs-lookup"><span data-stu-id="368d1-456">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="368d1-457">对终结点中的 IP 地址范围（子网）的支持</span><span class="sxs-lookup"><span data-stu-id="368d1-457">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="368d1-458">对配置文件中的自定义标头的支持</span><span class="sxs-lookup"><span data-stu-id="368d1-458">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="368d1-459">对配置文件中的预期状态代码范围的支持</span><span class="sxs-lookup"><span data-stu-id="368d1-459">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="368d1-460">对终结点中的自定义标头的支持</span><span class="sxs-lookup"><span data-stu-id="368d1-460">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="368d1-461">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="368d1-461">AzureRM.Websites</span></span>
* <span data-ttu-id="368d1-462">解决了错误地设置默认资源组的问题。</span><span class="sxs-lookup"><span data-stu-id="368d1-462">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="368d1-463">6.7.0 - 2018 年 8 月</span><span class="sxs-lookup"><span data-stu-id="368d1-463">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="368d1-464">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="368d1-464">AzureRM.Profile</span></span>
* <span data-ttu-id="368d1-465">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="368d1-465">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="368d1-466">向默认的上下文名称添加用户 ID，避免上下文冲突</span><span class="sxs-lookup"><span data-stu-id="368d1-466">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="368d1-467">修复了 Clear-AzureRmContext 在选择上下文 #6398 时出现的问题</span><span class="sxs-lookup"><span data-stu-id="368d1-467">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="368d1-468">允许将租户域传递给“Connect-AzureRmAccount”的“-TenantId”参数</span><span class="sxs-lookup"><span data-stu-id="368d1-468">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="368d1-469">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="368d1-469">Azure.Storage</span></span>
* <span data-ttu-id="368d1-470">去除了 Azure 文件共享配额的 5TB 限制</span><span class="sxs-lookup"><span data-stu-id="368d1-470">Remove the 5TB limitation for Azure File Share quota</span></span>
* <span data-ttu-id="368d1-471">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="368d1-471">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="368d1-472">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="368d1-472">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="368d1-473">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="368d1-473">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="368d1-474">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="368d1-474">Azure.AnalysisServices</span></span>
* <span data-ttu-id="368d1-475">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="368d1-475">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="368d1-476">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="368d1-476">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="368d1-477">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="368d1-477">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="368d1-478">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="368d1-478">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="368d1-479">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="368d1-479">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="368d1-480">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="368d1-480">AzureRM.Automation</span></span>
* <span data-ttu-id="368d1-481">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="368d1-481">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="368d1-482">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="368d1-482">AzureRM.Backup</span></span>
* <span data-ttu-id="368d1-483">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="368d1-483">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="368d1-484">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="368d1-484">AzureRM.Batch</span></span>
* <span data-ttu-id="368d1-485">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="368d1-485">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="368d1-486">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="368d1-486">AzureRM.Billing</span></span>
* <span data-ttu-id="368d1-487">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="368d1-487">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="368d1-488">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="368d1-488">AzureRM.Cdn</span></span>
* <span data-ttu-id="368d1-489">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="368d1-489">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="368d1-490">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="368d1-490">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="368d1-491">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="368d1-491">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="368d1-492">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="368d1-492">AzureRM.Compute</span></span>
* <span data-ttu-id="368d1-493">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="368d1-493">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="368d1-494">为 New-AzureRmVmssConfig 增加了 EvictionPolicy 参数</span><span class="sxs-lookup"><span data-stu-id="368d1-494">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="368d1-495">在 New-AzureRmVm 的 DiskFileParameterSet 中使用默认位置（如果未指定 Location）</span><span class="sxs-lookup"><span data-stu-id="368d1-495">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="368d1-496">修复了 Save-AzureRmVMImage 中的参数说明</span><span class="sxs-lookup"><span data-stu-id="368d1-496">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="368d1-497">修复了某些单次传递相关方案的 Get-AzureRmVMDiskEncryptionStatus cmdlet</span><span class="sxs-lookup"><span data-stu-id="368d1-497">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="368d1-498">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="368d1-498">AzureRM.Consumption</span></span>
* <span data-ttu-id="368d1-499">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="368d1-499">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="368d1-500">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="368d1-500">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="368d1-501">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="368d1-501">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="368d1-502">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="368d1-502">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="368d1-503">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="368d1-503">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="368d1-504">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="368d1-504">AzureRM.DataFactories</span></span>
* <span data-ttu-id="368d1-505">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="368d1-505">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="368d1-506">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="368d1-506">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="368d1-507">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="368d1-507">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="368d1-508">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="368d1-508">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="368d1-509">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="368d1-509">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="368d1-510">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="368d1-510">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="368d1-511">修复了从 PowerShell 命令行设置 DebugPreference 时的调试问题</span><span class="sxs-lookup"><span data-stu-id="368d1-511">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="368d1-512">更新了 Set-AzureRmDataLakeStoreItemAcl 的示例</span><span class="sxs-lookup"><span data-stu-id="368d1-512">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="368d1-513">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="368d1-513">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="368d1-514">更新了 Set-AzureRmDataLakeStoreItemAclEntry 的示例</span><span class="sxs-lookup"><span data-stu-id="368d1-514">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="368d1-515">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="368d1-515">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="368d1-516">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="368d1-516">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="368d1-517">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="368d1-517">AzureRM.Dns</span></span>
* <span data-ttu-id="368d1-518">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="368d1-518">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="368d1-519">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="368d1-519">AzureRM.EventGrid</span></span>
* <span data-ttu-id="368d1-520">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="368d1-520">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="368d1-521">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="368d1-521">AzureRM.EventHub</span></span>
* <span data-ttu-id="368d1-522">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="368d1-522">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="368d1-523">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="368d1-523">AzureRM.HDInsight</span></span>
* <span data-ttu-id="368d1-524">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="368d1-524">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="368d1-525">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="368d1-525">AzureRM.Insights</span></span>
* <span data-ttu-id="368d1-526">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="368d1-526">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="368d1-527">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="368d1-527">AzureRM.IotHub</span></span>
* <span data-ttu-id="368d1-528">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="368d1-528">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="368d1-529">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="368d1-529">AzureRM.KeyVault</span></span>
* <span data-ttu-id="368d1-530">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="368d1-530">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="368d1-531">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="368d1-531">AzureRM.LogicApp</span></span>
* <span data-ttu-id="368d1-532">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="368d1-532">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="368d1-533">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="368d1-533">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="368d1-534">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="368d1-534">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="368d1-535">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="368d1-535">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="368d1-536">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="368d1-536">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="368d1-537">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="368d1-537">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="368d1-538">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="368d1-538">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="368d1-539">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="368d1-539">AzureRM.Media</span></span>
* <span data-ttu-id="368d1-540">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="368d1-540">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="368d1-541">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="368d1-541">AzureRM.Network</span></span>
* <span data-ttu-id="368d1-542">增加了 Set-AzureRmLocalNetworkGateway 的示例</span><span class="sxs-lookup"><span data-stu-id="368d1-542">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="368d1-543">增加了 Add-AzureRmVirtualNetworkGatewayIpConfig、Get-AzureRmVirtualNetworkGatewayConnectionSharedKey 和 New-AzureRmVirtualNetworkGatewayConnection 的示例和说明</span><span class="sxs-lookup"><span data-stu-id="368d1-543">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="368d1-544">增加了 Remove-AzureRmVirtualNetworkGatewayIpConfig 和 Reset-AzureRmVirtualNetworkGateway 的示例</span><span class="sxs-lookup"><span data-stu-id="368d1-544">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="368d1-545">增加了 Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey 的示例</span><span class="sxs-lookup"><span data-stu-id="368d1-545">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="368d1-546">增加了 Set-AzureRmVirtualNetworkGatewayConnectionSharedKey 的示例</span><span class="sxs-lookup"><span data-stu-id="368d1-546">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="368d1-547">增加了 Set-AzureRmVirtualNetworkGatewayConnection 的示例</span><span class="sxs-lookup"><span data-stu-id="368d1-547">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="368d1-548">使用最新的代码生成器重新生成了 ApplicationSecurityGroup、RouteTable 和 Usage 的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="368d1-548">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="368d1-549">阐明了在尝试获取的子网不存在时 Get-AzureRmVirtualNetworkSubnetConfig 的错误消息</span><span class="sxs-lookup"><span data-stu-id="368d1-549">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="368d1-550">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="368d1-550">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="368d1-551">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="368d1-551">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="368d1-552">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="368d1-552">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="368d1-553">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="368d1-553">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="368d1-554">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="368d1-554">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="368d1-555">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="368d1-555">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="368d1-556">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="368d1-556">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="368d1-557">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="368d1-557">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="368d1-558">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="368d1-558">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="368d1-559">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="368d1-559">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="368d1-560">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="368d1-560">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="368d1-561">为 Get-AzureRmRecoveryServicesBackItem cmdlet 增加了策略筛选器。</span><span class="sxs-lookup"><span data-stu-id="368d1-561">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="368d1-562">此命令返回受给定策略 ID 保护的备份项的列表。</span><span class="sxs-lookup"><span data-stu-id="368d1-562">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="368d1-563">已将 Microsoft.Azure.Management.RecoveryServices.Backup 更新到 3.0.0-preview 版本。</span><span class="sxs-lookup"><span data-stu-id="368d1-563">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="368d1-564">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="368d1-564">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="368d1-565">为 Restore-AzureRmRecoveryServicesBackupItem 增加了 TargetResourceGroupName 参数。</span><span class="sxs-lookup"><span data-stu-id="368d1-565">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="368d1-566">托管磁盘还原到的资源组。</span><span class="sxs-lookup"><span data-stu-id="368d1-566">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="368d1-567">适用于包含托管磁盘的 VM 的备份。</span><span class="sxs-lookup"><span data-stu-id="368d1-567">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="368d1-568">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="368d1-568">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="368d1-569">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="368d1-569">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="368d1-570">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="368d1-570">AzureRM.RedisCache</span></span>
* <span data-ttu-id="368d1-571">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="368d1-571">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="368d1-572">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="368d1-572">AzureRM.Relay</span></span>
* <span data-ttu-id="368d1-573">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="368d1-573">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="368d1-574">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="368d1-574">AzureRM.Resources</span></span>
* <span data-ttu-id="368d1-575">支持在订阅范围部署模板。</span><span class="sxs-lookup"><span data-stu-id="368d1-575">Support template deployment at subscription scope.</span></span> <span data-ttu-id="368d1-576">增加了新 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="368d1-576">Add new Cmdlets:</span></span>
    - <span data-ttu-id="368d1-577">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="368d1-577">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="368d1-578">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="368d1-578">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="368d1-579">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="368d1-579">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="368d1-580">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="368d1-580">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="368d1-581">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="368d1-581">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="368d1-582">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="368d1-582">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="368d1-583">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="368d1-583">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="368d1-584">修复了在将上下文传递给 Set-AzureRmResource 时引发错误的问题</span><span class="sxs-lookup"><span data-stu-id="368d1-584">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="368d1-585">修复了 New-AzureRmResourceGroupDeployment 中的示例</span><span class="sxs-lookup"><span data-stu-id="368d1-585">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="368d1-586">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="368d1-586">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="368d1-587">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="368d1-587">AzureRM.Scheduler</span></span>
* <span data-ttu-id="368d1-588">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="368d1-588">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="368d1-589">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="368d1-589">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="368d1-590">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="368d1-590">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="368d1-591">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="368d1-591">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="368d1-592">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="368d1-592">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="368d1-593">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="368d1-593">AzureRM.Sql</span></span>
* <span data-ttu-id="368d1-594">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="368d1-594">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="368d1-595">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="368d1-595">AzureRM.Storage</span></span>
* <span data-ttu-id="368d1-596">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="368d1-596">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="368d1-597">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="368d1-597">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="368d1-598">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="368d1-598">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="368d1-599">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="368d1-599">AzureRM.Tags</span></span>
* <span data-ttu-id="368d1-600">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="368d1-600">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="368d1-601">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="368d1-601">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="368d1-602">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="368d1-602">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="368d1-603">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="368d1-603">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="368d1-604">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="368d1-604">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="368d1-605">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="368d1-605">AzureRM.Websites</span></span>
* <span data-ttu-id="368d1-606">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="368d1-606">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="368d1-607">6.6.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="368d1-607">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="368d1-608">常规</span><span class="sxs-lookup"><span data-stu-id="368d1-608">General</span></span>
* <span data-ttu-id="368d1-609">更新了所有帮助文件，以包括完整参数类型和正确的输入/输出类型。</span><span class="sxs-lookup"><span data-stu-id="368d1-609">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="368d1-610">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="368d1-610">AzureRM.Profile</span></span>
* <span data-ttu-id="368d1-611">更新了 Common.Strategy 库，以便能够验证资源的当前配置是否与目标资源兼容。</span><span class="sxs-lookup"><span data-stu-id="368d1-611">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="368d1-612">在 Common.Storage 中添加了 ps1xml 类型</span><span class="sxs-lookup"><span data-stu-id="368d1-612">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="368d1-613">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="368d1-613">Azure.Storage</span></span>
* <span data-ttu-id="368d1-614">增加了从 DefaultProfile 获取存储上下文的支持</span><span class="sxs-lookup"><span data-stu-id="368d1-614">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="368d1-615">为 cmdlet 输出类型属性增加了 Ps1XmlAttribute。</span><span class="sxs-lookup"><span data-stu-id="368d1-615">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="368d1-616">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="368d1-616">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="368d1-617">修复了问题 https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="368d1-617">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="368d1-618">修复了 Automapper 中将 PsApiManagementApi 转换为 ApiContract 的 bug</span><span class="sxs-lookup"><span data-stu-id="368d1-618">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="368d1-619">修复了问题 https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="368d1-619">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="368d1-620">修复了 File.Save 中没有使用编码类型重载的 bug</span><span class="sxs-lookup"><span data-stu-id="368d1-620">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="368d1-621">修复了问题 https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="368d1-621">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="368d1-622">升级到了 4.0.3 Nuget版本，该版本修复了 apiId 上的模式异常</span><span class="sxs-lookup"><span data-stu-id="368d1-622">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="368d1-623">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="368d1-623">AzureRM.Compute</span></span>
* <span data-ttu-id="368d1-624">修复因使用 PremiumLRS 存储帐户类型重命名而在 New-AzureRmVm 中使用 DiskFileParameterSet 创建 VM 失败的问题。</span><span class="sxs-lookup"><span data-stu-id="368d1-624">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="368d1-625">修复 Invoke-AzureRmVMRunCommand cmdlet</span><span class="sxs-lookup"><span data-stu-id="368d1-625">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="368d1-626">更新 Get-AzureRmAvailabilitySet 以启用列出订阅中的所有可用性集。</span><span class="sxs-lookup"><span data-stu-id="368d1-626">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="368d1-627">（ResouceGroupName 参数现在是可选的。）</span><span class="sxs-lookup"><span data-stu-id="368d1-627">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="368d1-628">更新“New-AzureRmVm”的 SimpleParameterSet 以在符合条件的 VM 上启用加速网络。</span><span class="sxs-lookup"><span data-stu-id="368d1-628">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="368d1-629">将 New-AzureRmVmss 简单参数集更新为在用户指定的 LB 已存在时创建 vmss 失败。</span><span class="sxs-lookup"><span data-stu-id="368d1-629">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="368d1-630">更新 New-AzureRmDisk 的示例</span><span class="sxs-lookup"><span data-stu-id="368d1-630">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="368d1-631">添加“New-AzureRmVM”的示例</span><span class="sxs-lookup"><span data-stu-id="368d1-631">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="368d1-632">更新 Set-AzureRmVMOSDisk 的说明</span><span class="sxs-lookup"><span data-stu-id="368d1-632">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="368d1-633">更新 Set-AzureRmVMBginfoExtension 的示例 1 以更正拼写和前缀。</span><span class="sxs-lookup"><span data-stu-id="368d1-633">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="368d1-634">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="368d1-634">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="368d1-635">将 ADF .Net SDK 版本更新为 1.1.0。</span><span class="sxs-lookup"><span data-stu-id="368d1-635">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="368d1-636">支持跨数据工厂的自承载集成运行时共享。</span><span class="sxs-lookup"><span data-stu-id="368d1-636">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="368d1-637">将新参数 -SharedIntegrationRuntimeResourceId 添加到 Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet。</span><span class="sxs-lookup"><span data-stu-id="368d1-637">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="368d1-638">将新的可选参数 -LinkedDataFactoryName 添加到 Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet。</span><span class="sxs-lookup"><span data-stu-id="368d1-638">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="368d1-639">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="368d1-639">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="368d1-640">将数据平面 SDK (Microsoft.Azure.DataLake.Store) 版本更新为 1.1.9</span><span class="sxs-lookup"><span data-stu-id="368d1-640">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="368d1-641">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="368d1-641">AzureRM.EventHub</span></span>
* <span data-ttu-id="368d1-642">在删除 cmdlet 中更新了 InputObject 和 ResourceId 的管道</span><span class="sxs-lookup"><span data-stu-id="368d1-642">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="368d1-643">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="368d1-643">AzureRM.Insights</span></span>
* <span data-ttu-id="368d1-644">修复了帮助文件中 OutputType 的格式问题</span><span class="sxs-lookup"><span data-stu-id="368d1-644">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="368d1-645">使用 Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span><span class="sxs-lookup"><span data-stu-id="368d1-645">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="368d1-646">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="368d1-646">AzureRM.KeyVault</span></span>
* <span data-ttu-id="368d1-647">修复了 Set-AzureRmKeyVaultAccessPolicy 中的管道问题</span><span class="sxs-lookup"><span data-stu-id="368d1-647">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="368d1-648">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="368d1-648">AzureRM.Network</span></span>
* <span data-ttu-id="368d1-649">添加了 LoadBalancerInboundNatPoolConfig cmdlet 的示例。</span><span class="sxs-lookup"><span data-stu-id="368d1-649">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="368d1-650">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="368d1-650">AzureRM.Resources</span></span>
* <span data-ttu-id="368d1-651">修复了为“Get-AzureRmResource”同时提供标记名称和值时出现的问题</span><span class="sxs-lookup"><span data-stu-id="368d1-651">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="368d1-652">使用“Set-AzureRmResource”修复管道方案</span><span class="sxs-lookup"><span data-stu-id="368d1-652">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="368d1-653">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="368d1-653">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="368d1-654">在删除 cmdlet 中更新了 InputObject 和 ResourceId 的管道</span><span class="sxs-lookup"><span data-stu-id="368d1-654">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="368d1-655">修复了几个问题</span><span class="sxs-lookup"><span data-stu-id="368d1-655">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="368d1-656">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="368d1-656">AzureRM.Sql</span></span>
* <span data-ttu-id="368d1-657">使用以下 cmdlet 添加服务器高级威胁防护支持：</span><span class="sxs-lookup"><span data-stu-id="368d1-657">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="368d1-658">Enable-AzureRmSqlServerAdvancedThreatProtection；Disable-AzureRmSqlServerAdvancedThreatProtection；Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="368d1-658">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="368d1-659">使用以下 cmdlet 添加漏洞评估支持：</span><span class="sxs-lookup"><span data-stu-id="368d1-659">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="368d1-660">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings；Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings；Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="368d1-660">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="368d1-661">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline；Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline；Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="368d1-661">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="368d1-662">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan；Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord；Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="368d1-662">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="368d1-663">修复了 Remove-AzureRmSqlServerFirewallRule 中的示例</span><span class="sxs-lookup"><span data-stu-id="368d1-663">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="368d1-664">修复了 Get-AzureSqlSyncGroupLog 中非美国基础文化的日期时间处理错误</span><span class="sxs-lookup"><span data-stu-id="368d1-664">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="368d1-665">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="368d1-665">AzureRM.Storage</span></span>
* <span data-ttu-id="368d1-666">将 Ps1XmlAttribute 添加到 cmdlet 输出类型属性</span><span class="sxs-lookup"><span data-stu-id="368d1-666">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="368d1-667">在表视图中显示 StorageAccount cmdlet 输出</span><span class="sxs-lookup"><span data-stu-id="368d1-667">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="368d1-668">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="368d1-668">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="368d1-669">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="368d1-669">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="368d1-670">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="368d1-670">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="368d1-671">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="368d1-671">AzureRM.Tags</span></span>
* <span data-ttu-id="368d1-672">从 Tag cmdlet 帮助中删除不正确的语句</span><span class="sxs-lookup"><span data-stu-id="368d1-672">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="368d1-673">6.5.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="368d1-673">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="368d1-674">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="368d1-674">AzureRM.Profile</span></span>
* <span data-ttu-id="368d1-675">更新了“Get-AzureRmContextAutosaveSetting”的帮助</span><span class="sxs-lookup"><span data-stu-id="368d1-675">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="368d1-676">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="368d1-676">Azure.Storage</span></span>
* <span data-ttu-id="368d1-677">支持使用只写 Sas 令牌上传 Blob 或文件</span><span class="sxs-lookup"><span data-stu-id="368d1-677">Support Upload Blob or File with write only Sas token</span></span>
* <span data-ttu-id="368d1-678">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="368d1-678">Set-AzureStorageBlobContent</span></span>
* <span data-ttu-id="368d1-679">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="368d1-679">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="368d1-680">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="368d1-680">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="368d1-681">将所需属性 ResourceGroupName 添加到 AS。</span><span class="sxs-lookup"><span data-stu-id="368d1-681">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="368d1-682">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="368d1-682">AzureRM.Automation</span></span>
* <span data-ttu-id="368d1-683">更新帮助并添加“New-AzureRMAutomationSchedule”的示例</span><span class="sxs-lookup"><span data-stu-id="368d1-683">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="368d1-684">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="368d1-684">AzureRM.Compute</span></span>
* <span data-ttu-id="368d1-685">将 -Tag 参数添加到 Update/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="368d1-685">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="368d1-686">添加“Add-AzureRmVmssExtension”的示例</span><span class="sxs-lookup"><span data-stu-id="368d1-686">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="368d1-687">添加“Remove-AzureRmVmssExtension”的示例</span><span class="sxs-lookup"><span data-stu-id="368d1-687">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="368d1-688">更新“Set-AzureRmVMAccessExtension”的帮助</span><span class="sxs-lookup"><span data-stu-id="368d1-688">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="368d1-689">更新 New-AzureRmVmss 的 SimpleParameterSet，以默认情况下将 SinglePlacementGroup 设置为false，并添加开关参数“SinglePlacementGroup”，使用户能够在单个放置组中创建 VMSS。</span><span class="sxs-lookup"><span data-stu-id="368d1-689">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="368d1-690">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="368d1-690">AzureRM.EventHub</span></span>
* <span data-ttu-id="368d1-691">向 PSEventHubDRConfigurationAttributes 类添加了一个只读属性“PendingReplicationOperationsCount”，该属性在复制过程中为挂起的复制操作计数</span><span class="sxs-lookup"><span data-stu-id="368d1-691">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="368d1-692">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="368d1-692">AzureRM.KeyVault</span></span>
* <span data-ttu-id="368d1-693">更新了 Set-AzureRmKeyVaultAccessPolicy 的错误消息</span><span class="sxs-lookup"><span data-stu-id="368d1-693">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="368d1-694">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="368d1-694">AzureRM.LogicApp</span></span>
* <span data-ttu-id="368d1-695">修复了 New-AzureRmLogicApp 中的“无法解析参数集”错误</span><span class="sxs-lookup"><span data-stu-id="368d1-695">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="368d1-696">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="368d1-696">AzureRM.Network</span></span>
* <span data-ttu-id="368d1-697">在多个租户中为 Set/Add-AzureRmVirtualNetworkPeering 启用跨虚拟网络对等互连</span><span class="sxs-lookup"><span data-stu-id="368d1-697">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="368d1-698">针对应用程序网关更新了以下 cmdlet</span><span class="sxs-lookup"><span data-stu-id="368d1-698">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="368d1-699">New-AzureRmApplicationGateway：添加了 EnableFIPS 标志和区域支持</span><span class="sxs-lookup"><span data-stu-id="368d1-699">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="368d1-700">New-AzureRmApplicationGatewaySku：添加了新的 sku Standard_v2 和 WAF_v2</span><span class="sxs-lookup"><span data-stu-id="368d1-700">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="368d1-701">Set-AzureRmApplicationGatewaySku：添加了新的 sku Standard_v2 和 WAF_v2</span><span class="sxs-lookup"><span data-stu-id="368d1-701">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="368d1-702">使用最新的生成器版本重新生成了 RouteTable cmdlet</span><span class="sxs-lookup"><span data-stu-id="368d1-702">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="368d1-703">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="368d1-703">AzureRM.Relay</span></span>
* <span data-ttu-id="368d1-704">更新了 Markdown 文件，其中修复了示例中的参数名称问题</span><span class="sxs-lookup"><span data-stu-id="368d1-704">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="368d1-705">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="368d1-705">AzureRM.Resources</span></span>
* <span data-ttu-id="368d1-706">更新了 Roleassignment 和 roledefinition cmdlet：</span><span class="sxs-lookup"><span data-stu-id="368d1-706">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="368d1-707">删除了作为分页的一部分完成的额外 roledefinition 调用。</span><span class="sxs-lookup"><span data-stu-id="368d1-707">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="368d1-708">修复了 Get-AzureRmRoleAssignment cmdlet</span><span class="sxs-lookup"><span data-stu-id="368d1-708">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="368d1-709">修复了 -ExpandPrincipalGroups 命令参数功能</span><span class="sxs-lookup"><span data-stu-id="368d1-709">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="368d1-710">修复了“Get-AzureRmResource”的问题，其中“-ResourceType”参数区分大小写</span><span class="sxs-lookup"><span data-stu-id="368d1-710">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="368d1-711">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="368d1-711">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="368d1-712">向列表 cmdlet 添加了 top 和 skip 参数</span><span class="sxs-lookup"><span data-stu-id="368d1-712">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="368d1-713">添加了标准到高级命名空间迁移 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="368d1-713">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="368d1-714">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="368d1-714">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="368d1-715">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="368d1-715">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="368d1-716">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="368d1-716">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="368d1-717">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="368d1-717">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="368d1-718">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="368d1-718">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="368d1-719">向 PSServiceBusDRConfigurationAttributes 类添加了一个只读属性“PendingReplicationOperationsCount”，该属性在复制过程中为挂起的复制操作计数</span><span class="sxs-lookup"><span data-stu-id="368d1-719">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="368d1-720">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="368d1-720">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="368d1-721">更新了“New-AzureRmServiceFabricCluster”的示例</span><span class="sxs-lookup"><span data-stu-id="368d1-721">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="368d1-722">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="368d1-722">AzureRM.Sql</span></span>
* <span data-ttu-id="368d1-723">为 Management.Sql 添加新的 Cmdlet，以允许客户将 TDE 证书添加到 Sql Server 实例或托管实例</span><span class="sxs-lookup"><span data-stu-id="368d1-723">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="368d1-724">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="368d1-724">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="368d1-725">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="368d1-725">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="368d1-726">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="368d1-726">AzureRM.Websites</span></span>
* <span data-ttu-id="368d1-727">设置为 false 时，`Set-AzureRmWebApp -AssignIdentity` 和 `Set-AzureRmWebAppSlot -AssignIdentity` 现在将从站点对象中删除 Identity 属性。同时移除预览标记。</span><span class="sxs-lookup"><span data-stu-id="368d1-727">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="368d1-728">`Get-AzureRmWebAppMetrics`、`Get-AzureRmAppServicePlanMetrics` 示例已更新</span><span class="sxs-lookup"><span data-stu-id="368d1-728">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="368d1-729">`Set-AzureRmWebApp -PhpVersion` 支持 off 作为有效的 php 版本</span><span class="sxs-lookup"><span data-stu-id="368d1-729">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="368d1-730">6.4.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="368d1-730">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="368d1-731">常规</span><span class="sxs-lookup"><span data-stu-id="368d1-731">General</span></span>
* <span data-ttu-id="368d1-732">修复了大多数模块的帮助文件中的 OutputType 格式问题</span><span class="sxs-lookup"><span data-stu-id="368d1-732">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="368d1-733">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="368d1-733">AzureRM.Profile</span></span>
* <span data-ttu-id="368d1-734">已将 Ps1Xml 属性添加到基本输出类型</span><span class="sxs-lookup"><span data-stu-id="368d1-734">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="368d1-735">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="368d1-735">AzureRM.Compute</span></span>
* <span data-ttu-id="368d1-736">VMSS 的 IP 标记功能</span><span class="sxs-lookup"><span data-stu-id="368d1-736">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="368d1-737">已添加“New-AzureRmVmssIpTagConfig”cmdlet</span><span class="sxs-lookup"><span data-stu-id="368d1-737">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="368d1-738">已将 IpTag 参数添加到 New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="368d1-738">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="368d1-739">VMSS 的自动 OS 回滚功能</span><span class="sxs-lookup"><span data-stu-id="368d1-739">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="368d1-740">已将 DisableAutoRollback 参数添加到 New-AzureRmVmssConfig 和 Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="368d1-740">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="368d1-741">VMSS 的 OS 升级历史记录功能</span><span class="sxs-lookup"><span data-stu-id="368d1-741">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="368d1-742">已将 OSUpgradeHistory 开关参数添加到 Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="368d1-742">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="368d1-743">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="368d1-743">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="368d1-744">通过以下命令添加目录 ACL 的支持：</span><span class="sxs-lookup"><span data-stu-id="368d1-744">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="368d1-745">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="368d1-745">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="368d1-746">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="368d1-746">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="368d1-747">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="368d1-747">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="368d1-748">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="368d1-748">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="368d1-749">为 Set-AzureRmDataLakeStoreItemAclEntry、Remove-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAcl 添加了取消支持和进度跟踪</span><span class="sxs-lookup"><span data-stu-id="368d1-749">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="368d1-750">为 Export-AzureRmDataLakeStoreChildItemProperties 添加了取消支持</span><span class="sxs-lookup"><span data-stu-id="368d1-750">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="368d1-751">修复了执行递归操作的 cmdlet 的调试消息刷新</span><span class="sxs-lookup"><span data-stu-id="368d1-751">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="368d1-752">修复了 DataLake cmdlet 的测试位置</span><span class="sxs-lookup"><span data-stu-id="368d1-752">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="368d1-753">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="368d1-753">AzureRM.EventHub</span></span>
* <span data-ttu-id="368d1-754">已将可选的 MaxCount 参数添加到“列出操作”cmdlet Get-AzureRmEventHub 和 Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="368d1-754">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="368d1-755">修复了 New-AzureRmEventHub cmdlet 的问题：创建新事件中心时至少需要一个参数。</span><span class="sxs-lookup"><span data-stu-id="368d1-755">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="368d1-756">提供了默认参数集。</span><span class="sxs-lookup"><span data-stu-id="368d1-756">Provided Default Parameter set.</span></span>
* <span data-ttu-id="368d1-757">已将可选参数 -KeyValue 添加到 New-AzureRmEventHubKey cmdlet，该参数可让用户提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="368d1-757">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="368d1-758">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="368d1-758">AzureRM.KeyVault</span></span>
* <span data-ttu-id="368d1-759">修复了 Get-AzureRmKeyVault -Tag 返回所有资源的问题</span><span class="sxs-lookup"><span data-stu-id="368d1-759">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="368d1-760">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="368d1-760">AzureRM.Network</span></span>
* <span data-ttu-id="368d1-761">为区域冗余的 VirtualNetworkGateways 公开新 SKU</span><span class="sxs-lookup"><span data-stu-id="368d1-761">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="368d1-762">通过 ARM 为以下功能添加了新命令：ExpressRoute 合作伙伴 API</span><span class="sxs-lookup"><span data-stu-id="368d1-762">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="368d1-763">添加了 Get-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="368d1-763">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="368d1-764">添加了 Set-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="368d1-764">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="368d1-765">添加了 Add-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="368d1-765">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="368d1-766">添加了 Get-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="368d1-766">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="368d1-767">添加了 Remove-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="368d1-767">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="368d1-768">添加了 Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="368d1-768">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="368d1-769">添加了 Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="368d1-769">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="368d1-770">添加了 Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="368d1-770">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="368d1-771">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="368d1-771">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="368d1-772">添加了 Get-AzureRmRecoveryServicesBackupStatus cmdlet。</span><span class="sxs-lookup"><span data-stu-id="368d1-772">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="368d1-773">此 cmdlet 采用 VM ID，并检查 VM 是否受订阅中的某个保管库保护。</span><span class="sxs-lookup"><span data-stu-id="368d1-773">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="368d1-774">如果存在此类保管库，该 cmdlet 会输出该保管库的详细信息。</span><span class="sxs-lookup"><span data-stu-id="368d1-774">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="368d1-775">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="368d1-775">AzureRM.Resources</span></span>
* <span data-ttu-id="368d1-776">更新了 Get-AzureRmPolicyAssignment cmdlet：</span><span class="sxs-lookup"><span data-stu-id="368d1-776">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="368d1-777">添加了在管理组级别列出 -Scope 值的支持</span><span class="sxs-lookup"><span data-stu-id="368d1-777">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="368d1-778">添加了在管理组级别使用 -Scope 值检索单个分配的支持</span><span class="sxs-lookup"><span data-stu-id="368d1-778">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="368d1-779">已将 -Effective 和 -All 开关添加到 control 参数</span><span class="sxs-lookup"><span data-stu-id="368d1-779">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="368d1-780">更新了 Get/New/Remove/Set-AzureRmPolicyDefinition cmdlet</span><span class="sxs-lookup"><span data-stu-id="368d1-780">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="368d1-781">添加了 -ManagementGroupName 参数，以将操作应用到给定的管理组</span><span class="sxs-lookup"><span data-stu-id="368d1-781">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="368d1-782">添加了 -SubscriptionId 参数，以将操作应用到给定的订阅</span><span class="sxs-lookup"><span data-stu-id="368d1-782">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="368d1-783">更新了 Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlet</span><span class="sxs-lookup"><span data-stu-id="368d1-783">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="368d1-784">添加了 -ManagementGroupName 参数，以将操作应用到给定的管理组</span><span class="sxs-lookup"><span data-stu-id="368d1-784">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="368d1-785">添加了 -SubscriptionId 参数，以将操作应用到给定的订阅</span><span class="sxs-lookup"><span data-stu-id="368d1-785">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="368d1-786">添加了使用 TemplateParameterObject 时在参数中指定 KeyVault 机密引用的支持</span><span class="sxs-lookup"><span data-stu-id="368d1-786">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="368d1-787">修复了忽略“New-AzureRmADAppCredential”的“-EndDate”参数的问题</span><span class="sxs-lookup"><span data-stu-id="368d1-787">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="368d1-788">修复了“Add-AzureRmADGroupMember”使用错误的 URL 发出请求的问题</span><span class="sxs-lookup"><span data-stu-id="368d1-788">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="368d1-789">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="368d1-789">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="368d1-790">已将可选参数 -KeyValue 添加到 New-AzureRmServiceBusKey cmdlet，该参数可让用户提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="368d1-790">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="368d1-791">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="368d1-791">AzureRM.Sql</span></span>
* <span data-ttu-id="368d1-792">在 AzureRmSqlDatabaseRestorePoint 帮助中澄清了 SQLDW 的用户定义还原点</span><span class="sxs-lookup"><span data-stu-id="368d1-792">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="368d1-793">更新了多个 cmdlet 中 -ComputeGeneration 参数的文档</span><span class="sxs-lookup"><span data-stu-id="368d1-793">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="368d1-794">6.3.0 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="368d1-794">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="368d1-795">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="368d1-795">AzureRM.Profile</span></span>
* <span data-ttu-id="368d1-796">更新了 Enable-AzureRmContextAutoSave 的错误消息</span><span class="sxs-lookup"><span data-stu-id="368d1-796">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="368d1-797">在运行没有旧上下文的“Connect-AzureRmAccount”时为每个订阅创建一个上下文</span><span class="sxs-lookup"><span data-stu-id="368d1-797">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="368d1-798">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="368d1-798">Azure.Storage</span></span>
* <span data-ttu-id="368d1-799">在帮助文件中增加了关于 -Permissions 参数的其他信息。</span><span class="sxs-lookup"><span data-stu-id="368d1-799">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="368d1-800">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="368d1-800">AzureRM.Compute</span></span>
* <span data-ttu-id="368d1-801">“Get-AzureRmVmDiskEncryptionStatus”修复了一个针对没有数据磁盘的 VM 观察到的问题</span><span class="sxs-lookup"><span data-stu-id="368d1-801">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="368d1-802">更新计算客户端库版本以修复以下 cmdlet</span><span class="sxs-lookup"><span data-stu-id="368d1-802">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="368d1-803">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="368d1-803">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="368d1-804">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="368d1-804">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="368d1-805">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="368d1-805">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="368d1-806">修复了以下 cmdlet，因此可以正确地显示“操作 ID”和“操作状态”：</span><span class="sxs-lookup"><span data-stu-id="368d1-806">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="368d1-807">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="368d1-807">Start-AzureRmVM</span></span>
    - <span data-ttu-id="368d1-808">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="368d1-808">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="368d1-809">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="368d1-809">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="368d1-810">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="368d1-810">Set-AzureRmVM</span></span>
    - <span data-ttu-id="368d1-811">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="368d1-811">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="368d1-812">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="368d1-812">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="368d1-813">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="368d1-813">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="368d1-814">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="368d1-814">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="368d1-815">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="368d1-815">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="368d1-816">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="368d1-816">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="368d1-817">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="368d1-817">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="368d1-818">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="368d1-818">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="368d1-819">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="368d1-819">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="368d1-820">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="368d1-820">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="368d1-821">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="368d1-821">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="368d1-822">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="368d1-822">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="368d1-823">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="368d1-823">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="368d1-824">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="368d1-824">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="368d1-825">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="368d1-825">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="368d1-826">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="368d1-826">AzureRM.EventGrid</span></span>
* <span data-ttu-id="368d1-827">在 Update-AzureRmEventGridSubscription cmdlet 中删除 SubjectBeginsWith/SubjectEndsWith 的 ValidateNotNullOrEmpty 验证条件，允许根据需要将这些参数更改为空字符串。</span><span class="sxs-lookup"><span data-stu-id="368d1-827">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="368d1-828">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="368d1-828">AzureRM.KeyVault</span></span>
* <span data-ttu-id="368d1-829">修复运行 Get-AzureRmKeyVault -Tag 时不返回任何标记的问题</span><span class="sxs-lookup"><span data-stu-id="368d1-829">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="368d1-830">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="368d1-830">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="368d1-831">策略见解 cmdlet 的公开发行版</span><span class="sxs-lookup"><span data-stu-id="368d1-831">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="368d1-832">使用 API 版本 2018-04-04</span><span class="sxs-lookup"><span data-stu-id="368d1-832">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="368d1-833">向 Get-AzureRmPolicyStateSummary 的结果添加了 PolicyDefinitionReferenceId</span><span class="sxs-lookup"><span data-stu-id="368d1-833">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="368d1-834">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="368d1-834">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="368d1-835">向 RecoveryServices.Backup cmdlet 添加了 -Vault 参数。</span><span class="sxs-lookup"><span data-stu-id="368d1-835">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="368d1-836">传递时，此项会替代 Set-AzureRmRecoveryServicesContext cmdlet。</span><span class="sxs-lookup"><span data-stu-id="368d1-836">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="368d1-837">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="368d1-837">AzureRM.Sql</span></span>
* <span data-ttu-id="368d1-838">更新了 Get-AzureRmSqlDatabaseExpanded 的帮助文件中的示例</span><span class="sxs-lookup"><span data-stu-id="368d1-838">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="368d1-839">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="368d1-839">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="368d1-840">更新了 Add-AzureRmTrafficManagerEndpointConfig 的帮助文件</span><span class="sxs-lookup"><span data-stu-id="368d1-840">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="368d1-841">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="368d1-841">AzureRM.Websites</span></span>
* <span data-ttu-id="368d1-842">更新了“Set-AzureRmWebApp”，在使用 -AssignIdentity 时不覆盖 AppSettings</span><span class="sxs-lookup"><span data-stu-id="368d1-842">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="368d1-843">更新了“New-AzureRmWebAppSlot”，允许使用 AppServicePlan 作为可选参数</span><span class="sxs-lookup"><span data-stu-id="368d1-843">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="368d1-844">6.2.1 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="368d1-844">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="368d1-845">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="368d1-845">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="368d1-846">更新了 PSWorkspace 模型，允许 Network 使用 type 作为参数</span><span class="sxs-lookup"><span data-stu-id="368d1-846">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="368d1-847">6.2.0 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="368d1-847">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="368d1-848">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="368d1-848">AzureRM.Profile</span></span>
* <span data-ttu-id="368d1-849">修复了 Newtonsoft.Json 的版本 10.0.3 在模块导入时无法加载的问题</span><span class="sxs-lookup"><span data-stu-id="368d1-849">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="368d1-850">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="368d1-850">AzureRM.Compute</span></span>
* <span data-ttu-id="368d1-851">VMSS VM 更新功能</span><span class="sxs-lookup"><span data-stu-id="368d1-851">VMSS VM Update feature</span></span>
    - <span data-ttu-id="368d1-852">增加了“Update-AzureRmVmssVM”和“New-AzureRmVMDataDisk”cmdlet</span><span class="sxs-lookup"><span data-stu-id="368d1-852">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="368d1-853">为“Add-AzureRmVMDataDisk”cmdlet 增加了 VirtualMachineScaleSetVM 参数，支持向 Vmss VM 添加数据磁盘。</span><span class="sxs-lookup"><span data-stu-id="368d1-853">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="368d1-854">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="368d1-854">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="368d1-855">将 ADF.Net SDK 版本更新到了 0.8.0-preview，其中包含以下更改：</span><span class="sxs-lookup"><span data-stu-id="368d1-855">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="368d1-856">增加了“配置工厂存储库”操作</span><span class="sxs-lookup"><span data-stu-id="368d1-856">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="368d1-857">更新了 QuickBooks LinkedService，可以公开 consumerKey 和 consumerSecret 属性</span><span class="sxs-lookup"><span data-stu-id="368d1-857">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="368d1-858">已将多个模型类型从 SecretBase 更新为 Object</span><span class="sxs-lookup"><span data-stu-id="368d1-858">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="368d1-859">增加了 Blob 事件触发器</span><span class="sxs-lookup"><span data-stu-id="368d1-859">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="368d1-860">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="368d1-860">AzureRM.KeyVault</span></span>
* <span data-ttu-id="368d1-861">使用示例输出更新了文档</span><span class="sxs-lookup"><span data-stu-id="368d1-861">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="368d1-862">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="368d1-862">AzureRM.Network</span></span>
* <span data-ttu-id="368d1-863">在网络观察程序 cmdlet 上启用了流量分析参数</span><span class="sxs-lookup"><span data-stu-id="368d1-863">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="368d1-864">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="368d1-864">AzureRM.Resources</span></span>
* <span data-ttu-id="368d1-865">修复了从“Get-AzureRmResource”返回的“PSResource”对象的“Properties”属性问题</span><span class="sxs-lookup"><span data-stu-id="368d1-865">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="368d1-866">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="368d1-866">AzureRM.Scheduler</span></span>
* <span data-ttu-id="368d1-867">修复了更新 ServiceBusQueueJob 无法设置新 Auth 值的问题</span><span class="sxs-lookup"><span data-stu-id="368d1-867">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="368d1-868">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="368d1-868">AzureRM.Sql</span></span>
* <span data-ttu-id="368d1-869">使用可选的 LicenseType 参数更新了以下 cmdlet</span><span class="sxs-lookup"><span data-stu-id="368d1-869">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="368d1-870">New-AzureRmSqlDatabase；Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="368d1-870">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="368d1-871">New-AzureRmSqlElasticPool；Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="368d1-871">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="368d1-872">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="368d1-872">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="368d1-873">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="368d1-873">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="368d1-874">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="368d1-874">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="368d1-875">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="368d1-875">AzureRM.Websites</span></span>
* <span data-ttu-id="368d1-876">更新了“New-AzureRMWebApp”，可以使用策略库中的常用算法。</span><span class="sxs-lookup"><span data-stu-id="368d1-876">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="368d1-877">6.1.0 - 2018 年 5 月</span><span class="sxs-lookup"><span data-stu-id="368d1-877">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="368d1-878">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="368d1-878">AzureRM.Profile</span></span>
* <span data-ttu-id="368d1-879">修复了运行“Clear-AzureRmContext”时会保留空上下文的问题，该上下文使用旧的默认上下文的名称，导致用户无法使用旧名称创建新的上下文</span><span class="sxs-lookup"><span data-stu-id="368d1-879">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="368d1-880">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="368d1-880">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="368d1-881">允许在 AS 上执行网关的关联/取消关联操作。</span><span class="sxs-lookup"><span data-stu-id="368d1-881">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="368d1-882">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="368d1-882">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="368d1-883">增加了对 ApiVersions、ApiReleases 和 ApiRevisions 的支持</span><span class="sxs-lookup"><span data-stu-id="368d1-883">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="368d1-884">增加了对 ServiceFabric 后端的支持</span><span class="sxs-lookup"><span data-stu-id="368d1-884">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="368d1-885">增加了对 Application Insights Logger 的支持</span><span class="sxs-lookup"><span data-stu-id="368d1-885">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="368d1-886">增加的支持包括认可“基本”SKU 是 API 管理服务的有效 SKU</span><span class="sxs-lookup"><span data-stu-id="368d1-886">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="368d1-887">增加的支持包括允许将专用 CA 颁发的证书作为根证书或 CA 证书安装</span><span class="sxs-lookup"><span data-stu-id="368d1-887">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="368d1-888">增加的支持包括通过 KeyVault 和多个代理主机名接受自定义 SSL 证书</span><span class="sxs-lookup"><span data-stu-id="368d1-888">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="368d1-889">增加了对 MSI 标识的支持</span><span class="sxs-lookup"><span data-stu-id="368d1-889">Added support for MSI identity</span></span>
* <span data-ttu-id="368d1-890">增加的支持包括通过 URL 接受策略 注意：以下 cmdlet 将在未来版本中弃用</span><span class="sxs-lookup"><span data-stu-id="368d1-890">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="368d1-891">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="368d1-891">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="368d1-892">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="368d1-892">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="368d1-893">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="368d1-893">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="368d1-894">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="368d1-894">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="368d1-895">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="368d1-895">AzureRM.Batch</span></span>
* <span data-ttu-id="368d1-896">发布新 cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="368d1-896">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="368d1-897">发布新 cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="368d1-897">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="368d1-898">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="368d1-898">AzureRM.Consumption</span></span>
* <span data-ttu-id="368d1-899">在 Cmdlet Get-AzureRmConsumptionUsageDetail 中增加了新参数 Expand、ResourceGroup、InstanceName、InstanceId、Tags、Top</span><span class="sxs-lookup"><span data-stu-id="368d1-899">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="368d1-900">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="368d1-900">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="368d1-901">修复了 Export-AzureRmDataLakeStoreChildItemProperties 的示例</span><span class="sxs-lookup"><span data-stu-id="368d1-901">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="368d1-902">修复了 Set-AzureRmDataLakeStoreItemAclEntry 中 Recurse 用例的 null 参数异常</span><span class="sxs-lookup"><span data-stu-id="368d1-902">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="368d1-903">修复了 Set-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAcl、Remove-AzureRmDataLakeStoreItemAclEntry 的帮助文件</span><span class="sxs-lookup"><span data-stu-id="368d1-903">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="368d1-904">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="368d1-904">AzureRM.Network</span></span>
* <span data-ttu-id="368d1-905">将网络 SDK 版本从 18.0.0-preview 升至 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="368d1-905">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="368d1-906">增加了用于创建协议配置的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="368d1-906">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="368d1-907">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="368d1-907">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="368d1-908">增加了用于向现有的快速路由线路添加新的线路连接的 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="368d1-908">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="368d1-909">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="368d1-909">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="368d1-910">增加了用于从现有的快速路由线路删除线路连接的 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="368d1-910">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="368d1-911">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="368d1-911">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="368d1-912">增加了用于检索线路连接的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="368d1-912">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="368d1-913">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="368d1-913">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="368d1-914">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="368d1-914">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="368d1-915">修复了使用生成的证书进行服务器身份验证的问题（问题 5998）</span><span class="sxs-lookup"><span data-stu-id="368d1-915">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="368d1-916">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="368d1-916">AzureRM.Sql</span></span>
* <span data-ttu-id="368d1-917">更新了审核 cmdlet，允许删除 AuditActions 或 AuditActionGroups</span><span class="sxs-lookup"><span data-stu-id="368d1-917">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="368d1-918">修复了设置新的灵活保留策略时使用 Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy 出现的问题。该问题的具体表现是：在命令失败的同时，出现“不再支持使用 Azure 恢复服务保管库和策略配置长期保留策略。</span><span class="sxs-lookup"><span data-stu-id="368d1-918">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="368d1-919">请使用新的灵活保留策略提交请求”错误消息。</span><span class="sxs-lookup"><span data-stu-id="368d1-919">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="368d1-920">更新了与 Azure SQL 数据库/ElasticPool 的创建/更新相关的所有 cmdlet，允许使用新的数据库 API，而这些 cmdlet 支持的 SKU 属性则适用于规模和层相关属性。</span><span class="sxs-lookup"><span data-stu-id="368d1-920">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="368d1-921">更新的 cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="368d1-921">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="368d1-922">New-AzureRmSqlDatabase；Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="368d1-922">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="368d1-923">New-AzureRmSqlElasticPool；Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="368d1-923">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="368d1-924">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="368d1-924">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="368d1-925">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="368d1-925">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="368d1-926">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="368d1-926">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="368d1-927">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="368d1-927">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="368d1-928">更新了“Get-AzureRmTrafficManagerProfile”的参数，要求在使用 -Name 参数时使用 -ResourceGroupName 参数。</span><span class="sxs-lookup"><span data-stu-id="368d1-928">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
