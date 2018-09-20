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
ms.sourcegitcommit: bc88e64c494337821274d6a66c1edad656c119c5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/20/2018
ms.locfileid: "46300827"
---
# <a name="release-notes"></a><span data-ttu-id="06f6c-103">发行说明</span><span class="sxs-lookup"><span data-stu-id="06f6c-103">Release notes</span></span>

<span data-ttu-id="06f6c-104">下面是此版本中对 Azure PowerShell 所做的更改列表。</span><span class="sxs-lookup"><span data-stu-id="06f6c-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="681---august-2018"></a><span data-ttu-id="06f6c-105">6.8.1 - 2018 年 8 月</span><span class="sxs-lookup"><span data-stu-id="06f6c-105">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="06f6c-106">常规</span><span class="sxs-lookup"><span data-stu-id="06f6c-106">General</span></span>
* <span data-ttu-id="06f6c-107">解决了未设置默认资源组的问题。</span><span class="sxs-lookup"><span data-stu-id="06f6c-107">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="06f6c-108">更新了公共运行时程序集</span><span class="sxs-lookup"><span data-stu-id="06f6c-108">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="06f6c-109">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="06f6c-109">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="06f6c-110">解决了未设置默认资源组的问题。</span><span class="sxs-lookup"><span data-stu-id="06f6c-110">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="06f6c-111">修复了问题 https://github.com/Azure/azure-powershell/issues/6603</span><span class="sxs-lookup"><span data-stu-id="06f6c-111">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="06f6c-112">Import-AzureRmApiManagementApi 和 \*-AzureRmApiManagementCertificate cmdlet 现在处理相对路径</span><span class="sxs-lookup"><span data-stu-id="06f6c-112">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="06f6c-113">修复了问题 https://github.com/Azure/azure-powershell/issues/6879</span><span class="sxs-lookup"><span data-stu-id="06f6c-113">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="06f6c-114">CertificateInformation 是使 Set-AzureRmApiManagement cmdlet 可以正常工作的可设置属性。</span><span class="sxs-lookup"><span data-stu-id="06f6c-114">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="06f6c-115">通过升级到 4.0.4-preview nuget 进行了修复</span><span class="sxs-lookup"><span data-stu-id="06f6c-115">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="06f6c-116">修复了问题 https://github.com/Azure/azure-powershell/issues/6853</span><span class="sxs-lookup"><span data-stu-id="06f6c-116">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="06f6c-117">针对按产品名称进行的搜索修复了 Odata 筛选器</span><span class="sxs-lookup"><span data-stu-id="06f6c-117">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="06f6c-118">修复了问题 https://github.com/Azure/azure-powershell/issues/6814</span><span class="sxs-lookup"><span data-stu-id="06f6c-118">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="06f6c-119">针对按 API 名称进行的搜索修复了 Odata 筛选器</span><span class="sxs-lookup"><span data-stu-id="06f6c-119">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="06f6c-120">添加了对 AzureMonitor 记录器的支持</span><span class="sxs-lookup"><span data-stu-id="06f6c-120">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="06f6c-121">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="06f6c-121">AzureRM.Compute</span></span>
* <span data-ttu-id="06f6c-122">解决了错误输出中缺少目标的问题。</span><span class="sxs-lookup"><span data-stu-id="06f6c-122">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="06f6c-123">解决了带有托管磁盘的 VM 的存储帐户类型问题</span><span class="sxs-lookup"><span data-stu-id="06f6c-123">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="06f6c-124">解决了未设置默认资源组的问题。</span><span class="sxs-lookup"><span data-stu-id="06f6c-124">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="06f6c-125">解决了在其他环境（例如 Azure 中国）中使用 AEM 扩展 cmdlet 的问题</span><span class="sxs-lookup"><span data-stu-id="06f6c-125">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="06f6c-126">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="06f6c-126">AzureRM.Network</span></span>
* <span data-ttu-id="06f6c-127">将默认 cmdlet 输出表示形式更改为表视图</span><span class="sxs-lookup"><span data-stu-id="06f6c-127">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="06f6c-128">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="06f6c-128">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="06f6c-129">修复了在尝试扩展停用的容量时 Update-AzureRmPowerBIEmbeddedCapacity 中出现的故障</span><span class="sxs-lookup"><span data-stu-id="06f6c-129">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="06f6c-130">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="06f6c-130">AzureRM.Resources</span></span>
* <span data-ttu-id="06f6c-131">解决了从市场创建托管应用程序的问题。</span><span class="sxs-lookup"><span data-stu-id="06f6c-131">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="06f6c-132">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="06f6c-132">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="06f6c-133">修复的问题</span><span class="sxs-lookup"><span data-stu-id="06f6c-133">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="06f6c-134">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="06f6c-134">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="06f6c-135">添加了对 MultiValue 路由方法的支持</span><span class="sxs-lookup"><span data-stu-id="06f6c-135">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="06f6c-136">MultiValue 路由的新参数“MaxReturn”</span><span class="sxs-lookup"><span data-stu-id="06f6c-136">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="06f6c-137">添加了对 Subnet 路由方法的支持</span><span class="sxs-lookup"><span data-stu-id="06f6c-137">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="06f6c-138">对终结点中的 IP 地址范围（子网）的支持</span><span class="sxs-lookup"><span data-stu-id="06f6c-138">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="06f6c-139">添加了对配置文件中的自定义标头的支持</span><span class="sxs-lookup"><span data-stu-id="06f6c-139">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="06f6c-140">添加了对配置文件中的预期状态代码范围的支持</span><span class="sxs-lookup"><span data-stu-id="06f6c-140">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="06f6c-141">添加了对终结点中的自定义标头的支持</span><span class="sxs-lookup"><span data-stu-id="06f6c-141">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="06f6c-142">6.8.0 - 2018 年 8 月</span><span class="sxs-lookup"><span data-stu-id="06f6c-142">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="06f6c-143">常规</span><span class="sxs-lookup"><span data-stu-id="06f6c-143">General</span></span>
* <span data-ttu-id="06f6c-144">解决了未设置默认资源组的问题。</span><span class="sxs-lookup"><span data-stu-id="06f6c-144">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="06f6c-145">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="06f6c-145">AzureRM.Profile</span></span>
* <span data-ttu-id="06f6c-146">为在执行 Connect-AzureRmAccount 期间返回的令牌添加了“过期”属性</span><span class="sxs-lookup"><span data-stu-id="06f6c-146">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="06f6c-147">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="06f6c-147">AzureRM.Compute</span></span>
* <span data-ttu-id="06f6c-148">解决了错误输出中缺少目标的问题。</span><span class="sxs-lookup"><span data-stu-id="06f6c-148">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="06f6c-149">解决了带有托管磁盘的 VM 的存储帐户类型问题</span><span class="sxs-lookup"><span data-stu-id="06f6c-149">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="06f6c-150">解决了在其他环境（例如 Azure 中国）中使用 AEM 扩展 cmdlet 的问题</span><span class="sxs-lookup"><span data-stu-id="06f6c-150">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="06f6c-151">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="06f6c-151">AzureRM.IotHub</span></span>
* <span data-ttu-id="06f6c-152">修复了 New-AzureRmIotHubExportDevices 和 New-AzureRmIotHubImportDevices的示例</span><span class="sxs-lookup"><span data-stu-id="06f6c-152">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="06f6c-153">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="06f6c-153">AzureRM.Network</span></span>
* <span data-ttu-id="06f6c-154">将默认模型表示形式更改为表视图</span><span class="sxs-lookup"><span data-stu-id="06f6c-154">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="06f6c-155">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="06f6c-155">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="06f6c-156">修复了在尝试扩展停用的容量时 Update-AzureRmPowerBIEmbeddedCapacity 中出现的故障</span><span class="sxs-lookup"><span data-stu-id="06f6c-156">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="06f6c-157">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="06f6c-157">AzureRM.Resources</span></span>
* <span data-ttu-id="06f6c-158">解决了从市场创建托管应用程序的问题。</span><span class="sxs-lookup"><span data-stu-id="06f6c-158">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="06f6c-159">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="06f6c-159">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="06f6c-160">解决了以下问题</span><span class="sxs-lookup"><span data-stu-id="06f6c-160">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="06f6c-161">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="06f6c-161">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="06f6c-162">对 MultiValue 路由方法的支持</span><span class="sxs-lookup"><span data-stu-id="06f6c-162">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="06f6c-163">MultiValue 路由的新参数“MaxReturn”</span><span class="sxs-lookup"><span data-stu-id="06f6c-163">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="06f6c-164">对 Subnet 路由方法的支持</span><span class="sxs-lookup"><span data-stu-id="06f6c-164">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="06f6c-165">对终结点中的 IP 地址范围（子网）的支持</span><span class="sxs-lookup"><span data-stu-id="06f6c-165">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="06f6c-166">对配置文件中的自定义标头的支持</span><span class="sxs-lookup"><span data-stu-id="06f6c-166">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="06f6c-167">对配置文件中的预期状态代码范围的支持</span><span class="sxs-lookup"><span data-stu-id="06f6c-167">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="06f6c-168">对终结点中的自定义标头的支持</span><span class="sxs-lookup"><span data-stu-id="06f6c-168">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="06f6c-169">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="06f6c-169">AzureRM.Websites</span></span>
* <span data-ttu-id="06f6c-170">解决了错误地设置默认资源组的问题。</span><span class="sxs-lookup"><span data-stu-id="06f6c-170">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="06f6c-171">6.7.0 - 2018 年 8 月</span><span class="sxs-lookup"><span data-stu-id="06f6c-171">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="06f6c-172">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="06f6c-172">AzureRM.Profile</span></span>
* <span data-ttu-id="06f6c-173">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="06f6c-173">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="06f6c-174">向默认的上下文名称添加用户 ID，避免上下文冲突</span><span class="sxs-lookup"><span data-stu-id="06f6c-174">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="06f6c-175">修复了 Clear-AzureRmContext 在选择上下文 #6398 时出现的问题</span><span class="sxs-lookup"><span data-stu-id="06f6c-175">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="06f6c-176">允许将租户域传递给“Connect-AzureRmAccount”的“-TenantId”参数</span><span class="sxs-lookup"><span data-stu-id="06f6c-176">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="06f6c-177">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="06f6c-177">Azure.Storage</span></span>
* <span data-ttu-id="06f6c-178">去除了 Azure 文件共享配额的 5TB 限制</span><span class="sxs-lookup"><span data-stu-id="06f6c-178">Remove the 5TB limitation for Azure File Share quota</span></span>
- <span data-ttu-id="06f6c-179">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="06f6c-179">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="06f6c-180">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="06f6c-180">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="06f6c-181">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="06f6c-181">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="06f6c-182">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="06f6c-182">Azure.AnalysisServices</span></span>
* <span data-ttu-id="06f6c-183">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="06f6c-183">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="06f6c-184">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="06f6c-184">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="06f6c-185">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="06f6c-185">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="06f6c-186">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="06f6c-186">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="06f6c-187">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="06f6c-187">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="06f6c-188">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="06f6c-188">AzureRM.Automation</span></span>
* <span data-ttu-id="06f6c-189">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="06f6c-189">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="06f6c-190">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="06f6c-190">AzureRM.Backup</span></span>
* <span data-ttu-id="06f6c-191">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="06f6c-191">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="06f6c-192">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="06f6c-192">AzureRM.Batch</span></span>
* <span data-ttu-id="06f6c-193">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="06f6c-193">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="06f6c-194">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="06f6c-194">AzureRM.Billing</span></span>
* <span data-ttu-id="06f6c-195">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="06f6c-195">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="06f6c-196">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="06f6c-196">AzureRM.Cdn</span></span>
* <span data-ttu-id="06f6c-197">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="06f6c-197">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="06f6c-198">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="06f6c-198">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="06f6c-199">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="06f6c-199">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="06f6c-200">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="06f6c-200">AzureRM.Compute</span></span>
* <span data-ttu-id="06f6c-201">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="06f6c-201">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="06f6c-202">为 New-AzureRmVmssConfig 增加了 EvictionPolicy 参数</span><span class="sxs-lookup"><span data-stu-id="06f6c-202">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="06f6c-203">在 New-AzureRmVm 的 DiskFileParameterSet 中使用默认位置（如果未指定 Location）</span><span class="sxs-lookup"><span data-stu-id="06f6c-203">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="06f6c-204">修复了 Save-AzureRmVMImage 中的参数说明</span><span class="sxs-lookup"><span data-stu-id="06f6c-204">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="06f6c-205">修复了某些单次传递相关方案的 Get-AzureRmVMDiskEncryptionStatus cmdlet</span><span class="sxs-lookup"><span data-stu-id="06f6c-205">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="06f6c-206">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="06f6c-206">AzureRM.Consumption</span></span>
* <span data-ttu-id="06f6c-207">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="06f6c-207">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="06f6c-208">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="06f6c-208">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="06f6c-209">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="06f6c-209">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="06f6c-210">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="06f6c-210">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="06f6c-211">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="06f6c-211">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="06f6c-212">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="06f6c-212">AzureRM.DataFactories</span></span>
* <span data-ttu-id="06f6c-213">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="06f6c-213">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="06f6c-214">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="06f6c-214">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="06f6c-215">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="06f6c-215">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="06f6c-216">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="06f6c-216">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="06f6c-217">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="06f6c-217">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="06f6c-218">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="06f6c-218">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="06f6c-219">修复了从 PowerShell 命令行设置 DebugPreference 时的调试问题</span><span class="sxs-lookup"><span data-stu-id="06f6c-219">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="06f6c-220">更新了 Set-AzureRmDataLakeStoreItemAcl 的示例</span><span class="sxs-lookup"><span data-stu-id="06f6c-220">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="06f6c-221">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="06f6c-221">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="06f6c-222">更新了 Set-AzureRmDataLakeStoreItemAclEntry 的示例</span><span class="sxs-lookup"><span data-stu-id="06f6c-222">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="06f6c-223">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="06f6c-223">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="06f6c-224">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="06f6c-224">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="06f6c-225">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="06f6c-225">AzureRM.Dns</span></span>
* <span data-ttu-id="06f6c-226">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="06f6c-226">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="06f6c-227">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="06f6c-227">AzureRM.EventGrid</span></span>
* <span data-ttu-id="06f6c-228">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="06f6c-228">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="06f6c-229">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="06f6c-229">AzureRM.EventHub</span></span>
* <span data-ttu-id="06f6c-230">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="06f6c-230">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="06f6c-231">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="06f6c-231">AzureRM.HDInsight</span></span>
* <span data-ttu-id="06f6c-232">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="06f6c-232">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="06f6c-233">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="06f6c-233">AzureRM.Insights</span></span>
* <span data-ttu-id="06f6c-234">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="06f6c-234">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="06f6c-235">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="06f6c-235">AzureRM.IotHub</span></span>
* <span data-ttu-id="06f6c-236">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="06f6c-236">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="06f6c-237">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="06f6c-237">AzureRM.KeyVault</span></span>
* <span data-ttu-id="06f6c-238">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="06f6c-238">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="06f6c-239">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="06f6c-239">AzureRM.LogicApp</span></span>
* <span data-ttu-id="06f6c-240">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="06f6c-240">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="06f6c-241">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="06f6c-241">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="06f6c-242">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="06f6c-242">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="06f6c-243">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="06f6c-243">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="06f6c-244">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="06f6c-244">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="06f6c-245">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="06f6c-245">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="06f6c-246">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="06f6c-246">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="06f6c-247">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="06f6c-247">AzureRM.Media</span></span>
* <span data-ttu-id="06f6c-248">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="06f6c-248">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="06f6c-249">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="06f6c-249">AzureRM.Network</span></span>
* <span data-ttu-id="06f6c-250">增加了 Set-AzureRmLocalNetworkGateway 的示例</span><span class="sxs-lookup"><span data-stu-id="06f6c-250">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="06f6c-251">增加了 Add-AzureRmVirtualNetworkGatewayIpConfig、Get-AzureRmVirtualNetworkGatewayConnectionSharedKey 和 New-AzureRmVirtualNetworkGatewayConnection 的示例和说明</span><span class="sxs-lookup"><span data-stu-id="06f6c-251">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="06f6c-252">增加了 Remove-AzureRmVirtualNetworkGatewayIpConfig 和 Reset-AzureRmVirtualNetworkGateway 的示例</span><span class="sxs-lookup"><span data-stu-id="06f6c-252">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="06f6c-253">增加了 Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey 的示例</span><span class="sxs-lookup"><span data-stu-id="06f6c-253">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="06f6c-254">增加了 Set-AzureRmVirtualNetworkGatewayConnectionSharedKey 的示例</span><span class="sxs-lookup"><span data-stu-id="06f6c-254">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="06f6c-255">增加了 Set-AzureRmVirtualNetworkGatewayConnection 的示例</span><span class="sxs-lookup"><span data-stu-id="06f6c-255">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="06f6c-256">使用最新的代码生成器重新生成了 ApplicationSecurityGroup、RouteTable 和 Usage 的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="06f6c-256">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="06f6c-257">阐明了在尝试获取的子网不存在时 Get-AzureRmVirtualNetworkSubnetConfig 的错误消息</span><span class="sxs-lookup"><span data-stu-id="06f6c-257">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="06f6c-258">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="06f6c-258">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="06f6c-259">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="06f6c-259">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="06f6c-260">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="06f6c-260">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="06f6c-261">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="06f6c-261">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="06f6c-262">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="06f6c-262">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="06f6c-263">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="06f6c-263">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="06f6c-264">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="06f6c-264">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="06f6c-265">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="06f6c-265">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="06f6c-266">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="06f6c-266">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="06f6c-267">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="06f6c-267">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="06f6c-268">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="06f6c-268">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="06f6c-269">为 Get-AzureRmRecoveryServicesBackItem cmdlet 增加了策略筛选器。</span><span class="sxs-lookup"><span data-stu-id="06f6c-269">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="06f6c-270">此命令返回受给定策略 ID 保护的备份项的列表。</span><span class="sxs-lookup"><span data-stu-id="06f6c-270">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="06f6c-271">已将 Microsoft.Azure.Management.RecoveryServices.Backup 更新到 3.0.0-preview 版本。</span><span class="sxs-lookup"><span data-stu-id="06f6c-271">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="06f6c-272">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="06f6c-272">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="06f6c-273">为 Restore-AzureRmRecoveryServicesBackupItem 增加了 TargetResourceGroupName 参数。</span><span class="sxs-lookup"><span data-stu-id="06f6c-273">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="06f6c-274">托管磁盘还原到的资源组。</span><span class="sxs-lookup"><span data-stu-id="06f6c-274">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="06f6c-275">适用于包含托管磁盘的 VM 的备份。</span><span class="sxs-lookup"><span data-stu-id="06f6c-275">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="06f6c-276">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="06f6c-276">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="06f6c-277">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="06f6c-277">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="06f6c-278">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="06f6c-278">AzureRM.RedisCache</span></span>
* <span data-ttu-id="06f6c-279">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="06f6c-279">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="06f6c-280">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="06f6c-280">AzureRM.Relay</span></span>
* <span data-ttu-id="06f6c-281">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="06f6c-281">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="06f6c-282">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="06f6c-282">AzureRM.Resources</span></span>
* <span data-ttu-id="06f6c-283">支持在订阅范围部署模板。</span><span class="sxs-lookup"><span data-stu-id="06f6c-283">Support template deployment at subscription scope.</span></span> <span data-ttu-id="06f6c-284">增加了新 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="06f6c-284">Add new Cmdlets:</span></span>
    - <span data-ttu-id="06f6c-285">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="06f6c-285">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="06f6c-286">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="06f6c-286">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="06f6c-287">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="06f6c-287">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="06f6c-288">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="06f6c-288">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="06f6c-289">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="06f6c-289">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="06f6c-290">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="06f6c-290">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="06f6c-291">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="06f6c-291">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="06f6c-292">修复了在将上下文传递给 Set-AzureRmResource 时引发错误的问题</span><span class="sxs-lookup"><span data-stu-id="06f6c-292">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="06f6c-293">修复了 New-AzureRmResourceGroupDeployment 中的示例</span><span class="sxs-lookup"><span data-stu-id="06f6c-293">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="06f6c-294">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="06f6c-294">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="06f6c-295">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="06f6c-295">AzureRM.Scheduler</span></span>
* <span data-ttu-id="06f6c-296">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="06f6c-296">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="06f6c-297">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="06f6c-297">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="06f6c-298">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="06f6c-298">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="06f6c-299">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="06f6c-299">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="06f6c-300">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="06f6c-300">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="06f6c-301">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="06f6c-301">AzureRM.Sql</span></span>
* <span data-ttu-id="06f6c-302">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="06f6c-302">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="06f6c-303">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="06f6c-303">AzureRM.Storage</span></span>
* <span data-ttu-id="06f6c-304">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="06f6c-304">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="06f6c-305">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="06f6c-305">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="06f6c-306">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="06f6c-306">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="06f6c-307">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="06f6c-307">AzureRM.Tags</span></span>
* <span data-ttu-id="06f6c-308">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="06f6c-308">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="06f6c-309">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="06f6c-309">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="06f6c-310">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="06f6c-310">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="06f6c-311">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="06f6c-311">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="06f6c-312">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="06f6c-312">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="06f6c-313">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="06f6c-313">AzureRM.Websites</span></span>
* <span data-ttu-id="06f6c-314">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="06f6c-314">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="06f6c-315">6.6.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="06f6c-315">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="06f6c-316">常规</span><span class="sxs-lookup"><span data-stu-id="06f6c-316">General</span></span>
* <span data-ttu-id="06f6c-317">更新了所有帮助文件，以包括完整参数类型和正确的输入/输出类型。</span><span class="sxs-lookup"><span data-stu-id="06f6c-317">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="06f6c-318">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="06f6c-318">AzureRM.Profile</span></span>
* <span data-ttu-id="06f6c-319">更新了 Common.Strategy 库，以便能够验证资源的当前配置是否与目标资源兼容。</span><span class="sxs-lookup"><span data-stu-id="06f6c-319">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="06f6c-320">在 Common.Storage 中添加了 ps1xml 类型</span><span class="sxs-lookup"><span data-stu-id="06f6c-320">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="06f6c-321">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="06f6c-321">Azure.Storage</span></span>
* <span data-ttu-id="06f6c-322">增加了从 DefaultProfile 获取存储上下文的支持</span><span class="sxs-lookup"><span data-stu-id="06f6c-322">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="06f6c-323">为 cmdlet 输出类型属性增加了 Ps1XmlAttribute。</span><span class="sxs-lookup"><span data-stu-id="06f6c-323">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="06f6c-324">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="06f6c-324">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="06f6c-325">修复了问题 https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="06f6c-325">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="06f6c-326">修复了 Automapper 中将 PsApiManagementApi 转换为 ApiContract 的 bug</span><span class="sxs-lookup"><span data-stu-id="06f6c-326">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="06f6c-327">修复了问题 https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="06f6c-327">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="06f6c-328">修复了 File.Save 中没有使用编码类型重载的 bug</span><span class="sxs-lookup"><span data-stu-id="06f6c-328">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="06f6c-329">修复了问题 https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="06f6c-329">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="06f6c-330">升级到了 4.0.3 Nuget版本，该版本修复了 apiId 上的模式异常</span><span class="sxs-lookup"><span data-stu-id="06f6c-330">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="06f6c-331">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="06f6c-331">AzureRM.Compute</span></span>
* <span data-ttu-id="06f6c-332">修复因使用 PremiumLRS 存储帐户类型重命名而在 New-AzureRmVm 中使用 DiskFileParameterSet 创建 VM 失败的问题。</span><span class="sxs-lookup"><span data-stu-id="06f6c-332">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="06f6c-333">修复 Invoke-AzureRmVMRunCommand cmdlet</span><span class="sxs-lookup"><span data-stu-id="06f6c-333">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="06f6c-334">更新 Get-AzureRmAvailabilitySet 以启用列出订阅中的所有可用性集。</span><span class="sxs-lookup"><span data-stu-id="06f6c-334">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="06f6c-335">（ResouceGroupName 参数现在是可选的。）</span><span class="sxs-lookup"><span data-stu-id="06f6c-335">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="06f6c-336">更新“New-AzureRmVm”的 SimpleParameterSet 以在符合条件的 VM 上启用加速网络。</span><span class="sxs-lookup"><span data-stu-id="06f6c-336">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="06f6c-337">将 New-AzureRmVmss 简单参数集更新为在用户指定的 LB 已存在时创建 vmss 失败。</span><span class="sxs-lookup"><span data-stu-id="06f6c-337">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="06f6c-338">更新 New-AzureRmDisk 的示例</span><span class="sxs-lookup"><span data-stu-id="06f6c-338">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="06f6c-339">添加“New-AzureRmVM”的示例</span><span class="sxs-lookup"><span data-stu-id="06f6c-339">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="06f6c-340">更新 Set-AzureRmVMOSDisk 的说明</span><span class="sxs-lookup"><span data-stu-id="06f6c-340">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="06f6c-341">更新 Set-AzureRmVMBginfoExtension 的示例 1 以更正拼写和前缀。</span><span class="sxs-lookup"><span data-stu-id="06f6c-341">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="06f6c-342">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="06f6c-342">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="06f6c-343">将 ADF .Net SDK 版本更新为 1.1.0。</span><span class="sxs-lookup"><span data-stu-id="06f6c-343">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="06f6c-344">支持跨数据工厂的自承载集成运行时共享。</span><span class="sxs-lookup"><span data-stu-id="06f6c-344">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="06f6c-345">将新参数 -SharedIntegrationRuntimeResourceId 添加到 Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet。</span><span class="sxs-lookup"><span data-stu-id="06f6c-345">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="06f6c-346">将新的可选参数 -LinkedDataFactoryName 添加到 Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet。</span><span class="sxs-lookup"><span data-stu-id="06f6c-346">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="06f6c-347">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="06f6c-347">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="06f6c-348">将数据平面 SDK (Microsoft.Azure.DataLake.Store) 版本更新为 1.1.9</span><span class="sxs-lookup"><span data-stu-id="06f6c-348">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="06f6c-349">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="06f6c-349">AzureRM.EventHub</span></span>
* <span data-ttu-id="06f6c-350">在删除 cmdlet 中更新了 InputObject 和 ResourceId 的管道</span><span class="sxs-lookup"><span data-stu-id="06f6c-350">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="06f6c-351">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="06f6c-351">AzureRM.Insights</span></span>
* <span data-ttu-id="06f6c-352">修复了帮助文件中 OutputType 的格式问题</span><span class="sxs-lookup"><span data-stu-id="06f6c-352">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="06f6c-353">使用 Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span><span class="sxs-lookup"><span data-stu-id="06f6c-353">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="06f6c-354">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="06f6c-354">AzureRM.KeyVault</span></span>
* <span data-ttu-id="06f6c-355">修复了 Set-AzureRmKeyVaultAccessPolicy 中的管道问题</span><span class="sxs-lookup"><span data-stu-id="06f6c-355">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="06f6c-356">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="06f6c-356">AzureRM.Network</span></span>
* <span data-ttu-id="06f6c-357">添加了 LoadBalancerInboundNatPoolConfig cmdlet 的示例。</span><span class="sxs-lookup"><span data-stu-id="06f6c-357">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="06f6c-358">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="06f6c-358">AzureRM.Resources</span></span>
* <span data-ttu-id="06f6c-359">修复了为“Get-AzureRmResource”同时提供标记名称和值时出现的问题</span><span class="sxs-lookup"><span data-stu-id="06f6c-359">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="06f6c-360">使用“Set-AzureRmResource”修复管道方案</span><span class="sxs-lookup"><span data-stu-id="06f6c-360">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="06f6c-361">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="06f6c-361">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="06f6c-362">在删除 cmdlet 中更新了 InputObject 和 ResourceId 的管道</span><span class="sxs-lookup"><span data-stu-id="06f6c-362">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="06f6c-363">修复了几个问题</span><span class="sxs-lookup"><span data-stu-id="06f6c-363">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="06f6c-364">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="06f6c-364">AzureRM.Sql</span></span>
* <span data-ttu-id="06f6c-365">使用以下 cmdlet 添加服务器高级威胁防护支持：</span><span class="sxs-lookup"><span data-stu-id="06f6c-365">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="06f6c-366">Enable-AzureRmSqlServerAdvancedThreatProtection；Disable-AzureRmSqlServerAdvancedThreatProtection；Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="06f6c-366">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="06f6c-367">使用以下 cmdlet 添加漏洞评估支持：</span><span class="sxs-lookup"><span data-stu-id="06f6c-367">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="06f6c-368">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings；Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings；Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="06f6c-368">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="06f6c-369">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline；Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline；Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="06f6c-369">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="06f6c-370">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan；Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord；Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="06f6c-370">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="06f6c-371">修复了 Remove-AzureRmSqlServerFirewallRule 中的示例</span><span class="sxs-lookup"><span data-stu-id="06f6c-371">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="06f6c-372">修复了 Get-AzureSqlSyncGroupLog 中非美国基础文化的日期时间处理错误</span><span class="sxs-lookup"><span data-stu-id="06f6c-372">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="06f6c-373">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="06f6c-373">AzureRM.Storage</span></span>
* <span data-ttu-id="06f6c-374">将 Ps1XmlAttribute 添加到 cmdlet 输出类型属性</span><span class="sxs-lookup"><span data-stu-id="06f6c-374">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="06f6c-375">在表视图中显示 StorageAccount cmdlet 输出</span><span class="sxs-lookup"><span data-stu-id="06f6c-375">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="06f6c-376">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="06f6c-376">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="06f6c-377">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="06f6c-377">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="06f6c-378">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="06f6c-378">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="06f6c-379">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="06f6c-379">AzureRM.Tags</span></span>
* <span data-ttu-id="06f6c-380">从 Tag cmdlet 帮助中删除不正确的语句</span><span class="sxs-lookup"><span data-stu-id="06f6c-380">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="06f6c-381">6.5.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="06f6c-381">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="06f6c-382">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="06f6c-382">AzureRM.Profile</span></span>
* <span data-ttu-id="06f6c-383">更新了“Get-AzureRmContextAutosaveSetting”的帮助</span><span class="sxs-lookup"><span data-stu-id="06f6c-383">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="06f6c-384">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="06f6c-384">Azure.Storage</span></span>
* <span data-ttu-id="06f6c-385">支持使用只写 Sas 令牌上传 Blob 或文件</span><span class="sxs-lookup"><span data-stu-id="06f6c-385">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="06f6c-386">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="06f6c-386">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="06f6c-387">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="06f6c-387">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="06f6c-388">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="06f6c-388">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="06f6c-389">将所需属性 ResourceGroupName 添加到 AS。</span><span class="sxs-lookup"><span data-stu-id="06f6c-389">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="06f6c-390">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="06f6c-390">AzureRM.Automation</span></span>
* <span data-ttu-id="06f6c-391">更新帮助并添加“New-AzureRMAutomationSchedule”的示例</span><span class="sxs-lookup"><span data-stu-id="06f6c-391">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="06f6c-392">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="06f6c-392">AzureRM.Compute</span></span>
* <span data-ttu-id="06f6c-393">将 -Tag 参数添加到 Update/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="06f6c-393">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="06f6c-394">添加“Add-AzureRmVmssExtension”的示例</span><span class="sxs-lookup"><span data-stu-id="06f6c-394">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="06f6c-395">添加“Remove-AzureRmVmssExtension”的示例</span><span class="sxs-lookup"><span data-stu-id="06f6c-395">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="06f6c-396">更新“Set-AzureRmVMAccessExtension”的帮助</span><span class="sxs-lookup"><span data-stu-id="06f6c-396">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="06f6c-397">更新 New-AzureRmVmss 的 SimpleParameterSet，以默认情况下将 SinglePlacementGroup 设置为false，并添加开关参数“SinglePlacementGroup”，使用户能够在单个放置组中创建 VMSS。</span><span class="sxs-lookup"><span data-stu-id="06f6c-397">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="06f6c-398">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="06f6c-398">AzureRM.EventHub</span></span>
* <span data-ttu-id="06f6c-399">向 PSEventHubDRConfigurationAttributes 类添加了一个只读属性“PendingReplicationOperationsCount”，该属性在复制过程中为挂起的复制操作计数</span><span class="sxs-lookup"><span data-stu-id="06f6c-399">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="06f6c-400">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="06f6c-400">AzureRM.KeyVault</span></span>
* <span data-ttu-id="06f6c-401">更新了 Set-AzureRmKeyVaultAccessPolicy 的错误消息</span><span class="sxs-lookup"><span data-stu-id="06f6c-401">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="06f6c-402">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="06f6c-402">AzureRM.LogicApp</span></span>
* <span data-ttu-id="06f6c-403">修复了 New-AzureRmLogicApp 中的“无法解析参数集”错误</span><span class="sxs-lookup"><span data-stu-id="06f6c-403">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="06f6c-404">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="06f6c-404">AzureRM.Network</span></span>
* <span data-ttu-id="06f6c-405">在多个租户中为 Set/Add-AzureRmVirtualNetworkPeering 启用跨虚拟网络对等互连</span><span class="sxs-lookup"><span data-stu-id="06f6c-405">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="06f6c-406">针对应用程序网关更新了以下 cmdlet</span><span class="sxs-lookup"><span data-stu-id="06f6c-406">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="06f6c-407">New-AzureRmApplicationGateway：添加了 EnableFIPS 标志和区域支持</span><span class="sxs-lookup"><span data-stu-id="06f6c-407">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="06f6c-408">New-AzureRmApplicationGatewaySku：添加了新的 sku Standard_v2 和 WAF_v2</span><span class="sxs-lookup"><span data-stu-id="06f6c-408">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="06f6c-409">Set-AzureRmApplicationGatewaySku：添加了新的 sku Standard_v2 和 WAF_v2</span><span class="sxs-lookup"><span data-stu-id="06f6c-409">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="06f6c-410">使用最新的生成器版本重新生成了 RouteTable cmdlet</span><span class="sxs-lookup"><span data-stu-id="06f6c-410">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="06f6c-411">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="06f6c-411">AzureRM.Relay</span></span>
* <span data-ttu-id="06f6c-412">更新了 Markdown 文件，其中修复了示例中的参数名称问题</span><span class="sxs-lookup"><span data-stu-id="06f6c-412">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="06f6c-413">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="06f6c-413">AzureRM.Resources</span></span>
* <span data-ttu-id="06f6c-414">更新了 Roleassignment 和 roledefinition cmdlet：</span><span class="sxs-lookup"><span data-stu-id="06f6c-414">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="06f6c-415">删除了作为分页的一部分完成的额外 roledefinition 调用。</span><span class="sxs-lookup"><span data-stu-id="06f6c-415">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="06f6c-416">修复了 Get-AzureRmRoleAssignment cmdlet</span><span class="sxs-lookup"><span data-stu-id="06f6c-416">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="06f6c-417">修复了 -ExpandPrincipalGroups 命令参数功能</span><span class="sxs-lookup"><span data-stu-id="06f6c-417">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="06f6c-418">修复了“Get-AzureRmResource”的问题，其中“-ResourceType”参数区分大小写</span><span class="sxs-lookup"><span data-stu-id="06f6c-418">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="06f6c-419">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="06f6c-419">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="06f6c-420">向列表 cmdlet 添加了 top 和 skip 参数</span><span class="sxs-lookup"><span data-stu-id="06f6c-420">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="06f6c-421">添加了标准到高级命名空间迁移 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="06f6c-421">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="06f6c-422">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="06f6c-422">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="06f6c-423">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="06f6c-423">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="06f6c-424">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="06f6c-424">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="06f6c-425">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="06f6c-425">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="06f6c-426">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="06f6c-426">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="06f6c-427">向 PSServiceBusDRConfigurationAttributes 类添加了一个只读属性“PendingReplicationOperationsCount”，该属性在复制过程中为挂起的复制操作计数</span><span class="sxs-lookup"><span data-stu-id="06f6c-427">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="06f6c-428">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="06f6c-428">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="06f6c-429">更新了“New-AzureRmServiceFabricCluster”的示例</span><span class="sxs-lookup"><span data-stu-id="06f6c-429">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="06f6c-430">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="06f6c-430">AzureRM.Sql</span></span>
* <span data-ttu-id="06f6c-431">为 Management.Sql 添加新的 Cmdlet，以允许客户将 TDE 证书添加到 Sql Server 实例或托管实例</span><span class="sxs-lookup"><span data-stu-id="06f6c-431">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="06f6c-432">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="06f6c-432">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="06f6c-433">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="06f6c-433">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="06f6c-434">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="06f6c-434">AzureRM.Websites</span></span>
* <span data-ttu-id="06f6c-435">设置为 false 时，`Set-AzureRmWebApp -AssignIdentity` 和 `Set-AzureRmWebAppSlot -AssignIdentity` 现在将从站点对象中删除 Identity 属性。同时移除预览标记。</span><span class="sxs-lookup"><span data-stu-id="06f6c-435">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="06f6c-436">`Get-AzureRmWebAppMetrics`、`Get-AzureRmAppServicePlanMetrics` 示例已更新</span><span class="sxs-lookup"><span data-stu-id="06f6c-436">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="06f6c-437">`Set-AzureRmWebApp -PhpVersion` 支持 off 作为有效的 php 版本</span><span class="sxs-lookup"><span data-stu-id="06f6c-437">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="06f6c-438">6.4.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="06f6c-438">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="06f6c-439">常规</span><span class="sxs-lookup"><span data-stu-id="06f6c-439">General</span></span>
* <span data-ttu-id="06f6c-440">修复了大多数模块的帮助文件中的 OutputType 格式问题</span><span class="sxs-lookup"><span data-stu-id="06f6c-440">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="06f6c-441">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="06f6c-441">AzureRM.Profile</span></span>
* <span data-ttu-id="06f6c-442">已将 Ps1Xml 属性添加到基本输出类型</span><span class="sxs-lookup"><span data-stu-id="06f6c-442">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="06f6c-443">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="06f6c-443">AzureRM.Compute</span></span>
* <span data-ttu-id="06f6c-444">VMSS 的 IP 标记功能</span><span class="sxs-lookup"><span data-stu-id="06f6c-444">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="06f6c-445">已添加“New-AzureRmVmssIpTagConfig”cmdlet</span><span class="sxs-lookup"><span data-stu-id="06f6c-445">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="06f6c-446">已将 IpTag 参数添加到 New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="06f6c-446">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="06f6c-447">VMSS 的自动 OS 回滚功能</span><span class="sxs-lookup"><span data-stu-id="06f6c-447">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="06f6c-448">已将 DisableAutoRollback 参数添加到 New-AzureRmVmssConfig 和 Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="06f6c-448">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="06f6c-449">VMSS 的 OS 升级历史记录功能</span><span class="sxs-lookup"><span data-stu-id="06f6c-449">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="06f6c-450">已将 OSUpgradeHistory 开关参数添加到 Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="06f6c-450">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="06f6c-451">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="06f6c-451">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="06f6c-452">通过以下命令添加目录 ACL 的支持：</span><span class="sxs-lookup"><span data-stu-id="06f6c-452">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="06f6c-453">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="06f6c-453">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="06f6c-454">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="06f6c-454">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="06f6c-455">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="06f6c-455">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="06f6c-456">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="06f6c-456">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="06f6c-457">为 Set-AzureRmDataLakeStoreItemAclEntry、Remove-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAcl 添加了取消支持和进度跟踪</span><span class="sxs-lookup"><span data-stu-id="06f6c-457">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="06f6c-458">为 Export-AzureRmDataLakeStoreChildItemProperties 添加了取消支持</span><span class="sxs-lookup"><span data-stu-id="06f6c-458">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="06f6c-459">修复了执行递归操作的 cmdlet 的调试消息刷新</span><span class="sxs-lookup"><span data-stu-id="06f6c-459">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="06f6c-460">修复了 DataLake cmdlet 的测试位置</span><span class="sxs-lookup"><span data-stu-id="06f6c-460">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="06f6c-461">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="06f6c-461">AzureRM.EventHub</span></span>
* <span data-ttu-id="06f6c-462">已将可选的 MaxCount 参数添加到“列出操作”cmdlet Get-AzureRmEventHub 和 Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="06f6c-462">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="06f6c-463">修复了 New-AzureRmEventHub cmdlet 的问题：创建新事件中心时至少需要一个参数。</span><span class="sxs-lookup"><span data-stu-id="06f6c-463">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="06f6c-464">提供了默认参数集。</span><span class="sxs-lookup"><span data-stu-id="06f6c-464">Provided Default Parameter set.</span></span>
* <span data-ttu-id="06f6c-465">已将可选参数 -KeyValue 添加到 New-AzureRmEventHubKey cmdlet，该参数可让用户提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="06f6c-465">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="06f6c-466">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="06f6c-466">AzureRM.KeyVault</span></span>
* <span data-ttu-id="06f6c-467">修复了 Get-AzureRmKeyVault -Tag 返回所有资源的问题</span><span class="sxs-lookup"><span data-stu-id="06f6c-467">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="06f6c-468">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="06f6c-468">AzureRM.Network</span></span>
* <span data-ttu-id="06f6c-469">为区域冗余的 VirtualNetworkGateways 公开新 SKU</span><span class="sxs-lookup"><span data-stu-id="06f6c-469">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="06f6c-470">通过 ARM 为以下功能添加了新命令：ExpressRoute 合作伙伴 API</span><span class="sxs-lookup"><span data-stu-id="06f6c-470">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="06f6c-471">添加了 Get-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="06f6c-471">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="06f6c-472">添加了 Set-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="06f6c-472">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="06f6c-473">添加了 Add-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="06f6c-473">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="06f6c-474">添加了 Get-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="06f6c-474">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="06f6c-475">添加了 Remove-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="06f6c-475">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="06f6c-476">添加了 Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="06f6c-476">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="06f6c-477">添加了 Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="06f6c-477">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="06f6c-478">添加了 Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="06f6c-478">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="06f6c-479">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="06f6c-479">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="06f6c-480">添加了 Get-AzureRmRecoveryServicesBackupStatus cmdlet。</span><span class="sxs-lookup"><span data-stu-id="06f6c-480">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="06f6c-481">此 cmdlet 采用 VM ID，并检查 VM 是否受订阅中的某个保管库保护。</span><span class="sxs-lookup"><span data-stu-id="06f6c-481">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="06f6c-482">如果存在此类保管库，该 cmdlet 会输出该保管库的详细信息。</span><span class="sxs-lookup"><span data-stu-id="06f6c-482">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="06f6c-483">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="06f6c-483">AzureRM.Resources</span></span>
* <span data-ttu-id="06f6c-484">更新了 Get-AzureRmPolicyAssignment cmdlet：</span><span class="sxs-lookup"><span data-stu-id="06f6c-484">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="06f6c-485">添加了在管理组级别列出 -Scope 值的支持</span><span class="sxs-lookup"><span data-stu-id="06f6c-485">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="06f6c-486">添加了在管理组级别使用 -Scope 值检索单个分配的支持</span><span class="sxs-lookup"><span data-stu-id="06f6c-486">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="06f6c-487">已将 -Effective 和 -All 开关添加到 control 参数</span><span class="sxs-lookup"><span data-stu-id="06f6c-487">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="06f6c-488">更新了 Get/New/Remove/Set-AzureRmPolicyDefinition cmdlet</span><span class="sxs-lookup"><span data-stu-id="06f6c-488">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="06f6c-489">添加了 -ManagementGroupName 参数，以将操作应用到给定的管理组</span><span class="sxs-lookup"><span data-stu-id="06f6c-489">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="06f6c-490">添加了 -SubscriptionId 参数，以将操作应用到给定的订阅</span><span class="sxs-lookup"><span data-stu-id="06f6c-490">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="06f6c-491">更新了 Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlet</span><span class="sxs-lookup"><span data-stu-id="06f6c-491">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="06f6c-492">添加了 -ManagementGroupName 参数，以将操作应用到给定的管理组</span><span class="sxs-lookup"><span data-stu-id="06f6c-492">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="06f6c-493">添加了 -SubscriptionId 参数，以将操作应用到给定的订阅</span><span class="sxs-lookup"><span data-stu-id="06f6c-493">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="06f6c-494">添加了使用 TemplateParameterObject 时在参数中指定 KeyVault 机密引用的支持</span><span class="sxs-lookup"><span data-stu-id="06f6c-494">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="06f6c-495">修复了忽略“New-AzureRmADAppCredential”的“-EndDate”参数的问题</span><span class="sxs-lookup"><span data-stu-id="06f6c-495">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="06f6c-496">修复了“Add-AzureRmADGroupMember”使用错误的 URL 发出请求的问题</span><span class="sxs-lookup"><span data-stu-id="06f6c-496">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="06f6c-497">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="06f6c-497">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="06f6c-498">已将可选参数 -KeyValue 添加到 New-AzureRmServiceBusKey cmdlet，该参数可让用户提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="06f6c-498">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="06f6c-499">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="06f6c-499">AzureRM.Sql</span></span>
* <span data-ttu-id="06f6c-500">在 AzureRmSqlDatabaseRestorePoint 帮助中澄清了 SQLDW 的用户定义还原点</span><span class="sxs-lookup"><span data-stu-id="06f6c-500">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="06f6c-501">更新了多个 cmdlet 中 -ComputeGeneration 参数的文档</span><span class="sxs-lookup"><span data-stu-id="06f6c-501">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="06f6c-502">6.3.0 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="06f6c-502">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="06f6c-503">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="06f6c-503">AzureRM.Profile</span></span>
* <span data-ttu-id="06f6c-504">更新了 Enable-AzureRmContextAutoSave 的错误消息</span><span class="sxs-lookup"><span data-stu-id="06f6c-504">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="06f6c-505">在运行没有旧上下文的“Connect-AzureRmAccount”时为每个订阅创建一个上下文</span><span class="sxs-lookup"><span data-stu-id="06f6c-505">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="06f6c-506">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="06f6c-506">Azure.Storage</span></span>
* <span data-ttu-id="06f6c-507">在帮助文件中增加了关于 -Permissions 参数的其他信息。</span><span class="sxs-lookup"><span data-stu-id="06f6c-507">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="06f6c-508">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="06f6c-508">AzureRM.Compute</span></span>
* <span data-ttu-id="06f6c-509">“Get-AzureRmVmDiskEncryptionStatus”修复了一个针对没有数据磁盘的 VM 观察到的问题</span><span class="sxs-lookup"><span data-stu-id="06f6c-509">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="06f6c-510">更新计算客户端库版本以修复以下 cmdlet</span><span class="sxs-lookup"><span data-stu-id="06f6c-510">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="06f6c-511">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="06f6c-511">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="06f6c-512">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="06f6c-512">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="06f6c-513">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="06f6c-513">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="06f6c-514">修复了以下 cmdlet，因此可以正确地显示“操作 ID”和“操作状态”：</span><span class="sxs-lookup"><span data-stu-id="06f6c-514">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="06f6c-515">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="06f6c-515">Start-AzureRmVM</span></span>
    - <span data-ttu-id="06f6c-516">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="06f6c-516">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="06f6c-517">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="06f6c-517">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="06f6c-518">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="06f6c-518">Set-AzureRmVM</span></span>
    - <span data-ttu-id="06f6c-519">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="06f6c-519">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="06f6c-520">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="06f6c-520">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="06f6c-521">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="06f6c-521">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="06f6c-522">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="06f6c-522">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="06f6c-523">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="06f6c-523">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="06f6c-524">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="06f6c-524">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="06f6c-525">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="06f6c-525">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="06f6c-526">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="06f6c-526">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="06f6c-527">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="06f6c-527">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="06f6c-528">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="06f6c-528">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="06f6c-529">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="06f6c-529">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="06f6c-530">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="06f6c-530">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="06f6c-531">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="06f6c-531">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="06f6c-532">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="06f6c-532">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="06f6c-533">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="06f6c-533">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="06f6c-534">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="06f6c-534">AzureRM.EventGrid</span></span>
* <span data-ttu-id="06f6c-535">在 Update-AzureRmEventGridSubscription cmdlet 中删除 SubjectBeginsWith/SubjectEndsWith 的 ValidateNotNullOrEmpty 验证条件，允许根据需要将这些参数更改为空字符串。</span><span class="sxs-lookup"><span data-stu-id="06f6c-535">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="06f6c-536">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="06f6c-536">AzureRM.KeyVault</span></span>
* <span data-ttu-id="06f6c-537">修复运行 Get-AzureRmKeyVault -Tag 时不返回任何标记的问题</span><span class="sxs-lookup"><span data-stu-id="06f6c-537">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="06f6c-538">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="06f6c-538">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="06f6c-539">策略见解 cmdlet 的公开发行版</span><span class="sxs-lookup"><span data-stu-id="06f6c-539">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="06f6c-540">使用 API 版本 2018-04-04</span><span class="sxs-lookup"><span data-stu-id="06f6c-540">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="06f6c-541">向 Get-AzureRmPolicyStateSummary 的结果添加了 PolicyDefinitionReferenceId</span><span class="sxs-lookup"><span data-stu-id="06f6c-541">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="06f6c-542">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="06f6c-542">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="06f6c-543">向 RecoveryServices.Backup cmdlet 添加了 -Vault 参数。</span><span class="sxs-lookup"><span data-stu-id="06f6c-543">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="06f6c-544">传递时，此项会替代 Set-AzureRmRecoveryServicesContext cmdlet。</span><span class="sxs-lookup"><span data-stu-id="06f6c-544">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="06f6c-545">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="06f6c-545">AzureRM.Sql</span></span>
* <span data-ttu-id="06f6c-546">更新了 Get-AzureRmSqlDatabaseExpanded 的帮助文件中的示例</span><span class="sxs-lookup"><span data-stu-id="06f6c-546">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="06f6c-547">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="06f6c-547">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="06f6c-548">更新了 Add-AzureRmTrafficManagerEndpointConfig 的帮助文件</span><span class="sxs-lookup"><span data-stu-id="06f6c-548">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="06f6c-549">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="06f6c-549">AzureRM.Websites</span></span>
* <span data-ttu-id="06f6c-550">更新了“Set-AzureRmWebApp”，在使用 -AssignIdentity 时不覆盖 AppSettings</span><span class="sxs-lookup"><span data-stu-id="06f6c-550">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="06f6c-551">更新了“New-AzureRmWebAppSlot”，允许使用 AppServicePlan 作为可选参数</span><span class="sxs-lookup"><span data-stu-id="06f6c-551">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="06f6c-552">6.2.1 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="06f6c-552">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="06f6c-553">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="06f6c-553">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="06f6c-554">更新了 PSWorkspace 模型，允许 Network 使用 type 作为参数</span><span class="sxs-lookup"><span data-stu-id="06f6c-554">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="06f6c-555">6.2.0 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="06f6c-555">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="06f6c-556">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="06f6c-556">AzureRM.Profile</span></span>
* <span data-ttu-id="06f6c-557">修复了 Newtonsoft.Json 的版本 10.0.3 在模块导入时无法加载的问题</span><span class="sxs-lookup"><span data-stu-id="06f6c-557">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="06f6c-558">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="06f6c-558">AzureRM.Compute</span></span>
* <span data-ttu-id="06f6c-559">VMSS VM 更新功能</span><span class="sxs-lookup"><span data-stu-id="06f6c-559">VMSS VM Update feature</span></span>
    - <span data-ttu-id="06f6c-560">增加了“Update-AzureRmVmssVM”和“New-AzureRmVMDataDisk”cmdlet</span><span class="sxs-lookup"><span data-stu-id="06f6c-560">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="06f6c-561">为“Add-AzureRmVMDataDisk”cmdlet 增加了 VirtualMachineScaleSetVM 参数，支持向 Vmss VM 添加数据磁盘。</span><span class="sxs-lookup"><span data-stu-id="06f6c-561">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="06f6c-562">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="06f6c-562">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="06f6c-563">将 ADF.Net SDK 版本更新到了 0.8.0-preview，其中包含以下更改：</span><span class="sxs-lookup"><span data-stu-id="06f6c-563">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="06f6c-564">增加了“配置工厂存储库”操作</span><span class="sxs-lookup"><span data-stu-id="06f6c-564">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="06f6c-565">更新了 QuickBooks LinkedService，可以公开 consumerKey 和 consumerSecret 属性</span><span class="sxs-lookup"><span data-stu-id="06f6c-565">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="06f6c-566">已将多个模型类型从 SecretBase 更新为 Object</span><span class="sxs-lookup"><span data-stu-id="06f6c-566">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="06f6c-567">增加了 Blob 事件触发器</span><span class="sxs-lookup"><span data-stu-id="06f6c-567">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="06f6c-568">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="06f6c-568">AzureRM.KeyVault</span></span>
* <span data-ttu-id="06f6c-569">使用示例输出更新了文档</span><span class="sxs-lookup"><span data-stu-id="06f6c-569">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="06f6c-570">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="06f6c-570">AzureRM.Network</span></span>
* <span data-ttu-id="06f6c-571">在网络观察程序 cmdlet 上启用了流量分析参数</span><span class="sxs-lookup"><span data-stu-id="06f6c-571">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="06f6c-572">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="06f6c-572">AzureRM.Resources</span></span>
* <span data-ttu-id="06f6c-573">修复了从“Get-AzureRmResource”返回的“PSResource”对象的“Properties”属性问题</span><span class="sxs-lookup"><span data-stu-id="06f6c-573">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="06f6c-574">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="06f6c-574">AzureRM.Scheduler</span></span>
* <span data-ttu-id="06f6c-575">修复了更新 ServiceBusQueueJob 无法设置新 Auth 值的问题</span><span class="sxs-lookup"><span data-stu-id="06f6c-575">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="06f6c-576">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="06f6c-576">AzureRM.Sql</span></span>
* <span data-ttu-id="06f6c-577">使用可选的 LicenseType 参数更新了以下 cmdlet</span><span class="sxs-lookup"><span data-stu-id="06f6c-577">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="06f6c-578">New-AzureRmSqlDatabase；Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="06f6c-578">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="06f6c-579">New-AzureRmSqlElasticPool；Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="06f6c-579">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="06f6c-580">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="06f6c-580">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="06f6c-581">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="06f6c-581">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="06f6c-582">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="06f6c-582">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="06f6c-583">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="06f6c-583">AzureRM.Websites</span></span>
* <span data-ttu-id="06f6c-584">更新了“New-AzureRMWebApp”，可以使用策略库中的常用算法。</span><span class="sxs-lookup"><span data-stu-id="06f6c-584">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="06f6c-585">6.1.0 - 2018 年 5 月</span><span class="sxs-lookup"><span data-stu-id="06f6c-585">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="06f6c-586">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="06f6c-586">AzureRM.Profile</span></span>
* <span data-ttu-id="06f6c-587">修复了运行“Clear-AzureRmContext”时会保留空上下文的问题，该上下文使用旧的默认上下文的名称，导致用户无法使用旧名称创建新的上下文</span><span class="sxs-lookup"><span data-stu-id="06f6c-587">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="06f6c-588">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="06f6c-588">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="06f6c-589">允许在 AS 上执行网关的关联/取消关联操作。</span><span class="sxs-lookup"><span data-stu-id="06f6c-589">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="06f6c-590">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="06f6c-590">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="06f6c-591">增加了对 ApiVersions、ApiReleases 和 ApiRevisions 的支持</span><span class="sxs-lookup"><span data-stu-id="06f6c-591">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="06f6c-592">增加了对 ServiceFabric 后端的支持</span><span class="sxs-lookup"><span data-stu-id="06f6c-592">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="06f6c-593">增加了对 Application Insights Logger 的支持</span><span class="sxs-lookup"><span data-stu-id="06f6c-593">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="06f6c-594">增加的支持包括认可“基本”SKU 是 API 管理服务的有效 SKU</span><span class="sxs-lookup"><span data-stu-id="06f6c-594">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="06f6c-595">增加的支持包括允许将专用 CA 颁发的证书作为根证书或 CA 证书安装</span><span class="sxs-lookup"><span data-stu-id="06f6c-595">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="06f6c-596">增加的支持包括通过 KeyVault 和多个代理主机名接受自定义 SSL 证书</span><span class="sxs-lookup"><span data-stu-id="06f6c-596">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="06f6c-597">增加了对 MSI 标识的支持</span><span class="sxs-lookup"><span data-stu-id="06f6c-597">Added support for MSI identity</span></span>
* <span data-ttu-id="06f6c-598">增加的支持包括通过 URL 接受策略 注意：以下 cmdlet 将在未来版本中弃用</span><span class="sxs-lookup"><span data-stu-id="06f6c-598">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="06f6c-599">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="06f6c-599">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="06f6c-600">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="06f6c-600">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="06f6c-601">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="06f6c-601">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="06f6c-602">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="06f6c-602">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="06f6c-603">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="06f6c-603">AzureRM.Batch</span></span>
* <span data-ttu-id="06f6c-604">发布新 cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="06f6c-604">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="06f6c-605">发布新 cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="06f6c-605">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="06f6c-606">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="06f6c-606">AzureRM.Consumption</span></span>
* <span data-ttu-id="06f6c-607">在 Cmdlet Get-AzureRmConsumptionUsageDetail 中增加了新参数 Expand、ResourceGroup、InstanceName、InstanceId、Tags、Top</span><span class="sxs-lookup"><span data-stu-id="06f6c-607">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="06f6c-608">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="06f6c-608">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="06f6c-609">修复了 Export-AzureRmDataLakeStoreChildItemProperties 的示例</span><span class="sxs-lookup"><span data-stu-id="06f6c-609">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="06f6c-610">修复了 Set-AzureRmDataLakeStoreItemAclEntry 中 Recurse 用例的 null 参数异常</span><span class="sxs-lookup"><span data-stu-id="06f6c-610">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="06f6c-611">修复了 Set-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAcl、Remove-AzureRmDataLakeStoreItemAclEntry 的帮助文件</span><span class="sxs-lookup"><span data-stu-id="06f6c-611">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="06f6c-612">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="06f6c-612">AzureRM.Network</span></span>
* <span data-ttu-id="06f6c-613">将网络 SDK 版本从 18.0.0-preview 升至 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="06f6c-613">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="06f6c-614">增加了用于创建协议配置的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="06f6c-614">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="06f6c-615">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="06f6c-615">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="06f6c-616">增加了用于向现有的快速路由线路添加新的线路连接的 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="06f6c-616">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="06f6c-617">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="06f6c-617">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="06f6c-618">增加了用于从现有的快速路由线路删除线路连接的 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="06f6c-618">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="06f6c-619">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="06f6c-619">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="06f6c-620">增加了用于检索线路连接的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="06f6c-620">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="06f6c-621">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="06f6c-621">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="06f6c-622">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="06f6c-622">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="06f6c-623">修复了使用生成的证书进行服务器身份验证的问题（问题 5998）</span><span class="sxs-lookup"><span data-stu-id="06f6c-623">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="06f6c-624">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="06f6c-624">AzureRM.Sql</span></span>
* <span data-ttu-id="06f6c-625">更新了审核 cmdlet，允许删除 AuditActions 或 AuditActionGroups</span><span class="sxs-lookup"><span data-stu-id="06f6c-625">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="06f6c-626">修复了设置新的灵活保留策略时使用 Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy 出现的问题。该问题的具体表现是：在命令失败的同时，出现“不再支持使用 Azure 恢复服务保管库和策略配置长期保留策略。</span><span class="sxs-lookup"><span data-stu-id="06f6c-626">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="06f6c-627">请使用新的灵活保留策略提交请求”错误消息。</span><span class="sxs-lookup"><span data-stu-id="06f6c-627">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="06f6c-628">更新了与 Azure SQL 数据库/ElasticPool 的创建/更新相关的所有 cmdlet，允许使用新的数据库 API，而这些 cmdlet 支持的 SKU 属性则适用于规模和层相关属性。</span><span class="sxs-lookup"><span data-stu-id="06f6c-628">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="06f6c-629">更新的 cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="06f6c-629">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="06f6c-630">New-AzureRmSqlDatabase；Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="06f6c-630">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="06f6c-631">New-AzureRmSqlElasticPool；Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="06f6c-631">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="06f6c-632">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="06f6c-632">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="06f6c-633">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="06f6c-633">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="06f6c-634">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="06f6c-634">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="06f6c-635">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="06f6c-635">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="06f6c-636">更新了“Get-AzureRmTrafficManagerProfile”的参数，要求在使用 -Name 参数时使用 -ResourceGroupName 参数。</span><span class="sxs-lookup"><span data-stu-id="06f6c-636">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
