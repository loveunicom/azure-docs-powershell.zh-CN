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
ms.openlocfilehash: f4f3141998be14f0b5b223aed1af283534bf061d
ms.sourcegitcommit: 971f19181b2cd68b7845bbebdb22858c06541c8c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/06/2018
ms.locfileid: "43383832"
---
# <a name="release-notes"></a><span data-ttu-id="10f51-103">发行说明</span><span class="sxs-lookup"><span data-stu-id="10f51-103">Release notes</span></span>

<span data-ttu-id="10f51-104">下面是此版本中对 Azure PowerShell 所做的更改列表。</span><span class="sxs-lookup"><span data-stu-id="10f51-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="681---august-2018"></a><span data-ttu-id="10f51-105">6.8.1 - 2018 年 8 月</span><span class="sxs-lookup"><span data-stu-id="10f51-105">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="10f51-106">常规</span><span class="sxs-lookup"><span data-stu-id="10f51-106">General</span></span>
* <span data-ttu-id="10f51-107">解决了未设置默认资源组的问题。</span><span class="sxs-lookup"><span data-stu-id="10f51-107">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="10f51-108">更新了公共运行时程序集</span><span class="sxs-lookup"><span data-stu-id="10f51-108">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="10f51-109">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="10f51-109">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="10f51-110">解决了未设置默认资源组的问题。</span><span class="sxs-lookup"><span data-stu-id="10f51-110">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="10f51-111">修复了问题 https://github.com/Azure/azure-powershell/issues/6603</span><span class="sxs-lookup"><span data-stu-id="10f51-111">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="10f51-112">Import-AzureRmApiManagementApi 和 \*-AzureRmApiManagementCertificate cmdlet 现在处理相对路径</span><span class="sxs-lookup"><span data-stu-id="10f51-112">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="10f51-113">修复了问题 https://github.com/Azure/azure-powershell/issues/6879</span><span class="sxs-lookup"><span data-stu-id="10f51-113">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="10f51-114">CertificateInformation 是使 Set-AzureRmApiManagement cmdlet 可以正常工作的可设置属性。</span><span class="sxs-lookup"><span data-stu-id="10f51-114">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="10f51-115">通过升级到 4.0.4-preview nuget 进行了修复</span><span class="sxs-lookup"><span data-stu-id="10f51-115">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="10f51-116">修复了问题 https://github.com/Azure/azure-powershell/issues/6853</span><span class="sxs-lookup"><span data-stu-id="10f51-116">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="10f51-117">针对按产品名称进行的搜索修复了 Odata 筛选器</span><span class="sxs-lookup"><span data-stu-id="10f51-117">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="10f51-118">修复了问题 https://github.com/Azure/azure-powershell/issues/6814</span><span class="sxs-lookup"><span data-stu-id="10f51-118">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="10f51-119">针对按 API 名称进行的搜索修复了 Odata 筛选器</span><span class="sxs-lookup"><span data-stu-id="10f51-119">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="10f51-120">添加了对 AzureMonitor 记录器的支持</span><span class="sxs-lookup"><span data-stu-id="10f51-120">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="10f51-121">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="10f51-121">AzureRM.Compute</span></span>
* <span data-ttu-id="10f51-122">解决了错误输出中缺少目标的问题。</span><span class="sxs-lookup"><span data-stu-id="10f51-122">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="10f51-123">解决了带有托管磁盘的 VM 的存储帐户类型问题</span><span class="sxs-lookup"><span data-stu-id="10f51-123">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="10f51-124">解决了未设置默认资源组的问题。</span><span class="sxs-lookup"><span data-stu-id="10f51-124">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="10f51-125">解决了在其他环境（例如 Azure 中国）中使用 AEM 扩展 cmdlet 的问题</span><span class="sxs-lookup"><span data-stu-id="10f51-125">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="10f51-126">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="10f51-126">AzureRM.Network</span></span>
* <span data-ttu-id="10f51-127">将默认 cmdlet 输出表示形式更改为表视图</span><span class="sxs-lookup"><span data-stu-id="10f51-127">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="10f51-128">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="10f51-128">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="10f51-129">修复了在尝试扩展停用的容量时 Update-AzureRmPowerBIEmbeddedCapacity 中出现的故障</span><span class="sxs-lookup"><span data-stu-id="10f51-129">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="10f51-130">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="10f51-130">AzureRM.Resources</span></span>
* <span data-ttu-id="10f51-131">解决了从市场创建托管应用程序的问题。</span><span class="sxs-lookup"><span data-stu-id="10f51-131">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="10f51-132">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="10f51-132">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="10f51-133">修复的问题</span><span class="sxs-lookup"><span data-stu-id="10f51-133">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="10f51-134">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="10f51-134">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="10f51-135">添加了对 MultiValue 路由方法的支持</span><span class="sxs-lookup"><span data-stu-id="10f51-135">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="10f51-136">MultiValue 路由的新参数“MaxReturn”</span><span class="sxs-lookup"><span data-stu-id="10f51-136">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="10f51-137">添加了对 Subnet 路由方法的支持</span><span class="sxs-lookup"><span data-stu-id="10f51-137">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="10f51-138">对终结点中的 IP 地址范围（子网）的支持</span><span class="sxs-lookup"><span data-stu-id="10f51-138">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="10f51-139">添加了对配置文件中的自定义标头的支持</span><span class="sxs-lookup"><span data-stu-id="10f51-139">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="10f51-140">添加了对配置文件中的预期状态代码范围的支持</span><span class="sxs-lookup"><span data-stu-id="10f51-140">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="10f51-141">添加了对终结点中的自定义标头的支持</span><span class="sxs-lookup"><span data-stu-id="10f51-141">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="10f51-142">6.8.0 - 2018 年 8 月</span><span class="sxs-lookup"><span data-stu-id="10f51-142">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="10f51-143">常规</span><span class="sxs-lookup"><span data-stu-id="10f51-143">General</span></span>
* <span data-ttu-id="10f51-144">解决了未设置默认资源组的问题。</span><span class="sxs-lookup"><span data-stu-id="10f51-144">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="10f51-145">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="10f51-145">AzureRM.Profile</span></span>
* <span data-ttu-id="10f51-146">为在执行 Connect-AzureRmAccount 期间返回的令牌添加了“过期”属性</span><span class="sxs-lookup"><span data-stu-id="10f51-146">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="10f51-147">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="10f51-147">AzureRM.Compute</span></span>
* <span data-ttu-id="10f51-148">解决了错误输出中缺少目标的问题。</span><span class="sxs-lookup"><span data-stu-id="10f51-148">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="10f51-149">解决了带有托管磁盘的 VM 的存储帐户类型问题</span><span class="sxs-lookup"><span data-stu-id="10f51-149">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="10f51-150">解决了在其他环境（例如 Azure 中国）中使用 AEM 扩展 cmdlet 的问题</span><span class="sxs-lookup"><span data-stu-id="10f51-150">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="10f51-151">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="10f51-151">AzureRM.IotHub</span></span>
* <span data-ttu-id="10f51-152">修复了 New-AzureRmIotHubExportDevices 和 New-AzureRmIotHubImportDevices的示例</span><span class="sxs-lookup"><span data-stu-id="10f51-152">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="10f51-153">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="10f51-153">AzureRM.Network</span></span>
* <span data-ttu-id="10f51-154">将默认模型表示形式更改为表视图</span><span class="sxs-lookup"><span data-stu-id="10f51-154">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="10f51-155">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="10f51-155">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="10f51-156">修复了在尝试扩展停用的容量时 Update-AzureRmPowerBIEmbeddedCapacity 中出现的故障</span><span class="sxs-lookup"><span data-stu-id="10f51-156">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="10f51-157">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="10f51-157">AzureRM.Resources</span></span>
* <span data-ttu-id="10f51-158">解决了从市场创建托管应用程序的问题。</span><span class="sxs-lookup"><span data-stu-id="10f51-158">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="10f51-159">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="10f51-159">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="10f51-160">解决了以下问题</span><span class="sxs-lookup"><span data-stu-id="10f51-160">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="10f51-161">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="10f51-161">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="10f51-162">对 MultiValue 路由方法的支持</span><span class="sxs-lookup"><span data-stu-id="10f51-162">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="10f51-163">MultiValue 路由的新参数“MaxReturn”</span><span class="sxs-lookup"><span data-stu-id="10f51-163">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="10f51-164">对 Subnet 路由方法的支持</span><span class="sxs-lookup"><span data-stu-id="10f51-164">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="10f51-165">对终结点中的 IP 地址范围（子网）的支持</span><span class="sxs-lookup"><span data-stu-id="10f51-165">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="10f51-166">对配置文件中的自定义标头的支持</span><span class="sxs-lookup"><span data-stu-id="10f51-166">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="10f51-167">对配置文件中的预期状态代码范围的支持</span><span class="sxs-lookup"><span data-stu-id="10f51-167">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="10f51-168">对终结点中的自定义标头的支持</span><span class="sxs-lookup"><span data-stu-id="10f51-168">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="10f51-169">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="10f51-169">AzureRM.Websites</span></span>
* <span data-ttu-id="10f51-170">解决了错误地设置默认资源组的问题。</span><span class="sxs-lookup"><span data-stu-id="10f51-170">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="10f51-171">6.7.0 - 2018 年 8 月</span><span class="sxs-lookup"><span data-stu-id="10f51-171">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="10f51-172">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="10f51-172">AzureRM.Profile</span></span>
* <span data-ttu-id="10f51-173">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="10f51-173">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="10f51-174">向默认的上下文名称添加用户 ID，避免上下文冲突</span><span class="sxs-lookup"><span data-stu-id="10f51-174">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="10f51-175">修复了 Clear-AzureRmContext 在选择上下文 #6398 时出现的问题</span><span class="sxs-lookup"><span data-stu-id="10f51-175">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="10f51-176">允许将租户域传递给“Connect-AzureRmAccount”的“-TenantId”参数</span><span class="sxs-lookup"><span data-stu-id="10f51-176">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="10f51-177">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="10f51-177">Azure.Storage</span></span>
* <span data-ttu-id="10f51-178">去除了 Azure 文件共享配额的 5TB 限制</span><span class="sxs-lookup"><span data-stu-id="10f51-178">Remove the 5TB limitation for Azure File Share quota</span></span>
- <span data-ttu-id="10f51-179">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="10f51-179">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="10f51-180">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="10f51-180">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="10f51-181">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="10f51-181">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="10f51-182">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="10f51-182">Azure.AnalysisServices</span></span>
* <span data-ttu-id="10f51-183">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="10f51-183">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="10f51-184">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="10f51-184">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="10f51-185">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="10f51-185">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="10f51-186">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="10f51-186">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="10f51-187">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="10f51-187">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="10f51-188">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="10f51-188">AzureRM.Automation</span></span>
* <span data-ttu-id="10f51-189">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="10f51-189">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="10f51-190">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="10f51-190">AzureRM.Backup</span></span>
* <span data-ttu-id="10f51-191">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="10f51-191">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="10f51-192">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="10f51-192">AzureRM.Batch</span></span>
* <span data-ttu-id="10f51-193">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="10f51-193">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="10f51-194">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="10f51-194">AzureRM.Billing</span></span>
* <span data-ttu-id="10f51-195">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="10f51-195">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="10f51-196">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="10f51-196">AzureRM.Cdn</span></span>
* <span data-ttu-id="10f51-197">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="10f51-197">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="10f51-198">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="10f51-198">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="10f51-199">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="10f51-199">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="10f51-200">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="10f51-200">AzureRM.Compute</span></span>
* <span data-ttu-id="10f51-201">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="10f51-201">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="10f51-202">为 New-AzureRmVmssConfig 增加了 EvictionPolicy 参数</span><span class="sxs-lookup"><span data-stu-id="10f51-202">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="10f51-203">在 New-AzureRmVm 的 DiskFileParameterSet 中使用默认位置（如果未指定 Location）</span><span class="sxs-lookup"><span data-stu-id="10f51-203">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="10f51-204">修复了 Save-AzureRmVMImage 中的参数说明</span><span class="sxs-lookup"><span data-stu-id="10f51-204">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="10f51-205">修复了某些单次传递相关方案的 Get-AzureRmVMDiskEncryptionStatus cmdlet</span><span class="sxs-lookup"><span data-stu-id="10f51-205">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="10f51-206">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="10f51-206">AzureRM.Consumption</span></span>
* <span data-ttu-id="10f51-207">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="10f51-207">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="10f51-208">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="10f51-208">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="10f51-209">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="10f51-209">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="10f51-210">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="10f51-210">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="10f51-211">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="10f51-211">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="10f51-212">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="10f51-212">AzureRM.DataFactories</span></span>
* <span data-ttu-id="10f51-213">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="10f51-213">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="10f51-214">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="10f51-214">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="10f51-215">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="10f51-215">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="10f51-216">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="10f51-216">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="10f51-217">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="10f51-217">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="10f51-218">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="10f51-218">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="10f51-219">修复了从 PowerShell 命令行设置 DebugPreference 时的调试问题</span><span class="sxs-lookup"><span data-stu-id="10f51-219">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="10f51-220">更新了 Set-AzureRmDataLakeStoreItemAcl 的示例</span><span class="sxs-lookup"><span data-stu-id="10f51-220">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="10f51-221">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="10f51-221">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="10f51-222">更新了 Set-AzureRmDataLakeStoreItemAclEntry 的示例</span><span class="sxs-lookup"><span data-stu-id="10f51-222">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="10f51-223">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="10f51-223">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="10f51-224">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="10f51-224">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="10f51-225">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="10f51-225">AzureRM.Dns</span></span>
* <span data-ttu-id="10f51-226">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="10f51-226">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="10f51-227">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="10f51-227">AzureRM.EventGrid</span></span>
* <span data-ttu-id="10f51-228">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="10f51-228">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="10f51-229">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="10f51-229">AzureRM.EventHub</span></span>
* <span data-ttu-id="10f51-230">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="10f51-230">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="10f51-231">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="10f51-231">AzureRM.HDInsight</span></span>
* <span data-ttu-id="10f51-232">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="10f51-232">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="10f51-233">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="10f51-233">AzureRM.Insights</span></span>
* <span data-ttu-id="10f51-234">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="10f51-234">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="10f51-235">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="10f51-235">AzureRM.IotHub</span></span>
* <span data-ttu-id="10f51-236">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="10f51-236">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="10f51-237">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="10f51-237">AzureRM.KeyVault</span></span>
* <span data-ttu-id="10f51-238">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="10f51-238">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="10f51-239">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="10f51-239">AzureRM.LogicApp</span></span>
* <span data-ttu-id="10f51-240">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="10f51-240">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="10f51-241">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="10f51-241">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="10f51-242">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="10f51-242">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="10f51-243">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="10f51-243">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="10f51-244">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="10f51-244">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="10f51-245">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="10f51-245">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="10f51-246">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="10f51-246">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="10f51-247">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="10f51-247">AzureRM.Media</span></span>
* <span data-ttu-id="10f51-248">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="10f51-248">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="10f51-249">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="10f51-249">AzureRM.Network</span></span>
* <span data-ttu-id="10f51-250">增加了 Set-AzureRmLocalNetworkGateway 的示例</span><span class="sxs-lookup"><span data-stu-id="10f51-250">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="10f51-251">增加了 Add-AzureRmVirtualNetworkGatewayIpConfig、Get-AzureRmVirtualNetworkGatewayConnectionSharedKey 和 New-AzureRmVirtualNetworkGatewayConnection 的示例和说明</span><span class="sxs-lookup"><span data-stu-id="10f51-251">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="10f51-252">增加了 Remove-AzureRmVirtualNetworkGatewayIpConfig 和 Reset-AzureRmVirtualNetworkGateway 的示例</span><span class="sxs-lookup"><span data-stu-id="10f51-252">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="10f51-253">增加了 Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey 的示例</span><span class="sxs-lookup"><span data-stu-id="10f51-253">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="10f51-254">增加了 Set-AzureRmVirtualNetworkGatewayConnectionSharedKey 的示例</span><span class="sxs-lookup"><span data-stu-id="10f51-254">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="10f51-255">增加了 Set-AzureRmVirtualNetworkGatewayConnection 的示例</span><span class="sxs-lookup"><span data-stu-id="10f51-255">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="10f51-256">使用最新的代码生成器重新生成了 ApplicationSecurityGroup、RouteTable 和 Usage 的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="10f51-256">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="10f51-257">阐明了在尝试获取的子网不存在时 Get-AzureRmVirtualNetworkSubnetConfig 的错误消息</span><span class="sxs-lookup"><span data-stu-id="10f51-257">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="10f51-258">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="10f51-258">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="10f51-259">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="10f51-259">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="10f51-260">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="10f51-260">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="10f51-261">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="10f51-261">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="10f51-262">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="10f51-262">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="10f51-263">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="10f51-263">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="10f51-264">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="10f51-264">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="10f51-265">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="10f51-265">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="10f51-266">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="10f51-266">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="10f51-267">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="10f51-267">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="10f51-268">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="10f51-268">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="10f51-269">为 Get-AzureRmRecoveryServicesBackItem cmdlet 增加了策略筛选器。</span><span class="sxs-lookup"><span data-stu-id="10f51-269">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="10f51-270">此命令返回受给定策略 ID 保护的备份项的列表。</span><span class="sxs-lookup"><span data-stu-id="10f51-270">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="10f51-271">已将 Microsoft.Azure.Management.RecoveryServices.Backup 更新到 3.0.0-preview 版本。</span><span class="sxs-lookup"><span data-stu-id="10f51-271">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="10f51-272">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="10f51-272">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="10f51-273">为 Restore-AzureRmRecoveryServicesBackupItem 增加了 TargetResourceGroupName 参数。</span><span class="sxs-lookup"><span data-stu-id="10f51-273">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="10f51-274">托管磁盘还原到的资源组。</span><span class="sxs-lookup"><span data-stu-id="10f51-274">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="10f51-275">适用于包含托管磁盘的 VM 的备份。</span><span class="sxs-lookup"><span data-stu-id="10f51-275">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="10f51-276">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="10f51-276">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="10f51-277">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="10f51-277">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="10f51-278">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="10f51-278">AzureRM.RedisCache</span></span>
* <span data-ttu-id="10f51-279">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="10f51-279">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="10f51-280">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="10f51-280">AzureRM.Relay</span></span>
* <span data-ttu-id="10f51-281">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="10f51-281">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="10f51-282">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="10f51-282">AzureRM.Resources</span></span>
* <span data-ttu-id="10f51-283">支持在订阅范围部署模板。</span><span class="sxs-lookup"><span data-stu-id="10f51-283">Support template deployment at subscription scope.</span></span> <span data-ttu-id="10f51-284">增加了新 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="10f51-284">Add new Cmdlets:</span></span>
    - <span data-ttu-id="10f51-285">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="10f51-285">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="10f51-286">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="10f51-286">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="10f51-287">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="10f51-287">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="10f51-288">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="10f51-288">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="10f51-289">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="10f51-289">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="10f51-290">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="10f51-290">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="10f51-291">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="10f51-291">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="10f51-292">修复了在将上下文传递给 Set-AzureRmResource 时引发错误的问题</span><span class="sxs-lookup"><span data-stu-id="10f51-292">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="10f51-293">修复了 New-AzureRmResourceGroupDeployment 中的示例</span><span class="sxs-lookup"><span data-stu-id="10f51-293">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="10f51-294">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="10f51-294">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="10f51-295">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="10f51-295">AzureRM.Scheduler</span></span>
* <span data-ttu-id="10f51-296">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="10f51-296">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="10f51-297">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="10f51-297">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="10f51-298">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="10f51-298">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="10f51-299">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="10f51-299">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="10f51-300">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="10f51-300">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="10f51-301">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="10f51-301">AzureRM.Sql</span></span>
* <span data-ttu-id="10f51-302">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="10f51-302">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="10f51-303">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="10f51-303">AzureRM.Storage</span></span>
* <span data-ttu-id="10f51-304">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="10f51-304">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="10f51-305">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="10f51-305">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="10f51-306">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="10f51-306">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="10f51-307">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="10f51-307">AzureRM.Tags</span></span>
* <span data-ttu-id="10f51-308">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="10f51-308">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="10f51-309">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="10f51-309">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="10f51-310">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="10f51-310">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="10f51-311">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="10f51-311">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="10f51-312">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="10f51-312">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="10f51-313">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="10f51-313">AzureRM.Websites</span></span>
* <span data-ttu-id="10f51-314">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="10f51-314">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="10f51-315">6.6.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="10f51-315">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="10f51-316">常规</span><span class="sxs-lookup"><span data-stu-id="10f51-316">General</span></span>
* <span data-ttu-id="10f51-317">更新了所有帮助文件，以包括完整参数类型和正确的输入/输出类型。</span><span class="sxs-lookup"><span data-stu-id="10f51-317">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="10f51-318">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="10f51-318">AzureRM.Profile</span></span>
* <span data-ttu-id="10f51-319">更新了 Common.Strategy 库，以便能够验证资源的当前配置是否与目标资源兼容。</span><span class="sxs-lookup"><span data-stu-id="10f51-319">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="10f51-320">在 Common.Storage 中添加了 ps1xml 类型</span><span class="sxs-lookup"><span data-stu-id="10f51-320">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="10f51-321">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="10f51-321">Azure.Storage</span></span>
* <span data-ttu-id="10f51-322">增加了从 DefaultProfile 获取存储上下文的支持</span><span class="sxs-lookup"><span data-stu-id="10f51-322">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="10f51-323">为 cmdlet 输出类型属性增加了 Ps1XmlAttribute。</span><span class="sxs-lookup"><span data-stu-id="10f51-323">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="10f51-324">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="10f51-324">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="10f51-325">修复了问题 https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="10f51-325">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="10f51-326">修复了 Automapper 中将 PsApiManagementApi 转换为 ApiContract 的 bug</span><span class="sxs-lookup"><span data-stu-id="10f51-326">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="10f51-327">修复了问题 https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="10f51-327">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="10f51-328">修复了 File.Save 中没有使用编码类型重载的 bug</span><span class="sxs-lookup"><span data-stu-id="10f51-328">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="10f51-329">修复了问题 https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="10f51-329">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="10f51-330">升级到了 4.0.3 Nuget版本，该版本修复了 apiId 上的模式异常</span><span class="sxs-lookup"><span data-stu-id="10f51-330">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="10f51-331">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="10f51-331">AzureRM.Compute</span></span>
* <span data-ttu-id="10f51-332">修复因使用 PremiumLRS 存储帐户类型重命名而在 New-AzureRmVm 中使用 DiskFileParameterSet 创建 VM 失败的问题。</span><span class="sxs-lookup"><span data-stu-id="10f51-332">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="10f51-333">修复 Invoke-AzureRmVMRunCommand cmdlet</span><span class="sxs-lookup"><span data-stu-id="10f51-333">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="10f51-334">更新 Get-AzureRmAvailabilitySet 以启用列出订阅中的所有可用性集。</span><span class="sxs-lookup"><span data-stu-id="10f51-334">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="10f51-335">（ResouceGroupName 参数现在是可选的。）</span><span class="sxs-lookup"><span data-stu-id="10f51-335">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="10f51-336">更新“New-AzureRmVm”的 SimpleParameterSet 以在符合条件的 VM 上启用加速网络。</span><span class="sxs-lookup"><span data-stu-id="10f51-336">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="10f51-337">将 New-AzureRmVmss 简单参数集更新为在用户指定的 LB 已存在时创建 vmss 失败。</span><span class="sxs-lookup"><span data-stu-id="10f51-337">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="10f51-338">更新 New-AzureRmDisk 的示例</span><span class="sxs-lookup"><span data-stu-id="10f51-338">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="10f51-339">添加“New-AzureRmVM”的示例</span><span class="sxs-lookup"><span data-stu-id="10f51-339">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="10f51-340">更新 Set-AzureRmVMOSDisk 的说明</span><span class="sxs-lookup"><span data-stu-id="10f51-340">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="10f51-341">更新 Set-AzureRmVMBginfoExtension 的示例 1 以更正拼写和前缀。</span><span class="sxs-lookup"><span data-stu-id="10f51-341">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="10f51-342">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="10f51-342">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="10f51-343">将 ADF .Net SDK 版本更新为 1.1.0。</span><span class="sxs-lookup"><span data-stu-id="10f51-343">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="10f51-344">支持跨数据工厂的自承载集成运行时共享。</span><span class="sxs-lookup"><span data-stu-id="10f51-344">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="10f51-345">将新参数 -SharedIntegrationRuntimeResourceId 添加到 Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet。</span><span class="sxs-lookup"><span data-stu-id="10f51-345">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="10f51-346">将新的可选参数 -LinkedDataFactoryName 添加到 Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet。</span><span class="sxs-lookup"><span data-stu-id="10f51-346">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="10f51-347">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="10f51-347">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="10f51-348">将数据平面 SDK (Microsoft.Azure.DataLake.Store) 版本更新为 1.1.9</span><span class="sxs-lookup"><span data-stu-id="10f51-348">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="10f51-349">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="10f51-349">AzureRM.EventHub</span></span>
* <span data-ttu-id="10f51-350">在删除 cmdlet 中更新了 InputObject 和 ResourceId 的管道</span><span class="sxs-lookup"><span data-stu-id="10f51-350">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="10f51-351">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="10f51-351">AzureRM.Insights</span></span>
* <span data-ttu-id="10f51-352">修复了帮助文件中 OutputType 的格式问题</span><span class="sxs-lookup"><span data-stu-id="10f51-352">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="10f51-353">使用 Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span><span class="sxs-lookup"><span data-stu-id="10f51-353">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="10f51-354">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="10f51-354">AzureRM.KeyVault</span></span>
* <span data-ttu-id="10f51-355">修复了 Set-AzureRmKeyVaultAccessPolicy 中的管道问题</span><span class="sxs-lookup"><span data-stu-id="10f51-355">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="10f51-356">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="10f51-356">AzureRM.Network</span></span>
* <span data-ttu-id="10f51-357">添加了 LoadBalancerInboundNatPoolConfig cmdlet 的示例。</span><span class="sxs-lookup"><span data-stu-id="10f51-357">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="10f51-358">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="10f51-358">AzureRM.Resources</span></span>
* <span data-ttu-id="10f51-359">修复了为“Get-AzureRmResource”同时提供标记名称和值时出现的问题</span><span class="sxs-lookup"><span data-stu-id="10f51-359">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="10f51-360">使用“Set-AzureRmResource”修复管道方案</span><span class="sxs-lookup"><span data-stu-id="10f51-360">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="10f51-361">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="10f51-361">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="10f51-362">在删除 cmdlet 中更新了 InputObject 和 ResourceId 的管道</span><span class="sxs-lookup"><span data-stu-id="10f51-362">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="10f51-363">修复了几个问题</span><span class="sxs-lookup"><span data-stu-id="10f51-363">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="10f51-364">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="10f51-364">AzureRM.Sql</span></span>
* <span data-ttu-id="10f51-365">使用以下 cmdlet 添加服务器高级威胁防护支持：</span><span class="sxs-lookup"><span data-stu-id="10f51-365">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="10f51-366">Enable-AzureRmSqlServerAdvancedThreatProtection；Disable-AzureRmSqlServerAdvancedThreatProtection；Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="10f51-366">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="10f51-367">使用以下 cmdlet 添加漏洞评估支持：</span><span class="sxs-lookup"><span data-stu-id="10f51-367">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="10f51-368">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings；Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings；Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="10f51-368">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="10f51-369">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline；Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline；Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="10f51-369">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="10f51-370">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan；Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord；Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="10f51-370">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="10f51-371">修复了 Remove-AzureRmSqlServerFirewallRule 中的示例</span><span class="sxs-lookup"><span data-stu-id="10f51-371">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="10f51-372">修复了 Get-AzureSqlSyncGroupLog 中非美国基础文化的日期时间处理错误</span><span class="sxs-lookup"><span data-stu-id="10f51-372">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="10f51-373">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="10f51-373">AzureRM.Storage</span></span>
* <span data-ttu-id="10f51-374">将 Ps1XmlAttribute 添加到 cmdlet 输出类型属性</span><span class="sxs-lookup"><span data-stu-id="10f51-374">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="10f51-375">在表视图中显示 StorageAccount cmdlet 输出</span><span class="sxs-lookup"><span data-stu-id="10f51-375">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="10f51-376">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="10f51-376">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="10f51-377">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="10f51-377">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="10f51-378">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="10f51-378">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="10f51-379">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="10f51-379">AzureRM.Tags</span></span>
* <span data-ttu-id="10f51-380">从 Tag cmdlet 帮助中删除不正确的语句</span><span class="sxs-lookup"><span data-stu-id="10f51-380">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="10f51-381">6.5.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="10f51-381">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="10f51-382">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="10f51-382">AzureRM.Profile</span></span>
* <span data-ttu-id="10f51-383">更新了“Get-AzureRmContextAutosaveSetting”的帮助</span><span class="sxs-lookup"><span data-stu-id="10f51-383">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="10f51-384">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="10f51-384">Azure.Storage</span></span>
* <span data-ttu-id="10f51-385">支持使用只写 Sas 令牌上传 Blob 或文件</span><span class="sxs-lookup"><span data-stu-id="10f51-385">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="10f51-386">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="10f51-386">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="10f51-387">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="10f51-387">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="10f51-388">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="10f51-388">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="10f51-389">将所需属性 ResourceGroupName 添加到 AS。</span><span class="sxs-lookup"><span data-stu-id="10f51-389">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="10f51-390">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="10f51-390">AzureRM.Automation</span></span>
* <span data-ttu-id="10f51-391">更新帮助并添加“New-AzureRMAutomationSchedule”的示例</span><span class="sxs-lookup"><span data-stu-id="10f51-391">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="10f51-392">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="10f51-392">AzureRM.Compute</span></span>
* <span data-ttu-id="10f51-393">将 -Tag 参数添加到 Update/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="10f51-393">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="10f51-394">添加“Add-AzureRmVmssExtension”的示例</span><span class="sxs-lookup"><span data-stu-id="10f51-394">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="10f51-395">添加“Remove-AzureRmVmssExtension”的示例</span><span class="sxs-lookup"><span data-stu-id="10f51-395">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="10f51-396">更新“Set-AzureRmVMAccessExtension”的帮助</span><span class="sxs-lookup"><span data-stu-id="10f51-396">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="10f51-397">更新 New-AzureRmVmss 的 SimpleParameterSet，以默认情况下将 SinglePlacementGroup 设置为false，并添加开关参数“SinglePlacementGroup”，使用户能够在单个放置组中创建 VMSS。</span><span class="sxs-lookup"><span data-stu-id="10f51-397">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="10f51-398">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="10f51-398">AzureRM.EventHub</span></span>
* <span data-ttu-id="10f51-399">向 PSEventHubDRConfigurationAttributes 类添加了一个只读属性“PendingReplicationOperationsCount”，该属性在复制过程中为挂起的复制操作计数</span><span class="sxs-lookup"><span data-stu-id="10f51-399">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="10f51-400">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="10f51-400">AzureRM.KeyVault</span></span>
* <span data-ttu-id="10f51-401">更新了 Set-AzureRmKeyVaultAccessPolicy 的错误消息</span><span class="sxs-lookup"><span data-stu-id="10f51-401">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="10f51-402">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="10f51-402">AzureRM.LogicApp</span></span>
* <span data-ttu-id="10f51-403">修复了 New-AzureRmLogicApp 中的“无法解析参数集”错误</span><span class="sxs-lookup"><span data-stu-id="10f51-403">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="10f51-404">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="10f51-404">AzureRM.Network</span></span>
* <span data-ttu-id="10f51-405">在多个租户中为 Set/Add-AzureRmVirtualNetworkPeering 启用跨虚拟网络对等互连</span><span class="sxs-lookup"><span data-stu-id="10f51-405">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="10f51-406">针对应用程序网关更新了以下 cmdlet</span><span class="sxs-lookup"><span data-stu-id="10f51-406">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="10f51-407">New-AzureRmApplicationGateway：添加了 EnableFIPS 标志和区域支持</span><span class="sxs-lookup"><span data-stu-id="10f51-407">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="10f51-408">New-AzureRmApplicationGatewaySku：添加了新的 sku Standard_v2 和 WAF_v2</span><span class="sxs-lookup"><span data-stu-id="10f51-408">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="10f51-409">Set-AzureRmApplicationGatewaySku：添加了新的 sku Standard_v2 和 WAF_v2</span><span class="sxs-lookup"><span data-stu-id="10f51-409">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="10f51-410">使用最新的生成器版本重新生成了 RouteTable cmdlet</span><span class="sxs-lookup"><span data-stu-id="10f51-410">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="10f51-411">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="10f51-411">AzureRM.Relay</span></span>
* <span data-ttu-id="10f51-412">更新了 Markdown 文件，其中修复了示例中的参数名称问题</span><span class="sxs-lookup"><span data-stu-id="10f51-412">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="10f51-413">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="10f51-413">AzureRM.Resources</span></span>
* <span data-ttu-id="10f51-414">更新了 Roleassignment 和 roledefinition cmdlet：</span><span class="sxs-lookup"><span data-stu-id="10f51-414">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="10f51-415">删除了作为分页的一部分完成的额外 roledefinition 调用。</span><span class="sxs-lookup"><span data-stu-id="10f51-415">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="10f51-416">修复了 Get-AzureRmRoleAssignment cmdlet</span><span class="sxs-lookup"><span data-stu-id="10f51-416">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="10f51-417">修复了 -ExpandPrincipalGroups 命令参数功能</span><span class="sxs-lookup"><span data-stu-id="10f51-417">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="10f51-418">修复了“Get-AzureRmResource”的问题，其中“-ResourceType”参数区分大小写</span><span class="sxs-lookup"><span data-stu-id="10f51-418">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="10f51-419">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="10f51-419">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="10f51-420">向列表 cmdlet 添加了 top 和 skip 参数</span><span class="sxs-lookup"><span data-stu-id="10f51-420">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="10f51-421">添加了标准到高级命名空间迁移 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="10f51-421">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="10f51-422">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="10f51-422">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="10f51-423">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="10f51-423">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="10f51-424">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="10f51-424">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="10f51-425">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="10f51-425">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="10f51-426">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="10f51-426">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="10f51-427">向 PSServiceBusDRConfigurationAttributes 类添加了一个只读属性“PendingReplicationOperationsCount”，该属性在复制过程中为挂起的复制操作计数</span><span class="sxs-lookup"><span data-stu-id="10f51-427">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="10f51-428">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="10f51-428">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="10f51-429">更新了“New-AzureRmServiceFabricCluster”的示例</span><span class="sxs-lookup"><span data-stu-id="10f51-429">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="10f51-430">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="10f51-430">AzureRM.Sql</span></span>
* <span data-ttu-id="10f51-431">为 Management.Sql 添加新的 Cmdlet，以允许客户将 TDE 证书添加到 Sql Server 实例或托管实例</span><span class="sxs-lookup"><span data-stu-id="10f51-431">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="10f51-432">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="10f51-432">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="10f51-433">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="10f51-433">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="10f51-434">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="10f51-434">AzureRM.Websites</span></span>
* <span data-ttu-id="10f51-435">设置为 false 时，`Set-AzureRmWebApp -AssignIdentity` 和 `Set-AzureRmWebAppSlot -AssignIdentity` 现在将从站点对象中删除 Identity 属性。同时移除预览标记。</span><span class="sxs-lookup"><span data-stu-id="10f51-435">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="10f51-436">`Get-AzureRmWebAppMetrics`、`Get-AzureRmAppServicePlanMetrics` 示例已更新</span><span class="sxs-lookup"><span data-stu-id="10f51-436">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="10f51-437">`Set-AzureRmWebApp -PhpVersion` 支持 off 作为有效的 php 版本</span><span class="sxs-lookup"><span data-stu-id="10f51-437">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="10f51-438">6.4.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="10f51-438">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="10f51-439">常规</span><span class="sxs-lookup"><span data-stu-id="10f51-439">General</span></span>
* <span data-ttu-id="10f51-440">修复了大多数模块的帮助文件中的 OutputType 格式问题</span><span class="sxs-lookup"><span data-stu-id="10f51-440">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="10f51-441">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="10f51-441">AzureRM.Profile</span></span>
* <span data-ttu-id="10f51-442">已将 Ps1Xml 属性添加到基本输出类型</span><span class="sxs-lookup"><span data-stu-id="10f51-442">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="10f51-443">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="10f51-443">AzureRM.Compute</span></span>
* <span data-ttu-id="10f51-444">VMSS 的 IP 标记功能</span><span class="sxs-lookup"><span data-stu-id="10f51-444">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="10f51-445">已添加“New-AzureRmVmssIpTagConfig”cmdlet</span><span class="sxs-lookup"><span data-stu-id="10f51-445">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="10f51-446">已将 IpTag 参数添加到 New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="10f51-446">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="10f51-447">VMSS 的自动 OS 回滚功能</span><span class="sxs-lookup"><span data-stu-id="10f51-447">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="10f51-448">已将 DisableAutoRollback 参数添加到 New-AzureRmVmssConfig 和 Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="10f51-448">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="10f51-449">VMSS 的 OS 升级历史记录功能</span><span class="sxs-lookup"><span data-stu-id="10f51-449">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="10f51-450">已将 OSUpgradeHistory 开关参数添加到 Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="10f51-450">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="10f51-451">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="10f51-451">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="10f51-452">通过以下命令添加目录 ACL 的支持：</span><span class="sxs-lookup"><span data-stu-id="10f51-452">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="10f51-453">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="10f51-453">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="10f51-454">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="10f51-454">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="10f51-455">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="10f51-455">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="10f51-456">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="10f51-456">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="10f51-457">为 Set-AzureRmDataLakeStoreItemAclEntry、Remove-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAcl 添加了取消支持和进度跟踪</span><span class="sxs-lookup"><span data-stu-id="10f51-457">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="10f51-458">为 Export-AzureRmDataLakeStoreChildItemProperties 添加了取消支持</span><span class="sxs-lookup"><span data-stu-id="10f51-458">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="10f51-459">修复了执行递归操作的 cmdlet 的调试消息刷新</span><span class="sxs-lookup"><span data-stu-id="10f51-459">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="10f51-460">修复了 DataLake cmdlet 的测试位置</span><span class="sxs-lookup"><span data-stu-id="10f51-460">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="10f51-461">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="10f51-461">AzureRM.EventHub</span></span>
* <span data-ttu-id="10f51-462">已将可选的 MaxCount 参数添加到“列出操作”cmdlet Get-AzureRmEventHub 和 Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="10f51-462">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="10f51-463">修复了 New-AzureRmEventHub cmdlet 的问题：创建新事件中心时至少需要一个参数。</span><span class="sxs-lookup"><span data-stu-id="10f51-463">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="10f51-464">提供了默认参数集。</span><span class="sxs-lookup"><span data-stu-id="10f51-464">Provided Default Parameter set.</span></span>
* <span data-ttu-id="10f51-465">已将可选参数 -KeyValue 添加到 New-AzureRmEventHubKey cmdlet，该参数可让用户提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="10f51-465">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="10f51-466">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="10f51-466">AzureRM.KeyVault</span></span>
* <span data-ttu-id="10f51-467">修复了 Get-AzureRmKeyVault -Tag 返回所有资源的问题</span><span class="sxs-lookup"><span data-stu-id="10f51-467">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="10f51-468">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="10f51-468">AzureRM.Network</span></span>
* <span data-ttu-id="10f51-469">为区域冗余的 VirtualNetworkGateways 公开新 SKU</span><span class="sxs-lookup"><span data-stu-id="10f51-469">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="10f51-470">通过 ARM 为以下功能添加了新命令：ExpressRoute 合作伙伴 API</span><span class="sxs-lookup"><span data-stu-id="10f51-470">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="10f51-471">添加了 Get-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="10f51-471">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="10f51-472">添加了 Set-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="10f51-472">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="10f51-473">添加了 Add-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="10f51-473">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="10f51-474">添加了 Get-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="10f51-474">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="10f51-475">添加了 Remove-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="10f51-475">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="10f51-476">添加了 Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="10f51-476">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="10f51-477">添加了 Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="10f51-477">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="10f51-478">添加了 Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="10f51-478">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="10f51-479">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="10f51-479">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="10f51-480">添加了 Get-AzureRmRecoveryServicesBackupStatus cmdlet。</span><span class="sxs-lookup"><span data-stu-id="10f51-480">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="10f51-481">此 cmdlet 采用 VM ID，并检查 VM 是否受订阅中的某个保管库保护。</span><span class="sxs-lookup"><span data-stu-id="10f51-481">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="10f51-482">如果存在此类保管库，该 cmdlet 会输出该保管库的详细信息。</span><span class="sxs-lookup"><span data-stu-id="10f51-482">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="10f51-483">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="10f51-483">AzureRM.Resources</span></span>
* <span data-ttu-id="10f51-484">更新了 Get-AzureRmPolicyAssignment cmdlet：</span><span class="sxs-lookup"><span data-stu-id="10f51-484">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="10f51-485">添加了在管理组级别列出 -Scope 值的支持</span><span class="sxs-lookup"><span data-stu-id="10f51-485">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="10f51-486">添加了在管理组级别使用 -Scope 值检索单个分配的支持</span><span class="sxs-lookup"><span data-stu-id="10f51-486">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="10f51-487">已将 -Effective 和 -All 开关添加到 control 参数</span><span class="sxs-lookup"><span data-stu-id="10f51-487">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="10f51-488">更新了 Get/New/Remove/Set-AzureRmPolicyDefinition cmdlet</span><span class="sxs-lookup"><span data-stu-id="10f51-488">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="10f51-489">添加了 -ManagementGroupName 参数，以将操作应用到给定的管理组</span><span class="sxs-lookup"><span data-stu-id="10f51-489">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="10f51-490">添加了 -SubscriptionId 参数，以将操作应用到给定的订阅</span><span class="sxs-lookup"><span data-stu-id="10f51-490">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="10f51-491">更新了 Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlet</span><span class="sxs-lookup"><span data-stu-id="10f51-491">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="10f51-492">添加了 -ManagementGroupName 参数，以将操作应用到给定的管理组</span><span class="sxs-lookup"><span data-stu-id="10f51-492">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="10f51-493">添加了 -SubscriptionId 参数，以将操作应用到给定的订阅</span><span class="sxs-lookup"><span data-stu-id="10f51-493">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="10f51-494">添加了使用 TemplateParameterObject 时在参数中指定 KeyVault 机密引用的支持</span><span class="sxs-lookup"><span data-stu-id="10f51-494">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="10f51-495">修复了忽略“New-AzureRmADAppCredential”的“-EndDate”参数的问题</span><span class="sxs-lookup"><span data-stu-id="10f51-495">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="10f51-496">修复了“Add-AzureRmADGroupMember”使用错误的 URL 发出请求的问题</span><span class="sxs-lookup"><span data-stu-id="10f51-496">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="10f51-497">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="10f51-497">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="10f51-498">已将可选参数 -KeyValue 添加到 New-AzureRmServiceBusKey cmdlet，该参数可让用户提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="10f51-498">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="10f51-499">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="10f51-499">AzureRM.Sql</span></span>
* <span data-ttu-id="10f51-500">在 AzureRmSqlDatabaseRestorePoint 帮助中澄清了 SQLDW 的用户定义还原点</span><span class="sxs-lookup"><span data-stu-id="10f51-500">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="10f51-501">更新了多个 cmdlet 中 -ComputeGeneration 参数的文档</span><span class="sxs-lookup"><span data-stu-id="10f51-501">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="10f51-502">6.3.0 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="10f51-502">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="10f51-503">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="10f51-503">AzureRM.Profile</span></span>
* <span data-ttu-id="10f51-504">更新了 Enable-AzureRmContextAutoSave 的错误消息</span><span class="sxs-lookup"><span data-stu-id="10f51-504">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="10f51-505">在运行没有旧上下文的“Connect-AzureRmAccount”时为每个订阅创建一个上下文</span><span class="sxs-lookup"><span data-stu-id="10f51-505">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="10f51-506">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="10f51-506">Azure.Storage</span></span>
* <span data-ttu-id="10f51-507">在帮助文件中增加了关于 -Permissions 参数的其他信息。</span><span class="sxs-lookup"><span data-stu-id="10f51-507">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="10f51-508">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="10f51-508">AzureRM.Compute</span></span>
* <span data-ttu-id="10f51-509">“Get-AzureRmVmDiskEncryptionStatus”修复了一个针对没有数据磁盘的 VM 观察到的问题</span><span class="sxs-lookup"><span data-stu-id="10f51-509">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="10f51-510">更新计算客户端库版本以修复以下 cmdlet</span><span class="sxs-lookup"><span data-stu-id="10f51-510">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="10f51-511">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="10f51-511">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="10f51-512">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="10f51-512">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="10f51-513">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="10f51-513">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="10f51-514">修复了以下 cmdlet，因此可以正确地显示“操作 ID”和“操作状态”：</span><span class="sxs-lookup"><span data-stu-id="10f51-514">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="10f51-515">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="10f51-515">Start-AzureRmVM</span></span>
    - <span data-ttu-id="10f51-516">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="10f51-516">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="10f51-517">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="10f51-517">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="10f51-518">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="10f51-518">Set-AzureRmVM</span></span>
    - <span data-ttu-id="10f51-519">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="10f51-519">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="10f51-520">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="10f51-520">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="10f51-521">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="10f51-521">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="10f51-522">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="10f51-522">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="10f51-523">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="10f51-523">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="10f51-524">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="10f51-524">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="10f51-525">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="10f51-525">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="10f51-526">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="10f51-526">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="10f51-527">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="10f51-527">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="10f51-528">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="10f51-528">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="10f51-529">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="10f51-529">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="10f51-530">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="10f51-530">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="10f51-531">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="10f51-531">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="10f51-532">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="10f51-532">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="10f51-533">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="10f51-533">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="10f51-534">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="10f51-534">AzureRM.EventGrid</span></span>
* <span data-ttu-id="10f51-535">在 Update-AzureRmEventGridSubscription cmdlet 中删除 SubjectBeginsWith/SubjectEndsWith 的 ValidateNotNullOrEmpty 验证条件，允许根据需要将这些参数更改为空字符串。</span><span class="sxs-lookup"><span data-stu-id="10f51-535">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="10f51-536">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="10f51-536">AzureRM.KeyVault</span></span>
* <span data-ttu-id="10f51-537">修复运行 Get-AzureRmKeyVault -Tag 时不返回任何标记的问题</span><span class="sxs-lookup"><span data-stu-id="10f51-537">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="10f51-538">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="10f51-538">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="10f51-539">策略见解 cmdlet 的公开发行版</span><span class="sxs-lookup"><span data-stu-id="10f51-539">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="10f51-540">使用 API 版本 2018-04-04</span><span class="sxs-lookup"><span data-stu-id="10f51-540">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="10f51-541">向 Get-AzureRmPolicyStateSummary 的结果添加了 PolicyDefinitionReferenceId</span><span class="sxs-lookup"><span data-stu-id="10f51-541">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="10f51-542">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="10f51-542">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="10f51-543">向 RecoveryServices.Backup cmdlet 添加了 -Vault 参数。</span><span class="sxs-lookup"><span data-stu-id="10f51-543">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="10f51-544">传递时，此项会替代 Set-AzureRmRecoveryServicesContext cmdlet。</span><span class="sxs-lookup"><span data-stu-id="10f51-544">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="10f51-545">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="10f51-545">AzureRM.Sql</span></span>
* <span data-ttu-id="10f51-546">更新了 Get-AzureRmSqlDatabaseExpanded 的帮助文件中的示例</span><span class="sxs-lookup"><span data-stu-id="10f51-546">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="10f51-547">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="10f51-547">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="10f51-548">更新了 Add-AzureRmTrafficManagerEndpointConfig 的帮助文件</span><span class="sxs-lookup"><span data-stu-id="10f51-548">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="10f51-549">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="10f51-549">AzureRM.Websites</span></span>
* <span data-ttu-id="10f51-550">更新了“Set-AzureRmWebApp”，在使用 -AssignIdentity 时不覆盖 AppSettings</span><span class="sxs-lookup"><span data-stu-id="10f51-550">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="10f51-551">更新了“New-AzureRmWebAppSlot”，允许使用 AppServicePlan 作为可选参数</span><span class="sxs-lookup"><span data-stu-id="10f51-551">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="10f51-552">6.2.1 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="10f51-552">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="10f51-553">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="10f51-553">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="10f51-554">更新了 PSWorkspace 模型，允许 Network 使用 type 作为参数</span><span class="sxs-lookup"><span data-stu-id="10f51-554">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="10f51-555">6.2.0 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="10f51-555">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="10f51-556">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="10f51-556">AzureRM.Profile</span></span>
* <span data-ttu-id="10f51-557">修复了 Newtonsoft.Json 的版本 10.0.3 在模块导入时无法加载的问题</span><span class="sxs-lookup"><span data-stu-id="10f51-557">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="10f51-558">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="10f51-558">AzureRM.Compute</span></span>
* <span data-ttu-id="10f51-559">VMSS VM 更新功能</span><span class="sxs-lookup"><span data-stu-id="10f51-559">VMSS VM Update feature</span></span>
    - <span data-ttu-id="10f51-560">增加了“Update-AzureRmVmssVM”和“New-AzureRmVMDataDisk”cmdlet</span><span class="sxs-lookup"><span data-stu-id="10f51-560">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="10f51-561">为“Add-AzureRmVMDataDisk”cmdlet 增加了 VirtualMachineScaleSetVM 参数，支持向 Vmss VM 添加数据磁盘。</span><span class="sxs-lookup"><span data-stu-id="10f51-561">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="10f51-562">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="10f51-562">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="10f51-563">将 ADF.Net SDK 版本更新到了 0.8.0-preview，其中包含以下更改：</span><span class="sxs-lookup"><span data-stu-id="10f51-563">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="10f51-564">增加了“配置工厂存储库”操作</span><span class="sxs-lookup"><span data-stu-id="10f51-564">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="10f51-565">更新了 QuickBooks LinkedService，可以公开 consumerKey 和 consumerSecret 属性</span><span class="sxs-lookup"><span data-stu-id="10f51-565">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="10f51-566">已将多个模型类型从 SecretBase 更新为 Object</span><span class="sxs-lookup"><span data-stu-id="10f51-566">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="10f51-567">增加了 Blob 事件触发器</span><span class="sxs-lookup"><span data-stu-id="10f51-567">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="10f51-568">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="10f51-568">AzureRM.KeyVault</span></span>
* <span data-ttu-id="10f51-569">使用示例输出更新了文档</span><span class="sxs-lookup"><span data-stu-id="10f51-569">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="10f51-570">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="10f51-570">AzureRM.Network</span></span>
* <span data-ttu-id="10f51-571">在网络观察程序 cmdlet 上启用了流量分析参数</span><span class="sxs-lookup"><span data-stu-id="10f51-571">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="10f51-572">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="10f51-572">AzureRM.Resources</span></span>
* <span data-ttu-id="10f51-573">修复了从“Get-AzureRmResource”返回的“PSResource”对象的“Properties”属性问题</span><span class="sxs-lookup"><span data-stu-id="10f51-573">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="10f51-574">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="10f51-574">AzureRM.Scheduler</span></span>
* <span data-ttu-id="10f51-575">修复了更新 ServiceBusQueueJob 无法设置新 Auth 值的问题</span><span class="sxs-lookup"><span data-stu-id="10f51-575">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="10f51-576">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="10f51-576">AzureRM.Sql</span></span>
* <span data-ttu-id="10f51-577">使用可选的 LicenseType 参数更新了以下 cmdlet</span><span class="sxs-lookup"><span data-stu-id="10f51-577">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="10f51-578">New-AzureRmSqlDatabase；Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="10f51-578">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="10f51-579">New-AzureRmSqlElasticPool；Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="10f51-579">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="10f51-580">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="10f51-580">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="10f51-581">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="10f51-581">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="10f51-582">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="10f51-582">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="10f51-583">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="10f51-583">AzureRM.Websites</span></span>
* <span data-ttu-id="10f51-584">更新了“New-AzureRMWebApp”，可以使用策略库中的常用算法。</span><span class="sxs-lookup"><span data-stu-id="10f51-584">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="10f51-585">6.1.0 - 2018 年 5 月</span><span class="sxs-lookup"><span data-stu-id="10f51-585">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="10f51-586">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="10f51-586">AzureRM.Profile</span></span>
* <span data-ttu-id="10f51-587">修复了运行“Clear-AzureRmContext”时会保留空上下文的问题，该上下文使用旧的默认上下文的名称，导致用户无法使用旧名称创建新的上下文</span><span class="sxs-lookup"><span data-stu-id="10f51-587">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="10f51-588">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="10f51-588">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="10f51-589">允许在 AS 上执行网关的关联/取消关联操作。</span><span class="sxs-lookup"><span data-stu-id="10f51-589">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="10f51-590">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="10f51-590">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="10f51-591">增加了对 ApiVersions、ApiReleases 和 ApiRevisions 的支持</span><span class="sxs-lookup"><span data-stu-id="10f51-591">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="10f51-592">增加了对 ServiceFabric 后端的支持</span><span class="sxs-lookup"><span data-stu-id="10f51-592">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="10f51-593">增加了对 Application Insights Logger 的支持</span><span class="sxs-lookup"><span data-stu-id="10f51-593">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="10f51-594">增加的支持包括认可“基本”SKU 是 API 管理服务的有效 SKU</span><span class="sxs-lookup"><span data-stu-id="10f51-594">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="10f51-595">增加的支持包括允许将专用 CA 颁发的证书作为根证书或 CA 证书安装</span><span class="sxs-lookup"><span data-stu-id="10f51-595">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="10f51-596">增加的支持包括通过 KeyVault 和多个代理主机名接受自定义 SSL 证书</span><span class="sxs-lookup"><span data-stu-id="10f51-596">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="10f51-597">增加了对 MSI 标识的支持</span><span class="sxs-lookup"><span data-stu-id="10f51-597">Added support for MSI identity</span></span>
* <span data-ttu-id="10f51-598">增加的支持包括通过 URL 接受策略 注意：以下 cmdlet 将在未来版本中弃用</span><span class="sxs-lookup"><span data-stu-id="10f51-598">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="10f51-599">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="10f51-599">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="10f51-600">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="10f51-600">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="10f51-601">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="10f51-601">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="10f51-602">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="10f51-602">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="10f51-603">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="10f51-603">AzureRM.Batch</span></span>
* <span data-ttu-id="10f51-604">发布新 cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="10f51-604">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="10f51-605">发布新 cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="10f51-605">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="10f51-606">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="10f51-606">AzureRM.Consumption</span></span>
* <span data-ttu-id="10f51-607">在 Cmdlet Get-AzureRmConsumptionUsageDetail 中增加了新参数 Expand、ResourceGroup、InstanceName、InstanceId、Tags、Top</span><span class="sxs-lookup"><span data-stu-id="10f51-607">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="10f51-608">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="10f51-608">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="10f51-609">修复了 Export-AzureRmDataLakeStoreChildItemProperties 的示例</span><span class="sxs-lookup"><span data-stu-id="10f51-609">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="10f51-610">修复了 Set-AzureRmDataLakeStoreItemAclEntry 中 Recurse 用例的 null 参数异常</span><span class="sxs-lookup"><span data-stu-id="10f51-610">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="10f51-611">修复了 Set-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAcl、Remove-AzureRmDataLakeStoreItemAclEntry 的帮助文件</span><span class="sxs-lookup"><span data-stu-id="10f51-611">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="10f51-612">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="10f51-612">AzureRM.Network</span></span>
* <span data-ttu-id="10f51-613">将网络 SDK 版本从 18.0.0-preview 升至 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="10f51-613">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="10f51-614">增加了用于创建协议配置的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="10f51-614">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="10f51-615">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="10f51-615">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="10f51-616">增加了用于向现有的快速路由线路添加新的线路连接的 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="10f51-616">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="10f51-617">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="10f51-617">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="10f51-618">增加了用于从现有的快速路由线路删除线路连接的 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="10f51-618">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="10f51-619">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="10f51-619">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="10f51-620">增加了用于检索线路连接的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="10f51-620">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="10f51-621">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="10f51-621">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="10f51-622">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="10f51-622">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="10f51-623">修复了使用生成的证书进行服务器身份验证的问题（问题 5998）</span><span class="sxs-lookup"><span data-stu-id="10f51-623">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="10f51-624">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="10f51-624">AzureRM.Sql</span></span>
* <span data-ttu-id="10f51-625">更新了审核 cmdlet，允许删除 AuditActions 或 AuditActionGroups</span><span class="sxs-lookup"><span data-stu-id="10f51-625">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="10f51-626">修复了设置新的灵活保留策略时使用 Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy 出现的问题。该问题的具体表现是：在命令失败的同时，出现“不再支持使用 Azure 恢复服务保管库和策略配置长期保留策略。</span><span class="sxs-lookup"><span data-stu-id="10f51-626">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="10f51-627">请使用新的灵活保留策略提交请求”错误消息。</span><span class="sxs-lookup"><span data-stu-id="10f51-627">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="10f51-628">更新了与 Azure SQL 数据库/ElasticPool 的创建/更新相关的所有 cmdlet，允许使用新的数据库 API，而这些 cmdlet 支持的 SKU 属性则适用于规模和层相关属性。</span><span class="sxs-lookup"><span data-stu-id="10f51-628">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="10f51-629">更新的 cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="10f51-629">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="10f51-630">New-AzureRmSqlDatabase；Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="10f51-630">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="10f51-631">New-AzureRmSqlElasticPool；Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="10f51-631">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="10f51-632">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="10f51-632">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="10f51-633">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="10f51-633">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="10f51-634">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="10f51-634">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="10f51-635">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="10f51-635">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="10f51-636">更新了“Get-AzureRmTrafficManagerProfile”的参数，要求在使用 -Name 参数时使用 -ResourceGroupName 参数。</span><span class="sxs-lookup"><span data-stu-id="10f51-636">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
