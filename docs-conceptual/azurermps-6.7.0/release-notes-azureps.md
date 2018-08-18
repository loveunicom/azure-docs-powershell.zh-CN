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
ms.openlocfilehash: 2a6e20137f12ae9317c7eeed330a2433774e1ea9
ms.sourcegitcommit: 7df99dc139e93a8a4e6d5b1a27968857588d75dd
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/16/2018
ms.locfileid: "40106398"
---
# <a name="release-notes"></a><span data-ttu-id="52403-103">发行说明</span><span class="sxs-lookup"><span data-stu-id="52403-103">Release notes</span></span>

<span data-ttu-id="52403-104">下面是此版本中对 Azure PowerShell 所做的更改列表。</span><span class="sxs-lookup"><span data-stu-id="52403-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="670---august-2018"></a><span data-ttu-id="52403-105">6.7.0 - 2018 年 8 月</span><span class="sxs-lookup"><span data-stu-id="52403-105">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="52403-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="52403-106">AzureRM.Profile</span></span>
* <span data-ttu-id="52403-107">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="52403-107">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="52403-108">向默认的上下文名称添加用户 ID，避免上下文冲突</span><span class="sxs-lookup"><span data-stu-id="52403-108">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="52403-109">修复了 Clear-AzureRmContext 在选择上下文 #6398 时出现的问题</span><span class="sxs-lookup"><span data-stu-id="52403-109">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="52403-110">允许将租户域传递给“Connect-AzureRmAccount”的“-TenantId”参数</span><span class="sxs-lookup"><span data-stu-id="52403-110">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="52403-111">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="52403-111">Azure.Storage</span></span>
* <span data-ttu-id="52403-112">去除了 Azure 文件共享配额的 5TB 限制</span><span class="sxs-lookup"><span data-stu-id="52403-112">Remove the 5TB limitation for Azure File Share quota</span></span>
- <span data-ttu-id="52403-113">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="52403-113">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="52403-114">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="52403-114">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="52403-115">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="52403-115">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="52403-116">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="52403-116">Azure.AnalysisServices</span></span>
* <span data-ttu-id="52403-117">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="52403-117">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="52403-118">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="52403-118">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="52403-119">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="52403-119">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="52403-120">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="52403-120">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="52403-121">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="52403-121">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="52403-122">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="52403-122">AzureRM.Automation</span></span>
* <span data-ttu-id="52403-123">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="52403-123">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="52403-124">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="52403-124">AzureRM.Backup</span></span>
* <span data-ttu-id="52403-125">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="52403-125">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="52403-126">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="52403-126">AzureRM.Batch</span></span>
* <span data-ttu-id="52403-127">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="52403-127">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="52403-128">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="52403-128">AzureRM.Billing</span></span>
* <span data-ttu-id="52403-129">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="52403-129">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="52403-130">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="52403-130">AzureRM.Cdn</span></span>
* <span data-ttu-id="52403-131">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="52403-131">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="52403-132">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="52403-132">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="52403-133">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="52403-133">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="52403-134">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="52403-134">AzureRM.Compute</span></span>
* <span data-ttu-id="52403-135">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="52403-135">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="52403-136">为 New-AzureRmVmssConfig 增加了 EvictionPolicy 参数</span><span class="sxs-lookup"><span data-stu-id="52403-136">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="52403-137">在 New-AzureRmVm 的 DiskFileParameterSet 中使用默认位置（如果未指定 Location）</span><span class="sxs-lookup"><span data-stu-id="52403-137">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="52403-138">修复了 Save-AzureRmVMImage 中的参数说明</span><span class="sxs-lookup"><span data-stu-id="52403-138">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="52403-139">修复了某些单次传递相关方案的 Get-AzureRmVMDiskEncryptionStatus cmdlet</span><span class="sxs-lookup"><span data-stu-id="52403-139">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="52403-140">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="52403-140">AzureRM.Consumption</span></span>
* <span data-ttu-id="52403-141">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="52403-141">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="52403-142">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="52403-142">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="52403-143">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="52403-143">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="52403-144">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="52403-144">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="52403-145">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="52403-145">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="52403-146">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="52403-146">AzureRM.DataFactories</span></span>
* <span data-ttu-id="52403-147">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="52403-147">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="52403-148">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="52403-148">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="52403-149">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="52403-149">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="52403-150">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="52403-150">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="52403-151">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="52403-151">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="52403-152">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="52403-152">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="52403-153">修复了从 PowerShell 命令行设置 DebugPreference 时的调试问题</span><span class="sxs-lookup"><span data-stu-id="52403-153">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="52403-154">更新了 Set-AzureRmDataLakeStoreItemAcl 的示例</span><span class="sxs-lookup"><span data-stu-id="52403-154">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="52403-155">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="52403-155">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="52403-156">更新了 Set-AzureRmDataLakeStoreItemAclEntry 的示例</span><span class="sxs-lookup"><span data-stu-id="52403-156">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="52403-157">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="52403-157">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="52403-158">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="52403-158">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="52403-159">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="52403-159">AzureRM.Dns</span></span>
* <span data-ttu-id="52403-160">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="52403-160">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="52403-161">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="52403-161">AzureRM.EventGrid</span></span>
* <span data-ttu-id="52403-162">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="52403-162">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="52403-163">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="52403-163">AzureRM.EventHub</span></span>
* <span data-ttu-id="52403-164">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="52403-164">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="52403-165">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="52403-165">AzureRM.HDInsight</span></span>
* <span data-ttu-id="52403-166">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="52403-166">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="52403-167">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="52403-167">AzureRM.Insights</span></span>
* <span data-ttu-id="52403-168">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="52403-168">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="52403-169">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="52403-169">AzureRM.IotHub</span></span>
* <span data-ttu-id="52403-170">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="52403-170">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="52403-171">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="52403-171">AzureRM.KeyVault</span></span>
* <span data-ttu-id="52403-172">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="52403-172">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="52403-173">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="52403-173">AzureRM.LogicApp</span></span>
* <span data-ttu-id="52403-174">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="52403-174">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="52403-175">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="52403-175">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="52403-176">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="52403-176">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="52403-177">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="52403-177">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="52403-178">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="52403-178">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="52403-179">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="52403-179">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="52403-180">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="52403-180">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="52403-181">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="52403-181">AzureRM.Media</span></span>
* <span data-ttu-id="52403-182">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="52403-182">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="52403-183">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="52403-183">AzureRM.Network</span></span>
* <span data-ttu-id="52403-184">增加了 Set-AzureRmLocalNetworkGateway 的示例</span><span class="sxs-lookup"><span data-stu-id="52403-184">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="52403-185">增加了 Add-AzureRmVirtualNetworkGatewayIpConfig、Get-AzureRmVirtualNetworkGatewayConnectionSharedKey 和 New-AzureRmVirtualNetworkGatewayConnection 的示例和说明</span><span class="sxs-lookup"><span data-stu-id="52403-185">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="52403-186">增加了 Remove-AzureRmVirtualNetworkGatewayIpConfig 和 Reset-AzureRmVirtualNetworkGateway 的示例</span><span class="sxs-lookup"><span data-stu-id="52403-186">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="52403-187">增加了 Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey 的示例</span><span class="sxs-lookup"><span data-stu-id="52403-187">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="52403-188">增加了 Set-AzureRmVirtualNetworkGatewayConnectionSharedKey 的示例</span><span class="sxs-lookup"><span data-stu-id="52403-188">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="52403-189">增加了 Set-AzureRmVirtualNetworkGatewayConnection 的示例</span><span class="sxs-lookup"><span data-stu-id="52403-189">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="52403-190">使用最新的代码生成器重新生成了 ApplicationSecurityGroup、RouteTable 和 Usage 的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="52403-190">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="52403-191">阐明了在尝试获取的子网不存在时 Get-AzureRmVirtualNetworkSubnetConfig 的错误消息</span><span class="sxs-lookup"><span data-stu-id="52403-191">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="52403-192">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="52403-192">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="52403-193">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="52403-193">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="52403-194">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="52403-194">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="52403-195">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="52403-195">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="52403-196">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="52403-196">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="52403-197">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="52403-197">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="52403-198">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="52403-198">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="52403-199">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="52403-199">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="52403-200">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="52403-200">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="52403-201">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="52403-201">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="52403-202">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="52403-202">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="52403-203">为 Get-AzureRmRecoveryServicesBackItem cmdlet 增加了策略筛选器。</span><span class="sxs-lookup"><span data-stu-id="52403-203">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="52403-204">此命令返回受给定策略 ID 保护的备份项的列表。</span><span class="sxs-lookup"><span data-stu-id="52403-204">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="52403-205">已将 Microsoft.Azure.Management.RecoveryServices.Backup 更新到 3.0.0-preview 版本。</span><span class="sxs-lookup"><span data-stu-id="52403-205">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="52403-206">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="52403-206">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="52403-207">为 Restore-AzureRmRecoveryServicesBackupItem 增加了 TargetResourceGroupName 参数。</span><span class="sxs-lookup"><span data-stu-id="52403-207">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="52403-208">托管磁盘还原到的资源组。</span><span class="sxs-lookup"><span data-stu-id="52403-208">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="52403-209">适用于包含托管磁盘的 VM 的备份。</span><span class="sxs-lookup"><span data-stu-id="52403-209">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="52403-210">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="52403-210">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="52403-211">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="52403-211">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="52403-212">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="52403-212">AzureRM.RedisCache</span></span>
* <span data-ttu-id="52403-213">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="52403-213">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="52403-214">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="52403-214">AzureRM.Relay</span></span>
* <span data-ttu-id="52403-215">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="52403-215">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="52403-216">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="52403-216">AzureRM.Resources</span></span>
* <span data-ttu-id="52403-217">支持在订阅范围部署模板。</span><span class="sxs-lookup"><span data-stu-id="52403-217">Support template deployment at subscription scope.</span></span> <span data-ttu-id="52403-218">增加了新 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="52403-218">Add new Cmdlets:</span></span>
    - <span data-ttu-id="52403-219">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="52403-219">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="52403-220">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="52403-220">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="52403-221">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="52403-221">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="52403-222">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="52403-222">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="52403-223">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="52403-223">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="52403-224">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="52403-224">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="52403-225">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="52403-225">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="52403-226">修复了在将上下文传递给 Set-AzureRmResource 时引发错误的问题</span><span class="sxs-lookup"><span data-stu-id="52403-226">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="52403-227">修复了 New-AzureRmResourceGroupDeployment 中的示例</span><span class="sxs-lookup"><span data-stu-id="52403-227">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="52403-228">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="52403-228">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="52403-229">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="52403-229">AzureRM.Scheduler</span></span>
* <span data-ttu-id="52403-230">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="52403-230">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="52403-231">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="52403-231">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="52403-232">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="52403-232">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="52403-233">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="52403-233">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="52403-234">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="52403-234">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="52403-235">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="52403-235">AzureRM.Sql</span></span>
* <span data-ttu-id="52403-236">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="52403-236">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="52403-237">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="52403-237">AzureRM.Storage</span></span>
* <span data-ttu-id="52403-238">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="52403-238">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="52403-239">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="52403-239">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="52403-240">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="52403-240">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="52403-241">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="52403-241">AzureRM.Tags</span></span>
* <span data-ttu-id="52403-242">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="52403-242">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="52403-243">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="52403-243">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="52403-244">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="52403-244">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="52403-245">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="52403-245">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="52403-246">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="52403-246">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="52403-247">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="52403-247">AzureRM.Websites</span></span>
* <span data-ttu-id="52403-248">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="52403-248">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="52403-249">6.6.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="52403-249">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="52403-250">常规</span><span class="sxs-lookup"><span data-stu-id="52403-250">General</span></span>
* <span data-ttu-id="52403-251">更新了所有帮助文件，以包括完整参数类型和正确的输入/输出类型。</span><span class="sxs-lookup"><span data-stu-id="52403-251">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="52403-252">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="52403-252">AzureRM.Profile</span></span>
* <span data-ttu-id="52403-253">更新了 Common.Strategy 库，以便能够验证资源的当前配置是否与目标资源兼容。</span><span class="sxs-lookup"><span data-stu-id="52403-253">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="52403-254">在 Common.Storage 中添加了 ps1xml 类型</span><span class="sxs-lookup"><span data-stu-id="52403-254">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="52403-255">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="52403-255">Azure.Storage</span></span>
* <span data-ttu-id="52403-256">增加了从 DefaultProfile 获取存储上下文的支持</span><span class="sxs-lookup"><span data-stu-id="52403-256">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="52403-257">为 cmdlet 输出类型属性增加了 Ps1XmlAttribute。</span><span class="sxs-lookup"><span data-stu-id="52403-257">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="52403-258">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="52403-258">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="52403-259">修复了问题 https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="52403-259">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="52403-260">修复了 Automapper 中将 PsApiManagementApi 转换为 ApiContract 的 bug</span><span class="sxs-lookup"><span data-stu-id="52403-260">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="52403-261">修复了问题 https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="52403-261">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="52403-262">修复了 File.Save 中没有使用编码类型重载的 bug</span><span class="sxs-lookup"><span data-stu-id="52403-262">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="52403-263">修复了问题 https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="52403-263">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="52403-264">升级到了 4.0.3 Nuget版本，该版本修复了 apiId 上的模式异常</span><span class="sxs-lookup"><span data-stu-id="52403-264">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="52403-265">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="52403-265">AzureRM.Compute</span></span>
* <span data-ttu-id="52403-266">修复因使用 PremiumLRS 存储帐户类型重命名而在 New-AzureRmVm 中使用 DiskFileParameterSet 创建 VM 失败的问题。</span><span class="sxs-lookup"><span data-stu-id="52403-266">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="52403-267">修复 Invoke-AzureRmVMRunCommand cmdlet</span><span class="sxs-lookup"><span data-stu-id="52403-267">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="52403-268">更新 Get-AzureRmAvailabilitySet 以启用列出订阅中的所有可用性集。</span><span class="sxs-lookup"><span data-stu-id="52403-268">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="52403-269">（ResouceGroupName 参数现在是可选的。）</span><span class="sxs-lookup"><span data-stu-id="52403-269">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="52403-270">更新“New-AzureRmVm”的 SimpleParameterSet 以在符合条件的 VM 上启用加速网络。</span><span class="sxs-lookup"><span data-stu-id="52403-270">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="52403-271">将 New-AzureRmVmss 简单参数集更新为在用户指定的 LB 已存在时创建 vmss 失败。</span><span class="sxs-lookup"><span data-stu-id="52403-271">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="52403-272">更新 New-AzureRmDisk 的示例</span><span class="sxs-lookup"><span data-stu-id="52403-272">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="52403-273">添加“New-AzureRmVM”的示例</span><span class="sxs-lookup"><span data-stu-id="52403-273">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="52403-274">更新 Set-AzureRmVMOSDisk 的说明</span><span class="sxs-lookup"><span data-stu-id="52403-274">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="52403-275">更新 Set-AzureRmVMBginfoExtension 的示例 1 以更正拼写和前缀。</span><span class="sxs-lookup"><span data-stu-id="52403-275">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="52403-276">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="52403-276">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="52403-277">将 ADF .Net SDK 版本更新为 1.1.0。</span><span class="sxs-lookup"><span data-stu-id="52403-277">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="52403-278">支持跨数据工厂的自承载集成运行时共享。</span><span class="sxs-lookup"><span data-stu-id="52403-278">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="52403-279">将新参数 -SharedIntegrationRuntimeResourceId 添加到 Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet。</span><span class="sxs-lookup"><span data-stu-id="52403-279">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="52403-280">将新的可选参数 -LinkedDataFactoryName 添加到 Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet。</span><span class="sxs-lookup"><span data-stu-id="52403-280">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="52403-281">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="52403-281">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="52403-282">将数据平面 SDK (Microsoft.Azure.DataLake.Store) 版本更新为 1.1.9</span><span class="sxs-lookup"><span data-stu-id="52403-282">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="52403-283">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="52403-283">AzureRM.EventHub</span></span>
* <span data-ttu-id="52403-284">在删除 cmdlet 中更新了 InputObject 和 ResourceId 的管道</span><span class="sxs-lookup"><span data-stu-id="52403-284">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="52403-285">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="52403-285">AzureRM.Insights</span></span>
* <span data-ttu-id="52403-286">修复了帮助文件中 OutputType 的格式问题</span><span class="sxs-lookup"><span data-stu-id="52403-286">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="52403-287">使用 Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span><span class="sxs-lookup"><span data-stu-id="52403-287">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="52403-288">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="52403-288">AzureRM.KeyVault</span></span>
* <span data-ttu-id="52403-289">修复了 Set-AzureRmKeyVaultAccessPolicy 中的管道问题</span><span class="sxs-lookup"><span data-stu-id="52403-289">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="52403-290">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="52403-290">AzureRM.Network</span></span>
* <span data-ttu-id="52403-291">添加了 LoadBalancerInboundNatPoolConfig cmdlet 的示例。</span><span class="sxs-lookup"><span data-stu-id="52403-291">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="52403-292">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="52403-292">AzureRM.Resources</span></span>
* <span data-ttu-id="52403-293">修复了为“Get-AzureRmResource”同时提供标记名称和值时出现的问题</span><span class="sxs-lookup"><span data-stu-id="52403-293">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="52403-294">使用“Set-AzureRmResource”修复管道方案</span><span class="sxs-lookup"><span data-stu-id="52403-294">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="52403-295">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="52403-295">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="52403-296">在删除 cmdlet 中更新了 InputObject 和 ResourceId 的管道</span><span class="sxs-lookup"><span data-stu-id="52403-296">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="52403-297">修复了几个问题</span><span class="sxs-lookup"><span data-stu-id="52403-297">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="52403-298">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="52403-298">AzureRM.Sql</span></span>
* <span data-ttu-id="52403-299">使用以下 cmdlet 添加服务器高级威胁防护支持：</span><span class="sxs-lookup"><span data-stu-id="52403-299">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="52403-300">Enable-AzureRmSqlServerAdvancedThreatProtection；Disable-AzureRmSqlServerAdvancedThreatProtection；Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="52403-300">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="52403-301">使用以下 cmdlet 添加漏洞评估支持：</span><span class="sxs-lookup"><span data-stu-id="52403-301">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="52403-302">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings；Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings；Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="52403-302">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="52403-303">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline；Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline；Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="52403-303">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="52403-304">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan；Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord；Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="52403-304">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="52403-305">修复了 Remove-AzureRmSqlServerFirewallRule 中的示例</span><span class="sxs-lookup"><span data-stu-id="52403-305">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="52403-306">修复了 Get-AzureSqlSyncGroupLog 中非美国基础文化的日期时间处理错误</span><span class="sxs-lookup"><span data-stu-id="52403-306">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="52403-307">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="52403-307">AzureRM.Storage</span></span>
* <span data-ttu-id="52403-308">将 Ps1XmlAttribute 添加到 cmdlet 输出类型属性</span><span class="sxs-lookup"><span data-stu-id="52403-308">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="52403-309">在表视图中显示 StorageAccount cmdlet 输出</span><span class="sxs-lookup"><span data-stu-id="52403-309">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="52403-310">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="52403-310">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="52403-311">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="52403-311">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="52403-312">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="52403-312">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="52403-313">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="52403-313">AzureRM.Tags</span></span>
* <span data-ttu-id="52403-314">从 Tag cmdlet 帮助中删除不正确的语句</span><span class="sxs-lookup"><span data-stu-id="52403-314">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="52403-315">6.5.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="52403-315">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="52403-316">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="52403-316">AzureRM.Profile</span></span>
* <span data-ttu-id="52403-317">更新了“Get-AzureRmContextAutosaveSetting”的帮助</span><span class="sxs-lookup"><span data-stu-id="52403-317">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="52403-318">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="52403-318">Azure.Storage</span></span>
* <span data-ttu-id="52403-319">支持使用只写 Sas 令牌上传 Blob 或文件</span><span class="sxs-lookup"><span data-stu-id="52403-319">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="52403-320">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="52403-320">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="52403-321">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="52403-321">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="52403-322">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="52403-322">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="52403-323">将所需属性 ResourceGroupName 添加到 AS。</span><span class="sxs-lookup"><span data-stu-id="52403-323">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="52403-324">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="52403-324">AzureRM.Automation</span></span>
* <span data-ttu-id="52403-325">更新帮助并添加“New-AzureRMAutomationSchedule”的示例</span><span class="sxs-lookup"><span data-stu-id="52403-325">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="52403-326">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="52403-326">AzureRM.Compute</span></span>
* <span data-ttu-id="52403-327">将 -Tag 参数添加到 Update/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="52403-327">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="52403-328">添加“Add-AzureRmVmssExtension”的示例</span><span class="sxs-lookup"><span data-stu-id="52403-328">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="52403-329">添加“Remove-AzureRmVmssExtension”的示例</span><span class="sxs-lookup"><span data-stu-id="52403-329">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="52403-330">更新“Set-AzureRmVMAccessExtension”的帮助</span><span class="sxs-lookup"><span data-stu-id="52403-330">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="52403-331">更新 New-AzureRmVmss 的 SimpleParameterSet，以默认情况下将 SinglePlacementGroup 设置为false，并添加开关参数“SinglePlacementGroup”，使用户能够在单个放置组中创建 VMSS。</span><span class="sxs-lookup"><span data-stu-id="52403-331">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="52403-332">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="52403-332">AzureRM.EventHub</span></span>
* <span data-ttu-id="52403-333">向 PSEventHubDRConfigurationAttributes 类添加了一个只读属性“PendingReplicationOperationsCount”，该属性在复制过程中为挂起的复制操作计数</span><span class="sxs-lookup"><span data-stu-id="52403-333">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="52403-334">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="52403-334">AzureRM.KeyVault</span></span>
* <span data-ttu-id="52403-335">更新了 Set-AzureRmKeyVaultAccessPolicy 的错误消息</span><span class="sxs-lookup"><span data-stu-id="52403-335">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="52403-336">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="52403-336">AzureRM.LogicApp</span></span>
* <span data-ttu-id="52403-337">修复了 New-AzureRmLogicApp 中的“无法解析参数集”错误</span><span class="sxs-lookup"><span data-stu-id="52403-337">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="52403-338">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="52403-338">AzureRM.Network</span></span>
* <span data-ttu-id="52403-339">在多个租户中为 Set/Add-AzureRmVirtualNetworkPeering 启用跨虚拟网络对等互连</span><span class="sxs-lookup"><span data-stu-id="52403-339">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="52403-340">针对应用程序网关更新了以下 cmdlet</span><span class="sxs-lookup"><span data-stu-id="52403-340">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="52403-341">New-AzureRmApplicationGateway：添加了 EnableFIPS 标志和区域支持</span><span class="sxs-lookup"><span data-stu-id="52403-341">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="52403-342">New-AzureRmApplicationGatewaySku：添加了新的 sku Standard_v2 和 WAF_v2</span><span class="sxs-lookup"><span data-stu-id="52403-342">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="52403-343">Set-AzureRmApplicationGatewaySku：添加了新的 sku Standard_v2 和 WAF_v2</span><span class="sxs-lookup"><span data-stu-id="52403-343">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="52403-344">使用最新的生成器版本重新生成了 RouteTable cmdlet</span><span class="sxs-lookup"><span data-stu-id="52403-344">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="52403-345">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="52403-345">AzureRM.Relay</span></span>
* <span data-ttu-id="52403-346">更新了 Markdown 文件，其中修复了示例中的参数名称问题</span><span class="sxs-lookup"><span data-stu-id="52403-346">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="52403-347">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="52403-347">AzureRM.Resources</span></span>
* <span data-ttu-id="52403-348">更新了 Roleassignment 和 roledefinition cmdlet：</span><span class="sxs-lookup"><span data-stu-id="52403-348">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="52403-349">删除了作为分页的一部分完成的额外 roledefinition 调用。</span><span class="sxs-lookup"><span data-stu-id="52403-349">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="52403-350">修复了 Get-AzureRmRoleAssignment cmdlet</span><span class="sxs-lookup"><span data-stu-id="52403-350">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="52403-351">修复了 -ExpandPrincipalGroups 命令参数功能</span><span class="sxs-lookup"><span data-stu-id="52403-351">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="52403-352">修复了“Get-AzureRmResource”的问题，其中“-ResourceType”参数区分大小写</span><span class="sxs-lookup"><span data-stu-id="52403-352">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="52403-353">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="52403-353">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="52403-354">向列表 cmdlet 添加了 top 和 skip 参数</span><span class="sxs-lookup"><span data-stu-id="52403-354">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="52403-355">添加了标准到高级命名空间迁移 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="52403-355">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="52403-356">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="52403-356">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="52403-357">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="52403-357">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="52403-358">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="52403-358">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="52403-359">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="52403-359">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="52403-360">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="52403-360">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="52403-361">向 PSServiceBusDRConfigurationAttributes 类添加了一个只读属性“PendingReplicationOperationsCount”，该属性在复制过程中为挂起的复制操作计数</span><span class="sxs-lookup"><span data-stu-id="52403-361">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="52403-362">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="52403-362">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="52403-363">更新了“New-AzureRmServiceFabricCluster”的示例</span><span class="sxs-lookup"><span data-stu-id="52403-363">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="52403-364">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="52403-364">AzureRM.Sql</span></span>
* <span data-ttu-id="52403-365">为 Management.Sql 添加新的 Cmdlet，以允许客户将 TDE 证书添加到 Sql Server 实例或托管实例</span><span class="sxs-lookup"><span data-stu-id="52403-365">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="52403-366">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="52403-366">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="52403-367">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="52403-367">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="52403-368">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="52403-368">AzureRM.Websites</span></span>
* <span data-ttu-id="52403-369">设置为 false 时，`Set-AzureRmWebApp -AssignIdentity` 和 `Set-AzureRmWebAppSlot -AssignIdentity` 现在将从站点对象中删除 Identity 属性。同时移除预览标记。</span><span class="sxs-lookup"><span data-stu-id="52403-369">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="52403-370">`Get-AzureRmWebAppMetrics`、`Get-AzureRmAppServicePlanMetrics` 示例已更新</span><span class="sxs-lookup"><span data-stu-id="52403-370">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="52403-371">`Set-AzureRmWebApp -PhpVersion` 支持 off 作为有效的 php 版本</span><span class="sxs-lookup"><span data-stu-id="52403-371">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="52403-372">6.4.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="52403-372">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="52403-373">常规</span><span class="sxs-lookup"><span data-stu-id="52403-373">General</span></span>
* <span data-ttu-id="52403-374">修复了大多数模块的帮助文件中的 OutputType 格式问题</span><span class="sxs-lookup"><span data-stu-id="52403-374">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="52403-375">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="52403-375">AzureRM.Profile</span></span>
* <span data-ttu-id="52403-376">已将 Ps1Xml 属性添加到基本输出类型</span><span class="sxs-lookup"><span data-stu-id="52403-376">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="52403-377">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="52403-377">AzureRM.Compute</span></span>
* <span data-ttu-id="52403-378">VMSS 的 IP 标记功能</span><span class="sxs-lookup"><span data-stu-id="52403-378">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="52403-379">已添加“New-AzureRmVmssIpTagConfig”cmdlet</span><span class="sxs-lookup"><span data-stu-id="52403-379">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="52403-380">已将 IpTag 参数添加到 New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="52403-380">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="52403-381">VMSS 的自动 OS 回滚功能</span><span class="sxs-lookup"><span data-stu-id="52403-381">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="52403-382">已将 DisableAutoRollback 参数添加到 New-AzureRmVmssConfig 和 Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="52403-382">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="52403-383">VMSS 的 OS 升级历史记录功能</span><span class="sxs-lookup"><span data-stu-id="52403-383">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="52403-384">已将 OSUpgradeHistory 开关参数添加到 Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="52403-384">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="52403-385">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="52403-385">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="52403-386">通过以下命令添加目录 ACL 的支持：</span><span class="sxs-lookup"><span data-stu-id="52403-386">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="52403-387">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="52403-387">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="52403-388">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="52403-388">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="52403-389">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="52403-389">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="52403-390">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="52403-390">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="52403-391">为 Set-AzureRmDataLakeStoreItemAclEntry、Remove-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAcl 添加了取消支持和进度跟踪</span><span class="sxs-lookup"><span data-stu-id="52403-391">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="52403-392">为 Export-AzureRmDataLakeStoreChildItemProperties 添加了取消支持</span><span class="sxs-lookup"><span data-stu-id="52403-392">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="52403-393">修复了执行递归操作的 cmdlet 的调试消息刷新</span><span class="sxs-lookup"><span data-stu-id="52403-393">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="52403-394">修复了 DataLake cmdlet 的测试位置</span><span class="sxs-lookup"><span data-stu-id="52403-394">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="52403-395">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="52403-395">AzureRM.EventHub</span></span>
* <span data-ttu-id="52403-396">已将可选的 MaxCount 参数添加到“列出操作”cmdlet Get-AzureRmEventHub 和 Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="52403-396">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="52403-397">修复了 New-AzureRmEventHub cmdlet 的问题：创建新事件中心时至少需要一个参数。</span><span class="sxs-lookup"><span data-stu-id="52403-397">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="52403-398">提供了默认参数集。</span><span class="sxs-lookup"><span data-stu-id="52403-398">Provided Default Parameter set.</span></span>
* <span data-ttu-id="52403-399">已将可选参数 -KeyValue 添加到 New-AzureRmEventHubKey cmdlet，该参数可让用户提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="52403-399">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="52403-400">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="52403-400">AzureRM.KeyVault</span></span>
* <span data-ttu-id="52403-401">修复了 Get-AzureRmKeyVault -Tag 返回所有资源的问题</span><span class="sxs-lookup"><span data-stu-id="52403-401">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="52403-402">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="52403-402">AzureRM.Network</span></span>
* <span data-ttu-id="52403-403">为区域冗余的 VirtualNetworkGateways 公开新 SKU</span><span class="sxs-lookup"><span data-stu-id="52403-403">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="52403-404">通过 ARM 为以下功能添加了新命令：ExpressRoute 合作伙伴 API</span><span class="sxs-lookup"><span data-stu-id="52403-404">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="52403-405">添加了 Get-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="52403-405">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="52403-406">添加了 Set-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="52403-406">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="52403-407">添加了 Add-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="52403-407">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="52403-408">添加了 Get-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="52403-408">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="52403-409">添加了 Remove-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="52403-409">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="52403-410">添加了 Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="52403-410">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="52403-411">添加了 Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="52403-411">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="52403-412">添加了 Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="52403-412">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="52403-413">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="52403-413">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="52403-414">添加了 Get-AzureRmRecoveryServicesBackupStatus cmdlet。</span><span class="sxs-lookup"><span data-stu-id="52403-414">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="52403-415">此 cmdlet 采用 VM ID，并检查 VM 是否受订阅中的某个保管库保护。</span><span class="sxs-lookup"><span data-stu-id="52403-415">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="52403-416">如果存在此类保管库，该 cmdlet 会输出该保管库的详细信息。</span><span class="sxs-lookup"><span data-stu-id="52403-416">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="52403-417">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="52403-417">AzureRM.Resources</span></span>
* <span data-ttu-id="52403-418">更新了 Get-AzureRmPolicyAssignment cmdlet：</span><span class="sxs-lookup"><span data-stu-id="52403-418">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="52403-419">添加了在管理组级别列出 -Scope 值的支持</span><span class="sxs-lookup"><span data-stu-id="52403-419">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="52403-420">添加了在管理组级别使用 -Scope 值检索单个分配的支持</span><span class="sxs-lookup"><span data-stu-id="52403-420">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="52403-421">已将 -Effective 和 -All 开关添加到 control 参数</span><span class="sxs-lookup"><span data-stu-id="52403-421">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="52403-422">更新了 Get/New/Remove/Set-AzureRmPolicyDefinition cmdlet</span><span class="sxs-lookup"><span data-stu-id="52403-422">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="52403-423">添加了 -ManagementGroupName 参数，以将操作应用到给定的管理组</span><span class="sxs-lookup"><span data-stu-id="52403-423">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="52403-424">添加了 -SubscriptionId 参数，以将操作应用到给定的订阅</span><span class="sxs-lookup"><span data-stu-id="52403-424">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="52403-425">更新了 Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlet</span><span class="sxs-lookup"><span data-stu-id="52403-425">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="52403-426">添加了 -ManagementGroupName 参数，以将操作应用到给定的管理组</span><span class="sxs-lookup"><span data-stu-id="52403-426">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="52403-427">添加了 -SubscriptionId 参数，以将操作应用到给定的订阅</span><span class="sxs-lookup"><span data-stu-id="52403-427">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="52403-428">添加了使用 TemplateParameterObject 时在参数中指定 KeyVault 机密引用的支持</span><span class="sxs-lookup"><span data-stu-id="52403-428">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="52403-429">修复了忽略“New-AzureRmADAppCredential”的“-EndDate”参数的问题</span><span class="sxs-lookup"><span data-stu-id="52403-429">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="52403-430">修复了“Add-AzureRmADGroupMember”使用错误的 URL 发出请求的问题</span><span class="sxs-lookup"><span data-stu-id="52403-430">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="52403-431">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="52403-431">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="52403-432">已将可选参数 -KeyValue 添加到 New-AzureRmServiceBusKey cmdlet，该参数可让用户提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="52403-432">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="52403-433">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="52403-433">AzureRM.Sql</span></span>
* <span data-ttu-id="52403-434">在 AzureRmSqlDatabaseRestorePoint 帮助中澄清了 SQLDW 的用户定义还原点</span><span class="sxs-lookup"><span data-stu-id="52403-434">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="52403-435">更新了多个 cmdlet 中 -ComputeGeneration 参数的文档</span><span class="sxs-lookup"><span data-stu-id="52403-435">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="52403-436">6.3.0 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="52403-436">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="52403-437">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="52403-437">AzureRM.Profile</span></span>
* <span data-ttu-id="52403-438">更新了 Enable-AzureRmContextAutoSave 的错误消息</span><span class="sxs-lookup"><span data-stu-id="52403-438">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="52403-439">在运行没有旧上下文的“Connect-AzureRmAccount”时为每个订阅创建一个上下文</span><span class="sxs-lookup"><span data-stu-id="52403-439">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="52403-440">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="52403-440">Azure.Storage</span></span>
* <span data-ttu-id="52403-441">在帮助文件中增加了关于 -Permissions 参数的其他信息。</span><span class="sxs-lookup"><span data-stu-id="52403-441">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="52403-442">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="52403-442">AzureRM.Compute</span></span>
* <span data-ttu-id="52403-443">“Get-AzureRmVmDiskEncryptionStatus”修复了一个针对没有数据磁盘的 VM 观察到的问题</span><span class="sxs-lookup"><span data-stu-id="52403-443">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="52403-444">更新计算客户端库版本以修复以下 cmdlet</span><span class="sxs-lookup"><span data-stu-id="52403-444">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="52403-445">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="52403-445">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="52403-446">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="52403-446">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="52403-447">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="52403-447">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="52403-448">修复了以下 cmdlet，因此可以正确地显示“操作 ID”和“操作状态”：</span><span class="sxs-lookup"><span data-stu-id="52403-448">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="52403-449">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="52403-449">Start-AzureRmVM</span></span>
    - <span data-ttu-id="52403-450">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="52403-450">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="52403-451">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="52403-451">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="52403-452">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="52403-452">Set-AzureRmVM</span></span>
    - <span data-ttu-id="52403-453">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="52403-453">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="52403-454">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="52403-454">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="52403-455">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="52403-455">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="52403-456">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="52403-456">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="52403-457">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="52403-457">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="52403-458">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="52403-458">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="52403-459">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="52403-459">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="52403-460">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="52403-460">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="52403-461">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="52403-461">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="52403-462">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="52403-462">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="52403-463">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="52403-463">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="52403-464">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="52403-464">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="52403-465">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="52403-465">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="52403-466">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="52403-466">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="52403-467">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="52403-467">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="52403-468">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="52403-468">AzureRM.EventGrid</span></span>
* <span data-ttu-id="52403-469">在 Update-AzureRmEventGridSubscription cmdlet 中删除 SubjectBeginsWith/SubjectEndsWith 的 ValidateNotNullOrEmpty 验证条件，允许根据需要将这些参数更改为空字符串。</span><span class="sxs-lookup"><span data-stu-id="52403-469">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="52403-470">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="52403-470">AzureRM.KeyVault</span></span>
* <span data-ttu-id="52403-471">修复运行 Get-AzureRmKeyVault -Tag 时不返回任何标记的问题</span><span class="sxs-lookup"><span data-stu-id="52403-471">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="52403-472">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="52403-472">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="52403-473">策略见解 cmdlet 的公开发行版</span><span class="sxs-lookup"><span data-stu-id="52403-473">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="52403-474">使用 API 版本 2018-04-04</span><span class="sxs-lookup"><span data-stu-id="52403-474">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="52403-475">向 Get-AzureRmPolicyStateSummary 的结果添加了 PolicyDefinitionReferenceId</span><span class="sxs-lookup"><span data-stu-id="52403-475">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="52403-476">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="52403-476">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="52403-477">向 RecoveryServices.Backup cmdlet 添加了 -Vault 参数。</span><span class="sxs-lookup"><span data-stu-id="52403-477">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="52403-478">传递时，此项会替代 Set-AzureRmRecoveryServicesContext cmdlet。</span><span class="sxs-lookup"><span data-stu-id="52403-478">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="52403-479">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="52403-479">AzureRM.Sql</span></span>
* <span data-ttu-id="52403-480">更新了 Get-AzureRmSqlDatabaseExpanded 的帮助文件中的示例</span><span class="sxs-lookup"><span data-stu-id="52403-480">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="52403-481">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="52403-481">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="52403-482">更新了 Add-AzureRmTrafficManagerEndpointConfig 的帮助文件</span><span class="sxs-lookup"><span data-stu-id="52403-482">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="52403-483">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="52403-483">AzureRM.Websites</span></span>
* <span data-ttu-id="52403-484">更新了“Set-AzureRmWebApp”，在使用 -AssignIdentity 时不覆盖 AppSettings</span><span class="sxs-lookup"><span data-stu-id="52403-484">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="52403-485">更新了“New-AzureRmWebAppSlot”，允许使用 AppServicePlan 作为可选参数</span><span class="sxs-lookup"><span data-stu-id="52403-485">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="52403-486">6.2.1 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="52403-486">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="52403-487">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="52403-487">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="52403-488">更新了 PSWorkspace 模型，允许 Network 使用 type 作为参数</span><span class="sxs-lookup"><span data-stu-id="52403-488">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="52403-489">6.2.0 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="52403-489">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="52403-490">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="52403-490">AzureRM.Profile</span></span>
* <span data-ttu-id="52403-491">修复了 Newtonsoft.Json 的版本 10.0.3 在模块导入时无法加载的问题</span><span class="sxs-lookup"><span data-stu-id="52403-491">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="52403-492">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="52403-492">AzureRM.Compute</span></span>
* <span data-ttu-id="52403-493">VMSS VM 更新功能</span><span class="sxs-lookup"><span data-stu-id="52403-493">VMSS VM Update feature</span></span>
    - <span data-ttu-id="52403-494">增加了“Update-AzureRmVmssVM”和“New-AzureRmVMDataDisk”cmdlet</span><span class="sxs-lookup"><span data-stu-id="52403-494">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="52403-495">为“Add-AzureRmVMDataDisk”cmdlet 增加了 VirtualMachineScaleSetVM 参数，支持向 Vmss VM 添加数据磁盘。</span><span class="sxs-lookup"><span data-stu-id="52403-495">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="52403-496">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="52403-496">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="52403-497">将 ADF.Net SDK 版本更新到了 0.8.0-preview，其中包含以下更改：</span><span class="sxs-lookup"><span data-stu-id="52403-497">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="52403-498">增加了“配置工厂存储库”操作</span><span class="sxs-lookup"><span data-stu-id="52403-498">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="52403-499">更新了 QuickBooks LinkedService，可以公开 consumerKey 和 consumerSecret 属性</span><span class="sxs-lookup"><span data-stu-id="52403-499">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="52403-500">已将多个模型类型从 SecretBase 更新为 Object</span><span class="sxs-lookup"><span data-stu-id="52403-500">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="52403-501">增加了 Blob 事件触发器</span><span class="sxs-lookup"><span data-stu-id="52403-501">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="52403-502">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="52403-502">AzureRM.KeyVault</span></span>
* <span data-ttu-id="52403-503">使用示例输出更新了文档</span><span class="sxs-lookup"><span data-stu-id="52403-503">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="52403-504">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="52403-504">AzureRM.Network</span></span>
* <span data-ttu-id="52403-505">在网络观察程序 cmdlet 上启用了流量分析参数</span><span class="sxs-lookup"><span data-stu-id="52403-505">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="52403-506">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="52403-506">AzureRM.Resources</span></span>
* <span data-ttu-id="52403-507">修复了从“Get-AzureRmResource”返回的“PSResource”对象的“Properties”属性问题</span><span class="sxs-lookup"><span data-stu-id="52403-507">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="52403-508">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="52403-508">AzureRM.Scheduler</span></span>
* <span data-ttu-id="52403-509">修复了更新 ServiceBusQueueJob 无法设置新 Auth 值的问题</span><span class="sxs-lookup"><span data-stu-id="52403-509">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="52403-510">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="52403-510">AzureRM.Sql</span></span>
* <span data-ttu-id="52403-511">使用可选的 LicenseType 参数更新了以下 cmdlet</span><span class="sxs-lookup"><span data-stu-id="52403-511">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="52403-512">New-AzureRmSqlDatabase；Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="52403-512">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="52403-513">New-AzureRmSqlElasticPool；Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="52403-513">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="52403-514">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="52403-514">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="52403-515">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="52403-515">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="52403-516">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="52403-516">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="52403-517">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="52403-517">AzureRM.Websites</span></span>
* <span data-ttu-id="52403-518">更新了“New-AzureRMWebApp”，可以使用策略库中的常用算法。</span><span class="sxs-lookup"><span data-stu-id="52403-518">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="52403-519">6.1.0 - 2018 年 5 月</span><span class="sxs-lookup"><span data-stu-id="52403-519">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="52403-520">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="52403-520">AzureRM.Profile</span></span>
* <span data-ttu-id="52403-521">修复了运行“Clear-AzureRmContext”时会保留空上下文的问题，该上下文使用旧的默认上下文的名称，导致用户无法使用旧名称创建新的上下文</span><span class="sxs-lookup"><span data-stu-id="52403-521">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="52403-522">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="52403-522">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="52403-523">允许在 AS 上执行网关的关联/取消关联操作。</span><span class="sxs-lookup"><span data-stu-id="52403-523">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="52403-524">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="52403-524">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="52403-525">增加了对 ApiVersions、ApiReleases 和 ApiRevisions 的支持</span><span class="sxs-lookup"><span data-stu-id="52403-525">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="52403-526">增加了对 ServiceFabric 后端的支持</span><span class="sxs-lookup"><span data-stu-id="52403-526">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="52403-527">增加了对 Application Insights Logger 的支持</span><span class="sxs-lookup"><span data-stu-id="52403-527">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="52403-528">增加的支持包括认可“基本”SKU 是 API 管理服务的有效 SKU</span><span class="sxs-lookup"><span data-stu-id="52403-528">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="52403-529">增加的支持包括允许将专用 CA 颁发的证书作为根证书或 CA 证书安装</span><span class="sxs-lookup"><span data-stu-id="52403-529">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="52403-530">增加的支持包括通过 KeyVault 和多个代理主机名接受自定义 SSL 证书</span><span class="sxs-lookup"><span data-stu-id="52403-530">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="52403-531">增加了对 MSI 标识的支持</span><span class="sxs-lookup"><span data-stu-id="52403-531">Added support for MSI identity</span></span>
* <span data-ttu-id="52403-532">增加的支持包括通过 URL 接受策略 注意：以下 cmdlet 将在未来版本中弃用</span><span class="sxs-lookup"><span data-stu-id="52403-532">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="52403-533">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="52403-533">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="52403-534">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="52403-534">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="52403-535">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="52403-535">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="52403-536">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="52403-536">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="52403-537">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="52403-537">AzureRM.Batch</span></span>
* <span data-ttu-id="52403-538">发布新 cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="52403-538">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="52403-539">发布新 cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="52403-539">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="52403-540">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="52403-540">AzureRM.Consumption</span></span>
* <span data-ttu-id="52403-541">在 Cmdlet Get-AzureRmConsumptionUsageDetail 中增加了新参数 Expand、ResourceGroup、InstanceName、InstanceId、Tags、Top</span><span class="sxs-lookup"><span data-stu-id="52403-541">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="52403-542">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="52403-542">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="52403-543">修复了 Export-AzureRmDataLakeStoreChildItemProperties 的示例</span><span class="sxs-lookup"><span data-stu-id="52403-543">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="52403-544">修复了 Set-AzureRmDataLakeStoreItemAclEntry 中 Recurse 用例的 null 参数异常</span><span class="sxs-lookup"><span data-stu-id="52403-544">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="52403-545">修复了 Set-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAcl、Remove-AzureRmDataLakeStoreItemAclEntry 的帮助文件</span><span class="sxs-lookup"><span data-stu-id="52403-545">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="52403-546">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="52403-546">AzureRM.Network</span></span>
* <span data-ttu-id="52403-547">将网络 SDK 版本从 18.0.0-preview 升至 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="52403-547">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="52403-548">增加了用于创建协议配置的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="52403-548">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="52403-549">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="52403-549">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="52403-550">增加了用于向现有的快速路由线路添加新的线路连接的 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="52403-550">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="52403-551">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="52403-551">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="52403-552">增加了用于从现有的快速路由线路删除线路连接的 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="52403-552">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="52403-553">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="52403-553">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="52403-554">增加了用于检索线路连接的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="52403-554">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="52403-555">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="52403-555">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="52403-556">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="52403-556">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="52403-557">修复了使用生成的证书进行服务器身份验证的问题（问题 5998）</span><span class="sxs-lookup"><span data-stu-id="52403-557">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="52403-558">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="52403-558">AzureRM.Sql</span></span>
* <span data-ttu-id="52403-559">更新了审核 cmdlet，允许删除 AuditActions 或 AuditActionGroups</span><span class="sxs-lookup"><span data-stu-id="52403-559">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="52403-560">修复了设置新的灵活保留策略时使用 Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy 出现的问题。该问题的具体表现是：在命令失败的同时，出现“不再支持使用 Azure 恢复服务保管库和策略配置长期保留策略。</span><span class="sxs-lookup"><span data-stu-id="52403-560">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="52403-561">请使用新的灵活保留策略提交请求”错误消息。</span><span class="sxs-lookup"><span data-stu-id="52403-561">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="52403-562">更新了与 Azure SQL 数据库/ElasticPool 的创建/更新相关的所有 cmdlet，允许使用新的数据库 API，而这些 cmdlet 支持的 SKU 属性则适用于规模和层相关属性。</span><span class="sxs-lookup"><span data-stu-id="52403-562">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="52403-563">更新的 cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="52403-563">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="52403-564">New-AzureRmSqlDatabase；Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="52403-564">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="52403-565">New-AzureRmSqlElasticPool；Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="52403-565">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="52403-566">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="52403-566">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="52403-567">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="52403-567">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="52403-568">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="52403-568">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="52403-569">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="52403-569">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="52403-570">更新了“Get-AzureRmTrafficManagerProfile”的参数，要求在使用 -Name 参数时使用 -ResourceGroupName 参数。</span><span class="sxs-lookup"><span data-stu-id="52403-570">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
