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
ms.sourcegitcommit: 558436c824d9b59731aa9b963cdc8df4dea932e7
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/29/2018
ms.locfileid: "52587833"
---
# <a name="release-notes"></a><span data-ttu-id="d15b5-103">发行说明</span><span class="sxs-lookup"><span data-stu-id="d15b5-103">Release notes</span></span>

<span data-ttu-id="d15b5-104">下面是此版本中对 Azure PowerShell 所做的更改列表。</span><span class="sxs-lookup"><span data-stu-id="d15b5-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="6130---november-2018"></a><span data-ttu-id="d15b5-105">6.13.0 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="d15b5-105">6.13.0 - November 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="d15b5-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="d15b5-106">AzureRM.Profile</span></span>
* <span data-ttu-id="d15b5-107">更新通用代码以使用最新版本的 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="d15b5-107">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="d15b5-108">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d15b5-108">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="d15b5-109">更新类型映射问题的依赖项</span><span class="sxs-lookup"><span data-stu-id="d15b5-109">Update dependencies for type mapping issue</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="d15b5-110">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="d15b5-110">AzureRM.Automation</span></span>
* <span data-ttu-id="d15b5-111">基于 Swagger 的 Azure 自动化 cmdlet</span><span class="sxs-lookup"><span data-stu-id="d15b5-111">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="d15b5-112">增加了更新管理 cmdlet</span><span class="sxs-lookup"><span data-stu-id="d15b5-112">Added Update Management cmdlets</span></span>
* <span data-ttu-id="d15b5-113">增加了源代码管理 cmdlet</span><span class="sxs-lookup"><span data-stu-id="d15b5-113">Added Source Control cmdlets</span></span>
* <span data-ttu-id="d15b5-114">增加了 Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span><span class="sxs-lookup"><span data-stu-id="d15b5-114">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="d15b5-115">修复了 DSC Register Node 命令</span><span class="sxs-lookup"><span data-stu-id="d15b5-115">Fixed the DSC Register Node command</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="d15b5-116">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="d15b5-116">AzureRM.Compute</span></span>
* <span data-ttu-id="d15b5-117">修复了 SystemAssigned 标识的标识问题</span><span class="sxs-lookup"><span data-stu-id="d15b5-117">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="d15b5-118">更新类型映射问题的依赖项</span><span class="sxs-lookup"><span data-stu-id="d15b5-118">Update dependencies for type mapping issue</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="d15b5-119">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="d15b5-119">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="d15b5-120">更新类型映射问题的依赖项</span><span class="sxs-lookup"><span data-stu-id="d15b5-120">Update dependencies for type mapping issue</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="d15b5-121">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="d15b5-121">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="d15b5-122">更新市场 cmdlet 的示例说明</span><span class="sxs-lookup"><span data-stu-id="d15b5-122">update the examples description for marketplace cmdlets</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="d15b5-123">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="d15b5-123">AzureRM.Network</span></span>
* <span data-ttu-id="d15b5-124">增加了 cmdlet New-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayCustomError、Get-AzureRmApplicationGatewayCustomError、Set-AzureRmApplicationGatewayCustomError、Remove-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayHttpListenerCustomError、Get-AzureRmApplicationGatewayHttpListenerCustomError、Set-AzureRmApplicationGatewayHttpListenerCustomError、Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="d15b5-124">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="d15b5-125">将 ICMP 重新添加到受支持的 AzureFirewall 网络协议</span><span class="sxs-lookup"><span data-stu-id="d15b5-125">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="d15b5-126">更新 cmdlet Test-AzureRmNetworkWatcherConnectivity，在目标 ID、地址和端口上添加验证。</span><span class="sxs-lookup"><span data-stu-id="d15b5-126">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="d15b5-127">修复 VirtualNetwork 映射中内存使用的问题</span><span class="sxs-lookup"><span data-stu-id="d15b5-127">Fix issues with memory usage in VirtualNetwork map</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="d15b5-128">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="d15b5-128">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="d15b5-129">修复受保护文件共享的策略修改问题。</span><span class="sxs-lookup"><span data-stu-id="d15b5-129">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="d15b5-130">将策略时区转换成了大写形式。</span><span class="sxs-lookup"><span data-stu-id="d15b5-130">Converted policy timezone to uppercase.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="d15b5-131">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="d15b5-131">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="d15b5-132">更正了 New-AzureRmRecoveryServicesAsrProtectableItem 中的示例</span><span class="sxs-lookup"><span data-stu-id="d15b5-132">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="d15b5-133">更新类型映射问题的依赖项</span><span class="sxs-lookup"><span data-stu-id="d15b5-133">Update dependencies for type mapping issue</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="d15b5-134">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="d15b5-134">AzureRM.Relay</span></span>
* <span data-ttu-id="d15b5-135">已将可选参数 -KeyValue 添加到 New-AzureRmRelayKey cmdlet，该参数允许用户提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="d15b5-135">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="d15b5-136">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="d15b5-136">AzureRM.Resources</span></span>
* <span data-ttu-id="d15b5-137">更新 `New-AzureRmPolicyAssignment` 和 `Set-AzureRmPolicyAssignment` 中资源标识相关参数的帮助文档</span><span class="sxs-lookup"><span data-stu-id="d15b5-137">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="d15b5-138">为使用 -Metadata 的 New-AzureRmPolicyDefinition 添加一个示例</span><span class="sxs-lookup"><span data-stu-id="d15b5-138">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="d15b5-139">修复后允许在 NetStandard 的 Tag 键中保留大小写：#7678 #7703</span><span class="sxs-lookup"><span data-stu-id="d15b5-139">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="d15b5-140">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d15b5-140">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="d15b5-141">在即将发布的重大更改中添加弃用消息</span><span class="sxs-lookup"><span data-stu-id="d15b5-141">Add deprecation messages for upcoming breaking changes</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="d15b5-142">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="d15b5-142">AzureRM.Sql</span></span>
* <span data-ttu-id="d15b5-143">为 Azure SQL 数据库托管实例和 Azure SQL 托管数据库上的 CRUD 操作添加了新的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="d15b5-143">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="d15b5-144">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="d15b5-144">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="d15b5-145">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="d15b5-145">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="d15b5-146">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="d15b5-146">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="d15b5-147">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="d15b5-147">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="d15b5-148">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="d15b5-148">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="d15b5-149">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="d15b5-149">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="d15b5-150">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="d15b5-150">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="d15b5-151">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="d15b5-151">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="d15b5-152">允许在服务器或数据库上进行扩展的审核策略管理。</span><span class="sxs-lookup"><span data-stu-id="d15b5-152">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="d15b5-153">添加了新的参数 (PredicateExpression)，用于筛选审核日志。</span><span class="sxs-lookup"><span data-stu-id="d15b5-153">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="d15b5-154">修改了 Cmdlet，以便使用 SQL 客户端而不是旧客户端。</span><span class="sxs-lookup"><span data-stu-id="d15b5-154">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="d15b5-155">Set-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="d15b5-155">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="d15b5-156">Get-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="d15b5-156">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="d15b5-157">Set-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="d15b5-157">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="d15b5-158">Get-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="d15b5-158">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="d15b5-159">修复了将 Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings 与存储帐户名称参数集配合使用时出现的问题</span><span class="sxs-lookup"><span data-stu-id="d15b5-159">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="6120---november-2018"></a><span data-ttu-id="d15b5-160">6.12.0 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="d15b5-160">6.12.0 - November 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="d15b5-161">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="d15b5-161">AzureRM.Profile</span></span>
* <span data-ttu-id="d15b5-162">更新通用代码以使用最新版本的 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="d15b5-162">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="d15b5-163">将 Connect-AzureRmAccount cmdlet 中的 TenantId 参数重命名为 Tenant，并为 TenantId 添加别名</span><span class="sxs-lookup"><span data-stu-id="d15b5-163">Rename param TenantId in cmdlet Connect-AzureRmAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="d15b5-164">更新了 Connect-AzureRmAccount 的 TenantId 说明</span><span class="sxs-lookup"><span data-stu-id="d15b5-164">Updated TenantId description for Connect-AzureRmAccount</span></span>
* <span data-ttu-id="d15b5-165">修复了在提供租户域时失败的登录的错误消息</span><span class="sxs-lookup"><span data-stu-id="d15b5-165">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="d15b5-166">为租户中没有订阅的帐户修复了上下文名称冲突的问题</span><span class="sxs-lookup"><span data-stu-id="d15b5-166">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="d15b5-167">修复了在使用 MSI 时的 DataLake 终结点问题</span><span class="sxs-lookup"><span data-stu-id="d15b5-167">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="d15b5-168">修复了在未连接时会引发“Disconnect-AzureRmAccount”的问题</span><span class="sxs-lookup"><span data-stu-id="d15b5-168">Fix issue where 'Disconnect-AzureRmAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azurermautomation"></a><span data-ttu-id="d15b5-169">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="d15b5-169">AzureRM.Automation</span></span>
* <span data-ttu-id="d15b5-170">已将 cmdlet DLL 文件名重命名为 Microsoft.Azure.Commands.Automation.dll</span><span class="sxs-lookup"><span data-stu-id="d15b5-170">Renamed cmdlet DLL filename to Microsoft.Azure.Commands.Automation.dll</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="d15b5-171">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d15b5-171">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="d15b5-172">添加了 Get-AzureRmCognitiveServicesAccountSkus 操作。</span><span class="sxs-lookup"><span data-stu-id="d15b5-172">Add Get-AzureRmCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="d15b5-173">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="d15b5-173">AzureRM.Compute</span></span>
* <span data-ttu-id="d15b5-174">添加了 Add-AzureRmVmssVMDataDisk 和 Remove-AzureRmVmssVMDataDisk cmdlet</span><span class="sxs-lookup"><span data-stu-id="d15b5-174">Add Add-AzureRmVmssVMDataDisk and Remove-AzureRmVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="d15b5-175">Get-AzureRmVMImage 显示 AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="d15b5-175">Get-AzureRmVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="d15b5-176">修复了 SetAzureRmVMChefExtension BootstrapOptions 和 -JsonAttribute 选项值未以 json 格式设置的问题。</span><span class="sxs-lookup"><span data-stu-id="d15b5-176">Fixed SetAzureRmVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="d15b5-177">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d15b5-177">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="d15b5-178">将 DataLake 程序包更新至 1.1.10。</span><span class="sxs-lookup"><span data-stu-id="d15b5-178">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="d15b5-179">将默认并发添加到多线程操作。</span><span class="sxs-lookup"><span data-stu-id="d15b5-179">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="d15b5-180">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="d15b5-180">AzureRM.Insights</span></span>
* <span data-ttu-id="d15b5-181">修复了问题 #7267（自动缩放区域）</span><span class="sxs-lookup"><span data-stu-id="d15b5-181">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="d15b5-182">创建新的自动缩放规则时未正确设置枚举的参数（始终将它们设置为默认值）的问题。</span><span class="sxs-lookup"><span data-stu-id="d15b5-182">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="d15b5-183">修复了问题 #7513 [见解] Set-AzureRMDiagnosticSetting 在创建设置期间需要显式指定类别</span><span class="sxs-lookup"><span data-stu-id="d15b5-183">Fixed issue #7513 [Insights] Set-AzureRMDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="d15b5-184">现在该 cmdlet 不需要在创建期间显式指示要启用的类别，即它会按记录工作</span><span class="sxs-lookup"><span data-stu-id="d15b5-184">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="d15b5-185">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="d15b5-185">AzureRM.Network</span></span>
* <span data-ttu-id="d15b5-186">已将 PeeringType 更改为以下 cmdlet 的必需参数：</span><span class="sxs-lookup"><span data-stu-id="d15b5-186">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="d15b5-187">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="d15b5-187">Get-AzureRmExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="d15b5-188">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="d15b5-188">Get-AzureRmExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="d15b5-189">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="d15b5-189">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="d15b5-190">Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="d15b5-190">Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="d15b5-191">Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="d15b5-191">Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="d15b5-192">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="d15b5-192">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="d15b5-193">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="d15b5-193">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="d15b5-194">添加了策略修正 cmdlet</span><span class="sxs-lookup"><span data-stu-id="d15b5-194">Added policy remediation cmdlets</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="d15b5-195">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="d15b5-195">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="d15b5-196">添加了对恢复服务中 azure 文件共享的支持。</span><span class="sxs-lookup"><span data-stu-id="d15b5-196">Added support for azure file shares in recovery services.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="d15b5-197">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="d15b5-197">AzureRM.Resources</span></span>
* <span data-ttu-id="d15b5-198">https://github.com/Azure/azure-powershell/issues/7402 的修复</span><span class="sxs-lookup"><span data-stu-id="d15b5-198">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="d15b5-199">允许对“Get-AzureRmResource”使用“-ResourceId”参数来列出资源</span><span class="sxs-lookup"><span data-stu-id="d15b5-199">Allow listing resources using the '-ResourceId' parameter for 'Get-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="d15b5-200">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d15b5-200">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="d15b5-201">为 PSServiceBusMigrationConfigurationAttributes 添加了 MigrationState 只读属性，这将有助于了解迁移状态。</span><span class="sxs-lookup"><span data-stu-id="d15b5-201">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="d15b5-202">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d15b5-202">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="d15b5-203">修复了将证书添加到 Linux Vmss 的问题。</span><span class="sxs-lookup"><span data-stu-id="d15b5-203">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="d15b5-204">修复了“Add-AzureRmServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="d15b5-204">Fix 'Add-AzureRmServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="d15b5-205">使用来自新证书的正确指纹 (Azure/service-fabric-issues#932)。</span><span class="sxs-lookup"><span data-stu-id="d15b5-205">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="d15b5-206">正确显示异常 (Azure/service-fabric-issues#1054)。</span><span class="sxs-lookup"><span data-stu-id="d15b5-206">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="d15b5-207">修复了“Update-AzureRmServiceFabricDurability”以在开始 Vmss CreateOrUpdate 操作之前更新群集配置。</span><span class="sxs-lookup"><span data-stu-id="d15b5-207">Fix 'Update-AzureRmServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="6110---october-2018"></a><span data-ttu-id="d15b5-208">6.11.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="d15b5-208">6.11.0 - October 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="d15b5-209">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="d15b5-209">AzureRM.Profile</span></span>
* <span data-ttu-id="d15b5-210">修复了 CloudShell 中 Get-AzureRmSubscription 的问题</span><span class="sxs-lookup"><span data-stu-id="d15b5-210">Fix issue with Get-AzureRmSubscription in CloudShell</span></span>
* <span data-ttu-id="d15b5-211">更新通用代码以使用最新版本的 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="d15b5-211">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="d15b5-212">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="d15b5-212">AzureRM.Backup</span></span>
* <span data-ttu-id="d15b5-213">已弃用 Azure 备份 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d15b5-213">Deprecated Azure Backup cmdlets.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="d15b5-214">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="d15b5-214">AzureRM.Compute</span></span>
* <span data-ttu-id="d15b5-215">向 VM 大小的允许列表添加了新的大小，这样就可以在将简单的参数集用于“New-AzureRmVm”时为这些大小启用加速网络</span><span class="sxs-lookup"><span data-stu-id="d15b5-215">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzureRmVm'</span></span>
* <span data-ttu-id="d15b5-216">向所有 cmdlet 添加了 ResourceName 参数补全选项。</span><span class="sxs-lookup"><span data-stu-id="d15b5-216">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="d15b5-217">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d15b5-217">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="d15b5-218">添加虚拟网络规则的支持</span><span class="sxs-lookup"><span data-stu-id="d15b5-218">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="d15b5-219">Get-AzureRmDataLakeStoreVirtualNetworkRule：获取或列出 Azure Data Lake Store 虚拟网络规则。</span><span class="sxs-lookup"><span data-stu-id="d15b5-219">Get-AzureRmDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="d15b5-220">Add-AzureRmDataLakeStoreVirtualNetworkRule：向指定的 Data Lake Store 帐户添加虚拟网络规则。</span><span class="sxs-lookup"><span data-stu-id="d15b5-220">Add-AzureRmDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="d15b5-221">Set-AzureRmDataLakeStoreVirtualNetworkRule：在指定的 Data Lake Store 帐户中修改指定的虚拟网络规则。</span><span class="sxs-lookup"><span data-stu-id="d15b5-221">Set-AzureRmDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="d15b5-222">Remove-AzureRmDataLakeStoreVirtualNetworkRule：删除 Azure Data Lake Store 虚拟网络规则。</span><span class="sxs-lookup"><span data-stu-id="d15b5-222">Remove-AzureRmDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="d15b5-223">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="d15b5-223">AzureRM.Network</span></span>
* <span data-ttu-id="d15b5-224">更新 cmdlet Test-AzureRmNetworkWatcherConnectivity，向后端传递协议值。</span><span class="sxs-lookup"><span data-stu-id="d15b5-224">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="d15b5-225">向所有 cmdlet 添加了 ResourceName 参数补全选项。</span><span class="sxs-lookup"><span data-stu-id="d15b5-225">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="d15b5-226">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="d15b5-226">AzureRM.Resources</span></span>
* <span data-ttu-id="d15b5-227">通过在方案中添加一个有意义的异常，修复了 Get-AzureRMRoleDefinition 在默认配置文件中没有订阅且未指定范围的情况下引发难以理解异常的问题。</span><span class="sxs-lookup"><span data-stu-id="d15b5-227">Fix isssue where Get-AzureRMRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="d15b5-228">另外，已将默认参数集设置为“RoleDefinitionNameParameterSet”。</span><span class="sxs-lookup"><span data-stu-id="d15b5-228">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="6100---october-2018"></a><span data-ttu-id="d15b5-229">6.10.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="d15b5-229">6.10.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="d15b5-230">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="d15b5-230">Azure.Storage</span></span>
* <span data-ttu-id="d15b5-231">修复了 Copy Blob/File 在目标有元数据问题时不会复制元数据的问题</span><span class="sxs-lookup"><span data-stu-id="d15b5-231">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="d15b5-232">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="d15b5-232">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="d15b5-233">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="d15b5-233">Start-AzureStorageFileCopy</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="d15b5-234">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d15b5-234">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="d15b5-235">在没有现有帐户的情况下支持 Get-AzureRmCognitiveServicesAccountSkus。</span><span class="sxs-lookup"><span data-stu-id="d15b5-235">Support Get-AzureRmCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="d15b5-236">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="d15b5-236">AzureRM.Compute</span></span>
* <span data-ttu-id="d15b5-237">修复了 Get-AzureRmVM -ResourceGroupName <rg>，以在需要时返回超过 50 个结果</span><span class="sxs-lookup"><span data-stu-id="d15b5-237">Fix Get-AzureRmVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="d15b5-238">在 New-AzureRmVmss cmdlet 帮助中添加了“SimpleParameterSet”的示例。</span><span class="sxs-lookup"><span data-stu-id="d15b5-238">Added an example of the 'SimpleParameterSet' to New-AzureRmVmss cmdlet help.</span></span>
* <span data-ttu-id="d15b5-239">修复了 Azure 磁盘加密进度消息中的拼写错误</span><span class="sxs-lookup"><span data-stu-id="d15b5-239">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="d15b5-240">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="d15b5-240">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="d15b5-241">将 ADF .Net SDK 版本更新为 2.3.0。</span><span class="sxs-lookup"><span data-stu-id="d15b5-241">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="d15b5-242">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="d15b5-242">AzureRM.Network</span></span>
* <span data-ttu-id="d15b5-243">添加了 NetworkProfile 功能。</span><span class="sxs-lookup"><span data-stu-id="d15b5-243">Added NetworkProfile functionality.</span></span> <span data-ttu-id="d15b5-244">添加了新 cmdlet</span><span class="sxs-lookup"><span data-stu-id="d15b5-244">new cmdlets added</span></span>
    - <span data-ttu-id="d15b5-245">Get-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="d15b5-245">Get-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="d15b5-246">New-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="d15b5-246">New-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="d15b5-247">Remove-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="d15b5-247">Remove-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="d15b5-248">Set-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="d15b5-248">Set-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="d15b5-249">New-AzureRMContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="d15b5-249">New-AzureRMContainerNicConfig</span></span>
    - <span data-ttu-id="d15b5-250">New-AzureRmContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="d15b5-250">New-AzureRmContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="d15b5-251">在子网模型上添加了服务关联链接</span><span class="sxs-lookup"><span data-stu-id="d15b5-251">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="d15b5-252">添加了 cmdlet New-AzureRmVirtualNetworkTap、Get-AzureRmVirtualNetworkTap、Set-AzureRmVirtualNetworkTap、Remove-AzureRmVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="d15b5-252">Added cmdlet New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap</span></span>
* <span data-ttu-id="d15b5-253">添加了 cmdlet Set-AzureRmNEtworkInterfaceTapConfig、Get-AzureRmNEtworkInterfaceTapConfig、Remove-AzureRmNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="d15b5-253">Added cmdlet Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="d15b5-254">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="d15b5-254">AzureRM.RedisCache</span></span>
* <span data-ttu-id="d15b5-255">今后允许任何字符串作为 Size 参数。</span><span class="sxs-lookup"><span data-stu-id="d15b5-255">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="d15b5-256">在 PSArgumentCompleter 弹出窗口中添加了 P5</span><span class="sxs-lookup"><span data-stu-id="d15b5-256">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="d15b5-257">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="d15b5-257">AzureRM.Resources</span></span>
* <span data-ttu-id="d15b5-258">将缺少的 -Mode 参数添加到 Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d15b5-258">Add missing -Mode parameter to Set-AzureRmPolicyDefinition</span></span>
* <span data-ttu-id="d15b5-259">对于使用包含用户的源的操作，修复了 Get-AzureRmProviderOperation commandlet bug</span><span class="sxs-lookup"><span data-stu-id="d15b5-259">Fix Get-AzureRmProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="d15b5-260">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="d15b5-260">AzureRM.Sql</span></span>
* <span data-ttu-id="d15b5-261">修复了某些备份 cmdlet 无法识别当前 azure 订阅的问题</span><span class="sxs-lookup"><span data-stu-id="d15b5-261">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="d15b5-262">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="d15b5-262">AzureRM.Storage</span></span>
* <span data-ttu-id="d15b5-263">支持获取特定位置的存储资源使用情况，并对于获取的全局存储资源使用情况已过时添加警告消息。</span><span class="sxs-lookup"><span data-stu-id="d15b5-263">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="d15b5-264">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="d15b5-264">Get-AzureRmStorageUsage</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="d15b5-265">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="d15b5-265">AzureRM.Websites</span></span>
* <span data-ttu-id="d15b5-266">新 Cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl - 获取容器持续部署 Webhook URL</span><span class="sxs-lookup"><span data-stu-id="d15b5-266">New Cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="d15b5-267">新 Cmdlet New-AzureRMWebAppContainerPSSession 和 Enter-WebAppContainerPSSession - 在 Windows 容器应用中启动 PowerShell 远程会话</span><span class="sxs-lookup"><span data-stu-id="d15b5-267">New Cmdlets New-AzureRMWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="690---september-2018"></a><span data-ttu-id="d15b5-268">6.9.0 - 2018 年 9 月</span><span class="sxs-lookup"><span data-stu-id="d15b5-268">6.9.0 - September 2018</span></span>
#### <a name="general"></a><span data-ttu-id="d15b5-269">常规</span><span class="sxs-lookup"><span data-stu-id="d15b5-269">General</span></span>
* <span data-ttu-id="d15b5-270">AzureRM.SignalR 已添加到 AzureRM 汇总模块</span><span class="sxs-lookup"><span data-stu-id="d15b5-270">AzureRM.SignalR was added to the AzureRM rollup module</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="d15b5-271">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="d15b5-271">AzureRM.Profile</span></span>
* <span data-ttu-id="d15b5-272">对存储常用代码进行了细微的更改</span><span class="sxs-lookup"><span data-stu-id="d15b5-272">Minor changes to the storage common code</span></span>
* <span data-ttu-id="d15b5-273">更新了帮助文件，使之包括完整参数类型。</span><span class="sxs-lookup"><span data-stu-id="d15b5-273">Updated help files to include full parameter types.</span></span>
* <span data-ttu-id="d15b5-274">已在 ServicePrincipalCertificateWithSubscriptionId 参数集中将 -ServicePrincipal 更改为非强制性项</span><span class="sxs-lookup"><span data-stu-id="d15b5-274">Changed -ServicePrincipal to non-mandatory in the ServicePrincipalCertificateWithSubscriptionId parameter set</span></span> 

#### <a name="azurestorage"></a><span data-ttu-id="d15b5-275">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="d15b5-275">Azure.Storage</span></span>
* <span data-ttu-id="d15b5-276">支持使用 OAuth 创建存储上下文。</span><span class="sxs-lookup"><span data-stu-id="d15b5-276">Support create Storage Context with OAuth.</span></span> 
    - <span data-ttu-id="d15b5-277">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="d15b5-277">New-AzureStorageContext</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="d15b5-278">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="d15b5-278">AzureRM.Cdn</span></span>
* <span data-ttu-id="d15b5-279">在 Cdn 定价 sku 中增加了 Standard_Microsoft。</span><span class="sxs-lookup"><span data-stu-id="d15b5-279">Added Standard_Microsoft in Cdn pricing sku.</span></span> 

#### <a name="azurermcompute"></a><span data-ttu-id="d15b5-280">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="d15b5-280">AzureRM.Compute</span></span>
* <span data-ttu-id="d15b5-281">将 Keyvault 和存储的依赖项移到了常用依赖项中</span><span class="sxs-lookup"><span data-stu-id="d15b5-281">Move dependencies on Keyvault and Storage to the common dependencies</span></span>
* <span data-ttu-id="d15b5-282">增加了对 AEM cmdlet 的支持，可以使用更多的虚拟机大小</span><span class="sxs-lookup"><span data-stu-id="d15b5-282">Add support for more virutal machine sizes to AEM cmdlets</span></span>
* <span data-ttu-id="d15b5-283">为 New-AzureRmVmssIpConfig 增加了 PublicIPPrefix 参数</span><span class="sxs-lookup"><span data-stu-id="d15b5-283">Add PublicIPPrefix parameter to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="d15b5-284">为 Invoke-AzureRmVMRunCommand cmdelt 增加了 ResourceId 参数</span><span class="sxs-lookup"><span data-stu-id="d15b5-284">Add ResourceId parameter to Invoke-AzureRmVMRunCommand cmdelt</span></span>
* <span data-ttu-id="d15b5-285">增加了 Invoke-AzureRmVmssVMRunCommand cmdlet</span><span class="sxs-lookup"><span data-stu-id="d15b5-285">Add Invoke-AzureRmVmssVMRunCommand cmdlet</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="d15b5-286">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="d15b5-286">AzureRM.Dns</span></span>
* <span data-ttu-id="d15b5-287">增加了在创建 dns 记录期间对别名记录的支持</span><span class="sxs-lookup"><span data-stu-id="d15b5-287">Added support for alias record during dns record creation</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="d15b5-288">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="d15b5-288">AzureRM.Insights</span></span>
* <span data-ttu-id="d15b5-289">修复了问题 #6833 和 #7102（诊断设置方面）</span><span class="sxs-lookup"><span data-stu-id="d15b5-289">Fixed issues #6833 and #7102 (Diagnostic Settings area)</span></span>
    - <span data-ttu-id="d15b5-290">在创建和列出/获取诊断设置期间出现的默认名称（即“service”）的问题</span><span class="sxs-lookup"><span data-stu-id="d15b5-290">Issues with the default name, i.e. 'service', during creation and listing/getting of diagnostic settings</span></span>
    - <span data-ttu-id="d15b5-291">通过类别创建诊断设置的问题</span><span class="sxs-lookup"><span data-stu-id="d15b5-291">Issues creating diagnostic settings with categories</span></span>
* <span data-ttu-id="d15b5-292">为指标时间粒度参数添加了弃用消息</span><span class="sxs-lookup"><span data-stu-id="d15b5-292">Added deprecation message for metrics time grains parameters</span></span>
    - <span data-ttu-id="d15b5-293">Timegrains 参数仍然会被接受（这是非重大变更），但在后端会被忽略，因为仅 PT1M 有效</span><span class="sxs-lookup"><span data-stu-id="d15b5-293">Timegrains parameters are still being accepted (this is a non-breaking change,) but they are ignored in the backend since only PT1M is valid</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="d15b5-294">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="d15b5-294">AzureRM.Network</span></span>
* <span data-ttu-id="d15b5-295">更改了 LoadBalancer cmdlet</span><span class="sxs-lookup"><span data-stu-id="d15b5-295">Changes to LoadBalancer cmdlets</span></span>
  - <span data-ttu-id="d15b5-296">LoadBalancerInboundNatPoolConfig：增加了 IdleTimeoutInMinutes、EnableFloatingIp 和 EnableTcpReset 参数</span><span class="sxs-lookup"><span data-stu-id="d15b5-296">LoadBalancerInboundNatPoolConfig: added parameters IdleTimeoutInMinutes, EnableFloatingIp and EnableTcpReset</span></span>
  - <span data-ttu-id="d15b5-297">LoadBalancerInboundNatRuleConfig：增加了 EnableTcpReset 参数</span><span class="sxs-lookup"><span data-stu-id="d15b5-297">LoadBalancerInboundNatRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="d15b5-298">LoadBalancerRuleConfig：增加了 EnableTcpReset 参数</span><span class="sxs-lookup"><span data-stu-id="d15b5-298">LoadBalancerRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="d15b5-299">LoadBalancerProbeConfig：增加了对参数 Protocol 的“Https”值的支持</span><span class="sxs-lookup"><span data-stu-id="d15b5-299">LoadBalancerProbeConfig: added support for value "Https" for parameter Protocol</span></span>
* <span data-ttu-id="d15b5-300">为新 LoadBalancer 的子资源 OutboundRule 增加了新命令</span><span class="sxs-lookup"><span data-stu-id="d15b5-300">Added new commands for new LoadBalancer's subresource OutboundRule</span></span>
  - <span data-ttu-id="d15b5-301">Add-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d15b5-301">Add-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="d15b5-302">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d15b5-302">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="d15b5-303">New-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d15b5-303">New-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="d15b5-304">Set-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d15b5-304">Set-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="d15b5-305">Remove-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d15b5-305">Remove-AzureRmLoadBalancerOutboundRuleConfig</span></span>
* <span data-ttu-id="d15b5-306">为 PSNetworkInterface 增加了新的 HostedWorkloads 属性</span><span class="sxs-lookup"><span data-stu-id="d15b5-306">Added new HostedWorkloads property for PSNetworkInterface</span></span>
* <span data-ttu-id="d15b5-307">通过 ARM 为 Azure 防火墙功能增加了新的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="d15b5-307">Added new cmdlets for feature: Azure Firewall via ARM</span></span>
  - <span data-ttu-id="d15b5-308">增加了 Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="d15b5-308">Added Get-AzureRmFirewall</span></span>
  - <span data-ttu-id="d15b5-309">增加了 Set-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="d15b5-309">Added Set-AzureRmFirewall</span></span>
  - <span data-ttu-id="d15b5-310">增加了 New-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="d15b5-310">Added New-AzureRmFirewall</span></span>
  - <span data-ttu-id="d15b5-311">增加了 Remove-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="d15b5-311">Added Remove-AzureRmFirewall</span></span>
  - <span data-ttu-id="d15b5-312">增加了 New-AzureRmFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="d15b5-312">Added New-AzureRmFirewallApplicationRuleCollection</span></span>
  - <span data-ttu-id="d15b5-313">增加了 New-AzureRmFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="d15b5-313">Added New-AzureRmFirewallApplicationRule</span></span>
  - <span data-ttu-id="d15b5-314">增加了 New-AzureRmFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="d15b5-314">Added New-AzureRmFirewallNatRuleCollection</span></span>
  - <span data-ttu-id="d15b5-315">增加了 New-AzureRmFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="d15b5-315">Added New-AzureRmFirewallNatRule</span></span>
  - <span data-ttu-id="d15b5-316">增加了 New-AzureRmFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="d15b5-316">Added New-AzureRmFirewallNetworkRuleCollection</span></span>
  - <span data-ttu-id="d15b5-317">增加了 New-AzureRmFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="d15b5-317">Added New-AzureRmFirewallNetworkRule</span></span>
* <span data-ttu-id="d15b5-318">在应用程序网关中增加了对受信任根证书和自动缩放配置的支持</span><span class="sxs-lookup"><span data-stu-id="d15b5-318">Added support for Trusted Root certificate and Autoscale configuration in Application Gateway</span></span>
  - <span data-ttu-id="d15b5-319">增加了新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="d15b5-319">New Cmdlets added:</span></span>
      - <span data-ttu-id="d15b5-320">Add-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="d15b5-320">Add-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="d15b5-321">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="d15b5-321">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="d15b5-322">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="d15b5-322">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="d15b5-323">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="d15b5-323">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="d15b5-324">Set-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="d15b5-324">Set-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="d15b5-325">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="d15b5-325">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="d15b5-326">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="d15b5-326">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="d15b5-327">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="d15b5-327">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="d15b5-328">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="d15b5-328">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
  - <span data-ttu-id="d15b5-329">使用可选参数 -TrustedRootCertificate 更新了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d15b5-329">Cmdlets updated with optonal parameter -TrustedRootCertificate</span></span>
      - <span data-ttu-id="d15b5-330">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d15b5-330">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="d15b5-331">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d15b5-331">Set-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="d15b5-332">New-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="d15b5-332">New-AzureRmApplicationGatewayBackendHttpSetting</span></span>
      - <span data-ttu-id="d15b5-333">Set-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="d15b5-333">Set-AzureRmApplicationGatewayBackendHttpSetting</span></span>
  - <span data-ttu-id="d15b5-334">使用可选参数 -AutoscaleConfiguration 更新了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d15b5-334">Cmdlets updated with optonal parameter -AutoscaleConfiguration</span></span>
      - <span data-ttu-id="d15b5-335">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d15b5-335">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="d15b5-336">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d15b5-336">Set-AzureRmApplicationGateway</span></span>
* <span data-ttu-id="d15b5-337">为接口终结点增加了 cmdlet Get-AzureInterfaceEndpoint</span><span class="sxs-lookup"><span data-stu-id="d15b5-337">Add cmdlet for Interface Endpoint Get-AzureInterfaceEndpoint</span></span>
* <span data-ttu-id="d15b5-338">在子网中增加了对多个地址前缀的支持。</span><span class="sxs-lookup"><span data-stu-id="d15b5-338">Added support for multiple address prefixes in a subnet.</span></span> <span data-ttu-id="d15b5-339">更新了 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="d15b5-339">Updated cmdlets:</span></span>
  - <span data-ttu-id="d15b5-340">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="d15b5-340">New-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="d15b5-341">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="d15b5-341">Set-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="d15b5-342">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="d15b5-342">Add-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="d15b5-343">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="d15b5-343">Get-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="d15b5-344">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="d15b5-344">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>
  - <span data-ttu-id="d15b5-345">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="d15b5-345">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="d15b5-346">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="d15b5-346">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="d15b5-347">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="d15b5-347">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="d15b5-348">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="d15b5-348">Add-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="d15b5-349">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="d15b5-349">New-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="d15b5-350">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="d15b5-350">Set-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="d15b5-351">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="d15b5-351">Add-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="d15b5-352">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="d15b5-352">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="d15b5-353">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="d15b5-353">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="d15b5-354">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="d15b5-354">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="d15b5-355">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="d15b5-355">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="d15b5-356">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="d15b5-356">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="d15b5-357">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="d15b5-357">New-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="d15b5-358">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d15b5-358">New-AzureRmNetworkInterface</span></span>
* <span data-ttu-id="d15b5-359">增加了用于子网委派的 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d15b5-359">Adding cmdlets for subnet delegation.</span></span>
  - <span data-ttu-id="d15b5-360">New-AzureRmDelegation：创建一个可以添加到子网的新委派</span><span class="sxs-lookup"><span data-stu-id="d15b5-360">New-AzureRmDelegation: Creates a new delegation, which can be added to a subnet</span></span>
  - <span data-ttu-id="d15b5-361">Remove-AzureRmDelegation：获取一个子网，然后从该子网中删除提供的委派名称</span><span class="sxs-lookup"><span data-stu-id="d15b5-361">Remove-AzureRmDelegation: Takes in a subnet and removes the provided delegation name from that subnet</span></span>
  - <span data-ttu-id="d15b5-362">Add-AzureRmDelegation：获取一个子网，然后向该子网添加提供的服务名称作为委派</span><span class="sxs-lookup"><span data-stu-id="d15b5-362">Add-AzureRmDelegation: Takes in a subnet and adds the provided service name as a delegation to that subnet</span></span>
  - <span data-ttu-id="d15b5-363">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="d15b5-363">Get-AzureRmDelegation</span></span>
  - <span data-ttu-id="d15b5-364">Get-AzureRmAvailableServiceDelegations</span><span class="sxs-lookup"><span data-stu-id="d15b5-364">Get-AzureRmAvailableServiceDelegations</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="d15b5-365">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="d15b5-365">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="d15b5-366">支持托管磁盘</span><span class="sxs-lookup"><span data-stu-id="d15b5-366">Support for managed Managed disk</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="d15b5-367">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="d15b5-367">AzureRM.RedisCache</span></span>
* <span data-ttu-id="d15b5-368">更新了 Insights 依赖项。</span><span class="sxs-lookup"><span data-stu-id="d15b5-368">Updated Insights dependency.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="d15b5-369">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="d15b5-369">AzureRM.Resources</span></span>
* <span data-ttu-id="d15b5-370">使用新参数 RollbackAction 更新了 New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d15b5-370">Update New-AzureRmResourceGroupDeployment with new parameter RollbackAction</span></span>
    - <span data-ttu-id="d15b5-371">使用新参数增加了对 OnErrorDeployment 的支持。</span><span class="sxs-lookup"><span data-stu-id="d15b5-371">Add support for OnErrorDeployment with the new parameter.</span></span>
* <span data-ttu-id="d15b5-372">在策略分配方面支持托管标识。</span><span class="sxs-lookup"><span data-stu-id="d15b5-372">Support managed identity on policy assignments.</span></span>
* <span data-ttu-id="d15b5-373">使用“New-AzureRmPolicyAssignment”来分配策略时，不再需要带默认值的参数</span><span class="sxs-lookup"><span data-stu-id="d15b5-373">Parameters with default values are no longer requred when assigning a policy with 'New-AzureRmPolicyAssignment'</span></span>
* <span data-ttu-id="d15b5-374">增加了新的 cmdlet Get-AzureRmPolicyAlias，用于检索策略别名</span><span class="sxs-lookup"><span data-stu-id="d15b5-374">Add new cmdlet Get-AzureRmPolicyAlias for retrieving policy aliases</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="d15b5-375">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d15b5-375">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="d15b5-376">修复了问题 #7161</span><span class="sxs-lookup"><span data-stu-id="d15b5-376">Fixed issue #7161</span></span>

#### <a name="azurermsignalr"></a><span data-ttu-id="d15b5-377">AzureRM.SignalR</span><span class="sxs-lookup"><span data-stu-id="d15b5-377">AzureRM.SignalR</span></span>
* <span data-ttu-id="d15b5-378">将 SKU 名称更新为 Free_F1 和 Standard_S1</span><span class="sxs-lookup"><span data-stu-id="d15b5-378">Update SKU names to Free_F1 and Standard_S1</span></span>
* <span data-ttu-id="d15b5-379">为 PSSignalRResource 对象增加了版本字段，为 PSSignalRKeys 对象增加了字符串。</span><span class="sxs-lookup"><span data-stu-id="d15b5-379">Add version field to the PSSignalRResource object and connection string to the PSSignalRKeys object.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="d15b5-380">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="d15b5-380">AzureRM.Storage</span></span>
* <span data-ttu-id="d15b5-381">在 AzureRm.Storage 中支持不可变性策略</span><span class="sxs-lookup"><span data-stu-id="d15b5-381">Support Immutability Policy in AzureRm.Storage</span></span> 
    - <span data-ttu-id="d15b5-382">Remove-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="d15b5-382">Remove-AzureRmStorageAccountNetworkRule</span></span>
    - <span data-ttu-id="d15b5-383">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="d15b5-383">Get-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="d15b5-384">Update-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="d15b5-384">Update-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="d15b5-385">New-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="d15b5-385">New-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="d15b5-386">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="d15b5-386">Remove-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="d15b5-387">Add-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="d15b5-387">Add-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="d15b5-388">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="d15b5-388">Remove-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="d15b5-389">Set-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="d15b5-389">Set-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="d15b5-390">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="d15b5-390">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="d15b5-391">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="d15b5-391">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="d15b5-392">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="d15b5-392">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="d15b5-393">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="d15b5-393">AzureRM.Websites</span></span>
* <span data-ttu-id="d15b5-394">增加了两个新的 cmdlet：Get-AzureRmDeletedWebApp 和 Restore-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="d15b5-394">Added two new cmdlets: Get-AzureRmDeletedWebApp and Restore-AzureRmDeletedWebApp</span></span>
* <span data-ttu-id="d15b5-395">增加了 New-AzureRmAppServicePlan -HyperV 开关，用于通过 Windows 容器创建应用服务计划</span><span class="sxs-lookup"><span data-stu-id="d15b5-395">New-AzureRmAppServicePlan -HyperV switch is added for create app service plan with windows container</span></span>
* <span data-ttu-id="d15b5-396">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - 增加了新参数 (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment)，用于创建和管理 Windows 容器应用</span><span class="sxs-lookup"><span data-stu-id="d15b5-396">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - New parameters (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) added for creating and managing windows container app</span></span>

## <a name="681---august-2018"></a><span data-ttu-id="d15b5-397">6.8.1 - 2018 年 8 月</span><span class="sxs-lookup"><span data-stu-id="d15b5-397">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="d15b5-398">常规</span><span class="sxs-lookup"><span data-stu-id="d15b5-398">General</span></span>
* <span data-ttu-id="d15b5-399">解决了未设置默认资源组的问题。</span><span class="sxs-lookup"><span data-stu-id="d15b5-399">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="d15b5-400">更新了公共运行时程序集</span><span class="sxs-lookup"><span data-stu-id="d15b5-400">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="d15b5-401">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d15b5-401">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="d15b5-402">解决了未设置默认资源组的问题。</span><span class="sxs-lookup"><span data-stu-id="d15b5-402">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="d15b5-403">修复了问题 https://github.com/Azure/azure-powershell/issues/6603</span><span class="sxs-lookup"><span data-stu-id="d15b5-403">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="d15b5-404">Import-AzureRmApiManagementApi 和 \*-AzureRmApiManagementCertificate cmdlet 现在处理相对路径</span><span class="sxs-lookup"><span data-stu-id="d15b5-404">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="d15b5-405">修复了问题 https://github.com/Azure/azure-powershell/issues/6879</span><span class="sxs-lookup"><span data-stu-id="d15b5-405">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="d15b5-406">CertificateInformation 是使 Set-AzureRmApiManagement cmdlet 可以正常工作的可设置属性。</span><span class="sxs-lookup"><span data-stu-id="d15b5-406">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="d15b5-407">通过升级到 4.0.4-preview nuget 进行了修复</span><span class="sxs-lookup"><span data-stu-id="d15b5-407">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="d15b5-408">修复了问题 https://github.com/Azure/azure-powershell/issues/6853</span><span class="sxs-lookup"><span data-stu-id="d15b5-408">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="d15b5-409">针对按产品名称进行的搜索修复了 Odata 筛选器</span><span class="sxs-lookup"><span data-stu-id="d15b5-409">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="d15b5-410">修复了问题 https://github.com/Azure/azure-powershell/issues/6814</span><span class="sxs-lookup"><span data-stu-id="d15b5-410">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="d15b5-411">针对按 API 名称进行的搜索修复了 Odata 筛选器</span><span class="sxs-lookup"><span data-stu-id="d15b5-411">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="d15b5-412">添加了对 AzureMonitor 记录器的支持</span><span class="sxs-lookup"><span data-stu-id="d15b5-412">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="d15b5-413">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="d15b5-413">AzureRM.Compute</span></span>
* <span data-ttu-id="d15b5-414">解决了错误输出中缺少目标的问题。</span><span class="sxs-lookup"><span data-stu-id="d15b5-414">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="d15b5-415">解决了带有托管磁盘的 VM 的存储帐户类型问题</span><span class="sxs-lookup"><span data-stu-id="d15b5-415">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="d15b5-416">解决了未设置默认资源组的问题。</span><span class="sxs-lookup"><span data-stu-id="d15b5-416">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="d15b5-417">解决了在其他环境（例如 Azure 中国）中使用 AEM 扩展 cmdlet 的问题</span><span class="sxs-lookup"><span data-stu-id="d15b5-417">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="d15b5-418">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="d15b5-418">AzureRM.Network</span></span>
* <span data-ttu-id="d15b5-419">将默认 cmdlet 输出表示形式更改为表视图</span><span class="sxs-lookup"><span data-stu-id="d15b5-419">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="d15b5-420">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="d15b5-420">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="d15b5-421">修复了在尝试扩展停用的容量时 Update-AzureRmPowerBIEmbeddedCapacity 中出现的故障</span><span class="sxs-lookup"><span data-stu-id="d15b5-421">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="d15b5-422">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="d15b5-422">AzureRM.Resources</span></span>
* <span data-ttu-id="d15b5-423">解决了从市场创建托管应用程序的问题。</span><span class="sxs-lookup"><span data-stu-id="d15b5-423">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="d15b5-424">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d15b5-424">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="d15b5-425">修复的问题</span><span class="sxs-lookup"><span data-stu-id="d15b5-425">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="d15b5-426">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="d15b5-426">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="d15b5-427">添加了对 MultiValue 路由方法的支持</span><span class="sxs-lookup"><span data-stu-id="d15b5-427">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="d15b5-428">MultiValue 路由的新参数“MaxReturn”</span><span class="sxs-lookup"><span data-stu-id="d15b5-428">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="d15b5-429">添加了对 Subnet 路由方法的支持</span><span class="sxs-lookup"><span data-stu-id="d15b5-429">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="d15b5-430">对终结点中的 IP 地址范围（子网）的支持</span><span class="sxs-lookup"><span data-stu-id="d15b5-430">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="d15b5-431">添加了对配置文件中的自定义标头的支持</span><span class="sxs-lookup"><span data-stu-id="d15b5-431">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="d15b5-432">添加了对配置文件中的预期状态代码范围的支持</span><span class="sxs-lookup"><span data-stu-id="d15b5-432">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="d15b5-433">添加了对终结点中的自定义标头的支持</span><span class="sxs-lookup"><span data-stu-id="d15b5-433">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="d15b5-434">6.8.0 - 2018 年 8 月</span><span class="sxs-lookup"><span data-stu-id="d15b5-434">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="d15b5-435">常规</span><span class="sxs-lookup"><span data-stu-id="d15b5-435">General</span></span>
* <span data-ttu-id="d15b5-436">解决了未设置默认资源组的问题。</span><span class="sxs-lookup"><span data-stu-id="d15b5-436">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="d15b5-437">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="d15b5-437">AzureRM.Profile</span></span>
* <span data-ttu-id="d15b5-438">为在执行 Connect-AzureRmAccount 期间返回的令牌添加了“过期”属性</span><span class="sxs-lookup"><span data-stu-id="d15b5-438">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="d15b5-439">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="d15b5-439">AzureRM.Compute</span></span>
* <span data-ttu-id="d15b5-440">解决了错误输出中缺少目标的问题。</span><span class="sxs-lookup"><span data-stu-id="d15b5-440">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="d15b5-441">解决了带有托管磁盘的 VM 的存储帐户类型问题</span><span class="sxs-lookup"><span data-stu-id="d15b5-441">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="d15b5-442">解决了在其他环境（例如 Azure 中国）中使用 AEM 扩展 cmdlet 的问题</span><span class="sxs-lookup"><span data-stu-id="d15b5-442">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="d15b5-443">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="d15b5-443">AzureRM.IotHub</span></span>
* <span data-ttu-id="d15b5-444">修复了 New-AzureRmIotHubExportDevices 和 New-AzureRmIotHubImportDevices的示例</span><span class="sxs-lookup"><span data-stu-id="d15b5-444">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="d15b5-445">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="d15b5-445">AzureRM.Network</span></span>
* <span data-ttu-id="d15b5-446">将默认模型表示形式更改为表视图</span><span class="sxs-lookup"><span data-stu-id="d15b5-446">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="d15b5-447">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="d15b5-447">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="d15b5-448">修复了在尝试扩展停用的容量时 Update-AzureRmPowerBIEmbeddedCapacity 中出现的故障</span><span class="sxs-lookup"><span data-stu-id="d15b5-448">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="d15b5-449">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="d15b5-449">AzureRM.Resources</span></span>
* <span data-ttu-id="d15b5-450">解决了从市场创建托管应用程序的问题。</span><span class="sxs-lookup"><span data-stu-id="d15b5-450">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="d15b5-451">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d15b5-451">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="d15b5-452">解决了以下问题</span><span class="sxs-lookup"><span data-stu-id="d15b5-452">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="d15b5-453">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="d15b5-453">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="d15b5-454">对 MultiValue 路由方法的支持</span><span class="sxs-lookup"><span data-stu-id="d15b5-454">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="d15b5-455">MultiValue 路由的新参数“MaxReturn”</span><span class="sxs-lookup"><span data-stu-id="d15b5-455">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="d15b5-456">对 Subnet 路由方法的支持</span><span class="sxs-lookup"><span data-stu-id="d15b5-456">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="d15b5-457">对终结点中的 IP 地址范围（子网）的支持</span><span class="sxs-lookup"><span data-stu-id="d15b5-457">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="d15b5-458">对配置文件中的自定义标头的支持</span><span class="sxs-lookup"><span data-stu-id="d15b5-458">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="d15b5-459">对配置文件中的预期状态代码范围的支持</span><span class="sxs-lookup"><span data-stu-id="d15b5-459">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="d15b5-460">对终结点中的自定义标头的支持</span><span class="sxs-lookup"><span data-stu-id="d15b5-460">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="d15b5-461">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="d15b5-461">AzureRM.Websites</span></span>
* <span data-ttu-id="d15b5-462">解决了错误地设置默认资源组的问题。</span><span class="sxs-lookup"><span data-stu-id="d15b5-462">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="d15b5-463">6.7.0 - 2018 年 8 月</span><span class="sxs-lookup"><span data-stu-id="d15b5-463">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="d15b5-464">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="d15b5-464">AzureRM.Profile</span></span>
* <span data-ttu-id="d15b5-465">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="d15b5-465">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="d15b5-466">向默认的上下文名称添加用户 ID，避免上下文冲突</span><span class="sxs-lookup"><span data-stu-id="d15b5-466">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="d15b5-467">修复了 Clear-AzureRmContext 在选择上下文 #6398 时出现的问题</span><span class="sxs-lookup"><span data-stu-id="d15b5-467">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="d15b5-468">允许将租户域传递给“Connect-AzureRmAccount”的“-TenantId”参数</span><span class="sxs-lookup"><span data-stu-id="d15b5-468">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="d15b5-469">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="d15b5-469">Azure.Storage</span></span>
* <span data-ttu-id="d15b5-470">去除了 Azure 文件共享配额的 5TB 限制</span><span class="sxs-lookup"><span data-stu-id="d15b5-470">Remove the 5TB limitation for Azure File Share quota</span></span>
* <span data-ttu-id="d15b5-471">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="d15b5-471">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="d15b5-472">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="d15b5-472">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="d15b5-473">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="d15b5-473">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="d15b5-474">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="d15b5-474">Azure.AnalysisServices</span></span>
* <span data-ttu-id="d15b5-475">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="d15b5-475">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="d15b5-476">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d15b5-476">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="d15b5-477">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="d15b5-477">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="d15b5-478">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="d15b5-478">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="d15b5-479">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="d15b5-479">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="d15b5-480">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="d15b5-480">AzureRM.Automation</span></span>
* <span data-ttu-id="d15b5-481">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="d15b5-481">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="d15b5-482">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="d15b5-482">AzureRM.Backup</span></span>
* <span data-ttu-id="d15b5-483">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="d15b5-483">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="d15b5-484">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="d15b5-484">AzureRM.Batch</span></span>
* <span data-ttu-id="d15b5-485">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="d15b5-485">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="d15b5-486">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="d15b5-486">AzureRM.Billing</span></span>
* <span data-ttu-id="d15b5-487">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="d15b5-487">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="d15b5-488">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="d15b5-488">AzureRM.Cdn</span></span>
* <span data-ttu-id="d15b5-489">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="d15b5-489">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="d15b5-490">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d15b5-490">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="d15b5-491">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="d15b5-491">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="d15b5-492">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="d15b5-492">AzureRM.Compute</span></span>
* <span data-ttu-id="d15b5-493">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="d15b5-493">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="d15b5-494">为 New-AzureRmVmssConfig 增加了 EvictionPolicy 参数</span><span class="sxs-lookup"><span data-stu-id="d15b5-494">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="d15b5-495">在 New-AzureRmVm 的 DiskFileParameterSet 中使用默认位置（如果未指定 Location）</span><span class="sxs-lookup"><span data-stu-id="d15b5-495">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="d15b5-496">修复了 Save-AzureRmVMImage 中的参数说明</span><span class="sxs-lookup"><span data-stu-id="d15b5-496">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="d15b5-497">修复了某些单次传递相关方案的 Get-AzureRmVMDiskEncryptionStatus cmdlet</span><span class="sxs-lookup"><span data-stu-id="d15b5-497">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="d15b5-498">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="d15b5-498">AzureRM.Consumption</span></span>
* <span data-ttu-id="d15b5-499">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="d15b5-499">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="d15b5-500">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="d15b5-500">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="d15b5-501">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="d15b5-501">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="d15b5-502">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d15b5-502">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="d15b5-503">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="d15b5-503">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="d15b5-504">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="d15b5-504">AzureRM.DataFactories</span></span>
* <span data-ttu-id="d15b5-505">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="d15b5-505">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="d15b5-506">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="d15b5-506">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="d15b5-507">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="d15b5-507">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="d15b5-508">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="d15b5-508">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="d15b5-509">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="d15b5-509">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="d15b5-510">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d15b5-510">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="d15b5-511">修复了从 PowerShell 命令行设置 DebugPreference 时的调试问题</span><span class="sxs-lookup"><span data-stu-id="d15b5-511">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="d15b5-512">更新了 Set-AzureRmDataLakeStoreItemAcl 的示例</span><span class="sxs-lookup"><span data-stu-id="d15b5-512">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="d15b5-513">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="d15b5-513">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="d15b5-514">更新了 Set-AzureRmDataLakeStoreItemAclEntry 的示例</span><span class="sxs-lookup"><span data-stu-id="d15b5-514">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="d15b5-515">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="d15b5-515">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="d15b5-516">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="d15b5-516">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="d15b5-517">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="d15b5-517">AzureRM.Dns</span></span>
* <span data-ttu-id="d15b5-518">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="d15b5-518">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="d15b5-519">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="d15b5-519">AzureRM.EventGrid</span></span>
* <span data-ttu-id="d15b5-520">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="d15b5-520">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="d15b5-521">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="d15b5-521">AzureRM.EventHub</span></span>
* <span data-ttu-id="d15b5-522">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="d15b5-522">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="d15b5-523">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d15b5-523">AzureRM.HDInsight</span></span>
* <span data-ttu-id="d15b5-524">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="d15b5-524">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="d15b5-525">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="d15b5-525">AzureRM.Insights</span></span>
* <span data-ttu-id="d15b5-526">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="d15b5-526">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="d15b5-527">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="d15b5-527">AzureRM.IotHub</span></span>
* <span data-ttu-id="d15b5-528">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="d15b5-528">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="d15b5-529">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d15b5-529">AzureRM.KeyVault</span></span>
* <span data-ttu-id="d15b5-530">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="d15b5-530">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="d15b5-531">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="d15b5-531">AzureRM.LogicApp</span></span>
* <span data-ttu-id="d15b5-532">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="d15b5-532">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="d15b5-533">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="d15b5-533">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="d15b5-534">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="d15b5-534">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="d15b5-535">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="d15b5-535">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="d15b5-536">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="d15b5-536">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="d15b5-537">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="d15b5-537">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="d15b5-538">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="d15b5-538">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="d15b5-539">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="d15b5-539">AzureRM.Media</span></span>
* <span data-ttu-id="d15b5-540">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="d15b5-540">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="d15b5-541">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="d15b5-541">AzureRM.Network</span></span>
* <span data-ttu-id="d15b5-542">增加了 Set-AzureRmLocalNetworkGateway 的示例</span><span class="sxs-lookup"><span data-stu-id="d15b5-542">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="d15b5-543">增加了 Add-AzureRmVirtualNetworkGatewayIpConfig、Get-AzureRmVirtualNetworkGatewayConnectionSharedKey 和 New-AzureRmVirtualNetworkGatewayConnection 的示例和说明</span><span class="sxs-lookup"><span data-stu-id="d15b5-543">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="d15b5-544">增加了 Remove-AzureRmVirtualNetworkGatewayIpConfig 和 Reset-AzureRmVirtualNetworkGateway 的示例</span><span class="sxs-lookup"><span data-stu-id="d15b5-544">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="d15b5-545">增加了 Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey 的示例</span><span class="sxs-lookup"><span data-stu-id="d15b5-545">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="d15b5-546">增加了 Set-AzureRmVirtualNetworkGatewayConnectionSharedKey 的示例</span><span class="sxs-lookup"><span data-stu-id="d15b5-546">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="d15b5-547">增加了 Set-AzureRmVirtualNetworkGatewayConnection 的示例</span><span class="sxs-lookup"><span data-stu-id="d15b5-547">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="d15b5-548">使用最新的代码生成器重新生成了 ApplicationSecurityGroup、RouteTable 和 Usage 的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="d15b5-548">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="d15b5-549">阐明了在尝试获取的子网不存在时 Get-AzureRmVirtualNetworkSubnetConfig 的错误消息</span><span class="sxs-lookup"><span data-stu-id="d15b5-549">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="d15b5-550">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="d15b5-550">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="d15b5-551">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="d15b5-551">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="d15b5-552">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d15b5-552">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="d15b5-553">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="d15b5-553">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="d15b5-554">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="d15b5-554">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="d15b5-555">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="d15b5-555">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="d15b5-556">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="d15b5-556">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="d15b5-557">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="d15b5-557">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="d15b5-558">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d15b5-558">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="d15b5-559">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="d15b5-559">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="d15b5-560">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="d15b5-560">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="d15b5-561">为 Get-AzureRmRecoveryServicesBackItem cmdlet 增加了策略筛选器。</span><span class="sxs-lookup"><span data-stu-id="d15b5-561">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="d15b5-562">此命令返回受给定策略 ID 保护的备份项的列表。</span><span class="sxs-lookup"><span data-stu-id="d15b5-562">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="d15b5-563">已将 Microsoft.Azure.Management.RecoveryServices.Backup 更新到 3.0.0-preview 版本。</span><span class="sxs-lookup"><span data-stu-id="d15b5-563">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="d15b5-564">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="d15b5-564">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="d15b5-565">为 Restore-AzureRmRecoveryServicesBackupItem 增加了 TargetResourceGroupName 参数。</span><span class="sxs-lookup"><span data-stu-id="d15b5-565">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="d15b5-566">托管磁盘还原到的资源组。</span><span class="sxs-lookup"><span data-stu-id="d15b5-566">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="d15b5-567">适用于包含托管磁盘的 VM 的备份。</span><span class="sxs-lookup"><span data-stu-id="d15b5-567">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="d15b5-568">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="d15b5-568">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="d15b5-569">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="d15b5-569">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="d15b5-570">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="d15b5-570">AzureRM.RedisCache</span></span>
* <span data-ttu-id="d15b5-571">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="d15b5-571">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="d15b5-572">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="d15b5-572">AzureRM.Relay</span></span>
* <span data-ttu-id="d15b5-573">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="d15b5-573">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="d15b5-574">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="d15b5-574">AzureRM.Resources</span></span>
* <span data-ttu-id="d15b5-575">支持在订阅范围部署模板。</span><span class="sxs-lookup"><span data-stu-id="d15b5-575">Support template deployment at subscription scope.</span></span> <span data-ttu-id="d15b5-576">增加了新 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="d15b5-576">Add new Cmdlets:</span></span>
    - <span data-ttu-id="d15b5-577">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="d15b5-577">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="d15b5-578">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="d15b5-578">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="d15b5-579">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="d15b5-579">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="d15b5-580">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="d15b5-580">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="d15b5-581">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="d15b5-581">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="d15b5-582">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="d15b5-582">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="d15b5-583">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="d15b5-583">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="d15b5-584">修复了在将上下文传递给 Set-AzureRmResource 时引发错误的问题</span><span class="sxs-lookup"><span data-stu-id="d15b5-584">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="d15b5-585">修复了 New-AzureRmResourceGroupDeployment 中的示例</span><span class="sxs-lookup"><span data-stu-id="d15b5-585">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="d15b5-586">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="d15b5-586">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="d15b5-587">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="d15b5-587">AzureRM.Scheduler</span></span>
* <span data-ttu-id="d15b5-588">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="d15b5-588">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="d15b5-589">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d15b5-589">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="d15b5-590">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="d15b5-590">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="d15b5-591">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d15b5-591">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="d15b5-592">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="d15b5-592">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="d15b5-593">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="d15b5-593">AzureRM.Sql</span></span>
* <span data-ttu-id="d15b5-594">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="d15b5-594">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="d15b5-595">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="d15b5-595">AzureRM.Storage</span></span>
* <span data-ttu-id="d15b5-596">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="d15b5-596">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="d15b5-597">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="d15b5-597">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="d15b5-598">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="d15b5-598">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="d15b5-599">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="d15b5-599">AzureRM.Tags</span></span>
* <span data-ttu-id="d15b5-600">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="d15b5-600">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="d15b5-601">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="d15b5-601">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="d15b5-602">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="d15b5-602">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="d15b5-603">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="d15b5-603">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="d15b5-604">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="d15b5-604">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="d15b5-605">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="d15b5-605">AzureRM.Websites</span></span>
* <span data-ttu-id="d15b5-606">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="d15b5-606">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="d15b5-607">6.6.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="d15b5-607">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="d15b5-608">常规</span><span class="sxs-lookup"><span data-stu-id="d15b5-608">General</span></span>
* <span data-ttu-id="d15b5-609">更新了所有帮助文件，以包括完整参数类型和正确的输入/输出类型。</span><span class="sxs-lookup"><span data-stu-id="d15b5-609">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="d15b5-610">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="d15b5-610">AzureRM.Profile</span></span>
* <span data-ttu-id="d15b5-611">更新了 Common.Strategy 库，以便能够验证资源的当前配置是否与目标资源兼容。</span><span class="sxs-lookup"><span data-stu-id="d15b5-611">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="d15b5-612">在 Common.Storage 中添加了 ps1xml 类型</span><span class="sxs-lookup"><span data-stu-id="d15b5-612">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="d15b5-613">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="d15b5-613">Azure.Storage</span></span>
* <span data-ttu-id="d15b5-614">增加了从 DefaultProfile 获取存储上下文的支持</span><span class="sxs-lookup"><span data-stu-id="d15b5-614">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="d15b5-615">为 cmdlet 输出类型属性增加了 Ps1XmlAttribute。</span><span class="sxs-lookup"><span data-stu-id="d15b5-615">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="d15b5-616">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d15b5-616">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="d15b5-617">修复了问题 https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="d15b5-617">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="d15b5-618">修复了 Automapper 中将 PsApiManagementApi 转换为 ApiContract 的 bug</span><span class="sxs-lookup"><span data-stu-id="d15b5-618">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="d15b5-619">修复了问题 https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="d15b5-619">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="d15b5-620">修复了 File.Save 中没有使用编码类型重载的 bug</span><span class="sxs-lookup"><span data-stu-id="d15b5-620">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="d15b5-621">修复了问题 https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="d15b5-621">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="d15b5-622">升级到了 4.0.3 Nuget版本，该版本修复了 apiId 上的模式异常</span><span class="sxs-lookup"><span data-stu-id="d15b5-622">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="d15b5-623">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="d15b5-623">AzureRM.Compute</span></span>
* <span data-ttu-id="d15b5-624">修复因使用 PremiumLRS 存储帐户类型重命名而在 New-AzureRmVm 中使用 DiskFileParameterSet 创建 VM 失败的问题。</span><span class="sxs-lookup"><span data-stu-id="d15b5-624">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="d15b5-625">修复 Invoke-AzureRmVMRunCommand cmdlet</span><span class="sxs-lookup"><span data-stu-id="d15b5-625">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="d15b5-626">更新 Get-AzureRmAvailabilitySet 以启用列出订阅中的所有可用性集。</span><span class="sxs-lookup"><span data-stu-id="d15b5-626">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="d15b5-627">（ResouceGroupName 参数现在是可选的。）</span><span class="sxs-lookup"><span data-stu-id="d15b5-627">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="d15b5-628">更新“New-AzureRmVm”的 SimpleParameterSet 以在符合条件的 VM 上启用加速网络。</span><span class="sxs-lookup"><span data-stu-id="d15b5-628">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="d15b5-629">将 New-AzureRmVmss 简单参数集更新为在用户指定的 LB 已存在时创建 vmss 失败。</span><span class="sxs-lookup"><span data-stu-id="d15b5-629">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="d15b5-630">更新 New-AzureRmDisk 的示例</span><span class="sxs-lookup"><span data-stu-id="d15b5-630">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="d15b5-631">添加“New-AzureRmVM”的示例</span><span class="sxs-lookup"><span data-stu-id="d15b5-631">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="d15b5-632">更新 Set-AzureRmVMOSDisk 的说明</span><span class="sxs-lookup"><span data-stu-id="d15b5-632">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="d15b5-633">更新 Set-AzureRmVMBginfoExtension 的示例 1 以更正拼写和前缀。</span><span class="sxs-lookup"><span data-stu-id="d15b5-633">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="d15b5-634">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="d15b5-634">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="d15b5-635">将 ADF .Net SDK 版本更新为 1.1.0。</span><span class="sxs-lookup"><span data-stu-id="d15b5-635">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="d15b5-636">支持跨数据工厂的自承载集成运行时共享。</span><span class="sxs-lookup"><span data-stu-id="d15b5-636">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="d15b5-637">将新参数 -SharedIntegrationRuntimeResourceId 添加到 Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d15b5-637">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="d15b5-638">将新的可选参数 -LinkedDataFactoryName 添加到 Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d15b5-638">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="d15b5-639">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d15b5-639">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="d15b5-640">将数据平面 SDK (Microsoft.Azure.DataLake.Store) 版本更新为 1.1.9</span><span class="sxs-lookup"><span data-stu-id="d15b5-640">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="d15b5-641">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="d15b5-641">AzureRM.EventHub</span></span>
* <span data-ttu-id="d15b5-642">在删除 cmdlet 中更新了 InputObject 和 ResourceId 的管道</span><span class="sxs-lookup"><span data-stu-id="d15b5-642">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="d15b5-643">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="d15b5-643">AzureRM.Insights</span></span>
* <span data-ttu-id="d15b5-644">修复了帮助文件中 OutputType 的格式问题</span><span class="sxs-lookup"><span data-stu-id="d15b5-644">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="d15b5-645">使用 Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span><span class="sxs-lookup"><span data-stu-id="d15b5-645">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="d15b5-646">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d15b5-646">AzureRM.KeyVault</span></span>
* <span data-ttu-id="d15b5-647">修复了 Set-AzureRmKeyVaultAccessPolicy 中的管道问题</span><span class="sxs-lookup"><span data-stu-id="d15b5-647">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="d15b5-648">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="d15b5-648">AzureRM.Network</span></span>
* <span data-ttu-id="d15b5-649">添加了 LoadBalancerInboundNatPoolConfig cmdlet 的示例。</span><span class="sxs-lookup"><span data-stu-id="d15b5-649">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="d15b5-650">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="d15b5-650">AzureRM.Resources</span></span>
* <span data-ttu-id="d15b5-651">修复了为“Get-AzureRmResource”同时提供标记名称和值时出现的问题</span><span class="sxs-lookup"><span data-stu-id="d15b5-651">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="d15b5-652">使用“Set-AzureRmResource”修复管道方案</span><span class="sxs-lookup"><span data-stu-id="d15b5-652">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="d15b5-653">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d15b5-653">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="d15b5-654">在删除 cmdlet 中更新了 InputObject 和 ResourceId 的管道</span><span class="sxs-lookup"><span data-stu-id="d15b5-654">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="d15b5-655">修复了几个问题</span><span class="sxs-lookup"><span data-stu-id="d15b5-655">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="d15b5-656">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="d15b5-656">AzureRM.Sql</span></span>
* <span data-ttu-id="d15b5-657">使用以下 cmdlet 添加服务器高级威胁防护支持：</span><span class="sxs-lookup"><span data-stu-id="d15b5-657">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="d15b5-658">Enable-AzureRmSqlServerAdvancedThreatProtection；Disable-AzureRmSqlServerAdvancedThreatProtection；Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d15b5-658">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="d15b5-659">使用以下 cmdlet 添加漏洞评估支持：</span><span class="sxs-lookup"><span data-stu-id="d15b5-659">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="d15b5-660">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings；Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings；Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="d15b5-660">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="d15b5-661">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline；Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline；Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="d15b5-661">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="d15b5-662">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan；Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord；Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="d15b5-662">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="d15b5-663">修复了 Remove-AzureRmSqlServerFirewallRule 中的示例</span><span class="sxs-lookup"><span data-stu-id="d15b5-663">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="d15b5-664">修复了 Get-AzureSqlSyncGroupLog 中非美国基础文化的日期时间处理错误</span><span class="sxs-lookup"><span data-stu-id="d15b5-664">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="d15b5-665">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="d15b5-665">AzureRM.Storage</span></span>
* <span data-ttu-id="d15b5-666">将 Ps1XmlAttribute 添加到 cmdlet 输出类型属性</span><span class="sxs-lookup"><span data-stu-id="d15b5-666">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="d15b5-667">在表视图中显示 StorageAccount cmdlet 输出</span><span class="sxs-lookup"><span data-stu-id="d15b5-667">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="d15b5-668">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d15b5-668">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="d15b5-669">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d15b5-669">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="d15b5-670">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d15b5-670">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="d15b5-671">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="d15b5-671">AzureRM.Tags</span></span>
* <span data-ttu-id="d15b5-672">从 Tag cmdlet 帮助中删除不正确的语句</span><span class="sxs-lookup"><span data-stu-id="d15b5-672">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="d15b5-673">6.5.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="d15b5-673">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="d15b5-674">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="d15b5-674">AzureRM.Profile</span></span>
* <span data-ttu-id="d15b5-675">更新了“Get-AzureRmContextAutosaveSetting”的帮助</span><span class="sxs-lookup"><span data-stu-id="d15b5-675">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="d15b5-676">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="d15b5-676">Azure.Storage</span></span>
* <span data-ttu-id="d15b5-677">支持使用只写 Sas 令牌上传 Blob 或文件</span><span class="sxs-lookup"><span data-stu-id="d15b5-677">Support Upload Blob or File with write only Sas token</span></span>
* <span data-ttu-id="d15b5-678">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="d15b5-678">Set-AzureStorageBlobContent</span></span>
* <span data-ttu-id="d15b5-679">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="d15b5-679">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="d15b5-680">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="d15b5-680">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="d15b5-681">将所需属性 ResourceGroupName 添加到 AS。</span><span class="sxs-lookup"><span data-stu-id="d15b5-681">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="d15b5-682">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="d15b5-682">AzureRM.Automation</span></span>
* <span data-ttu-id="d15b5-683">更新帮助并添加“New-AzureRMAutomationSchedule”的示例</span><span class="sxs-lookup"><span data-stu-id="d15b5-683">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="d15b5-684">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="d15b5-684">AzureRM.Compute</span></span>
* <span data-ttu-id="d15b5-685">将 -Tag 参数添加到 Update/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d15b5-685">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="d15b5-686">添加“Add-AzureRmVmssExtension”的示例</span><span class="sxs-lookup"><span data-stu-id="d15b5-686">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="d15b5-687">添加“Remove-AzureRmVmssExtension”的示例</span><span class="sxs-lookup"><span data-stu-id="d15b5-687">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="d15b5-688">更新“Set-AzureRmVMAccessExtension”的帮助</span><span class="sxs-lookup"><span data-stu-id="d15b5-688">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="d15b5-689">更新 New-AzureRmVmss 的 SimpleParameterSet，以默认情况下将 SinglePlacementGroup 设置为false，并添加开关参数“SinglePlacementGroup”，使用户能够在单个放置组中创建 VMSS。</span><span class="sxs-lookup"><span data-stu-id="d15b5-689">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="d15b5-690">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="d15b5-690">AzureRM.EventHub</span></span>
* <span data-ttu-id="d15b5-691">向 PSEventHubDRConfigurationAttributes 类添加了一个只读属性“PendingReplicationOperationsCount”，该属性在复制过程中为挂起的复制操作计数</span><span class="sxs-lookup"><span data-stu-id="d15b5-691">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="d15b5-692">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d15b5-692">AzureRM.KeyVault</span></span>
* <span data-ttu-id="d15b5-693">更新了 Set-AzureRmKeyVaultAccessPolicy 的错误消息</span><span class="sxs-lookup"><span data-stu-id="d15b5-693">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="d15b5-694">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="d15b5-694">AzureRM.LogicApp</span></span>
* <span data-ttu-id="d15b5-695">修复了 New-AzureRmLogicApp 中的“无法解析参数集”错误</span><span class="sxs-lookup"><span data-stu-id="d15b5-695">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="d15b5-696">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="d15b5-696">AzureRM.Network</span></span>
* <span data-ttu-id="d15b5-697">在多个租户中为 Set/Add-AzureRmVirtualNetworkPeering 启用跨虚拟网络对等互连</span><span class="sxs-lookup"><span data-stu-id="d15b5-697">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="d15b5-698">针对应用程序网关更新了以下 cmdlet</span><span class="sxs-lookup"><span data-stu-id="d15b5-698">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="d15b5-699">New-AzureRmApplicationGateway：添加了 EnableFIPS 标志和区域支持</span><span class="sxs-lookup"><span data-stu-id="d15b5-699">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="d15b5-700">New-AzureRmApplicationGatewaySku：添加了新的 sku Standard_v2 和 WAF_v2</span><span class="sxs-lookup"><span data-stu-id="d15b5-700">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="d15b5-701">Set-AzureRmApplicationGatewaySku：添加了新的 sku Standard_v2 和 WAF_v2</span><span class="sxs-lookup"><span data-stu-id="d15b5-701">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="d15b5-702">使用最新的生成器版本重新生成了 RouteTable cmdlet</span><span class="sxs-lookup"><span data-stu-id="d15b5-702">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="d15b5-703">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="d15b5-703">AzureRM.Relay</span></span>
* <span data-ttu-id="d15b5-704">更新了 Markdown 文件，其中修复了示例中的参数名称问题</span><span class="sxs-lookup"><span data-stu-id="d15b5-704">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="d15b5-705">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="d15b5-705">AzureRM.Resources</span></span>
* <span data-ttu-id="d15b5-706">更新了 Roleassignment 和 roledefinition cmdlet：</span><span class="sxs-lookup"><span data-stu-id="d15b5-706">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="d15b5-707">删除了作为分页的一部分完成的额外 roledefinition 调用。</span><span class="sxs-lookup"><span data-stu-id="d15b5-707">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="d15b5-708">修复了 Get-AzureRmRoleAssignment cmdlet</span><span class="sxs-lookup"><span data-stu-id="d15b5-708">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="d15b5-709">修复了 -ExpandPrincipalGroups 命令参数功能</span><span class="sxs-lookup"><span data-stu-id="d15b5-709">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="d15b5-710">修复了“Get-AzureRmResource”的问题，其中“-ResourceType”参数区分大小写</span><span class="sxs-lookup"><span data-stu-id="d15b5-710">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="d15b5-711">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d15b5-711">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="d15b5-712">向列表 cmdlet 添加了 top 和 skip 参数</span><span class="sxs-lookup"><span data-stu-id="d15b5-712">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="d15b5-713">添加了标准到高级命名空间迁移 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="d15b5-713">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="d15b5-714">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="d15b5-714">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="d15b5-715">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="d15b5-715">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="d15b5-716">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="d15b5-716">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="d15b5-717">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="d15b5-717">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="d15b5-718">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="d15b5-718">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="d15b5-719">向 PSServiceBusDRConfigurationAttributes 类添加了一个只读属性“PendingReplicationOperationsCount”，该属性在复制过程中为挂起的复制操作计数</span><span class="sxs-lookup"><span data-stu-id="d15b5-719">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="d15b5-720">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d15b5-720">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="d15b5-721">更新了“New-AzureRmServiceFabricCluster”的示例</span><span class="sxs-lookup"><span data-stu-id="d15b5-721">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="d15b5-722">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="d15b5-722">AzureRM.Sql</span></span>
* <span data-ttu-id="d15b5-723">为 Management.Sql 添加新的 Cmdlet，以允许客户将 TDE 证书添加到 Sql Server 实例或托管实例</span><span class="sxs-lookup"><span data-stu-id="d15b5-723">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="d15b5-724">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="d15b5-724">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="d15b5-725">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="d15b5-725">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="d15b5-726">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="d15b5-726">AzureRM.Websites</span></span>
* <span data-ttu-id="d15b5-727">设置为 false 时，`Set-AzureRmWebApp -AssignIdentity` 和 `Set-AzureRmWebAppSlot -AssignIdentity` 现在将从站点对象中删除 Identity 属性。同时移除预览标记。</span><span class="sxs-lookup"><span data-stu-id="d15b5-727">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="d15b5-728">`Get-AzureRmWebAppMetrics`、`Get-AzureRmAppServicePlanMetrics` 示例已更新</span><span class="sxs-lookup"><span data-stu-id="d15b5-728">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="d15b5-729">`Set-AzureRmWebApp -PhpVersion` 支持 off 作为有效的 php 版本</span><span class="sxs-lookup"><span data-stu-id="d15b5-729">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="d15b5-730">6.4.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="d15b5-730">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="d15b5-731">常规</span><span class="sxs-lookup"><span data-stu-id="d15b5-731">General</span></span>
* <span data-ttu-id="d15b5-732">修复了大多数模块的帮助文件中的 OutputType 格式问题</span><span class="sxs-lookup"><span data-stu-id="d15b5-732">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="d15b5-733">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="d15b5-733">AzureRM.Profile</span></span>
* <span data-ttu-id="d15b5-734">已将 Ps1Xml 属性添加到基本输出类型</span><span class="sxs-lookup"><span data-stu-id="d15b5-734">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="d15b5-735">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="d15b5-735">AzureRM.Compute</span></span>
* <span data-ttu-id="d15b5-736">VMSS 的 IP 标记功能</span><span class="sxs-lookup"><span data-stu-id="d15b5-736">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="d15b5-737">已添加“New-AzureRmVmssIpTagConfig”cmdlet</span><span class="sxs-lookup"><span data-stu-id="d15b5-737">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="d15b5-738">已将 IpTag 参数添加到 New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="d15b5-738">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="d15b5-739">VMSS 的自动 OS 回滚功能</span><span class="sxs-lookup"><span data-stu-id="d15b5-739">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="d15b5-740">已将 DisableAutoRollback 参数添加到 New-AzureRmVmssConfig 和 Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d15b5-740">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="d15b5-741">VMSS 的 OS 升级历史记录功能</span><span class="sxs-lookup"><span data-stu-id="d15b5-741">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="d15b5-742">已将 OSUpgradeHistory 开关参数添加到 Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d15b5-742">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="d15b5-743">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="d15b5-743">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="d15b5-744">通过以下命令添加目录 ACL 的支持：</span><span class="sxs-lookup"><span data-stu-id="d15b5-744">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="d15b5-745">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="d15b5-745">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="d15b5-746">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="d15b5-746">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="d15b5-747">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="d15b5-747">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="d15b5-748">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d15b5-748">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="d15b5-749">为 Set-AzureRmDataLakeStoreItemAclEntry、Remove-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAcl 添加了取消支持和进度跟踪</span><span class="sxs-lookup"><span data-stu-id="d15b5-749">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="d15b5-750">为 Export-AzureRmDataLakeStoreChildItemProperties 添加了取消支持</span><span class="sxs-lookup"><span data-stu-id="d15b5-750">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="d15b5-751">修复了执行递归操作的 cmdlet 的调试消息刷新</span><span class="sxs-lookup"><span data-stu-id="d15b5-751">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="d15b5-752">修复了 DataLake cmdlet 的测试位置</span><span class="sxs-lookup"><span data-stu-id="d15b5-752">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="d15b5-753">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="d15b5-753">AzureRM.EventHub</span></span>
* <span data-ttu-id="d15b5-754">已将可选的 MaxCount 参数添加到“列出操作”cmdlet Get-AzureRmEventHub 和 Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="d15b5-754">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="d15b5-755">修复了 New-AzureRmEventHub cmdlet 的问题：创建新事件中心时至少需要一个参数。</span><span class="sxs-lookup"><span data-stu-id="d15b5-755">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="d15b5-756">提供了默认参数集。</span><span class="sxs-lookup"><span data-stu-id="d15b5-756">Provided Default Parameter set.</span></span>
* <span data-ttu-id="d15b5-757">已将可选参数 -KeyValue 添加到 New-AzureRmEventHubKey cmdlet，该参数可让用户提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="d15b5-757">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="d15b5-758">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d15b5-758">AzureRM.KeyVault</span></span>
* <span data-ttu-id="d15b5-759">修复了 Get-AzureRmKeyVault -Tag 返回所有资源的问题</span><span class="sxs-lookup"><span data-stu-id="d15b5-759">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="d15b5-760">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="d15b5-760">AzureRM.Network</span></span>
* <span data-ttu-id="d15b5-761">为区域冗余的 VirtualNetworkGateways 公开新 SKU</span><span class="sxs-lookup"><span data-stu-id="d15b5-761">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="d15b5-762">通过 ARM 为以下功能添加了新命令：ExpressRoute 合作伙伴 API</span><span class="sxs-lookup"><span data-stu-id="d15b5-762">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="d15b5-763">添加了 Get-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="d15b5-763">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="d15b5-764">添加了 Set-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="d15b5-764">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="d15b5-765">添加了 Add-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="d15b5-765">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="d15b5-766">添加了 Get-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="d15b5-766">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="d15b5-767">添加了 Remove-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="d15b5-767">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="d15b5-768">添加了 Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="d15b5-768">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="d15b5-769">添加了 Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="d15b5-769">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="d15b5-770">添加了 Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="d15b5-770">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="d15b5-771">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="d15b5-771">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="d15b5-772">添加了 Get-AzureRmRecoveryServicesBackupStatus cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d15b5-772">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="d15b5-773">此 cmdlet 采用 VM ID，并检查 VM 是否受订阅中的某个保管库保护。</span><span class="sxs-lookup"><span data-stu-id="d15b5-773">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="d15b5-774">如果存在此类保管库，该 cmdlet 会输出该保管库的详细信息。</span><span class="sxs-lookup"><span data-stu-id="d15b5-774">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="d15b5-775">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="d15b5-775">AzureRM.Resources</span></span>
* <span data-ttu-id="d15b5-776">更新了 Get-AzureRmPolicyAssignment cmdlet：</span><span class="sxs-lookup"><span data-stu-id="d15b5-776">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="d15b5-777">添加了在管理组级别列出 -Scope 值的支持</span><span class="sxs-lookup"><span data-stu-id="d15b5-777">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="d15b5-778">添加了在管理组级别使用 -Scope 值检索单个分配的支持</span><span class="sxs-lookup"><span data-stu-id="d15b5-778">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="d15b5-779">已将 -Effective 和 -All 开关添加到 control 参数</span><span class="sxs-lookup"><span data-stu-id="d15b5-779">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="d15b5-780">更新了 Get/New/Remove/Set-AzureRmPolicyDefinition cmdlet</span><span class="sxs-lookup"><span data-stu-id="d15b5-780">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="d15b5-781">添加了 -ManagementGroupName 参数，以将操作应用到给定的管理组</span><span class="sxs-lookup"><span data-stu-id="d15b5-781">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="d15b5-782">添加了 -SubscriptionId 参数，以将操作应用到给定的订阅</span><span class="sxs-lookup"><span data-stu-id="d15b5-782">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="d15b5-783">更新了 Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlet</span><span class="sxs-lookup"><span data-stu-id="d15b5-783">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="d15b5-784">添加了 -ManagementGroupName 参数，以将操作应用到给定的管理组</span><span class="sxs-lookup"><span data-stu-id="d15b5-784">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="d15b5-785">添加了 -SubscriptionId 参数，以将操作应用到给定的订阅</span><span class="sxs-lookup"><span data-stu-id="d15b5-785">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="d15b5-786">添加了使用 TemplateParameterObject 时在参数中指定 KeyVault 机密引用的支持</span><span class="sxs-lookup"><span data-stu-id="d15b5-786">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="d15b5-787">修复了忽略“New-AzureRmADAppCredential”的“-EndDate”参数的问题</span><span class="sxs-lookup"><span data-stu-id="d15b5-787">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="d15b5-788">修复了“Add-AzureRmADGroupMember”使用错误的 URL 发出请求的问题</span><span class="sxs-lookup"><span data-stu-id="d15b5-788">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="d15b5-789">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d15b5-789">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="d15b5-790">已将可选参数 -KeyValue 添加到 New-AzureRmServiceBusKey cmdlet，该参数可让用户提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="d15b5-790">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="d15b5-791">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="d15b5-791">AzureRM.Sql</span></span>
* <span data-ttu-id="d15b5-792">在 AzureRmSqlDatabaseRestorePoint 帮助中澄清了 SQLDW 的用户定义还原点</span><span class="sxs-lookup"><span data-stu-id="d15b5-792">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="d15b5-793">更新了多个 cmdlet 中 -ComputeGeneration 参数的文档</span><span class="sxs-lookup"><span data-stu-id="d15b5-793">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="d15b5-794">6.3.0 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="d15b5-794">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="d15b5-795">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="d15b5-795">AzureRM.Profile</span></span>
* <span data-ttu-id="d15b5-796">更新了 Enable-AzureRmContextAutoSave 的错误消息</span><span class="sxs-lookup"><span data-stu-id="d15b5-796">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="d15b5-797">在运行没有旧上下文的“Connect-AzureRmAccount”时为每个订阅创建一个上下文</span><span class="sxs-lookup"><span data-stu-id="d15b5-797">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="d15b5-798">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="d15b5-798">Azure.Storage</span></span>
* <span data-ttu-id="d15b5-799">在帮助文件中增加了关于 -Permissions 参数的其他信息。</span><span class="sxs-lookup"><span data-stu-id="d15b5-799">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="d15b5-800">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="d15b5-800">AzureRM.Compute</span></span>
* <span data-ttu-id="d15b5-801">“Get-AzureRmVmDiskEncryptionStatus”修复了一个针对没有数据磁盘的 VM 观察到的问题</span><span class="sxs-lookup"><span data-stu-id="d15b5-801">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="d15b5-802">更新计算客户端库版本以修复以下 cmdlet</span><span class="sxs-lookup"><span data-stu-id="d15b5-802">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="d15b5-803">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="d15b5-803">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="d15b5-804">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="d15b5-804">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="d15b5-805">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="d15b5-805">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="d15b5-806">修复了以下 cmdlet，因此可以正确地显示“操作 ID”和“操作状态”：</span><span class="sxs-lookup"><span data-stu-id="d15b5-806">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="d15b5-807">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="d15b5-807">Start-AzureRmVM</span></span>
    - <span data-ttu-id="d15b5-808">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="d15b5-808">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="d15b5-809">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="d15b5-809">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="d15b5-810">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="d15b5-810">Set-AzureRmVM</span></span>
    - <span data-ttu-id="d15b5-811">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="d15b5-811">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="d15b5-812">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d15b5-812">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="d15b5-813">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="d15b5-813">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="d15b5-814">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="d15b5-814">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="d15b5-815">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d15b5-815">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="d15b5-816">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d15b5-816">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="d15b5-817">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d15b5-817">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="d15b5-818">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d15b5-818">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="d15b5-819">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="d15b5-819">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="d15b5-820">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="d15b5-820">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="d15b5-821">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="d15b5-821">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="d15b5-822">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="d15b5-822">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="d15b5-823">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="d15b5-823">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="d15b5-824">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="d15b5-824">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="d15b5-825">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d15b5-825">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="d15b5-826">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="d15b5-826">AzureRM.EventGrid</span></span>
* <span data-ttu-id="d15b5-827">在 Update-AzureRmEventGridSubscription cmdlet 中删除 SubjectBeginsWith/SubjectEndsWith 的 ValidateNotNullOrEmpty 验证条件，允许根据需要将这些参数更改为空字符串。</span><span class="sxs-lookup"><span data-stu-id="d15b5-827">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="d15b5-828">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d15b5-828">AzureRM.KeyVault</span></span>
* <span data-ttu-id="d15b5-829">修复运行 Get-AzureRmKeyVault -Tag 时不返回任何标记的问题</span><span class="sxs-lookup"><span data-stu-id="d15b5-829">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="d15b5-830">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="d15b5-830">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="d15b5-831">策略见解 cmdlet 的公开发行版</span><span class="sxs-lookup"><span data-stu-id="d15b5-831">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="d15b5-832">使用 API 版本 2018-04-04</span><span class="sxs-lookup"><span data-stu-id="d15b5-832">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="d15b5-833">向 Get-AzureRmPolicyStateSummary 的结果添加了 PolicyDefinitionReferenceId</span><span class="sxs-lookup"><span data-stu-id="d15b5-833">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="d15b5-834">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="d15b5-834">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="d15b5-835">向 RecoveryServices.Backup cmdlet 添加了 -Vault 参数。</span><span class="sxs-lookup"><span data-stu-id="d15b5-835">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="d15b5-836">传递时，此项会替代 Set-AzureRmRecoveryServicesContext cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d15b5-836">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="d15b5-837">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="d15b5-837">AzureRM.Sql</span></span>
* <span data-ttu-id="d15b5-838">更新了 Get-AzureRmSqlDatabaseExpanded 的帮助文件中的示例</span><span class="sxs-lookup"><span data-stu-id="d15b5-838">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="d15b5-839">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="d15b5-839">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="d15b5-840">更新了 Add-AzureRmTrafficManagerEndpointConfig 的帮助文件</span><span class="sxs-lookup"><span data-stu-id="d15b5-840">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="d15b5-841">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="d15b5-841">AzureRM.Websites</span></span>
* <span data-ttu-id="d15b5-842">更新了“Set-AzureRmWebApp”，在使用 -AssignIdentity 时不覆盖 AppSettings</span><span class="sxs-lookup"><span data-stu-id="d15b5-842">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="d15b5-843">更新了“New-AzureRmWebAppSlot”，允许使用 AppServicePlan 作为可选参数</span><span class="sxs-lookup"><span data-stu-id="d15b5-843">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="d15b5-844">6.2.1 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="d15b5-844">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="d15b5-845">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d15b5-845">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="d15b5-846">更新了 PSWorkspace 模型，允许 Network 使用 type 作为参数</span><span class="sxs-lookup"><span data-stu-id="d15b5-846">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="d15b5-847">6.2.0 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="d15b5-847">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="d15b5-848">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="d15b5-848">AzureRM.Profile</span></span>
* <span data-ttu-id="d15b5-849">修复了 Newtonsoft.Json 的版本 10.0.3 在模块导入时无法加载的问题</span><span class="sxs-lookup"><span data-stu-id="d15b5-849">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="d15b5-850">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="d15b5-850">AzureRM.Compute</span></span>
* <span data-ttu-id="d15b5-851">VMSS VM 更新功能</span><span class="sxs-lookup"><span data-stu-id="d15b5-851">VMSS VM Update feature</span></span>
    - <span data-ttu-id="d15b5-852">增加了“Update-AzureRmVmssVM”和“New-AzureRmVMDataDisk”cmdlet</span><span class="sxs-lookup"><span data-stu-id="d15b5-852">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="d15b5-853">为“Add-AzureRmVMDataDisk”cmdlet 增加了 VirtualMachineScaleSetVM 参数，支持向 Vmss VM 添加数据磁盘。</span><span class="sxs-lookup"><span data-stu-id="d15b5-853">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="d15b5-854">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="d15b5-854">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="d15b5-855">将 ADF.Net SDK 版本更新到了 0.8.0-preview，其中包含以下更改：</span><span class="sxs-lookup"><span data-stu-id="d15b5-855">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="d15b5-856">增加了“配置工厂存储库”操作</span><span class="sxs-lookup"><span data-stu-id="d15b5-856">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="d15b5-857">更新了 QuickBooks LinkedService，可以公开 consumerKey 和 consumerSecret 属性</span><span class="sxs-lookup"><span data-stu-id="d15b5-857">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="d15b5-858">已将多个模型类型从 SecretBase 更新为 Object</span><span class="sxs-lookup"><span data-stu-id="d15b5-858">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="d15b5-859">增加了 Blob 事件触发器</span><span class="sxs-lookup"><span data-stu-id="d15b5-859">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="d15b5-860">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d15b5-860">AzureRM.KeyVault</span></span>
* <span data-ttu-id="d15b5-861">使用示例输出更新了文档</span><span class="sxs-lookup"><span data-stu-id="d15b5-861">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="d15b5-862">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="d15b5-862">AzureRM.Network</span></span>
* <span data-ttu-id="d15b5-863">在网络观察程序 cmdlet 上启用了流量分析参数</span><span class="sxs-lookup"><span data-stu-id="d15b5-863">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="d15b5-864">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="d15b5-864">AzureRM.Resources</span></span>
* <span data-ttu-id="d15b5-865">修复了从“Get-AzureRmResource”返回的“PSResource”对象的“Properties”属性问题</span><span class="sxs-lookup"><span data-stu-id="d15b5-865">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="d15b5-866">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="d15b5-866">AzureRM.Scheduler</span></span>
* <span data-ttu-id="d15b5-867">修复了更新 ServiceBusQueueJob 无法设置新 Auth 值的问题</span><span class="sxs-lookup"><span data-stu-id="d15b5-867">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="d15b5-868">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="d15b5-868">AzureRM.Sql</span></span>
* <span data-ttu-id="d15b5-869">使用可选的 LicenseType 参数更新了以下 cmdlet</span><span class="sxs-lookup"><span data-stu-id="d15b5-869">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="d15b5-870">New-AzureRmSqlDatabase；Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d15b5-870">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="d15b5-871">New-AzureRmSqlElasticPool；Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="d15b5-871">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="d15b5-872">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="d15b5-872">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="d15b5-873">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="d15b5-873">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="d15b5-874">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d15b5-874">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="d15b5-875">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="d15b5-875">AzureRM.Websites</span></span>
* <span data-ttu-id="d15b5-876">更新了“New-AzureRMWebApp”，可以使用策略库中的常用算法。</span><span class="sxs-lookup"><span data-stu-id="d15b5-876">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="d15b5-877">6.1.0 - 2018 年 5 月</span><span class="sxs-lookup"><span data-stu-id="d15b5-877">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="d15b5-878">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="d15b5-878">AzureRM.Profile</span></span>
* <span data-ttu-id="d15b5-879">修复了运行“Clear-AzureRmContext”时会保留空上下文的问题，该上下文使用旧的默认上下文的名称，导致用户无法使用旧名称创建新的上下文</span><span class="sxs-lookup"><span data-stu-id="d15b5-879">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="d15b5-880">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="d15b5-880">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="d15b5-881">允许在 AS 上执行网关的关联/取消关联操作。</span><span class="sxs-lookup"><span data-stu-id="d15b5-881">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="d15b5-882">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d15b5-882">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="d15b5-883">增加了对 ApiVersions、ApiReleases 和 ApiRevisions 的支持</span><span class="sxs-lookup"><span data-stu-id="d15b5-883">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="d15b5-884">增加了对 ServiceFabric 后端的支持</span><span class="sxs-lookup"><span data-stu-id="d15b5-884">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="d15b5-885">增加了对 Application Insights Logger 的支持</span><span class="sxs-lookup"><span data-stu-id="d15b5-885">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="d15b5-886">增加的支持包括认可“基本”SKU 是 API 管理服务的有效 SKU</span><span class="sxs-lookup"><span data-stu-id="d15b5-886">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="d15b5-887">增加的支持包括允许将专用 CA 颁发的证书作为根证书或 CA 证书安装</span><span class="sxs-lookup"><span data-stu-id="d15b5-887">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="d15b5-888">增加的支持包括通过 KeyVault 和多个代理主机名接受自定义 SSL 证书</span><span class="sxs-lookup"><span data-stu-id="d15b5-888">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="d15b5-889">增加了对 MSI 标识的支持</span><span class="sxs-lookup"><span data-stu-id="d15b5-889">Added support for MSI identity</span></span>
* <span data-ttu-id="d15b5-890">增加的支持包括通过 URL 接受策略 注意：以下 cmdlet 将在未来版本中弃用</span><span class="sxs-lookup"><span data-stu-id="d15b5-890">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="d15b5-891">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="d15b5-891">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="d15b5-892">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="d15b5-892">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="d15b5-893">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="d15b5-893">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="d15b5-894">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="d15b5-894">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="d15b5-895">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="d15b5-895">AzureRM.Batch</span></span>
* <span data-ttu-id="d15b5-896">发布新 cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="d15b5-896">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="d15b5-897">发布新 cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="d15b5-897">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="d15b5-898">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="d15b5-898">AzureRM.Consumption</span></span>
* <span data-ttu-id="d15b5-899">在 Cmdlet Get-AzureRmConsumptionUsageDetail 中增加了新参数 Expand、ResourceGroup、InstanceName、InstanceId、Tags、Top</span><span class="sxs-lookup"><span data-stu-id="d15b5-899">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="d15b5-900">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d15b5-900">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="d15b5-901">修复了 Export-AzureRmDataLakeStoreChildItemProperties 的示例</span><span class="sxs-lookup"><span data-stu-id="d15b5-901">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="d15b5-902">修复了 Set-AzureRmDataLakeStoreItemAclEntry 中 Recurse 用例的 null 参数异常</span><span class="sxs-lookup"><span data-stu-id="d15b5-902">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="d15b5-903">修复了 Set-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAcl、Remove-AzureRmDataLakeStoreItemAclEntry 的帮助文件</span><span class="sxs-lookup"><span data-stu-id="d15b5-903">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="d15b5-904">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="d15b5-904">AzureRM.Network</span></span>
* <span data-ttu-id="d15b5-905">将网络 SDK 版本从 18.0.0-preview 升至 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="d15b5-905">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="d15b5-906">增加了用于创建协议配置的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="d15b5-906">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="d15b5-907">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="d15b5-907">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="d15b5-908">增加了用于向现有的快速路由线路添加新的线路连接的 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d15b5-908">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="d15b5-909">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="d15b5-909">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="d15b5-910">增加了用于从现有的快速路由线路删除线路连接的 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d15b5-910">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="d15b5-911">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="d15b5-911">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="d15b5-912">增加了用于检索线路连接的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="d15b5-912">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="d15b5-913">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="d15b5-913">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="d15b5-914">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d15b5-914">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="d15b5-915">修复了使用生成的证书进行服务器身份验证的问题（问题 5998）</span><span class="sxs-lookup"><span data-stu-id="d15b5-915">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="d15b5-916">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="d15b5-916">AzureRM.Sql</span></span>
* <span data-ttu-id="d15b5-917">更新了审核 cmdlet，允许删除 AuditActions 或 AuditActionGroups</span><span class="sxs-lookup"><span data-stu-id="d15b5-917">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="d15b5-918">修复了设置新的灵活保留策略时使用 Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy 出现的问题。该问题的具体表现是：在命令失败的同时，出现“不再支持使用 Azure 恢复服务保管库和策略配置长期保留策略。</span><span class="sxs-lookup"><span data-stu-id="d15b5-918">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="d15b5-919">请使用新的灵活保留策略提交请求”错误消息。</span><span class="sxs-lookup"><span data-stu-id="d15b5-919">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="d15b5-920">更新了与 Azure SQL 数据库/ElasticPool 的创建/更新相关的所有 cmdlet，允许使用新的数据库 API，而这些 cmdlet 支持的 SKU 属性则适用于规模和层相关属性。</span><span class="sxs-lookup"><span data-stu-id="d15b5-920">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="d15b5-921">更新的 cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="d15b5-921">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="d15b5-922">New-AzureRmSqlDatabase；Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d15b5-922">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="d15b5-923">New-AzureRmSqlElasticPool；Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="d15b5-923">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="d15b5-924">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="d15b5-924">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="d15b5-925">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="d15b5-925">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="d15b5-926">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d15b5-926">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="d15b5-927">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="d15b5-927">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="d15b5-928">更新了“Get-AzureRmTrafficManagerProfile”的参数，要求在使用 -Name 参数时使用 -ResourceGroupName 参数。</span><span class="sxs-lookup"><span data-stu-id="d15b5-928">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
