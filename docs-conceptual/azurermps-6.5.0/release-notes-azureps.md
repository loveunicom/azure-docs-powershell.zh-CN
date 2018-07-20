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
ms.openlocfilehash: e9fa2d75c1c4e6ffaa2f7dd8e400f5b13dd4527d
ms.sourcegitcommit: 8b882d1c27d9e323447ff85f56d11bbf5e244d7f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/18/2018
ms.locfileid: "39110477"
---
# <a name="release-notes"></a><span data-ttu-id="561b5-103">发行说明</span><span class="sxs-lookup"><span data-stu-id="561b5-103">Release notes</span></span>

<span data-ttu-id="561b5-104">下面是此版本中对 Azure PowerShell 所做的更改列表。</span><span class="sxs-lookup"><span data-stu-id="561b5-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="650---july-2018"></a><span data-ttu-id="561b5-105">6.5.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="561b5-105">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="561b5-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="561b5-106">AzureRM.Profile</span></span>
* <span data-ttu-id="561b5-107">更新了“Get-AzureRmContextAutosaveSetting”的帮助</span><span class="sxs-lookup"><span data-stu-id="561b5-107">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="561b5-108">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="561b5-108">Azure.Storage</span></span>
* <span data-ttu-id="561b5-109">支持使用只写 Sas 令牌上传 Blob 或文件</span><span class="sxs-lookup"><span data-stu-id="561b5-109">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="561b5-110">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="561b5-110">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="561b5-111">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="561b5-111">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="561b5-112">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="561b5-112">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="561b5-113">将所需属性 ResourceGroupName 添加到 AS。</span><span class="sxs-lookup"><span data-stu-id="561b5-113">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="561b5-114">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="561b5-114">AzureRM.Automation</span></span>
* <span data-ttu-id="561b5-115">更新帮助并添加“New-AzureRMAutomationSchedule”的示例</span><span class="sxs-lookup"><span data-stu-id="561b5-115">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="561b5-116">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="561b5-116">AzureRM.Compute</span></span>
* <span data-ttu-id="561b5-117">将 -Tag 参数添加到 Update/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="561b5-117">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="561b5-118">添加“Add-AzureRmVmssExtension”的示例</span><span class="sxs-lookup"><span data-stu-id="561b5-118">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="561b5-119">添加“Remove-AzureRmVmssExtension”的示例</span><span class="sxs-lookup"><span data-stu-id="561b5-119">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="561b5-120">更新“Set-AzureRmVMAccessExtension”的帮助</span><span class="sxs-lookup"><span data-stu-id="561b5-120">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="561b5-121">更新 New-AzureRmVmss 的 SimpleParameterSet，以默认情况下将 SinglePlacementGroup 设置为false，并添加开关参数“SinglePlacementGroup”，使用户能够在单个放置组中创建 VMSS。</span><span class="sxs-lookup"><span data-stu-id="561b5-121">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="561b5-122">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="561b5-122">AzureRM.EventHub</span></span>
* <span data-ttu-id="561b5-123">向 PSEventHubDRConfigurationAttributes 类添加了一个只读属性“PendingReplicationOperationsCount”，该属性在复制过程中为挂起的复制操作计数</span><span class="sxs-lookup"><span data-stu-id="561b5-123">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="561b5-124">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="561b5-124">AzureRM.KeyVault</span></span>
* <span data-ttu-id="561b5-125">更新了 Set-AzureRmKeyVaultAccessPolicy 的错误消息</span><span class="sxs-lookup"><span data-stu-id="561b5-125">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="561b5-126">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="561b5-126">AzureRM.LogicApp</span></span>
* <span data-ttu-id="561b5-127">修复了 New-AzureRmLogicApp 中的“无法解析参数集”错误</span><span class="sxs-lookup"><span data-stu-id="561b5-127">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="561b5-128">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="561b5-128">AzureRM.Network</span></span>
* <span data-ttu-id="561b5-129">在多个租户中为 Set/Add-AzureRmVirtualNetworkPeering 启用跨虚拟网络对等互连</span><span class="sxs-lookup"><span data-stu-id="561b5-129">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="561b5-130">针对应用程序网关更新了以下 cmdlet</span><span class="sxs-lookup"><span data-stu-id="561b5-130">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="561b5-131">New-AzureRmApplicationGateway：添加了 EnableFIPS 标志和区域支持</span><span class="sxs-lookup"><span data-stu-id="561b5-131">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="561b5-132">New-AzureRmApplicationGatewaySku：添加了新的 sku Standard_v2 和 WAF_v2</span><span class="sxs-lookup"><span data-stu-id="561b5-132">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="561b5-133">Set-AzureRmApplicationGatewaySku：添加了新的 sku Standard_v2 和 WAF_v2</span><span class="sxs-lookup"><span data-stu-id="561b5-133">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="561b5-134">使用最新的生成器版本重新生成了 RouteTable cmdlet</span><span class="sxs-lookup"><span data-stu-id="561b5-134">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="561b5-135">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="561b5-135">AzureRM.Relay</span></span>
* <span data-ttu-id="561b5-136">更新了 Markdown 文件，其中修复了示例中的参数名称问题</span><span class="sxs-lookup"><span data-stu-id="561b5-136">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="561b5-137">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="561b5-137">AzureRM.Resources</span></span>
* <span data-ttu-id="561b5-138">更新了 Roleassignment 和 roledefinition cmdlet：</span><span class="sxs-lookup"><span data-stu-id="561b5-138">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="561b5-139">删除了作为分页的一部分完成的额外 roledefinition 调用。</span><span class="sxs-lookup"><span data-stu-id="561b5-139">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="561b5-140">修复了 Get-AzureRmRoleAssignment cmdlet</span><span class="sxs-lookup"><span data-stu-id="561b5-140">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="561b5-141">修复了 -ExpandPrincipalGroups 命令参数功能</span><span class="sxs-lookup"><span data-stu-id="561b5-141">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="561b5-142">修复了“Get-AzureRmResource”的问题，其中“-ResourceType”参数区分大小写</span><span class="sxs-lookup"><span data-stu-id="561b5-142">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="561b5-143">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="561b5-143">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="561b5-144">向列表 cmdlet 添加了 top 和 skip 参数</span><span class="sxs-lookup"><span data-stu-id="561b5-144">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="561b5-145">添加了标准到高级命名空间迁移 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="561b5-145">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="561b5-146">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="561b5-146">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="561b5-147">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="561b5-147">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="561b5-148">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="561b5-148">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="561b5-149">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="561b5-149">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="561b5-150">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="561b5-150">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="561b5-151">向 PSServiceBusDRConfigurationAttributes 类添加了一个只读属性“PendingReplicationOperationsCount”，该属性在复制过程中为挂起的复制操作计数</span><span class="sxs-lookup"><span data-stu-id="561b5-151">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="561b5-152">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="561b5-152">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="561b5-153">更新了“New-AzureRmServiceFabricCluster”的示例</span><span class="sxs-lookup"><span data-stu-id="561b5-153">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="561b5-154">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="561b5-154">AzureRM.Sql</span></span>
* <span data-ttu-id="561b5-155">为 Management.Sql 添加新的 Cmdlet，以允许客户将 TDE 证书添加到 Sql Server 实例或托管实例</span><span class="sxs-lookup"><span data-stu-id="561b5-155">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="561b5-156">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="561b5-156">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="561b5-157">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="561b5-157">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="561b5-158">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="561b5-158">AzureRM.Websites</span></span>
* <span data-ttu-id="561b5-159">设置为 false 时，`Set-AzureRmWebApp -AssignIdentity` 和 `Set-AzureRmWebAppSlot -AssignIdentity` 现在将从站点对象中删除 Identity 属性。同时移除预览标记。</span><span class="sxs-lookup"><span data-stu-id="561b5-159">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="561b5-160">`Get-AzureRmWebAppMetrics`、`Get-AzureRmAppServicePlanMetrics` 示例已更新</span><span class="sxs-lookup"><span data-stu-id="561b5-160">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="561b5-161">`Set-AzureRmWebApp -PhpVersion` 支持 off 作为有效的 php 版本</span><span class="sxs-lookup"><span data-stu-id="561b5-161">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="561b5-162">6.4.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="561b5-162">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="561b5-163">常规</span><span class="sxs-lookup"><span data-stu-id="561b5-163">General</span></span>
* <span data-ttu-id="561b5-164">修复了大多数模块的帮助文件中的 OutputType 格式问题</span><span class="sxs-lookup"><span data-stu-id="561b5-164">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="561b5-165">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="561b5-165">AzureRM.Profile</span></span>
* <span data-ttu-id="561b5-166">已将 Ps1Xml 属性添加到基本输出类型</span><span class="sxs-lookup"><span data-stu-id="561b5-166">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="561b5-167">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="561b5-167">AzureRM.Compute</span></span>
* <span data-ttu-id="561b5-168">VMSS 的 IP 标记功能</span><span class="sxs-lookup"><span data-stu-id="561b5-168">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="561b5-169">已添加“New-AzureRmVmssIpTagConfig”cmdlet</span><span class="sxs-lookup"><span data-stu-id="561b5-169">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="561b5-170">已将 IpTag 参数添加到 New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="561b5-170">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="561b5-171">VMSS 的自动 OS 回滚功能</span><span class="sxs-lookup"><span data-stu-id="561b5-171">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="561b5-172">已将 DisableAutoRollback 参数添加到 New-AzureRmVmssConfig 和 Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="561b5-172">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="561b5-173">VMSS 的 OS 升级历史记录功能</span><span class="sxs-lookup"><span data-stu-id="561b5-173">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="561b5-174">已将 OSUpgradeHistory 开关参数添加到 Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="561b5-174">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="561b5-175">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="561b5-175">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="561b5-176">通过以下命令添加目录 ACL 的支持：</span><span class="sxs-lookup"><span data-stu-id="561b5-176">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="561b5-177">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="561b5-177">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="561b5-178">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="561b5-178">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="561b5-179">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="561b5-179">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="561b5-180">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="561b5-180">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="561b5-181">为 Set-AzureRmDataLakeStoreItemAclEntry、Remove-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAcl 添加了取消支持和进度跟踪</span><span class="sxs-lookup"><span data-stu-id="561b5-181">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="561b5-182">为 Export-AzureRmDataLakeStoreChildItemProperties 添加了取消支持</span><span class="sxs-lookup"><span data-stu-id="561b5-182">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="561b5-183">修复了执行递归操作的 cmdlet 的调试消息刷新</span><span class="sxs-lookup"><span data-stu-id="561b5-183">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="561b5-184">修复了 DataLake cmdlet 的测试位置</span><span class="sxs-lookup"><span data-stu-id="561b5-184">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="561b5-185">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="561b5-185">AzureRM.EventHub</span></span>
* <span data-ttu-id="561b5-186">已将可选的 MaxCount 参数添加到“列出操作”cmdlet Get-AzureRmEventHub 和 Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="561b5-186">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="561b5-187">修复了 New-AzureRmEventHub cmdlet 的问题：创建新事件中心时至少需要一个参数。</span><span class="sxs-lookup"><span data-stu-id="561b5-187">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="561b5-188">提供了默认参数集。</span><span class="sxs-lookup"><span data-stu-id="561b5-188">Provided Default Parameter set.</span></span>
* <span data-ttu-id="561b5-189">已将可选参数 -KeyValue 添加到 New-AzureRmEventHubKey cmdlet，该参数可让用户提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="561b5-189">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="561b5-190">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="561b5-190">AzureRM.KeyVault</span></span>
* <span data-ttu-id="561b5-191">修复了 Get-AzureRmKeyVault -Tag 返回所有资源的问题</span><span class="sxs-lookup"><span data-stu-id="561b5-191">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="561b5-192">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="561b5-192">AzureRM.Network</span></span>
* <span data-ttu-id="561b5-193">为区域冗余的 VirtualNetworkGateways 公开新 SKU</span><span class="sxs-lookup"><span data-stu-id="561b5-193">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="561b5-194">通过 ARM 为以下功能添加了新命令：ExpressRoute 合作伙伴 API</span><span class="sxs-lookup"><span data-stu-id="561b5-194">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="561b5-195">添加了 Get-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="561b5-195">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="561b5-196">添加了 Set-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="561b5-196">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="561b5-197">添加了 Add-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="561b5-197">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="561b5-198">添加了 Get-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="561b5-198">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="561b5-199">添加了 Remove-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="561b5-199">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="561b5-200">添加了 Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="561b5-200">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="561b5-201">添加了 Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="561b5-201">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="561b5-202">添加了 Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="561b5-202">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="561b5-203">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="561b5-203">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="561b5-204">添加了 Get-AzureRmRecoveryServicesBackupStatus cmdlet。</span><span class="sxs-lookup"><span data-stu-id="561b5-204">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="561b5-205">此 cmdlet 采用 VM ID，并检查 VM 是否受订阅中的某个保管库保护。</span><span class="sxs-lookup"><span data-stu-id="561b5-205">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="561b5-206">如果存在此类保管库，该 cmdlet 会输出该保管库的详细信息。</span><span class="sxs-lookup"><span data-stu-id="561b5-206">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="561b5-207">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="561b5-207">AzureRM.Resources</span></span>
* <span data-ttu-id="561b5-208">更新了 Get-AzureRmPolicyAssignment cmdlet：</span><span class="sxs-lookup"><span data-stu-id="561b5-208">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="561b5-209">添加了在管理组级别列出 -Scope 值的支持</span><span class="sxs-lookup"><span data-stu-id="561b5-209">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="561b5-210">添加了在管理组级别使用 -Scope 值检索单个分配的支持</span><span class="sxs-lookup"><span data-stu-id="561b5-210">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="561b5-211">已将 -Effective 和 -All 开关添加到 control 参数</span><span class="sxs-lookup"><span data-stu-id="561b5-211">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="561b5-212">更新了 Get/New/Remove/Set-AzureRmPolicyDefinition cmdlet</span><span class="sxs-lookup"><span data-stu-id="561b5-212">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="561b5-213">添加了 -ManagementGroupName 参数，以将操作应用到给定的管理组</span><span class="sxs-lookup"><span data-stu-id="561b5-213">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="561b5-214">添加了 -SubscriptionId 参数，以将操作应用到给定的订阅</span><span class="sxs-lookup"><span data-stu-id="561b5-214">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="561b5-215">更新了 Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlet</span><span class="sxs-lookup"><span data-stu-id="561b5-215">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="561b5-216">添加了 -ManagementGroupName 参数，以将操作应用到给定的管理组</span><span class="sxs-lookup"><span data-stu-id="561b5-216">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="561b5-217">添加了 -SubscriptionId 参数，以将操作应用到给定的订阅</span><span class="sxs-lookup"><span data-stu-id="561b5-217">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="561b5-218">添加了使用 TemplateParameterObject 时在参数中指定 KeyVault 机密引用的支持</span><span class="sxs-lookup"><span data-stu-id="561b5-218">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="561b5-219">修复了忽略“New-AzureRmADAppCredential”的“-EndDate”参数的问题</span><span class="sxs-lookup"><span data-stu-id="561b5-219">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="561b5-220">修复了“Add-AzureRmADGroupMember”使用错误的 URL 发出请求的问题</span><span class="sxs-lookup"><span data-stu-id="561b5-220">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="561b5-221">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="561b5-221">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="561b5-222">已将可选参数 -KeyValue 添加到 New-AzureRmServiceBusKey cmdlet，该参数可让用户提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="561b5-222">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="561b5-223">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="561b5-223">AzureRM.Sql</span></span>
* <span data-ttu-id="561b5-224">在 AzureRmSqlDatabaseRestorePoint 帮助中澄清了 SQLDW 的用户定义还原点</span><span class="sxs-lookup"><span data-stu-id="561b5-224">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="561b5-225">更新了多个 cmdlet 中 -ComputeGeneration 参数的文档</span><span class="sxs-lookup"><span data-stu-id="561b5-225">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="561b5-226">6.3.0 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="561b5-226">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="561b5-227">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="561b5-227">AzureRM.Profile</span></span>
* <span data-ttu-id="561b5-228">更新了 Enable-AzureRmContextAutoSave 的错误消息</span><span class="sxs-lookup"><span data-stu-id="561b5-228">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="561b5-229">在运行没有旧上下文的“Connect-AzureRmAccount”时为每个订阅创建一个上下文</span><span class="sxs-lookup"><span data-stu-id="561b5-229">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="561b5-230">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="561b5-230">Azure.Storage</span></span>
* <span data-ttu-id="561b5-231">在帮助文件中增加了关于 -Permissions 参数的其他信息。</span><span class="sxs-lookup"><span data-stu-id="561b5-231">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="561b5-232">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="561b5-232">AzureRM.Compute</span></span>
* <span data-ttu-id="561b5-233">“Get-AzureRmVmDiskEncryptionStatus”修复了一个针对没有数据磁盘的 VM 观察到的问题</span><span class="sxs-lookup"><span data-stu-id="561b5-233">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="561b5-234">更新计算客户端库版本以修复以下 cmdlet</span><span class="sxs-lookup"><span data-stu-id="561b5-234">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="561b5-235">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="561b5-235">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="561b5-236">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="561b5-236">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="561b5-237">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="561b5-237">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="561b5-238">修复了以下 cmdlet，因此可以正确地显示“操作 ID”和“操作状态”：</span><span class="sxs-lookup"><span data-stu-id="561b5-238">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="561b5-239">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="561b5-239">Start-AzureRmVM</span></span>
    - <span data-ttu-id="561b5-240">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="561b5-240">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="561b5-241">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="561b5-241">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="561b5-242">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="561b5-242">Set-AzureRmVM</span></span>
    - <span data-ttu-id="561b5-243">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="561b5-243">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="561b5-244">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="561b5-244">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="561b5-245">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="561b5-245">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="561b5-246">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="561b5-246">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="561b5-247">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="561b5-247">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="561b5-248">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="561b5-248">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="561b5-249">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="561b5-249">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="561b5-250">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="561b5-250">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="561b5-251">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="561b5-251">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="561b5-252">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="561b5-252">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="561b5-253">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="561b5-253">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="561b5-254">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="561b5-254">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="561b5-255">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="561b5-255">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="561b5-256">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="561b5-256">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="561b5-257">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="561b5-257">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="561b5-258">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="561b5-258">AzureRM.EventGrid</span></span>
* <span data-ttu-id="561b5-259">在 Update-AzureRmEventGridSubscription cmdlet 中删除 SubjectBeginsWith/SubjectEndsWith 的 ValidateNotNullOrEmpty 验证条件，允许根据需要将这些参数更改为空字符串。</span><span class="sxs-lookup"><span data-stu-id="561b5-259">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="561b5-260">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="561b5-260">AzureRM.KeyVault</span></span>
* <span data-ttu-id="561b5-261">修复运行 Get-AzureRmKeyVault -Tag 时不返回任何标记的问题</span><span class="sxs-lookup"><span data-stu-id="561b5-261">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="561b5-262">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="561b5-262">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="561b5-263">策略见解 cmdlet 的公开发行版</span><span class="sxs-lookup"><span data-stu-id="561b5-263">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="561b5-264">使用 API 版本 2018-04-04</span><span class="sxs-lookup"><span data-stu-id="561b5-264">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="561b5-265">向 Get-AzureRmPolicyStateSummary 的结果添加了 PolicyDefinitionReferenceId</span><span class="sxs-lookup"><span data-stu-id="561b5-265">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="561b5-266">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="561b5-266">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="561b5-267">向 RecoveryServices.Backup cmdlet 添加了 -Vault 参数。</span><span class="sxs-lookup"><span data-stu-id="561b5-267">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="561b5-268">传递时，此项会替代 Set-AzureRmRecoveryServicesContext cmdlet。</span><span class="sxs-lookup"><span data-stu-id="561b5-268">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="561b5-269">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="561b5-269">AzureRM.Sql</span></span>
* <span data-ttu-id="561b5-270">更新了 Get-AzureRmSqlDatabaseExpanded 的帮助文件中的示例</span><span class="sxs-lookup"><span data-stu-id="561b5-270">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="561b5-271">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="561b5-271">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="561b5-272">更新了 Add-AzureRmTrafficManagerEndpointConfig 的帮助文件</span><span class="sxs-lookup"><span data-stu-id="561b5-272">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="561b5-273">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="561b5-273">AzureRM.Websites</span></span>
* <span data-ttu-id="561b5-274">更新了“Set-AzureRmWebApp”，在使用 -AssignIdentity 时不覆盖 AppSettings</span><span class="sxs-lookup"><span data-stu-id="561b5-274">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="561b5-275">更新了“New-AzureRmWebAppSlot”，允许使用 AppServicePlan 作为可选参数</span><span class="sxs-lookup"><span data-stu-id="561b5-275">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="561b5-276">6.2.1 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="561b5-276">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="561b5-277">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="561b5-277">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="561b5-278">更新了 PSWorkspace 模型，允许 Network 使用 type 作为参数</span><span class="sxs-lookup"><span data-stu-id="561b5-278">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="561b5-279">6.2.0 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="561b5-279">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="561b5-280">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="561b5-280">AzureRM.Profile</span></span>
* <span data-ttu-id="561b5-281">修复了 Newtonsoft.Json 的版本 10.0.3 在模块导入时无法加载的问题</span><span class="sxs-lookup"><span data-stu-id="561b5-281">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="561b5-282">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="561b5-282">AzureRM.Compute</span></span>
* <span data-ttu-id="561b5-283">VMSS VM 更新功能</span><span class="sxs-lookup"><span data-stu-id="561b5-283">VMSS VM Update feature</span></span>
    - <span data-ttu-id="561b5-284">增加了“Update-AzureRmVmssVM”和“New-AzureRmVMDataDisk”cmdlet</span><span class="sxs-lookup"><span data-stu-id="561b5-284">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="561b5-285">为“Add-AzureRmVMDataDisk”cmdlet 增加了 VirtualMachineScaleSetVM 参数，支持向 Vmss VM 添加数据磁盘。</span><span class="sxs-lookup"><span data-stu-id="561b5-285">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="561b5-286">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="561b5-286">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="561b5-287">将 ADF.Net SDK 版本更新到了 0.8.0-preview，其中包含以下更改：</span><span class="sxs-lookup"><span data-stu-id="561b5-287">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="561b5-288">增加了“配置工厂存储库”操作</span><span class="sxs-lookup"><span data-stu-id="561b5-288">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="561b5-289">更新了 QuickBooks LinkedService，可以公开 consumerKey 和 consumerSecret 属性</span><span class="sxs-lookup"><span data-stu-id="561b5-289">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="561b5-290">已将多个模型类型从 SecretBase 更新为 Object</span><span class="sxs-lookup"><span data-stu-id="561b5-290">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="561b5-291">增加了 Blob 事件触发器</span><span class="sxs-lookup"><span data-stu-id="561b5-291">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="561b5-292">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="561b5-292">AzureRM.KeyVault</span></span>
* <span data-ttu-id="561b5-293">使用示例输出更新了文档</span><span class="sxs-lookup"><span data-stu-id="561b5-293">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="561b5-294">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="561b5-294">AzureRM.Network</span></span>
* <span data-ttu-id="561b5-295">在网络观察程序 cmdlet 上启用了流量分析参数</span><span class="sxs-lookup"><span data-stu-id="561b5-295">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="561b5-296">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="561b5-296">AzureRM.Resources</span></span>
* <span data-ttu-id="561b5-297">修复了从“Get-AzureRmResource”返回的“PSResource”对象的“Properties”属性问题</span><span class="sxs-lookup"><span data-stu-id="561b5-297">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="561b5-298">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="561b5-298">AzureRM.Scheduler</span></span>
* <span data-ttu-id="561b5-299">修复了更新 ServiceBusQueueJob 无法设置新 Auth 值的问题</span><span class="sxs-lookup"><span data-stu-id="561b5-299">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="561b5-300">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="561b5-300">AzureRM.Sql</span></span>
* <span data-ttu-id="561b5-301">使用可选的 LicenseType 参数更新了以下 cmdlet</span><span class="sxs-lookup"><span data-stu-id="561b5-301">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="561b5-302">New-AzureRmSqlDatabase；Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="561b5-302">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="561b5-303">New-AzureRmSqlElasticPool；Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="561b5-303">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="561b5-304">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="561b5-304">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="561b5-305">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="561b5-305">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="561b5-306">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="561b5-306">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="561b5-307">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="561b5-307">AzureRM.Websites</span></span>
* <span data-ttu-id="561b5-308">更新了“New-AzureRMWebApp”，可以使用策略库中的常用算法。</span><span class="sxs-lookup"><span data-stu-id="561b5-308">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="561b5-309">6.1.0 - 2018 年 5 月</span><span class="sxs-lookup"><span data-stu-id="561b5-309">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="561b5-310">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="561b5-310">AzureRM.Profile</span></span>
* <span data-ttu-id="561b5-311">修复了运行“Clear-AzureRmContext”时会保留空上下文的问题，该上下文使用旧的默认上下文的名称，导致用户无法使用旧名称创建新的上下文</span><span class="sxs-lookup"><span data-stu-id="561b5-311">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="561b5-312">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="561b5-312">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="561b5-313">允许在 AS 上执行网关的关联/取消关联操作。</span><span class="sxs-lookup"><span data-stu-id="561b5-313">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="561b5-314">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="561b5-314">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="561b5-315">增加了对 ApiVersions、ApiReleases 和 ApiRevisions 的支持</span><span class="sxs-lookup"><span data-stu-id="561b5-315">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="561b5-316">增加了对 ServiceFabric 后端的支持</span><span class="sxs-lookup"><span data-stu-id="561b5-316">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="561b5-317">增加了对 Application Insights Logger 的支持</span><span class="sxs-lookup"><span data-stu-id="561b5-317">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="561b5-318">增加的支持包括认可“基本”SKU 是 API 管理服务的有效 SKU</span><span class="sxs-lookup"><span data-stu-id="561b5-318">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="561b5-319">增加的支持包括允许将专用 CA 颁发的证书作为根证书或 CA 证书安装</span><span class="sxs-lookup"><span data-stu-id="561b5-319">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="561b5-320">增加的支持包括通过 KeyVault 和多个代理主机名接受自定义 SSL 证书</span><span class="sxs-lookup"><span data-stu-id="561b5-320">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="561b5-321">增加了对 MSI 标识的支持</span><span class="sxs-lookup"><span data-stu-id="561b5-321">Added support for MSI identity</span></span>
* <span data-ttu-id="561b5-322">增加的支持包括通过 URL 接受策略 注意：以下 cmdlet 将在未来版本中弃用</span><span class="sxs-lookup"><span data-stu-id="561b5-322">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="561b5-323">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="561b5-323">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="561b5-324">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="561b5-324">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="561b5-325">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="561b5-325">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="561b5-326">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="561b5-326">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="561b5-327">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="561b5-327">AzureRM.Batch</span></span>
* <span data-ttu-id="561b5-328">发布新 cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="561b5-328">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="561b5-329">发布新 cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="561b5-329">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="561b5-330">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="561b5-330">AzureRM.Consumption</span></span>
* <span data-ttu-id="561b5-331">在 Cmdlet Get-AzureRmConsumptionUsageDetail 中增加了新参数 Expand、ResourceGroup、InstanceName、InstanceId、Tags、Top</span><span class="sxs-lookup"><span data-stu-id="561b5-331">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="561b5-332">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="561b5-332">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="561b5-333">修复了 Export-AzureRmDataLakeStoreChildItemProperties 的示例</span><span class="sxs-lookup"><span data-stu-id="561b5-333">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="561b5-334">修复了 Set-AzureRmDataLakeStoreItemAclEntry 中 Recurse 用例的 null 参数异常</span><span class="sxs-lookup"><span data-stu-id="561b5-334">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="561b5-335">修复了 Set-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAcl、Remove-AzureRmDataLakeStoreItemAclEntry 的帮助文件</span><span class="sxs-lookup"><span data-stu-id="561b5-335">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="561b5-336">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="561b5-336">AzureRM.Network</span></span>
* <span data-ttu-id="561b5-337">将网络 SDK 版本从 18.0.0-preview 升至 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="561b5-337">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="561b5-338">增加了用于创建协议配置的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="561b5-338">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="561b5-339">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="561b5-339">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="561b5-340">增加了用于向现有的快速路由线路添加新的线路连接的 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="561b5-340">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="561b5-341">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="561b5-341">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="561b5-342">增加了用于从现有的快速路由线路删除线路连接的 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="561b5-342">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="561b5-343">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="561b5-343">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="561b5-344">增加了用于检索线路连接的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="561b5-344">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="561b5-345">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="561b5-345">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="561b5-346">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="561b5-346">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="561b5-347">修复了使用生成的证书进行服务器身份验证的问题（问题 5998）</span><span class="sxs-lookup"><span data-stu-id="561b5-347">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="561b5-348">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="561b5-348">AzureRM.Sql</span></span>
* <span data-ttu-id="561b5-349">更新了审核 cmdlet，允许删除 AuditActions 或 AuditActionGroups</span><span class="sxs-lookup"><span data-stu-id="561b5-349">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="561b5-350">修复了设置新的灵活保留策略时使用 Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy 出现的问题。该问题的具体表现是：在命令失败的同时，出现“不再支持使用 Azure 恢复服务保管库和策略配置长期保留策略。</span><span class="sxs-lookup"><span data-stu-id="561b5-350">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="561b5-351">请使用新的灵活保留策略提交请求”错误消息。</span><span class="sxs-lookup"><span data-stu-id="561b5-351">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="561b5-352">更新了与 Azure SQL 数据库/ElasticPool 的创建/更新相关的所有 cmdlet，允许使用新的数据库 API，而这些 cmdlet 支持的 SKU 属性则适用于规模和层相关属性。</span><span class="sxs-lookup"><span data-stu-id="561b5-352">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="561b5-353">更新的 cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="561b5-353">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="561b5-354">New-AzureRmSqlDatabase；Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="561b5-354">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="561b5-355">New-AzureRmSqlElasticPool；Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="561b5-355">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="561b5-356">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="561b5-356">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="561b5-357">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="561b5-357">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="561b5-358">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="561b5-358">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="561b5-359">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="561b5-359">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="561b5-360">更新了“Get-AzureRmTrafficManagerProfile”的参数，要求在使用 -Name 参数时使用 -ResourceGroupName 参数。</span><span class="sxs-lookup"><span data-stu-id="561b5-360">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>