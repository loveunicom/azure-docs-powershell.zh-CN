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
ms.openlocfilehash: 3cb71087a61a0fcd06c014394e8f9e5654d4c1a8
ms.sourcegitcommit: 19dffee617477001f98d43e39a50ce1fad087b74
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2018
ms.locfileid: "47178997"
---
# <a name="release-notes"></a><span data-ttu-id="ddc6d-103">发行说明</span><span class="sxs-lookup"><span data-stu-id="ddc6d-103">Release notes</span></span>

<span data-ttu-id="ddc6d-104">下面是此版本中对 Azure PowerShell 所做的更改列表。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="690---september-2018"></a><span data-ttu-id="ddc6d-105">6.9.0 - 2018 年 9 月</span><span class="sxs-lookup"><span data-stu-id="ddc6d-105">6.9.0 - September 2018</span></span>
#### <a name="general"></a><span data-ttu-id="ddc6d-106">常规</span><span class="sxs-lookup"><span data-stu-id="ddc6d-106">General</span></span>
* <span data-ttu-id="ddc6d-107">AzureRM.SignalR 已添加到 AzureRM 汇总模块</span><span class="sxs-lookup"><span data-stu-id="ddc6d-107">AzureRM.SignalR was added to the AzureRM rollup module</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="ddc6d-108">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ddc6d-108">AzureRM.Profile</span></span>
* <span data-ttu-id="ddc6d-109">对存储常用代码进行了细微的更改</span><span class="sxs-lookup"><span data-stu-id="ddc6d-109">Minor changes to the storage common code</span></span>
* <span data-ttu-id="ddc6d-110">更新了帮助文件，使之包括完整参数类型。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-110">Updated help files to include full parameter types.</span></span>
- <span data-ttu-id="ddc6d-111">已在 ServicePrincipalCertificateWithSubscriptionId 参数集中将 -ServicePrincipal 更改为非强制性项</span><span class="sxs-lookup"><span data-stu-id="ddc6d-111">Changed -ServicePrincipal to non-mandatory in the ServicePrincipalCertificateWithSubscriptionId parameter set</span></span> 

#### <a name="azurestorage"></a><span data-ttu-id="ddc6d-112">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="ddc6d-112">Azure.Storage</span></span>
* <span data-ttu-id="ddc6d-113">支持使用 OAuth 创建存储上下文。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-113">Support create Storage Context with OAuth.</span></span> 
    - <span data-ttu-id="ddc6d-114">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="ddc6d-114">New-AzureStorageContext</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="ddc6d-115">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="ddc6d-115">AzureRM.Cdn</span></span>
* <span data-ttu-id="ddc6d-116">在 Cdn 定价 sku 中增加了 Standard_Microsoft。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-116">Added Standard_Microsoft in Cdn pricing sku.</span></span> 

#### <a name="azurermcompute"></a><span data-ttu-id="ddc6d-117">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ddc6d-117">AzureRM.Compute</span></span>
* <span data-ttu-id="ddc6d-118">将 Keyvault 和存储的依赖项移到了常用依赖项中</span><span class="sxs-lookup"><span data-stu-id="ddc6d-118">Move dependencies on Keyvault and Storage to the common dependencies</span></span>
* <span data-ttu-id="ddc6d-119">增加了对 AEM cmdlet 的支持，可以使用更多的虚拟机大小</span><span class="sxs-lookup"><span data-stu-id="ddc6d-119">Add support for more virutal machine sizes to AEM cmdlets</span></span>
* <span data-ttu-id="ddc6d-120">为 New-AzureRmVmssIpConfig 增加了 PublicIPPrefix 参数</span><span class="sxs-lookup"><span data-stu-id="ddc6d-120">Add PublicIPPrefix parameter to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="ddc6d-121">为 Invoke-AzureRmVMRunCommand cmdelt 增加了 ResourceId 参数</span><span class="sxs-lookup"><span data-stu-id="ddc6d-121">Add ResourceId parameter to Invoke-AzureRmVMRunCommand cmdelt</span></span>
* <span data-ttu-id="ddc6d-122">增加了 Invoke-AzureRmVmssVMRunCommand cmdlet</span><span class="sxs-lookup"><span data-stu-id="ddc6d-122">Add Invoke-AzureRmVmssVMRunCommand cmdlet</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="ddc6d-123">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="ddc6d-123">AzureRM.Dns</span></span>
* <span data-ttu-id="ddc6d-124">增加了在创建 dns 记录期间对别名记录的支持</span><span class="sxs-lookup"><span data-stu-id="ddc6d-124">Added support for alias record during dns record creation</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="ddc6d-125">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="ddc6d-125">AzureRM.Insights</span></span>
* <span data-ttu-id="ddc6d-126">修复了问题 #6833 和 #7102（诊断设置方面）</span><span class="sxs-lookup"><span data-stu-id="ddc6d-126">Fixed issues #6833 and #7102 (Diagnostic Settings area)</span></span>
    - <span data-ttu-id="ddc6d-127">在创建和列出/获取诊断设置期间出现的默认名称（即“service”）的问题</span><span class="sxs-lookup"><span data-stu-id="ddc6d-127">Issues with the default name, i.e. 'service', during creation and listing/getting of diagnostic settings</span></span>
    - <span data-ttu-id="ddc6d-128">通过类别创建诊断设置的问题</span><span class="sxs-lookup"><span data-stu-id="ddc6d-128">Issues creating diagnostic settings with categories</span></span>
* <span data-ttu-id="ddc6d-129">为指标时间粒度参数添加了弃用消息</span><span class="sxs-lookup"><span data-stu-id="ddc6d-129">Added deprecation message for metrics time grains parameters</span></span>
    - <span data-ttu-id="ddc6d-130">Timegrains 参数仍然会被接受（这是非重大变更），但在后端会被忽略，因为仅 PT1M 有效</span><span class="sxs-lookup"><span data-stu-id="ddc6d-130">Timegrains parameters are still being accepted (this is a non-breaking change,) but they are ignored in the backend since only PT1M is valid</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ddc6d-131">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ddc6d-131">AzureRM.Network</span></span>
* <span data-ttu-id="ddc6d-132">更改了 LoadBalancer cmdlet</span><span class="sxs-lookup"><span data-stu-id="ddc6d-132">Changes to LoadBalancer cmdlets</span></span>
  - <span data-ttu-id="ddc6d-133">LoadBalancerInboundNatPoolConfig：增加了 IdleTimeoutInMinutes、EnableFloatingIp 和 EnableTcpReset 参数</span><span class="sxs-lookup"><span data-stu-id="ddc6d-133">LoadBalancerInboundNatPoolConfig: added parameters IdleTimeoutInMinutes, EnableFloatingIp and EnableTcpReset</span></span>
  - <span data-ttu-id="ddc6d-134">LoadBalancerInboundNatRuleConfig：增加了 EnableTcpReset 参数</span><span class="sxs-lookup"><span data-stu-id="ddc6d-134">LoadBalancerInboundNatRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="ddc6d-135">LoadBalancerRuleConfig：增加了 EnableTcpReset 参数</span><span class="sxs-lookup"><span data-stu-id="ddc6d-135">LoadBalancerRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="ddc6d-136">LoadBalancerProbeConfig：增加了对参数 Protocol 的“Https”值的支持</span><span class="sxs-lookup"><span data-stu-id="ddc6d-136">LoadBalancerProbeConfig: added support for value "Https" for parameter Protocol</span></span>
* <span data-ttu-id="ddc6d-137">为新 LoadBalancer 的子资源 OutboundRule 增加了新命令</span><span class="sxs-lookup"><span data-stu-id="ddc6d-137">Added new commands for new LoadBalancer's subresource OutboundRule</span></span>
  - <span data-ttu-id="ddc6d-138">Add-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ddc6d-138">Add-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="ddc6d-139">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ddc6d-139">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="ddc6d-140">New-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ddc6d-140">New-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="ddc6d-141">Set-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ddc6d-141">Set-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="ddc6d-142">Remove-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ddc6d-142">Remove-AzureRmLoadBalancerOutboundRuleConfig</span></span>
* <span data-ttu-id="ddc6d-143">为 PSNetworkInterface 增加了新的 HostedWorkloads 属性</span><span class="sxs-lookup"><span data-stu-id="ddc6d-143">Added new HostedWorkloads property for PSNetworkInterface</span></span>
* <span data-ttu-id="ddc6d-144">通过 ARM 为 Azure 防火墙功能增加了新的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="ddc6d-144">Added new cmdlets for feature: Azure Firewall via ARM</span></span>
  - <span data-ttu-id="ddc6d-145">增加了 Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="ddc6d-145">Added Get-AzureRmFirewall</span></span>
  - <span data-ttu-id="ddc6d-146">增加了 Set-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="ddc6d-146">Added Set-AzureRmFirewall</span></span>
  - <span data-ttu-id="ddc6d-147">增加了 New-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="ddc6d-147">Added New-AzureRmFirewall</span></span>
  - <span data-ttu-id="ddc6d-148">增加了 Remove-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="ddc6d-148">Added Remove-AzureRmFirewall</span></span>
  - <span data-ttu-id="ddc6d-149">增加了 New-AzureRmFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="ddc6d-149">Added New-AzureRmFirewallApplicationRuleCollection</span></span>
  - <span data-ttu-id="ddc6d-150">增加了 New-AzureRmFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="ddc6d-150">Added New-AzureRmFirewallApplicationRule</span></span>
  - <span data-ttu-id="ddc6d-151">增加了 New-AzureRmFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="ddc6d-151">Added New-AzureRmFirewallNatRuleCollection</span></span>
  - <span data-ttu-id="ddc6d-152">增加了 New-AzureRmFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="ddc6d-152">Added New-AzureRmFirewallNatRule</span></span>
  - <span data-ttu-id="ddc6d-153">增加了 New-AzureRmFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="ddc6d-153">Added New-AzureRmFirewallNetworkRuleCollection</span></span>
  - <span data-ttu-id="ddc6d-154">增加了 New-AzureRmFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ddc6d-154">Added New-AzureRmFirewallNetworkRule</span></span>
* <span data-ttu-id="ddc6d-155">在应用程序网关中增加了对受信任根证书和自动缩放配置的支持</span><span class="sxs-lookup"><span data-stu-id="ddc6d-155">Added support for Trusted Root certificate and Autoscale configuration in Application Gateway</span></span>
  - <span data-ttu-id="ddc6d-156">增加了新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="ddc6d-156">New Cmdlets added:</span></span>
      - <span data-ttu-id="ddc6d-157">Add-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ddc6d-157">Add-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="ddc6d-158">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ddc6d-158">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="ddc6d-159">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ddc6d-159">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="ddc6d-160">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ddc6d-160">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="ddc6d-161">Set-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ddc6d-161">Set-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="ddc6d-162">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ddc6d-162">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="ddc6d-163">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ddc6d-163">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="ddc6d-164">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ddc6d-164">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="ddc6d-165">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ddc6d-165">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
  - <span data-ttu-id="ddc6d-166">使用可选参数 -TrustedRootCertificate 更新了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ddc6d-166">Cmdlets updated with optonal parameter -TrustedRootCertificate</span></span>
      - <span data-ttu-id="ddc6d-167">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ddc6d-167">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="ddc6d-168">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ddc6d-168">Set-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="ddc6d-169">New-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="ddc6d-169">New-AzureRmApplicationGatewayBackendHttpSetting</span></span>
      - <span data-ttu-id="ddc6d-170">Set-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="ddc6d-170">Set-AzureRmApplicationGatewayBackendHttpSetting</span></span>
  - <span data-ttu-id="ddc6d-171">使用可选参数 -AutoscaleConfiguration 更新了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ddc6d-171">Cmdlets updated with optonal parameter -AutoscaleConfiguration</span></span>
      - <span data-ttu-id="ddc6d-172">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ddc6d-172">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="ddc6d-173">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ddc6d-173">Set-AzureRmApplicationGateway</span></span>
* <span data-ttu-id="ddc6d-174">为接口终结点增加了 cmdlet Get-AzureInterfaceEndpoint</span><span class="sxs-lookup"><span data-stu-id="ddc6d-174">Add cmdlet for Interface Endpoint Get-AzureInterfaceEndpoint</span></span>
* <span data-ttu-id="ddc6d-175">在子网中增加了对多个地址前缀的支持。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-175">Added support for multiple address prefixes in a subnet.</span></span> <span data-ttu-id="ddc6d-176">更新了 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="ddc6d-176">Updated cmdlets:</span></span>
  - <span data-ttu-id="ddc6d-177">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="ddc6d-177">New-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="ddc6d-178">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="ddc6d-178">Set-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="ddc6d-179">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="ddc6d-179">Add-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="ddc6d-180">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="ddc6d-180">Get-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="ddc6d-181">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ddc6d-181">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>
  - <span data-ttu-id="ddc6d-182">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="ddc6d-182">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="ddc6d-183">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="ddc6d-183">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="ddc6d-184">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="ddc6d-184">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="ddc6d-185">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ddc6d-185">Add-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="ddc6d-186">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ddc6d-186">New-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="ddc6d-187">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ddc6d-187">Set-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="ddc6d-188">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ddc6d-188">Add-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="ddc6d-189">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ddc6d-189">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="ddc6d-190">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="ddc6d-190">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="ddc6d-191">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="ddc6d-191">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="ddc6d-192">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ddc6d-192">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="ddc6d-193">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ddc6d-193">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="ddc6d-194">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ddc6d-194">New-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="ddc6d-195">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="ddc6d-195">New-AzureRmNetworkInterface</span></span>
* <span data-ttu-id="ddc6d-196">增加了用于子网委派的 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-196">Adding cmdlets for subnet delegation.</span></span>
  - <span data-ttu-id="ddc6d-197">New-AzureRmDelegation：创建一个可以添加到子网的新委派</span><span class="sxs-lookup"><span data-stu-id="ddc6d-197">New-AzureRmDelegation: Creates a new delegation, which can be added to a subnet</span></span>
  - <span data-ttu-id="ddc6d-198">Remove-AzureRmDelegation：获取一个子网，然后从该子网中删除提供的委派名称</span><span class="sxs-lookup"><span data-stu-id="ddc6d-198">Remove-AzureRmDelegation: Takes in a subnet and removes the provided delegation name from that subnet</span></span>
  - <span data-ttu-id="ddc6d-199">Add-AzureRmDelegation：获取一个子网，然后向该子网添加提供的服务名称作为委派</span><span class="sxs-lookup"><span data-stu-id="ddc6d-199">Add-AzureRmDelegation: Takes in a subnet and adds the provided service name as a delegation to that subnet</span></span>
  - <span data-ttu-id="ddc6d-200">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="ddc6d-200">Get-AzureRmDelegation</span></span>
  - <span data-ttu-id="ddc6d-201">Get-AzureRmAvailableServiceDelegations</span><span class="sxs-lookup"><span data-stu-id="ddc6d-201">Get-AzureRmAvailableServiceDelegations</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="ddc6d-202">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="ddc6d-202">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="ddc6d-203">支持托管磁盘</span><span class="sxs-lookup"><span data-stu-id="ddc6d-203">Support for managed Managed disk</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="ddc6d-204">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="ddc6d-204">AzureRM.RedisCache</span></span>
* <span data-ttu-id="ddc6d-205">更新了 Insights 依赖项。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-205">Updated Insights dependency.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ddc6d-206">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ddc6d-206">AzureRM.Resources</span></span>
* <span data-ttu-id="ddc6d-207">使用新参数 RollbackAction 更新了 New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ddc6d-207">Update New-AzureRmResourceGroupDeployment with new parameter RollbackAction</span></span>
    - <span data-ttu-id="ddc6d-208">使用新参数增加了对 OnErrorDeployment 的支持。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-208">Add support for OnErrorDeployment with the new parameter.</span></span>
* <span data-ttu-id="ddc6d-209">在策略分配方面支持托管标识。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-209">Support managed identity on policy assignments.</span></span>
* <span data-ttu-id="ddc6d-210">使用“New-AzureRmPolicyAssignment”来分配策略时，不再需要带默认值的参数</span><span class="sxs-lookup"><span data-stu-id="ddc6d-210">Parameters with default values are no longer requred when assigning a policy with 'New-AzureRmPolicyAssignment'</span></span>
* <span data-ttu-id="ddc6d-211">增加了新的 cmdlet Get-AzureRmPolicyAlias，用于检索策略别名</span><span class="sxs-lookup"><span data-stu-id="ddc6d-211">Add new cmdlet Get-AzureRmPolicyAlias for retrieving policy aliases</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="ddc6d-212">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ddc6d-212">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="ddc6d-213">修复了问题 #7161</span><span class="sxs-lookup"><span data-stu-id="ddc6d-213">Fixed issue #7161</span></span>

#### <a name="azurermsignalr"></a><span data-ttu-id="ddc6d-214">AzureRM.SignalR</span><span class="sxs-lookup"><span data-stu-id="ddc6d-214">AzureRM.SignalR</span></span>
* <span data-ttu-id="ddc6d-215">将 SKU 名称更新为 Free_F1 和 Standard_S1</span><span class="sxs-lookup"><span data-stu-id="ddc6d-215">Update SKU names to Free_F1 and Standard_S1</span></span>
* <span data-ttu-id="ddc6d-216">为 PSSignalRResource 对象增加了版本字段，为 PSSignalRKeys 对象增加了字符串。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-216">Add version field to the PSSignalRResource object and connection string to the PSSignalRKeys object.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="ddc6d-217">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="ddc6d-217">AzureRM.Storage</span></span>
* <span data-ttu-id="ddc6d-218">在 AzureRm.Storage 中支持不可变性策略</span><span class="sxs-lookup"><span data-stu-id="ddc6d-218">Support Immutability Policy in AzureRm.Storage</span></span> 
    - <span data-ttu-id="ddc6d-219">Remove-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ddc6d-219">Remove-AzureRmStorageAccountNetworkRule</span></span>
    - <span data-ttu-id="ddc6d-220">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ddc6d-220">Get-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="ddc6d-221">Update-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ddc6d-221">Update-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="ddc6d-222">New-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ddc6d-222">New-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="ddc6d-223">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ddc6d-223">Remove-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="ddc6d-224">Add-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="ddc6d-224">Add-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="ddc6d-225">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="ddc6d-225">Remove-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="ddc6d-226">Set-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="ddc6d-226">Set-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="ddc6d-227">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="ddc6d-227">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="ddc6d-228">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="ddc6d-228">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="ddc6d-229">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="ddc6d-229">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="ddc6d-230">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="ddc6d-230">AzureRM.Websites</span></span>
* <span data-ttu-id="ddc6d-231">增加了两个新的 cmdlet：Get-AzureRmDeletedWebApp 和 Restore-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="ddc6d-231">Added two new cmdlets: Get-AzureRmDeletedWebApp and Restore-AzureRmDeletedWebApp</span></span>
* <span data-ttu-id="ddc6d-232">增加了 New-AzureRmAppServicePlan -HyperV 开关，用于通过 Windows 容器创建应用服务计划</span><span class="sxs-lookup"><span data-stu-id="ddc6d-232">New-AzureRmAppServicePlan -HyperV switch is added for create app service plan with windows container</span></span>
* <span data-ttu-id="ddc6d-233">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - 增加了新参数 (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment)，用于创建和管理 Windows 容器应用</span><span class="sxs-lookup"><span data-stu-id="ddc6d-233">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - New parameters (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) added for creating and managing windows container app</span></span>

## <a name="681---august-2018"></a><span data-ttu-id="ddc6d-234">6.8.1 - 2018 年 8 月</span><span class="sxs-lookup"><span data-stu-id="ddc6d-234">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="ddc6d-235">常规</span><span class="sxs-lookup"><span data-stu-id="ddc6d-235">General</span></span>
* <span data-ttu-id="ddc6d-236">解决了未设置默认资源组的问题。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-236">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="ddc6d-237">更新了公共运行时程序集</span><span class="sxs-lookup"><span data-stu-id="ddc6d-237">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="ddc6d-238">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ddc6d-238">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="ddc6d-239">解决了未设置默认资源组的问题。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-239">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="ddc6d-240">修复了问题 https://github.com/Azure/azure-powershell/issues/6603</span><span class="sxs-lookup"><span data-stu-id="ddc6d-240">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="ddc6d-241">Import-AzureRmApiManagementApi 和 \*-AzureRmApiManagementCertificate cmdlet 现在处理相对路径</span><span class="sxs-lookup"><span data-stu-id="ddc6d-241">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="ddc6d-242">修复了问题 https://github.com/Azure/azure-powershell/issues/6879</span><span class="sxs-lookup"><span data-stu-id="ddc6d-242">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="ddc6d-243">CertificateInformation 是使 Set-AzureRmApiManagement cmdlet 可以正常工作的可设置属性。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-243">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="ddc6d-244">通过升级到 4.0.4-preview nuget 进行了修复</span><span class="sxs-lookup"><span data-stu-id="ddc6d-244">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="ddc6d-245">修复了问题 https://github.com/Azure/azure-powershell/issues/6853</span><span class="sxs-lookup"><span data-stu-id="ddc6d-245">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="ddc6d-246">针对按产品名称进行的搜索修复了 Odata 筛选器</span><span class="sxs-lookup"><span data-stu-id="ddc6d-246">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="ddc6d-247">修复了问题 https://github.com/Azure/azure-powershell/issues/6814</span><span class="sxs-lookup"><span data-stu-id="ddc6d-247">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="ddc6d-248">针对按 API 名称进行的搜索修复了 Odata 筛选器</span><span class="sxs-lookup"><span data-stu-id="ddc6d-248">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="ddc6d-249">添加了对 AzureMonitor 记录器的支持</span><span class="sxs-lookup"><span data-stu-id="ddc6d-249">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="ddc6d-250">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ddc6d-250">AzureRM.Compute</span></span>
* <span data-ttu-id="ddc6d-251">解决了错误输出中缺少目标的问题。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-251">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="ddc6d-252">解决了带有托管磁盘的 VM 的存储帐户类型问题</span><span class="sxs-lookup"><span data-stu-id="ddc6d-252">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="ddc6d-253">解决了未设置默认资源组的问题。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-253">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="ddc6d-254">解决了在其他环境（例如 Azure 中国）中使用 AEM 扩展 cmdlet 的问题</span><span class="sxs-lookup"><span data-stu-id="ddc6d-254">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ddc6d-255">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ddc6d-255">AzureRM.Network</span></span>
* <span data-ttu-id="ddc6d-256">将默认 cmdlet 输出表示形式更改为表视图</span><span class="sxs-lookup"><span data-stu-id="ddc6d-256">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="ddc6d-257">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="ddc6d-257">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="ddc6d-258">修复了在尝试扩展停用的容量时 Update-AzureRmPowerBIEmbeddedCapacity 中出现的故障</span><span class="sxs-lookup"><span data-stu-id="ddc6d-258">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="ddc6d-259">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ddc6d-259">AzureRM.Resources</span></span>
* <span data-ttu-id="ddc6d-260">解决了从市场创建托管应用程序的问题。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-260">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="ddc6d-261">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ddc6d-261">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="ddc6d-262">修复的问题</span><span class="sxs-lookup"><span data-stu-id="ddc6d-262">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="ddc6d-263">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="ddc6d-263">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="ddc6d-264">添加了对 MultiValue 路由方法的支持</span><span class="sxs-lookup"><span data-stu-id="ddc6d-264">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="ddc6d-265">MultiValue 路由的新参数“MaxReturn”</span><span class="sxs-lookup"><span data-stu-id="ddc6d-265">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="ddc6d-266">添加了对 Subnet 路由方法的支持</span><span class="sxs-lookup"><span data-stu-id="ddc6d-266">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="ddc6d-267">对终结点中的 IP 地址范围（子网）的支持</span><span class="sxs-lookup"><span data-stu-id="ddc6d-267">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="ddc6d-268">添加了对配置文件中的自定义标头的支持</span><span class="sxs-lookup"><span data-stu-id="ddc6d-268">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="ddc6d-269">添加了对配置文件中的预期状态代码范围的支持</span><span class="sxs-lookup"><span data-stu-id="ddc6d-269">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="ddc6d-270">添加了对终结点中的自定义标头的支持</span><span class="sxs-lookup"><span data-stu-id="ddc6d-270">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="ddc6d-271">6.8.0 - 2018 年 8 月</span><span class="sxs-lookup"><span data-stu-id="ddc6d-271">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="ddc6d-272">常规</span><span class="sxs-lookup"><span data-stu-id="ddc6d-272">General</span></span>
* <span data-ttu-id="ddc6d-273">解决了未设置默认资源组的问题。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-273">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="ddc6d-274">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ddc6d-274">AzureRM.Profile</span></span>
* <span data-ttu-id="ddc6d-275">为在执行 Connect-AzureRmAccount 期间返回的令牌添加了“过期”属性</span><span class="sxs-lookup"><span data-stu-id="ddc6d-275">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ddc6d-276">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ddc6d-276">AzureRM.Compute</span></span>
* <span data-ttu-id="ddc6d-277">解决了错误输出中缺少目标的问题。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-277">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="ddc6d-278">解决了带有托管磁盘的 VM 的存储帐户类型问题</span><span class="sxs-lookup"><span data-stu-id="ddc6d-278">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="ddc6d-279">解决了在其他环境（例如 Azure 中国）中使用 AEM 扩展 cmdlet 的问题</span><span class="sxs-lookup"><span data-stu-id="ddc6d-279">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="ddc6d-280">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="ddc6d-280">AzureRM.IotHub</span></span>
* <span data-ttu-id="ddc6d-281">修复了 New-AzureRmIotHubExportDevices 和 New-AzureRmIotHubImportDevices的示例</span><span class="sxs-lookup"><span data-stu-id="ddc6d-281">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ddc6d-282">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ddc6d-282">AzureRM.Network</span></span>
* <span data-ttu-id="ddc6d-283">将默认模型表示形式更改为表视图</span><span class="sxs-lookup"><span data-stu-id="ddc6d-283">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="ddc6d-284">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="ddc6d-284">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="ddc6d-285">修复了在尝试扩展停用的容量时 Update-AzureRmPowerBIEmbeddedCapacity 中出现的故障</span><span class="sxs-lookup"><span data-stu-id="ddc6d-285">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ddc6d-286">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ddc6d-286">AzureRM.Resources</span></span>
* <span data-ttu-id="ddc6d-287">解决了从市场创建托管应用程序的问题。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-287">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="ddc6d-288">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ddc6d-288">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="ddc6d-289">解决了以下问题</span><span class="sxs-lookup"><span data-stu-id="ddc6d-289">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="ddc6d-290">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="ddc6d-290">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="ddc6d-291">对 MultiValue 路由方法的支持</span><span class="sxs-lookup"><span data-stu-id="ddc6d-291">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="ddc6d-292">MultiValue 路由的新参数“MaxReturn”</span><span class="sxs-lookup"><span data-stu-id="ddc6d-292">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="ddc6d-293">对 Subnet 路由方法的支持</span><span class="sxs-lookup"><span data-stu-id="ddc6d-293">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="ddc6d-294">对终结点中的 IP 地址范围（子网）的支持</span><span class="sxs-lookup"><span data-stu-id="ddc6d-294">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="ddc6d-295">对配置文件中的自定义标头的支持</span><span class="sxs-lookup"><span data-stu-id="ddc6d-295">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="ddc6d-296">对配置文件中的预期状态代码范围的支持</span><span class="sxs-lookup"><span data-stu-id="ddc6d-296">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="ddc6d-297">对终结点中的自定义标头的支持</span><span class="sxs-lookup"><span data-stu-id="ddc6d-297">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="ddc6d-298">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="ddc6d-298">AzureRM.Websites</span></span>
* <span data-ttu-id="ddc6d-299">解决了错误地设置默认资源组的问题。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-299">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="ddc6d-300">6.7.0 - 2018 年 8 月</span><span class="sxs-lookup"><span data-stu-id="ddc6d-300">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="ddc6d-301">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ddc6d-301">AzureRM.Profile</span></span>
* <span data-ttu-id="ddc6d-302">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-302">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="ddc6d-303">向默认的上下文名称添加用户 ID，避免上下文冲突</span><span class="sxs-lookup"><span data-stu-id="ddc6d-303">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="ddc6d-304">修复了 Clear-AzureRmContext 在选择上下文 #6398 时出现的问题</span><span class="sxs-lookup"><span data-stu-id="ddc6d-304">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="ddc6d-305">允许将租户域传递给“Connect-AzureRmAccount”的“-TenantId”参数</span><span class="sxs-lookup"><span data-stu-id="ddc6d-305">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="ddc6d-306">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="ddc6d-306">Azure.Storage</span></span>
* <span data-ttu-id="ddc6d-307">去除了 Azure 文件共享配额的 5TB 限制</span><span class="sxs-lookup"><span data-stu-id="ddc6d-307">Remove the 5TB limitation for Azure File Share quota</span></span>
- <span data-ttu-id="ddc6d-308">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="ddc6d-308">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="ddc6d-309">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ddc6d-309">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="ddc6d-310">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-310">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="ddc6d-311">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ddc6d-311">Azure.AnalysisServices</span></span>
* <span data-ttu-id="ddc6d-312">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-312">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="ddc6d-313">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ddc6d-313">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="ddc6d-314">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-314">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="ddc6d-315">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="ddc6d-315">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="ddc6d-316">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-316">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="ddc6d-317">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="ddc6d-317">AzureRM.Automation</span></span>
* <span data-ttu-id="ddc6d-318">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-318">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="ddc6d-319">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="ddc6d-319">AzureRM.Backup</span></span>
* <span data-ttu-id="ddc6d-320">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-320">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="ddc6d-321">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="ddc6d-321">AzureRM.Batch</span></span>
* <span data-ttu-id="ddc6d-322">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-322">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="ddc6d-323">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="ddc6d-323">AzureRM.Billing</span></span>
* <span data-ttu-id="ddc6d-324">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-324">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="ddc6d-325">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="ddc6d-325">AzureRM.Cdn</span></span>
* <span data-ttu-id="ddc6d-326">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-326">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="ddc6d-327">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ddc6d-327">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="ddc6d-328">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-328">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ddc6d-329">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ddc6d-329">AzureRM.Compute</span></span>
* <span data-ttu-id="ddc6d-330">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-330">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="ddc6d-331">为 New-AzureRmVmssConfig 增加了 EvictionPolicy 参数</span><span class="sxs-lookup"><span data-stu-id="ddc6d-331">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="ddc6d-332">在 New-AzureRmVm 的 DiskFileParameterSet 中使用默认位置（如果未指定 Location）</span><span class="sxs-lookup"><span data-stu-id="ddc6d-332">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="ddc6d-333">修复了 Save-AzureRmVMImage 中的参数说明</span><span class="sxs-lookup"><span data-stu-id="ddc6d-333">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="ddc6d-334">修复了某些单次传递相关方案的 Get-AzureRmVMDiskEncryptionStatus cmdlet</span><span class="sxs-lookup"><span data-stu-id="ddc6d-334">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="ddc6d-335">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="ddc6d-335">AzureRM.Consumption</span></span>
* <span data-ttu-id="ddc6d-336">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-336">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="ddc6d-337">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="ddc6d-337">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="ddc6d-338">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-338">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="ddc6d-339">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ddc6d-339">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="ddc6d-340">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-340">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="ddc6d-341">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="ddc6d-341">AzureRM.DataFactories</span></span>
* <span data-ttu-id="ddc6d-342">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-342">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="ddc6d-343">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ddc6d-343">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="ddc6d-344">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-344">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="ddc6d-345">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="ddc6d-345">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="ddc6d-346">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-346">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="ddc6d-347">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ddc6d-347">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="ddc6d-348">修复了从 PowerShell 命令行设置 DebugPreference 时的调试问题</span><span class="sxs-lookup"><span data-stu-id="ddc6d-348">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="ddc6d-349">更新了 Set-AzureRmDataLakeStoreItemAcl 的示例</span><span class="sxs-lookup"><span data-stu-id="ddc6d-349">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="ddc6d-350">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-350">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="ddc6d-351">更新了 Set-AzureRmDataLakeStoreItemAclEntry 的示例</span><span class="sxs-lookup"><span data-stu-id="ddc6d-351">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="ddc6d-352">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="ddc6d-352">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="ddc6d-353">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-353">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="ddc6d-354">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="ddc6d-354">AzureRM.Dns</span></span>
* <span data-ttu-id="ddc6d-355">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-355">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="ddc6d-356">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="ddc6d-356">AzureRM.EventGrid</span></span>
* <span data-ttu-id="ddc6d-357">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-357">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="ddc6d-358">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="ddc6d-358">AzureRM.EventHub</span></span>
* <span data-ttu-id="ddc6d-359">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-359">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="ddc6d-360">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="ddc6d-360">AzureRM.HDInsight</span></span>
* <span data-ttu-id="ddc6d-361">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-361">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="ddc6d-362">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="ddc6d-362">AzureRM.Insights</span></span>
* <span data-ttu-id="ddc6d-363">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-363">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="ddc6d-364">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="ddc6d-364">AzureRM.IotHub</span></span>
* <span data-ttu-id="ddc6d-365">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-365">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="ddc6d-366">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ddc6d-366">AzureRM.KeyVault</span></span>
* <span data-ttu-id="ddc6d-367">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-367">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="ddc6d-368">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ddc6d-368">AzureRM.LogicApp</span></span>
* <span data-ttu-id="ddc6d-369">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-369">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="ddc6d-370">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="ddc6d-370">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="ddc6d-371">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-371">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="ddc6d-372">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="ddc6d-372">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="ddc6d-373">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-373">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="ddc6d-374">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="ddc6d-374">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="ddc6d-375">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-375">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="ddc6d-376">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="ddc6d-376">AzureRM.Media</span></span>
* <span data-ttu-id="ddc6d-377">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-377">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ddc6d-378">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ddc6d-378">AzureRM.Network</span></span>
* <span data-ttu-id="ddc6d-379">增加了 Set-AzureRmLocalNetworkGateway 的示例</span><span class="sxs-lookup"><span data-stu-id="ddc6d-379">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="ddc6d-380">增加了 Add-AzureRmVirtualNetworkGatewayIpConfig、Get-AzureRmVirtualNetworkGatewayConnectionSharedKey 和 New-AzureRmVirtualNetworkGatewayConnection 的示例和说明</span><span class="sxs-lookup"><span data-stu-id="ddc6d-380">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="ddc6d-381">增加了 Remove-AzureRmVirtualNetworkGatewayIpConfig 和 Reset-AzureRmVirtualNetworkGateway 的示例</span><span class="sxs-lookup"><span data-stu-id="ddc6d-381">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="ddc6d-382">增加了 Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey 的示例</span><span class="sxs-lookup"><span data-stu-id="ddc6d-382">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="ddc6d-383">增加了 Set-AzureRmVirtualNetworkGatewayConnectionSharedKey 的示例</span><span class="sxs-lookup"><span data-stu-id="ddc6d-383">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="ddc6d-384">增加了 Set-AzureRmVirtualNetworkGatewayConnection 的示例</span><span class="sxs-lookup"><span data-stu-id="ddc6d-384">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="ddc6d-385">使用最新的代码生成器重新生成了 ApplicationSecurityGroup、RouteTable 和 Usage 的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="ddc6d-385">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="ddc6d-386">阐明了在尝试获取的子网不存在时 Get-AzureRmVirtualNetworkSubnetConfig 的错误消息</span><span class="sxs-lookup"><span data-stu-id="ddc6d-386">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="ddc6d-387">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="ddc6d-387">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="ddc6d-388">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-388">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="ddc6d-389">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ddc6d-389">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="ddc6d-390">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-390">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="ddc6d-391">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ddc6d-391">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="ddc6d-392">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-392">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="ddc6d-393">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="ddc6d-393">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="ddc6d-394">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-394">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="ddc6d-395">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ddc6d-395">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="ddc6d-396">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-396">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="ddc6d-397">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="ddc6d-397">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="ddc6d-398">为 Get-AzureRmRecoveryServicesBackItem cmdlet 增加了策略筛选器。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-398">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="ddc6d-399">此命令返回受给定策略 ID 保护的备份项的列表。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-399">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="ddc6d-400">已将 Microsoft.Azure.Management.RecoveryServices.Backup 更新到 3.0.0-preview 版本。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-400">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="ddc6d-401">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-401">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="ddc6d-402">为 Restore-AzureRmRecoveryServicesBackupItem 增加了 TargetResourceGroupName 参数。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-402">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="ddc6d-403">托管磁盘还原到的资源组。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-403">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="ddc6d-404">适用于包含托管磁盘的 VM 的备份。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-404">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="ddc6d-405">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="ddc6d-405">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="ddc6d-406">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-406">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="ddc6d-407">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="ddc6d-407">AzureRM.RedisCache</span></span>
* <span data-ttu-id="ddc6d-408">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-408">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="ddc6d-409">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="ddc6d-409">AzureRM.Relay</span></span>
* <span data-ttu-id="ddc6d-410">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-410">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ddc6d-411">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ddc6d-411">AzureRM.Resources</span></span>
* <span data-ttu-id="ddc6d-412">支持在订阅范围部署模板。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-412">Support template deployment at subscription scope.</span></span> <span data-ttu-id="ddc6d-413">增加了新 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="ddc6d-413">Add new Cmdlets:</span></span>
    - <span data-ttu-id="ddc6d-414">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="ddc6d-414">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="ddc6d-415">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="ddc6d-415">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="ddc6d-416">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="ddc6d-416">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="ddc6d-417">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="ddc6d-417">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="ddc6d-418">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="ddc6d-418">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="ddc6d-419">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="ddc6d-419">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="ddc6d-420">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="ddc6d-420">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="ddc6d-421">修复了在将上下文传递给 Set-AzureRmResource 时引发错误的问题</span><span class="sxs-lookup"><span data-stu-id="ddc6d-421">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="ddc6d-422">修复了 New-AzureRmResourceGroupDeployment 中的示例</span><span class="sxs-lookup"><span data-stu-id="ddc6d-422">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="ddc6d-423">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-423">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="ddc6d-424">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="ddc6d-424">AzureRM.Scheduler</span></span>
* <span data-ttu-id="ddc6d-425">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-425">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="ddc6d-426">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ddc6d-426">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="ddc6d-427">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-427">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="ddc6d-428">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ddc6d-428">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="ddc6d-429">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-429">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="ddc6d-430">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ddc6d-430">AzureRM.Sql</span></span>
* <span data-ttu-id="ddc6d-431">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-431">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="ddc6d-432">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="ddc6d-432">AzureRM.Storage</span></span>
* <span data-ttu-id="ddc6d-433">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-433">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="ddc6d-434">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="ddc6d-434">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="ddc6d-435">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-435">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="ddc6d-436">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="ddc6d-436">AzureRM.Tags</span></span>
* <span data-ttu-id="ddc6d-437">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-437">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="ddc6d-438">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="ddc6d-438">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="ddc6d-439">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-439">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="ddc6d-440">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="ddc6d-440">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="ddc6d-441">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-441">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="ddc6d-442">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="ddc6d-442">AzureRM.Websites</span></span>
* <span data-ttu-id="ddc6d-443">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-443">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="ddc6d-444">6.6.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="ddc6d-444">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="ddc6d-445">常规</span><span class="sxs-lookup"><span data-stu-id="ddc6d-445">General</span></span>
* <span data-ttu-id="ddc6d-446">更新了所有帮助文件，以包括完整参数类型和正确的输入/输出类型。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-446">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="ddc6d-447">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ddc6d-447">AzureRM.Profile</span></span>
* <span data-ttu-id="ddc6d-448">更新了 Common.Strategy 库，以便能够验证资源的当前配置是否与目标资源兼容。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-448">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="ddc6d-449">在 Common.Storage 中添加了 ps1xml 类型</span><span class="sxs-lookup"><span data-stu-id="ddc6d-449">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="ddc6d-450">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="ddc6d-450">Azure.Storage</span></span>
* <span data-ttu-id="ddc6d-451">增加了从 DefaultProfile 获取存储上下文的支持</span><span class="sxs-lookup"><span data-stu-id="ddc6d-451">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="ddc6d-452">为 cmdlet 输出类型属性增加了 Ps1XmlAttribute。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-452">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="ddc6d-453">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ddc6d-453">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="ddc6d-454">修复了问题 https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="ddc6d-454">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="ddc6d-455">修复了 Automapper 中将 PsApiManagementApi 转换为 ApiContract 的 bug</span><span class="sxs-lookup"><span data-stu-id="ddc6d-455">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="ddc6d-456">修复了问题 https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="ddc6d-456">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="ddc6d-457">修复了 File.Save 中没有使用编码类型重载的 bug</span><span class="sxs-lookup"><span data-stu-id="ddc6d-457">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="ddc6d-458">修复了问题 https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="ddc6d-458">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="ddc6d-459">升级到了 4.0.3 Nuget版本，该版本修复了 apiId 上的模式异常</span><span class="sxs-lookup"><span data-stu-id="ddc6d-459">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ddc6d-460">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ddc6d-460">AzureRM.Compute</span></span>
* <span data-ttu-id="ddc6d-461">修复因使用 PremiumLRS 存储帐户类型重命名而在 New-AzureRmVm 中使用 DiskFileParameterSet 创建 VM 失败的问题。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-461">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="ddc6d-462">修复 Invoke-AzureRmVMRunCommand cmdlet</span><span class="sxs-lookup"><span data-stu-id="ddc6d-462">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="ddc6d-463">更新 Get-AzureRmAvailabilitySet 以启用列出订阅中的所有可用性集。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-463">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="ddc6d-464">（ResouceGroupName 参数现在是可选的。）</span><span class="sxs-lookup"><span data-stu-id="ddc6d-464">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="ddc6d-465">更新“New-AzureRmVm”的 SimpleParameterSet 以在符合条件的 VM 上启用加速网络。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-465">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="ddc6d-466">将 New-AzureRmVmss 简单参数集更新为在用户指定的 LB 已存在时创建 vmss 失败。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-466">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="ddc6d-467">更新 New-AzureRmDisk 的示例</span><span class="sxs-lookup"><span data-stu-id="ddc6d-467">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="ddc6d-468">添加“New-AzureRmVM”的示例</span><span class="sxs-lookup"><span data-stu-id="ddc6d-468">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="ddc6d-469">更新 Set-AzureRmVMOSDisk 的说明</span><span class="sxs-lookup"><span data-stu-id="ddc6d-469">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="ddc6d-470">更新 Set-AzureRmVMBginfoExtension 的示例 1 以更正拼写和前缀。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-470">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="ddc6d-471">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ddc6d-471">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="ddc6d-472">将 ADF .Net SDK 版本更新为 1.1.0。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-472">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="ddc6d-473">支持跨数据工厂的自承载集成运行时共享。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-473">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="ddc6d-474">将新参数 -SharedIntegrationRuntimeResourceId 添加到 Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-474">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="ddc6d-475">将新的可选参数 -LinkedDataFactoryName 添加到 Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-475">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="ddc6d-476">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ddc6d-476">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="ddc6d-477">将数据平面 SDK (Microsoft.Azure.DataLake.Store) 版本更新为 1.1.9</span><span class="sxs-lookup"><span data-stu-id="ddc6d-477">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="ddc6d-478">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="ddc6d-478">AzureRM.EventHub</span></span>
* <span data-ttu-id="ddc6d-479">在删除 cmdlet 中更新了 InputObject 和 ResourceId 的管道</span><span class="sxs-lookup"><span data-stu-id="ddc6d-479">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="ddc6d-480">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="ddc6d-480">AzureRM.Insights</span></span>
* <span data-ttu-id="ddc6d-481">修复了帮助文件中 OutputType 的格式问题</span><span class="sxs-lookup"><span data-stu-id="ddc6d-481">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="ddc6d-482">使用 Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span><span class="sxs-lookup"><span data-stu-id="ddc6d-482">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="ddc6d-483">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ddc6d-483">AzureRM.KeyVault</span></span>
* <span data-ttu-id="ddc6d-484">修复了 Set-AzureRmKeyVaultAccessPolicy 中的管道问题</span><span class="sxs-lookup"><span data-stu-id="ddc6d-484">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ddc6d-485">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ddc6d-485">AzureRM.Network</span></span>
* <span data-ttu-id="ddc6d-486">添加了 LoadBalancerInboundNatPoolConfig cmdlet 的示例。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-486">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ddc6d-487">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ddc6d-487">AzureRM.Resources</span></span>
* <span data-ttu-id="ddc6d-488">修复了为“Get-AzureRmResource”同时提供标记名称和值时出现的问题</span><span class="sxs-lookup"><span data-stu-id="ddc6d-488">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="ddc6d-489">使用“Set-AzureRmResource”修复管道方案</span><span class="sxs-lookup"><span data-stu-id="ddc6d-489">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="ddc6d-490">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ddc6d-490">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="ddc6d-491">在删除 cmdlet 中更新了 InputObject 和 ResourceId 的管道</span><span class="sxs-lookup"><span data-stu-id="ddc6d-491">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="ddc6d-492">修复了几个问题</span><span class="sxs-lookup"><span data-stu-id="ddc6d-492">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="ddc6d-493">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ddc6d-493">AzureRM.Sql</span></span>
* <span data-ttu-id="ddc6d-494">使用以下 cmdlet 添加服务器高级威胁防护支持：</span><span class="sxs-lookup"><span data-stu-id="ddc6d-494">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="ddc6d-495">Enable-AzureRmSqlServerAdvancedThreatProtection；Disable-AzureRmSqlServerAdvancedThreatProtection；Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="ddc6d-495">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="ddc6d-496">使用以下 cmdlet 添加漏洞评估支持：</span><span class="sxs-lookup"><span data-stu-id="ddc6d-496">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="ddc6d-497">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings；Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings；Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="ddc6d-497">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="ddc6d-498">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline；Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline；Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="ddc6d-498">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="ddc6d-499">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan；Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord；Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="ddc6d-499">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="ddc6d-500">修复了 Remove-AzureRmSqlServerFirewallRule 中的示例</span><span class="sxs-lookup"><span data-stu-id="ddc6d-500">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="ddc6d-501">修复了 Get-AzureSqlSyncGroupLog 中非美国基础文化的日期时间处理错误</span><span class="sxs-lookup"><span data-stu-id="ddc6d-501">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="ddc6d-502">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="ddc6d-502">AzureRM.Storage</span></span>
* <span data-ttu-id="ddc6d-503">将 Ps1XmlAttribute 添加到 cmdlet 输出类型属性</span><span class="sxs-lookup"><span data-stu-id="ddc6d-503">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="ddc6d-504">在表视图中显示 StorageAccount cmdlet 输出</span><span class="sxs-lookup"><span data-stu-id="ddc6d-504">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="ddc6d-505">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ddc6d-505">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="ddc6d-506">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ddc6d-506">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="ddc6d-507">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ddc6d-507">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="ddc6d-508">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="ddc6d-508">AzureRM.Tags</span></span>
* <span data-ttu-id="ddc6d-509">从 Tag cmdlet 帮助中删除不正确的语句</span><span class="sxs-lookup"><span data-stu-id="ddc6d-509">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="ddc6d-510">6.5.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="ddc6d-510">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="ddc6d-511">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ddc6d-511">AzureRM.Profile</span></span>
* <span data-ttu-id="ddc6d-512">更新了“Get-AzureRmContextAutosaveSetting”的帮助</span><span class="sxs-lookup"><span data-stu-id="ddc6d-512">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="ddc6d-513">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="ddc6d-513">Azure.Storage</span></span>
* <span data-ttu-id="ddc6d-514">支持使用只写 Sas 令牌上传 Blob 或文件</span><span class="sxs-lookup"><span data-stu-id="ddc6d-514">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="ddc6d-515">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ddc6d-515">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="ddc6d-516">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="ddc6d-516">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="ddc6d-517">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ddc6d-517">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="ddc6d-518">将所需属性 ResourceGroupName 添加到 AS。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-518">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="ddc6d-519">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="ddc6d-519">AzureRM.Automation</span></span>
* <span data-ttu-id="ddc6d-520">更新帮助并添加“New-AzureRMAutomationSchedule”的示例</span><span class="sxs-lookup"><span data-stu-id="ddc6d-520">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ddc6d-521">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ddc6d-521">AzureRM.Compute</span></span>
* <span data-ttu-id="ddc6d-522">将 -Tag 参数添加到 Update/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="ddc6d-522">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="ddc6d-523">添加“Add-AzureRmVmssExtension”的示例</span><span class="sxs-lookup"><span data-stu-id="ddc6d-523">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="ddc6d-524">添加“Remove-AzureRmVmssExtension”的示例</span><span class="sxs-lookup"><span data-stu-id="ddc6d-524">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="ddc6d-525">更新“Set-AzureRmVMAccessExtension”的帮助</span><span class="sxs-lookup"><span data-stu-id="ddc6d-525">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="ddc6d-526">更新 New-AzureRmVmss 的 SimpleParameterSet，以默认情况下将 SinglePlacementGroup 设置为false，并添加开关参数“SinglePlacementGroup”，使用户能够在单个放置组中创建 VMSS。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-526">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="ddc6d-527">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="ddc6d-527">AzureRM.EventHub</span></span>
* <span data-ttu-id="ddc6d-528">向 PSEventHubDRConfigurationAttributes 类添加了一个只读属性“PendingReplicationOperationsCount”，该属性在复制过程中为挂起的复制操作计数</span><span class="sxs-lookup"><span data-stu-id="ddc6d-528">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="ddc6d-529">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ddc6d-529">AzureRM.KeyVault</span></span>
* <span data-ttu-id="ddc6d-530">更新了 Set-AzureRmKeyVaultAccessPolicy 的错误消息</span><span class="sxs-lookup"><span data-stu-id="ddc6d-530">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="ddc6d-531">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ddc6d-531">AzureRM.LogicApp</span></span>
* <span data-ttu-id="ddc6d-532">修复了 New-AzureRmLogicApp 中的“无法解析参数集”错误</span><span class="sxs-lookup"><span data-stu-id="ddc6d-532">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ddc6d-533">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ddc6d-533">AzureRM.Network</span></span>
* <span data-ttu-id="ddc6d-534">在多个租户中为 Set/Add-AzureRmVirtualNetworkPeering 启用跨虚拟网络对等互连</span><span class="sxs-lookup"><span data-stu-id="ddc6d-534">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="ddc6d-535">针对应用程序网关更新了以下 cmdlet</span><span class="sxs-lookup"><span data-stu-id="ddc6d-535">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="ddc6d-536">New-AzureRmApplicationGateway：添加了 EnableFIPS 标志和区域支持</span><span class="sxs-lookup"><span data-stu-id="ddc6d-536">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="ddc6d-537">New-AzureRmApplicationGatewaySku：添加了新的 sku Standard_v2 和 WAF_v2</span><span class="sxs-lookup"><span data-stu-id="ddc6d-537">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="ddc6d-538">Set-AzureRmApplicationGatewaySku：添加了新的 sku Standard_v2 和 WAF_v2</span><span class="sxs-lookup"><span data-stu-id="ddc6d-538">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="ddc6d-539">使用最新的生成器版本重新生成了 RouteTable cmdlet</span><span class="sxs-lookup"><span data-stu-id="ddc6d-539">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="ddc6d-540">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="ddc6d-540">AzureRM.Relay</span></span>
* <span data-ttu-id="ddc6d-541">更新了 Markdown 文件，其中修复了示例中的参数名称问题</span><span class="sxs-lookup"><span data-stu-id="ddc6d-541">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ddc6d-542">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ddc6d-542">AzureRM.Resources</span></span>
* <span data-ttu-id="ddc6d-543">更新了 Roleassignment 和 roledefinition cmdlet：</span><span class="sxs-lookup"><span data-stu-id="ddc6d-543">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="ddc6d-544">删除了作为分页的一部分完成的额外 roledefinition 调用。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-544">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="ddc6d-545">修复了 Get-AzureRmRoleAssignment cmdlet</span><span class="sxs-lookup"><span data-stu-id="ddc6d-545">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="ddc6d-546">修复了 -ExpandPrincipalGroups 命令参数功能</span><span class="sxs-lookup"><span data-stu-id="ddc6d-546">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="ddc6d-547">修复了“Get-AzureRmResource”的问题，其中“-ResourceType”参数区分大小写</span><span class="sxs-lookup"><span data-stu-id="ddc6d-547">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="ddc6d-548">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ddc6d-548">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="ddc6d-549">向列表 cmdlet 添加了 top 和 skip 参数</span><span class="sxs-lookup"><span data-stu-id="ddc6d-549">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="ddc6d-550">添加了标准到高级命名空间迁移 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="ddc6d-550">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="ddc6d-551">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="ddc6d-551">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="ddc6d-552">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="ddc6d-552">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="ddc6d-553">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="ddc6d-553">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="ddc6d-554">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="ddc6d-554">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="ddc6d-555">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="ddc6d-555">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="ddc6d-556">向 PSServiceBusDRConfigurationAttributes 类添加了一个只读属性“PendingReplicationOperationsCount”，该属性在复制过程中为挂起的复制操作计数</span><span class="sxs-lookup"><span data-stu-id="ddc6d-556">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="ddc6d-557">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ddc6d-557">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="ddc6d-558">更新了“New-AzureRmServiceFabricCluster”的示例</span><span class="sxs-lookup"><span data-stu-id="ddc6d-558">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="ddc6d-559">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ddc6d-559">AzureRM.Sql</span></span>
* <span data-ttu-id="ddc6d-560">为 Management.Sql 添加新的 Cmdlet，以允许客户将 TDE 证书添加到 Sql Server 实例或托管实例</span><span class="sxs-lookup"><span data-stu-id="ddc6d-560">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="ddc6d-561">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="ddc6d-561">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="ddc6d-562">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="ddc6d-562">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="ddc6d-563">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="ddc6d-563">AzureRM.Websites</span></span>
* <span data-ttu-id="ddc6d-564">设置为 false 时，`Set-AzureRmWebApp -AssignIdentity` 和 `Set-AzureRmWebAppSlot -AssignIdentity` 现在将从站点对象中删除 Identity 属性。同时移除预览标记。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-564">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="ddc6d-565">`Get-AzureRmWebAppMetrics`、`Get-AzureRmAppServicePlanMetrics` 示例已更新</span><span class="sxs-lookup"><span data-stu-id="ddc6d-565">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="ddc6d-566">`Set-AzureRmWebApp -PhpVersion` 支持 off 作为有效的 php 版本</span><span class="sxs-lookup"><span data-stu-id="ddc6d-566">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="ddc6d-567">6.4.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="ddc6d-567">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="ddc6d-568">常规</span><span class="sxs-lookup"><span data-stu-id="ddc6d-568">General</span></span>
* <span data-ttu-id="ddc6d-569">修复了大多数模块的帮助文件中的 OutputType 格式问题</span><span class="sxs-lookup"><span data-stu-id="ddc6d-569">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="ddc6d-570">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ddc6d-570">AzureRM.Profile</span></span>
* <span data-ttu-id="ddc6d-571">已将 Ps1Xml 属性添加到基本输出类型</span><span class="sxs-lookup"><span data-stu-id="ddc6d-571">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ddc6d-572">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ddc6d-572">AzureRM.Compute</span></span>
* <span data-ttu-id="ddc6d-573">VMSS 的 IP 标记功能</span><span class="sxs-lookup"><span data-stu-id="ddc6d-573">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="ddc6d-574">已添加“New-AzureRmVmssIpTagConfig”cmdlet</span><span class="sxs-lookup"><span data-stu-id="ddc6d-574">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="ddc6d-575">已将 IpTag 参数添加到 New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="ddc6d-575">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="ddc6d-576">VMSS 的自动 OS 回滚功能</span><span class="sxs-lookup"><span data-stu-id="ddc6d-576">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="ddc6d-577">已将 DisableAutoRollback 参数添加到 New-AzureRmVmssConfig 和 Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ddc6d-577">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="ddc6d-578">VMSS 的 OS 升级历史记录功能</span><span class="sxs-lookup"><span data-stu-id="ddc6d-578">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="ddc6d-579">已将 OSUpgradeHistory 开关参数添加到 Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ddc6d-579">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="ddc6d-580">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="ddc6d-580">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="ddc6d-581">通过以下命令添加目录 ACL 的支持：</span><span class="sxs-lookup"><span data-stu-id="ddc6d-581">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="ddc6d-582">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="ddc6d-582">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="ddc6d-583">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="ddc6d-583">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="ddc6d-584">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="ddc6d-584">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="ddc6d-585">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ddc6d-585">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="ddc6d-586">为 Set-AzureRmDataLakeStoreItemAclEntry、Remove-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAcl 添加了取消支持和进度跟踪</span><span class="sxs-lookup"><span data-stu-id="ddc6d-586">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="ddc6d-587">为 Export-AzureRmDataLakeStoreChildItemProperties 添加了取消支持</span><span class="sxs-lookup"><span data-stu-id="ddc6d-587">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="ddc6d-588">修复了执行递归操作的 cmdlet 的调试消息刷新</span><span class="sxs-lookup"><span data-stu-id="ddc6d-588">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="ddc6d-589">修复了 DataLake cmdlet 的测试位置</span><span class="sxs-lookup"><span data-stu-id="ddc6d-589">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="ddc6d-590">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="ddc6d-590">AzureRM.EventHub</span></span>
* <span data-ttu-id="ddc6d-591">已将可选的 MaxCount 参数添加到“列出操作”cmdlet Get-AzureRmEventHub 和 Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="ddc6d-591">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="ddc6d-592">修复了 New-AzureRmEventHub cmdlet 的问题：创建新事件中心时至少需要一个参数。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-592">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="ddc6d-593">提供了默认参数集。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-593">Provided Default Parameter set.</span></span>
* <span data-ttu-id="ddc6d-594">已将可选参数 -KeyValue 添加到 New-AzureRmEventHubKey cmdlet，该参数可让用户提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-594">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="ddc6d-595">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ddc6d-595">AzureRM.KeyVault</span></span>
* <span data-ttu-id="ddc6d-596">修复了 Get-AzureRmKeyVault -Tag 返回所有资源的问题</span><span class="sxs-lookup"><span data-stu-id="ddc6d-596">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ddc6d-597">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ddc6d-597">AzureRM.Network</span></span>
* <span data-ttu-id="ddc6d-598">为区域冗余的 VirtualNetworkGateways 公开新 SKU</span><span class="sxs-lookup"><span data-stu-id="ddc6d-598">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="ddc6d-599">通过 ARM 为以下功能添加了新命令：ExpressRoute 合作伙伴 API</span><span class="sxs-lookup"><span data-stu-id="ddc6d-599">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="ddc6d-600">添加了 Get-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="ddc6d-600">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="ddc6d-601">添加了 Set-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="ddc6d-601">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="ddc6d-602">添加了 Add-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="ddc6d-602">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="ddc6d-603">添加了 Get-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="ddc6d-603">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="ddc6d-604">添加了 Remove-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="ddc6d-604">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="ddc6d-605">添加了 Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="ddc6d-605">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="ddc6d-606">添加了 Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="ddc6d-606">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="ddc6d-607">添加了 Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="ddc6d-607">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="ddc6d-608">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="ddc6d-608">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="ddc6d-609">添加了 Get-AzureRmRecoveryServicesBackupStatus cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-609">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="ddc6d-610">此 cmdlet 采用 VM ID，并检查 VM 是否受订阅中的某个保管库保护。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-610">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="ddc6d-611">如果存在此类保管库，该 cmdlet 会输出该保管库的详细信息。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-611">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ddc6d-612">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ddc6d-612">AzureRM.Resources</span></span>
* <span data-ttu-id="ddc6d-613">更新了 Get-AzureRmPolicyAssignment cmdlet：</span><span class="sxs-lookup"><span data-stu-id="ddc6d-613">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="ddc6d-614">添加了在管理组级别列出 -Scope 值的支持</span><span class="sxs-lookup"><span data-stu-id="ddc6d-614">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="ddc6d-615">添加了在管理组级别使用 -Scope 值检索单个分配的支持</span><span class="sxs-lookup"><span data-stu-id="ddc6d-615">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="ddc6d-616">已将 -Effective 和 -All 开关添加到 control 参数</span><span class="sxs-lookup"><span data-stu-id="ddc6d-616">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="ddc6d-617">更新了 Get/New/Remove/Set-AzureRmPolicyDefinition cmdlet</span><span class="sxs-lookup"><span data-stu-id="ddc6d-617">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="ddc6d-618">添加了 -ManagementGroupName 参数，以将操作应用到给定的管理组</span><span class="sxs-lookup"><span data-stu-id="ddc6d-618">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="ddc6d-619">添加了 -SubscriptionId 参数，以将操作应用到给定的订阅</span><span class="sxs-lookup"><span data-stu-id="ddc6d-619">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="ddc6d-620">更新了 Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlet</span><span class="sxs-lookup"><span data-stu-id="ddc6d-620">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="ddc6d-621">添加了 -ManagementGroupName 参数，以将操作应用到给定的管理组</span><span class="sxs-lookup"><span data-stu-id="ddc6d-621">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="ddc6d-622">添加了 -SubscriptionId 参数，以将操作应用到给定的订阅</span><span class="sxs-lookup"><span data-stu-id="ddc6d-622">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="ddc6d-623">添加了使用 TemplateParameterObject 时在参数中指定 KeyVault 机密引用的支持</span><span class="sxs-lookup"><span data-stu-id="ddc6d-623">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="ddc6d-624">修复了忽略“New-AzureRmADAppCredential”的“-EndDate”参数的问题</span><span class="sxs-lookup"><span data-stu-id="ddc6d-624">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="ddc6d-625">修复了“Add-AzureRmADGroupMember”使用错误的 URL 发出请求的问题</span><span class="sxs-lookup"><span data-stu-id="ddc6d-625">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="ddc6d-626">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ddc6d-626">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="ddc6d-627">已将可选参数 -KeyValue 添加到 New-AzureRmServiceBusKey cmdlet，该参数可让用户提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-627">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="ddc6d-628">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ddc6d-628">AzureRM.Sql</span></span>
* <span data-ttu-id="ddc6d-629">在 AzureRmSqlDatabaseRestorePoint 帮助中澄清了 SQLDW 的用户定义还原点</span><span class="sxs-lookup"><span data-stu-id="ddc6d-629">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="ddc6d-630">更新了多个 cmdlet 中 -ComputeGeneration 参数的文档</span><span class="sxs-lookup"><span data-stu-id="ddc6d-630">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="ddc6d-631">6.3.0 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="ddc6d-631">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="ddc6d-632">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ddc6d-632">AzureRM.Profile</span></span>
* <span data-ttu-id="ddc6d-633">更新了 Enable-AzureRmContextAutoSave 的错误消息</span><span class="sxs-lookup"><span data-stu-id="ddc6d-633">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="ddc6d-634">在运行没有旧上下文的“Connect-AzureRmAccount”时为每个订阅创建一个上下文</span><span class="sxs-lookup"><span data-stu-id="ddc6d-634">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="ddc6d-635">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="ddc6d-635">Azure.Storage</span></span>
* <span data-ttu-id="ddc6d-636">在帮助文件中增加了关于 -Permissions 参数的其他信息。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-636">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ddc6d-637">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ddc6d-637">AzureRM.Compute</span></span>
* <span data-ttu-id="ddc6d-638">“Get-AzureRmVmDiskEncryptionStatus”修复了一个针对没有数据磁盘的 VM 观察到的问题</span><span class="sxs-lookup"><span data-stu-id="ddc6d-638">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="ddc6d-639">更新计算客户端库版本以修复以下 cmdlet</span><span class="sxs-lookup"><span data-stu-id="ddc6d-639">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="ddc6d-640">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="ddc6d-640">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="ddc6d-641">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="ddc6d-641">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="ddc6d-642">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="ddc6d-642">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="ddc6d-643">修复了以下 cmdlet，因此可以正确地显示“操作 ID”和“操作状态”：</span><span class="sxs-lookup"><span data-stu-id="ddc6d-643">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="ddc6d-644">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ddc6d-644">Start-AzureRmVM</span></span>
    - <span data-ttu-id="ddc6d-645">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ddc6d-645">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="ddc6d-646">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ddc6d-646">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="ddc6d-647">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ddc6d-647">Set-AzureRmVM</span></span>
    - <span data-ttu-id="ddc6d-648">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="ddc6d-648">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="ddc6d-649">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ddc6d-649">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="ddc6d-650">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="ddc6d-650">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="ddc6d-651">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="ddc6d-651">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="ddc6d-652">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ddc6d-652">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="ddc6d-653">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ddc6d-653">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="ddc6d-654">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ddc6d-654">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="ddc6d-655">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ddc6d-655">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="ddc6d-656">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="ddc6d-656">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="ddc6d-657">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="ddc6d-657">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="ddc6d-658">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="ddc6d-658">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="ddc6d-659">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="ddc6d-659">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="ddc6d-660">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="ddc6d-660">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="ddc6d-661">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="ddc6d-661">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="ddc6d-662">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="ddc6d-662">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="ddc6d-663">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="ddc6d-663">AzureRM.EventGrid</span></span>
* <span data-ttu-id="ddc6d-664">在 Update-AzureRmEventGridSubscription cmdlet 中删除 SubjectBeginsWith/SubjectEndsWith 的 ValidateNotNullOrEmpty 验证条件，允许根据需要将这些参数更改为空字符串。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-664">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="ddc6d-665">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ddc6d-665">AzureRM.KeyVault</span></span>
* <span data-ttu-id="ddc6d-666">修复运行 Get-AzureRmKeyVault -Tag 时不返回任何标记的问题</span><span class="sxs-lookup"><span data-stu-id="ddc6d-666">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="ddc6d-667">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ddc6d-667">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="ddc6d-668">策略见解 cmdlet 的公开发行版</span><span class="sxs-lookup"><span data-stu-id="ddc6d-668">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="ddc6d-669">使用 API 版本 2018-04-04</span><span class="sxs-lookup"><span data-stu-id="ddc6d-669">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="ddc6d-670">向 Get-AzureRmPolicyStateSummary 的结果添加了 PolicyDefinitionReferenceId</span><span class="sxs-lookup"><span data-stu-id="ddc6d-670">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="ddc6d-671">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="ddc6d-671">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="ddc6d-672">向 RecoveryServices.Backup cmdlet 添加了 -Vault 参数。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-672">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="ddc6d-673">传递时，此项会替代 Set-AzureRmRecoveryServicesContext cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-673">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="ddc6d-674">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ddc6d-674">AzureRM.Sql</span></span>
* <span data-ttu-id="ddc6d-675">更新了 Get-AzureRmSqlDatabaseExpanded 的帮助文件中的示例</span><span class="sxs-lookup"><span data-stu-id="ddc6d-675">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="ddc6d-676">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="ddc6d-676">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="ddc6d-677">更新了 Add-AzureRmTrafficManagerEndpointConfig 的帮助文件</span><span class="sxs-lookup"><span data-stu-id="ddc6d-677">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="ddc6d-678">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="ddc6d-678">AzureRM.Websites</span></span>
* <span data-ttu-id="ddc6d-679">更新了“Set-AzureRmWebApp”，在使用 -AssignIdentity 时不覆盖 AppSettings</span><span class="sxs-lookup"><span data-stu-id="ddc6d-679">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="ddc6d-680">更新了“New-AzureRmWebAppSlot”，允许使用 AppServicePlan 作为可选参数</span><span class="sxs-lookup"><span data-stu-id="ddc6d-680">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="ddc6d-681">6.2.1 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="ddc6d-681">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="ddc6d-682">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ddc6d-682">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="ddc6d-683">更新了 PSWorkspace 模型，允许 Network 使用 type 作为参数</span><span class="sxs-lookup"><span data-stu-id="ddc6d-683">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="ddc6d-684">6.2.0 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="ddc6d-684">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="ddc6d-685">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ddc6d-685">AzureRM.Profile</span></span>
* <span data-ttu-id="ddc6d-686">修复了 Newtonsoft.Json 的版本 10.0.3 在模块导入时无法加载的问题</span><span class="sxs-lookup"><span data-stu-id="ddc6d-686">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ddc6d-687">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ddc6d-687">AzureRM.Compute</span></span>
* <span data-ttu-id="ddc6d-688">VMSS VM 更新功能</span><span class="sxs-lookup"><span data-stu-id="ddc6d-688">VMSS VM Update feature</span></span>
    - <span data-ttu-id="ddc6d-689">增加了“Update-AzureRmVmssVM”和“New-AzureRmVMDataDisk”cmdlet</span><span class="sxs-lookup"><span data-stu-id="ddc6d-689">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="ddc6d-690">为“Add-AzureRmVMDataDisk”cmdlet 增加了 VirtualMachineScaleSetVM 参数，支持向 Vmss VM 添加数据磁盘。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-690">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="ddc6d-691">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ddc6d-691">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="ddc6d-692">将 ADF.Net SDK 版本更新到了 0.8.0-preview，其中包含以下更改：</span><span class="sxs-lookup"><span data-stu-id="ddc6d-692">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="ddc6d-693">增加了“配置工厂存储库”操作</span><span class="sxs-lookup"><span data-stu-id="ddc6d-693">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="ddc6d-694">更新了 QuickBooks LinkedService，可以公开 consumerKey 和 consumerSecret 属性</span><span class="sxs-lookup"><span data-stu-id="ddc6d-694">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="ddc6d-695">已将多个模型类型从 SecretBase 更新为 Object</span><span class="sxs-lookup"><span data-stu-id="ddc6d-695">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="ddc6d-696">增加了 Blob 事件触发器</span><span class="sxs-lookup"><span data-stu-id="ddc6d-696">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="ddc6d-697">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ddc6d-697">AzureRM.KeyVault</span></span>
* <span data-ttu-id="ddc6d-698">使用示例输出更新了文档</span><span class="sxs-lookup"><span data-stu-id="ddc6d-698">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="ddc6d-699">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ddc6d-699">AzureRM.Network</span></span>
* <span data-ttu-id="ddc6d-700">在网络观察程序 cmdlet 上启用了流量分析参数</span><span class="sxs-lookup"><span data-stu-id="ddc6d-700">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ddc6d-701">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ddc6d-701">AzureRM.Resources</span></span>
* <span data-ttu-id="ddc6d-702">修复了从“Get-AzureRmResource”返回的“PSResource”对象的“Properties”属性问题</span><span class="sxs-lookup"><span data-stu-id="ddc6d-702">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="ddc6d-703">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="ddc6d-703">AzureRM.Scheduler</span></span>
* <span data-ttu-id="ddc6d-704">修复了更新 ServiceBusQueueJob 无法设置新 Auth 值的问题</span><span class="sxs-lookup"><span data-stu-id="ddc6d-704">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="ddc6d-705">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ddc6d-705">AzureRM.Sql</span></span>
* <span data-ttu-id="ddc6d-706">使用可选的 LicenseType 参数更新了以下 cmdlet</span><span class="sxs-lookup"><span data-stu-id="ddc6d-706">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="ddc6d-707">New-AzureRmSqlDatabase；Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ddc6d-707">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="ddc6d-708">New-AzureRmSqlElasticPool；Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="ddc6d-708">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="ddc6d-709">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="ddc6d-709">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="ddc6d-710">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="ddc6d-710">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="ddc6d-711">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ddc6d-711">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="ddc6d-712">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="ddc6d-712">AzureRM.Websites</span></span>
* <span data-ttu-id="ddc6d-713">更新了“New-AzureRMWebApp”，可以使用策略库中的常用算法。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-713">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="ddc6d-714">6.1.0 - 2018 年 5 月</span><span class="sxs-lookup"><span data-stu-id="ddc6d-714">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="ddc6d-715">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ddc6d-715">AzureRM.Profile</span></span>
* <span data-ttu-id="ddc6d-716">修复了运行“Clear-AzureRmContext”时会保留空上下文的问题，该上下文使用旧的默认上下文的名称，导致用户无法使用旧名称创建新的上下文</span><span class="sxs-lookup"><span data-stu-id="ddc6d-716">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="ddc6d-717">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ddc6d-717">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="ddc6d-718">允许在 AS 上执行网关的关联/取消关联操作。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-718">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="ddc6d-719">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ddc6d-719">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="ddc6d-720">增加了对 ApiVersions、ApiReleases 和 ApiRevisions 的支持</span><span class="sxs-lookup"><span data-stu-id="ddc6d-720">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="ddc6d-721">增加了对 ServiceFabric 后端的支持</span><span class="sxs-lookup"><span data-stu-id="ddc6d-721">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="ddc6d-722">增加了对 Application Insights Logger 的支持</span><span class="sxs-lookup"><span data-stu-id="ddc6d-722">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="ddc6d-723">增加的支持包括认可“基本”SKU 是 API 管理服务的有效 SKU</span><span class="sxs-lookup"><span data-stu-id="ddc6d-723">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="ddc6d-724">增加的支持包括允许将专用 CA 颁发的证书作为根证书或 CA 证书安装</span><span class="sxs-lookup"><span data-stu-id="ddc6d-724">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="ddc6d-725">增加的支持包括通过 KeyVault 和多个代理主机名接受自定义 SSL 证书</span><span class="sxs-lookup"><span data-stu-id="ddc6d-725">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="ddc6d-726">增加了对 MSI 标识的支持</span><span class="sxs-lookup"><span data-stu-id="ddc6d-726">Added support for MSI identity</span></span>
* <span data-ttu-id="ddc6d-727">增加的支持包括通过 URL 接受策略 注意：以下 cmdlet 将在未来版本中弃用</span><span class="sxs-lookup"><span data-stu-id="ddc6d-727">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="ddc6d-728">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="ddc6d-728">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="ddc6d-729">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="ddc6d-729">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="ddc6d-730">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="ddc6d-730">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="ddc6d-731">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="ddc6d-731">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="ddc6d-732">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="ddc6d-732">AzureRM.Batch</span></span>
* <span data-ttu-id="ddc6d-733">发布新 cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="ddc6d-733">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="ddc6d-734">发布新 cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="ddc6d-734">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="ddc6d-735">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="ddc6d-735">AzureRM.Consumption</span></span>
* <span data-ttu-id="ddc6d-736">在 Cmdlet Get-AzureRmConsumptionUsageDetail 中增加了新参数 Expand、ResourceGroup、InstanceName、InstanceId、Tags、Top</span><span class="sxs-lookup"><span data-stu-id="ddc6d-736">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="ddc6d-737">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ddc6d-737">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="ddc6d-738">修复了 Export-AzureRmDataLakeStoreChildItemProperties 的示例</span><span class="sxs-lookup"><span data-stu-id="ddc6d-738">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="ddc6d-739">修复了 Set-AzureRmDataLakeStoreItemAclEntry 中 Recurse 用例的 null 参数异常</span><span class="sxs-lookup"><span data-stu-id="ddc6d-739">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="ddc6d-740">修复了 Set-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAcl、Remove-AzureRmDataLakeStoreItemAclEntry 的帮助文件</span><span class="sxs-lookup"><span data-stu-id="ddc6d-740">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="ddc6d-741">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ddc6d-741">AzureRM.Network</span></span>
* <span data-ttu-id="ddc6d-742">将网络 SDK 版本从 18.0.0-preview 升至 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="ddc6d-742">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="ddc6d-743">增加了用于创建协议配置的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="ddc6d-743">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="ddc6d-744">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="ddc6d-744">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="ddc6d-745">增加了用于向现有的快速路由线路添加新的线路连接的 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-745">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="ddc6d-746">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="ddc6d-746">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="ddc6d-747">增加了用于从现有的快速路由线路删除线路连接的 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-747">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="ddc6d-748">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="ddc6d-748">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="ddc6d-749">增加了用于检索线路连接的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="ddc6d-749">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="ddc6d-750">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="ddc6d-750">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="ddc6d-751">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ddc6d-751">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="ddc6d-752">修复了使用生成的证书进行服务器身份验证的问题（问题 5998）</span><span class="sxs-lookup"><span data-stu-id="ddc6d-752">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="ddc6d-753">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ddc6d-753">AzureRM.Sql</span></span>
* <span data-ttu-id="ddc6d-754">更新了审核 cmdlet，允许删除 AuditActions 或 AuditActionGroups</span><span class="sxs-lookup"><span data-stu-id="ddc6d-754">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="ddc6d-755">修复了设置新的灵活保留策略时使用 Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy 出现的问题。该问题的具体表现是：在命令失败的同时，出现“不再支持使用 Azure 恢复服务保管库和策略配置长期保留策略。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-755">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="ddc6d-756">请使用新的灵活保留策略提交请求”错误消息。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-756">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="ddc6d-757">更新了与 Azure SQL 数据库/ElasticPool 的创建/更新相关的所有 cmdlet，允许使用新的数据库 API，而这些 cmdlet 支持的 SKU 属性则适用于规模和层相关属性。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-757">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="ddc6d-758">更新的 cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="ddc6d-758">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="ddc6d-759">New-AzureRmSqlDatabase；Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ddc6d-759">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="ddc6d-760">New-AzureRmSqlElasticPool；Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="ddc6d-760">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="ddc6d-761">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="ddc6d-761">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="ddc6d-762">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="ddc6d-762">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="ddc6d-763">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ddc6d-763">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="ddc6d-764">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="ddc6d-764">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="ddc6d-765">更新了“Get-AzureRmTrafficManagerProfile”的参数，要求在使用 -Name 参数时使用 -ResourceGroupName 参数。</span><span class="sxs-lookup"><span data-stu-id="ddc6d-765">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
