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
ms.openlocfilehash: 255e26aea5ea3cea866faa0d095cdf643c8ef0a8
ms.sourcegitcommit: de0e60800df1add9f3400166faacca202ef567d9
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/03/2018
ms.locfileid: "37406153"
---
# <a name="release-notes"></a><span data-ttu-id="6e1b1-103">发行说明</span><span class="sxs-lookup"><span data-stu-id="6e1b1-103">Release notes</span></span>

<span data-ttu-id="6e1b1-104">下面是此版本中对 Azure PowerShell 所做的更改列表。</span><span class="sxs-lookup"><span data-stu-id="6e1b1-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="640---july-2018"></a><span data-ttu-id="6e1b1-105">6.4.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="6e1b1-105">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="6e1b1-106">常规</span><span class="sxs-lookup"><span data-stu-id="6e1b1-106">General</span></span>
* <span data-ttu-id="6e1b1-107">修复了大多数模块的帮助文件中的 OutputType 格式问题</span><span class="sxs-lookup"><span data-stu-id="6e1b1-107">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="6e1b1-108">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="6e1b1-108">AzureRM.Profile</span></span>
* <span data-ttu-id="6e1b1-109">已将 Ps1Xml 属性添加到基本输出类型</span><span class="sxs-lookup"><span data-stu-id="6e1b1-109">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="6e1b1-110">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="6e1b1-110">AzureRM.Compute</span></span>
* <span data-ttu-id="6e1b1-111">VMSS 的 IP 标记功能</span><span class="sxs-lookup"><span data-stu-id="6e1b1-111">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="6e1b1-112">已添加“New-AzureRmVmssIpTagConfig”cmdlet</span><span class="sxs-lookup"><span data-stu-id="6e1b1-112">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="6e1b1-113">已将 IpTag 参数添加到 New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="6e1b1-113">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="6e1b1-114">VMSS 的自动 OS 回滚功能</span><span class="sxs-lookup"><span data-stu-id="6e1b1-114">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="6e1b1-115">已将 DisableAutoRollback 参数添加到 New-AzureRmVmssConfig 和 Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6e1b1-115">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="6e1b1-116">VMSS 的 OS 升级历史记录功能</span><span class="sxs-lookup"><span data-stu-id="6e1b1-116">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="6e1b1-117">已将 OSUpgradeHistory 开关参数添加到 Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6e1b1-117">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="6e1b1-118">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="6e1b1-118">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="6e1b1-119">通过以下命令添加目录 ACL 的支持：</span><span class="sxs-lookup"><span data-stu-id="6e1b1-119">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="6e1b1-120">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="6e1b1-120">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="6e1b1-121">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="6e1b1-121">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="6e1b1-122">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="6e1b1-122">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="6e1b1-123">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6e1b1-123">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="6e1b1-124">为 Set-AzureRmDataLakeStoreItemAclEntry、Remove-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAcl 添加了取消支持和进度跟踪</span><span class="sxs-lookup"><span data-stu-id="6e1b1-124">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="6e1b1-125">为 Export-AzureRmDataLakeStoreChildItemProperties 添加了取消支持</span><span class="sxs-lookup"><span data-stu-id="6e1b1-125">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="6e1b1-126">修复了执行递归操作的 cmdlet 的调试消息刷新</span><span class="sxs-lookup"><span data-stu-id="6e1b1-126">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="6e1b1-127">修复了 DataLake cmdlet 的测试位置</span><span class="sxs-lookup"><span data-stu-id="6e1b1-127">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="6e1b1-128">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="6e1b1-128">AzureRM.EventHub</span></span>
* <span data-ttu-id="6e1b1-129">已将可选的 MaxCount 参数添加到“列出操作”cmdlet Get-AzureRmEventHub 和 Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="6e1b1-129">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="6e1b1-130">修复了 New-AzureRmEventHub cmdlet 的问题：创建新事件中心时至少需要一个参数。</span><span class="sxs-lookup"><span data-stu-id="6e1b1-130">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="6e1b1-131">提供了默认参数集。</span><span class="sxs-lookup"><span data-stu-id="6e1b1-131">Provided Default Parameter set.</span></span>
* <span data-ttu-id="6e1b1-132">已将可选参数 -KeyValue 添加到 New-AzureRmEventHubKey cmdlet，该参数可让用户提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="6e1b1-132">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="6e1b1-133">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6e1b1-133">AzureRM.KeyVault</span></span>
* <span data-ttu-id="6e1b1-134">修复了 Get-AzureRmKeyVault -Tag 返回所有资源的问题</span><span class="sxs-lookup"><span data-stu-id="6e1b1-134">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="6e1b1-135">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="6e1b1-135">AzureRM.Network</span></span>
* <span data-ttu-id="6e1b1-136">为区域冗余的 VirtualNetworkGateways 公开新 SKU</span><span class="sxs-lookup"><span data-stu-id="6e1b1-136">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="6e1b1-137">通过 ARM 为以下功能添加了新命令：ExpressRoute 合作伙伴 API</span><span class="sxs-lookup"><span data-stu-id="6e1b1-137">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="6e1b1-138">添加了 Get-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="6e1b1-138">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="6e1b1-139">添加了 Set-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="6e1b1-139">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="6e1b1-140">添加了 Add-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="6e1b1-140">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="6e1b1-141">添加了 Get-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="6e1b1-141">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="6e1b1-142">添加了 Remove-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="6e1b1-142">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="6e1b1-143">添加了 Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="6e1b1-143">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="6e1b1-144">添加了 Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="6e1b1-144">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="6e1b1-145">添加了 Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="6e1b1-145">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="6e1b1-146">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="6e1b1-146">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="6e1b1-147">添加了 Get-AzureRmRecoveryServicesBackupStatus cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6e1b1-147">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="6e1b1-148">此 cmdlet 采用 VM ID，并检查 VM 是否受订阅中的某个保管库保护。</span><span class="sxs-lookup"><span data-stu-id="6e1b1-148">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="6e1b1-149">如果存在此类保管库，该 cmdlet 会输出该保管库的详细信息。</span><span class="sxs-lookup"><span data-stu-id="6e1b1-149">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="6e1b1-150">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="6e1b1-150">AzureRM.Resources</span></span>
* <span data-ttu-id="6e1b1-151">更新了 Get-AzureRmPolicyAssignment cmdlet：</span><span class="sxs-lookup"><span data-stu-id="6e1b1-151">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="6e1b1-152">添加了在管理组级别列出 -Scope 值的支持</span><span class="sxs-lookup"><span data-stu-id="6e1b1-152">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="6e1b1-153">添加了在管理组级别使用 -Scope 值检索单个分配的支持</span><span class="sxs-lookup"><span data-stu-id="6e1b1-153">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="6e1b1-154">已将 -Effective 和 -All 开关添加到 control 参数</span><span class="sxs-lookup"><span data-stu-id="6e1b1-154">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="6e1b1-155">更新了 Get/New/Remove/Set-AzureRmPolicyDefinition cmdlet</span><span class="sxs-lookup"><span data-stu-id="6e1b1-155">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="6e1b1-156">添加了 -ManagementGroupName 参数，以将操作应用到给定的管理组</span><span class="sxs-lookup"><span data-stu-id="6e1b1-156">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="6e1b1-157">添加了 -SubscriptionId 参数，以将操作应用到给定的订阅</span><span class="sxs-lookup"><span data-stu-id="6e1b1-157">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="6e1b1-158">更新了 Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlet</span><span class="sxs-lookup"><span data-stu-id="6e1b1-158">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="6e1b1-159">添加了 -ManagementGroupName 参数，以将操作应用到给定的管理组</span><span class="sxs-lookup"><span data-stu-id="6e1b1-159">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="6e1b1-160">添加了 -SubscriptionId 参数，以将操作应用到给定的订阅</span><span class="sxs-lookup"><span data-stu-id="6e1b1-160">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="6e1b1-161">添加了使用 TemplateParameterObject 时在参数中指定 KeyVault 机密引用的支持</span><span class="sxs-lookup"><span data-stu-id="6e1b1-161">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="6e1b1-162">修复了忽略“New-AzureRmADAppCredential”的“-EndDate”参数的问题</span><span class="sxs-lookup"><span data-stu-id="6e1b1-162">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="6e1b1-163">修复了“Add-AzureRmADGroupMember”使用错误的 URL 发出请求的问题</span><span class="sxs-lookup"><span data-stu-id="6e1b1-163">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="6e1b1-164">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6e1b1-164">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="6e1b1-165">已将可选参数 -KeyValue 添加到 New-AzureRmServiceBusKey cmdlet，该参数可让用户提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="6e1b1-165">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="6e1b1-166">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="6e1b1-166">AzureRM.Sql</span></span>
* <span data-ttu-id="6e1b1-167">在 AzureRmSqlDatabaseRestorePoint 帮助中澄清了 SQLDW 的用户定义还原点</span><span class="sxs-lookup"><span data-stu-id="6e1b1-167">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="6e1b1-168">更新了多个 cmdlet 中 -ComputeGeneration 参数的文档</span><span class="sxs-lookup"><span data-stu-id="6e1b1-168">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="6e1b1-169">6.3.0 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="6e1b1-169">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="6e1b1-170">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="6e1b1-170">AzureRM.Profile</span></span>
* <span data-ttu-id="6e1b1-171">更新了 Enable-AzureRmContextAutoSave 的错误消息</span><span class="sxs-lookup"><span data-stu-id="6e1b1-171">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="6e1b1-172">在运行没有旧上下文的“Connect-AzureRmAccount”时为每个订阅创建一个上下文</span><span class="sxs-lookup"><span data-stu-id="6e1b1-172">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="6e1b1-173">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="6e1b1-173">Azure.Storage</span></span>
* <span data-ttu-id="6e1b1-174">在帮助文件中增加了关于 -Permissions 参数的其他信息。</span><span class="sxs-lookup"><span data-stu-id="6e1b1-174">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="6e1b1-175">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="6e1b1-175">AzureRM.Compute</span></span>
* <span data-ttu-id="6e1b1-176">“Get-AzureRmVmDiskEncryptionStatus”修复了一个针对没有数据磁盘的 VM 观察到的问题</span><span class="sxs-lookup"><span data-stu-id="6e1b1-176">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="6e1b1-177">更新计算客户端库版本以修复以下 cmdlet</span><span class="sxs-lookup"><span data-stu-id="6e1b1-177">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="6e1b1-178">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="6e1b1-178">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="6e1b1-179">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="6e1b1-179">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="6e1b1-180">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="6e1b1-180">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="6e1b1-181">修复了以下 cmdlet，因此可以正确地显示“操作 ID”和“操作状态”：</span><span class="sxs-lookup"><span data-stu-id="6e1b1-181">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="6e1b1-182">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6e1b1-182">Start-AzureRmVM</span></span>
    - <span data-ttu-id="6e1b1-183">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6e1b1-183">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="6e1b1-184">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6e1b1-184">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="6e1b1-185">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6e1b1-185">Set-AzureRmVM</span></span>
    - <span data-ttu-id="6e1b1-186">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="6e1b1-186">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="6e1b1-187">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6e1b1-187">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="6e1b1-188">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="6e1b1-188">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="6e1b1-189">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="6e1b1-189">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="6e1b1-190">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6e1b1-190">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="6e1b1-191">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6e1b1-191">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="6e1b1-192">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6e1b1-192">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="6e1b1-193">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6e1b1-193">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="6e1b1-194">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="6e1b1-194">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="6e1b1-195">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="6e1b1-195">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="6e1b1-196">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="6e1b1-196">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="6e1b1-197">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="6e1b1-197">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="6e1b1-198">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="6e1b1-198">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="6e1b1-199">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="6e1b1-199">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="6e1b1-200">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="6e1b1-200">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="6e1b1-201">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="6e1b1-201">AzureRM.EventGrid</span></span>
* <span data-ttu-id="6e1b1-202">在 Update-AzureRmEventGridSubscription cmdlet 中删除 SubjectBeginsWith/SubjectEndsWith 的 ValidateNotNullOrEmpty 验证条件，允许根据需要将这些参数更改为空字符串。</span><span class="sxs-lookup"><span data-stu-id="6e1b1-202">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="6e1b1-203">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6e1b1-203">AzureRM.KeyVault</span></span>
* <span data-ttu-id="6e1b1-204">修复运行 Get-AzureRmKeyVault -Tag 时不返回任何标记的问题</span><span class="sxs-lookup"><span data-stu-id="6e1b1-204">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="6e1b1-205">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6e1b1-205">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="6e1b1-206">策略见解 cmdlet 的公开发行版</span><span class="sxs-lookup"><span data-stu-id="6e1b1-206">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="6e1b1-207">使用 API 版本 2018-04-04</span><span class="sxs-lookup"><span data-stu-id="6e1b1-207">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="6e1b1-208">向 Get-AzureRmPolicyStateSummary 的结果添加了 PolicyDefinitionReferenceId</span><span class="sxs-lookup"><span data-stu-id="6e1b1-208">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="6e1b1-209">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="6e1b1-209">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="6e1b1-210">向 RecoveryServices.Backup cmdlet 添加了 -Vault 参数。</span><span class="sxs-lookup"><span data-stu-id="6e1b1-210">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="6e1b1-211">传递时，此项会替代 Set-AzureRmRecoveryServicesContext cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6e1b1-211">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="6e1b1-212">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="6e1b1-212">AzureRM.Sql</span></span>
* <span data-ttu-id="6e1b1-213">更新了 Get-AzureRmSqlDatabaseExpanded 的帮助文件中的示例</span><span class="sxs-lookup"><span data-stu-id="6e1b1-213">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="6e1b1-214">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="6e1b1-214">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="6e1b1-215">更新了 Add-AzureRmTrafficManagerEndpointConfig 的帮助文件</span><span class="sxs-lookup"><span data-stu-id="6e1b1-215">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="6e1b1-216">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="6e1b1-216">AzureRM.Websites</span></span>
* <span data-ttu-id="6e1b1-217">更新了“Set-AzureRmWebApp”，在使用 -AssignIdentity 时不覆盖 AppSettings</span><span class="sxs-lookup"><span data-stu-id="6e1b1-217">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="6e1b1-218">更新了“New-AzureRmWebAppSlot”，允许使用 AppServicePlan 作为可选参数</span><span class="sxs-lookup"><span data-stu-id="6e1b1-218">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="6e1b1-219">6.2.1 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="6e1b1-219">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="6e1b1-220">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6e1b1-220">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="6e1b1-221">更新了 PSWorkspace 模型，允许 Network 使用 type 作为参数</span><span class="sxs-lookup"><span data-stu-id="6e1b1-221">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="6e1b1-222">6.2.0 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="6e1b1-222">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="6e1b1-223">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="6e1b1-223">AzureRM.Profile</span></span>
* <span data-ttu-id="6e1b1-224">修复了 Newtonsoft.Json 的版本 10.0.3 在模块导入时无法加载的问题</span><span class="sxs-lookup"><span data-stu-id="6e1b1-224">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="6e1b1-225">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="6e1b1-225">AzureRM.Compute</span></span>
* <span data-ttu-id="6e1b1-226">VMSS VM 更新功能</span><span class="sxs-lookup"><span data-stu-id="6e1b1-226">VMSS VM Update feature</span></span>
    - <span data-ttu-id="6e1b1-227">增加了“Update-AzureRmVmssVM”和“New-AzureRmVMDataDisk”cmdlet</span><span class="sxs-lookup"><span data-stu-id="6e1b1-227">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="6e1b1-228">为“Add-AzureRmVMDataDisk”cmdlet 增加了 VirtualMachineScaleSetVM 参数，支持向 Vmss VM 添加数据磁盘。</span><span class="sxs-lookup"><span data-stu-id="6e1b1-228">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="6e1b1-229">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="6e1b1-229">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="6e1b1-230">将 ADF.Net SDK 版本更新到了 0.8.0-preview，其中包含以下更改：</span><span class="sxs-lookup"><span data-stu-id="6e1b1-230">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="6e1b1-231">增加了“配置工厂存储库”操作</span><span class="sxs-lookup"><span data-stu-id="6e1b1-231">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="6e1b1-232">更新了 QuickBooks LinkedService，可以公开 consumerKey 和 consumerSecret 属性</span><span class="sxs-lookup"><span data-stu-id="6e1b1-232">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="6e1b1-233">已将多个模型类型从 SecretBase 更新为 Object</span><span class="sxs-lookup"><span data-stu-id="6e1b1-233">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="6e1b1-234">增加了 Blob 事件触发器</span><span class="sxs-lookup"><span data-stu-id="6e1b1-234">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="6e1b1-235">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6e1b1-235">AzureRM.KeyVault</span></span>
* <span data-ttu-id="6e1b1-236">使用示例输出更新了文档</span><span class="sxs-lookup"><span data-stu-id="6e1b1-236">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="6e1b1-237">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="6e1b1-237">AzureRM.Network</span></span>
* <span data-ttu-id="6e1b1-238">在网络观察程序 cmdlet 上启用了流量分析参数</span><span class="sxs-lookup"><span data-stu-id="6e1b1-238">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="6e1b1-239">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="6e1b1-239">AzureRM.Resources</span></span>
* <span data-ttu-id="6e1b1-240">修复了从“Get-AzureRmResource”返回的“PSResource”对象的“Properties”属性问题</span><span class="sxs-lookup"><span data-stu-id="6e1b1-240">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="6e1b1-241">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="6e1b1-241">AzureRM.Scheduler</span></span>
* <span data-ttu-id="6e1b1-242">修复了更新 ServiceBusQueueJob 无法设置新 Auth 值的问题</span><span class="sxs-lookup"><span data-stu-id="6e1b1-242">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="6e1b1-243">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="6e1b1-243">AzureRM.Sql</span></span>
* <span data-ttu-id="6e1b1-244">使用可选的 LicenseType 参数更新了以下 cmdlet</span><span class="sxs-lookup"><span data-stu-id="6e1b1-244">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="6e1b1-245">New-AzureRmSqlDatabase；Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6e1b1-245">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="6e1b1-246">New-AzureRmSqlElasticPool；Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="6e1b1-246">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="6e1b1-247">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="6e1b1-247">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="6e1b1-248">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="6e1b1-248">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="6e1b1-249">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6e1b1-249">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="6e1b1-250">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="6e1b1-250">AzureRM.Websites</span></span>
* <span data-ttu-id="6e1b1-251">更新了“New-AzureRMWebApp”，可以使用策略库中的常用算法。</span><span class="sxs-lookup"><span data-stu-id="6e1b1-251">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="6e1b1-252">6.1.0 - 2018 年 5 月</span><span class="sxs-lookup"><span data-stu-id="6e1b1-252">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="6e1b1-253">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="6e1b1-253">AzureRM.Profile</span></span>
* <span data-ttu-id="6e1b1-254">修复了运行“Clear-AzureRmContext”时会保留空上下文的问题，该上下文使用旧的默认上下文的名称，导致用户无法使用旧名称创建新的上下文</span><span class="sxs-lookup"><span data-stu-id="6e1b1-254">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="6e1b1-255">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6e1b1-255">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="6e1b1-256">允许在 AS 上执行网关的关联/取消关联操作。</span><span class="sxs-lookup"><span data-stu-id="6e1b1-256">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="6e1b1-257">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6e1b1-257">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="6e1b1-258">增加了对 ApiVersions、ApiReleases 和 ApiRevisions 的支持</span><span class="sxs-lookup"><span data-stu-id="6e1b1-258">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="6e1b1-259">增加了对 ServiceFabric 后端的支持</span><span class="sxs-lookup"><span data-stu-id="6e1b1-259">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="6e1b1-260">增加了对 Application Insights Logger 的支持</span><span class="sxs-lookup"><span data-stu-id="6e1b1-260">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="6e1b1-261">增加的支持包括认可“基本”SKU 是 API 管理服务的有效 SKU</span><span class="sxs-lookup"><span data-stu-id="6e1b1-261">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="6e1b1-262">增加的支持包括允许将专用 CA 颁发的证书作为根证书或 CA 证书安装</span><span class="sxs-lookup"><span data-stu-id="6e1b1-262">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="6e1b1-263">增加的支持包括通过 KeyVault 和多个代理主机名接受自定义 SSL 证书</span><span class="sxs-lookup"><span data-stu-id="6e1b1-263">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="6e1b1-264">增加了对 MSI 标识的支持</span><span class="sxs-lookup"><span data-stu-id="6e1b1-264">Added support for MSI identity</span></span>
* <span data-ttu-id="6e1b1-265">增加的支持包括通过 URL 接受策略 注意：以下 cmdlet 将在未来版本中弃用</span><span class="sxs-lookup"><span data-stu-id="6e1b1-265">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="6e1b1-266">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="6e1b1-266">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="6e1b1-267">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="6e1b1-267">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="6e1b1-268">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="6e1b1-268">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="6e1b1-269">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="6e1b1-269">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="6e1b1-270">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="6e1b1-270">AzureRM.Batch</span></span>
* <span data-ttu-id="6e1b1-271">发布新 cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="6e1b1-271">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="6e1b1-272">发布新 cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="6e1b1-272">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="6e1b1-273">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="6e1b1-273">AzureRM.Consumption</span></span>
* <span data-ttu-id="6e1b1-274">在 Cmdlet Get-AzureRmConsumptionUsageDetail 中增加了新参数 Expand、ResourceGroup、InstanceName、InstanceId、Tags、Top</span><span class="sxs-lookup"><span data-stu-id="6e1b1-274">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="6e1b1-275">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6e1b1-275">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="6e1b1-276">修复了 Export-AzureRmDataLakeStoreChildItemProperties 的示例</span><span class="sxs-lookup"><span data-stu-id="6e1b1-276">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="6e1b1-277">修复了 Set-AzureRmDataLakeStoreItemAclEntry 中 Recurse 用例的 null 参数异常</span><span class="sxs-lookup"><span data-stu-id="6e1b1-277">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="6e1b1-278">修复了 Set-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAcl、Remove-AzureRmDataLakeStoreItemAclEntry 的帮助文件</span><span class="sxs-lookup"><span data-stu-id="6e1b1-278">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="6e1b1-279">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="6e1b1-279">AzureRM.Network</span></span>
* <span data-ttu-id="6e1b1-280">将网络 SDK 版本从 18.0.0-preview 升至 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="6e1b1-280">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="6e1b1-281">增加了用于创建协议配置的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="6e1b1-281">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="6e1b1-282">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="6e1b1-282">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="6e1b1-283">增加了用于向现有的快速路由线路添加新的线路连接的 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6e1b1-283">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="6e1b1-284">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="6e1b1-284">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="6e1b1-285">增加了用于从现有的快速路由线路删除线路连接的 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6e1b1-285">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="6e1b1-286">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="6e1b1-286">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="6e1b1-287">增加了用于检索线路连接的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="6e1b1-287">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="6e1b1-288">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="6e1b1-288">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="6e1b1-289">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6e1b1-289">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="6e1b1-290">修复了使用生成的证书进行服务器身份验证的问题（问题 5998）</span><span class="sxs-lookup"><span data-stu-id="6e1b1-290">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="6e1b1-291">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="6e1b1-291">AzureRM.Sql</span></span>
* <span data-ttu-id="6e1b1-292">更新了审核 cmdlet，允许删除 AuditActions 或 AuditActionGroups</span><span class="sxs-lookup"><span data-stu-id="6e1b1-292">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="6e1b1-293">修复了设置新的灵活保留策略时使用 Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy 出现的问题。该问题的具体表现是：在命令失败的同时，出现“不再支持使用 Azure 恢复服务保管库和策略配置长期保留策略。</span><span class="sxs-lookup"><span data-stu-id="6e1b1-293">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="6e1b1-294">请使用新的灵活保留策略提交请求”错误消息。</span><span class="sxs-lookup"><span data-stu-id="6e1b1-294">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="6e1b1-295">更新了与 Azure SQL 数据库/ElasticPool 的创建/更新相关的所有 cmdlet，允许使用新的数据库 API，而这些 cmdlet 支持的 SKU 属性则适用于规模和层相关属性。</span><span class="sxs-lookup"><span data-stu-id="6e1b1-295">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="6e1b1-296">更新的 cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="6e1b1-296">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="6e1b1-297">New-AzureRmSqlDatabase；Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6e1b1-297">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="6e1b1-298">New-AzureRmSqlElasticPool；Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="6e1b1-298">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="6e1b1-299">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="6e1b1-299">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="6e1b1-300">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="6e1b1-300">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="6e1b1-301">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6e1b1-301">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="6e1b1-302">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="6e1b1-302">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="6e1b1-303">更新了“Get-AzureRmTrafficManagerProfile”的参数，要求在使用 -Name 参数时使用 -ResourceGroupName 参数。</span><span class="sxs-lookup"><span data-stu-id="6e1b1-303">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>