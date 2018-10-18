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
ms.openlocfilehash: 6a33d1a85fc61d0281bf1183163185b0dc4d3a12
ms.sourcegitcommit: f6f5e256143aa6c097de3e57e930d8badea49f30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2018
ms.locfileid: "49399053"
---
# <a name="release-notes"></a><span data-ttu-id="a0f9a-103">发行说明</span><span class="sxs-lookup"><span data-stu-id="a0f9a-103">Release notes</span></span>

<span data-ttu-id="a0f9a-104">下面是此版本中对 Azure PowerShell 所做的更改列表。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="6100---october-2018"></a><span data-ttu-id="a0f9a-105">6.10.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="a0f9a-105">6.10.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="a0f9a-106">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="a0f9a-106">Azure.Storage</span></span>
* <span data-ttu-id="a0f9a-107">修复了 Copy Blob/File 在目标有元数据问题时不会复制元数据的问题</span><span class="sxs-lookup"><span data-stu-id="a0f9a-107">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="a0f9a-108">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="a0f9a-108">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="a0f9a-109">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="a0f9a-109">Start-AzureStorageFileCopy</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="a0f9a-110">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a0f9a-110">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="a0f9a-111">在没有现有帐户的情况下支持 Get-AzureRmCognitiveServicesAccountSkus。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-111">Support Get-AzureRmCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="a0f9a-112">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a0f9a-112">AzureRM.Compute</span></span>
* <span data-ttu-id="a0f9a-113">修复了 Get-AzureRmVM -ResourceGroupName <rg>，以在需要时返回超过 50 个结果</span><span class="sxs-lookup"><span data-stu-id="a0f9a-113">Fix Get-AzureRmVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="a0f9a-114">在 New-AzureRmVmss cmdlet 帮助中添加了“SimpleParameterSet”的示例。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-114">Added an example of the 'SimpleParameterSet' to New-AzureRmVmss cmdlet help.</span></span>
* <span data-ttu-id="a0f9a-115">修复了 Azure 磁盘加密进度消息中的拼写错误</span><span class="sxs-lookup"><span data-stu-id="a0f9a-115">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="a0f9a-116">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="a0f9a-116">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="a0f9a-117">将 ADF .Net SDK 版本更新为 2.3.0。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-117">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="a0f9a-118">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a0f9a-118">AzureRM.Network</span></span>
* <span data-ttu-id="a0f9a-119">添加了 NetworkProfile 功能。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-119">Added NetworkProfile functionality.</span></span> <span data-ttu-id="a0f9a-120">添加了新 cmdlet</span><span class="sxs-lookup"><span data-stu-id="a0f9a-120">new cmdlets added</span></span>
    - <span data-ttu-id="a0f9a-121">Get-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a0f9a-121">Get-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="a0f9a-122">New-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a0f9a-122">New-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="a0f9a-123">Remove-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a0f9a-123">Remove-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="a0f9a-124">Set-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a0f9a-124">Set-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="a0f9a-125">New-AzureRMContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="a0f9a-125">New-AzureRMContainerNicConfig</span></span>
    - <span data-ttu-id="a0f9a-126">New-AzureRmContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="a0f9a-126">New-AzureRmContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="a0f9a-127">在子网模型上添加了服务关联链接</span><span class="sxs-lookup"><span data-stu-id="a0f9a-127">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="a0f9a-128">添加了 cmdlet New-AzureRmVirtualNetworkTap、Get-AzureRmVirtualNetworkTap、Set-AzureRmVirtualNetworkTap、Remove-AzureRmVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="a0f9a-128">Added cmdlet New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap</span></span>
* <span data-ttu-id="a0f9a-129">添加了 cmdlet Set-AzureRmNEtworkInterfaceTapConfig、Get-AzureRmNEtworkInterfaceTapConfig、Remove-AzureRmNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="a0f9a-129">Added cmdlet Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="a0f9a-130">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="a0f9a-130">AzureRM.RedisCache</span></span>
* <span data-ttu-id="a0f9a-131">今后允许任何字符串作为 Size 参数。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-131">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="a0f9a-132">在 PSArgumentCompleter 弹出窗口中添加了 P5</span><span class="sxs-lookup"><span data-stu-id="a0f9a-132">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="a0f9a-133">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="a0f9a-133">AzureRM.Resources</span></span>
* <span data-ttu-id="a0f9a-134">将缺少的 -Mode 参数添加到 Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a0f9a-134">Add missing -Mode parameter to Set-AzureRmPolicyDefinition</span></span>
* <span data-ttu-id="a0f9a-135">对于使用包含用户的源的操作，修复了 Get-AzureRmProviderOperation commandlet bug</span><span class="sxs-lookup"><span data-stu-id="a0f9a-135">Fix Get-AzureRmProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="a0f9a-136">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="a0f9a-136">AzureRM.Sql</span></span>
* <span data-ttu-id="a0f9a-137">修复了某些备份 cmdlet 无法识别当前 azure 订阅的问题</span><span class="sxs-lookup"><span data-stu-id="a0f9a-137">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="a0f9a-138">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="a0f9a-138">AzureRM.Storage</span></span>
* <span data-ttu-id="a0f9a-139">支持获取特定位置的存储资源使用情况，并对于获取的全局存储资源使用情况已过时添加警告消息。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-139">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="a0f9a-140">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="a0f9a-140">Get-AzureRmStorageUsage</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="a0f9a-141">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="a0f9a-141">AzureRM.Websites</span></span>
* <span data-ttu-id="a0f9a-142">新 Cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl - 获取容器持续部署 Webhook URL</span><span class="sxs-lookup"><span data-stu-id="a0f9a-142">New Cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="a0f9a-143">新 Cmdlet New-AzureRMWebAppContainerPSSession 和 Enter-WebAppContainerPSSession - 在 Windows 容器应用中启动 PowerShell 远程会话</span><span class="sxs-lookup"><span data-stu-id="a0f9a-143">New Cmdlets New-AzureRMWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="690---september-2018"></a><span data-ttu-id="a0f9a-144">6.9.0 - 2018 年 9 月</span><span class="sxs-lookup"><span data-stu-id="a0f9a-144">6.9.0 - September 2018</span></span>
#### <a name="general"></a><span data-ttu-id="a0f9a-145">常规</span><span class="sxs-lookup"><span data-stu-id="a0f9a-145">General</span></span>
* <span data-ttu-id="a0f9a-146">AzureRM.SignalR 已添加到 AzureRM 汇总模块</span><span class="sxs-lookup"><span data-stu-id="a0f9a-146">AzureRM.SignalR was added to the AzureRM rollup module</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="a0f9a-147">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="a0f9a-147">AzureRM.Profile</span></span>
* <span data-ttu-id="a0f9a-148">对存储常用代码进行了细微的更改</span><span class="sxs-lookup"><span data-stu-id="a0f9a-148">Minor changes to the storage common code</span></span>
* <span data-ttu-id="a0f9a-149">更新了帮助文件，使之包括完整参数类型。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-149">Updated help files to include full parameter types.</span></span>
- <span data-ttu-id="a0f9a-150">已在 ServicePrincipalCertificateWithSubscriptionId 参数集中将 -ServicePrincipal 更改为非强制性项</span><span class="sxs-lookup"><span data-stu-id="a0f9a-150">Changed -ServicePrincipal to non-mandatory in the ServicePrincipalCertificateWithSubscriptionId parameter set</span></span> 

#### <a name="azurestorage"></a><span data-ttu-id="a0f9a-151">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="a0f9a-151">Azure.Storage</span></span>
* <span data-ttu-id="a0f9a-152">支持使用 OAuth 创建存储上下文。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-152">Support create Storage Context with OAuth.</span></span> 
    - <span data-ttu-id="a0f9a-153">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="a0f9a-153">New-AzureStorageContext</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="a0f9a-154">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="a0f9a-154">AzureRM.Cdn</span></span>
* <span data-ttu-id="a0f9a-155">在 Cdn 定价 sku 中增加了 Standard_Microsoft。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-155">Added Standard_Microsoft in Cdn pricing sku.</span></span> 

#### <a name="azurermcompute"></a><span data-ttu-id="a0f9a-156">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a0f9a-156">AzureRM.Compute</span></span>
* <span data-ttu-id="a0f9a-157">将 Keyvault 和存储的依赖项移到了常用依赖项中</span><span class="sxs-lookup"><span data-stu-id="a0f9a-157">Move dependencies on Keyvault and Storage to the common dependencies</span></span>
* <span data-ttu-id="a0f9a-158">增加了对 AEM cmdlet 的支持，可以使用更多的虚拟机大小</span><span class="sxs-lookup"><span data-stu-id="a0f9a-158">Add support for more virutal machine sizes to AEM cmdlets</span></span>
* <span data-ttu-id="a0f9a-159">为 New-AzureRmVmssIpConfig 增加了 PublicIPPrefix 参数</span><span class="sxs-lookup"><span data-stu-id="a0f9a-159">Add PublicIPPrefix parameter to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="a0f9a-160">为 Invoke-AzureRmVMRunCommand cmdelt 增加了 ResourceId 参数</span><span class="sxs-lookup"><span data-stu-id="a0f9a-160">Add ResourceId parameter to Invoke-AzureRmVMRunCommand cmdelt</span></span>
* <span data-ttu-id="a0f9a-161">增加了 Invoke-AzureRmVmssVMRunCommand cmdlet</span><span class="sxs-lookup"><span data-stu-id="a0f9a-161">Add Invoke-AzureRmVmssVMRunCommand cmdlet</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="a0f9a-162">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="a0f9a-162">AzureRM.Dns</span></span>
* <span data-ttu-id="a0f9a-163">增加了在创建 dns 记录期间对别名记录的支持</span><span class="sxs-lookup"><span data-stu-id="a0f9a-163">Added support for alias record during dns record creation</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="a0f9a-164">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="a0f9a-164">AzureRM.Insights</span></span>
* <span data-ttu-id="a0f9a-165">修复了问题 #6833 和 #7102（诊断设置方面）</span><span class="sxs-lookup"><span data-stu-id="a0f9a-165">Fixed issues #6833 and #7102 (Diagnostic Settings area)</span></span>
    - <span data-ttu-id="a0f9a-166">在创建和列出/获取诊断设置期间出现的默认名称（即“service”）的问题</span><span class="sxs-lookup"><span data-stu-id="a0f9a-166">Issues with the default name, i.e. 'service', during creation and listing/getting of diagnostic settings</span></span>
    - <span data-ttu-id="a0f9a-167">通过类别创建诊断设置的问题</span><span class="sxs-lookup"><span data-stu-id="a0f9a-167">Issues creating diagnostic settings with categories</span></span>
* <span data-ttu-id="a0f9a-168">为指标时间粒度参数添加了弃用消息</span><span class="sxs-lookup"><span data-stu-id="a0f9a-168">Added deprecation message for metrics time grains parameters</span></span>
    - <span data-ttu-id="a0f9a-169">Timegrains 参数仍然会被接受（这是非重大变更），但在后端会被忽略，因为仅 PT1M 有效</span><span class="sxs-lookup"><span data-stu-id="a0f9a-169">Timegrains parameters are still being accepted (this is a non-breaking change,) but they are ignored in the backend since only PT1M is valid</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="a0f9a-170">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a0f9a-170">AzureRM.Network</span></span>
* <span data-ttu-id="a0f9a-171">更改了 LoadBalancer cmdlet</span><span class="sxs-lookup"><span data-stu-id="a0f9a-171">Changes to LoadBalancer cmdlets</span></span>
  - <span data-ttu-id="a0f9a-172">LoadBalancerInboundNatPoolConfig：增加了 IdleTimeoutInMinutes、EnableFloatingIp 和 EnableTcpReset 参数</span><span class="sxs-lookup"><span data-stu-id="a0f9a-172">LoadBalancerInboundNatPoolConfig: added parameters IdleTimeoutInMinutes, EnableFloatingIp and EnableTcpReset</span></span>
  - <span data-ttu-id="a0f9a-173">LoadBalancerInboundNatRuleConfig：增加了 EnableTcpReset 参数</span><span class="sxs-lookup"><span data-stu-id="a0f9a-173">LoadBalancerInboundNatRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="a0f9a-174">LoadBalancerRuleConfig：增加了 EnableTcpReset 参数</span><span class="sxs-lookup"><span data-stu-id="a0f9a-174">LoadBalancerRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="a0f9a-175">LoadBalancerProbeConfig：增加了对参数 Protocol 的“Https”值的支持</span><span class="sxs-lookup"><span data-stu-id="a0f9a-175">LoadBalancerProbeConfig: added support for value "Https" for parameter Protocol</span></span>
* <span data-ttu-id="a0f9a-176">为新 LoadBalancer 的子资源 OutboundRule 增加了新命令</span><span class="sxs-lookup"><span data-stu-id="a0f9a-176">Added new commands for new LoadBalancer's subresource OutboundRule</span></span>
  - <span data-ttu-id="a0f9a-177">Add-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a0f9a-177">Add-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="a0f9a-178">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a0f9a-178">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="a0f9a-179">New-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a0f9a-179">New-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="a0f9a-180">Set-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a0f9a-180">Set-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="a0f9a-181">Remove-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a0f9a-181">Remove-AzureRmLoadBalancerOutboundRuleConfig</span></span>
* <span data-ttu-id="a0f9a-182">为 PSNetworkInterface 增加了新的 HostedWorkloads 属性</span><span class="sxs-lookup"><span data-stu-id="a0f9a-182">Added new HostedWorkloads property for PSNetworkInterface</span></span>
* <span data-ttu-id="a0f9a-183">通过 ARM 为 Azure 防火墙功能增加了新的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="a0f9a-183">Added new cmdlets for feature: Azure Firewall via ARM</span></span>
  - <span data-ttu-id="a0f9a-184">增加了 Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="a0f9a-184">Added Get-AzureRmFirewall</span></span>
  - <span data-ttu-id="a0f9a-185">增加了 Set-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="a0f9a-185">Added Set-AzureRmFirewall</span></span>
  - <span data-ttu-id="a0f9a-186">增加了 New-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="a0f9a-186">Added New-AzureRmFirewall</span></span>
  - <span data-ttu-id="a0f9a-187">增加了 Remove-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="a0f9a-187">Added Remove-AzureRmFirewall</span></span>
  - <span data-ttu-id="a0f9a-188">增加了 New-AzureRmFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="a0f9a-188">Added New-AzureRmFirewallApplicationRuleCollection</span></span>
  - <span data-ttu-id="a0f9a-189">增加了 New-AzureRmFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="a0f9a-189">Added New-AzureRmFirewallApplicationRule</span></span>
  - <span data-ttu-id="a0f9a-190">增加了 New-AzureRmFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="a0f9a-190">Added New-AzureRmFirewallNatRuleCollection</span></span>
  - <span data-ttu-id="a0f9a-191">增加了 New-AzureRmFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="a0f9a-191">Added New-AzureRmFirewallNatRule</span></span>
  - <span data-ttu-id="a0f9a-192">增加了 New-AzureRmFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="a0f9a-192">Added New-AzureRmFirewallNetworkRuleCollection</span></span>
  - <span data-ttu-id="a0f9a-193">增加了 New-AzureRmFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a0f9a-193">Added New-AzureRmFirewallNetworkRule</span></span>
* <span data-ttu-id="a0f9a-194">在应用程序网关中增加了对受信任根证书和自动缩放配置的支持</span><span class="sxs-lookup"><span data-stu-id="a0f9a-194">Added support for Trusted Root certificate and Autoscale configuration in Application Gateway</span></span>
  - <span data-ttu-id="a0f9a-195">增加了新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="a0f9a-195">New Cmdlets added:</span></span>
      - <span data-ttu-id="a0f9a-196">Add-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="a0f9a-196">Add-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="a0f9a-197">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="a0f9a-197">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="a0f9a-198">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="a0f9a-198">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="a0f9a-199">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="a0f9a-199">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="a0f9a-200">Set-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="a0f9a-200">Set-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="a0f9a-201">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="a0f9a-201">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="a0f9a-202">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="a0f9a-202">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="a0f9a-203">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="a0f9a-203">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="a0f9a-204">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="a0f9a-204">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
  - <span data-ttu-id="a0f9a-205">使用可选参数 -TrustedRootCertificate 更新了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a0f9a-205">Cmdlets updated with optonal parameter -TrustedRootCertificate</span></span>
      - <span data-ttu-id="a0f9a-206">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a0f9a-206">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="a0f9a-207">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a0f9a-207">Set-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="a0f9a-208">New-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="a0f9a-208">New-AzureRmApplicationGatewayBackendHttpSetting</span></span>
      - <span data-ttu-id="a0f9a-209">Set-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="a0f9a-209">Set-AzureRmApplicationGatewayBackendHttpSetting</span></span>
  - <span data-ttu-id="a0f9a-210">使用可选参数 -AutoscaleConfiguration 更新了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a0f9a-210">Cmdlets updated with optonal parameter -AutoscaleConfiguration</span></span>
      - <span data-ttu-id="a0f9a-211">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a0f9a-211">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="a0f9a-212">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a0f9a-212">Set-AzureRmApplicationGateway</span></span>
* <span data-ttu-id="a0f9a-213">为接口终结点增加了 cmdlet Get-AzureInterfaceEndpoint</span><span class="sxs-lookup"><span data-stu-id="a0f9a-213">Add cmdlet for Interface Endpoint Get-AzureInterfaceEndpoint</span></span>
* <span data-ttu-id="a0f9a-214">在子网中增加了对多个地址前缀的支持。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-214">Added support for multiple address prefixes in a subnet.</span></span> <span data-ttu-id="a0f9a-215">更新了 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="a0f9a-215">Updated cmdlets:</span></span>
  - <span data-ttu-id="a0f9a-216">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a0f9a-216">New-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="a0f9a-217">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a0f9a-217">Set-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="a0f9a-218">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a0f9a-218">Add-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="a0f9a-219">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a0f9a-219">Get-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="a0f9a-220">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="a0f9a-220">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>
  - <span data-ttu-id="a0f9a-221">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="a0f9a-221">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="a0f9a-222">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="a0f9a-222">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="a0f9a-223">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="a0f9a-223">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="a0f9a-224">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="a0f9a-224">Add-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="a0f9a-225">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="a0f9a-225">New-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="a0f9a-226">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="a0f9a-226">Set-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="a0f9a-227">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="a0f9a-227">Add-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="a0f9a-228">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="a0f9a-228">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="a0f9a-229">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="a0f9a-229">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="a0f9a-230">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="a0f9a-230">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="a0f9a-231">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a0f9a-231">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="a0f9a-232">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a0f9a-232">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="a0f9a-233">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a0f9a-233">New-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="a0f9a-234">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="a0f9a-234">New-AzureRmNetworkInterface</span></span>
* <span data-ttu-id="a0f9a-235">增加了用于子网委派的 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-235">Adding cmdlets for subnet delegation.</span></span>
  - <span data-ttu-id="a0f9a-236">New-AzureRmDelegation：创建一个可以添加到子网的新委派</span><span class="sxs-lookup"><span data-stu-id="a0f9a-236">New-AzureRmDelegation: Creates a new delegation, which can be added to a subnet</span></span>
  - <span data-ttu-id="a0f9a-237">Remove-AzureRmDelegation：获取一个子网，然后从该子网中删除提供的委派名称</span><span class="sxs-lookup"><span data-stu-id="a0f9a-237">Remove-AzureRmDelegation: Takes in a subnet and removes the provided delegation name from that subnet</span></span>
  - <span data-ttu-id="a0f9a-238">Add-AzureRmDelegation：获取一个子网，然后向该子网添加提供的服务名称作为委派</span><span class="sxs-lookup"><span data-stu-id="a0f9a-238">Add-AzureRmDelegation: Takes in a subnet and adds the provided service name as a delegation to that subnet</span></span>
  - <span data-ttu-id="a0f9a-239">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="a0f9a-239">Get-AzureRmDelegation</span></span>
  - <span data-ttu-id="a0f9a-240">Get-AzureRmAvailableServiceDelegations</span><span class="sxs-lookup"><span data-stu-id="a0f9a-240">Get-AzureRmAvailableServiceDelegations</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="a0f9a-241">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="a0f9a-241">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="a0f9a-242">支持托管磁盘</span><span class="sxs-lookup"><span data-stu-id="a0f9a-242">Support for managed Managed disk</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="a0f9a-243">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="a0f9a-243">AzureRM.RedisCache</span></span>
* <span data-ttu-id="a0f9a-244">更新了 Insights 依赖项。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-244">Updated Insights dependency.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="a0f9a-245">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="a0f9a-245">AzureRM.Resources</span></span>
* <span data-ttu-id="a0f9a-246">使用新参数 RollbackAction 更新了 New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a0f9a-246">Update New-AzureRmResourceGroupDeployment with new parameter RollbackAction</span></span>
    - <span data-ttu-id="a0f9a-247">使用新参数增加了对 OnErrorDeployment 的支持。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-247">Add support for OnErrorDeployment with the new parameter.</span></span>
* <span data-ttu-id="a0f9a-248">在策略分配方面支持托管标识。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-248">Support managed identity on policy assignments.</span></span>
* <span data-ttu-id="a0f9a-249">使用“New-AzureRmPolicyAssignment”来分配策略时，不再需要带默认值的参数</span><span class="sxs-lookup"><span data-stu-id="a0f9a-249">Parameters with default values are no longer requred when assigning a policy with 'New-AzureRmPolicyAssignment'</span></span>
* <span data-ttu-id="a0f9a-250">增加了新的 cmdlet Get-AzureRmPolicyAlias，用于检索策略别名</span><span class="sxs-lookup"><span data-stu-id="a0f9a-250">Add new cmdlet Get-AzureRmPolicyAlias for retrieving policy aliases</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="a0f9a-251">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a0f9a-251">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="a0f9a-252">修复了问题 #7161</span><span class="sxs-lookup"><span data-stu-id="a0f9a-252">Fixed issue #7161</span></span>

#### <a name="azurermsignalr"></a><span data-ttu-id="a0f9a-253">AzureRM.SignalR</span><span class="sxs-lookup"><span data-stu-id="a0f9a-253">AzureRM.SignalR</span></span>
* <span data-ttu-id="a0f9a-254">将 SKU 名称更新为 Free_F1 和 Standard_S1</span><span class="sxs-lookup"><span data-stu-id="a0f9a-254">Update SKU names to Free_F1 and Standard_S1</span></span>
* <span data-ttu-id="a0f9a-255">为 PSSignalRResource 对象增加了版本字段，为 PSSignalRKeys 对象增加了字符串。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-255">Add version field to the PSSignalRResource object and connection string to the PSSignalRKeys object.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="a0f9a-256">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="a0f9a-256">AzureRM.Storage</span></span>
* <span data-ttu-id="a0f9a-257">在 AzureRm.Storage 中支持不可变性策略</span><span class="sxs-lookup"><span data-stu-id="a0f9a-257">Support Immutability Policy in AzureRm.Storage</span></span> 
    - <span data-ttu-id="a0f9a-258">Remove-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a0f9a-258">Remove-AzureRmStorageAccountNetworkRule</span></span>
    - <span data-ttu-id="a0f9a-259">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a0f9a-259">Get-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="a0f9a-260">Update-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a0f9a-260">Update-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="a0f9a-261">New-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a0f9a-261">New-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="a0f9a-262">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a0f9a-262">Remove-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="a0f9a-263">Add-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="a0f9a-263">Add-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="a0f9a-264">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="a0f9a-264">Remove-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="a0f9a-265">Set-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="a0f9a-265">Set-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="a0f9a-266">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="a0f9a-266">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="a0f9a-267">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="a0f9a-267">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="a0f9a-268">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="a0f9a-268">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="a0f9a-269">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="a0f9a-269">AzureRM.Websites</span></span>
* <span data-ttu-id="a0f9a-270">增加了两个新的 cmdlet：Get-AzureRmDeletedWebApp 和 Restore-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="a0f9a-270">Added two new cmdlets: Get-AzureRmDeletedWebApp and Restore-AzureRmDeletedWebApp</span></span>
* <span data-ttu-id="a0f9a-271">增加了 New-AzureRmAppServicePlan -HyperV 开关，用于通过 Windows 容器创建应用服务计划</span><span class="sxs-lookup"><span data-stu-id="a0f9a-271">New-AzureRmAppServicePlan -HyperV switch is added for create app service plan with windows container</span></span>
* <span data-ttu-id="a0f9a-272">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - 增加了新参数 (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment)，用于创建和管理 Windows 容器应用</span><span class="sxs-lookup"><span data-stu-id="a0f9a-272">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - New parameters (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) added for creating and managing windows container app</span></span>

## <a name="681---august-2018"></a><span data-ttu-id="a0f9a-273">6.8.1 - 2018 年 8 月</span><span class="sxs-lookup"><span data-stu-id="a0f9a-273">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="a0f9a-274">常规</span><span class="sxs-lookup"><span data-stu-id="a0f9a-274">General</span></span>
* <span data-ttu-id="a0f9a-275">解决了未设置默认资源组的问题。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-275">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="a0f9a-276">更新了公共运行时程序集</span><span class="sxs-lookup"><span data-stu-id="a0f9a-276">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="a0f9a-277">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a0f9a-277">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="a0f9a-278">解决了未设置默认资源组的问题。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-278">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="a0f9a-279">修复了问题 https://github.com/Azure/azure-powershell/issues/6603</span><span class="sxs-lookup"><span data-stu-id="a0f9a-279">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="a0f9a-280">Import-AzureRmApiManagementApi 和 \*-AzureRmApiManagementCertificate cmdlet 现在处理相对路径</span><span class="sxs-lookup"><span data-stu-id="a0f9a-280">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="a0f9a-281">修复了问题 https://github.com/Azure/azure-powershell/issues/6879</span><span class="sxs-lookup"><span data-stu-id="a0f9a-281">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="a0f9a-282">CertificateInformation 是使 Set-AzureRmApiManagement cmdlet 可以正常工作的可设置属性。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-282">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="a0f9a-283">通过升级到 4.0.4-preview nuget 进行了修复</span><span class="sxs-lookup"><span data-stu-id="a0f9a-283">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="a0f9a-284">修复了问题 https://github.com/Azure/azure-powershell/issues/6853</span><span class="sxs-lookup"><span data-stu-id="a0f9a-284">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="a0f9a-285">针对按产品名称进行的搜索修复了 Odata 筛选器</span><span class="sxs-lookup"><span data-stu-id="a0f9a-285">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="a0f9a-286">修复了问题 https://github.com/Azure/azure-powershell/issues/6814</span><span class="sxs-lookup"><span data-stu-id="a0f9a-286">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="a0f9a-287">针对按 API 名称进行的搜索修复了 Odata 筛选器</span><span class="sxs-lookup"><span data-stu-id="a0f9a-287">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="a0f9a-288">添加了对 AzureMonitor 记录器的支持</span><span class="sxs-lookup"><span data-stu-id="a0f9a-288">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="a0f9a-289">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a0f9a-289">AzureRM.Compute</span></span>
* <span data-ttu-id="a0f9a-290">解决了错误输出中缺少目标的问题。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-290">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="a0f9a-291">解决了带有托管磁盘的 VM 的存储帐户类型问题</span><span class="sxs-lookup"><span data-stu-id="a0f9a-291">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="a0f9a-292">解决了未设置默认资源组的问题。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-292">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="a0f9a-293">解决了在其他环境（例如 Azure 中国）中使用 AEM 扩展 cmdlet 的问题</span><span class="sxs-lookup"><span data-stu-id="a0f9a-293">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="a0f9a-294">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a0f9a-294">AzureRM.Network</span></span>
* <span data-ttu-id="a0f9a-295">将默认 cmdlet 输出表示形式更改为表视图</span><span class="sxs-lookup"><span data-stu-id="a0f9a-295">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="a0f9a-296">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="a0f9a-296">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="a0f9a-297">修复了在尝试扩展停用的容量时 Update-AzureRmPowerBIEmbeddedCapacity 中出现的故障</span><span class="sxs-lookup"><span data-stu-id="a0f9a-297">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="a0f9a-298">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="a0f9a-298">AzureRM.Resources</span></span>
* <span data-ttu-id="a0f9a-299">解决了从市场创建托管应用程序的问题。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-299">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="a0f9a-300">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a0f9a-300">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="a0f9a-301">修复的问题</span><span class="sxs-lookup"><span data-stu-id="a0f9a-301">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="a0f9a-302">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="a0f9a-302">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="a0f9a-303">添加了对 MultiValue 路由方法的支持</span><span class="sxs-lookup"><span data-stu-id="a0f9a-303">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="a0f9a-304">MultiValue 路由的新参数“MaxReturn”</span><span class="sxs-lookup"><span data-stu-id="a0f9a-304">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="a0f9a-305">添加了对 Subnet 路由方法的支持</span><span class="sxs-lookup"><span data-stu-id="a0f9a-305">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="a0f9a-306">对终结点中的 IP 地址范围（子网）的支持</span><span class="sxs-lookup"><span data-stu-id="a0f9a-306">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="a0f9a-307">添加了对配置文件中的自定义标头的支持</span><span class="sxs-lookup"><span data-stu-id="a0f9a-307">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="a0f9a-308">添加了对配置文件中的预期状态代码范围的支持</span><span class="sxs-lookup"><span data-stu-id="a0f9a-308">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="a0f9a-309">添加了对终结点中的自定义标头的支持</span><span class="sxs-lookup"><span data-stu-id="a0f9a-309">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="a0f9a-310">6.8.0 - 2018 年 8 月</span><span class="sxs-lookup"><span data-stu-id="a0f9a-310">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="a0f9a-311">常规</span><span class="sxs-lookup"><span data-stu-id="a0f9a-311">General</span></span>
* <span data-ttu-id="a0f9a-312">解决了未设置默认资源组的问题。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-312">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="a0f9a-313">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="a0f9a-313">AzureRM.Profile</span></span>
* <span data-ttu-id="a0f9a-314">为在执行 Connect-AzureRmAccount 期间返回的令牌添加了“过期”属性</span><span class="sxs-lookup"><span data-stu-id="a0f9a-314">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="a0f9a-315">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a0f9a-315">AzureRM.Compute</span></span>
* <span data-ttu-id="a0f9a-316">解决了错误输出中缺少目标的问题。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-316">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="a0f9a-317">解决了带有托管磁盘的 VM 的存储帐户类型问题</span><span class="sxs-lookup"><span data-stu-id="a0f9a-317">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="a0f9a-318">解决了在其他环境（例如 Azure 中国）中使用 AEM 扩展 cmdlet 的问题</span><span class="sxs-lookup"><span data-stu-id="a0f9a-318">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="a0f9a-319">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="a0f9a-319">AzureRM.IotHub</span></span>
* <span data-ttu-id="a0f9a-320">修复了 New-AzureRmIotHubExportDevices 和 New-AzureRmIotHubImportDevices的示例</span><span class="sxs-lookup"><span data-stu-id="a0f9a-320">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="a0f9a-321">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a0f9a-321">AzureRM.Network</span></span>
* <span data-ttu-id="a0f9a-322">将默认模型表示形式更改为表视图</span><span class="sxs-lookup"><span data-stu-id="a0f9a-322">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="a0f9a-323">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="a0f9a-323">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="a0f9a-324">修复了在尝试扩展停用的容量时 Update-AzureRmPowerBIEmbeddedCapacity 中出现的故障</span><span class="sxs-lookup"><span data-stu-id="a0f9a-324">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="a0f9a-325">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="a0f9a-325">AzureRM.Resources</span></span>
* <span data-ttu-id="a0f9a-326">解决了从市场创建托管应用程序的问题。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-326">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="a0f9a-327">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a0f9a-327">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="a0f9a-328">解决了以下问题</span><span class="sxs-lookup"><span data-stu-id="a0f9a-328">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="a0f9a-329">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="a0f9a-329">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="a0f9a-330">对 MultiValue 路由方法的支持</span><span class="sxs-lookup"><span data-stu-id="a0f9a-330">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="a0f9a-331">MultiValue 路由的新参数“MaxReturn”</span><span class="sxs-lookup"><span data-stu-id="a0f9a-331">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="a0f9a-332">对 Subnet 路由方法的支持</span><span class="sxs-lookup"><span data-stu-id="a0f9a-332">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="a0f9a-333">对终结点中的 IP 地址范围（子网）的支持</span><span class="sxs-lookup"><span data-stu-id="a0f9a-333">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="a0f9a-334">对配置文件中的自定义标头的支持</span><span class="sxs-lookup"><span data-stu-id="a0f9a-334">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="a0f9a-335">对配置文件中的预期状态代码范围的支持</span><span class="sxs-lookup"><span data-stu-id="a0f9a-335">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="a0f9a-336">对终结点中的自定义标头的支持</span><span class="sxs-lookup"><span data-stu-id="a0f9a-336">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="a0f9a-337">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="a0f9a-337">AzureRM.Websites</span></span>
* <span data-ttu-id="a0f9a-338">解决了错误地设置默认资源组的问题。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-338">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="a0f9a-339">6.7.0 - 2018 年 8 月</span><span class="sxs-lookup"><span data-stu-id="a0f9a-339">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="a0f9a-340">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="a0f9a-340">AzureRM.Profile</span></span>
* <span data-ttu-id="a0f9a-341">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-341">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="a0f9a-342">向默认的上下文名称添加用户 ID，避免上下文冲突</span><span class="sxs-lookup"><span data-stu-id="a0f9a-342">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="a0f9a-343">修复了 Clear-AzureRmContext 在选择上下文 #6398 时出现的问题</span><span class="sxs-lookup"><span data-stu-id="a0f9a-343">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="a0f9a-344">允许将租户域传递给“Connect-AzureRmAccount”的“-TenantId”参数</span><span class="sxs-lookup"><span data-stu-id="a0f9a-344">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="a0f9a-345">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="a0f9a-345">Azure.Storage</span></span>
* <span data-ttu-id="a0f9a-346">去除了 Azure 文件共享配额的 5TB 限制</span><span class="sxs-lookup"><span data-stu-id="a0f9a-346">Remove the 5TB limitation for Azure File Share quota</span></span>
- <span data-ttu-id="a0f9a-347">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="a0f9a-347">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="a0f9a-348">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a0f9a-348">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="a0f9a-349">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-349">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="a0f9a-350">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a0f9a-350">Azure.AnalysisServices</span></span>
* <span data-ttu-id="a0f9a-351">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-351">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="a0f9a-352">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a0f9a-352">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="a0f9a-353">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-353">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="a0f9a-354">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="a0f9a-354">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="a0f9a-355">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-355">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="a0f9a-356">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="a0f9a-356">AzureRM.Automation</span></span>
* <span data-ttu-id="a0f9a-357">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-357">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="a0f9a-358">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="a0f9a-358">AzureRM.Backup</span></span>
* <span data-ttu-id="a0f9a-359">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-359">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="a0f9a-360">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="a0f9a-360">AzureRM.Batch</span></span>
* <span data-ttu-id="a0f9a-361">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-361">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="a0f9a-362">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="a0f9a-362">AzureRM.Billing</span></span>
* <span data-ttu-id="a0f9a-363">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-363">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="a0f9a-364">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="a0f9a-364">AzureRM.Cdn</span></span>
* <span data-ttu-id="a0f9a-365">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-365">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="a0f9a-366">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a0f9a-366">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="a0f9a-367">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-367">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="a0f9a-368">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a0f9a-368">AzureRM.Compute</span></span>
* <span data-ttu-id="a0f9a-369">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-369">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="a0f9a-370">为 New-AzureRmVmssConfig 增加了 EvictionPolicy 参数</span><span class="sxs-lookup"><span data-stu-id="a0f9a-370">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="a0f9a-371">在 New-AzureRmVm 的 DiskFileParameterSet 中使用默认位置（如果未指定 Location）</span><span class="sxs-lookup"><span data-stu-id="a0f9a-371">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="a0f9a-372">修复了 Save-AzureRmVMImage 中的参数说明</span><span class="sxs-lookup"><span data-stu-id="a0f9a-372">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="a0f9a-373">修复了某些单次传递相关方案的 Get-AzureRmVMDiskEncryptionStatus cmdlet</span><span class="sxs-lookup"><span data-stu-id="a0f9a-373">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="a0f9a-374">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="a0f9a-374">AzureRM.Consumption</span></span>
* <span data-ttu-id="a0f9a-375">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-375">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="a0f9a-376">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="a0f9a-376">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="a0f9a-377">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-377">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="a0f9a-378">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a0f9a-378">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="a0f9a-379">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-379">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="a0f9a-380">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="a0f9a-380">AzureRM.DataFactories</span></span>
* <span data-ttu-id="a0f9a-381">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-381">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="a0f9a-382">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="a0f9a-382">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="a0f9a-383">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-383">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="a0f9a-384">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="a0f9a-384">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="a0f9a-385">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-385">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="a0f9a-386">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a0f9a-386">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="a0f9a-387">修复了从 PowerShell 命令行设置 DebugPreference 时的调试问题</span><span class="sxs-lookup"><span data-stu-id="a0f9a-387">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="a0f9a-388">更新了 Set-AzureRmDataLakeStoreItemAcl 的示例</span><span class="sxs-lookup"><span data-stu-id="a0f9a-388">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="a0f9a-389">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-389">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="a0f9a-390">更新了 Set-AzureRmDataLakeStoreItemAclEntry 的示例</span><span class="sxs-lookup"><span data-stu-id="a0f9a-390">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="a0f9a-391">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="a0f9a-391">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="a0f9a-392">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-392">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="a0f9a-393">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="a0f9a-393">AzureRM.Dns</span></span>
* <span data-ttu-id="a0f9a-394">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-394">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="a0f9a-395">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="a0f9a-395">AzureRM.EventGrid</span></span>
* <span data-ttu-id="a0f9a-396">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-396">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="a0f9a-397">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="a0f9a-397">AzureRM.EventHub</span></span>
* <span data-ttu-id="a0f9a-398">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-398">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="a0f9a-399">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a0f9a-399">AzureRM.HDInsight</span></span>
* <span data-ttu-id="a0f9a-400">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-400">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="a0f9a-401">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="a0f9a-401">AzureRM.Insights</span></span>
* <span data-ttu-id="a0f9a-402">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-402">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="a0f9a-403">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="a0f9a-403">AzureRM.IotHub</span></span>
* <span data-ttu-id="a0f9a-404">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-404">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="a0f9a-405">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a0f9a-405">AzureRM.KeyVault</span></span>
* <span data-ttu-id="a0f9a-406">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-406">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="a0f9a-407">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a0f9a-407">AzureRM.LogicApp</span></span>
* <span data-ttu-id="a0f9a-408">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-408">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="a0f9a-409">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="a0f9a-409">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="a0f9a-410">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-410">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="a0f9a-411">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="a0f9a-411">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="a0f9a-412">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-412">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="a0f9a-413">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="a0f9a-413">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="a0f9a-414">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-414">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="a0f9a-415">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="a0f9a-415">AzureRM.Media</span></span>
* <span data-ttu-id="a0f9a-416">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-416">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="a0f9a-417">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a0f9a-417">AzureRM.Network</span></span>
* <span data-ttu-id="a0f9a-418">增加了 Set-AzureRmLocalNetworkGateway 的示例</span><span class="sxs-lookup"><span data-stu-id="a0f9a-418">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="a0f9a-419">增加了 Add-AzureRmVirtualNetworkGatewayIpConfig、Get-AzureRmVirtualNetworkGatewayConnectionSharedKey 和 New-AzureRmVirtualNetworkGatewayConnection 的示例和说明</span><span class="sxs-lookup"><span data-stu-id="a0f9a-419">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="a0f9a-420">增加了 Remove-AzureRmVirtualNetworkGatewayIpConfig 和 Reset-AzureRmVirtualNetworkGateway 的示例</span><span class="sxs-lookup"><span data-stu-id="a0f9a-420">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="a0f9a-421">增加了 Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey 的示例</span><span class="sxs-lookup"><span data-stu-id="a0f9a-421">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="a0f9a-422">增加了 Set-AzureRmVirtualNetworkGatewayConnectionSharedKey 的示例</span><span class="sxs-lookup"><span data-stu-id="a0f9a-422">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="a0f9a-423">增加了 Set-AzureRmVirtualNetworkGatewayConnection 的示例</span><span class="sxs-lookup"><span data-stu-id="a0f9a-423">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="a0f9a-424">使用最新的代码生成器重新生成了 ApplicationSecurityGroup、RouteTable 和 Usage 的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="a0f9a-424">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="a0f9a-425">阐明了在尝试获取的子网不存在时 Get-AzureRmVirtualNetworkSubnetConfig 的错误消息</span><span class="sxs-lookup"><span data-stu-id="a0f9a-425">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="a0f9a-426">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="a0f9a-426">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="a0f9a-427">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-427">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="a0f9a-428">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a0f9a-428">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="a0f9a-429">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-429">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="a0f9a-430">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a0f9a-430">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="a0f9a-431">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-431">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="a0f9a-432">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="a0f9a-432">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="a0f9a-433">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-433">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="a0f9a-434">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a0f9a-434">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="a0f9a-435">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-435">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="a0f9a-436">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="a0f9a-436">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="a0f9a-437">为 Get-AzureRmRecoveryServicesBackItem cmdlet 增加了策略筛选器。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-437">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="a0f9a-438">此命令返回受给定策略 ID 保护的备份项的列表。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-438">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="a0f9a-439">已将 Microsoft.Azure.Management.RecoveryServices.Backup 更新到 3.0.0-preview 版本。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-439">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="a0f9a-440">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-440">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="a0f9a-441">为 Restore-AzureRmRecoveryServicesBackupItem 增加了 TargetResourceGroupName 参数。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-441">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="a0f9a-442">托管磁盘还原到的资源组。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-442">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="a0f9a-443">适用于包含托管磁盘的 VM 的备份。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-443">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="a0f9a-444">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="a0f9a-444">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="a0f9a-445">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-445">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="a0f9a-446">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="a0f9a-446">AzureRM.RedisCache</span></span>
* <span data-ttu-id="a0f9a-447">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-447">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="a0f9a-448">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="a0f9a-448">AzureRM.Relay</span></span>
* <span data-ttu-id="a0f9a-449">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-449">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="a0f9a-450">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="a0f9a-450">AzureRM.Resources</span></span>
* <span data-ttu-id="a0f9a-451">支持在订阅范围部署模板。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-451">Support template deployment at subscription scope.</span></span> <span data-ttu-id="a0f9a-452">增加了新 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="a0f9a-452">Add new Cmdlets:</span></span>
    - <span data-ttu-id="a0f9a-453">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="a0f9a-453">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="a0f9a-454">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="a0f9a-454">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="a0f9a-455">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="a0f9a-455">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="a0f9a-456">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="a0f9a-456">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="a0f9a-457">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="a0f9a-457">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="a0f9a-458">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="a0f9a-458">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="a0f9a-459">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="a0f9a-459">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="a0f9a-460">修复了在将上下文传递给 Set-AzureRmResource 时引发错误的问题</span><span class="sxs-lookup"><span data-stu-id="a0f9a-460">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="a0f9a-461">修复了 New-AzureRmResourceGroupDeployment 中的示例</span><span class="sxs-lookup"><span data-stu-id="a0f9a-461">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="a0f9a-462">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-462">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="a0f9a-463">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="a0f9a-463">AzureRM.Scheduler</span></span>
* <span data-ttu-id="a0f9a-464">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-464">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="a0f9a-465">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a0f9a-465">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="a0f9a-466">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-466">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="a0f9a-467">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a0f9a-467">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="a0f9a-468">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-468">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="a0f9a-469">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="a0f9a-469">AzureRM.Sql</span></span>
* <span data-ttu-id="a0f9a-470">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-470">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="a0f9a-471">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="a0f9a-471">AzureRM.Storage</span></span>
* <span data-ttu-id="a0f9a-472">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-472">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="a0f9a-473">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="a0f9a-473">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="a0f9a-474">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-474">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="a0f9a-475">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="a0f9a-475">AzureRM.Tags</span></span>
* <span data-ttu-id="a0f9a-476">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-476">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="a0f9a-477">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="a0f9a-477">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="a0f9a-478">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-478">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="a0f9a-479">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="a0f9a-479">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="a0f9a-480">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-480">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="a0f9a-481">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="a0f9a-481">AzureRM.Websites</span></span>
* <span data-ttu-id="a0f9a-482">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-482">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="a0f9a-483">6.6.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="a0f9a-483">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="a0f9a-484">常规</span><span class="sxs-lookup"><span data-stu-id="a0f9a-484">General</span></span>
* <span data-ttu-id="a0f9a-485">更新了所有帮助文件，以包括完整参数类型和正确的输入/输出类型。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-485">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="a0f9a-486">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="a0f9a-486">AzureRM.Profile</span></span>
* <span data-ttu-id="a0f9a-487">更新了 Common.Strategy 库，以便能够验证资源的当前配置是否与目标资源兼容。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-487">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="a0f9a-488">在 Common.Storage 中添加了 ps1xml 类型</span><span class="sxs-lookup"><span data-stu-id="a0f9a-488">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="a0f9a-489">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="a0f9a-489">Azure.Storage</span></span>
* <span data-ttu-id="a0f9a-490">增加了从 DefaultProfile 获取存储上下文的支持</span><span class="sxs-lookup"><span data-stu-id="a0f9a-490">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="a0f9a-491">为 cmdlet 输出类型属性增加了 Ps1XmlAttribute。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-491">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="a0f9a-492">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a0f9a-492">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="a0f9a-493">修复了问题 https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="a0f9a-493">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="a0f9a-494">修复了 Automapper 中将 PsApiManagementApi 转换为 ApiContract 的 bug</span><span class="sxs-lookup"><span data-stu-id="a0f9a-494">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="a0f9a-495">修复了问题 https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="a0f9a-495">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="a0f9a-496">修复了 File.Save 中没有使用编码类型重载的 bug</span><span class="sxs-lookup"><span data-stu-id="a0f9a-496">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="a0f9a-497">修复了问题 https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="a0f9a-497">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="a0f9a-498">升级到了 4.0.3 Nuget版本，该版本修复了 apiId 上的模式异常</span><span class="sxs-lookup"><span data-stu-id="a0f9a-498">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="a0f9a-499">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a0f9a-499">AzureRM.Compute</span></span>
* <span data-ttu-id="a0f9a-500">修复因使用 PremiumLRS 存储帐户类型重命名而在 New-AzureRmVm 中使用 DiskFileParameterSet 创建 VM 失败的问题。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-500">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="a0f9a-501">修复 Invoke-AzureRmVMRunCommand cmdlet</span><span class="sxs-lookup"><span data-stu-id="a0f9a-501">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="a0f9a-502">更新 Get-AzureRmAvailabilitySet 以启用列出订阅中的所有可用性集。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-502">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="a0f9a-503">（ResouceGroupName 参数现在是可选的。）</span><span class="sxs-lookup"><span data-stu-id="a0f9a-503">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="a0f9a-504">更新“New-AzureRmVm”的 SimpleParameterSet 以在符合条件的 VM 上启用加速网络。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-504">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="a0f9a-505">将 New-AzureRmVmss 简单参数集更新为在用户指定的 LB 已存在时创建 vmss 失败。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-505">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="a0f9a-506">更新 New-AzureRmDisk 的示例</span><span class="sxs-lookup"><span data-stu-id="a0f9a-506">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="a0f9a-507">添加“New-AzureRmVM”的示例</span><span class="sxs-lookup"><span data-stu-id="a0f9a-507">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="a0f9a-508">更新 Set-AzureRmVMOSDisk 的说明</span><span class="sxs-lookup"><span data-stu-id="a0f9a-508">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="a0f9a-509">更新 Set-AzureRmVMBginfoExtension 的示例 1 以更正拼写和前缀。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-509">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="a0f9a-510">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="a0f9a-510">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="a0f9a-511">将 ADF .Net SDK 版本更新为 1.1.0。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-511">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="a0f9a-512">支持跨数据工厂的自承载集成运行时共享。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-512">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="a0f9a-513">将新参数 -SharedIntegrationRuntimeResourceId 添加到 Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-513">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="a0f9a-514">将新的可选参数 -LinkedDataFactoryName 添加到 Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-514">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="a0f9a-515">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a0f9a-515">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="a0f9a-516">将数据平面 SDK (Microsoft.Azure.DataLake.Store) 版本更新为 1.1.9</span><span class="sxs-lookup"><span data-stu-id="a0f9a-516">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="a0f9a-517">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="a0f9a-517">AzureRM.EventHub</span></span>
* <span data-ttu-id="a0f9a-518">在删除 cmdlet 中更新了 InputObject 和 ResourceId 的管道</span><span class="sxs-lookup"><span data-stu-id="a0f9a-518">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="a0f9a-519">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="a0f9a-519">AzureRM.Insights</span></span>
* <span data-ttu-id="a0f9a-520">修复了帮助文件中 OutputType 的格式问题</span><span class="sxs-lookup"><span data-stu-id="a0f9a-520">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="a0f9a-521">使用 Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span><span class="sxs-lookup"><span data-stu-id="a0f9a-521">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="a0f9a-522">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a0f9a-522">AzureRM.KeyVault</span></span>
* <span data-ttu-id="a0f9a-523">修复了 Set-AzureRmKeyVaultAccessPolicy 中的管道问题</span><span class="sxs-lookup"><span data-stu-id="a0f9a-523">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="a0f9a-524">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a0f9a-524">AzureRM.Network</span></span>
* <span data-ttu-id="a0f9a-525">添加了 LoadBalancerInboundNatPoolConfig cmdlet 的示例。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-525">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="a0f9a-526">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="a0f9a-526">AzureRM.Resources</span></span>
* <span data-ttu-id="a0f9a-527">修复了为“Get-AzureRmResource”同时提供标记名称和值时出现的问题</span><span class="sxs-lookup"><span data-stu-id="a0f9a-527">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="a0f9a-528">使用“Set-AzureRmResource”修复管道方案</span><span class="sxs-lookup"><span data-stu-id="a0f9a-528">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="a0f9a-529">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a0f9a-529">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="a0f9a-530">在删除 cmdlet 中更新了 InputObject 和 ResourceId 的管道</span><span class="sxs-lookup"><span data-stu-id="a0f9a-530">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="a0f9a-531">修复了几个问题</span><span class="sxs-lookup"><span data-stu-id="a0f9a-531">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="a0f9a-532">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="a0f9a-532">AzureRM.Sql</span></span>
* <span data-ttu-id="a0f9a-533">使用以下 cmdlet 添加服务器高级威胁防护支持：</span><span class="sxs-lookup"><span data-stu-id="a0f9a-533">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="a0f9a-534">Enable-AzureRmSqlServerAdvancedThreatProtection；Disable-AzureRmSqlServerAdvancedThreatProtection；Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="a0f9a-534">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="a0f9a-535">使用以下 cmdlet 添加漏洞评估支持：</span><span class="sxs-lookup"><span data-stu-id="a0f9a-535">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="a0f9a-536">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings；Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings；Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="a0f9a-536">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="a0f9a-537">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline；Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline；Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="a0f9a-537">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="a0f9a-538">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan；Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord；Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="a0f9a-538">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="a0f9a-539">修复了 Remove-AzureRmSqlServerFirewallRule 中的示例</span><span class="sxs-lookup"><span data-stu-id="a0f9a-539">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="a0f9a-540">修复了 Get-AzureSqlSyncGroupLog 中非美国基础文化的日期时间处理错误</span><span class="sxs-lookup"><span data-stu-id="a0f9a-540">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="a0f9a-541">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="a0f9a-541">AzureRM.Storage</span></span>
* <span data-ttu-id="a0f9a-542">将 Ps1XmlAttribute 添加到 cmdlet 输出类型属性</span><span class="sxs-lookup"><span data-stu-id="a0f9a-542">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="a0f9a-543">在表视图中显示 StorageAccount cmdlet 输出</span><span class="sxs-lookup"><span data-stu-id="a0f9a-543">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="a0f9a-544">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a0f9a-544">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="a0f9a-545">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a0f9a-545">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="a0f9a-546">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a0f9a-546">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="a0f9a-547">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="a0f9a-547">AzureRM.Tags</span></span>
* <span data-ttu-id="a0f9a-548">从 Tag cmdlet 帮助中删除不正确的语句</span><span class="sxs-lookup"><span data-stu-id="a0f9a-548">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="a0f9a-549">6.5.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="a0f9a-549">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="a0f9a-550">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="a0f9a-550">AzureRM.Profile</span></span>
* <span data-ttu-id="a0f9a-551">更新了“Get-AzureRmContextAutosaveSetting”的帮助</span><span class="sxs-lookup"><span data-stu-id="a0f9a-551">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="a0f9a-552">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="a0f9a-552">Azure.Storage</span></span>
* <span data-ttu-id="a0f9a-553">支持使用只写 Sas 令牌上传 Blob 或文件</span><span class="sxs-lookup"><span data-stu-id="a0f9a-553">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="a0f9a-554">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a0f9a-554">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="a0f9a-555">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="a0f9a-555">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="a0f9a-556">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a0f9a-556">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="a0f9a-557">将所需属性 ResourceGroupName 添加到 AS。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-557">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="a0f9a-558">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="a0f9a-558">AzureRM.Automation</span></span>
* <span data-ttu-id="a0f9a-559">更新帮助并添加“New-AzureRMAutomationSchedule”的示例</span><span class="sxs-lookup"><span data-stu-id="a0f9a-559">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="a0f9a-560">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a0f9a-560">AzureRM.Compute</span></span>
* <span data-ttu-id="a0f9a-561">将 -Tag 参数添加到 Update/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="a0f9a-561">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="a0f9a-562">添加“Add-AzureRmVmssExtension”的示例</span><span class="sxs-lookup"><span data-stu-id="a0f9a-562">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="a0f9a-563">添加“Remove-AzureRmVmssExtension”的示例</span><span class="sxs-lookup"><span data-stu-id="a0f9a-563">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="a0f9a-564">更新“Set-AzureRmVMAccessExtension”的帮助</span><span class="sxs-lookup"><span data-stu-id="a0f9a-564">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="a0f9a-565">更新 New-AzureRmVmss 的 SimpleParameterSet，以默认情况下将 SinglePlacementGroup 设置为false，并添加开关参数“SinglePlacementGroup”，使用户能够在单个放置组中创建 VMSS。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-565">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="a0f9a-566">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="a0f9a-566">AzureRM.EventHub</span></span>
* <span data-ttu-id="a0f9a-567">向 PSEventHubDRConfigurationAttributes 类添加了一个只读属性“PendingReplicationOperationsCount”，该属性在复制过程中为挂起的复制操作计数</span><span class="sxs-lookup"><span data-stu-id="a0f9a-567">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="a0f9a-568">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a0f9a-568">AzureRM.KeyVault</span></span>
* <span data-ttu-id="a0f9a-569">更新了 Set-AzureRmKeyVaultAccessPolicy 的错误消息</span><span class="sxs-lookup"><span data-stu-id="a0f9a-569">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="a0f9a-570">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a0f9a-570">AzureRM.LogicApp</span></span>
* <span data-ttu-id="a0f9a-571">修复了 New-AzureRmLogicApp 中的“无法解析参数集”错误</span><span class="sxs-lookup"><span data-stu-id="a0f9a-571">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="a0f9a-572">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a0f9a-572">AzureRM.Network</span></span>
* <span data-ttu-id="a0f9a-573">在多个租户中为 Set/Add-AzureRmVirtualNetworkPeering 启用跨虚拟网络对等互连</span><span class="sxs-lookup"><span data-stu-id="a0f9a-573">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="a0f9a-574">针对应用程序网关更新了以下 cmdlet</span><span class="sxs-lookup"><span data-stu-id="a0f9a-574">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="a0f9a-575">New-AzureRmApplicationGateway：添加了 EnableFIPS 标志和区域支持</span><span class="sxs-lookup"><span data-stu-id="a0f9a-575">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="a0f9a-576">New-AzureRmApplicationGatewaySku：添加了新的 sku Standard_v2 和 WAF_v2</span><span class="sxs-lookup"><span data-stu-id="a0f9a-576">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="a0f9a-577">Set-AzureRmApplicationGatewaySku：添加了新的 sku Standard_v2 和 WAF_v2</span><span class="sxs-lookup"><span data-stu-id="a0f9a-577">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="a0f9a-578">使用最新的生成器版本重新生成了 RouteTable cmdlet</span><span class="sxs-lookup"><span data-stu-id="a0f9a-578">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="a0f9a-579">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="a0f9a-579">AzureRM.Relay</span></span>
* <span data-ttu-id="a0f9a-580">更新了 Markdown 文件，其中修复了示例中的参数名称问题</span><span class="sxs-lookup"><span data-stu-id="a0f9a-580">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="a0f9a-581">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="a0f9a-581">AzureRM.Resources</span></span>
* <span data-ttu-id="a0f9a-582">更新了 Roleassignment 和 roledefinition cmdlet：</span><span class="sxs-lookup"><span data-stu-id="a0f9a-582">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="a0f9a-583">删除了作为分页的一部分完成的额外 roledefinition 调用。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-583">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="a0f9a-584">修复了 Get-AzureRmRoleAssignment cmdlet</span><span class="sxs-lookup"><span data-stu-id="a0f9a-584">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="a0f9a-585">修复了 -ExpandPrincipalGroups 命令参数功能</span><span class="sxs-lookup"><span data-stu-id="a0f9a-585">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="a0f9a-586">修复了“Get-AzureRmResource”的问题，其中“-ResourceType”参数区分大小写</span><span class="sxs-lookup"><span data-stu-id="a0f9a-586">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="a0f9a-587">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a0f9a-587">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="a0f9a-588">向列表 cmdlet 添加了 top 和 skip 参数</span><span class="sxs-lookup"><span data-stu-id="a0f9a-588">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="a0f9a-589">添加了标准到高级命名空间迁移 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="a0f9a-589">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="a0f9a-590">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="a0f9a-590">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="a0f9a-591">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="a0f9a-591">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="a0f9a-592">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="a0f9a-592">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="a0f9a-593">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="a0f9a-593">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="a0f9a-594">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="a0f9a-594">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="a0f9a-595">向 PSServiceBusDRConfigurationAttributes 类添加了一个只读属性“PendingReplicationOperationsCount”，该属性在复制过程中为挂起的复制操作计数</span><span class="sxs-lookup"><span data-stu-id="a0f9a-595">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="a0f9a-596">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a0f9a-596">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="a0f9a-597">更新了“New-AzureRmServiceFabricCluster”的示例</span><span class="sxs-lookup"><span data-stu-id="a0f9a-597">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="a0f9a-598">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="a0f9a-598">AzureRM.Sql</span></span>
* <span data-ttu-id="a0f9a-599">为 Management.Sql 添加新的 Cmdlet，以允许客户将 TDE 证书添加到 Sql Server 实例或托管实例</span><span class="sxs-lookup"><span data-stu-id="a0f9a-599">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="a0f9a-600">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="a0f9a-600">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="a0f9a-601">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="a0f9a-601">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="a0f9a-602">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="a0f9a-602">AzureRM.Websites</span></span>
* <span data-ttu-id="a0f9a-603">设置为 false 时，`Set-AzureRmWebApp -AssignIdentity` 和 `Set-AzureRmWebAppSlot -AssignIdentity` 现在将从站点对象中删除 Identity 属性。同时移除预览标记。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-603">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="a0f9a-604">`Get-AzureRmWebAppMetrics`、`Get-AzureRmAppServicePlanMetrics` 示例已更新</span><span class="sxs-lookup"><span data-stu-id="a0f9a-604">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="a0f9a-605">`Set-AzureRmWebApp -PhpVersion` 支持 off 作为有效的 php 版本</span><span class="sxs-lookup"><span data-stu-id="a0f9a-605">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="a0f9a-606">6.4.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="a0f9a-606">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="a0f9a-607">常规</span><span class="sxs-lookup"><span data-stu-id="a0f9a-607">General</span></span>
* <span data-ttu-id="a0f9a-608">修复了大多数模块的帮助文件中的 OutputType 格式问题</span><span class="sxs-lookup"><span data-stu-id="a0f9a-608">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="a0f9a-609">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="a0f9a-609">AzureRM.Profile</span></span>
* <span data-ttu-id="a0f9a-610">已将 Ps1Xml 属性添加到基本输出类型</span><span class="sxs-lookup"><span data-stu-id="a0f9a-610">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="a0f9a-611">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a0f9a-611">AzureRM.Compute</span></span>
* <span data-ttu-id="a0f9a-612">VMSS 的 IP 标记功能</span><span class="sxs-lookup"><span data-stu-id="a0f9a-612">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="a0f9a-613">已添加“New-AzureRmVmssIpTagConfig”cmdlet</span><span class="sxs-lookup"><span data-stu-id="a0f9a-613">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="a0f9a-614">已将 IpTag 参数添加到 New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="a0f9a-614">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="a0f9a-615">VMSS 的自动 OS 回滚功能</span><span class="sxs-lookup"><span data-stu-id="a0f9a-615">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="a0f9a-616">已将 DisableAutoRollback 参数添加到 New-AzureRmVmssConfig 和 Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a0f9a-616">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="a0f9a-617">VMSS 的 OS 升级历史记录功能</span><span class="sxs-lookup"><span data-stu-id="a0f9a-617">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="a0f9a-618">已将 OSUpgradeHistory 开关参数添加到 Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a0f9a-618">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="a0f9a-619">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="a0f9a-619">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="a0f9a-620">通过以下命令添加目录 ACL 的支持：</span><span class="sxs-lookup"><span data-stu-id="a0f9a-620">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="a0f9a-621">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="a0f9a-621">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="a0f9a-622">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="a0f9a-622">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="a0f9a-623">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="a0f9a-623">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="a0f9a-624">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a0f9a-624">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="a0f9a-625">为 Set-AzureRmDataLakeStoreItemAclEntry、Remove-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAcl 添加了取消支持和进度跟踪</span><span class="sxs-lookup"><span data-stu-id="a0f9a-625">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="a0f9a-626">为 Export-AzureRmDataLakeStoreChildItemProperties 添加了取消支持</span><span class="sxs-lookup"><span data-stu-id="a0f9a-626">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="a0f9a-627">修复了执行递归操作的 cmdlet 的调试消息刷新</span><span class="sxs-lookup"><span data-stu-id="a0f9a-627">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="a0f9a-628">修复了 DataLake cmdlet 的测试位置</span><span class="sxs-lookup"><span data-stu-id="a0f9a-628">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="a0f9a-629">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="a0f9a-629">AzureRM.EventHub</span></span>
* <span data-ttu-id="a0f9a-630">已将可选的 MaxCount 参数添加到“列出操作”cmdlet Get-AzureRmEventHub 和 Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="a0f9a-630">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="a0f9a-631">修复了 New-AzureRmEventHub cmdlet 的问题：创建新事件中心时至少需要一个参数。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-631">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="a0f9a-632">提供了默认参数集。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-632">Provided Default Parameter set.</span></span>
* <span data-ttu-id="a0f9a-633">已将可选参数 -KeyValue 添加到 New-AzureRmEventHubKey cmdlet，该参数可让用户提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-633">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="a0f9a-634">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a0f9a-634">AzureRM.KeyVault</span></span>
* <span data-ttu-id="a0f9a-635">修复了 Get-AzureRmKeyVault -Tag 返回所有资源的问题</span><span class="sxs-lookup"><span data-stu-id="a0f9a-635">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="a0f9a-636">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a0f9a-636">AzureRM.Network</span></span>
* <span data-ttu-id="a0f9a-637">为区域冗余的 VirtualNetworkGateways 公开新 SKU</span><span class="sxs-lookup"><span data-stu-id="a0f9a-637">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="a0f9a-638">通过 ARM 为以下功能添加了新命令：ExpressRoute 合作伙伴 API</span><span class="sxs-lookup"><span data-stu-id="a0f9a-638">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="a0f9a-639">添加了 Get-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="a0f9a-639">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="a0f9a-640">添加了 Set-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="a0f9a-640">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="a0f9a-641">添加了 Add-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="a0f9a-641">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="a0f9a-642">添加了 Get-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="a0f9a-642">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="a0f9a-643">添加了 Remove-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="a0f9a-643">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="a0f9a-644">添加了 Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="a0f9a-644">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="a0f9a-645">添加了 Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="a0f9a-645">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="a0f9a-646">添加了 Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="a0f9a-646">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="a0f9a-647">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="a0f9a-647">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="a0f9a-648">添加了 Get-AzureRmRecoveryServicesBackupStatus cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-648">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="a0f9a-649">此 cmdlet 采用 VM ID，并检查 VM 是否受订阅中的某个保管库保护。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-649">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="a0f9a-650">如果存在此类保管库，该 cmdlet 会输出该保管库的详细信息。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-650">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="a0f9a-651">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="a0f9a-651">AzureRM.Resources</span></span>
* <span data-ttu-id="a0f9a-652">更新了 Get-AzureRmPolicyAssignment cmdlet：</span><span class="sxs-lookup"><span data-stu-id="a0f9a-652">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="a0f9a-653">添加了在管理组级别列出 -Scope 值的支持</span><span class="sxs-lookup"><span data-stu-id="a0f9a-653">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="a0f9a-654">添加了在管理组级别使用 -Scope 值检索单个分配的支持</span><span class="sxs-lookup"><span data-stu-id="a0f9a-654">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="a0f9a-655">已将 -Effective 和 -All 开关添加到 control 参数</span><span class="sxs-lookup"><span data-stu-id="a0f9a-655">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="a0f9a-656">更新了 Get/New/Remove/Set-AzureRmPolicyDefinition cmdlet</span><span class="sxs-lookup"><span data-stu-id="a0f9a-656">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="a0f9a-657">添加了 -ManagementGroupName 参数，以将操作应用到给定的管理组</span><span class="sxs-lookup"><span data-stu-id="a0f9a-657">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="a0f9a-658">添加了 -SubscriptionId 参数，以将操作应用到给定的订阅</span><span class="sxs-lookup"><span data-stu-id="a0f9a-658">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="a0f9a-659">更新了 Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlet</span><span class="sxs-lookup"><span data-stu-id="a0f9a-659">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="a0f9a-660">添加了 -ManagementGroupName 参数，以将操作应用到给定的管理组</span><span class="sxs-lookup"><span data-stu-id="a0f9a-660">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="a0f9a-661">添加了 -SubscriptionId 参数，以将操作应用到给定的订阅</span><span class="sxs-lookup"><span data-stu-id="a0f9a-661">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="a0f9a-662">添加了使用 TemplateParameterObject 时在参数中指定 KeyVault 机密引用的支持</span><span class="sxs-lookup"><span data-stu-id="a0f9a-662">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="a0f9a-663">修复了忽略“New-AzureRmADAppCredential”的“-EndDate”参数的问题</span><span class="sxs-lookup"><span data-stu-id="a0f9a-663">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="a0f9a-664">修复了“Add-AzureRmADGroupMember”使用错误的 URL 发出请求的问题</span><span class="sxs-lookup"><span data-stu-id="a0f9a-664">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="a0f9a-665">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a0f9a-665">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="a0f9a-666">已将可选参数 -KeyValue 添加到 New-AzureRmServiceBusKey cmdlet，该参数可让用户提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-666">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="a0f9a-667">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="a0f9a-667">AzureRM.Sql</span></span>
* <span data-ttu-id="a0f9a-668">在 AzureRmSqlDatabaseRestorePoint 帮助中澄清了 SQLDW 的用户定义还原点</span><span class="sxs-lookup"><span data-stu-id="a0f9a-668">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="a0f9a-669">更新了多个 cmdlet 中 -ComputeGeneration 参数的文档</span><span class="sxs-lookup"><span data-stu-id="a0f9a-669">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="a0f9a-670">6.3.0 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="a0f9a-670">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="a0f9a-671">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="a0f9a-671">AzureRM.Profile</span></span>
* <span data-ttu-id="a0f9a-672">更新了 Enable-AzureRmContextAutoSave 的错误消息</span><span class="sxs-lookup"><span data-stu-id="a0f9a-672">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="a0f9a-673">在运行没有旧上下文的“Connect-AzureRmAccount”时为每个订阅创建一个上下文</span><span class="sxs-lookup"><span data-stu-id="a0f9a-673">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="a0f9a-674">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="a0f9a-674">Azure.Storage</span></span>
* <span data-ttu-id="a0f9a-675">在帮助文件中增加了关于 -Permissions 参数的其他信息。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-675">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="a0f9a-676">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a0f9a-676">AzureRM.Compute</span></span>
* <span data-ttu-id="a0f9a-677">“Get-AzureRmVmDiskEncryptionStatus”修复了一个针对没有数据磁盘的 VM 观察到的问题</span><span class="sxs-lookup"><span data-stu-id="a0f9a-677">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="a0f9a-678">更新计算客户端库版本以修复以下 cmdlet</span><span class="sxs-lookup"><span data-stu-id="a0f9a-678">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="a0f9a-679">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="a0f9a-679">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="a0f9a-680">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="a0f9a-680">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="a0f9a-681">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="a0f9a-681">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="a0f9a-682">修复了以下 cmdlet，因此可以正确地显示“操作 ID”和“操作状态”：</span><span class="sxs-lookup"><span data-stu-id="a0f9a-682">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="a0f9a-683">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a0f9a-683">Start-AzureRmVM</span></span>
    - <span data-ttu-id="a0f9a-684">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a0f9a-684">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="a0f9a-685">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a0f9a-685">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="a0f9a-686">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a0f9a-686">Set-AzureRmVM</span></span>
    - <span data-ttu-id="a0f9a-687">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="a0f9a-687">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="a0f9a-688">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a0f9a-688">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="a0f9a-689">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="a0f9a-689">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="a0f9a-690">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="a0f9a-690">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="a0f9a-691">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a0f9a-691">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="a0f9a-692">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a0f9a-692">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="a0f9a-693">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a0f9a-693">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="a0f9a-694">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a0f9a-694">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="a0f9a-695">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="a0f9a-695">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="a0f9a-696">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="a0f9a-696">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="a0f9a-697">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="a0f9a-697">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="a0f9a-698">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="a0f9a-698">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="a0f9a-699">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="a0f9a-699">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="a0f9a-700">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="a0f9a-700">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="a0f9a-701">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="a0f9a-701">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="a0f9a-702">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="a0f9a-702">AzureRM.EventGrid</span></span>
* <span data-ttu-id="a0f9a-703">在 Update-AzureRmEventGridSubscription cmdlet 中删除 SubjectBeginsWith/SubjectEndsWith 的 ValidateNotNullOrEmpty 验证条件，允许根据需要将这些参数更改为空字符串。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-703">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="a0f9a-704">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a0f9a-704">AzureRM.KeyVault</span></span>
* <span data-ttu-id="a0f9a-705">修复运行 Get-AzureRmKeyVault -Tag 时不返回任何标记的问题</span><span class="sxs-lookup"><span data-stu-id="a0f9a-705">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="a0f9a-706">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a0f9a-706">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="a0f9a-707">策略见解 cmdlet 的公开发行版</span><span class="sxs-lookup"><span data-stu-id="a0f9a-707">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="a0f9a-708">使用 API 版本 2018-04-04</span><span class="sxs-lookup"><span data-stu-id="a0f9a-708">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="a0f9a-709">向 Get-AzureRmPolicyStateSummary 的结果添加了 PolicyDefinitionReferenceId</span><span class="sxs-lookup"><span data-stu-id="a0f9a-709">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="a0f9a-710">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="a0f9a-710">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="a0f9a-711">向 RecoveryServices.Backup cmdlet 添加了 -Vault 参数。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-711">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="a0f9a-712">传递时，此项会替代 Set-AzureRmRecoveryServicesContext cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-712">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="a0f9a-713">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="a0f9a-713">AzureRM.Sql</span></span>
* <span data-ttu-id="a0f9a-714">更新了 Get-AzureRmSqlDatabaseExpanded 的帮助文件中的示例</span><span class="sxs-lookup"><span data-stu-id="a0f9a-714">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="a0f9a-715">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="a0f9a-715">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="a0f9a-716">更新了 Add-AzureRmTrafficManagerEndpointConfig 的帮助文件</span><span class="sxs-lookup"><span data-stu-id="a0f9a-716">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="a0f9a-717">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="a0f9a-717">AzureRM.Websites</span></span>
* <span data-ttu-id="a0f9a-718">更新了“Set-AzureRmWebApp”，在使用 -AssignIdentity 时不覆盖 AppSettings</span><span class="sxs-lookup"><span data-stu-id="a0f9a-718">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="a0f9a-719">更新了“New-AzureRmWebAppSlot”，允许使用 AppServicePlan 作为可选参数</span><span class="sxs-lookup"><span data-stu-id="a0f9a-719">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="a0f9a-720">6.2.1 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="a0f9a-720">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="a0f9a-721">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a0f9a-721">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="a0f9a-722">更新了 PSWorkspace 模型，允许 Network 使用 type 作为参数</span><span class="sxs-lookup"><span data-stu-id="a0f9a-722">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="a0f9a-723">6.2.0 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="a0f9a-723">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="a0f9a-724">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="a0f9a-724">AzureRM.Profile</span></span>
* <span data-ttu-id="a0f9a-725">修复了 Newtonsoft.Json 的版本 10.0.3 在模块导入时无法加载的问题</span><span class="sxs-lookup"><span data-stu-id="a0f9a-725">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="a0f9a-726">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a0f9a-726">AzureRM.Compute</span></span>
* <span data-ttu-id="a0f9a-727">VMSS VM 更新功能</span><span class="sxs-lookup"><span data-stu-id="a0f9a-727">VMSS VM Update feature</span></span>
    - <span data-ttu-id="a0f9a-728">增加了“Update-AzureRmVmssVM”和“New-AzureRmVMDataDisk”cmdlet</span><span class="sxs-lookup"><span data-stu-id="a0f9a-728">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="a0f9a-729">为“Add-AzureRmVMDataDisk”cmdlet 增加了 VirtualMachineScaleSetVM 参数，支持向 Vmss VM 添加数据磁盘。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-729">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="a0f9a-730">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="a0f9a-730">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="a0f9a-731">将 ADF.Net SDK 版本更新到了 0.8.0-preview，其中包含以下更改：</span><span class="sxs-lookup"><span data-stu-id="a0f9a-731">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="a0f9a-732">增加了“配置工厂存储库”操作</span><span class="sxs-lookup"><span data-stu-id="a0f9a-732">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="a0f9a-733">更新了 QuickBooks LinkedService，可以公开 consumerKey 和 consumerSecret 属性</span><span class="sxs-lookup"><span data-stu-id="a0f9a-733">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="a0f9a-734">已将多个模型类型从 SecretBase 更新为 Object</span><span class="sxs-lookup"><span data-stu-id="a0f9a-734">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="a0f9a-735">增加了 Blob 事件触发器</span><span class="sxs-lookup"><span data-stu-id="a0f9a-735">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="a0f9a-736">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a0f9a-736">AzureRM.KeyVault</span></span>
* <span data-ttu-id="a0f9a-737">使用示例输出更新了文档</span><span class="sxs-lookup"><span data-stu-id="a0f9a-737">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="a0f9a-738">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a0f9a-738">AzureRM.Network</span></span>
* <span data-ttu-id="a0f9a-739">在网络观察程序 cmdlet 上启用了流量分析参数</span><span class="sxs-lookup"><span data-stu-id="a0f9a-739">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="a0f9a-740">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="a0f9a-740">AzureRM.Resources</span></span>
* <span data-ttu-id="a0f9a-741">修复了从“Get-AzureRmResource”返回的“PSResource”对象的“Properties”属性问题</span><span class="sxs-lookup"><span data-stu-id="a0f9a-741">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="a0f9a-742">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="a0f9a-742">AzureRM.Scheduler</span></span>
* <span data-ttu-id="a0f9a-743">修复了更新 ServiceBusQueueJob 无法设置新 Auth 值的问题</span><span class="sxs-lookup"><span data-stu-id="a0f9a-743">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="a0f9a-744">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="a0f9a-744">AzureRM.Sql</span></span>
* <span data-ttu-id="a0f9a-745">使用可选的 LicenseType 参数更新了以下 cmdlet</span><span class="sxs-lookup"><span data-stu-id="a0f9a-745">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="a0f9a-746">New-AzureRmSqlDatabase；Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a0f9a-746">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="a0f9a-747">New-AzureRmSqlElasticPool；Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="a0f9a-747">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="a0f9a-748">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="a0f9a-748">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="a0f9a-749">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="a0f9a-749">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="a0f9a-750">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a0f9a-750">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="a0f9a-751">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="a0f9a-751">AzureRM.Websites</span></span>
* <span data-ttu-id="a0f9a-752">更新了“New-AzureRMWebApp”，可以使用策略库中的常用算法。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-752">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="a0f9a-753">6.1.0 - 2018 年 5 月</span><span class="sxs-lookup"><span data-stu-id="a0f9a-753">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="a0f9a-754">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="a0f9a-754">AzureRM.Profile</span></span>
* <span data-ttu-id="a0f9a-755">修复了运行“Clear-AzureRmContext”时会保留空上下文的问题，该上下文使用旧的默认上下文的名称，导致用户无法使用旧名称创建新的上下文</span><span class="sxs-lookup"><span data-stu-id="a0f9a-755">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="a0f9a-756">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a0f9a-756">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="a0f9a-757">允许在 AS 上执行网关的关联/取消关联操作。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-757">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="a0f9a-758">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a0f9a-758">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="a0f9a-759">增加了对 ApiVersions、ApiReleases 和 ApiRevisions 的支持</span><span class="sxs-lookup"><span data-stu-id="a0f9a-759">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="a0f9a-760">增加了对 ServiceFabric 后端的支持</span><span class="sxs-lookup"><span data-stu-id="a0f9a-760">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="a0f9a-761">增加了对 Application Insights Logger 的支持</span><span class="sxs-lookup"><span data-stu-id="a0f9a-761">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="a0f9a-762">增加的支持包括认可“基本”SKU 是 API 管理服务的有效 SKU</span><span class="sxs-lookup"><span data-stu-id="a0f9a-762">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="a0f9a-763">增加的支持包括允许将专用 CA 颁发的证书作为根证书或 CA 证书安装</span><span class="sxs-lookup"><span data-stu-id="a0f9a-763">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="a0f9a-764">增加的支持包括通过 KeyVault 和多个代理主机名接受自定义 SSL 证书</span><span class="sxs-lookup"><span data-stu-id="a0f9a-764">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="a0f9a-765">增加了对 MSI 标识的支持</span><span class="sxs-lookup"><span data-stu-id="a0f9a-765">Added support for MSI identity</span></span>
* <span data-ttu-id="a0f9a-766">增加的支持包括通过 URL 接受策略 注意：以下 cmdlet 将在未来版本中弃用</span><span class="sxs-lookup"><span data-stu-id="a0f9a-766">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="a0f9a-767">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="a0f9a-767">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="a0f9a-768">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="a0f9a-768">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="a0f9a-769">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="a0f9a-769">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="a0f9a-770">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="a0f9a-770">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="a0f9a-771">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="a0f9a-771">AzureRM.Batch</span></span>
* <span data-ttu-id="a0f9a-772">发布新 cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="a0f9a-772">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="a0f9a-773">发布新 cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="a0f9a-773">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="a0f9a-774">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="a0f9a-774">AzureRM.Consumption</span></span>
* <span data-ttu-id="a0f9a-775">在 Cmdlet Get-AzureRmConsumptionUsageDetail 中增加了新参数 Expand、ResourceGroup、InstanceName、InstanceId、Tags、Top</span><span class="sxs-lookup"><span data-stu-id="a0f9a-775">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="a0f9a-776">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a0f9a-776">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="a0f9a-777">修复了 Export-AzureRmDataLakeStoreChildItemProperties 的示例</span><span class="sxs-lookup"><span data-stu-id="a0f9a-777">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="a0f9a-778">修复了 Set-AzureRmDataLakeStoreItemAclEntry 中 Recurse 用例的 null 参数异常</span><span class="sxs-lookup"><span data-stu-id="a0f9a-778">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="a0f9a-779">修复了 Set-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAcl、Remove-AzureRmDataLakeStoreItemAclEntry 的帮助文件</span><span class="sxs-lookup"><span data-stu-id="a0f9a-779">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="a0f9a-780">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a0f9a-780">AzureRM.Network</span></span>
* <span data-ttu-id="a0f9a-781">将网络 SDK 版本从 18.0.0-preview 升至 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="a0f9a-781">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="a0f9a-782">增加了用于创建协议配置的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="a0f9a-782">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="a0f9a-783">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="a0f9a-783">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="a0f9a-784">增加了用于向现有的快速路由线路添加新的线路连接的 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-784">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="a0f9a-785">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="a0f9a-785">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="a0f9a-786">增加了用于从现有的快速路由线路删除线路连接的 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-786">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="a0f9a-787">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="a0f9a-787">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="a0f9a-788">增加了用于检索线路连接的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="a0f9a-788">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="a0f9a-789">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="a0f9a-789">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="a0f9a-790">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a0f9a-790">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="a0f9a-791">修复了使用生成的证书进行服务器身份验证的问题（问题 5998）</span><span class="sxs-lookup"><span data-stu-id="a0f9a-791">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="a0f9a-792">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="a0f9a-792">AzureRM.Sql</span></span>
* <span data-ttu-id="a0f9a-793">更新了审核 cmdlet，允许删除 AuditActions 或 AuditActionGroups</span><span class="sxs-lookup"><span data-stu-id="a0f9a-793">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="a0f9a-794">修复了设置新的灵活保留策略时使用 Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy 出现的问题。该问题的具体表现是：在命令失败的同时，出现“不再支持使用 Azure 恢复服务保管库和策略配置长期保留策略。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-794">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="a0f9a-795">请使用新的灵活保留策略提交请求”错误消息。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-795">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="a0f9a-796">更新了与 Azure SQL 数据库/ElasticPool 的创建/更新相关的所有 cmdlet，允许使用新的数据库 API，而这些 cmdlet 支持的 SKU 属性则适用于规模和层相关属性。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-796">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="a0f9a-797">更新的 cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="a0f9a-797">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="a0f9a-798">New-AzureRmSqlDatabase；Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a0f9a-798">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="a0f9a-799">New-AzureRmSqlElasticPool；Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="a0f9a-799">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="a0f9a-800">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="a0f9a-800">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="a0f9a-801">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="a0f9a-801">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="a0f9a-802">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a0f9a-802">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="a0f9a-803">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="a0f9a-803">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="a0f9a-804">更新了“Get-AzureRmTrafficManagerProfile”的参数，要求在使用 -Name 参数时使用 -ResourceGroupName 参数。</span><span class="sxs-lookup"><span data-stu-id="a0f9a-804">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
