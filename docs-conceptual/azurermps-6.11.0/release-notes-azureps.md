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
ms.openlocfilehash: eec8b5960f787fa9ca1130b4f8b49c9d896aa99e
ms.sourcegitcommit: 1f699b72bf544d92459da9d888cc0091f9415b65
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/06/2018
ms.locfileid: "50971969"
---
# <a name="release-notes"></a><span data-ttu-id="1d563-103">发行说明</span><span class="sxs-lookup"><span data-stu-id="1d563-103">Release notes</span></span>

<span data-ttu-id="1d563-104">下面是此版本中对 Azure PowerShell 所做的更改列表。</span><span class="sxs-lookup"><span data-stu-id="1d563-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="6110---october-2018"></a><span data-ttu-id="1d563-105">6.11.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="1d563-105">6.11.0 - October 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="1d563-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="1d563-106">AzureRM.Profile</span></span>
* <span data-ttu-id="1d563-107">修复了 CloudShell 中 Get-AzureRmSubscription 的问题</span><span class="sxs-lookup"><span data-stu-id="1d563-107">Fix issue with Get-AzureRmSubscription in CloudShell</span></span>
* <span data-ttu-id="1d563-108">更新通用代码以使用最新版本的 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="1d563-108">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="1d563-109">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="1d563-109">AzureRM.Backup</span></span>
* <span data-ttu-id="1d563-110">已弃用 Azure 备份 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1d563-110">Deprecated Azure Backup cmdlets.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="1d563-111">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="1d563-111">AzureRM.Compute</span></span>
* <span data-ttu-id="1d563-112">向 VM 大小的允许列表添加了新的大小，这样就可以在将简单的参数集用于“New-AzureRmVm”时为这些大小启用加速网络</span><span class="sxs-lookup"><span data-stu-id="1d563-112">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzureRmVm'</span></span>
* <span data-ttu-id="1d563-113">向所有 cmdlet 添加了 ResourceName 参数补全选项。</span><span class="sxs-lookup"><span data-stu-id="1d563-113">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="1d563-114">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1d563-114">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="1d563-115">添加虚拟网络规则的支持</span><span class="sxs-lookup"><span data-stu-id="1d563-115">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="1d563-116">Get-AzureRmDataLakeStoreVirtualNetworkRule：获取或列出 Azure Data Lake Store 虚拟网络规则。</span><span class="sxs-lookup"><span data-stu-id="1d563-116">Get-AzureRmDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="1d563-117">Add-AzureRmDataLakeStoreVirtualNetworkRule：向指定的 Data Lake Store 帐户添加虚拟网络规则。</span><span class="sxs-lookup"><span data-stu-id="1d563-117">Add-AzureRmDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="1d563-118">Set-AzureRmDataLakeStoreVirtualNetworkRule：在指定的 Data Lake Store 帐户中修改指定的虚拟网络规则。</span><span class="sxs-lookup"><span data-stu-id="1d563-118">Set-AzureRmDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="1d563-119">Remove-AzureRmDataLakeStoreVirtualNetworkRule：删除 Azure Data Lake Store 虚拟网络规则。</span><span class="sxs-lookup"><span data-stu-id="1d563-119">Remove-AzureRmDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="1d563-120">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="1d563-120">AzureRM.Network</span></span>
* <span data-ttu-id="1d563-121">更新 cmdlet Test-AzureRmNetworkWatcherConnectivity，向后端传递协议值。</span><span class="sxs-lookup"><span data-stu-id="1d563-121">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="1d563-122">向所有 cmdlet 添加了 ResourceName 参数补全选项。</span><span class="sxs-lookup"><span data-stu-id="1d563-122">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="1d563-123">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="1d563-123">AzureRM.Resources</span></span>
* <span data-ttu-id="1d563-124">通过在方案中添加一个有意义的异常，修复了 Get-AzureRMRoleDefinition 在默认配置文件中没有订阅且未指定范围的情况下引发难以理解异常的问题。</span><span class="sxs-lookup"><span data-stu-id="1d563-124">Fix isssue where Get-AzureRMRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="1d563-125">另外，已将默认参数集设置为“RoleDefinitionNameParameterSet”。</span><span class="sxs-lookup"><span data-stu-id="1d563-125">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="6100---october-2018"></a><span data-ttu-id="1d563-126">6.10.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="1d563-126">6.10.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="1d563-127">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="1d563-127">Azure.Storage</span></span>
* <span data-ttu-id="1d563-128">修复了 Copy Blob/File 在目标有元数据问题时不会复制元数据的问题</span><span class="sxs-lookup"><span data-stu-id="1d563-128">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="1d563-129">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="1d563-129">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="1d563-130">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="1d563-130">Start-AzureStorageFileCopy</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="1d563-131">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="1d563-131">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="1d563-132">在没有现有帐户的情况下支持 Get-AzureRmCognitiveServicesAccountSkus。</span><span class="sxs-lookup"><span data-stu-id="1d563-132">Support Get-AzureRmCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="1d563-133">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="1d563-133">AzureRM.Compute</span></span>
* <span data-ttu-id="1d563-134">修复了 Get-AzureRmVM -ResourceGroupName <rg>，以在需要时返回超过 50 个结果</span><span class="sxs-lookup"><span data-stu-id="1d563-134">Fix Get-AzureRmVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="1d563-135">在 New-AzureRmVmss cmdlet 帮助中添加了“SimpleParameterSet”的示例。</span><span class="sxs-lookup"><span data-stu-id="1d563-135">Added an example of the 'SimpleParameterSet' to New-AzureRmVmss cmdlet help.</span></span>
* <span data-ttu-id="1d563-136">修复了 Azure 磁盘加密进度消息中的拼写错误</span><span class="sxs-lookup"><span data-stu-id="1d563-136">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="1d563-137">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="1d563-137">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="1d563-138">将 ADF .Net SDK 版本更新为 2.3.0。</span><span class="sxs-lookup"><span data-stu-id="1d563-138">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="1d563-139">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="1d563-139">AzureRM.Network</span></span>
* <span data-ttu-id="1d563-140">添加了 NetworkProfile 功能。</span><span class="sxs-lookup"><span data-stu-id="1d563-140">Added NetworkProfile functionality.</span></span> <span data-ttu-id="1d563-141">添加了新 cmdlet</span><span class="sxs-lookup"><span data-stu-id="1d563-141">new cmdlets added</span></span>
    - <span data-ttu-id="1d563-142">Get-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="1d563-142">Get-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="1d563-143">New-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="1d563-143">New-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="1d563-144">Remove-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="1d563-144">Remove-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="1d563-145">Set-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="1d563-145">Set-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="1d563-146">New-AzureRMContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="1d563-146">New-AzureRMContainerNicConfig</span></span>
    - <span data-ttu-id="1d563-147">New-AzureRmContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="1d563-147">New-AzureRmContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="1d563-148">在子网模型上添加了服务关联链接</span><span class="sxs-lookup"><span data-stu-id="1d563-148">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="1d563-149">添加了 cmdlet New-AzureRmVirtualNetworkTap、Get-AzureRmVirtualNetworkTap、Set-AzureRmVirtualNetworkTap、Remove-AzureRmVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="1d563-149">Added cmdlet New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap</span></span>
* <span data-ttu-id="1d563-150">添加了 cmdlet Set-AzureRmNEtworkInterfaceTapConfig、Get-AzureRmNEtworkInterfaceTapConfig、Remove-AzureRmNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="1d563-150">Added cmdlet Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="1d563-151">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="1d563-151">AzureRM.RedisCache</span></span>
* <span data-ttu-id="1d563-152">今后允许任何字符串作为 Size 参数。</span><span class="sxs-lookup"><span data-stu-id="1d563-152">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="1d563-153">在 PSArgumentCompleter 弹出窗口中添加了 P5</span><span class="sxs-lookup"><span data-stu-id="1d563-153">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="1d563-154">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="1d563-154">AzureRM.Resources</span></span>
* <span data-ttu-id="1d563-155">将缺少的 -Mode 参数添加到 Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1d563-155">Add missing -Mode parameter to Set-AzureRmPolicyDefinition</span></span>
* <span data-ttu-id="1d563-156">对于使用包含用户的源的操作，修复了 Get-AzureRmProviderOperation commandlet bug</span><span class="sxs-lookup"><span data-stu-id="1d563-156">Fix Get-AzureRmProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="1d563-157">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="1d563-157">AzureRM.Sql</span></span>
* <span data-ttu-id="1d563-158">修复了某些备份 cmdlet 无法识别当前 azure 订阅的问题</span><span class="sxs-lookup"><span data-stu-id="1d563-158">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="1d563-159">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="1d563-159">AzureRM.Storage</span></span>
* <span data-ttu-id="1d563-160">支持获取特定位置的存储资源使用情况，并对于获取的全局存储资源使用情况已过时添加警告消息。</span><span class="sxs-lookup"><span data-stu-id="1d563-160">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="1d563-161">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="1d563-161">Get-AzureRmStorageUsage</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="1d563-162">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="1d563-162">AzureRM.Websites</span></span>
* <span data-ttu-id="1d563-163">新 Cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl - 获取容器持续部署 Webhook URL</span><span class="sxs-lookup"><span data-stu-id="1d563-163">New Cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="1d563-164">新 Cmdlet New-AzureRMWebAppContainerPSSession 和 Enter-WebAppContainerPSSession - 在 Windows 容器应用中启动 PowerShell 远程会话</span><span class="sxs-lookup"><span data-stu-id="1d563-164">New Cmdlets New-AzureRMWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="690---september-2018"></a><span data-ttu-id="1d563-165">6.9.0 - 2018 年 9 月</span><span class="sxs-lookup"><span data-stu-id="1d563-165">6.9.0 - September 2018</span></span>
#### <a name="general"></a><span data-ttu-id="1d563-166">常规</span><span class="sxs-lookup"><span data-stu-id="1d563-166">General</span></span>
* <span data-ttu-id="1d563-167">AzureRM.SignalR 已添加到 AzureRM 汇总模块</span><span class="sxs-lookup"><span data-stu-id="1d563-167">AzureRM.SignalR was added to the AzureRM rollup module</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="1d563-168">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="1d563-168">AzureRM.Profile</span></span>
* <span data-ttu-id="1d563-169">对存储常用代码进行了细微的更改</span><span class="sxs-lookup"><span data-stu-id="1d563-169">Minor changes to the storage common code</span></span>
* <span data-ttu-id="1d563-170">更新了帮助文件，使之包括完整参数类型。</span><span class="sxs-lookup"><span data-stu-id="1d563-170">Updated help files to include full parameter types.</span></span>
- <span data-ttu-id="1d563-171">已在 ServicePrincipalCertificateWithSubscriptionId 参数集中将 -ServicePrincipal 更改为非强制性项</span><span class="sxs-lookup"><span data-stu-id="1d563-171">Changed -ServicePrincipal to non-mandatory in the ServicePrincipalCertificateWithSubscriptionId parameter set</span></span> 

#### <a name="azurestorage"></a><span data-ttu-id="1d563-172">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="1d563-172">Azure.Storage</span></span>
* <span data-ttu-id="1d563-173">支持使用 OAuth 创建存储上下文。</span><span class="sxs-lookup"><span data-stu-id="1d563-173">Support create Storage Context with OAuth.</span></span> 
    - <span data-ttu-id="1d563-174">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="1d563-174">New-AzureStorageContext</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="1d563-175">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="1d563-175">AzureRM.Cdn</span></span>
* <span data-ttu-id="1d563-176">在 Cdn 定价 sku 中增加了 Standard_Microsoft。</span><span class="sxs-lookup"><span data-stu-id="1d563-176">Added Standard_Microsoft in Cdn pricing sku.</span></span> 

#### <a name="azurermcompute"></a><span data-ttu-id="1d563-177">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="1d563-177">AzureRM.Compute</span></span>
* <span data-ttu-id="1d563-178">将 Keyvault 和存储的依赖项移到了常用依赖项中</span><span class="sxs-lookup"><span data-stu-id="1d563-178">Move dependencies on Keyvault and Storage to the common dependencies</span></span>
* <span data-ttu-id="1d563-179">增加了对 AEM cmdlet 的支持，可以使用更多的虚拟机大小</span><span class="sxs-lookup"><span data-stu-id="1d563-179">Add support for more virutal machine sizes to AEM cmdlets</span></span>
* <span data-ttu-id="1d563-180">为 New-AzureRmVmssIpConfig 增加了 PublicIPPrefix 参数</span><span class="sxs-lookup"><span data-stu-id="1d563-180">Add PublicIPPrefix parameter to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="1d563-181">为 Invoke-AzureRmVMRunCommand cmdelt 增加了 ResourceId 参数</span><span class="sxs-lookup"><span data-stu-id="1d563-181">Add ResourceId parameter to Invoke-AzureRmVMRunCommand cmdelt</span></span>
* <span data-ttu-id="1d563-182">增加了 Invoke-AzureRmVmssVMRunCommand cmdlet</span><span class="sxs-lookup"><span data-stu-id="1d563-182">Add Invoke-AzureRmVmssVMRunCommand cmdlet</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="1d563-183">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="1d563-183">AzureRM.Dns</span></span>
* <span data-ttu-id="1d563-184">增加了在创建 dns 记录期间对别名记录的支持</span><span class="sxs-lookup"><span data-stu-id="1d563-184">Added support for alias record during dns record creation</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="1d563-185">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="1d563-185">AzureRM.Insights</span></span>
* <span data-ttu-id="1d563-186">修复了问题 #6833 和 #7102（诊断设置方面）</span><span class="sxs-lookup"><span data-stu-id="1d563-186">Fixed issues #6833 and #7102 (Diagnostic Settings area)</span></span>
    - <span data-ttu-id="1d563-187">在创建和列出/获取诊断设置期间出现的默认名称（即“service”）的问题</span><span class="sxs-lookup"><span data-stu-id="1d563-187">Issues with the default name, i.e. 'service', during creation and listing/getting of diagnostic settings</span></span>
    - <span data-ttu-id="1d563-188">通过类别创建诊断设置的问题</span><span class="sxs-lookup"><span data-stu-id="1d563-188">Issues creating diagnostic settings with categories</span></span>
* <span data-ttu-id="1d563-189">为指标时间粒度参数添加了弃用消息</span><span class="sxs-lookup"><span data-stu-id="1d563-189">Added deprecation message for metrics time grains parameters</span></span>
    - <span data-ttu-id="1d563-190">Timegrains 参数仍然会被接受（这是非重大变更），但在后端会被忽略，因为仅 PT1M 有效</span><span class="sxs-lookup"><span data-stu-id="1d563-190">Timegrains parameters are still being accepted (this is a non-breaking change,) but they are ignored in the backend since only PT1M is valid</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="1d563-191">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="1d563-191">AzureRM.Network</span></span>
* <span data-ttu-id="1d563-192">更改了 LoadBalancer cmdlet</span><span class="sxs-lookup"><span data-stu-id="1d563-192">Changes to LoadBalancer cmdlets</span></span>
  - <span data-ttu-id="1d563-193">LoadBalancerInboundNatPoolConfig：增加了 IdleTimeoutInMinutes、EnableFloatingIp 和 EnableTcpReset 参数</span><span class="sxs-lookup"><span data-stu-id="1d563-193">LoadBalancerInboundNatPoolConfig: added parameters IdleTimeoutInMinutes, EnableFloatingIp and EnableTcpReset</span></span>
  - <span data-ttu-id="1d563-194">LoadBalancerInboundNatRuleConfig：增加了 EnableTcpReset 参数</span><span class="sxs-lookup"><span data-stu-id="1d563-194">LoadBalancerInboundNatRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="1d563-195">LoadBalancerRuleConfig：增加了 EnableTcpReset 参数</span><span class="sxs-lookup"><span data-stu-id="1d563-195">LoadBalancerRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="1d563-196">LoadBalancerProbeConfig：增加了对参数 Protocol 的“Https”值的支持</span><span class="sxs-lookup"><span data-stu-id="1d563-196">LoadBalancerProbeConfig: added support for value "Https" for parameter Protocol</span></span>
* <span data-ttu-id="1d563-197">为新 LoadBalancer 的子资源 OutboundRule 增加了新命令</span><span class="sxs-lookup"><span data-stu-id="1d563-197">Added new commands for new LoadBalancer's subresource OutboundRule</span></span>
  - <span data-ttu-id="1d563-198">Add-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1d563-198">Add-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="1d563-199">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1d563-199">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="1d563-200">New-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1d563-200">New-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="1d563-201">Set-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1d563-201">Set-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="1d563-202">Remove-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1d563-202">Remove-AzureRmLoadBalancerOutboundRuleConfig</span></span>
* <span data-ttu-id="1d563-203">为 PSNetworkInterface 增加了新的 HostedWorkloads 属性</span><span class="sxs-lookup"><span data-stu-id="1d563-203">Added new HostedWorkloads property for PSNetworkInterface</span></span>
* <span data-ttu-id="1d563-204">通过 ARM 为 Azure 防火墙功能增加了新的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="1d563-204">Added new cmdlets for feature: Azure Firewall via ARM</span></span>
  - <span data-ttu-id="1d563-205">增加了 Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="1d563-205">Added Get-AzureRmFirewall</span></span>
  - <span data-ttu-id="1d563-206">增加了 Set-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="1d563-206">Added Set-AzureRmFirewall</span></span>
  - <span data-ttu-id="1d563-207">增加了 New-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="1d563-207">Added New-AzureRmFirewall</span></span>
  - <span data-ttu-id="1d563-208">增加了 Remove-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="1d563-208">Added Remove-AzureRmFirewall</span></span>
  - <span data-ttu-id="1d563-209">增加了 New-AzureRmFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="1d563-209">Added New-AzureRmFirewallApplicationRuleCollection</span></span>
  - <span data-ttu-id="1d563-210">增加了 New-AzureRmFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="1d563-210">Added New-AzureRmFirewallApplicationRule</span></span>
  - <span data-ttu-id="1d563-211">增加了 New-AzureRmFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="1d563-211">Added New-AzureRmFirewallNatRuleCollection</span></span>
  - <span data-ttu-id="1d563-212">增加了 New-AzureRmFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="1d563-212">Added New-AzureRmFirewallNatRule</span></span>
  - <span data-ttu-id="1d563-213">增加了 New-AzureRmFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="1d563-213">Added New-AzureRmFirewallNetworkRuleCollection</span></span>
  - <span data-ttu-id="1d563-214">增加了 New-AzureRmFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="1d563-214">Added New-AzureRmFirewallNetworkRule</span></span>
* <span data-ttu-id="1d563-215">在应用程序网关中增加了对受信任根证书和自动缩放配置的支持</span><span class="sxs-lookup"><span data-stu-id="1d563-215">Added support for Trusted Root certificate and Autoscale configuration in Application Gateway</span></span>
  - <span data-ttu-id="1d563-216">增加了新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="1d563-216">New Cmdlets added:</span></span>
      - <span data-ttu-id="1d563-217">Add-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="1d563-217">Add-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="1d563-218">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="1d563-218">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="1d563-219">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="1d563-219">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="1d563-220">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="1d563-220">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="1d563-221">Set-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="1d563-221">Set-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="1d563-222">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="1d563-222">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="1d563-223">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="1d563-223">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="1d563-224">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="1d563-224">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="1d563-225">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="1d563-225">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
  - <span data-ttu-id="1d563-226">使用可选参数 -TrustedRootCertificate 更新了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1d563-226">Cmdlets updated with optonal parameter -TrustedRootCertificate</span></span>
      - <span data-ttu-id="1d563-227">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1d563-227">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="1d563-228">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1d563-228">Set-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="1d563-229">New-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="1d563-229">New-AzureRmApplicationGatewayBackendHttpSetting</span></span>
      - <span data-ttu-id="1d563-230">Set-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="1d563-230">Set-AzureRmApplicationGatewayBackendHttpSetting</span></span>
  - <span data-ttu-id="1d563-231">使用可选参数 -AutoscaleConfiguration 更新了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1d563-231">Cmdlets updated with optonal parameter -AutoscaleConfiguration</span></span>
      - <span data-ttu-id="1d563-232">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1d563-232">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="1d563-233">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1d563-233">Set-AzureRmApplicationGateway</span></span>
* <span data-ttu-id="1d563-234">为接口终结点增加了 cmdlet Get-AzureInterfaceEndpoint</span><span class="sxs-lookup"><span data-stu-id="1d563-234">Add cmdlet for Interface Endpoint Get-AzureInterfaceEndpoint</span></span>
* <span data-ttu-id="1d563-235">在子网中增加了对多个地址前缀的支持。</span><span class="sxs-lookup"><span data-stu-id="1d563-235">Added support for multiple address prefixes in a subnet.</span></span> <span data-ttu-id="1d563-236">更新了 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="1d563-236">Updated cmdlets:</span></span>
  - <span data-ttu-id="1d563-237">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="1d563-237">New-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="1d563-238">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="1d563-238">Set-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="1d563-239">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="1d563-239">Add-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="1d563-240">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="1d563-240">Get-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="1d563-241">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="1d563-241">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>
  - <span data-ttu-id="1d563-242">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="1d563-242">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="1d563-243">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="1d563-243">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="1d563-244">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="1d563-244">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="1d563-245">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="1d563-245">Add-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="1d563-246">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="1d563-246">New-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="1d563-247">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="1d563-247">Set-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="1d563-248">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="1d563-248">Add-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="1d563-249">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="1d563-249">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="1d563-250">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="1d563-250">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="1d563-251">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="1d563-251">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="1d563-252">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="1d563-252">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="1d563-253">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="1d563-253">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="1d563-254">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="1d563-254">New-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="1d563-255">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="1d563-255">New-AzureRmNetworkInterface</span></span>
* <span data-ttu-id="1d563-256">增加了用于子网委派的 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1d563-256">Adding cmdlets for subnet delegation.</span></span>
  - <span data-ttu-id="1d563-257">New-AzureRmDelegation：创建一个可以添加到子网的新委派</span><span class="sxs-lookup"><span data-stu-id="1d563-257">New-AzureRmDelegation: Creates a new delegation, which can be added to a subnet</span></span>
  - <span data-ttu-id="1d563-258">Remove-AzureRmDelegation：获取一个子网，然后从该子网中删除提供的委派名称</span><span class="sxs-lookup"><span data-stu-id="1d563-258">Remove-AzureRmDelegation: Takes in a subnet and removes the provided delegation name from that subnet</span></span>
  - <span data-ttu-id="1d563-259">Add-AzureRmDelegation：获取一个子网，然后向该子网添加提供的服务名称作为委派</span><span class="sxs-lookup"><span data-stu-id="1d563-259">Add-AzureRmDelegation: Takes in a subnet and adds the provided service name as a delegation to that subnet</span></span>
  - <span data-ttu-id="1d563-260">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="1d563-260">Get-AzureRmDelegation</span></span>
  - <span data-ttu-id="1d563-261">Get-AzureRmAvailableServiceDelegations</span><span class="sxs-lookup"><span data-stu-id="1d563-261">Get-AzureRmAvailableServiceDelegations</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="1d563-262">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="1d563-262">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="1d563-263">支持托管磁盘</span><span class="sxs-lookup"><span data-stu-id="1d563-263">Support for managed Managed disk</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="1d563-264">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="1d563-264">AzureRM.RedisCache</span></span>
* <span data-ttu-id="1d563-265">更新了 Insights 依赖项。</span><span class="sxs-lookup"><span data-stu-id="1d563-265">Updated Insights dependency.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="1d563-266">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="1d563-266">AzureRM.Resources</span></span>
* <span data-ttu-id="1d563-267">使用新参数 RollbackAction 更新了 New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="1d563-267">Update New-AzureRmResourceGroupDeployment with new parameter RollbackAction</span></span>
    - <span data-ttu-id="1d563-268">使用新参数增加了对 OnErrorDeployment 的支持。</span><span class="sxs-lookup"><span data-stu-id="1d563-268">Add support for OnErrorDeployment with the new parameter.</span></span>
* <span data-ttu-id="1d563-269">在策略分配方面支持托管标识。</span><span class="sxs-lookup"><span data-stu-id="1d563-269">Support managed identity on policy assignments.</span></span>
* <span data-ttu-id="1d563-270">使用“New-AzureRmPolicyAssignment”来分配策略时，不再需要带默认值的参数</span><span class="sxs-lookup"><span data-stu-id="1d563-270">Parameters with default values are no longer requred when assigning a policy with 'New-AzureRmPolicyAssignment'</span></span>
* <span data-ttu-id="1d563-271">增加了新的 cmdlet Get-AzureRmPolicyAlias，用于检索策略别名</span><span class="sxs-lookup"><span data-stu-id="1d563-271">Add new cmdlet Get-AzureRmPolicyAlias for retrieving policy aliases</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="1d563-272">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="1d563-272">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="1d563-273">修复了问题 #7161</span><span class="sxs-lookup"><span data-stu-id="1d563-273">Fixed issue #7161</span></span>

#### <a name="azurermsignalr"></a><span data-ttu-id="1d563-274">AzureRM.SignalR</span><span class="sxs-lookup"><span data-stu-id="1d563-274">AzureRM.SignalR</span></span>
* <span data-ttu-id="1d563-275">将 SKU 名称更新为 Free_F1 和 Standard_S1</span><span class="sxs-lookup"><span data-stu-id="1d563-275">Update SKU names to Free_F1 and Standard_S1</span></span>
* <span data-ttu-id="1d563-276">为 PSSignalRResource 对象增加了版本字段，为 PSSignalRKeys 对象增加了字符串。</span><span class="sxs-lookup"><span data-stu-id="1d563-276">Add version field to the PSSignalRResource object and connection string to the PSSignalRKeys object.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="1d563-277">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="1d563-277">AzureRM.Storage</span></span>
* <span data-ttu-id="1d563-278">在 AzureRm.Storage 中支持不可变性策略</span><span class="sxs-lookup"><span data-stu-id="1d563-278">Support Immutability Policy in AzureRm.Storage</span></span> 
    - <span data-ttu-id="1d563-279">Remove-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="1d563-279">Remove-AzureRmStorageAccountNetworkRule</span></span>
    - <span data-ttu-id="1d563-280">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="1d563-280">Get-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="1d563-281">Update-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="1d563-281">Update-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="1d563-282">New-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="1d563-282">New-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="1d563-283">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="1d563-283">Remove-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="1d563-284">Add-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="1d563-284">Add-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="1d563-285">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="1d563-285">Remove-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="1d563-286">Set-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="1d563-286">Set-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="1d563-287">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="1d563-287">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="1d563-288">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="1d563-288">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="1d563-289">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="1d563-289">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="1d563-290">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="1d563-290">AzureRM.Websites</span></span>
* <span data-ttu-id="1d563-291">增加了两个新的 cmdlet：Get-AzureRmDeletedWebApp 和 Restore-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="1d563-291">Added two new cmdlets: Get-AzureRmDeletedWebApp and Restore-AzureRmDeletedWebApp</span></span>
* <span data-ttu-id="1d563-292">增加了 New-AzureRmAppServicePlan -HyperV 开关，用于通过 Windows 容器创建应用服务计划</span><span class="sxs-lookup"><span data-stu-id="1d563-292">New-AzureRmAppServicePlan -HyperV switch is added for create app service plan with windows container</span></span>
* <span data-ttu-id="1d563-293">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - 增加了新参数 (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment)，用于创建和管理 Windows 容器应用</span><span class="sxs-lookup"><span data-stu-id="1d563-293">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - New parameters (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) added for creating and managing windows container app</span></span>

## <a name="681---august-2018"></a><span data-ttu-id="1d563-294">6.8.1 - 2018 年 8 月</span><span class="sxs-lookup"><span data-stu-id="1d563-294">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="1d563-295">常规</span><span class="sxs-lookup"><span data-stu-id="1d563-295">General</span></span>
* <span data-ttu-id="1d563-296">解决了未设置默认资源组的问题。</span><span class="sxs-lookup"><span data-stu-id="1d563-296">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="1d563-297">更新了公共运行时程序集</span><span class="sxs-lookup"><span data-stu-id="1d563-297">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="1d563-298">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="1d563-298">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="1d563-299">解决了未设置默认资源组的问题。</span><span class="sxs-lookup"><span data-stu-id="1d563-299">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="1d563-300">修复了问题 https://github.com/Azure/azure-powershell/issues/6603</span><span class="sxs-lookup"><span data-stu-id="1d563-300">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="1d563-301">Import-AzureRmApiManagementApi 和 \*-AzureRmApiManagementCertificate cmdlet 现在处理相对路径</span><span class="sxs-lookup"><span data-stu-id="1d563-301">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="1d563-302">修复了问题 https://github.com/Azure/azure-powershell/issues/6879</span><span class="sxs-lookup"><span data-stu-id="1d563-302">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="1d563-303">CertificateInformation 是使 Set-AzureRmApiManagement cmdlet 可以正常工作的可设置属性。</span><span class="sxs-lookup"><span data-stu-id="1d563-303">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="1d563-304">通过升级到 4.0.4-preview nuget 进行了修复</span><span class="sxs-lookup"><span data-stu-id="1d563-304">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="1d563-305">修复了问题 https://github.com/Azure/azure-powershell/issues/6853</span><span class="sxs-lookup"><span data-stu-id="1d563-305">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="1d563-306">针对按产品名称进行的搜索修复了 Odata 筛选器</span><span class="sxs-lookup"><span data-stu-id="1d563-306">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="1d563-307">修复了问题 https://github.com/Azure/azure-powershell/issues/6814</span><span class="sxs-lookup"><span data-stu-id="1d563-307">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="1d563-308">针对按 API 名称进行的搜索修复了 Odata 筛选器</span><span class="sxs-lookup"><span data-stu-id="1d563-308">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="1d563-309">添加了对 AzureMonitor 记录器的支持</span><span class="sxs-lookup"><span data-stu-id="1d563-309">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="1d563-310">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="1d563-310">AzureRM.Compute</span></span>
* <span data-ttu-id="1d563-311">解决了错误输出中缺少目标的问题。</span><span class="sxs-lookup"><span data-stu-id="1d563-311">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="1d563-312">解决了带有托管磁盘的 VM 的存储帐户类型问题</span><span class="sxs-lookup"><span data-stu-id="1d563-312">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="1d563-313">解决了未设置默认资源组的问题。</span><span class="sxs-lookup"><span data-stu-id="1d563-313">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="1d563-314">解决了在其他环境（例如 Azure 中国）中使用 AEM 扩展 cmdlet 的问题</span><span class="sxs-lookup"><span data-stu-id="1d563-314">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="1d563-315">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="1d563-315">AzureRM.Network</span></span>
* <span data-ttu-id="1d563-316">将默认 cmdlet 输出表示形式更改为表视图</span><span class="sxs-lookup"><span data-stu-id="1d563-316">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="1d563-317">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="1d563-317">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="1d563-318">修复了在尝试扩展停用的容量时 Update-AzureRmPowerBIEmbeddedCapacity 中出现的故障</span><span class="sxs-lookup"><span data-stu-id="1d563-318">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="1d563-319">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="1d563-319">AzureRM.Resources</span></span>
* <span data-ttu-id="1d563-320">解决了从市场创建托管应用程序的问题。</span><span class="sxs-lookup"><span data-stu-id="1d563-320">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="1d563-321">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="1d563-321">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="1d563-322">修复的问题</span><span class="sxs-lookup"><span data-stu-id="1d563-322">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="1d563-323">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="1d563-323">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="1d563-324">添加了对 MultiValue 路由方法的支持</span><span class="sxs-lookup"><span data-stu-id="1d563-324">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="1d563-325">MultiValue 路由的新参数“MaxReturn”</span><span class="sxs-lookup"><span data-stu-id="1d563-325">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="1d563-326">添加了对 Subnet 路由方法的支持</span><span class="sxs-lookup"><span data-stu-id="1d563-326">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="1d563-327">对终结点中的 IP 地址范围（子网）的支持</span><span class="sxs-lookup"><span data-stu-id="1d563-327">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="1d563-328">添加了对配置文件中的自定义标头的支持</span><span class="sxs-lookup"><span data-stu-id="1d563-328">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="1d563-329">添加了对配置文件中的预期状态代码范围的支持</span><span class="sxs-lookup"><span data-stu-id="1d563-329">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="1d563-330">添加了对终结点中的自定义标头的支持</span><span class="sxs-lookup"><span data-stu-id="1d563-330">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="1d563-331">6.8.0 - 2018 年 8 月</span><span class="sxs-lookup"><span data-stu-id="1d563-331">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="1d563-332">常规</span><span class="sxs-lookup"><span data-stu-id="1d563-332">General</span></span>
* <span data-ttu-id="1d563-333">解决了未设置默认资源组的问题。</span><span class="sxs-lookup"><span data-stu-id="1d563-333">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="1d563-334">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="1d563-334">AzureRM.Profile</span></span>
* <span data-ttu-id="1d563-335">为在执行 Connect-AzureRmAccount 期间返回的令牌添加了“过期”属性</span><span class="sxs-lookup"><span data-stu-id="1d563-335">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="1d563-336">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="1d563-336">AzureRM.Compute</span></span>
* <span data-ttu-id="1d563-337">解决了错误输出中缺少目标的问题。</span><span class="sxs-lookup"><span data-stu-id="1d563-337">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="1d563-338">解决了带有托管磁盘的 VM 的存储帐户类型问题</span><span class="sxs-lookup"><span data-stu-id="1d563-338">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="1d563-339">解决了在其他环境（例如 Azure 中国）中使用 AEM 扩展 cmdlet 的问题</span><span class="sxs-lookup"><span data-stu-id="1d563-339">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="1d563-340">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="1d563-340">AzureRM.IotHub</span></span>
* <span data-ttu-id="1d563-341">修复了 New-AzureRmIotHubExportDevices 和 New-AzureRmIotHubImportDevices的示例</span><span class="sxs-lookup"><span data-stu-id="1d563-341">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="1d563-342">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="1d563-342">AzureRM.Network</span></span>
* <span data-ttu-id="1d563-343">将默认模型表示形式更改为表视图</span><span class="sxs-lookup"><span data-stu-id="1d563-343">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="1d563-344">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="1d563-344">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="1d563-345">修复了在尝试扩展停用的容量时 Update-AzureRmPowerBIEmbeddedCapacity 中出现的故障</span><span class="sxs-lookup"><span data-stu-id="1d563-345">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="1d563-346">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="1d563-346">AzureRM.Resources</span></span>
* <span data-ttu-id="1d563-347">解决了从市场创建托管应用程序的问题。</span><span class="sxs-lookup"><span data-stu-id="1d563-347">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="1d563-348">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="1d563-348">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="1d563-349">解决了以下问题</span><span class="sxs-lookup"><span data-stu-id="1d563-349">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="1d563-350">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="1d563-350">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="1d563-351">对 MultiValue 路由方法的支持</span><span class="sxs-lookup"><span data-stu-id="1d563-351">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="1d563-352">MultiValue 路由的新参数“MaxReturn”</span><span class="sxs-lookup"><span data-stu-id="1d563-352">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="1d563-353">对 Subnet 路由方法的支持</span><span class="sxs-lookup"><span data-stu-id="1d563-353">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="1d563-354">对终结点中的 IP 地址范围（子网）的支持</span><span class="sxs-lookup"><span data-stu-id="1d563-354">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="1d563-355">对配置文件中的自定义标头的支持</span><span class="sxs-lookup"><span data-stu-id="1d563-355">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="1d563-356">对配置文件中的预期状态代码范围的支持</span><span class="sxs-lookup"><span data-stu-id="1d563-356">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="1d563-357">对终结点中的自定义标头的支持</span><span class="sxs-lookup"><span data-stu-id="1d563-357">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="1d563-358">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="1d563-358">AzureRM.Websites</span></span>
* <span data-ttu-id="1d563-359">解决了错误地设置默认资源组的问题。</span><span class="sxs-lookup"><span data-stu-id="1d563-359">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="1d563-360">6.7.0 - 2018 年 8 月</span><span class="sxs-lookup"><span data-stu-id="1d563-360">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="1d563-361">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="1d563-361">AzureRM.Profile</span></span>
* <span data-ttu-id="1d563-362">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1d563-362">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="1d563-363">向默认的上下文名称添加用户 ID，避免上下文冲突</span><span class="sxs-lookup"><span data-stu-id="1d563-363">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="1d563-364">修复了 Clear-AzureRmContext 在选择上下文 #6398 时出现的问题</span><span class="sxs-lookup"><span data-stu-id="1d563-364">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="1d563-365">允许将租户域传递给“Connect-AzureRmAccount”的“-TenantId”参数</span><span class="sxs-lookup"><span data-stu-id="1d563-365">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="1d563-366">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="1d563-366">Azure.Storage</span></span>
* <span data-ttu-id="1d563-367">去除了 Azure 文件共享配额的 5TB 限制</span><span class="sxs-lookup"><span data-stu-id="1d563-367">Remove the 5TB limitation for Azure File Share quota</span></span>
- <span data-ttu-id="1d563-368">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="1d563-368">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="1d563-369">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="1d563-369">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="1d563-370">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1d563-370">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="1d563-371">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="1d563-371">Azure.AnalysisServices</span></span>
* <span data-ttu-id="1d563-372">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1d563-372">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="1d563-373">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="1d563-373">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="1d563-374">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1d563-374">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="1d563-375">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="1d563-375">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="1d563-376">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1d563-376">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="1d563-377">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="1d563-377">AzureRM.Automation</span></span>
* <span data-ttu-id="1d563-378">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1d563-378">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="1d563-379">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="1d563-379">AzureRM.Backup</span></span>
* <span data-ttu-id="1d563-380">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1d563-380">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="1d563-381">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="1d563-381">AzureRM.Batch</span></span>
* <span data-ttu-id="1d563-382">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1d563-382">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="1d563-383">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="1d563-383">AzureRM.Billing</span></span>
* <span data-ttu-id="1d563-384">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1d563-384">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="1d563-385">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="1d563-385">AzureRM.Cdn</span></span>
* <span data-ttu-id="1d563-386">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1d563-386">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="1d563-387">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="1d563-387">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="1d563-388">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1d563-388">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="1d563-389">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="1d563-389">AzureRM.Compute</span></span>
* <span data-ttu-id="1d563-390">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1d563-390">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="1d563-391">为 New-AzureRmVmssConfig 增加了 EvictionPolicy 参数</span><span class="sxs-lookup"><span data-stu-id="1d563-391">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="1d563-392">在 New-AzureRmVm 的 DiskFileParameterSet 中使用默认位置（如果未指定 Location）</span><span class="sxs-lookup"><span data-stu-id="1d563-392">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="1d563-393">修复了 Save-AzureRmVMImage 中的参数说明</span><span class="sxs-lookup"><span data-stu-id="1d563-393">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="1d563-394">修复了某些单次传递相关方案的 Get-AzureRmVMDiskEncryptionStatus cmdlet</span><span class="sxs-lookup"><span data-stu-id="1d563-394">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="1d563-395">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="1d563-395">AzureRM.Consumption</span></span>
* <span data-ttu-id="1d563-396">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1d563-396">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="1d563-397">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="1d563-397">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="1d563-398">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1d563-398">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="1d563-399">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1d563-399">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="1d563-400">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1d563-400">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="1d563-401">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="1d563-401">AzureRM.DataFactories</span></span>
* <span data-ttu-id="1d563-402">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1d563-402">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="1d563-403">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="1d563-403">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="1d563-404">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1d563-404">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="1d563-405">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="1d563-405">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="1d563-406">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1d563-406">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="1d563-407">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1d563-407">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="1d563-408">修复了从 PowerShell 命令行设置 DebugPreference 时的调试问题</span><span class="sxs-lookup"><span data-stu-id="1d563-408">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="1d563-409">更新了 Set-AzureRmDataLakeStoreItemAcl 的示例</span><span class="sxs-lookup"><span data-stu-id="1d563-409">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="1d563-410">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1d563-410">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="1d563-411">更新了 Set-AzureRmDataLakeStoreItemAclEntry 的示例</span><span class="sxs-lookup"><span data-stu-id="1d563-411">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="1d563-412">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="1d563-412">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="1d563-413">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1d563-413">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="1d563-414">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="1d563-414">AzureRM.Dns</span></span>
* <span data-ttu-id="1d563-415">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1d563-415">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="1d563-416">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="1d563-416">AzureRM.EventGrid</span></span>
* <span data-ttu-id="1d563-417">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1d563-417">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="1d563-418">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="1d563-418">AzureRM.EventHub</span></span>
* <span data-ttu-id="1d563-419">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1d563-419">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="1d563-420">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="1d563-420">AzureRM.HDInsight</span></span>
* <span data-ttu-id="1d563-421">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1d563-421">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="1d563-422">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="1d563-422">AzureRM.Insights</span></span>
* <span data-ttu-id="1d563-423">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1d563-423">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="1d563-424">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="1d563-424">AzureRM.IotHub</span></span>
* <span data-ttu-id="1d563-425">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1d563-425">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="1d563-426">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1d563-426">AzureRM.KeyVault</span></span>
* <span data-ttu-id="1d563-427">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1d563-427">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="1d563-428">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="1d563-428">AzureRM.LogicApp</span></span>
* <span data-ttu-id="1d563-429">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1d563-429">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="1d563-430">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="1d563-430">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="1d563-431">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1d563-431">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="1d563-432">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="1d563-432">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="1d563-433">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1d563-433">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="1d563-434">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="1d563-434">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="1d563-435">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1d563-435">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="1d563-436">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="1d563-436">AzureRM.Media</span></span>
* <span data-ttu-id="1d563-437">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1d563-437">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="1d563-438">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="1d563-438">AzureRM.Network</span></span>
* <span data-ttu-id="1d563-439">增加了 Set-AzureRmLocalNetworkGateway 的示例</span><span class="sxs-lookup"><span data-stu-id="1d563-439">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="1d563-440">增加了 Add-AzureRmVirtualNetworkGatewayIpConfig、Get-AzureRmVirtualNetworkGatewayConnectionSharedKey 和 New-AzureRmVirtualNetworkGatewayConnection 的示例和说明</span><span class="sxs-lookup"><span data-stu-id="1d563-440">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="1d563-441">增加了 Remove-AzureRmVirtualNetworkGatewayIpConfig 和 Reset-AzureRmVirtualNetworkGateway 的示例</span><span class="sxs-lookup"><span data-stu-id="1d563-441">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="1d563-442">增加了 Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey 的示例</span><span class="sxs-lookup"><span data-stu-id="1d563-442">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="1d563-443">增加了 Set-AzureRmVirtualNetworkGatewayConnectionSharedKey 的示例</span><span class="sxs-lookup"><span data-stu-id="1d563-443">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="1d563-444">增加了 Set-AzureRmVirtualNetworkGatewayConnection 的示例</span><span class="sxs-lookup"><span data-stu-id="1d563-444">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="1d563-445">使用最新的代码生成器重新生成了 ApplicationSecurityGroup、RouteTable 和 Usage 的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="1d563-445">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="1d563-446">阐明了在尝试获取的子网不存在时 Get-AzureRmVirtualNetworkSubnetConfig 的错误消息</span><span class="sxs-lookup"><span data-stu-id="1d563-446">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="1d563-447">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="1d563-447">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="1d563-448">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1d563-448">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="1d563-449">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="1d563-449">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="1d563-450">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1d563-450">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="1d563-451">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="1d563-451">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="1d563-452">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1d563-452">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="1d563-453">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="1d563-453">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="1d563-454">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1d563-454">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="1d563-455">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1d563-455">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="1d563-456">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1d563-456">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="1d563-457">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="1d563-457">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="1d563-458">为 Get-AzureRmRecoveryServicesBackItem cmdlet 增加了策略筛选器。</span><span class="sxs-lookup"><span data-stu-id="1d563-458">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="1d563-459">此命令返回受给定策略 ID 保护的备份项的列表。</span><span class="sxs-lookup"><span data-stu-id="1d563-459">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="1d563-460">已将 Microsoft.Azure.Management.RecoveryServices.Backup 更新到 3.0.0-preview 版本。</span><span class="sxs-lookup"><span data-stu-id="1d563-460">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="1d563-461">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1d563-461">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="1d563-462">为 Restore-AzureRmRecoveryServicesBackupItem 增加了 TargetResourceGroupName 参数。</span><span class="sxs-lookup"><span data-stu-id="1d563-462">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="1d563-463">托管磁盘还原到的资源组。</span><span class="sxs-lookup"><span data-stu-id="1d563-463">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="1d563-464">适用于包含托管磁盘的 VM 的备份。</span><span class="sxs-lookup"><span data-stu-id="1d563-464">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="1d563-465">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="1d563-465">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="1d563-466">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1d563-466">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="1d563-467">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="1d563-467">AzureRM.RedisCache</span></span>
* <span data-ttu-id="1d563-468">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1d563-468">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="1d563-469">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="1d563-469">AzureRM.Relay</span></span>
* <span data-ttu-id="1d563-470">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1d563-470">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="1d563-471">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="1d563-471">AzureRM.Resources</span></span>
* <span data-ttu-id="1d563-472">支持在订阅范围部署模板。</span><span class="sxs-lookup"><span data-stu-id="1d563-472">Support template deployment at subscription scope.</span></span> <span data-ttu-id="1d563-473">增加了新 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="1d563-473">Add new Cmdlets:</span></span>
    - <span data-ttu-id="1d563-474">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="1d563-474">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="1d563-475">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="1d563-475">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="1d563-476">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="1d563-476">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="1d563-477">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="1d563-477">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="1d563-478">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="1d563-478">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="1d563-479">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="1d563-479">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="1d563-480">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="1d563-480">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="1d563-481">修复了在将上下文传递给 Set-AzureRmResource 时引发错误的问题</span><span class="sxs-lookup"><span data-stu-id="1d563-481">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="1d563-482">修复了 New-AzureRmResourceGroupDeployment 中的示例</span><span class="sxs-lookup"><span data-stu-id="1d563-482">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="1d563-483">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1d563-483">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="1d563-484">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="1d563-484">AzureRM.Scheduler</span></span>
* <span data-ttu-id="1d563-485">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1d563-485">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="1d563-486">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="1d563-486">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="1d563-487">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1d563-487">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="1d563-488">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1d563-488">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="1d563-489">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1d563-489">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="1d563-490">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="1d563-490">AzureRM.Sql</span></span>
* <span data-ttu-id="1d563-491">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1d563-491">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="1d563-492">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="1d563-492">AzureRM.Storage</span></span>
* <span data-ttu-id="1d563-493">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1d563-493">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="1d563-494">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="1d563-494">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="1d563-495">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1d563-495">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="1d563-496">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="1d563-496">AzureRM.Tags</span></span>
* <span data-ttu-id="1d563-497">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1d563-497">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="1d563-498">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="1d563-498">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="1d563-499">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1d563-499">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="1d563-500">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="1d563-500">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="1d563-501">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1d563-501">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="1d563-502">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="1d563-502">AzureRM.Websites</span></span>
* <span data-ttu-id="1d563-503">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1d563-503">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="1d563-504">6.6.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="1d563-504">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="1d563-505">常规</span><span class="sxs-lookup"><span data-stu-id="1d563-505">General</span></span>
* <span data-ttu-id="1d563-506">更新了所有帮助文件，以包括完整参数类型和正确的输入/输出类型。</span><span class="sxs-lookup"><span data-stu-id="1d563-506">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="1d563-507">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="1d563-507">AzureRM.Profile</span></span>
* <span data-ttu-id="1d563-508">更新了 Common.Strategy 库，以便能够验证资源的当前配置是否与目标资源兼容。</span><span class="sxs-lookup"><span data-stu-id="1d563-508">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="1d563-509">在 Common.Storage 中添加了 ps1xml 类型</span><span class="sxs-lookup"><span data-stu-id="1d563-509">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="1d563-510">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="1d563-510">Azure.Storage</span></span>
* <span data-ttu-id="1d563-511">增加了从 DefaultProfile 获取存储上下文的支持</span><span class="sxs-lookup"><span data-stu-id="1d563-511">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="1d563-512">为 cmdlet 输出类型属性增加了 Ps1XmlAttribute。</span><span class="sxs-lookup"><span data-stu-id="1d563-512">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="1d563-513">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="1d563-513">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="1d563-514">修复了问题 https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="1d563-514">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="1d563-515">修复了 Automapper 中将 PsApiManagementApi 转换为 ApiContract 的 bug</span><span class="sxs-lookup"><span data-stu-id="1d563-515">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="1d563-516">修复了问题 https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="1d563-516">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="1d563-517">修复了 File.Save 中没有使用编码类型重载的 bug</span><span class="sxs-lookup"><span data-stu-id="1d563-517">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="1d563-518">修复了问题 https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="1d563-518">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="1d563-519">升级到了 4.0.3 Nuget版本，该版本修复了 apiId 上的模式异常</span><span class="sxs-lookup"><span data-stu-id="1d563-519">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="1d563-520">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="1d563-520">AzureRM.Compute</span></span>
* <span data-ttu-id="1d563-521">修复因使用 PremiumLRS 存储帐户类型重命名而在 New-AzureRmVm 中使用 DiskFileParameterSet 创建 VM 失败的问题。</span><span class="sxs-lookup"><span data-stu-id="1d563-521">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="1d563-522">修复 Invoke-AzureRmVMRunCommand cmdlet</span><span class="sxs-lookup"><span data-stu-id="1d563-522">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="1d563-523">更新 Get-AzureRmAvailabilitySet 以启用列出订阅中的所有可用性集。</span><span class="sxs-lookup"><span data-stu-id="1d563-523">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="1d563-524">（ResouceGroupName 参数现在是可选的。）</span><span class="sxs-lookup"><span data-stu-id="1d563-524">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="1d563-525">更新“New-AzureRmVm”的 SimpleParameterSet 以在符合条件的 VM 上启用加速网络。</span><span class="sxs-lookup"><span data-stu-id="1d563-525">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="1d563-526">将 New-AzureRmVmss 简单参数集更新为在用户指定的 LB 已存在时创建 vmss 失败。</span><span class="sxs-lookup"><span data-stu-id="1d563-526">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="1d563-527">更新 New-AzureRmDisk 的示例</span><span class="sxs-lookup"><span data-stu-id="1d563-527">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="1d563-528">添加“New-AzureRmVM”的示例</span><span class="sxs-lookup"><span data-stu-id="1d563-528">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="1d563-529">更新 Set-AzureRmVMOSDisk 的说明</span><span class="sxs-lookup"><span data-stu-id="1d563-529">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="1d563-530">更新 Set-AzureRmVMBginfoExtension 的示例 1 以更正拼写和前缀。</span><span class="sxs-lookup"><span data-stu-id="1d563-530">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="1d563-531">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="1d563-531">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="1d563-532">将 ADF .Net SDK 版本更新为 1.1.0。</span><span class="sxs-lookup"><span data-stu-id="1d563-532">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="1d563-533">支持跨数据工厂的自承载集成运行时共享。</span><span class="sxs-lookup"><span data-stu-id="1d563-533">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="1d563-534">将新参数 -SharedIntegrationRuntimeResourceId 添加到 Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1d563-534">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="1d563-535">将新的可选参数 -LinkedDataFactoryName 添加到 Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1d563-535">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="1d563-536">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1d563-536">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="1d563-537">将数据平面 SDK (Microsoft.Azure.DataLake.Store) 版本更新为 1.1.9</span><span class="sxs-lookup"><span data-stu-id="1d563-537">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="1d563-538">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="1d563-538">AzureRM.EventHub</span></span>
* <span data-ttu-id="1d563-539">在删除 cmdlet 中更新了 InputObject 和 ResourceId 的管道</span><span class="sxs-lookup"><span data-stu-id="1d563-539">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="1d563-540">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="1d563-540">AzureRM.Insights</span></span>
* <span data-ttu-id="1d563-541">修复了帮助文件中 OutputType 的格式问题</span><span class="sxs-lookup"><span data-stu-id="1d563-541">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="1d563-542">使用 Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span><span class="sxs-lookup"><span data-stu-id="1d563-542">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="1d563-543">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1d563-543">AzureRM.KeyVault</span></span>
* <span data-ttu-id="1d563-544">修复了 Set-AzureRmKeyVaultAccessPolicy 中的管道问题</span><span class="sxs-lookup"><span data-stu-id="1d563-544">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="1d563-545">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="1d563-545">AzureRM.Network</span></span>
* <span data-ttu-id="1d563-546">添加了 LoadBalancerInboundNatPoolConfig cmdlet 的示例。</span><span class="sxs-lookup"><span data-stu-id="1d563-546">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="1d563-547">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="1d563-547">AzureRM.Resources</span></span>
* <span data-ttu-id="1d563-548">修复了为“Get-AzureRmResource”同时提供标记名称和值时出现的问题</span><span class="sxs-lookup"><span data-stu-id="1d563-548">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="1d563-549">使用“Set-AzureRmResource”修复管道方案</span><span class="sxs-lookup"><span data-stu-id="1d563-549">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="1d563-550">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="1d563-550">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="1d563-551">在删除 cmdlet 中更新了 InputObject 和 ResourceId 的管道</span><span class="sxs-lookup"><span data-stu-id="1d563-551">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="1d563-552">修复了几个问题</span><span class="sxs-lookup"><span data-stu-id="1d563-552">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="1d563-553">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="1d563-553">AzureRM.Sql</span></span>
* <span data-ttu-id="1d563-554">使用以下 cmdlet 添加服务器高级威胁防护支持：</span><span class="sxs-lookup"><span data-stu-id="1d563-554">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="1d563-555">Enable-AzureRmSqlServerAdvancedThreatProtection；Disable-AzureRmSqlServerAdvancedThreatProtection；Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1d563-555">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="1d563-556">使用以下 cmdlet 添加漏洞评估支持：</span><span class="sxs-lookup"><span data-stu-id="1d563-556">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="1d563-557">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings；Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings；Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="1d563-557">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="1d563-558">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline；Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline；Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="1d563-558">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="1d563-559">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan；Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord；Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="1d563-559">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="1d563-560">修复了 Remove-AzureRmSqlServerFirewallRule 中的示例</span><span class="sxs-lookup"><span data-stu-id="1d563-560">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="1d563-561">修复了 Get-AzureSqlSyncGroupLog 中非美国基础文化的日期时间处理错误</span><span class="sxs-lookup"><span data-stu-id="1d563-561">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="1d563-562">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="1d563-562">AzureRM.Storage</span></span>
* <span data-ttu-id="1d563-563">将 Ps1XmlAttribute 添加到 cmdlet 输出类型属性</span><span class="sxs-lookup"><span data-stu-id="1d563-563">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="1d563-564">在表视图中显示 StorageAccount cmdlet 输出</span><span class="sxs-lookup"><span data-stu-id="1d563-564">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="1d563-565">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1d563-565">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="1d563-566">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1d563-566">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="1d563-567">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1d563-567">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="1d563-568">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="1d563-568">AzureRM.Tags</span></span>
* <span data-ttu-id="1d563-569">从 Tag cmdlet 帮助中删除不正确的语句</span><span class="sxs-lookup"><span data-stu-id="1d563-569">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="1d563-570">6.5.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="1d563-570">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="1d563-571">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="1d563-571">AzureRM.Profile</span></span>
* <span data-ttu-id="1d563-572">更新了“Get-AzureRmContextAutosaveSetting”的帮助</span><span class="sxs-lookup"><span data-stu-id="1d563-572">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="1d563-573">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="1d563-573">Azure.Storage</span></span>
* <span data-ttu-id="1d563-574">支持使用只写 Sas 令牌上传 Blob 或文件</span><span class="sxs-lookup"><span data-stu-id="1d563-574">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="1d563-575">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="1d563-575">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="1d563-576">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="1d563-576">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="1d563-577">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="1d563-577">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="1d563-578">将所需属性 ResourceGroupName 添加到 AS。</span><span class="sxs-lookup"><span data-stu-id="1d563-578">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="1d563-579">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="1d563-579">AzureRM.Automation</span></span>
* <span data-ttu-id="1d563-580">更新帮助并添加“New-AzureRMAutomationSchedule”的示例</span><span class="sxs-lookup"><span data-stu-id="1d563-580">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="1d563-581">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="1d563-581">AzureRM.Compute</span></span>
* <span data-ttu-id="1d563-582">将 -Tag 参数添加到 Update/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="1d563-582">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="1d563-583">添加“Add-AzureRmVmssExtension”的示例</span><span class="sxs-lookup"><span data-stu-id="1d563-583">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="1d563-584">添加“Remove-AzureRmVmssExtension”的示例</span><span class="sxs-lookup"><span data-stu-id="1d563-584">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="1d563-585">更新“Set-AzureRmVMAccessExtension”的帮助</span><span class="sxs-lookup"><span data-stu-id="1d563-585">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="1d563-586">更新 New-AzureRmVmss 的 SimpleParameterSet，以默认情况下将 SinglePlacementGroup 设置为false，并添加开关参数“SinglePlacementGroup”，使用户能够在单个放置组中创建 VMSS。</span><span class="sxs-lookup"><span data-stu-id="1d563-586">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="1d563-587">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="1d563-587">AzureRM.EventHub</span></span>
* <span data-ttu-id="1d563-588">向 PSEventHubDRConfigurationAttributes 类添加了一个只读属性“PendingReplicationOperationsCount”，该属性在复制过程中为挂起的复制操作计数</span><span class="sxs-lookup"><span data-stu-id="1d563-588">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="1d563-589">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1d563-589">AzureRM.KeyVault</span></span>
* <span data-ttu-id="1d563-590">更新了 Set-AzureRmKeyVaultAccessPolicy 的错误消息</span><span class="sxs-lookup"><span data-stu-id="1d563-590">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="1d563-591">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="1d563-591">AzureRM.LogicApp</span></span>
* <span data-ttu-id="1d563-592">修复了 New-AzureRmLogicApp 中的“无法解析参数集”错误</span><span class="sxs-lookup"><span data-stu-id="1d563-592">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="1d563-593">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="1d563-593">AzureRM.Network</span></span>
* <span data-ttu-id="1d563-594">在多个租户中为 Set/Add-AzureRmVirtualNetworkPeering 启用跨虚拟网络对等互连</span><span class="sxs-lookup"><span data-stu-id="1d563-594">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="1d563-595">针对应用程序网关更新了以下 cmdlet</span><span class="sxs-lookup"><span data-stu-id="1d563-595">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="1d563-596">New-AzureRmApplicationGateway：添加了 EnableFIPS 标志和区域支持</span><span class="sxs-lookup"><span data-stu-id="1d563-596">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="1d563-597">New-AzureRmApplicationGatewaySku：添加了新的 sku Standard_v2 和 WAF_v2</span><span class="sxs-lookup"><span data-stu-id="1d563-597">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="1d563-598">Set-AzureRmApplicationGatewaySku：添加了新的 sku Standard_v2 和 WAF_v2</span><span class="sxs-lookup"><span data-stu-id="1d563-598">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="1d563-599">使用最新的生成器版本重新生成了 RouteTable cmdlet</span><span class="sxs-lookup"><span data-stu-id="1d563-599">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="1d563-600">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="1d563-600">AzureRM.Relay</span></span>
* <span data-ttu-id="1d563-601">更新了 Markdown 文件，其中修复了示例中的参数名称问题</span><span class="sxs-lookup"><span data-stu-id="1d563-601">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="1d563-602">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="1d563-602">AzureRM.Resources</span></span>
* <span data-ttu-id="1d563-603">更新了 Roleassignment 和 roledefinition cmdlet：</span><span class="sxs-lookup"><span data-stu-id="1d563-603">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="1d563-604">删除了作为分页的一部分完成的额外 roledefinition 调用。</span><span class="sxs-lookup"><span data-stu-id="1d563-604">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="1d563-605">修复了 Get-AzureRmRoleAssignment cmdlet</span><span class="sxs-lookup"><span data-stu-id="1d563-605">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="1d563-606">修复了 -ExpandPrincipalGroups 命令参数功能</span><span class="sxs-lookup"><span data-stu-id="1d563-606">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="1d563-607">修复了“Get-AzureRmResource”的问题，其中“-ResourceType”参数区分大小写</span><span class="sxs-lookup"><span data-stu-id="1d563-607">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="1d563-608">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="1d563-608">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="1d563-609">向列表 cmdlet 添加了 top 和 skip 参数</span><span class="sxs-lookup"><span data-stu-id="1d563-609">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="1d563-610">添加了标准到高级命名空间迁移 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="1d563-610">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="1d563-611">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="1d563-611">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="1d563-612">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="1d563-612">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="1d563-613">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="1d563-613">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="1d563-614">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="1d563-614">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="1d563-615">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="1d563-615">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="1d563-616">向 PSServiceBusDRConfigurationAttributes 类添加了一个只读属性“PendingReplicationOperationsCount”，该属性在复制过程中为挂起的复制操作计数</span><span class="sxs-lookup"><span data-stu-id="1d563-616">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="1d563-617">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1d563-617">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="1d563-618">更新了“New-AzureRmServiceFabricCluster”的示例</span><span class="sxs-lookup"><span data-stu-id="1d563-618">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="1d563-619">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="1d563-619">AzureRM.Sql</span></span>
* <span data-ttu-id="1d563-620">为 Management.Sql 添加新的 Cmdlet，以允许客户将 TDE 证书添加到 Sql Server 实例或托管实例</span><span class="sxs-lookup"><span data-stu-id="1d563-620">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="1d563-621">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="1d563-621">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="1d563-622">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="1d563-622">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="1d563-623">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="1d563-623">AzureRM.Websites</span></span>
* <span data-ttu-id="1d563-624">设置为 false 时，`Set-AzureRmWebApp -AssignIdentity` 和 `Set-AzureRmWebAppSlot -AssignIdentity` 现在将从站点对象中删除 Identity 属性。同时移除预览标记。</span><span class="sxs-lookup"><span data-stu-id="1d563-624">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="1d563-625">`Get-AzureRmWebAppMetrics`、`Get-AzureRmAppServicePlanMetrics` 示例已更新</span><span class="sxs-lookup"><span data-stu-id="1d563-625">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="1d563-626">`Set-AzureRmWebApp -PhpVersion` 支持 off 作为有效的 php 版本</span><span class="sxs-lookup"><span data-stu-id="1d563-626">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="1d563-627">6.4.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="1d563-627">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="1d563-628">常规</span><span class="sxs-lookup"><span data-stu-id="1d563-628">General</span></span>
* <span data-ttu-id="1d563-629">修复了大多数模块的帮助文件中的 OutputType 格式问题</span><span class="sxs-lookup"><span data-stu-id="1d563-629">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="1d563-630">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="1d563-630">AzureRM.Profile</span></span>
* <span data-ttu-id="1d563-631">已将 Ps1Xml 属性添加到基本输出类型</span><span class="sxs-lookup"><span data-stu-id="1d563-631">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="1d563-632">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="1d563-632">AzureRM.Compute</span></span>
* <span data-ttu-id="1d563-633">VMSS 的 IP 标记功能</span><span class="sxs-lookup"><span data-stu-id="1d563-633">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="1d563-634">已添加“New-AzureRmVmssIpTagConfig”cmdlet</span><span class="sxs-lookup"><span data-stu-id="1d563-634">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="1d563-635">已将 IpTag 参数添加到 New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="1d563-635">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="1d563-636">VMSS 的自动 OS 回滚功能</span><span class="sxs-lookup"><span data-stu-id="1d563-636">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="1d563-637">已将 DisableAutoRollback 参数添加到 New-AzureRmVmssConfig 和 Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="1d563-637">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="1d563-638">VMSS 的 OS 升级历史记录功能</span><span class="sxs-lookup"><span data-stu-id="1d563-638">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="1d563-639">已将 OSUpgradeHistory 开关参数添加到 Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="1d563-639">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="1d563-640">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="1d563-640">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="1d563-641">通过以下命令添加目录 ACL 的支持：</span><span class="sxs-lookup"><span data-stu-id="1d563-641">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="1d563-642">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="1d563-642">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="1d563-643">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="1d563-643">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="1d563-644">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="1d563-644">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="1d563-645">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1d563-645">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="1d563-646">为 Set-AzureRmDataLakeStoreItemAclEntry、Remove-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAcl 添加了取消支持和进度跟踪</span><span class="sxs-lookup"><span data-stu-id="1d563-646">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="1d563-647">为 Export-AzureRmDataLakeStoreChildItemProperties 添加了取消支持</span><span class="sxs-lookup"><span data-stu-id="1d563-647">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="1d563-648">修复了执行递归操作的 cmdlet 的调试消息刷新</span><span class="sxs-lookup"><span data-stu-id="1d563-648">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="1d563-649">修复了 DataLake cmdlet 的测试位置</span><span class="sxs-lookup"><span data-stu-id="1d563-649">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="1d563-650">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="1d563-650">AzureRM.EventHub</span></span>
* <span data-ttu-id="1d563-651">已将可选的 MaxCount 参数添加到“列出操作”cmdlet Get-AzureRmEventHub 和 Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="1d563-651">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="1d563-652">修复了 New-AzureRmEventHub cmdlet 的问题：创建新事件中心时至少需要一个参数。</span><span class="sxs-lookup"><span data-stu-id="1d563-652">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="1d563-653">提供了默认参数集。</span><span class="sxs-lookup"><span data-stu-id="1d563-653">Provided Default Parameter set.</span></span>
* <span data-ttu-id="1d563-654">已将可选参数 -KeyValue 添加到 New-AzureRmEventHubKey cmdlet，该参数可让用户提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="1d563-654">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="1d563-655">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1d563-655">AzureRM.KeyVault</span></span>
* <span data-ttu-id="1d563-656">修复了 Get-AzureRmKeyVault -Tag 返回所有资源的问题</span><span class="sxs-lookup"><span data-stu-id="1d563-656">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="1d563-657">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="1d563-657">AzureRM.Network</span></span>
* <span data-ttu-id="1d563-658">为区域冗余的 VirtualNetworkGateways 公开新 SKU</span><span class="sxs-lookup"><span data-stu-id="1d563-658">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="1d563-659">通过 ARM 为以下功能添加了新命令：ExpressRoute 合作伙伴 API</span><span class="sxs-lookup"><span data-stu-id="1d563-659">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="1d563-660">添加了 Get-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="1d563-660">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="1d563-661">添加了 Set-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="1d563-661">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="1d563-662">添加了 Add-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="1d563-662">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="1d563-663">添加了 Get-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="1d563-663">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="1d563-664">添加了 Remove-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="1d563-664">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="1d563-665">添加了 Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="1d563-665">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="1d563-666">添加了 Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="1d563-666">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="1d563-667">添加了 Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="1d563-667">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="1d563-668">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="1d563-668">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="1d563-669">添加了 Get-AzureRmRecoveryServicesBackupStatus cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1d563-669">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="1d563-670">此 cmdlet 采用 VM ID，并检查 VM 是否受订阅中的某个保管库保护。</span><span class="sxs-lookup"><span data-stu-id="1d563-670">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="1d563-671">如果存在此类保管库，该 cmdlet 会输出该保管库的详细信息。</span><span class="sxs-lookup"><span data-stu-id="1d563-671">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="1d563-672">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="1d563-672">AzureRM.Resources</span></span>
* <span data-ttu-id="1d563-673">更新了 Get-AzureRmPolicyAssignment cmdlet：</span><span class="sxs-lookup"><span data-stu-id="1d563-673">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="1d563-674">添加了在管理组级别列出 -Scope 值的支持</span><span class="sxs-lookup"><span data-stu-id="1d563-674">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="1d563-675">添加了在管理组级别使用 -Scope 值检索单个分配的支持</span><span class="sxs-lookup"><span data-stu-id="1d563-675">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="1d563-676">已将 -Effective 和 -All 开关添加到 control 参数</span><span class="sxs-lookup"><span data-stu-id="1d563-676">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="1d563-677">更新了 Get/New/Remove/Set-AzureRmPolicyDefinition cmdlet</span><span class="sxs-lookup"><span data-stu-id="1d563-677">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="1d563-678">添加了 -ManagementGroupName 参数，以将操作应用到给定的管理组</span><span class="sxs-lookup"><span data-stu-id="1d563-678">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="1d563-679">添加了 -SubscriptionId 参数，以将操作应用到给定的订阅</span><span class="sxs-lookup"><span data-stu-id="1d563-679">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="1d563-680">更新了 Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlet</span><span class="sxs-lookup"><span data-stu-id="1d563-680">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="1d563-681">添加了 -ManagementGroupName 参数，以将操作应用到给定的管理组</span><span class="sxs-lookup"><span data-stu-id="1d563-681">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="1d563-682">添加了 -SubscriptionId 参数，以将操作应用到给定的订阅</span><span class="sxs-lookup"><span data-stu-id="1d563-682">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="1d563-683">添加了使用 TemplateParameterObject 时在参数中指定 KeyVault 机密引用的支持</span><span class="sxs-lookup"><span data-stu-id="1d563-683">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="1d563-684">修复了忽略“New-AzureRmADAppCredential”的“-EndDate”参数的问题</span><span class="sxs-lookup"><span data-stu-id="1d563-684">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="1d563-685">修复了“Add-AzureRmADGroupMember”使用错误的 URL 发出请求的问题</span><span class="sxs-lookup"><span data-stu-id="1d563-685">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="1d563-686">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="1d563-686">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="1d563-687">已将可选参数 -KeyValue 添加到 New-AzureRmServiceBusKey cmdlet，该参数可让用户提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="1d563-687">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="1d563-688">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="1d563-688">AzureRM.Sql</span></span>
* <span data-ttu-id="1d563-689">在 AzureRmSqlDatabaseRestorePoint 帮助中澄清了 SQLDW 的用户定义还原点</span><span class="sxs-lookup"><span data-stu-id="1d563-689">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="1d563-690">更新了多个 cmdlet 中 -ComputeGeneration 参数的文档</span><span class="sxs-lookup"><span data-stu-id="1d563-690">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="1d563-691">6.3.0 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="1d563-691">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="1d563-692">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="1d563-692">AzureRM.Profile</span></span>
* <span data-ttu-id="1d563-693">更新了 Enable-AzureRmContextAutoSave 的错误消息</span><span class="sxs-lookup"><span data-stu-id="1d563-693">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="1d563-694">在运行没有旧上下文的“Connect-AzureRmAccount”时为每个订阅创建一个上下文</span><span class="sxs-lookup"><span data-stu-id="1d563-694">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="1d563-695">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="1d563-695">Azure.Storage</span></span>
* <span data-ttu-id="1d563-696">在帮助文件中增加了关于 -Permissions 参数的其他信息。</span><span class="sxs-lookup"><span data-stu-id="1d563-696">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="1d563-697">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="1d563-697">AzureRM.Compute</span></span>
* <span data-ttu-id="1d563-698">“Get-AzureRmVmDiskEncryptionStatus”修复了一个针对没有数据磁盘的 VM 观察到的问题</span><span class="sxs-lookup"><span data-stu-id="1d563-698">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="1d563-699">更新计算客户端库版本以修复以下 cmdlet</span><span class="sxs-lookup"><span data-stu-id="1d563-699">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="1d563-700">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="1d563-700">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="1d563-701">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="1d563-701">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="1d563-702">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="1d563-702">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="1d563-703">修复了以下 cmdlet，因此可以正确地显示“操作 ID”和“操作状态”：</span><span class="sxs-lookup"><span data-stu-id="1d563-703">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="1d563-704">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="1d563-704">Start-AzureRmVM</span></span>
    - <span data-ttu-id="1d563-705">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="1d563-705">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="1d563-706">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="1d563-706">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="1d563-707">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="1d563-707">Set-AzureRmVM</span></span>
    - <span data-ttu-id="1d563-708">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="1d563-708">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="1d563-709">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="1d563-709">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="1d563-710">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="1d563-710">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="1d563-711">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="1d563-711">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="1d563-712">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="1d563-712">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="1d563-713">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="1d563-713">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="1d563-714">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="1d563-714">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="1d563-715">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="1d563-715">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="1d563-716">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="1d563-716">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="1d563-717">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="1d563-717">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="1d563-718">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="1d563-718">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="1d563-719">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="1d563-719">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="1d563-720">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="1d563-720">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="1d563-721">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="1d563-721">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="1d563-722">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="1d563-722">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="1d563-723">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="1d563-723">AzureRM.EventGrid</span></span>
* <span data-ttu-id="1d563-724">在 Update-AzureRmEventGridSubscription cmdlet 中删除 SubjectBeginsWith/SubjectEndsWith 的 ValidateNotNullOrEmpty 验证条件，允许根据需要将这些参数更改为空字符串。</span><span class="sxs-lookup"><span data-stu-id="1d563-724">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="1d563-725">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1d563-725">AzureRM.KeyVault</span></span>
* <span data-ttu-id="1d563-726">修复运行 Get-AzureRmKeyVault -Tag 时不返回任何标记的问题</span><span class="sxs-lookup"><span data-stu-id="1d563-726">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="1d563-727">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="1d563-727">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="1d563-728">策略见解 cmdlet 的公开发行版</span><span class="sxs-lookup"><span data-stu-id="1d563-728">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="1d563-729">使用 API 版本 2018-04-04</span><span class="sxs-lookup"><span data-stu-id="1d563-729">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="1d563-730">向 Get-AzureRmPolicyStateSummary 的结果添加了 PolicyDefinitionReferenceId</span><span class="sxs-lookup"><span data-stu-id="1d563-730">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="1d563-731">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="1d563-731">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="1d563-732">向 RecoveryServices.Backup cmdlet 添加了 -Vault 参数。</span><span class="sxs-lookup"><span data-stu-id="1d563-732">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="1d563-733">传递时，此项会替代 Set-AzureRmRecoveryServicesContext cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1d563-733">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="1d563-734">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="1d563-734">AzureRM.Sql</span></span>
* <span data-ttu-id="1d563-735">更新了 Get-AzureRmSqlDatabaseExpanded 的帮助文件中的示例</span><span class="sxs-lookup"><span data-stu-id="1d563-735">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="1d563-736">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="1d563-736">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="1d563-737">更新了 Add-AzureRmTrafficManagerEndpointConfig 的帮助文件</span><span class="sxs-lookup"><span data-stu-id="1d563-737">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="1d563-738">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="1d563-738">AzureRM.Websites</span></span>
* <span data-ttu-id="1d563-739">更新了“Set-AzureRmWebApp”，在使用 -AssignIdentity 时不覆盖 AppSettings</span><span class="sxs-lookup"><span data-stu-id="1d563-739">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="1d563-740">更新了“New-AzureRmWebAppSlot”，允许使用 AppServicePlan 作为可选参数</span><span class="sxs-lookup"><span data-stu-id="1d563-740">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="1d563-741">6.2.1 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="1d563-741">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="1d563-742">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="1d563-742">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="1d563-743">更新了 PSWorkspace 模型，允许 Network 使用 type 作为参数</span><span class="sxs-lookup"><span data-stu-id="1d563-743">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="1d563-744">6.2.0 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="1d563-744">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="1d563-745">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="1d563-745">AzureRM.Profile</span></span>
* <span data-ttu-id="1d563-746">修复了 Newtonsoft.Json 的版本 10.0.3 在模块导入时无法加载的问题</span><span class="sxs-lookup"><span data-stu-id="1d563-746">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="1d563-747">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="1d563-747">AzureRM.Compute</span></span>
* <span data-ttu-id="1d563-748">VMSS VM 更新功能</span><span class="sxs-lookup"><span data-stu-id="1d563-748">VMSS VM Update feature</span></span>
    - <span data-ttu-id="1d563-749">增加了“Update-AzureRmVmssVM”和“New-AzureRmVMDataDisk”cmdlet</span><span class="sxs-lookup"><span data-stu-id="1d563-749">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="1d563-750">为“Add-AzureRmVMDataDisk”cmdlet 增加了 VirtualMachineScaleSetVM 参数，支持向 Vmss VM 添加数据磁盘。</span><span class="sxs-lookup"><span data-stu-id="1d563-750">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="1d563-751">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="1d563-751">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="1d563-752">将 ADF.Net SDK 版本更新到了 0.8.0-preview，其中包含以下更改：</span><span class="sxs-lookup"><span data-stu-id="1d563-752">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="1d563-753">增加了“配置工厂存储库”操作</span><span class="sxs-lookup"><span data-stu-id="1d563-753">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="1d563-754">更新了 QuickBooks LinkedService，可以公开 consumerKey 和 consumerSecret 属性</span><span class="sxs-lookup"><span data-stu-id="1d563-754">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="1d563-755">已将多个模型类型从 SecretBase 更新为 Object</span><span class="sxs-lookup"><span data-stu-id="1d563-755">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="1d563-756">增加了 Blob 事件触发器</span><span class="sxs-lookup"><span data-stu-id="1d563-756">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="1d563-757">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1d563-757">AzureRM.KeyVault</span></span>
* <span data-ttu-id="1d563-758">使用示例输出更新了文档</span><span class="sxs-lookup"><span data-stu-id="1d563-758">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="1d563-759">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="1d563-759">AzureRM.Network</span></span>
* <span data-ttu-id="1d563-760">在网络观察程序 cmdlet 上启用了流量分析参数</span><span class="sxs-lookup"><span data-stu-id="1d563-760">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="1d563-761">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="1d563-761">AzureRM.Resources</span></span>
* <span data-ttu-id="1d563-762">修复了从“Get-AzureRmResource”返回的“PSResource”对象的“Properties”属性问题</span><span class="sxs-lookup"><span data-stu-id="1d563-762">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="1d563-763">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="1d563-763">AzureRM.Scheduler</span></span>
* <span data-ttu-id="1d563-764">修复了更新 ServiceBusQueueJob 无法设置新 Auth 值的问题</span><span class="sxs-lookup"><span data-stu-id="1d563-764">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="1d563-765">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="1d563-765">AzureRM.Sql</span></span>
* <span data-ttu-id="1d563-766">使用可选的 LicenseType 参数更新了以下 cmdlet</span><span class="sxs-lookup"><span data-stu-id="1d563-766">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="1d563-767">New-AzureRmSqlDatabase；Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1d563-767">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="1d563-768">New-AzureRmSqlElasticPool；Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="1d563-768">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="1d563-769">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="1d563-769">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="1d563-770">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="1d563-770">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="1d563-771">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1d563-771">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="1d563-772">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="1d563-772">AzureRM.Websites</span></span>
* <span data-ttu-id="1d563-773">更新了“New-AzureRMWebApp”，可以使用策略库中的常用算法。</span><span class="sxs-lookup"><span data-stu-id="1d563-773">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="1d563-774">6.1.0 - 2018 年 5 月</span><span class="sxs-lookup"><span data-stu-id="1d563-774">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="1d563-775">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="1d563-775">AzureRM.Profile</span></span>
* <span data-ttu-id="1d563-776">修复了运行“Clear-AzureRmContext”时会保留空上下文的问题，该上下文使用旧的默认上下文的名称，导致用户无法使用旧名称创建新的上下文</span><span class="sxs-lookup"><span data-stu-id="1d563-776">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="1d563-777">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="1d563-777">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="1d563-778">允许在 AS 上执行网关的关联/取消关联操作。</span><span class="sxs-lookup"><span data-stu-id="1d563-778">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="1d563-779">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="1d563-779">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="1d563-780">增加了对 ApiVersions、ApiReleases 和 ApiRevisions 的支持</span><span class="sxs-lookup"><span data-stu-id="1d563-780">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="1d563-781">增加了对 ServiceFabric 后端的支持</span><span class="sxs-lookup"><span data-stu-id="1d563-781">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="1d563-782">增加了对 Application Insights Logger 的支持</span><span class="sxs-lookup"><span data-stu-id="1d563-782">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="1d563-783">增加的支持包括认可“基本”SKU 是 API 管理服务的有效 SKU</span><span class="sxs-lookup"><span data-stu-id="1d563-783">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="1d563-784">增加的支持包括允许将专用 CA 颁发的证书作为根证书或 CA 证书安装</span><span class="sxs-lookup"><span data-stu-id="1d563-784">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="1d563-785">增加的支持包括通过 KeyVault 和多个代理主机名接受自定义 SSL 证书</span><span class="sxs-lookup"><span data-stu-id="1d563-785">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="1d563-786">增加了对 MSI 标识的支持</span><span class="sxs-lookup"><span data-stu-id="1d563-786">Added support for MSI identity</span></span>
* <span data-ttu-id="1d563-787">增加的支持包括通过 URL 接受策略 注意：以下 cmdlet 将在未来版本中弃用</span><span class="sxs-lookup"><span data-stu-id="1d563-787">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="1d563-788">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="1d563-788">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="1d563-789">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="1d563-789">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="1d563-790">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="1d563-790">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="1d563-791">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="1d563-791">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="1d563-792">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="1d563-792">AzureRM.Batch</span></span>
* <span data-ttu-id="1d563-793">发布新 cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="1d563-793">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="1d563-794">发布新 cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="1d563-794">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="1d563-795">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="1d563-795">AzureRM.Consumption</span></span>
* <span data-ttu-id="1d563-796">在 Cmdlet Get-AzureRmConsumptionUsageDetail 中增加了新参数 Expand、ResourceGroup、InstanceName、InstanceId、Tags、Top</span><span class="sxs-lookup"><span data-stu-id="1d563-796">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="1d563-797">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1d563-797">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="1d563-798">修复了 Export-AzureRmDataLakeStoreChildItemProperties 的示例</span><span class="sxs-lookup"><span data-stu-id="1d563-798">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="1d563-799">修复了 Set-AzureRmDataLakeStoreItemAclEntry 中 Recurse 用例的 null 参数异常</span><span class="sxs-lookup"><span data-stu-id="1d563-799">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="1d563-800">修复了 Set-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAcl、Remove-AzureRmDataLakeStoreItemAclEntry 的帮助文件</span><span class="sxs-lookup"><span data-stu-id="1d563-800">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="1d563-801">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="1d563-801">AzureRM.Network</span></span>
* <span data-ttu-id="1d563-802">将网络 SDK 版本从 18.0.0-preview 升至 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="1d563-802">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="1d563-803">增加了用于创建协议配置的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="1d563-803">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="1d563-804">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="1d563-804">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="1d563-805">增加了用于向现有的快速路由线路添加新的线路连接的 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1d563-805">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="1d563-806">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="1d563-806">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="1d563-807">增加了用于从现有的快速路由线路删除线路连接的 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1d563-807">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="1d563-808">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="1d563-808">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="1d563-809">增加了用于检索线路连接的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="1d563-809">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="1d563-810">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="1d563-810">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="1d563-811">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1d563-811">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="1d563-812">修复了使用生成的证书进行服务器身份验证的问题（问题 5998）</span><span class="sxs-lookup"><span data-stu-id="1d563-812">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="1d563-813">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="1d563-813">AzureRM.Sql</span></span>
* <span data-ttu-id="1d563-814">更新了审核 cmdlet，允许删除 AuditActions 或 AuditActionGroups</span><span class="sxs-lookup"><span data-stu-id="1d563-814">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="1d563-815">修复了设置新的灵活保留策略时使用 Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy 出现的问题。该问题的具体表现是：在命令失败的同时，出现“不再支持使用 Azure 恢复服务保管库和策略配置长期保留策略。</span><span class="sxs-lookup"><span data-stu-id="1d563-815">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="1d563-816">请使用新的灵活保留策略提交请求”错误消息。</span><span class="sxs-lookup"><span data-stu-id="1d563-816">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="1d563-817">更新了与 Azure SQL 数据库/ElasticPool 的创建/更新相关的所有 cmdlet，允许使用新的数据库 API，而这些 cmdlet 支持的 SKU 属性则适用于规模和层相关属性。</span><span class="sxs-lookup"><span data-stu-id="1d563-817">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="1d563-818">更新的 cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="1d563-818">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="1d563-819">New-AzureRmSqlDatabase；Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1d563-819">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="1d563-820">New-AzureRmSqlElasticPool；Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="1d563-820">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="1d563-821">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="1d563-821">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="1d563-822">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="1d563-822">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="1d563-823">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1d563-823">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="1d563-824">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="1d563-824">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="1d563-825">更新了“Get-AzureRmTrafficManagerProfile”的参数，要求在使用 -Name 参数时使用 -ResourceGroupName 参数。</span><span class="sxs-lookup"><span data-stu-id="1d563-825">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
