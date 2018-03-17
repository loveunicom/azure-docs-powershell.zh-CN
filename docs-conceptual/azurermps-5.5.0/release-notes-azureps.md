---
title: "Azure PowerShell 更改日志 | Microsoft Docs"
description: "下面提供了对 Azure PowerShell 最新版本所做更改的历史记录。"
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: 
ms.date: 2/20/2018
ms.openlocfilehash: 61306d057c81f533267a452f7a7e11b839b09718
ms.sourcegitcommit: 20af779cd523c758d40e23d60eb989a4ef982d5c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/15/2018
---
# <a name="release-notes"></a><span data-ttu-id="c2c8c-103">发行说明</span><span class="sxs-lookup"><span data-stu-id="c2c8c-103">Release notes</span></span>

<span data-ttu-id="c2c8c-104">下面是此版本中对 Azure PowerShell 所做的更改列表。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---

## <a name="550---march-2018"></a><span data-ttu-id="c2c8c-105">5.5.0 - 2018 年 3 月</span><span class="sxs-lookup"><span data-stu-id="c2c8c-105">5.5.0 - March 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="c2c8c-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c2c8c-106">AzureRM.Profile</span></span>
* <span data-ttu-id="c2c8c-107">修复了导入别名的问题</span><span class="sxs-lookup"><span data-stu-id="c2c8c-107">Fixed issue with importing aliases</span></span>
* <span data-ttu-id="c2c8c-108">将 Newtonsoft.Json 的 10.0.3 版随 6.0.8 版一起加载</span><span class="sxs-lookup"><span data-stu-id="c2c8c-108">Load version 10.0.3 of Newtonsoft.Json side-by-side with version 6.0.8</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="c2c8c-109">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="c2c8c-109">Azure.Storage</span></span>
* <span data-ttu-id="c2c8c-110">支持软删除功能</span><span class="sxs-lookup"><span data-stu-id="c2c8c-110">Support Soft-Delete feature</span></span>
    - <span data-ttu-id="c2c8c-111">Enable-AzureStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="c2c8c-111">Enable-AzureStorageDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="c2c8c-112">Disable-AzureStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="c2c8c-112">Disable-AzureStorageDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="c2c8c-113">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="c2c8c-113">Get-AzureStorageBlob</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="c2c8c-114">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="c2c8c-114">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="c2c8c-115">修复了导入别名的问题</span><span class="sxs-lookup"><span data-stu-id="c2c8c-115">Fixed issue with importing aliases</span></span>
* <span data-ttu-id="c2c8c-116">添加对防火墙和查询向外扩展功能的支持，以及对 2017-08-01 api 版本的支持。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-116">Add support of firewall and query scaleout feature, as well as support of 2017-08-01 api version.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="c2c8c-117">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="c2c8c-117">AzureRM.Automation</span></span>
* <span data-ttu-id="c2c8c-118">修复了导入别名的问题</span><span class="sxs-lookup"><span data-stu-id="c2c8c-118">Fixed issue with importing aliases</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="c2c8c-119">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="c2c8c-119">AzureRM.Cdn</span></span>
* <span data-ttu-id="c2c8c-120">修复了导入别名的问题</span><span class="sxs-lookup"><span data-stu-id="c2c8c-120">Fixed issue with importing aliases</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="c2c8c-121">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c2c8c-121">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="c2c8c-122">更新 notice.txt 和通知消息。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-122">Update notice.txt and notice message.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="c2c8c-123">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c2c8c-123">AzureRM.Compute</span></span>
* <span data-ttu-id="c2c8c-124">'New-AzureRmVMSS' 以详细模式打印连接字符串。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-124">'New-AzureRmVMSS' prints connection strings in verbose mode.</span></span>
* <span data-ttu-id="c2c8c-125">'New-AzureRmVmss' 支持公共 IP 地址、负载均衡规则、入站 NAT 规则。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-125">'New-AzureRmVmss' supports public IP address, load balancing rules, inbound NAT rules.</span></span>
* <span data-ttu-id="c2c8c-126">WriteAccelerator 功能</span><span class="sxs-lookup"><span data-stu-id="c2c8c-126">WriteAccelerator feature</span></span>
    - <span data-ttu-id="c2c8c-127">将 WriteAccelerator 开关参数添加到了以下 cmdlet：Set-AzureRmVMOSDisk Set-AzureRmVMDataDisk Add-AzureRmVMDataDisk Add-AzureRmVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="c2c8c-127">Added WriteAccelerator switch parameter to the following cmdlets: Set-AzureRmVMOSDisk Set-AzureRmVMDataDisk Add-AzureRmVMDataDisk Add-AzureRmVmssDataDisk</span></span>
    - <span data-ttu-id="c2c8c-128">将 OsDiskWriteAccelerator 开关参数添加到了以下 cmdlet：     Set-AzureRmVmssStorageProfile。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-128">Added OsDiskWriteAccelerator switch parameter to the following cmdlet:     Set-AzureRmVmssStorageProfile.</span></span>
    - <span data-ttu-id="c2c8c-129">将 OsDiskWriteAccelerator 布尔参数添加到了以下 cmdlet：     Update-AzureRmVM     Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c2c8c-129">Added OsDiskWriteAccelerator Boolean parameter to the following cmdlets:     Update-AzureRmVM     Update-AzureRmVmss</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="c2c8c-130">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="c2c8c-130">AzureRM.DataFactories</span></span>
* <span data-ttu-id="c2c8c-131">修复了导致某些加密操作没有有意义错误的凭据加密问题</span><span class="sxs-lookup"><span data-stu-id="c2c8c-131">Fix credential encryption issue that caused no meaningful error for some encryption operations</span></span>
* <span data-ttu-id="c2c8c-132">允许跨数据工厂共享集成运行时</span><span class="sxs-lookup"><span data-stu-id="c2c8c-132">Enable integration runtime to be shared across data factory</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="c2c8c-133">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="c2c8c-133">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="c2c8c-134">为 "Set-AzureRmDataFactoryV2IntegrationRuntime" cmd 添加了参数 "SetupScriptContainerSasUri" 和 "Edition" 以启用自定义安装和版本选择功能</span><span class="sxs-lookup"><span data-stu-id="c2c8c-134">Add parameter "SetupScriptContainerSasUri" and "Edition" for "Set-AzureRmDataFactoryV2IntegrationRuntime" cmd to enable custom setup and edition selection functionality</span></span>
* <span data-ttu-id="c2c8c-135">修复了导致某些加密操作没有有意义错误的凭据加密问题。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-135">Fix credential encryption issue that caused no meaningful error for some encryption operations.</span></span>
* <span data-ttu-id="c2c8c-136">允许跨数据工厂共享集成运行时</span><span class="sxs-lookup"><span data-stu-id="c2c8c-136">Enable integration runtime to be shared across data factory</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="c2c8c-137">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="c2c8c-137">AzureRM.HDInsight</span></span>
* <span data-ttu-id="c2c8c-138">修复了导入别名的问题</span><span class="sxs-lookup"><span data-stu-id="c2c8c-138">Fixed issue with importing aliases</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="c2c8c-139">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c2c8c-139">AzureRM.KeyVault</span></span>
* <span data-ttu-id="c2c8c-140">修复了 Set-AzureRmKeyVaultAccessPolicy 的示例</span><span class="sxs-lookup"><span data-stu-id="c2c8c-140">Fixed example for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="c2c8c-141">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c2c8c-141">AzureRM.Network</span></span>
* <span data-ttu-id="c2c8c-142">修复了导入别名的问题</span><span class="sxs-lookup"><span data-stu-id="c2c8c-142">Fixed issue with importing aliases</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="c2c8c-143">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="c2c8c-143">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="c2c8c-144">修复了导入别名的问题</span><span class="sxs-lookup"><span data-stu-id="c2c8c-144">Fixed issue with importing aliases</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="c2c8c-145">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c2c8c-145">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="c2c8c-146">修复了导入别名的问题</span><span class="sxs-lookup"><span data-stu-id="c2c8c-146">Fixed issue with importing aliases</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="c2c8c-147">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="c2c8c-147">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="c2c8c-148">修复了导入别名的问题</span><span class="sxs-lookup"><span data-stu-id="c2c8c-148">Fixed issue with importing aliases</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="c2c8c-149">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="c2c8c-149">AzureRM.Resources</span></span>
* <span data-ttu-id="c2c8c-150">修复了导入别名的问题</span><span class="sxs-lookup"><span data-stu-id="c2c8c-150">Fixed issue with importing aliases</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="c2c8c-151">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c2c8c-151">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="c2c8c-152">为 Queue 添加了 EnableBatchedOperations 属性</span><span class="sxs-lookup"><span data-stu-id="c2c8c-152">Added EnableBatchedOperations property to Queue</span></span>
* <span data-ttu-id="c2c8c-153">为 Subscriptions 添加了 DeadLetteringOnFilterEvaluationExceptions 属性</span><span class="sxs-lookup"><span data-stu-id="c2c8c-153">Added DeadLetteringOnFilterEvaluationExceptions property to Subscriptions</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="c2c8c-154">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c2c8c-154">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="c2c8c-155">Service Fabric cmdlet 刷新</span><span class="sxs-lookup"><span data-stu-id="c2c8c-155">Service Fabric cmdlet refresh</span></span>
  - <span data-ttu-id="c2c8c-156">更新了 ARM 模板</span><span class="sxs-lookup"><span data-stu-id="c2c8c-156">Updated ARM templates</span></span>
  - <span data-ttu-id="c2c8c-157">失败的操作不再回滚</span><span class="sxs-lookup"><span data-stu-id="c2c8c-157">Failed operations no longer rollback</span></span>
  - <span data-ttu-id="c2c8c-158">Add-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="c2c8c-158">Add-AzureRmServiceFabricNodeType</span></span>
    - <span data-ttu-id="c2c8c-159">VM 默认为托管磁盘</span><span class="sxs-lookup"><span data-stu-id="c2c8c-159">VMs default to managed disks</span></span>
    - <span data-ttu-id="c2c8c-160">使用了现有 VMSS 子网</span><span class="sxs-lookup"><span data-stu-id="c2c8c-160">Existing VMSS subnet used</span></span>
    - <span data-ttu-id="c2c8c-161">所有操作都是幂等的</span><span class="sxs-lookup"><span data-stu-id="c2c8c-161">All operations are idempotent</span></span>
  - <span data-ttu-id="c2c8c-162">Remove-AzureRmServiceFabricNodeType 清除部分创建的 VMSS 和/或群集节点类型</span><span class="sxs-lookup"><span data-stu-id="c2c8c-162">Remove-AzureRmServiceFabricNodeType cleans up partially created VMSS and/or cluster node types</span></span>
  - <span data-ttu-id="c2c8c-163">修复了复杂属性类型的 PSCluster 对象输出</span><span class="sxs-lookup"><span data-stu-id="c2c8c-163">Fixed output of PSCluster object for complex property types</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="c2c8c-164">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="c2c8c-164">AzureRM.Sql</span></span>
* <span data-ttu-id="c2c8c-165">修复了导入别名的问题</span><span class="sxs-lookup"><span data-stu-id="c2c8c-165">Fixed issue with importing aliases</span></span>
* <span data-ttu-id="c2c8c-166">Get-AzureRmSqlServer、New-AzureRmSqlServer 和 Remove-AzureRmSqlServer 响应现在包括 FullyQualifiedDomainName 属性。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-166">Get-AzureRmSqlServer, New-AzureRmSqlServer, and Remove-AzureRmSqlServer response now includes FullyQualifiedDomainName property.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="c2c8c-167">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="c2c8c-167">AzureRM.Websites</span></span>
* <span data-ttu-id="c2c8c-168">修复了导入别名的问题</span><span class="sxs-lookup"><span data-stu-id="c2c8c-168">Fixed issue with importing aliases</span></span>
* <span data-ttu-id="c2c8c-169">New-AzureRMWebApp - 添加了参数集以用于简化的 WebApp 创建，并提供本地 Git 存储库支持。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-169">New-AzureRMWebApp - added parameter set for simplified WebApp creation, with local git repository support.</span></span>

## <a name="540---february-2018"></a><span data-ttu-id="c2c8c-170">5.4.0 - 2018 年 2 月</span><span class="sxs-lookup"><span data-stu-id="c2c8c-170">5.4.0 - February 2018</span></span>
#### <a name="azurermautomation"></a><span data-ttu-id="c2c8c-171">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="c2c8c-171">AzureRM.Automation</span></span>
* <span data-ttu-id="c2c8c-172">从 New-AzureRmAutomationModule 到 Import-AzureRmAutomationModule 添加了别名</span><span class="sxs-lookup"><span data-stu-id="c2c8c-172">Added alias from New-AzureRmAutomationModule to Import-AzureRmAutomationModule</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="c2c8c-173">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c2c8c-173">AzureRM.Compute</span></span>
* <span data-ttu-id="c2c8c-174">解决某些 Get cmdlet 的 ErrorAction 问题。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-174">Fix ErrorAction issue for some of Get cmdlets.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="c2c8c-175">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="c2c8c-175">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="c2c8c-176">应用 Azure 容器实例 SDK 2018-02-01</span><span class="sxs-lookup"><span data-stu-id="c2c8c-176">Apply Azure Container Instance SDK 2018-02-01</span></span>
    - <span data-ttu-id="c2c8c-177">支持 DNS 名称标签</span><span class="sxs-lookup"><span data-stu-id="c2c8c-177">Support DNS name label</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="c2c8c-178">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="c2c8c-178">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="c2c8c-179">修复了以前无法正常运行的所有 GET cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-179">Fixed all of the GET cmdlets which previously weren't working.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="c2c8c-180">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="c2c8c-180">AzureRM.EventHub</span></span>
* <span data-ttu-id="c2c8c-181">修复 Get-AzureRmEventHubGeoDRConfiguration 帮助中的 bug</span><span class="sxs-lookup"><span data-stu-id="c2c8c-181">Fix bug in Get-AzureRmEventHubGeoDRConfiguration help</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="c2c8c-182">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c2c8c-182">AzureRM.Network</span></span>
* <span data-ttu-id="c2c8c-183">添加了 cmdlet 以创建新的连接监视器</span><span class="sxs-lookup"><span data-stu-id="c2c8c-183">Added cmdlet to create a new connection monitor</span></span>
    - <span data-ttu-id="c2c8c-184">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c2c8c-184">New-AzureRmNetworkWatcherConnectionMonitor</span></span>
* <span data-ttu-id="c2c8c-185">添加了 cmdlet 以更新连接监视器</span><span class="sxs-lookup"><span data-stu-id="c2c8c-185">Added cmdlet to update a connection monitor</span></span>
    - <span data-ttu-id="c2c8c-186">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c2c8c-186">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>
* <span data-ttu-id="c2c8c-187">添加了 cmdlet 来获取连接监视器或连接监视器列表</span><span class="sxs-lookup"><span data-stu-id="c2c8c-187">Added cmdlet to get connection monitor or connection monitor list</span></span>
    - <span data-ttu-id="c2c8c-188">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c2c8c-188">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>
* <span data-ttu-id="c2c8c-189">添加了 cmdlet 以查询连接监视器</span><span class="sxs-lookup"><span data-stu-id="c2c8c-189">Added cmdlet to query connection monitor</span></span>
    - <span data-ttu-id="c2c8c-190">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="c2c8c-190">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>
* <span data-ttu-id="c2c8c-191">添加了 cmdlet 以启动连接监视器</span><span class="sxs-lookup"><span data-stu-id="c2c8c-191">Added cmdlet to start connection monitor</span></span>
    - <span data-ttu-id="c2c8c-192">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c2c8c-192">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>
* <span data-ttu-id="c2c8c-193">添加了 cmdlet 以停止连接监视器</span><span class="sxs-lookup"><span data-stu-id="c2c8c-193">Added cmdlet to stop connection monitor</span></span>
    - <span data-ttu-id="c2c8c-194">Stop-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c2c8c-194">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>
* <span data-ttu-id="c2c8c-195">添加了 cmdlet 以删除连接监视器</span><span class="sxs-lookup"><span data-stu-id="c2c8c-195">Added cmdlet to remove connection monitor</span></span>
    - <span data-ttu-id="c2c8c-196">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c2c8c-196">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>
* <span data-ttu-id="c2c8c-197">更新了 Set-AzureRmApplicationGatewayBackendAddressPool 文档以删除弃用的示例</span><span class="sxs-lookup"><span data-stu-id="c2c8c-197">Updated Set-AzureRmApplicationGatewayBackendAddressPool documentation to remove deprecated example</span></span>
* <span data-ttu-id="c2c8c-198">将 EnableHttp2 标志添加到了应用程序网关</span><span class="sxs-lookup"><span data-stu-id="c2c8c-198">Added EnableHttp2 flag to Application Gateway</span></span>
    - <span data-ttu-id="c2c8c-199">更新了 New-AzureRmApplicationGateway：添加了可选参数 -EnableHttp2</span><span class="sxs-lookup"><span data-stu-id="c2c8c-199">Updated New-AzureRmApplicationGateway: Added optional parameter -EnableHttp2</span></span>
* <span data-ttu-id="c2c8c-200">将 IpTags 添加到 PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c2c8c-200">Add IpTags to PublicIpAddress</span></span>
    - <span data-ttu-id="c2c8c-201">更新了 New-AzureRmPublicIpAddress：添加了 IpTags</span><span class="sxs-lookup"><span data-stu-id="c2c8c-201">Updated New-AzureRmPublicIpAddress: Added IpTags</span></span>
    - <span data-ttu-id="c2c8c-202">用于添加 Iptag 的 New-AzureRmPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="c2c8c-202">New-AzureRmPublicIpTag to add Iptag</span></span>
* <span data-ttu-id="c2c8c-203">在 RouteTable 和 effectiveRoute 中添加 DisableBgpRoutePropagation 属性。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-203">Add DisableBgpRoutePropagation property in RouteTable and effectiveRoute.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="c2c8c-204">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="c2c8c-204">AzureRM.Resources</span></span>
* <span data-ttu-id="c2c8c-205">Register-AzureRmProviderFeature：添加了文档中缺少的示例</span><span class="sxs-lookup"><span data-stu-id="c2c8c-205">Register-AzureRmProviderFeature: Added missing example in the docs</span></span>
* <span data-ttu-id="c2c8c-206">Register-AzureRmResourceProvider：添加了文档中缺少的示例</span><span class="sxs-lookup"><span data-stu-id="c2c8c-206">Register-AzureRmResourceProvider: Added missing example in the docs</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="c2c8c-207">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="c2c8c-207">AzureRM.Storage</span></span>
* <span data-ttu-id="c2c8c-208">在用于新建和设置存储帐户的 cmdlet（EnableEncryptionService 和 DisableEncryptionService）中废弃以下参数，因为静态加密在默认情况下处于启用状态，并且不能禁用。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-208">Obsolete following parameters in new and set Storage Account cmdlets: EnableEncryptionService and DisableEncryptionService, since Encryption at Rest is enabled by default and can't be disabled.</span></span>
    - <span data-ttu-id="c2c8c-209">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c2c8c-209">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="c2c8c-210">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c2c8c-210">Set-AzureRmStorageAccount</span></span>


## <a name="530---february-2018"></a><span data-ttu-id="c2c8c-211">5.3.0 - 2018 年 2 月</span><span class="sxs-lookup"><span data-stu-id="c2c8c-211">5.3.0 - February 2018</span></span>
### <a name="azurermprofile"></a><span data-ttu-id="c2c8c-212">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c2c8c-212">AzureRM.Profile</span></span>
* <span data-ttu-id="c2c8c-213">对 PowerShell 3 和 PowerShell 4 添加了弃用警告</span><span class="sxs-lookup"><span data-stu-id="c2c8c-213">Added deprecation warning for PowerShell 3 and 4</span></span>
* <span data-ttu-id="c2c8c-214">`Add-AzureRmAccount` 已重命名为 `Connect-AzureRmAccount`；为旧的 cmdlet 名称添加了别名，并将其他别名（`Login-AzAccount` 和 `Login-AzureRmAccount`）重定向到了新的 cmdlet 名称。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-214">`Add-AzureRmAccount` has been renamed as `Connect-AzureRmAccount`; an alias has been added for the old cmdlet name, and other aliases (`Login-AzAccount` and `Login-AzureRmAccount`) have been redirected to the new cmdlet name.</span></span>
* <span data-ttu-id="c2c8c-215">`Remove-AzureRmAccount` 已重命名为 `Disconnect-AzureRmAccount`；为旧的 cmdlet 名称添加了别名，并将其他别名（`Logout-AzAccount` 和 `Logout-AzureRmAccount`）重定向到了新的 cmdlet 名称。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-215">`Remove-AzureRmAccount` has been renamed as `Disconnect-AzureRmAccount`; an alias has been added for the old cmdlet name, and other aliases (`Logout-AzAccount` and `Logout-AzureRmAccount`) have been redirected to the new cmdlet name.</span></span>
* <span data-ttu-id="c2c8c-216">更正了资源字符串以使用 `Connect-AzureRmAccount` 而不是 `Login-AzureRmAccount`</span><span class="sxs-lookup"><span data-stu-id="c2c8c-216">Corrected Resource Strings to use `Connect-AzureRmAccount` instead of `Login-AzureRmAccount`</span></span>
* <span data-ttu-id="c2c8c-217">`Add-AzureRmEnvironment` 和 `Set-AzureRmEnvironment`</span><span class="sxs-lookup"><span data-stu-id="c2c8c-217">`Add-AzureRmEnvironment` and `Set-AzureRmEnvironment`</span></span>
  - <span data-ttu-id="c2c8c-218">添加了 `-AzureOperationalInsightsEndpoint` 和 `-AzureOperationalInsightsEndpointResourceId` 作为要用于 OperationalInsights 数据平面 RP 的参数。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-218">Added `-AzureOperationalInsightsEndpoint` and `-AzureOperationalInsightsEndpointResourceId` as parameters for use with OperationalInsights data plane RP.</span></span>

### <a name="azurermanalysisservices"></a><span data-ttu-id="c2c8c-219">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="c2c8c-219">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="c2c8c-220">更正了 `Login-AzureRmAccount` 的用法以使用 `Connect-AzureRmAccount`</span><span class="sxs-lookup"><span data-stu-id="c2c8c-220">Corrected usage of `Login-AzureRmAccount` to use `Connect-AzureRmAccount`</span></span>

### <a name="azurermcompute"></a><span data-ttu-id="c2c8c-221">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c2c8c-221">AzureRM.Compute</span></span>
* <span data-ttu-id="c2c8c-222">向 `New-AzureRmVM` 的简化参数集添加了 `-AvailabilitySetName` 参数。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-222">Added `-AvailabilitySetName` parameter to the simplified parameterset of `New-AzureRmVM`.</span></span>
* <span data-ttu-id="c2c8c-223">更正了 `Login-AzureRmAccount` 的用法以使用 `Connect-AzureRmAccount`</span><span class="sxs-lookup"><span data-stu-id="c2c8c-223">Corrected usage of `Login-AzureRmAccount` to use `Connect-AzureRmAccount`</span></span>
* <span data-ttu-id="c2c8c-224">对 VM 和 VM 规模集的用户分配标识支持</span><span class="sxs-lookup"><span data-stu-id="c2c8c-224">User assigned identity support for VM and VM scale set</span></span>
    - <span data-ttu-id="c2c8c-225">将 `-IdentityType` 和 `-IdentityId` 参数添加到了 `New-AzureRmVMConfig`、`New-AzureRmVmssConfig`、`Update-AzureRmVM` 和 `Update-AzureRmVmss`</span><span class="sxs-lookup"><span data-stu-id="c2c8c-225">`-IdentityType` and `-IdentityId` parameters are added to `New-AzureRmVMConfig`, `New-AzureRmVmssConfig`, `Update-AzureRmVM` and `Update-AzureRmVmss`</span></span>
* <span data-ttu-id="c2c8c-226">为 `Add-AzureRmVmssNetworkInterfaceConfig` 添加了 `-EnableIPForwarding` 参数</span><span class="sxs-lookup"><span data-stu-id="c2c8c-226">Added `-EnableIPForwarding` parameter to `Add-AzureRmVmssNetworkInterfaceConfig`</span></span>
* <span data-ttu-id="c2c8c-227">为 `New-AzureRmVmssConfig` 添加了 `-Priority` 参数</span><span class="sxs-lookup"><span data-stu-id="c2c8c-227">Added `-Priority` parameter to `New-AzureRmVmssConfig`</span></span>

### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="c2c8c-228">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="c2c8c-228">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="c2c8c-229">更正了 `Login-AzureRmAccount` 的用法以使用 `Connect-AzureRmAccount`</span><span class="sxs-lookup"><span data-stu-id="c2c8c-229">Corrected usage of `Login-AzureRmAccount` to use `Connect-AzureRmAccount`</span></span>

### <a name="azurermdatalakestore"></a><span data-ttu-id="c2c8c-230">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c2c8c-230">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="c2c8c-231">更正了 `Login-AzureRmAccount` 的用法以使用 `Connect-AzureRmAccount`</span><span class="sxs-lookup"><span data-stu-id="c2c8c-231">Corrected usage of `Login-AzureRmAccount` to use `Connect-AzureRmAccount`</span></span>
* <span data-ttu-id="c2c8c-232">更正了未使用 `Login-AzureRmAccount` 登录便运行 `Test-AzureRmDataLakeStoreAccount` 时显示的此 cmdlet 的错误消息</span><span class="sxs-lookup"><span data-stu-id="c2c8c-232">Corrected the error message of `Test-AzureRmDataLakeStoreAccount` when running this cmdlet without having logged in with `Login-AzureRmAccount`</span></span>

### <a name="azurermeventgrid"></a><span data-ttu-id="c2c8c-233">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="c2c8c-233">AzureRM.EventGrid</span></span>
* <span data-ttu-id="c2c8c-234">已更新以使用 2018-01-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-234">Updated to use the 2018-01-01 API version.</span></span>

### <a name="azurermeventhub"></a><span data-ttu-id="c2c8c-235">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="c2c8c-235">AzureRM.EventHub</span></span>
* <span data-ttu-id="c2c8c-236">添加了以下新命令以便执行异地灾难恢复操作。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-236">Added below new commands for Geo Disaster Recovery operations.</span></span>
    <span data-ttu-id="c2c8c-237">- 创建新别名（灾难恢复配置）：- `New-AzureRmEventHubGeoDRConfiguration` -检索别名（灾难恢复配置）：- `Get-AzureRmEventHubGeoDRConfiguration` - 禁用灾难恢复并停止将主要命名空间中的更改复制到辅助命名空间 - `Set-AzureRmEventHubGeoDRConfigurationBreakPair`- 调用灾难恢复故障转移并重新配置别名使其指向辅助命名空间 - `Set-AzureRmEventHubGeoDRConfigurationFailOver` - 删除别名（灾难恢复配置）- `Remove-AzureRmEventHubGeoDRConfiguration`</span><span class="sxs-lookup"><span data-stu-id="c2c8c-237">-Creating a new Alias(Disaster Recovery configuration): - `New-AzureRmEventHubGeoDRConfiguration` -Retrieve Alias(Disaster Recovery configuration) : - `Get-AzureRmEventHubGeoDRConfiguration` -Disabling the Disaster Recovery and stops replicating changes from primary to secondary namespaces - `Set-AzureRmEventHubGeoDRConfigurationBreakPair` -Invoking Disaster Recovery failover and reconfigure the alias to point to the secondary namespace - `Set-AzureRmEventHubGeoDRConfigurationFailOver` -Deleting an Alias(Disaster Recovery configuration) - `Remove-AzureRmEventHubGeoDRConfiguration`</span></span>
* <span data-ttu-id="c2c8c-238">添加了以下新命令，用于检查命名空间名称和 GeoDr 配置名称 - 别名可用性。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-238">Added below new commands for checking the Namespace Name and GeoDr Configuration Name - Alias availability.</span></span>
    <span data-ttu-id="c2c8c-239">-检查命名空间名称或别名（灾难恢复配置）名称的可用性：- `Test-AzureRmEventHubName`</span><span class="sxs-lookup"><span data-stu-id="c2c8c-239">-Check the Availability of Namespace name or Alias(Disaster Recovery configuration) name: - `Test-AzureRmEventHubName`</span></span>

### <a name="azurerminsights"></a><span data-ttu-id="c2c8c-240">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="c2c8c-240">AzureRM.Insights</span></span>
* <span data-ttu-id="c2c8c-241">更正了 `Login-AzureRmAccount` 的用法以使用 `Connect-AzureRmAccount`</span><span class="sxs-lookup"><span data-stu-id="c2c8c-241">Corrected usage of `Login-AzureRmAccount` to use `Connect-AzureRmAccount`</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="c2c8c-242">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c2c8c-242">AzureRM.KeyVault</span></span>
* <span data-ttu-id="c2c8c-243">更正了 `Login-AzureRmAccount` 的用法以使用 `Connect-AzureRmAccount`</span><span class="sxs-lookup"><span data-stu-id="c2c8c-243">Corrected usage of `Login-AzureRmAccount` to use `Connect-AzureRmAccount`</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="c2c8c-244">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c2c8c-244">AzureRM.Network</span></span>
* <span data-ttu-id="c2c8c-245">修复了覆盖消息“是否确实要覆盖资源”</span><span class="sxs-lookup"><span data-stu-id="c2c8c-245">Fix overwrite message 'Are you sure you want to overwriteresource'</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="c2c8c-246">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="c2c8c-246">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="c2c8c-247">通过 `Invoke-AzureRmOperationalInsightsQuery` 添加了对 V2 API 查询的支持。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-247">Added support for V2 API querying via `Invoke-AzureRmOperationalInsightsQuery`.</span></span> <span data-ttu-id="c2c8c-248">有关新 API 的详细信息，请参阅 [https://dev.loganalytics.io/](https://dev.loganalytics.io/)。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-248">See [https://dev.loganalytics.io/](https://dev.loganalytics.io/) for more info on the new API.</span></span>

### <a name="azurermresources"></a><span data-ttu-id="c2c8c-249">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="c2c8c-249">AzureRM.Resources</span></span>
* <span data-ttu-id="c2c8c-250">`Get-AzureRmADServicePrincipal`：从默认 Empty 参数集中删除了 `-ServicePrincipalName`，因为它对于 SPN 参数集是冗余的</span><span class="sxs-lookup"><span data-stu-id="c2c8c-250">`Get-AzureRmADServicePrincipal`: Removed `-ServicePrincipalName` from the default Empty parameter set as it was redundant with the SPN parameter set</span></span>

### <a name="azurermservicebus"></a><span data-ttu-id="c2c8c-251">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c2c8c-251">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="c2c8c-252">为 `Remove-AzureRmServiceBusRule` 和 `Get-AzureRmServiceBusKey` 添加了功能修复</span><span class="sxs-lookup"><span data-stu-id="c2c8c-252">Added functionality fix for `Remove-AzureRmServiceBusRule` and `Get-AzureRmServiceBusKey`</span></span>
* <span data-ttu-id="c2c8c-253">添加了以下新 cmdlet 以便执行异地灾难恢复操作。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-253">Added below new commandlets for Geo Disaster Recovery operations.</span></span>
    <span data-ttu-id="c2c8c-254">- 创建新别名（灾难恢复配置）：- `New-AzureRmServiceBusDRConfigurations` -检索别名（灾难恢复配置）：- `Get-AzureRmServiceBusDRConfigurations` - 禁用灾难恢复并停止将主要命名空间中的更改复制到辅助命名空间 - `Set-AzureRmServiceBusDRConfigurationsBreakPairing`- 调用灾难恢复故障转移并重新配置别名使其指向辅助命名空间 - `Set-AzureRmServiceBusDRConfigurationsFailOver` - 删除别名（灾难恢复配置）- `Remove-AzureRmServiceBusDRConfigurations`</span><span class="sxs-lookup"><span data-stu-id="c2c8c-254">-Creating a new Alias(Disaster Recovery configuration): - `New-AzureRmServiceBusDRConfigurations` -Retrieve Alias(Disaster Recovery configuration) : - `Get-AzureRmServiceBusDRConfigurations` -Disabling the Disaster Recovery and stops replicating changes from primary to secondary namespaces - `Set-AzureRmServiceBusDRConfigurationsBreakPairing` -Invoking Disaster Recovery failover and reconfigure the alias to point to the secondary namespace - `Set-AzureRmServiceBusDRConfigurationsFailOver` -Deleting an Alias(Disaster Recovery configuration) - `Remove-AzureRmServiceBusDRConfigurations`</span></span>
* <span data-ttu-id="c2c8c-255">更新了 `Test-AzureRmServiceBusName` cmdlet 以支持异地灾难恢复 - 别名检查可用性操作。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-255">Updated `Test-AzureRmServiceBusName` commandlets to support Geo Disaster Recovery - Alias name check availability operations.</span></span>
    <span data-ttu-id="c2c8c-256">-检查命名空间名称或别名（灾难恢复配置）名称的可用性：- `Test-AzureRmServiceBusName`</span><span class="sxs-lookup"><span data-stu-id="c2c8c-256">-Check the Availability of Namespace name or Alias(Disaster Recovery configuration) name: - `Test-AzureRmServiceBusName`</span></span>

### <a name="azurermusageaggregates"></a><span data-ttu-id="c2c8c-257">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="c2c8c-257">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="c2c8c-258">更正了 `Login-AzureRmAccount` 的用法以使用 `Connect-AzureRmAccount`</span><span class="sxs-lookup"><span data-stu-id="c2c8c-258">Corrected usage of `Login-AzureRmAccount` to use `Connect-AzureRmAccount`</span></span>

## <a name="520---january-2018"></a><span data-ttu-id="c2c8c-259">5.2.0 - 2018 年 1 月</span><span class="sxs-lookup"><span data-stu-id="c2c8c-259">5.2.0 - January 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="c2c8c-260">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c2c8c-260">AzureRM.Profile</span></span>
* <span data-ttu-id="c2c8c-261">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="c2c8c-261">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="c2c8c-262">Add-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="c2c8c-262">Add-AzureRmAccount</span></span>
  * <span data-ttu-id="c2c8c-263">添加了 -MSI 登录名，用于通过当前 VM/服务的托管服务标识的凭据进行身份验证</span><span class="sxs-lookup"><span data-stu-id="c2c8c-263">Added -MSI login for authenticationg using the credentials of the Managed Service Identity of the current VM / Service</span></span>
  * <span data-ttu-id="c2c8c-264">修复了使用用户提供的访问令牌登录时存在的 KeyVault 身份验证问题</span><span class="sxs-lookup"><span data-stu-id="c2c8c-264">Fixed KeyVault Authentication when logging in with user-provided access tokens</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="c2c8c-265">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="c2c8c-265">Azure.Storage</span></span>
* <span data-ttu-id="c2c8c-266">添加了 cmdlet 用于获取和设置存储服务属性</span><span class="sxs-lookup"><span data-stu-id="c2c8c-266">Add cmdlets to get and set Storage service properties</span></span>
    - <span data-ttu-id="c2c8c-267">Get-AzureStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="c2c8c-267">Get-AzureStorageServiceProperty</span></span>
    - <span data-ttu-id="c2c8c-268">Update-AzureStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="c2c8c-268">Update-AzureStorageServiceProperty</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="c2c8c-269">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="c2c8c-269">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="c2c8c-270">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="c2c8c-270">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="c2c8c-271">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c2c8c-271">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="c2c8c-272">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="c2c8c-272">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="c2c8c-273">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="c2c8c-273">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="c2c8c-274">已弃用 -Tags，对 New-AzureRmApiManagementProperty、Set-AzureRmApiManagementProperty 和 New-AzureRmApiManagement 改用 -Tag</span><span class="sxs-lookup"><span data-stu-id="c2c8c-274">Obsoleted -Tags in favor of -Tag for New-AzureRmApiManagementProperty, Set-AzureRmApiManagementProperty, and New-AzureRmApiManagement</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="c2c8c-275">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="c2c8c-275">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="c2c8c-276">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="c2c8c-276">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="c2c8c-277">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="c2c8c-277">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="c2c8c-278">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="c2c8c-278">AzureRM.Automation</span></span>
* <span data-ttu-id="c2c8c-279">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="c2c8c-279">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="c2c8c-280">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="c2c8c-280">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="c2c8c-281">已弃用 -Tags，对 Set-AzureRmAutomationRunbook 改用 -Tag</span><span class="sxs-lookup"><span data-stu-id="c2c8c-281">Obsoleted -Tags in favor of -Tag for Set-AzureRmAutomationRunbook</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="c2c8c-282">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="c2c8c-282">AzureRM.Backup</span></span>
* <span data-ttu-id="c2c8c-283">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="c2c8c-283">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="c2c8c-284">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="c2c8c-284">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="c2c8c-285">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="c2c8c-285">AzureRM.Batch</span></span>
* <span data-ttu-id="c2c8c-286">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="c2c8c-286">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="c2c8c-287">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="c2c8c-287">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="c2c8c-288">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="c2c8c-288">AzureRM.Cdn</span></span>
* <span data-ttu-id="c2c8c-289">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="c2c8c-289">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="c2c8c-290">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="c2c8c-290">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="c2c8c-291">已弃用 -Tags，对 New-AzureRmCdnEndpoint 和 New-AzureRmCdnProfile 改用 -Tag</span><span class="sxs-lookup"><span data-stu-id="c2c8c-291">Obsoleted -Tags in favor of -Tag for New-AzureRmCdnEndpoint and New-AzureRmCdnProfile</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="c2c8c-292">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c2c8c-292">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="c2c8c-293">与认知服务管理 SDK 版本 3.0.0 集成。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-293">Integrate with Cognitive Services Management SDK version 3.0.0.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="c2c8c-294">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c2c8c-294">AzureRM.Compute</span></span>
* <span data-ttu-id="c2c8c-295">为 New-AzureRmVmss 添加了简化的参数集，用于通过智能默认值创建虚拟机规模集和所有必需的资源</span><span class="sxs-lookup"><span data-stu-id="c2c8c-295">Added simplified parameter set to New-AzureRmVmss, which creates a Virtual Machine Scale Set and all required resources using smart defaults</span></span>
* <span data-ttu-id="c2c8c-296">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="c2c8c-296">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="c2c8c-297">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="c2c8c-297">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="c2c8c-298">已弃用 -Tags，对 New-AzureRmVm 和 Update-AzureRmVm 改用 -Tag</span><span class="sxs-lookup"><span data-stu-id="c2c8c-298">Obsoleted -Tags in favor of -Tag for New-AzureRmVm and Update-AzureRmVm</span></span>
* <span data-ttu-id="c2c8c-299">修复了 Zone 受限制时的 Get-AzureRmComputeResourceSku cmdlet 问题。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-299">Fixed Get-AzureRmComputeResourceSku cmdlet when Zone is included in restriction.</span></span>
* <span data-ttu-id="c2c8c-300">为 Azure Monitor 接收器支持更新了诊断代理配置架构。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-300">Updated Diagnostics Agent configuration schema for Azure Monitor sink support.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="c2c8c-301">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="c2c8c-301">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="c2c8c-302">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="c2c8c-302">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="c2c8c-303">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="c2c8c-303">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="c2c8c-304">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c2c8c-304">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="c2c8c-305">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="c2c8c-305">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="c2c8c-306">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="c2c8c-306">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="c2c8c-307">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="c2c8c-307">AzureRM.DataFactories</span></span>
* <span data-ttu-id="c2c8c-308">对所有数据存储链接服务启用了 Azure Key Vault 支持</span><span class="sxs-lookup"><span data-stu-id="c2c8c-308">Enabled Azure Key Vault support for all data store linked services</span></span>
* <span data-ttu-id="c2c8c-309">添加了 Azure SSIS 集成运行时的许可证类型属性</span><span class="sxs-lookup"><span data-stu-id="c2c8c-309">Added license type property for Azure SSIS integration runtime</span></span>
* <span data-ttu-id="c2c8c-310">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="c2c8c-310">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="c2c8c-311">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="c2c8c-311">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="c2c8c-312">已弃用 -Tags，对 New-AzureRmDataFactory 改用 -Tag</span><span class="sxs-lookup"><span data-stu-id="c2c8c-312">Obsoleted -Tags in favor of -Tag for New-AzureRmDataFactory</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="c2c8c-313">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="c2c8c-313">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="c2c8c-314">对所有数据存储链接服务启用了 Azure Key Vault 支持</span><span class="sxs-lookup"><span data-stu-id="c2c8c-314">Enabled Azure Key Vault support for all data store linked services</span></span>
* <span data-ttu-id="c2c8c-315">添加了 Azure SSIS 集成运行时的许可证类型属性</span><span class="sxs-lookup"><span data-stu-id="c2c8c-315">Added license type property for Azure SSIS integration runtime</span></span>
* <span data-ttu-id="c2c8c-316">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="c2c8c-316">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="c2c8c-317">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="c2c8c-317">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="c2c8c-318">为“Set-AzureRmDataFactoryV2IntegrationRuntime”cmd 添加了参数“LicenseType”，以启用 AHUB 功能</span><span class="sxs-lookup"><span data-stu-id="c2c8c-318">Add parameter "LicenseType" for "Set-AzureRmDataFactoryV2IntegrationRuntime" cmd to enable AHUB functionality</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="c2c8c-319">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="c2c8c-319">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="c2c8c-320">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="c2c8c-320">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="c2c8c-321">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="c2c8c-321">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="c2c8c-322">已弃用 -Tags，对 New-AzureRmDataLakeAnalyticsAccount 和 Set-AzureRmDataLakeAnalyticsAccount 改用 -Tag</span><span class="sxs-lookup"><span data-stu-id="c2c8c-322">Obsoleted -Tags in favor of -Tag for New-AzureRmDataLakeAnalyticsAccount and Set-AzureRmDataLakeAnalyticsAccount</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="c2c8c-323">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c2c8c-323">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="c2c8c-324">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="c2c8c-324">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="c2c8c-325">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="c2c8c-325">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="c2c8c-326">已弃用 -Tags，对 New-AzureRmDataLakeStoreAccount 和 Set-AzureRmDataLakeStoreAccount 改用 -Tag</span><span class="sxs-lookup"><span data-stu-id="c2c8c-326">Obsoleted -Tags in favor of -Tag for New-AzureRmDataLakeStoreAccount and Set-AzureRmDataLakeStoreAccount</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="c2c8c-327">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="c2c8c-327">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="c2c8c-328">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="c2c8c-328">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="c2c8c-329">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="c2c8c-329">AzureRM.Dns</span></span>
* <span data-ttu-id="c2c8c-330">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="c2c8c-330">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="c2c8c-331">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="c2c8c-331">AzureRM.EventGrid</span></span>
* <span data-ttu-id="c2c8c-332">添加了以下新的 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="c2c8c-332">Added the following new cmdlet:</span></span>
    - <span data-ttu-id="c2c8c-333">Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="c2c8c-333">Update-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="c2c8c-334">更新了事件网格事件订阅的属性。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-334">Update the properties of an Event Grid event subscription.</span></span>
* <span data-ttu-id="c2c8c-335">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="c2c8c-335">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="c2c8c-336">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="c2c8c-336">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="c2c8c-337">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="c2c8c-337">AzureRM.EventHub</span></span>
* <span data-ttu-id="c2c8c-338">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="c2c8c-338">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="c2c8c-339">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="c2c8c-339">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="c2c8c-340">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="c2c8c-340">AzureRM.HDInsight</span></span>
* <span data-ttu-id="c2c8c-341">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="c2c8c-341">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="c2c8c-342">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="c2c8c-342">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="c2c8c-343">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="c2c8c-343">AzureRM.Insights</span></span>
* <span data-ttu-id="c2c8c-344">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="c2c8c-344">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="c2c8c-345">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="c2c8c-345">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="c2c8c-346">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="c2c8c-346">AzureRM.IotHub</span></span>
* <span data-ttu-id="c2c8c-347">添加了对 IoTHub cmdlet 的 Certificate 支持</span><span class="sxs-lookup"><span data-stu-id="c2c8c-347">Add Certificate support for IoTHub cmdlets</span></span>
* <span data-ttu-id="c2c8c-348">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="c2c8c-348">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="c2c8c-349">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="c2c8c-349">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="c2c8c-350">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c2c8c-350">AzureRM.KeyVault</span></span>
* <span data-ttu-id="c2c8c-351">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="c2c8c-351">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="c2c8c-352">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="c2c8c-352">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="c2c8c-353">添加了对长时间运行的 KeyVault cmdlet 的 -AsJob 支持。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-353">Added -AsJob support for long-running KeyVault cmdlets.</span></span> <span data-ttu-id="c2c8c-354">允许选定的 cmdlet 在后台运行并返回可跟踪和控制进度的作业。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-354">Allows selected cmdlets to run in the background and return a job to track and control progress.</span></span>
    * <span data-ttu-id="c2c8c-355">受影响的 cmdlet 为：Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="c2c8c-355">Affected cmdlet is: Remove-AzureRmKeyVault</span></span>
* <span data-ttu-id="c2c8c-356">修复了 Set-AzureRmKeyVaultAccessPolicy 的 bug：AAD 筛选器将 SPN 设置为提供的 UPN，而不是设置 UPN</span><span class="sxs-lookup"><span data-stu-id="c2c8c-356">Fixed bug in Set-AzureRmKeyVaultAccessPolicy where the AAD filter was setting SPN to the provided UPN, rather than setting the UPN</span></span>
   - <span data-ttu-id="c2c8c-357">有关详细信息，请参阅以下问题：https://github.com/Azure/azure-powershell/issues/5201</span><span class="sxs-lookup"><span data-stu-id="c2c8c-357">See the following issue for more information: https://github.com/Azure/azure-powershell/issues/5201</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="c2c8c-358">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="c2c8c-358">AzureRM.LogicApp</span></span>
* <span data-ttu-id="c2c8c-359">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="c2c8c-359">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="c2c8c-360">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="c2c8c-360">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="c2c8c-361">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="c2c8c-361">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="c2c8c-362">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="c2c8c-362">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="c2c8c-363">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="c2c8c-363">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="c2c8c-364">已弃用 -Tags，对 Update-AzureRmMlCommitmentPlan 改用 -Tag</span><span class="sxs-lookup"><span data-stu-id="c2c8c-364">Obsoleted -Tags in favor of -Tag for Update-AzureRmMlCommitmentPlan</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="c2c8c-365">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="c2c8c-365">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="c2c8c-366">将 IncludeAllResources 参数添加到了 Remove-AzureRmMlOpCluster cmdlet</span><span class="sxs-lookup"><span data-stu-id="c2c8c-366">Add IncludeAllResources parameter to Remove-AzureRmMlOpCluster cmdlet</span></span>
    - <span data-ttu-id="c2c8c-367">使用此开关参数会删除最初在群集中创建的所有资源</span><span class="sxs-lookup"><span data-stu-id="c2c8c-367">Using this switch parameter will remove all resources that were created with the cluster originally</span></span>
* <span data-ttu-id="c2c8c-368">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="c2c8c-368">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="c2c8c-369">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="c2c8c-369">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="c2c8c-370">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="c2c8c-370">AzureRM.Media</span></span>
* <span data-ttu-id="c2c8c-371">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="c2c8c-371">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="c2c8c-372">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="c2c8c-372">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="c2c8c-373">已弃用 -Tags，对 Set-AzureRmMediaService 和 New-AzureRmMediaService 改用 -Tag</span><span class="sxs-lookup"><span data-stu-id="c2c8c-373">Obsoleted -Tags in favor of -Tag for Set-AzureRmMediaService and New-AzureRmMediaService</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="c2c8c-374">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c2c8c-374">AzureRM.Network</span></span>
* <span data-ttu-id="c2c8c-375">添加了对长时间运行的 Network cmdlet 的 -AsJob 支持。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-375">Added -AsJob support for long-running Network cmdlets.</span></span> <span data-ttu-id="c2c8c-376">允许选定的 cmdlet 在后台运行并返回可跟踪和控制进度的作业。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-376">Allows selected cmdlets to run in the background and return a job to track and control progress.</span></span>
* <span data-ttu-id="c2c8c-377">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="c2c8c-377">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="c2c8c-378">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="c2c8c-378">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="c2c8c-379">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="c2c8c-379">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="c2c8c-380">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="c2c8c-380">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="c2c8c-381">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="c2c8c-381">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="c2c8c-382">已弃用 -Tags，对 New-AzureRmNotificationHubsNamespace 和 Set-AzureRmNotificationHubsNamespace 改用 -Tag</span><span class="sxs-lookup"><span data-stu-id="c2c8c-382">Obsoleted -Tags in favor of -Tag for New-AzureRmNotificationHubsNamespace and Set-AzureRmNotificationHubsNamespace</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="c2c8c-383">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="c2c8c-383">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="c2c8c-384">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="c2c8c-384">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="c2c8c-385">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="c2c8c-385">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="c2c8c-386">已弃用 -Tags，对 New-AzureRmOperationalInsightsSavedSearch、Set-AzureRmOperationalInsightsSavedSearch、New-AzureRmOperationalInsightsWorkspace 和 Set-AzureRmOperationalInsightsWorkspace 改用 -Tag</span><span class="sxs-lookup"><span data-stu-id="c2c8c-386">Obsoleted -Tags in favor of -Tag for New-AzureRmOperationalInsightsSavedSearch, Set-AzureRmOperationalInsightsSavedSearch, New-AzureRmOperationalInsightsWorkspace, and Set-AzureRmOperationalInsightsWorkspace</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="c2c8c-387">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="c2c8c-387">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="c2c8c-388">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="c2c8c-388">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="c2c8c-389">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="c2c8c-389">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="c2c8c-390">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c2c8c-390">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="c2c8c-391">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="c2c8c-391">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="c2c8c-392">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="c2c8c-392">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="c2c8c-393">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="c2c8c-393">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="c2c8c-394">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="c2c8c-394">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="c2c8c-395">为 Restore-AzureRmRecoveryServicesBackupItem cmdlet 添加了 -UseOriginalStorageAccount 选项。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-395">Added -UseOriginalStorageAccount option to the Restore-AzureRmRecoveryServicesBackupItem cmdlet.</span></span>
    - <span data-ttu-id="c2c8c-396">启用此标志会导致将磁盘还原到其原始存储帐户，从而让用户尽量将还原后的 VM 的配置接近原始 VM。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-396">Enabling this flag results in restoring disks to their original storage accounts which allows users to maintain the configuration of restored VM as close to the original VMs as possible.</span></span>
    - <span data-ttu-id="c2c8c-397">此外，这还有助于提高还原操作的性能。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-397">It also helps in improving the performance of the restore operation.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="c2c8c-398">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="c2c8c-398">AzureRM.RedisCache</span></span>
* <span data-ttu-id="c2c8c-399">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="c2c8c-399">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="c2c8c-400">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="c2c8c-400">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="c2c8c-401">为防火墙规则添加了 3 个新的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="c2c8c-401">Added  3 new cmdlets for firewall rules</span></span>
* <span data-ttu-id="c2c8c-402">为异地复制添加了 3 个新的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="c2c8c-402">Added  3 new cmdlets for geo replication</span></span>
* <span data-ttu-id="c2c8c-403">添加了对区域和标记的支持</span><span class="sxs-lookup"><span data-stu-id="c2c8c-403">Added support for zones and tags</span></span>
* <span data-ttu-id="c2c8c-404">尽量将 ResourceGroup 用作可选选项。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-404">Make ResourceGroup as optional whenever possible.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="c2c8c-405">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="c2c8c-405">AzureRM.Relay</span></span>
* <span data-ttu-id="c2c8c-406">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="c2c8c-406">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="c2c8c-407">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="c2c8c-407">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="c2c8c-408">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="c2c8c-408">AzureRM.Resources</span></span>
* <span data-ttu-id="c2c8c-409">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="c2c8c-409">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="c2c8c-410">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="c2c8c-410">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="c2c8c-411">添加了对长时间运行的 Resources cmdlet 的 -AsJob 支持。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-411">Added -AsJob support for long-running Resources cmdlets.</span></span> <span data-ttu-id="c2c8c-412">允许选定的 cmdlet 在后台运行并返回可跟踪和控制进度的作业。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-412">Allows selected cmdlets to run in the background and return a job to track and control progress.</span></span>
* <span data-ttu-id="c2c8c-413">将别名从 Get-AzureRmProviderOperation 更改为 Get-AzureRmResourceProviderAction，以符合命名约定</span><span class="sxs-lookup"><span data-stu-id="c2c8c-413">Added alias from Get-AzureRmProviderOperation to Get-AzureRmResourceProviderAction to conform with naming conventions</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="c2c8c-414">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="c2c8c-414">AzureRM.Scheduler</span></span>
* <span data-ttu-id="c2c8c-415">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="c2c8c-415">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="c2c8c-416">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="c2c8c-416">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermservermanagement"></a><span data-ttu-id="c2c8c-417">AzureRM.ServerManagement</span><span class="sxs-lookup"><span data-stu-id="c2c8c-417">AzureRM.ServerManagement</span></span>
* <span data-ttu-id="c2c8c-418">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="c2c8c-418">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="c2c8c-419">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="c2c8c-419">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="c2c8c-420">已弃用 -Tags，对 New-AzureRmServerManagementNode 和 New-AzureRmServerManagementGateway 改用 -Tag</span><span class="sxs-lookup"><span data-stu-id="c2c8c-420">Obsoleted -Tags in favor of -Tag for New-AzureRmServerManagementNode and New-AzureRmServerManagementGateway</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="c2c8c-421">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c2c8c-421">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="c2c8c-422">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="c2c8c-422">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="c2c8c-423">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="c2c8c-423">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="c2c8c-424">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c2c8c-424">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="c2c8c-425">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="c2c8c-425">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="c2c8c-426">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="c2c8c-426">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermsiterecovery"></a><span data-ttu-id="c2c8c-427">AzureRM.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="c2c8c-427">AzureRM.SiteRecovery</span></span>
* <span data-ttu-id="c2c8c-428">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="c2c8c-428">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="c2c8c-429">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="c2c8c-429">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="c2c8c-430">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="c2c8c-430">AzureRM.Sql</span></span>
* <span data-ttu-id="c2c8c-431">更新了 Auditing 命令参数说明</span><span class="sxs-lookup"><span data-stu-id="c2c8c-431">Update the Auditing commands parameters description</span></span>
* <span data-ttu-id="c2c8c-432">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="c2c8c-432">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="c2c8c-433">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="c2c8c-433">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="c2c8c-434">为长时间运行的 cmdlet 添加了 -AsJob 参数</span><span class="sxs-lookup"><span data-stu-id="c2c8c-434">Added -AsJob parameter to long running cmdlets</span></span>
* <span data-ttu-id="c2c8c-435">已弃用 Get-AzureRmSqlServiceObjective 的 -DatabaseName 参数</span><span class="sxs-lookup"><span data-stu-id="c2c8c-435">Obsoleted -DatabaseName parameter from Get-AzureRmSqlServiceObjective</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="c2c8c-436">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="c2c8c-436">AzureRM.Storage</span></span>
* <span data-ttu-id="c2c8c-437">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="c2c8c-437">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="c2c8c-438">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="c2c8c-438">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="c2c8c-439">修复了结合 -EnableEncryptionService None 参数运行 cmdlet New-AzureRMStorageAccount 时的空引用问题</span><span class="sxs-lookup"><span data-stu-id="c2c8c-439">Fix a null reference issue of run cmdlet New-AzureRMStorageAccount with parameter -EnableEncryptionService None</span></span>
* <span data-ttu-id="c2c8c-440">添加了对长时间运行的 Storage cmdlet 的 -AsJob 支持。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-440">Added -AsJob support for long-running Storage cmdlets.</span></span> <span data-ttu-id="c2c8c-441">允许选定的 cmdlet 在后台运行并返回可跟踪和控制进度的作业。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-441">Allows selected cmdlets to run in the background and return a job to track and control progress.</span></span>
    - <span data-ttu-id="c2c8c-442">受影响的 cmdlet 为针对存储帐户和存储帐户网络规则的 New-、Remove-、Add- 和 Update-。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-442">Affected cmdlets are New-, Remove-, Add-, and Update- for Storage Account and Storage Account Network Rule.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="c2c8c-443">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="c2c8c-443">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="c2c8c-444">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="c2c8c-444">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="c2c8c-445">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="c2c8c-445">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="c2c8c-446">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="c2c8c-446">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="c2c8c-447">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="c2c8c-447">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="c2c8c-448">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="c2c8c-448">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="c2c8c-449">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="c2c8c-449">AzureRM.Websites</span></span>
* <span data-ttu-id="c2c8c-450">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="c2c8c-450">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="c2c8c-451">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="c2c8c-451">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="c2c8c-452">添加了对长时间运行的 Websites cmdlet 的 -AsJob 支持。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-452">Added -AsJob support for long-running Websites cmdlets.</span></span> <span data-ttu-id="c2c8c-453">允许选定的 cmdlet 在后台运行并返回可跟踪和控制进度的作业。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-453">Allows selected cmdlets to run in the background and return a job to track and control progress.</span></span>
     - <span data-ttu-id="c2c8c-454">受影响的 cmdlet 为针对 Web 应用、应用服务计划和槽位的 New-、Remove-、Add- 和 Set-</span><span class="sxs-lookup"><span data-stu-id="c2c8c-454">Affected cmdlets are New-, Remove-, Add-, and Set- for WebApps, AppServicePlan and Slots</span></span>

## <a name="2017128-version-511"></a><span data-ttu-id="c2c8c-455">2017.12.8 版本 5.1.1</span><span class="sxs-lookup"><span data-stu-id="c2c8c-455">2017.12.8 Version 5.1.1</span></span>
* <span data-ttu-id="c2c8c-456">AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="c2c8c-456">AnalysisServices</span></span>
    - <span data-ttu-id="c2c8c-457">将位置的验证集更改为动态查找，以便支持所有云。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-457">Change validate set of location to dynamic lookup so that all clouds are supported.</span></span>
* <span data-ttu-id="c2c8c-458">自动化</span><span class="sxs-lookup"><span data-stu-id="c2c8c-458">Automation</span></span>
    - <span data-ttu-id="c2c8c-459">更新为 Import-AzureRMAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c2c8c-459">Update to Import-AzureRMAutomationRunbook</span></span>
        - <span data-ttu-id="c2c8c-460">现在为 Python2 Runbook 提供支持</span><span class="sxs-lookup"><span data-stu-id="c2c8c-460">Support is now being provided for Python2 runbooks</span></span>
* <span data-ttu-id="c2c8c-461">Batch</span><span class="sxs-lookup"><span data-stu-id="c2c8c-461">Batch</span></span>
    - <span data-ttu-id="c2c8c-462">修复了没有资源组时帐户操作无法自动检测资源组这一 Bug</span><span class="sxs-lookup"><span data-stu-id="c2c8c-462">Fixed a bug where account operations without a resource group failed to auto-detect the resource group</span></span>
* <span data-ttu-id="c2c8c-463">计算</span><span class="sxs-lookup"><span data-stu-id="c2c8c-463">Compute</span></span>
    - <span data-ttu-id="c2c8c-464">Get-AzureRmComputeResourceSku 显示区域信息。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-464">Get-AzureRmComputeResourceSku shows zone information.</span></span>
    - <span data-ttu-id="c2c8c-465">更新 Disable-AzureRmVmssDiskEncryption 以修复问题 https://github.com/Azure/azure-powershell/issues/5038</span><span class="sxs-lookup"><span data-stu-id="c2c8c-465">Update Disable-AzureRmVmssDiskEncryption to fix issue https://github.com/Azure/azure-powershell/issues/5038</span></span>
    - <span data-ttu-id="c2c8c-466">添加了对长时间运行的计算 cmdlet 的 -AsJob 支持。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-466">Added -AsJob support for long-running Compute cmdlets.</span></span> <span data-ttu-id="c2c8c-467">允许选定的 cmdlet 在后台运行并返回可跟踪和控制进度的作业。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-467">Allows selected cmdlets to run in the background and return a job to track and control progress.</span></span>
        - <span data-ttu-id="c2c8c-468">受影响的 cmdlet 包括适用于虚拟机和虚拟机规模集的 New-、Update-、Set-、Remove-、Start-、Restart-、Stop- cmdlet</span><span class="sxs-lookup"><span data-stu-id="c2c8c-468">Affected cmdlets include: New-, Update-, Set-, Remove-, Start-, Restart-, Stop- cmdlets for Virtual Machines and Virtual Machine Scale Sets</span></span>
    - <span data-ttu-id="c2c8c-469">向 New-AzureRmVM（可使用智能默认设置创建虚拟机和所有必需的资源）添加了简化的参数集</span><span class="sxs-lookup"><span data-stu-id="c2c8c-469">Added simplified parameter set to New-AzureRmVM, which creates a Virtual Machine and all required resources using smart defaults</span></span>
* <span data-ttu-id="c2c8c-470">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="c2c8c-470">ContainerInstance</span></span>
    - <span data-ttu-id="c2c8c-471">应用 Azure 容器实例 SDK 2017-10-01</span><span class="sxs-lookup"><span data-stu-id="c2c8c-471">Apply Azure Container Instance SDK 2017-10-01</span></span>
        - <span data-ttu-id="c2c8c-472">支持容器 run-to-completion</span><span class="sxs-lookup"><span data-stu-id="c2c8c-472">Support container run-to-completion</span></span>
        - <span data-ttu-id="c2c8c-473">支持 Azure 文件卷装载</span><span class="sxs-lookup"><span data-stu-id="c2c8c-473">Support Azure File volume mount</span></span>
        - <span data-ttu-id="c2c8c-474">支持为公共 IP 打开多个端口</span><span class="sxs-lookup"><span data-stu-id="c2c8c-474">Support opening multiple ports for public IP</span></span>
* <span data-ttu-id="c2c8c-475">ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c2c8c-475">ContainerRegistry</span></span>
    - <span data-ttu-id="c2c8c-476">用于异地复制和 Webhook 的新 cmdlet</span><span class="sxs-lookup"><span data-stu-id="c2c8c-476">New cmdlets for geo-replication and webhooks</span></span>
        - <span data-ttu-id="c2c8c-477">Get/New/Remove-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="c2c8c-477">Get/New/Remove-AzureRmContainerRegistryReplication</span></span>
        - <span data-ttu-id="c2c8c-478">Get/New/Remove/Test/Update-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="c2c8c-478">Get/New/Remove/Test/Update-AzureRmContainerRegistryWebhook</span></span>
* <span data-ttu-id="c2c8c-479">数据工厂</span><span class="sxs-lookup"><span data-stu-id="c2c8c-479">DataFactories</span></span>
    - <span data-ttu-id="c2c8c-480">凭据加密功能现在适用于启用了“远程访问”的操作（通过网络的操作）和禁用了“远程访问”的操作（本地计算机操作）。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-480">Credential encryption functionality now works with both "Remote Access" enabled (Over Network) and "Remote Access" disabled (Local Machine).</span></span>
* <span data-ttu-id="c2c8c-481">DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="c2c8c-481">DataFactoryV2</span></span>
    - <span data-ttu-id="c2c8c-482">添加了两个新的 cmdlet：Update-AzureRmDataFactoryV2 和 Stop-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="c2c8c-482">Added two new cmdlets: Update-AzureRmDataFactoryV2 and Stop-AzureRmDataFactoryV2PipelineRun</span></span>
* <span data-ttu-id="c2c8c-483">DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="c2c8c-483">DataLakeAnalytics</span></span>
    - <span data-ttu-id="c2c8c-484">向 Submit-AzureRmDataLakeAnalyticsJob 添加了名为 ScriptParameter 的参数</span><span class="sxs-lookup"><span data-stu-id="c2c8c-484">Added a parameter called ScriptParameter to Submit-AzureRmDataLakeAnalyticsJob</span></span>
        - <span data-ttu-id="c2c8c-485">可以对 Submit-AzureRmDataLakeAnalyticsJob 使用 Get-Help 来查找有关 ScriptParameter 的详细信息</span><span class="sxs-lookup"><span data-stu-id="c2c8c-485">Detailed information about ScriptParameter can be found using Get-Help on Submit-AzureRmDataLakeAnalyticsJob</span></span>
    - <span data-ttu-id="c2c8c-486">已将 New-AzureRmDataLakeAnalyticsAccount 的参数 MaxDegreeOfParallelism 更改为 MaxAnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="c2c8c-486">For New-AzureRmDataLakeAnalyticsAccount, changed the parameter MaxDegreeOfParallelism to MaxAnalyticsUnits</span></span>
        - <span data-ttu-id="c2c8c-487">为参数 MaxAnalyticsUnits 添加了别名 MaxDegreeOfParallelism</span><span class="sxs-lookup"><span data-stu-id="c2c8c-487">Added an alias for the parameter MaxAnalyticsUnits: MaxDegreeOfParallelism</span></span>
    - <span data-ttu-id="c2c8c-488">已将 New-AzureRmDataLakeAnalyticsComputePolicy 的参数 MaxDegreeOfParallelismPerJob 更改为 MaxAnalyticsUnitsPerJob</span><span class="sxs-lookup"><span data-stu-id="c2c8c-488">For New-AzureRmDataLakeAnalyticsComputePolicy, changed the parameter MaxDegreeOfParallelismPerJob to MaxAnalyticsUnitsPerJob</span></span>
        - <span data-ttu-id="c2c8c-489">为参数 MaxAnalyticsUnitsPerJob 添加了别名 MaxDegreeOfParallelismPerJob</span><span class="sxs-lookup"><span data-stu-id="c2c8c-489">Added an alias for the parameter MaxAnalyticsUnitsPerJob: MaxDegreeOfParallelismPerJob</span></span>
    - <span data-ttu-id="c2c8c-490">已将 Set-AzureRmDataLakeAnalyticsAccount 的参数 MaxDegreeOfParallelism 更改为 MaxAnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="c2c8c-490">For Set-AzureRmDataLakeAnalyticsAccount, changed the parameter MaxDegreeOfParallelism to MaxAnalyticsUnits</span></span>
        - <span data-ttu-id="c2c8c-491">为参数 MaxAnalyticsUnits 添加了别名 MaxDegreeOfParallelism</span><span class="sxs-lookup"><span data-stu-id="c2c8c-491">Added an alias for the parameter MaxAnalyticsUnits: MaxDegreeOfParallelism</span></span>
    - <span data-ttu-id="c2c8c-492">已将 Submit-AzureRmDataLakeAnalyticsJob 的参数 DegreeOfParallelism 更改为 AnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="c2c8c-492">For Submit-AzureRmDataLakeAnalyticsJob, changed the parameter DegreeOfParallelism to AnalyticsUnits</span></span>
        - <span data-ttu-id="c2c8c-493">为参数 AnalyticsUnits 添加了别名 DegreeOfParallelism</span><span class="sxs-lookup"><span data-stu-id="c2c8c-493">Added an alias for the parameter AnalyticsUnits: DegreeOfParallelism</span></span>
    - <span data-ttu-id="c2c8c-494">已将 Update-AzureRmDataLakeAnalyticsComputePolicy 的参数 MaxDegreeOfParallelismPerJob 更改为 MaxAnalyticsUnitsPerJob</span><span class="sxs-lookup"><span data-stu-id="c2c8c-494">For Update-AzureRmDataLakeAnalyticsComputePolicy, changed the parameter MaxDegreeOfParallelismPerJob to MaxAnalyticsUnitsPerJob</span></span>
        - <span data-ttu-id="c2c8c-495">为参数 MaxAnalyticsUnitsPerJob 添加了别名 MaxDegreeOfParallelismPerJob</span><span class="sxs-lookup"><span data-stu-id="c2c8c-495">Added an alias for the parameter MaxAnalyticsUnitsPerJob: MaxDegreeOfParallelismPerJob</span></span>
* <span data-ttu-id="c2c8c-496">MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="c2c8c-496">MachineLearningCompute</span></span>
    - <span data-ttu-id="c2c8c-497">添加 Set-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="c2c8c-497">Add Set-AzureRmMlOpCluster</span></span>
        - <span data-ttu-id="c2c8c-498">更新群集的代理计数或 SSL 配置</span><span class="sxs-lookup"><span data-stu-id="c2c8c-498">Update a cluster's agent count or SSL configuration</span></span>
    - <span data-ttu-id="c2c8c-499">业务流程协调程序属性为可选</span><span class="sxs-lookup"><span data-stu-id="c2c8c-499">Orchestrator properties are optional</span></span>
        - <span data-ttu-id="c2c8c-500">此服务会创建服务主体（如果未提供），因此业务流程协调程序属性现在为可选</span><span class="sxs-lookup"><span data-stu-id="c2c8c-500">The service will create a service principal if not provided, so the orchestrator properties are now optional</span></span>
* <span data-ttu-id="c2c8c-501">PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="c2c8c-501">PowerBIEmbedded</span></span>
    - <span data-ttu-id="c2c8c-502">添加对 Power BI Embedded 容量 cmdlet 的支持</span><span class="sxs-lookup"><span data-stu-id="c2c8c-502">Add support for Power BI Embedded Capacity cmdlets</span></span>
    - <span data-ttu-id="c2c8c-503">全新 Cmdlet Get-AzureRmPowerBIEmbeddedCapacity - 获取 PowerBI Embedded 容量的详细信息。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-503">New Cmdlet Get-AzureRmPowerBIEmbeddedCapacity - Gets the details of a PowerBI Embedded Capacity.</span></span>
    - <span data-ttu-id="c2c8c-504">全新 Cmdlet New-AzureRmPowerBIEmbeddedCapacity - 创建新的 PowerBI Embedded 容量</span><span class="sxs-lookup"><span data-stu-id="c2c8c-504">New Cmdlet New-AzureRmPowerBIEmbeddedCapacity - Creates a new PowerBI Embedded Capacity</span></span>
    - <span data-ttu-id="c2c8c-505">全新 Cmdlet Remove-AzureRmPowerBIEmbeddedCapacity - 删除 PowerBI Embedded 容量的实例</span><span class="sxs-lookup"><span data-stu-id="c2c8c-505">New Cmdlet Remove-AzureRmPowerBIEmbeddedCapacity - Deletes an instance of PowerBI Embedded Capacity</span></span>
    - <span data-ttu-id="c2c8c-506">全新 Cmdlet Resume-AzureRmPowerBIEmbeddedCapacity - 恢复 PowerBI Embedded 容量的实例</span><span class="sxs-lookup"><span data-stu-id="c2c8c-506">New Cmdlet Resume-AzureRmPowerBIEmbeddedCapacity - Resumes an instance of PowerBI Embedded Capacity</span></span>
    - <span data-ttu-id="c2c8c-507">全新 Cmdlet Suspend-AzureRmPowerBIEmbeddedCapacity - 暂停 PowerBI Embedded 容量的实例</span><span class="sxs-lookup"><span data-stu-id="c2c8c-507">New Cmdlet Suspend-AzureRmPowerBIEmbeddedCapacity - Suspends an instance of PowerBI Embedded Capacity</span></span>
    - <span data-ttu-id="c2c8c-508">全新 Cmdlet Test-AzureRmPowerBIEmbeddedCapacity - 测试 PowerBI Embedded 容量的实例是否存在</span><span class="sxs-lookup"><span data-stu-id="c2c8c-508">New Cmdlet Test-AzureRmPowerBIEmbeddedCapacity - Tests the existence of an instance of PowerBI Embedded Capacity</span></span>
    - <span data-ttu-id="c2c8c-509">全新 Cmdlet Update-AzureRmPowerBIEmbeddedCapacity - 修改 PowerBI Embedded 容量的实例</span><span class="sxs-lookup"><span data-stu-id="c2c8c-509">New Cmdlet Update-AzureRmPowerBIEmbeddedCapacity - Modifies an instance of PowerBI Embedded Capacity</span></span>
* <span data-ttu-id="c2c8c-510">配置文件</span><span class="sxs-lookup"><span data-stu-id="c2c8c-510">Profile</span></span>
    - <span data-ttu-id="c2c8c-511">将 USGovernmentActiveDirectoryEndpoint 更新到了 https://login.microsoftonline.us/</span><span class="sxs-lookup"><span data-stu-id="c2c8c-511">Updated USGovernmentActiveDirectoryEndpoint to https://login.microsoftonline.us/</span></span>
        - <span data-ttu-id="c2c8c-512">有关 Azure 政府版终结点映射的详细信息，请参阅下文：https://docs.microsoft.com/en-us/azure/azure-government/documentation-government-developer-guide#endpoint-mapping</span><span class="sxs-lookup"><span data-stu-id="c2c8c-512">For more information about the Azure Government endpoint mappings, please see the following: https://docs.microsoft.com/en-us/azure/azure-government/documentation-government-developer-guide#endpoint-mapping</span></span>
    - <span data-ttu-id="c2c8c-513">添加了对 cmdlet 的 -AsJob 支持，允许所选 cmdlet 在后台执行并返回可跟踪和控制进度的作业</span><span class="sxs-lookup"><span data-stu-id="c2c8c-513">Added -AsJob support for cmdlets, enabling selected cmdlets to execute in the background and return a job to track and control progress</span></span>
    - <span data-ttu-id="c2c8c-514">向 Get-AzureRmSubscription cmdlet 添加了 -AsJob 参数</span><span class="sxs-lookup"><span data-stu-id="c2c8c-514">Added -AsJob parameter to Get-AzureRmSubscription cmdlet</span></span>
* <span data-ttu-id="c2c8c-515">RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="c2c8c-515">RecoveryServices.Backup</span></span>
    - <span data-ttu-id="c2c8c-516">修复了 Bug - Get-AzureRmRecoveryServicesBackupItem 应该为容器名称筛选器执行不区分大小写的比较。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-516">Fixed bug - Get-AzureRmRecoveryServicesBackupItem should do case insensitive comparison for container name filter.</span></span>
    - <span data-ttu-id="c2c8c-517">修复了 Bug - AzureVmItem 现在有一个可显示上次进行备份操作的时间的属性 - LastBackupTime.</span><span class="sxs-lookup"><span data-stu-id="c2c8c-517">Fixed bug - AzureVmItem now has a property that shows the last time a backup operation has happened - LastBackupTime.</span></span>
* <span data-ttu-id="c2c8c-518">资源</span><span class="sxs-lookup"><span data-stu-id="c2c8c-518">Resources</span></span>
    - <span data-ttu-id="c2c8c-519">修复了 Get-AzureRMRoleAssignment 所进行的分配没有为自定义角色提供 roledefiniton 名称的问题</span><span class="sxs-lookup"><span data-stu-id="c2c8c-519">Fixed issue where Get-AzureRMRoleAssignment would result in a assignments without roledefiniton name for custom roles</span></span>
        - <span data-ttu-id="c2c8c-520">用户现在可以对具有 roledefinition 名称的分配使用 Get-AzureRMRoleAssignment，不管角色类型如何</span><span class="sxs-lookup"><span data-stu-id="c2c8c-520">Users can now use Get-AzureRMRoleAssignment with assignments having roledefinition names irrespective of the type of role</span></span>
    - <span data-ttu-id="c2c8c-521">修复了在 assignablescopes 中存在新作用域时使用 Set-AzureRMRoleRoleDefinition 引发“找不到 RD”错误的问题</span><span class="sxs-lookup"><span data-stu-id="c2c8c-521">Fixed issue where Set-AzureRMRoleRoleDefinition used to throw RD not found error when there was a new scope in assignablescopes</span></span>
        - <span data-ttu-id="c2c8c-522">用户现在可以将 Set-AzureRMRoleRoleDefinition 与包括新作用域在内的可分配作用域配合使用，不管作用域的位置如何</span><span class="sxs-lookup"><span data-stu-id="c2c8c-522">Users can now use Set-AzureRMRoleRoleDefinition with assignable scopes including new scopes irrespective of the position of the scope</span></span>
    - <span data-ttu-id="c2c8c-523">允许作用域以“/”结尾</span><span class="sxs-lookup"><span data-stu-id="c2c8c-523">Allow scopes to end with "/"</span></span>
        - <span data-ttu-id="c2c8c-524">用户现在可以使用作用域以“/”结尾的 RoleDefinition 和 RoleAssignment cmdlet，与 API 和 CLI 保持一致</span><span class="sxs-lookup"><span data-stu-id="c2c8c-524">Users can now use RoleDefinition and RoleAssignment commandlets with scopes ending with "/" ,consistent with API and CLI</span></span>
    - <span data-ttu-id="c2c8c-525">允许用户使用委派标志创建 RoleAssignment</span><span class="sxs-lookup"><span data-stu-id="c2c8c-525">Allow users to create RoleAssignment using delegation flag</span></span>
        - <span data-ttu-id="c2c8c-526">用户现在可以使用 New-AzureRMRoleAssignment，其中的一个选项是添加委派标志</span><span class="sxs-lookup"><span data-stu-id="c2c8c-526">Users can now use New-AzureRMRoleAssignment with an option of adding the delegation flag</span></span>
    - <span data-ttu-id="c2c8c-527">修复了可接受作用域参数的 RoleAssignment get 的问题</span><span class="sxs-lookup"><span data-stu-id="c2c8c-527">Fix RoleAssignment get to respect the scope parameter</span></span>
    - <span data-ttu-id="c2c8c-528">在 New-AzureRmRoleAssignment cmdlet 中添加了 ServicePrincipalName 的别名</span><span class="sxs-lookup"><span data-stu-id="c2c8c-528">Add an alias for ServicePrincipalName in the New-AzureRmRoleAssignment Commandlet</span></span>
        - <span data-ttu-id="c2c8c-529">在使用 New-AzureRmRoleAssignment cmdlet 时，用户现在可以使用 ApplicationId 而非 ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="c2c8c-529">Users can now use the ApplicationId instead of the ServicePrincipalName when using the New-AzureRmRoleAssignment commandlet</span></span>
* <span data-ttu-id="c2c8c-530">SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="c2c8c-530">SiteRecovery</span></span>
    - <span data-ttu-id="c2c8c-531">在此模块中添加了针对所有 cmdlet 的弃用警告，为下一次发布重大更改做准备。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-531">Add deprecation warnings for all cmdlets in this module in preparation for the next breaking change release.</span></span>
        - <span data-ttu-id="c2c8c-532">请参阅即将发布的重大更改指南，详细了解如何从 AzureRM 迁移 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-532">Please see the upcoming breaking changes guide for more information on how to migrate your cmdlets from AzureRM.</span></span>
* <span data-ttu-id="c2c8c-533">Sql</span><span class="sxs-lookup"><span data-stu-id="c2c8c-533">Sql</span></span>
    - <span data-ttu-id="c2c8c-534">添加了使用 Set-AzureRmSqlDatabase 重命名数据库的功能</span><span class="sxs-lookup"><span data-stu-id="c2c8c-534">Added ability to rename database using Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="c2c8c-535">修复了问题 https://github.com/Azure/azure-powershell/issues/4974</span><span class="sxs-lookup"><span data-stu-id="c2c8c-535">Fixed issue https://github.com/Azure/azure-powershell/issues/4974</span></span>
        - <span data-ttu-id="c2c8c-536">为审核 cmdlet 提供无效的 AUDIT_CHANGED_GROUP 值时，不再引发错误。此项将在即将发布的版本中删除。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-536">Providing invalid AUDIT_CHANGED_GROUP value for auditing cmdlets no longer throws an error and will be removed in an upcoming release.</span></span>
    - <span data-ttu-id="c2c8c-537">修复了问题 https://github.com/Azure/azure-powershell/issues/5046</span><span class="sxs-lookup"><span data-stu-id="c2c8c-537">Fixed issue https://github.com/Azure/azure-powershell/issues/5046</span></span>
        - <span data-ttu-id="c2c8c-538">不再忽略审核 cmdlet 中的 AuditAction 参数</span><span class="sxs-lookup"><span data-stu-id="c2c8c-538">AuditAction parameter in auditing cmdlets is no longer being ignored</span></span>
    - <span data-ttu-id="c2c8c-539">修复了提供的 StorageKeyType 为“Secondary”时审核 cmdlet 中存在的问题</span><span class="sxs-lookup"><span data-stu-id="c2c8c-539">Fixed an issue in Auditing cmdlets when 'Secondary' StorageKeyType is provided</span></span>
        - <span data-ttu-id="c2c8c-540">以前在设置 Blob 审核时，如果为 StorageKeyType 参数提供的值为“Secondary”，会使用主存储帐户密钥而非辅助密钥。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-540">When setting blob auditing, the primary storage account key was used instead of the secondary key when providing 'Secondary' value for StorageKeyType parameter.</span></span>
    - <span data-ttu-id="c2c8c-541">更改 Set-AzureRmSqlServerTransparentDataEncryptionProtector 中确认消息的措辞</span><span class="sxs-lookup"><span data-stu-id="c2c8c-541">Changing the wording for confirmation message from Set-AzureRmSqlServerTransparentDataEncryptionProtector</span></span>
* <span data-ttu-id="c2c8c-542">Azure (RDFE)</span><span class="sxs-lookup"><span data-stu-id="c2c8c-542">Azure (RDFE)</span></span>
    - <span data-ttu-id="c2c8c-543">删除了所有 RemoteApp cmdlet</span><span class="sxs-lookup"><span data-stu-id="c2c8c-543">Removed all RemoteApp Cmdles</span></span>
* <span data-ttu-id="c2c8c-544">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="c2c8c-544">Azure.Storage</span></span>
    - <span data-ttu-id="c2c8c-545">升级到 Azure 存储客户端库 8.6.0 和 Azure 存储 DataMovement 库 0.6.5</span><span class="sxs-lookup"><span data-stu-id="c2c8c-545">Upgrade to Azure Storage Client Library 8.6.0 and Azure Storage DataMovement Library 0.6.5</span></span>

## <a name="20171110-version-501"></a><span data-ttu-id="c2c8c-546">2017.11.10 版本 5.0.1</span><span class="sxs-lookup"><span data-stu-id="c2c8c-546">2017.11.10 Version 5.0.1</span></span>
* <span data-ttu-id="c2c8c-547">修复了在以下模块中执行时会导致某些 cmdlet 失败的程序集加载问题：</span><span class="sxs-lookup"><span data-stu-id="c2c8c-547">Fixed assembly loading issue that caused some cmdlets to fail when executing in the following modules:</span></span>
    - <span data-ttu-id="c2c8c-548">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c2c8c-548">AzureRM.ApiManagement</span></span>
    - <span data-ttu-id="c2c8c-549">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="c2c8c-549">AzureRM.Backup</span></span>
    - <span data-ttu-id="c2c8c-550">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="c2c8c-550">AzureRM.Batch</span></span>
    - <span data-ttu-id="c2c8c-551">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c2c8c-551">AzureRM.Compute</span></span>
    - <span data-ttu-id="c2c8c-552">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="c2c8c-552">AzureRM.DataFactories</span></span>
    - <span data-ttu-id="c2c8c-553">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="c2c8c-553">AzureRM.HDInsight</span></span>
    - <span data-ttu-id="c2c8c-554">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c2c8c-554">AzureRM.KeyVault</span></span>
    - <span data-ttu-id="c2c8c-555">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c2c8c-555">AzureRM.RecoveryServices</span></span>
    - <span data-ttu-id="c2c8c-556">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="c2c8c-556">AzureRM.RecoveryServices.Backup</span></span>
    - <span data-ttu-id="c2c8c-557">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="c2c8c-557">AzureRM.RecoveryServices.SiteRecovery</span></span>
    - <span data-ttu-id="c2c8c-558">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="c2c8c-558">AzureRM.RedisCache</span></span>
    - <span data-ttu-id="c2c8c-559">AzureRM.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="c2c8c-559">AzureRM.SiteRecovery</span></span>
    - <span data-ttu-id="c2c8c-560">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="c2c8c-560">AzureRM.Sql</span></span>
    - <span data-ttu-id="c2c8c-561">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="c2c8c-561">AzureRM.Storage</span></span>
    - <span data-ttu-id="c2c8c-562">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="c2c8c-562">AzureRM.StreamAnalytics</span></span>

## <a name="2017118---version-500"></a><span data-ttu-id="c2c8c-563">2017.11.8 - 版本 5.0.0</span><span class="sxs-lookup"><span data-stu-id="c2c8c-563">2017.11.8 - Version 5.0.0</span></span>
* <span data-ttu-id="c2c8c-564">注意：这是一个有重大更改的版本。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-564">NOTE: This is a breaking change release.</span></span> <span data-ttu-id="c2c8c-565">有关引入的重大更改的完整列表，请参阅迁移指南 (https://aka.ms/azps-migration-guide)。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-565">Please see the migration guide (https://aka.ms/azps-migration-guide) for a full list of introduced breaking changes.</span></span>
* <span data-ttu-id="c2c8c-566">AzureRM 中的所有 cmdlet 现在支持联机帮助</span><span class="sxs-lookup"><span data-stu-id="c2c8c-566">All cmdlets in AzureRM now support online help</span></span>
    - <span data-ttu-id="c2c8c-567">结合 -Online 参数运行 Get-Help 可在默认 Internet 浏览器中打开联机帮助</span><span class="sxs-lookup"><span data-stu-id="c2c8c-567">Run Get-Help with the -Online parameter to open the online help in your default Internet browser</span></span>
* <span data-ttu-id="c2c8c-568">AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="c2c8c-568">AnalysisServices</span></span>
    * <span data-ttu-id="c2c8c-569">修复了 Synchronize-AzureAsInstance 命令，现在它可以配合新的 AsAzure REST API 进行同步</span><span class="sxs-lookup"><span data-stu-id="c2c8c-569">Fixed Synchronize-AzureAsInstance command to work with new AsAzure REST API for sync</span></span>
* <span data-ttu-id="c2c8c-570">ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c2c8c-570">ApiManagement</span></span>
    * <span data-ttu-id="c2c8c-571">有关此版本中对 ApiManagement 所做的重大更改，参阅迁移指南</span><span class="sxs-lookup"><span data-stu-id="c2c8c-571">Please see the migration guide for breaking changes made to ApiManagement this release</span></span>
    * <span data-ttu-id="c2c8c-572">更新了 Cmdlet Get-AzureRmApiManagementUser 以修复问题 https://github.com/Azure/azure-powershell/issues/4510</span><span class="sxs-lookup"><span data-stu-id="c2c8c-572">Updated Cmdlet Get-AzureRmApiManagementUser to fix issue https://github.com/Azure/azure-powershell/issues/4510</span></span>
    * <span data-ttu-id="c2c8c-573">更新了 Cmdlet New-AzureRmApiManagementApi 以创建包含空路径的 API https://github.com/Azure/azure-powershell/issues/4069</span><span class="sxs-lookup"><span data-stu-id="c2c8c-573">Updated Cmdlet New-AzureRmApiManagementApi to create Api with Empty Path https://github.com/Azure/azure-powershell/issues/4069</span></span>
* <span data-ttu-id="c2c8c-574">ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="c2c8c-574">ApplicationInsights</span></span>
    * <span data-ttu-id="c2c8c-575">添加用于获取/创建/删除 Applicaiton Insights 资源的命令</span><span class="sxs-lookup"><span data-stu-id="c2c8c-575">Add commands to get/create/remove applicaiton insights resource</span></span>
        - <span data-ttu-id="c2c8c-576">Get-AzureRmApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="c2c8c-576">Get-AzureRmApplicationInsights</span></span>
        - <span data-ttu-id="c2c8c-577">New-AzureRmApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="c2c8c-577">New-AzureRmApplicationInsights</span></span>
        - <span data-ttu-id="c2c8c-578">Remove-AzureRmApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="c2c8c-578">Remove-AzureRmApplicationInsights</span></span>
    * <span data-ttu-id="c2c8c-579">添加用于获取/更新 Applicaiton Insights 资源定价/每日上限的命令</span><span class="sxs-lookup"><span data-stu-id="c2c8c-579">Add commands to get/update pricing/daily cap of applicaiton insights resource</span></span>
        - <span data-ttu-id="c2c8c-580">Get-AzureRmApplicationInsights -IncludeDailyCap</span><span class="sxs-lookup"><span data-stu-id="c2c8c-580">Get-AzureRmApplicationInsights -IncludeDailyCap</span></span>
        - <span data-ttu-id="c2c8c-581">Set-AzureRmApplicationInsightsPricingPlan</span><span class="sxs-lookup"><span data-stu-id="c2c8c-581">Set-AzureRmApplicationInsightsPricingPlan</span></span>
        - <span data-ttu-id="c2c8c-582">Set-AzureRmApplicationInsightsDailyCap</span><span class="sxs-lookup"><span data-stu-id="c2c8c-582">Set-AzureRmApplicationInsightsDailyCap</span></span>
    * <span data-ttu-id="c2c8c-583">添加用于获取/创建/更新/删除 Applicaiton Insights 资源连续导出的命令</span><span class="sxs-lookup"><span data-stu-id="c2c8c-583">Add commands to get/create/update/remove continuous export of applicaiton insights resource</span></span>
        - <span data-ttu-id="c2c8c-584">Get-AzureRmApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="c2c8c-584">Get-AzureRmApplicationInsightsContinuousExport</span></span>
        - <span data-ttu-id="c2c8c-585">Set-AzureRmApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="c2c8c-585">Set-AzureRmApplicationInsightsContinuousExport</span></span>
        - <span data-ttu-id="c2c8c-586">New-AzureRmApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="c2c8c-586">New-AzureRmApplicationInsightsContinuousExport</span></span>
        - <span data-ttu-id="c2c8c-587">Remove-AzureRmApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="c2c8c-587">Remove-AzureRmApplicationInsightsContinuousExport</span></span>
    * <span data-ttu-id="c2c8c-588">添加用于获取/创建/删除 Applicaiton Insights 资源 API 密钥的命令</span><span class="sxs-lookup"><span data-stu-id="c2c8c-588">Add commands to get/create/remove api keys of applicaiton insights resoruce</span></span>
        - <span data-ttu-id="c2c8c-589">Get-AzureRmApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="c2c8c-589">Get-AzureRmApplicationInsightsApiKey</span></span>
        - <span data-ttu-id="c2c8c-590">New-AzureRmApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="c2c8c-590">New-AzureRmApplicationInsightsApiKey</span></span>
        - <span data-ttu-id="c2c8c-591">Remove-AzureRmApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="c2c8c-591">Remove-AzureRmApplicationInsightsApiKey</span></span>
* <span data-ttu-id="c2c8c-592">AzureBatch</span><span class="sxs-lookup"><span data-stu-id="c2c8c-592">AzureBatch</span></span>
    * <span data-ttu-id="c2c8c-593">为 `New-AzureRmBatchAccount` 添加了新参数。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-593">Added new parameters to `New-AzureRmBatchAccount`.</span></span>
        - <span data-ttu-id="c2c8c-594">`PoolAllocationMode`：用于在 Batch 帐户中创建池的分配模式。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-594">`PoolAllocationMode`: The allocation mode to use for creating pools in the Batch account.</span></span> <span data-ttu-id="c2c8c-595">若要创建一个可在用户订阅中分配池节点的 Batch 帐户，请将此参数设置为 `UserSubscription`。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-595">To create a Batch account which allocates pool nodes in the user's subscription, set this to `UserSubscription`.</span></span>
        - <span data-ttu-id="c2c8c-596">`KeyVaultId`：与 Batch 帐户关联的 Azure Key Vault 的资源 ID。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-596">`KeyVaultId`: The resource ID of the Azure key vault associated with the Batch account.</span></span>
        - <span data-ttu-id="c2c8c-597">`KeyVaultUrl`：与 Batch 帐户关联的 Azure Key Vault 的 URL。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-597">`KeyVaultUrl`: The URL of the Azure key vault associated with the Batch account.</span></span>
    * <span data-ttu-id="c2c8c-598">更新了 `New-AzureBatchTask` 的参数。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-598">Updated parameters to `New-AzureBatchTask`.</span></span>
        - <span data-ttu-id="c2c8c-599">删除了 `RunElevated` 开关。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-599">Removed the `RunElevated` switch.</span></span> <span data-ttu-id="c2c8c-600">已添加 `UserIdentity` 参数来取代 `RunElevated`，可按如下所示，通过构造 `PSUserIdentity` 来实现等效的行为：</span><span class="sxs-lookup"><span data-stu-id="c2c8c-600">The `UserIdentity` parameter has been added to replace `RunElevated`, and the equivalent behavior can be achieved by constructing a `PSUserIdentity` as shown below:</span></span>
            - <span data-ttu-id="c2c8c-601">$autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")</span><span class="sxs-lookup"><span data-stu-id="c2c8c-601">$autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")</span></span>
            - <span data-ttu-id="c2c8c-602">$userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser</span><span class="sxs-lookup"><span data-stu-id="c2c8c-602">$userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser</span></span>
        - <span data-ttu-id="c2c8c-603">添加了 `AuthenticationTokenSettings` 参数。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-603">Added the `AuthenticationTokenSettings` parameter.</span></span> <span data-ttu-id="c2c8c-604">使用此参数可以请求 Batch 服务向运行的任务提供身份验证令牌，从而无需向该任务传递 Batch 帐户密钥来向 Batch 服务发出请求。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-604">This parameter allows you to request the Batch service provide an authentication token to the task when it runs, avoiding the need to pass Batch account keys to the task in order to issue requests to the Batch service.</span></span>
        - <span data-ttu-id="c2c8c-605">添加了 `ContainerSettings` 参数。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-605">Added the `ContainerSettings` parameter.</span></span>
            - <span data-ttu-id="c2c8c-606">使用此参数可以请求 Batch 服务在容器内部运行任务。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-606">This parameter allows you to request the Batch service run the task inside a container.</span></span>
        - <span data-ttu-id="c2c8c-607">添加了 `OutputFiles` 参数。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-607">Added the `OutputFiles` parameter.</span></span>
            - <span data-ttu-id="c2c8c-608">使用此参数可以配置任务，以便在完成任务之后将文件上传到 Azure 存储。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-608">This parameter allows you to configure the task to upload files to Azure Storage after it has finished.</span></span>
    * <span data-ttu-id="c2c8c-609">更新了 `New-AzureBatchPool` 的参数。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-609">Updated parameters to `New-AzureBatchPool`.</span></span>
        - <span data-ttu-id="c2c8c-610">添加了 `UserAccounts` 参数。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-610">Added the `UserAccounts` parameter.</span></span>
            - <span data-ttu-id="c2c8c-611">此参数定义在池中每个节点上创建的用户帐户。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-611">This parameter defines user accounts created on each node in the pool.</span></span>
        - <span data-ttu-id="c2c8c-612">添加了 `TargetLowPriorityComputeNodes`，并已将 `TargetDedicated` 重命名为 `TargetDedicatedComputeNodes`。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-612">Added `TargetLowPriorityComputeNodes` and renamed `TargetDedicated` to `TargetDedicatedComputeNodes`.</span></span>
            - <span data-ttu-id="c2c8c-613">为 `TargetDedicatedComputeNodes` 参数创建了 `TargetDedicated` 别名。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-613">A `TargetDedicated` alias was created for the `TargetDedicatedComputeNodes` parameter.</span></span>
        - <span data-ttu-id="c2c8c-614">添加了 `NetworkConfiguration` 参数。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-614">Added the `NetworkConfiguration` parameter.</span></span>
            - <span data-ttu-id="c2c8c-615">使用此参数可以配置池的网络设置。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-615">This parameter allows you to configure the pools network settings.</span></span>
    * <span data-ttu-id="c2c8c-616">更新了 `New-AzureBatchCertificate` 的参数。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-616">Updated parameters to `New-AzureBatchCertificate`.</span></span>
        - <span data-ttu-id="c2c8c-617">`Password` 参数现在是 `SecureString`。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-617">The `Password` parameter is now a `SecureString`.</span></span>
    * <span data-ttu-id="c2c8c-618">更新了 `New-AzureBatchComputeNodeUser` 的参数。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-618">Updated parameters to `New-AzureBatchComputeNodeUser`.</span></span>
        - <span data-ttu-id="c2c8c-619">`Password` 参数现在是 `SecureString`。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-619">The `Password` parameter is now a `SecureString`.</span></span>
    * <span data-ttu-id="c2c8c-620">更新了 `Set-AzureBatchComputeNodeUser` 的参数。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-620">Updated parameters to `Set-AzureBatchComputeNodeUser`.</span></span>
        - <span data-ttu-id="c2c8c-621">`Password` 参数现在是 `SecureString`。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-621">The `Password` parameter is now a `SecureString`.</span></span>
    * <span data-ttu-id="c2c8c-622">已将 `Get-AzureBatchNodeFile`、`Get-AzureBatchNodeFileContent` 和 `Remove-AzureBatchNodeFile` 的 `Name` 参数重命名为 `Path`。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-622">Renamed the `Name` parameter to `Path` on `Get-AzureBatchNodeFile`, `Get-AzureBatchNodeFileContent`, and `Remove-AzureBatchNodeFile`.</span></span>
        - <span data-ttu-id="c2c8c-623">为 `Path` 参数创建了 `Name` 别名。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-623">A `Name` alias was created for the `Path` parameter.</span></span>
    * <span data-ttu-id="c2c8c-624">对象更改</span><span class="sxs-lookup"><span data-stu-id="c2c8c-624">Changes to objects</span></span>
        - <span data-ttu-id="c2c8c-625">有关完整列表，参阅 Batch 更改日志</span><span class="sxs-lookup"><span data-stu-id="c2c8c-625">Please see the Batch change log for the full list</span></span>
    * <span data-ttu-id="c2c8c-626">添加了对基于 Azure Active Directory 的身份验证的支持。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-626">Added support for Azure Active Directory based authentication.</span></span>
        - <span data-ttu-id="c2c8c-627">若要使用 Azure Active Directory 身份验证，请使用 `Get-AzureRmBatchAccount` cmdlet 检索 `BatchAccountContext` 对象，并将此 `BatchAccountContext` 提供给 Batch 服务 cmdlet 的 `-BatchContext` 参数。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-627">To use Azure Active Directory authentication, retrieve a `BatchAccountContext` object using the `Get-AzureRmBatchAccount` cmdlet, and supply this `BatchAccountContext` to the `-BatchContext` parameter of a Batch service cmdlet.</span></span> <span data-ttu-id="c2c8c-628">采用 `PoolAllocationMode = UserSubscription` 设置的帐户必须使用 Azure Active Directory 身份验证。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-628">Azure Active Directory authentication is mandatory for accounts with `PoolAllocationMode = UserSubscription`.</span></span>
        - <span data-ttu-id="c2c8c-629">对于现有帐户或使用 `PoolAllocationMode = BatchService` 创建的新帐户，可通过使用 `Get-AzureRmBatchAccoutKeys` cmdlet 检索 `BatchAccountContext` 对象，来继续使用共享密钥身份验证。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-629">For existing accounts or for new accounts created with `PoolAllocationMode = BatchService`, you may continue to use shared key authentication by retrieving a `BatchAccountContext` object using the `Get-AzureRmBatchAccoutKeys` cmdlet.</span></span>
* <span data-ttu-id="c2c8c-630">计算</span><span class="sxs-lookup"><span data-stu-id="c2c8c-630">Compute</span></span>
    * <span data-ttu-id="c2c8c-631">Azure 磁盘加密扩展命令</span><span class="sxs-lookup"><span data-stu-id="c2c8c-631">Azure Disk Encryption Extension Commands</span></span>
        - <span data-ttu-id="c2c8c-632">“Set-AzureRmVmDiskEncryptionExtension”的新参数“-EncryptFormatAll”可以加密形式格式化数据磁盘</span><span class="sxs-lookup"><span data-stu-id="c2c8c-632">New Parameter for 'Set-AzureRmVmDiskEncryptionExtension': '-EncryptFormatAll' encrypt formats data disks</span></span>
        - <span data-ttu-id="c2c8c-633">“Set-AzureRmVmDiskEncryptionExtension”的新参数“-ExtensionPublisherName”和“-ExtensionType”可用于切换到扩展的其他版本</span><span class="sxs-lookup"><span data-stu-id="c2c8c-633">New Parameters for 'Set-AzureRmVmDiskEncryptionExtension': '-ExtensionPublisherName' and '-ExtensionType' allow switching to other versions of the extension</span></span>
        - <span data-ttu-id="c2c8c-634">“Disable-AzureRmVmDiskEncryption”的新参数“-ExtensionPublisherName”和“-ExtensionType”可用于切换到扩展的其他版本</span><span class="sxs-lookup"><span data-stu-id="c2c8c-634">New Parameters for 'Disable-AzureRmVmDiskEncryption': '-ExtensionPublisherName' and '-ExtensionType' allow switching to other versions of the extension</span></span>
        - <span data-ttu-id="c2c8c-635">“Get-AzureRmVmDiskEncryptionStatus”的新参数“-ExtensionPublisherName”和“-ExtensionType”可用于切换到扩展的其他版本</span><span class="sxs-lookup"><span data-stu-id="c2c8c-635">New Parameters for 'Get-AzureRmVmDiskEncryptionStatus': '-ExtensionPublisherName' and '-ExtensionType' allow switching to other versions of the extension</span></span>
* <span data-ttu-id="c2c8c-636">DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="c2c8c-636">DataLakeAnalytics</span></span>
    * <span data-ttu-id="c2c8c-637">有关此版本中对 DataLakeAnalytics 所做的重大更改，参阅迁移指南</span><span class="sxs-lookup"><span data-stu-id="c2c8c-637">Please see the migration guide for breaking changes made to DataLakeAnalytics this release</span></span>
    * <span data-ttu-id="c2c8c-638">更改了 Get-AzureRmDataLakeAnalyticsAccount 的两个 OutputType 中的一个</span><span class="sxs-lookup"><span data-stu-id="c2c8c-638">Changed one of the two OutputTypes of Get-AzureRmDataLakeAnalyticsAccount</span></span>
        - <span data-ttu-id="c2c8c-639">List\<DataLakeAnalyticsAccount> 已更改为 List\<PSDataLakeAnalyticsAccountBasic></span><span class="sxs-lookup"><span data-stu-id="c2c8c-639">List\<DataLakeAnalyticsAccount> to List\<PSDataLakeAnalyticsAccountBasic></span></span>
        - <span data-ttu-id="c2c8c-640">PSDataLakeAnalyticsAccountBasic 的属性是 DataLakeAnalyticsAccount 的属性的严格子集</span><span class="sxs-lookup"><span data-stu-id="c2c8c-640">The properties of PSDataLakeAnalyticsAccountBasic is a strict subset of the properties of DataLakeAnalyticsAccount</span></span>
        - <span data-ttu-id="c2c8c-641">DataLakeAnalyticsAccount 中的附加属性不会由服务返回。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-641">The additional properties that are in DataLakeAnalyticsAccount are not returned by the service.</span></span>  <span data-ttu-id="c2c8c-642">因此，此项更改旨在准确反映这种情况。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-642">Therefore, this change is to reflect this accurately.</span></span> <span data-ttu-id="c2c8c-643">这些附加属性仍在 PSDataLakeAnalyticsAccountBasic 中，但已标记为“已过时”。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-643">These additional properties are still in PSDataLakeAnalyticsAccountBasic, but they are tagged as Obsolete.</span></span>
    * <span data-ttu-id="c2c8c-644">更改了 Get-AzureRmDataLakeAnalyticsJob 的两个 OutputType 中的一个</span><span class="sxs-lookup"><span data-stu-id="c2c8c-644">Changed one of the two OutputTypes of Get-AzureRmDataLakeAnalyticsJob</span></span>
        - <span data-ttu-id="c2c8c-645">List\<JobInformation> 已更改为 List\<PSJobInformationBasic></span><span class="sxs-lookup"><span data-stu-id="c2c8c-645">List\<JobInformation> to List\<PSJobInformationBasic></span></span>
        - <span data-ttu-id="c2c8c-646">PSJobInformationBasic 的属性是 JobInformation 的属性的严格子集</span><span class="sxs-lookup"><span data-stu-id="c2c8c-646">The properties of PSJobInformationBasic is a strict subset of the properties of JobInformation</span></span>
        - <span data-ttu-id="c2c8c-647">JobInformation 中的附加属性不会由服务返回。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-647">The additional properties that are in JobInformation are not returned by the service.</span></span>  <span data-ttu-id="c2c8c-648">因此，此项更改旨在准确反映这种情况。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-648">Therefore, this change is to reflect this accurately.</span></span> <span data-ttu-id="c2c8c-649">这些附加属性仍在 PSJobInformationBasic 中，但已标记为“已过时”。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-649">These additional properties are still in PSJobInformationBasic, but they are tagged as Obsolete.</span></span>
* <span data-ttu-id="c2c8c-650">DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c2c8c-650">DataLakeStore</span></span>
    * <span data-ttu-id="c2c8c-651">有关此版本中对 DataLakeStore 所做的重大更改，参阅迁移指南</span><span class="sxs-lookup"><span data-stu-id="c2c8c-651">Please see the migration guide for breaking changes made to DataLakeStore this release</span></span>
    * <span data-ttu-id="c2c8c-652">更改了 Get-AzureRmDataLakeStoreAccount 的两个 OutputType 中的一个</span><span class="sxs-lookup"><span data-stu-id="c2c8c-652">Changed one of the two OutputTypes of Get-AzureRmDataLakeStoreAccount</span></span>
        - <span data-ttu-id="c2c8c-653">List\<PSDataLakeStoreAccount> 已更改为 List\<PSDataLakeStoreAccountBasic></span><span class="sxs-lookup"><span data-stu-id="c2c8c-653">List\<PSDataLakeStoreAccount> to List\<PSDataLakeStoreAccountBasic></span></span>
        - <span data-ttu-id="c2c8c-654">PSDataLakeStoreAccountBasic 的属性是 PSDataLakeStoreAccount 的属性的严格子集</span><span class="sxs-lookup"><span data-stu-id="c2c8c-654">The properties of PSDataLakeStoreAccountBasic is a strict subset of the properties of PSDataLakeStoreAccount</span></span>
        - <span data-ttu-id="c2c8c-655">PSDataLakeStoreAccount 中的附加属性不会由服务返回。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-655">The additional properties that are in PSDataLakeStoreAccount are not returned by the service.</span></span>  <span data-ttu-id="c2c8c-656">因此，此项更改旨在准确反映这种情况。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-656">Therefore, this change is to reflect this accurately.</span></span> <span data-ttu-id="c2c8c-657">这些附加属性仍在 PSDataLakeStoreAccountBasic 中，但已标记为“已过时”。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-657">These additional properties are still in PSDataLakeStoreAccountBasic, but they are tagged as Obsolete.</span></span>
* <span data-ttu-id="c2c8c-658">Dns</span><span class="sxs-lookup"><span data-stu-id="c2c8c-658">Dns</span></span>
    * <span data-ttu-id="c2c8c-659">对 Azure DNS 中 CAA 记录类型的支持</span><span class="sxs-lookup"><span data-stu-id="c2c8c-659">Support for CAA record types in Azure DNS</span></span>
       - <span data-ttu-id="c2c8c-660">支持对 CAA 记录类型执行所有操作</span><span class="sxs-lookup"><span data-stu-id="c2c8c-660">Supports all operations on CAA record type</span></span>
* <span data-ttu-id="c2c8c-661">EventHub</span><span class="sxs-lookup"><span data-stu-id="c2c8c-661">EventHub</span></span>
    * <span data-ttu-id="c2c8c-662">有关此版本中对 EventHub 所做的重大更改，参阅迁移指南</span><span class="sxs-lookup"><span data-stu-id="c2c8c-662">Please see the migration guide for breaking changes made to EventHub this release</span></span>
* <span data-ttu-id="c2c8c-663">洞察力</span><span class="sxs-lookup"><span data-stu-id="c2c8c-663">Insights</span></span>
    * <span data-ttu-id="c2c8c-664">有关此版本中对 Insights 所做的重大更改，参阅迁移指南</span><span class="sxs-lookup"><span data-stu-id="c2c8c-664">Please see the migration guide for breaking changes made to Insights this release</span></span>
* <span data-ttu-id="c2c8c-665">网络</span><span class="sxs-lookup"><span data-stu-id="c2c8c-665">Network</span></span>
    * <span data-ttu-id="c2c8c-666">有关此版本中对 Network 所做的重大更改，参阅迁移指南</span><span class="sxs-lookup"><span data-stu-id="c2c8c-666">Please see the migration guide for breaking changes made to Network this release</span></span>
    * <span data-ttu-id="c2c8c-667">添加了 cmdlet 用于列出指定 Azure 区域的可用 Internet 服务提供商</span><span class="sxs-lookup"><span data-stu-id="c2c8c-667">Added cmdlet to list available internet service providers for a specified Azure region</span></span>
        - <span data-ttu-id="c2c8c-668">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="c2c8c-668">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>
    * <span data-ttu-id="c2c8c-669">添加了 cmdlet 用于获取 Internet 服务提供商从指定位置到 Azure 区域的相对延迟评分</span><span class="sxs-lookup"><span data-stu-id="c2c8c-669">Added cmdlet to get the relative latency score for internet service providers from a specified location to Azure regions</span></span>
        - <span data-ttu-id="c2c8c-670">Get-AzureRmNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="c2c8c-670">Get-AzureRmNetworkWatcherReachabilityReport</span></span>
* <span data-ttu-id="c2c8c-671">配置文件</span><span class="sxs-lookup"><span data-stu-id="c2c8c-671">Profile</span></span>
    - <span data-ttu-id="c2c8c-672">Set-AzureRmDefault</span><span class="sxs-lookup"><span data-stu-id="c2c8c-672">Set-AzureRmDefault</span></span>
        - <span data-ttu-id="c2c8c-673">使用此 cmdlet 可设置默认资源组。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-673">Use this cmdlet to set a default resource group.</span></span>  <span data-ttu-id="c2c8c-674">因此，对于某些 cmdlet 可以选择性地使用 -ResourceGroup 参数；如果未指定资源组，将使用默认值</span><span class="sxs-lookup"><span data-stu-id="c2c8c-674">This will make the -ResourceGroup parameter optional for some cmdlets, and will use the default when a resource group is not specified</span></span>
        - ```Set-AzureRmDefault -ResourceGroupName "ExampleResourceGroup"```
        - <span data-ttu-id="c2c8c-675">如果订阅中存在指定的资源组，此资源组将设置为默认值。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-675">If resource group specified exists in the subscription, this resource group will be set to default.</span></span>  <span data-ttu-id="c2c8c-676">否则，将创建资源组并将其设置为默认值。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-676">Otherwise, the resource group will be created and then set to default.</span></span>
    - <span data-ttu-id="c2c8c-677">Get-AzureRmDefault</span><span class="sxs-lookup"><span data-stu-id="c2c8c-677">Get-AzureRmDefault</span></span>
        - <span data-ttu-id="c2c8c-678">使用此 cmdlet 可获取当前的默认资源组（和将来的其他默认资源组）。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-678">Use this cmdlet to get the current default resource group (and other defaults in the future).</span></span>
        - ```Get-AzureRmDefault -ResourceGroup```
    - <span data-ttu-id="c2c8c-679">Clear-AzureRmDefault</span><span class="sxs-lookup"><span data-stu-id="c2c8c-679">Clear-AzureRmDefault</span></span>
        - <span data-ttu-id="c2c8c-680">使用此 cmdlet 可删除当前的默认资源组</span><span class="sxs-lookup"><span data-stu-id="c2c8c-680">Use this cmdlet to remove the current default resource group</span></span>
        - ```Clear-AzureRmDefault -ResourceGroup```
    - <span data-ttu-id="c2c8c-681">Add-AzureRmEnvironment 和 Set-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="c2c8c-681">Add-AzureRmEnvironment and Set-AzureRmEnvironment</span></span>
        - <span data-ttu-id="c2c8c-682">添加 BatchAudience 参数，以便指定在获取 Batch 服务的身份验证令牌时要使用的 Azure Batch Active Directory 受众。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-682">Add the BatchAudience parameter, which allows you to specify the Azure Batch Active Directory audience to use when acquiring authentication tokens for the Batch service.</span></span>
* <span data-ttu-id="c2c8c-683">RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="c2c8c-683">RecoveryServices.Backup</span></span>
    * <span data-ttu-id="c2c8c-684">添加了 cmdlet 用于执行即时文件恢复。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-684">Added cmdlets to perform instant file recovery.</span></span>
        - <span data-ttu-id="c2c8c-685">Get-AzureRmRecoveryServicesBackupRPMountScript</span><span class="sxs-lookup"><span data-stu-id="c2c8c-685">Get-AzureRmRecoveryServicesBackupRPMountScript</span></span>
        - <span data-ttu-id="c2c8c-686">Disable-AzureRmRecoveryServicesBackupRPMountScript</span><span class="sxs-lookup"><span data-stu-id="c2c8c-686">Disable-AzureRmRecoveryServicesBackupRPMountScript</span></span>
    * <span data-ttu-id="c2c8c-687">已 RecoveryServices.Backup SDK 版本更新到最新版</span><span class="sxs-lookup"><span data-stu-id="c2c8c-687">Updated RecoveryServices.Backup SDK version to the latest</span></span>
    * <span data-ttu-id="c2c8c-688">更新了 Azure VM 工作负荷的测试，以便测试运行所需的所有设置由测试本身完成。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-688">Updated tests for the Azure VM workload so that, all setups needed for test runs are done by the tests themselves.</span></span>
    * <span data-ttu-id="c2c8c-689">修复 https://github.com/Azure/azure-powershell/issues/3164</span><span class="sxs-lookup"><span data-stu-id="c2c8c-689">Fixes https://github.com/Azure/azure-powershell/issues/3164</span></span>
* <span data-ttu-id="c2c8c-690">RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="c2c8c-690">RecoveryServices.SiteRecovery</span></span>
    * <span data-ttu-id="c2c8c-691">对 ASR VMware 到 Azure Site Recovery 的迁移所做的更改（cmdlet 目前支持企业到企业、企业到 Azure 以及 HyperV 到 Azure 的操作）</span><span class="sxs-lookup"><span data-stu-id="c2c8c-691">Changes for ASR VMware to Azure Site Recovery (cmdlets are currently supporting operations for Enterprise to Enterprise, Enterprise to Azure, HyperV to Azure)</span></span>
        - <span data-ttu-id="c2c8c-692">New-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="c2c8c-692">New-AzureRmRecoveryServicesAsrPolicy</span></span>
        - <span data-ttu-id="c2c8c-693">New-AzureRmRecoveryServicesAsrProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c2c8c-693">New-AzureRmRecoveryServicesAsrProtectedItem</span></span>
        - <span data-ttu-id="c2c8c-694">Update-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="c2c8c-694">Update-AzureRmRecoveryServicesAsrPolicy</span></span>
        - <span data-ttu-id="c2c8c-695">Update-AzureRmRecoveryServicesAsrProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="c2c8c-695">Update-AzureRmRecoveryServicesAsrProtectionDirection</span></span>
    * <span data-ttu-id="c2c8c-696">添加了对基于 AAD 的保管库的支持</span><span class="sxs-lookup"><span data-stu-id="c2c8c-696">Added support to AAD-based vault</span></span>
    * <span data-ttu-id="c2c8c-697">添加了 cmdlet 用于管理 VCenter 资源</span><span class="sxs-lookup"><span data-stu-id="c2c8c-697">Added cmdlets to manage VCenter resources</span></span>
        - <span data-ttu-id="c2c8c-698">Get-AzureRmRecoveryServicesAsrVCenter</span><span class="sxs-lookup"><span data-stu-id="c2c8c-698">Get-AzureRmRecoveryServicesAsrVCenter</span></span>
        - <span data-ttu-id="c2c8c-699">New-AzureRmRecoveryServicesAsrVCenter</span><span class="sxs-lookup"><span data-stu-id="c2c8c-699">New-AzureRmRecoveryServicesAsrVCenter</span></span>
        - <span data-ttu-id="c2c8c-700">Remove-AzureRmRecoveryServicesAsrVCenter</span><span class="sxs-lookup"><span data-stu-id="c2c8c-700">Remove-AzureRmRecoveryServicesAsrVCenter</span></span>
        - <span data-ttu-id="c2c8c-701">Update-AzureRmRecoveryServicesAsrVCenter</span><span class="sxs-lookup"><span data-stu-id="c2c8c-701">Update-AzureRmRecoveryServicesAsrVCenter</span></span>
    * <span data-ttu-id="c2c8c-702">添加了其他 cmdlet</span><span class="sxs-lookup"><span data-stu-id="c2c8c-702">Added other cmdlets</span></span>
        - <span data-ttu-id="c2c8c-703">Get-AzureRmRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="c2c8c-703">Get-AzureRmRecoveryServicesAsrAlertSetting</span></span>
        - <span data-ttu-id="c2c8c-704">Get-AzureRmRecoveryServicesAsrEvent</span><span class="sxs-lookup"><span data-stu-id="c2c8c-704">Get-AzureRmRecoveryServicesAsrEvent</span></span>
        - <span data-ttu-id="c2c8c-705">New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="c2c8c-705">New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
        - <span data-ttu-id="c2c8c-706">Set-AzureRmRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="c2c8c-706">Set-AzureRmRecoveryServicesAsrAlertSetting</span></span>
        - <span data-ttu-id="c2c8c-707">Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob</span><span class="sxs-lookup"><span data-stu-id="c2c8c-707">Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob</span></span>
        - <span data-ttu-id="c2c8c-708">Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob</span><span class="sxs-lookup"><span data-stu-id="c2c8c-708">Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob</span></span>
        - <span data-ttu-id="c2c8c-709">Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob</span><span class="sxs-lookup"><span data-stu-id="c2c8c-709">Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob</span></span>
        - <span data-ttu-id="c2c8c-710">Update-AzureRmRecoveryServicesAsrMobilityService</span><span class="sxs-lookup"><span data-stu-id="c2c8c-710">Update-AzureRmRecoveryServicesAsrMobilityService</span></span>
* <span data-ttu-id="c2c8c-711">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c2c8c-711">ServiceBus</span></span>
    - <span data-ttu-id="c2c8c-712">有关此版本中对 ServiceBus 所做的重大更改，参阅迁移指南</span><span class="sxs-lookup"><span data-stu-id="c2c8c-712">Please see the migration guide for breaking changes made to ServiceBus this release</span></span>
* <span data-ttu-id="c2c8c-713">Sql</span><span class="sxs-lookup"><span data-stu-id="c2c8c-713">Sql</span></span>
    * <span data-ttu-id="c2c8c-714">添加列出和取消对数据库执行的异步 updateslo 操作的支持</span><span class="sxs-lookup"><span data-stu-id="c2c8c-714">Adding support for list and cancel the asynchronous updateslo operation on the database</span></span>
        - <span data-ttu-id="c2c8c-715">更新现有的 cmdlet Get-AzureRmSqlDatabaseActivity 以返回 DB updateslo 操作状态。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-715">update existing cmdlet Get-AzureRmSqlDatabaseActivity to return DB updateslo operation status.</span></span>
        - <span data-ttu-id="c2c8c-716">添加新的 cmdlet Stop-AzureRmSqlDatabaseActivity，以取消对数据库执行的 updateslo 异步操作。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-716">add new cmdlet Stop-AzureRmSqlDatabaseActivity for cancel the asynchronous updateslo operation on the database.</span></span>
    * <span data-ttu-id="c2c8c-717">添加数据库和弹性池区域冗余的支持</span><span class="sxs-lookup"><span data-stu-id="c2c8c-717">Adding support for Zone Redundancy for databases and elastic pools</span></span>
        - <span data-ttu-id="c2c8c-718">添加 New-AzureRmSqlDatabase 的 ZoneRedundant 开关参数</span><span class="sxs-lookup"><span data-stu-id="c2c8c-718">Adding ZoneRedundant switch parameter to New-AzureRmSqlDatabase</span></span>
        - <span data-ttu-id="c2c8c-719">添加 Set-AzureRmSqlDatabase 的 ZoneRedundant 开关参数</span><span class="sxs-lookup"><span data-stu-id="c2c8c-719">Adding ZoneRedundant switch parameter to Set-AzureRmSqlDatabase</span></span>
        - <span data-ttu-id="c2c8c-720">添加 New-AzureRmSqlElasticPool 的 ZoneRedundant 开关参数</span><span class="sxs-lookup"><span data-stu-id="c2c8c-720">Adding ZoneRedundant switch parameter to New-AzureRmSqlElasticPool</span></span>
        - <span data-ttu-id="c2c8c-721">添加 Set-AzureRmSqlElasticPool 的 ZoneRedundant 开关参数</span><span class="sxs-lookup"><span data-stu-id="c2c8c-721">Adding ZoneRedundant switch parameter to Set-AzureRmSqlElasticPool</span></span>
    * <span data-ttu-id="c2c8c-722">添加对服务器 DNS 别名的支持</span><span class="sxs-lookup"><span data-stu-id="c2c8c-722">Adding support for Server DNS Aliases</span></span>
        - <span data-ttu-id="c2c8c-723">添加 Get-AzureRmSqlServerDnsAlias cmdlet，用于根据服务器和别名获取服务器 DNS 别名，或 Azure SQL Server 的一系列服务器 DNS 别名。</span><span class="sxs-lookup"><span data-stu-id="c2c8c-723">Adding Get-AzureRmSqlServerDnsAlias cmdlet which gets server dns aliases by server and alias name or a list of server dns aliases for an azure Sql Server.</span></span>
        - <span data-ttu-id="c2c8c-724">添加 New-AzureRmSqlServerDnsAlias cmdlet，用于新建给定 Azure SQL Server 的服务器 DNS 别名</span><span class="sxs-lookup"><span data-stu-id="c2c8c-724">Adding New-AzureRmSqlServerDnsAlias cmdlet which creates new server dns alias for a given Azure Sql server</span></span>
        - <span data-ttu-id="c2c8c-725">添加 Set-AzurermSqlServerDnsAlias cmlet，用于更新服务器 DNS 别名所指向的 Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="c2c8c-725">Adding Set-AzurermSqlServerDnsAlias cmlet which allows updating a Azure Sql Server to which server dns alias is pointing</span></span>
        - <span data-ttu-id="c2c8c-726">添加 Remove-AzureRmSqlServerDnsAlias cmdlet，用于删除 Azure SQL Server 的服务器 DNS 别名</span><span class="sxs-lookup"><span data-stu-id="c2c8c-726">Adding Remove-AzureRmSqlServerDnsAlias cmdlet which removes a server dns alias for a Azure Sql Server</span></span>
* <span data-ttu-id="c2c8c-727">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="c2c8c-727">Azure.Storage</span></span>
    * <span data-ttu-id="c2c8c-728">升级到 Azure 存储客户端库 8.5.0 和 Azure 存储 DataMovement 库 0.6.3</span><span class="sxs-lookup"><span data-stu-id="c2c8c-728">Upgrade to Azure Storage Client Library 8.5.0 and Azure Storage DataMovement Library 0.6.3</span></span>
    * <span data-ttu-id="c2c8c-729">添加文件共享支持快照</span><span class="sxs-lookup"><span data-stu-id="c2c8c-729">Add File Share Snapshot Support Feature</span></span>
        - <span data-ttu-id="c2c8c-730">为 Get-AzureStorageShare 添加“SnapshotTime”参数</span><span class="sxs-lookup"><span data-stu-id="c2c8c-730">Add 'SnapshotTime' parameter to Get-AzureStorageShare</span></span>
        - <span data-ttu-id="c2c8c-731">为 Remove-AzureStorageShare 添加“IncludeAllSnapshot”参数</span><span class="sxs-lookup"><span data-stu-id="c2c8c-731">Add 'IncludeAllSnapshot' parameter to Remove-AzureStorageShare</span></span>
