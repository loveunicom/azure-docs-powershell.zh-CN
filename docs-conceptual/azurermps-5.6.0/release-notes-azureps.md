---
title: Azure PowerShell 更改日志 | Microsoft Docs
description: 下面提供了对 Azure PowerShell 最新版本所做更改的历史记录。
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 2/20/2018
ms.openlocfilehash: 985e0fbaa2da73b398d4c574515bcbab5b1a16e0
ms.sourcegitcommit: 15bf69bf95eceb936b3a429e741add95c308826a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/28/2018
---
# <a name="release-notes"></a><span data-ttu-id="fcda8-103">发行说明</span><span class="sxs-lookup"><span data-stu-id="fcda8-103">Release notes</span></span>

<span data-ttu-id="fcda8-104">下面是此版本中对 Azure PowerShell 所做的更改列表。</span><span class="sxs-lookup"><span data-stu-id="fcda8-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---

## <a name="560---march-2018"></a><span data-ttu-id="fcda8-105">5.6.0 - 2018 年 3 月</span><span class="sxs-lookup"><span data-stu-id="fcda8-105">5.6.0 - March 2018</span></span>

#### <a name="general"></a><span data-ttu-id="fcda8-106">常规</span><span class="sxs-lookup"><span data-stu-id="fcda8-106">General</span></span>
* <span data-ttu-id="fcda8-107">修复了 CloudShell 中的默认资源组的问题</span><span class="sxs-lookup"><span data-stu-id="fcda8-107">Fix issue with Default Resource Group in CloudShell</span></span>
* <span data-ttu-id="fcda8-108">修复了在模块导入过程中执行错误启动脚本的问题</span><span class="sxs-lookup"><span data-stu-id="fcda8-108">Fix issue where incorrect startup scripts were being executed during module import</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="fcda8-109">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="fcda8-109">AzureRM.Profile</span></span>
* <span data-ttu-id="fcda8-110">在不支持的方案中启用 MSI 身份验证</span><span class="sxs-lookup"><span data-stu-id="fcda8-110">Enable MSI authentication in unsupported scenarios</span></span>
* <span data-ttu-id="fcda8-111">添加对用户定义的托管服务标识的支持</span><span class="sxs-lookup"><span data-stu-id="fcda8-111">Add support for user-defined Managed Service Identity</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="fcda8-112">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="fcda8-112">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="fcda8-113">修复了在生成时清理脚本的问题</span><span class="sxs-lookup"><span data-stu-id="fcda8-113">Fixed issue with cleaning up scripts in build</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="fcda8-114">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="fcda8-114">AzureRM.Cdn</span></span>
* <span data-ttu-id="fcda8-115">修复了在生成时清理脚本的问题</span><span class="sxs-lookup"><span data-stu-id="fcda8-115">Fixed issue with cleaning up scripts in build</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="fcda8-116">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="fcda8-116">AzureRM.Compute</span></span>
* <span data-ttu-id="fcda8-117">“New-AzureRmVM”和“New-AzureRmVMSS”支持数据磁盘。</span><span class="sxs-lookup"><span data-stu-id="fcda8-117">'New-AzureRmVM' and 'New-AzureRmVMSS' support data disks.</span></span>
* <span data-ttu-id="fcda8-118">“New-AzureRmVM”和“New-AzureRmVMSS”支持按名称或按 ID 指定自定义映像。</span><span class="sxs-lookup"><span data-stu-id="fcda8-118">'New-AzureRmVM' and 'New-AzureRmVMSS' support custom image by name or by id.</span></span>
* <span data-ttu-id="fcda8-119">日志分析功能</span><span class="sxs-lookup"><span data-stu-id="fcda8-119">Log analytic feature</span></span>
    - <span data-ttu-id="fcda8-120">添加了“Export-AzureRmLogAnalyticRequestRateByInterval”cmdlet</span><span class="sxs-lookup"><span data-stu-id="fcda8-120">Added 'Export-AzureRmLogAnalyticRequestRateByInterval' cmdlet</span></span>
    - <span data-ttu-id="fcda8-121">添加了“Export-AzureRmLogAnalyticThrottledRequests”cmdlet</span><span class="sxs-lookup"><span data-stu-id="fcda8-121">Added 'Export-AzureRmLogAnalyticThrottledRequests' cmdlet</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="fcda8-122">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="fcda8-122">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="fcda8-123">修复了容器注册表和 azure 文件卷装载的参数集问题</span><span class="sxs-lookup"><span data-stu-id="fcda8-123">Fix parameter sets issue for container registry and azure file volume mount</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="fcda8-124">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="fcda8-124">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="fcda8-125">将 ADF.Net SDK 更新到了版本 0.6.0-preview，其中包含以下更改：</span><span class="sxs-lookup"><span data-stu-id="fcda8-125">Updated the ADF .Net SDK to version 0.6.0-preview containing the following changes:</span></span>
    - <span data-ttu-id="fcda8-126">添加了新的 AzureDatabricks LinkedService 和 DatabricksNotebook 活动</span><span class="sxs-lookup"><span data-stu-id="fcda8-126">Added new AzureDatabricks LinkedService and DatabricksNotebook Activity</span></span>
    - <span data-ttu-id="fcda8-127">在 HDInsightOnDemand LinkedService 中添加了 headNodeSize 和 dataNodeSize 属性</span><span class="sxs-lookup"><span data-stu-id="fcda8-127">Added headNodeSize and dataNodeSize properties in HDInsightOnDemand LinkedService</span></span>
    - <span data-ttu-id="fcda8-128">为 SalesforceMarketingCloud 添加了 LinkedService、Dataset、CopySource</span><span class="sxs-lookup"><span data-stu-id="fcda8-128">Added LinkedService, Dataset, CopySource for SalesforceMarketingCloud</span></span>
    - <span data-ttu-id="fcda8-129">在所有活动上添加了对 SecureOutput 的支持</span><span class="sxs-lookup"><span data-stu-id="fcda8-129">Added support for SecureOutput on all activities</span></span>
    - <span data-ttu-id="fcda8-130">在 ForEach 活动上添加了新的 BatchCount 属性，以控制要运行的并发活动数量</span><span class="sxs-lookup"><span data-stu-id="fcda8-130">Added new BatchCount property on ForEach activity which control how many concurrent activities to run</span></span>
    - <span data-ttu-id="fcda8-131">添加了新的 Filter 活动</span><span class="sxs-lookup"><span data-stu-id="fcda8-131">Added new Filter Activity</span></span>
    - <span data-ttu-id="fcda8-132">添加了链接服务参数支持</span><span class="sxs-lookup"><span data-stu-id="fcda8-132">Added Linked Service Parameters support</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="fcda8-133">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="fcda8-133">AzureRM.Dns</span></span>
* <span data-ttu-id="fcda8-134">对专用 DNS 区域的支持（公共预览版）</span><span class="sxs-lookup"><span data-stu-id="fcda8-134">Support for Private DNS Zones (Public Preview)</span></span>
    - <span data-ttu-id="fcda8-135">添加了创建仅对关联虚拟网络可见的 DNS 区域的功能</span><span class="sxs-lookup"><span data-stu-id="fcda8-135">Adds ability to create DNS zones that are visible only to the associated virtual networks</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="fcda8-136">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="fcda8-136">AzureRM.Network</span></span>
* <span data-ttu-id="fcda8-137">更新模型类型以便与 DNS cmdlet 兼容。</span><span class="sxs-lookup"><span data-stu-id="fcda8-137">Updating model types for compatibility with DNS cmdlets.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="fcda8-138">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="fcda8-138">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="fcda8-139">对 ASR Azure 到 Azure Site Recovery 的迁移所做的更改（cmdlet 目前支持企业到企业、企业到 Azure、HyperV 到 Azure 以及 VMware 到 Azure 的操作）</span><span class="sxs-lookup"><span data-stu-id="fcda8-139">Changes for ASR Azure to Azure Site Recovery (cmdlets are currently supporting operations for Enterprise to Enterprise, Enterprise to Azure, HyperV to Azure,VMware to Azure)</span></span>
    - <span data-ttu-id="fcda8-140">New-AzureRmRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="fcda8-140">New-AzureRmRecoveryServicesAsrProtectionContainer</span></span>
    - <span data-ttu-id="fcda8-141">New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="fcda8-141">New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span></span>
    - <span data-ttu-id="fcda8-142">Remove-AzureRmRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="fcda8-142">Remove-AzureRmRecoveryServicesAsrProtectionContainer</span></span>
    - <span data-ttu-id="fcda8-143">Update-AzureRmRecoveryServicesAsrProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="fcda8-143">Update-AzureRmRecoveryServicesAsrProtectionDirection</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="fcda8-144">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="fcda8-144">AzureRM.Storage</span></span>
* <span data-ttu-id="fcda8-145">在用于新建和设置存储帐户的 cmdlet（EnableEncryptionService 和 DisableEncryptionService）中废弃以下参数，因为静态加密在默认情况下处于启用状态，并且不能禁用。</span><span class="sxs-lookup"><span data-stu-id="fcda8-145">Obsolete following parameters in new and set Storage Account cmdlets: EnableEncryptionService and DisableEncryptionService, since Encryption at Rest is enabled by default and can't be disabled.</span></span>
    - <span data-ttu-id="fcda8-146">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fcda8-146">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="fcda8-147">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fcda8-147">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="fcda8-148">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="fcda8-148">AzureRM.Websites</span></span>
* <span data-ttu-id="fcda8-149">修复了 Remove-AzureRmWebAppSlot 的帮助</span><span class="sxs-lookup"><span data-stu-id="fcda8-149">Fixed the help for Remove-AzureRmWebAppSlot</span></span>

## <a name="550---march-2018"></a><span data-ttu-id="fcda8-150">5.5.0 - 2018 年 3 月</span><span class="sxs-lookup"><span data-stu-id="fcda8-150">5.5.0 - March 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="fcda8-151">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="fcda8-151">AzureRM.Profile</span></span>
* <span data-ttu-id="fcda8-152">修复了导入别名的问题</span><span class="sxs-lookup"><span data-stu-id="fcda8-152">Fixed issue with importing aliases</span></span>
* <span data-ttu-id="fcda8-153">将 Newtonsoft.Json 的 10.0.3 版随 6.0.8 版一起加载</span><span class="sxs-lookup"><span data-stu-id="fcda8-153">Load version 10.0.3 of Newtonsoft.Json side-by-side with version 6.0.8</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="fcda8-154">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="fcda8-154">Azure.Storage</span></span>
* <span data-ttu-id="fcda8-155">支持软删除功能</span><span class="sxs-lookup"><span data-stu-id="fcda8-155">Support Soft-Delete feature</span></span>
    - <span data-ttu-id="fcda8-156">Enable-AzureStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="fcda8-156">Enable-AzureStorageDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="fcda8-157">Disable-AzureStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="fcda8-157">Disable-AzureStorageDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="fcda8-158">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="fcda8-158">Get-AzureStorageBlob</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="fcda8-159">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="fcda8-159">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="fcda8-160">修复了导入别名的问题</span><span class="sxs-lookup"><span data-stu-id="fcda8-160">Fixed issue with importing aliases</span></span>
* <span data-ttu-id="fcda8-161">添加对防火墙和查询向外扩展功能的支持，以及对 2017-08-01 api 版本的支持。</span><span class="sxs-lookup"><span data-stu-id="fcda8-161">Add support of firewall and query scaleout feature, as well as support of 2017-08-01 api version.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="fcda8-162">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="fcda8-162">AzureRM.Automation</span></span>
* <span data-ttu-id="fcda8-163">修复了导入别名的问题</span><span class="sxs-lookup"><span data-stu-id="fcda8-163">Fixed issue with importing aliases</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="fcda8-164">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="fcda8-164">AzureRM.Cdn</span></span>
* <span data-ttu-id="fcda8-165">修复了导入别名的问题</span><span class="sxs-lookup"><span data-stu-id="fcda8-165">Fixed issue with importing aliases</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="fcda8-166">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="fcda8-166">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="fcda8-167">更新 notice.txt 和通知消息。</span><span class="sxs-lookup"><span data-stu-id="fcda8-167">Update notice.txt and notice message.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="fcda8-168">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="fcda8-168">AzureRM.Compute</span></span>
* <span data-ttu-id="fcda8-169">'New-AzureRmVMSS' 以详细模式打印连接字符串。</span><span class="sxs-lookup"><span data-stu-id="fcda8-169">'New-AzureRmVMSS' prints connection strings in verbose mode.</span></span>
* <span data-ttu-id="fcda8-170">'New-AzureRmVmss' 支持公共 IP 地址、负载均衡规则、入站 NAT 规则。</span><span class="sxs-lookup"><span data-stu-id="fcda8-170">'New-AzureRmVmss' supports public IP address, load balancing rules, inbound NAT rules.</span></span>
* <span data-ttu-id="fcda8-171">WriteAccelerator 功能</span><span class="sxs-lookup"><span data-stu-id="fcda8-171">WriteAccelerator feature</span></span>
    - <span data-ttu-id="fcda8-172">将 WriteAccelerator 开关参数添加到了以下 cmdlet：Set-AzureRmVMOSDisk Set-AzureRmVMDataDisk Add-AzureRmVMDataDisk Add-AzureRmVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="fcda8-172">Added WriteAccelerator switch parameter to the following cmdlets: Set-AzureRmVMOSDisk Set-AzureRmVMDataDisk Add-AzureRmVMDataDisk Add-AzureRmVmssDataDisk</span></span>
    - <span data-ttu-id="fcda8-173">将 OsDiskWriteAccelerator 开关参数添加到了以下 cmdlet：     Set-AzureRmVmssStorageProfile。</span><span class="sxs-lookup"><span data-stu-id="fcda8-173">Added OsDiskWriteAccelerator switch parameter to the following cmdlet:     Set-AzureRmVmssStorageProfile.</span></span>
    - <span data-ttu-id="fcda8-174">将 OsDiskWriteAccelerator 布尔参数添加到了以下 cmdlet：     Update-AzureRmVM     Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fcda8-174">Added OsDiskWriteAccelerator Boolean parameter to the following cmdlets:     Update-AzureRmVM     Update-AzureRmVmss</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="fcda8-175">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="fcda8-175">AzureRM.DataFactories</span></span>
* <span data-ttu-id="fcda8-176">修复了导致某些加密操作没有有意义错误的凭据加密问题</span><span class="sxs-lookup"><span data-stu-id="fcda8-176">Fix credential encryption issue that caused no meaningful error for some encryption operations</span></span>
* <span data-ttu-id="fcda8-177">允许跨数据工厂共享集成运行时</span><span class="sxs-lookup"><span data-stu-id="fcda8-177">Enable integration runtime to be shared across data factory</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="fcda8-178">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="fcda8-178">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="fcda8-179">为 "Set-AzureRmDataFactoryV2IntegrationRuntime" cmd 添加了参数 "SetupScriptContainerSasUri" 和 "Edition" 以启用自定义安装和版本选择功能</span><span class="sxs-lookup"><span data-stu-id="fcda8-179">Add parameter "SetupScriptContainerSasUri" and "Edition" for "Set-AzureRmDataFactoryV2IntegrationRuntime" cmd to enable custom setup and edition selection functionality</span></span>
* <span data-ttu-id="fcda8-180">修复了导致某些加密操作没有有意义错误的凭据加密问题。</span><span class="sxs-lookup"><span data-stu-id="fcda8-180">Fix credential encryption issue that caused no meaningful error for some encryption operations.</span></span>
* <span data-ttu-id="fcda8-181">允许跨数据工厂共享集成运行时</span><span class="sxs-lookup"><span data-stu-id="fcda8-181">Enable integration runtime to be shared across data factory</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="fcda8-182">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="fcda8-182">AzureRM.HDInsight</span></span>
* <span data-ttu-id="fcda8-183">修复了导入别名的问题</span><span class="sxs-lookup"><span data-stu-id="fcda8-183">Fixed issue with importing aliases</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="fcda8-184">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="fcda8-184">AzureRM.KeyVault</span></span>
* <span data-ttu-id="fcda8-185">修复了 Set-AzureRmKeyVaultAccessPolicy 的示例</span><span class="sxs-lookup"><span data-stu-id="fcda8-185">Fixed example for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="fcda8-186">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="fcda8-186">AzureRM.Network</span></span>
* <span data-ttu-id="fcda8-187">修复了导入别名的问题</span><span class="sxs-lookup"><span data-stu-id="fcda8-187">Fixed issue with importing aliases</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="fcda8-188">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="fcda8-188">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="fcda8-189">修复了导入别名的问题</span><span class="sxs-lookup"><span data-stu-id="fcda8-189">Fixed issue with importing aliases</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="fcda8-190">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fcda8-190">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="fcda8-191">修复了导入别名的问题</span><span class="sxs-lookup"><span data-stu-id="fcda8-191">Fixed issue with importing aliases</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="fcda8-192">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="fcda8-192">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="fcda8-193">修复了导入别名的问题</span><span class="sxs-lookup"><span data-stu-id="fcda8-193">Fixed issue with importing aliases</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="fcda8-194">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="fcda8-194">AzureRM.Resources</span></span>
* <span data-ttu-id="fcda8-195">修复了导入别名的问题</span><span class="sxs-lookup"><span data-stu-id="fcda8-195">Fixed issue with importing aliases</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="fcda8-196">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="fcda8-196">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="fcda8-197">为 Queue 添加了 EnableBatchedOperations 属性</span><span class="sxs-lookup"><span data-stu-id="fcda8-197">Added EnableBatchedOperations property to Queue</span></span>
* <span data-ttu-id="fcda8-198">为 Subscriptions 添加了 DeadLetteringOnFilterEvaluationExceptions 属性</span><span class="sxs-lookup"><span data-stu-id="fcda8-198">Added DeadLetteringOnFilterEvaluationExceptions property to Subscriptions</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="fcda8-199">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="fcda8-199">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="fcda8-200">Service Fabric cmdlet 刷新</span><span class="sxs-lookup"><span data-stu-id="fcda8-200">Service Fabric cmdlet refresh</span></span>
  - <span data-ttu-id="fcda8-201">更新了 ARM 模板</span><span class="sxs-lookup"><span data-stu-id="fcda8-201">Updated ARM templates</span></span>
  - <span data-ttu-id="fcda8-202">失败的操作不再回滚</span><span class="sxs-lookup"><span data-stu-id="fcda8-202">Failed operations no longer rollback</span></span>
  - <span data-ttu-id="fcda8-203">Add-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="fcda8-203">Add-AzureRmServiceFabricNodeType</span></span>
    - <span data-ttu-id="fcda8-204">VM 默认为托管磁盘</span><span class="sxs-lookup"><span data-stu-id="fcda8-204">VMs default to managed disks</span></span>
    - <span data-ttu-id="fcda8-205">使用了现有 VMSS 子网</span><span class="sxs-lookup"><span data-stu-id="fcda8-205">Existing VMSS subnet used</span></span>
    - <span data-ttu-id="fcda8-206">所有操作都是幂等的</span><span class="sxs-lookup"><span data-stu-id="fcda8-206">All operations are idempotent</span></span>
  - <span data-ttu-id="fcda8-207">Remove-AzureRmServiceFabricNodeType 清除部分创建的 VMSS 和/或群集节点类型</span><span class="sxs-lookup"><span data-stu-id="fcda8-207">Remove-AzureRmServiceFabricNodeType cleans up partially created VMSS and/or cluster node types</span></span>
  - <span data-ttu-id="fcda8-208">修复了复杂属性类型的 PSCluster 对象输出</span><span class="sxs-lookup"><span data-stu-id="fcda8-208">Fixed output of PSCluster object for complex property types</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="fcda8-209">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="fcda8-209">AzureRM.Sql</span></span>
* <span data-ttu-id="fcda8-210">修复了导入别名的问题</span><span class="sxs-lookup"><span data-stu-id="fcda8-210">Fixed issue with importing aliases</span></span>
* <span data-ttu-id="fcda8-211">Get-AzureRmSqlServer、New-AzureRmSqlServer 和 Remove-AzureRmSqlServer 响应现在包括 FullyQualifiedDomainName 属性。</span><span class="sxs-lookup"><span data-stu-id="fcda8-211">Get-AzureRmSqlServer, New-AzureRmSqlServer, and Remove-AzureRmSqlServer response now includes FullyQualifiedDomainName property.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="fcda8-212">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="fcda8-212">AzureRM.Websites</span></span>
* <span data-ttu-id="fcda8-213">修复了导入别名的问题</span><span class="sxs-lookup"><span data-stu-id="fcda8-213">Fixed issue with importing aliases</span></span>
* <span data-ttu-id="fcda8-214">New-AzureRMWebApp - 添加了参数集以用于简化的 WebApp 创建，并提供本地 Git 存储库支持。</span><span class="sxs-lookup"><span data-stu-id="fcda8-214">New-AzureRMWebApp - added parameter set for simplified WebApp creation, with local git repository support.</span></span>

## <a name="540---february-2018"></a><span data-ttu-id="fcda8-215">5.4.0 - 2018 年 2 月</span><span class="sxs-lookup"><span data-stu-id="fcda8-215">5.4.0 - February 2018</span></span>
#### <a name="azurermautomation"></a><span data-ttu-id="fcda8-216">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="fcda8-216">AzureRM.Automation</span></span>
* <span data-ttu-id="fcda8-217">从 New-AzureRmAutomationModule 到 Import-AzureRmAutomationModule 添加了别名</span><span class="sxs-lookup"><span data-stu-id="fcda8-217">Added alias from New-AzureRmAutomationModule to Import-AzureRmAutomationModule</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="fcda8-218">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="fcda8-218">AzureRM.Compute</span></span>
* <span data-ttu-id="fcda8-219">解决某些 Get cmdlet 的 ErrorAction 问题。</span><span class="sxs-lookup"><span data-stu-id="fcda8-219">Fix ErrorAction issue for some of Get cmdlets.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="fcda8-220">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="fcda8-220">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="fcda8-221">应用 Azure 容器实例 SDK 2018-02-01</span><span class="sxs-lookup"><span data-stu-id="fcda8-221">Apply Azure Container Instance SDK 2018-02-01</span></span>
    - <span data-ttu-id="fcda8-222">支持 DNS 名称标签</span><span class="sxs-lookup"><span data-stu-id="fcda8-222">Support DNS name label</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="fcda8-223">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="fcda8-223">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="fcda8-224">修复了以前无法正常运行的所有 GET cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fcda8-224">Fixed all of the GET cmdlets which previously weren't working.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="fcda8-225">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="fcda8-225">AzureRM.EventHub</span></span>
* <span data-ttu-id="fcda8-226">修复 Get-AzureRmEventHubGeoDRConfiguration 帮助中的 bug</span><span class="sxs-lookup"><span data-stu-id="fcda8-226">Fix bug in Get-AzureRmEventHubGeoDRConfiguration help</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="fcda8-227">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="fcda8-227">AzureRM.Network</span></span>
* <span data-ttu-id="fcda8-228">添加了 cmdlet 以创建新的连接监视器</span><span class="sxs-lookup"><span data-stu-id="fcda8-228">Added cmdlet to create a new connection monitor</span></span>
    - <span data-ttu-id="fcda8-229">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fcda8-229">New-AzureRmNetworkWatcherConnectionMonitor</span></span>
* <span data-ttu-id="fcda8-230">添加了 cmdlet 以更新连接监视器</span><span class="sxs-lookup"><span data-stu-id="fcda8-230">Added cmdlet to update a connection monitor</span></span>
    - <span data-ttu-id="fcda8-231">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fcda8-231">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>
* <span data-ttu-id="fcda8-232">添加了 cmdlet 来获取连接监视器或连接监视器列表</span><span class="sxs-lookup"><span data-stu-id="fcda8-232">Added cmdlet to get connection monitor or connection monitor list</span></span>
    - <span data-ttu-id="fcda8-233">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fcda8-233">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>
* <span data-ttu-id="fcda8-234">添加了 cmdlet 以查询连接监视器</span><span class="sxs-lookup"><span data-stu-id="fcda8-234">Added cmdlet to query connection monitor</span></span>
    - <span data-ttu-id="fcda8-235">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="fcda8-235">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>
* <span data-ttu-id="fcda8-236">添加了 cmdlet 以启动连接监视器</span><span class="sxs-lookup"><span data-stu-id="fcda8-236">Added cmdlet to start connection monitor</span></span>
    - <span data-ttu-id="fcda8-237">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fcda8-237">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>
* <span data-ttu-id="fcda8-238">添加了 cmdlet 以停止连接监视器</span><span class="sxs-lookup"><span data-stu-id="fcda8-238">Added cmdlet to stop connection monitor</span></span>
    - <span data-ttu-id="fcda8-239">Stop-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fcda8-239">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>
* <span data-ttu-id="fcda8-240">添加了 cmdlet 以删除连接监视器</span><span class="sxs-lookup"><span data-stu-id="fcda8-240">Added cmdlet to remove connection monitor</span></span>
    - <span data-ttu-id="fcda8-241">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fcda8-241">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>
* <span data-ttu-id="fcda8-242">更新了 Set-AzureRmApplicationGatewayBackendAddressPool 文档以删除弃用的示例</span><span class="sxs-lookup"><span data-stu-id="fcda8-242">Updated Set-AzureRmApplicationGatewayBackendAddressPool documentation to remove deprecated example</span></span>
* <span data-ttu-id="fcda8-243">将 EnableHttp2 标志添加到了应用程序网关</span><span class="sxs-lookup"><span data-stu-id="fcda8-243">Added EnableHttp2 flag to Application Gateway</span></span>
    - <span data-ttu-id="fcda8-244">更新了 New-AzureRmApplicationGateway：添加了可选参数 -EnableHttp2</span><span class="sxs-lookup"><span data-stu-id="fcda8-244">Updated New-AzureRmApplicationGateway: Added optional parameter -EnableHttp2</span></span>
* <span data-ttu-id="fcda8-245">将 IpTags 添加到 PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="fcda8-245">Add IpTags to PublicIpAddress</span></span>
    - <span data-ttu-id="fcda8-246">更新了 New-AzureRmPublicIpAddress：添加了 IpTags</span><span class="sxs-lookup"><span data-stu-id="fcda8-246">Updated New-AzureRmPublicIpAddress: Added IpTags</span></span>
    - <span data-ttu-id="fcda8-247">用于添加 Iptag 的 New-AzureRmPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="fcda8-247">New-AzureRmPublicIpTag to add Iptag</span></span>
* <span data-ttu-id="fcda8-248">在 RouteTable 和 effectiveRoute 中添加 DisableBgpRoutePropagation 属性。</span><span class="sxs-lookup"><span data-stu-id="fcda8-248">Add DisableBgpRoutePropagation property in RouteTable and effectiveRoute.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="fcda8-249">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="fcda8-249">AzureRM.Resources</span></span>
* <span data-ttu-id="fcda8-250">Register-AzureRmProviderFeature：添加了文档中缺少的示例</span><span class="sxs-lookup"><span data-stu-id="fcda8-250">Register-AzureRmProviderFeature: Added missing example in the docs</span></span>
* <span data-ttu-id="fcda8-251">Register-AzureRmResourceProvider：添加了文档中缺少的示例</span><span class="sxs-lookup"><span data-stu-id="fcda8-251">Register-AzureRmResourceProvider: Added missing example in the docs</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="fcda8-252">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="fcda8-252">AzureRM.Storage</span></span>
* <span data-ttu-id="fcda8-253">在用于新建和设置存储帐户的 cmdlet（EnableEncryptionService 和 DisableEncryptionService）中废弃以下参数，因为静态加密在默认情况下处于启用状态，并且不能禁用。</span><span class="sxs-lookup"><span data-stu-id="fcda8-253">Obsolete following parameters in new and set Storage Account cmdlets: EnableEncryptionService and DisableEncryptionService, since Encryption at Rest is enabled by default and can't be disabled.</span></span>
    - <span data-ttu-id="fcda8-254">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fcda8-254">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="fcda8-255">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fcda8-255">Set-AzureRmStorageAccount</span></span>


## <a name="530---february-2018"></a><span data-ttu-id="fcda8-256">5.3.0 - 2018 年 2 月</span><span class="sxs-lookup"><span data-stu-id="fcda8-256">5.3.0 - February 2018</span></span>
### <a name="azurermprofile"></a><span data-ttu-id="fcda8-257">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="fcda8-257">AzureRM.Profile</span></span>
* <span data-ttu-id="fcda8-258">对 PowerShell 3 和 PowerShell 4 添加了弃用警告</span><span class="sxs-lookup"><span data-stu-id="fcda8-258">Added deprecation warning for PowerShell 3 and 4</span></span>
* <span data-ttu-id="fcda8-259">`Add-AzureRmAccount` 已重命名为 `Connect-AzureRmAccount`；为旧的 cmdlet 名称添加了别名，并将其他别名（`Login-AzAccount` 和 `Login-AzureRmAccount`）重定向到了新的 cmdlet 名称。</span><span class="sxs-lookup"><span data-stu-id="fcda8-259">`Add-AzureRmAccount` has been renamed as `Connect-AzureRmAccount`; an alias has been added for the old cmdlet name, and other aliases (`Login-AzAccount` and `Login-AzureRmAccount`) have been redirected to the new cmdlet name.</span></span>
* <span data-ttu-id="fcda8-260">`Remove-AzureRmAccount` 已重命名为 `Disconnect-AzureRmAccount`；为旧的 cmdlet 名称添加了别名，并将其他别名（`Logout-AzAccount` 和 `Logout-AzureRmAccount`）重定向到了新的 cmdlet 名称。</span><span class="sxs-lookup"><span data-stu-id="fcda8-260">`Remove-AzureRmAccount` has been renamed as `Disconnect-AzureRmAccount`; an alias has been added for the old cmdlet name, and other aliases (`Logout-AzAccount` and `Logout-AzureRmAccount`) have been redirected to the new cmdlet name.</span></span>
* <span data-ttu-id="fcda8-261">更正了资源字符串以使用 `Connect-AzureRmAccount` 而不是 `Login-AzureRmAccount`</span><span class="sxs-lookup"><span data-stu-id="fcda8-261">Corrected Resource Strings to use `Connect-AzureRmAccount` instead of `Login-AzureRmAccount`</span></span>
* <span data-ttu-id="fcda8-262">`Add-AzureRmEnvironment` 和 `Set-AzureRmEnvironment`</span><span class="sxs-lookup"><span data-stu-id="fcda8-262">`Add-AzureRmEnvironment` and `Set-AzureRmEnvironment`</span></span>
  - <span data-ttu-id="fcda8-263">添加了 `-AzureOperationalInsightsEndpoint` 和 `-AzureOperationalInsightsEndpointResourceId` 作为要用于 OperationalInsights 数据平面 RP 的参数。</span><span class="sxs-lookup"><span data-stu-id="fcda8-263">Added `-AzureOperationalInsightsEndpoint` and `-AzureOperationalInsightsEndpointResourceId` as parameters for use with OperationalInsights data plane RP.</span></span>

### <a name="azurermanalysisservices"></a><span data-ttu-id="fcda8-264">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="fcda8-264">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="fcda8-265">更正了 `Login-AzureRmAccount` 的用法以使用 `Connect-AzureRmAccount`</span><span class="sxs-lookup"><span data-stu-id="fcda8-265">Corrected usage of `Login-AzureRmAccount` to use `Connect-AzureRmAccount`</span></span>

### <a name="azurermcompute"></a><span data-ttu-id="fcda8-266">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="fcda8-266">AzureRM.Compute</span></span>
* <span data-ttu-id="fcda8-267">向 `New-AzureRmVM` 的简化参数集添加了 `-AvailabilitySetName` 参数。</span><span class="sxs-lookup"><span data-stu-id="fcda8-267">Added `-AvailabilitySetName` parameter to the simplified parameterset of `New-AzureRmVM`.</span></span>
* <span data-ttu-id="fcda8-268">更正了 `Login-AzureRmAccount` 的用法以使用 `Connect-AzureRmAccount`</span><span class="sxs-lookup"><span data-stu-id="fcda8-268">Corrected usage of `Login-AzureRmAccount` to use `Connect-AzureRmAccount`</span></span>
* <span data-ttu-id="fcda8-269">对 VM 和 VM 规模集的用户分配标识支持</span><span class="sxs-lookup"><span data-stu-id="fcda8-269">User assigned identity support for VM and VM scale set</span></span>
    - <span data-ttu-id="fcda8-270">将 `-IdentityType` 和 `-IdentityId` 参数添加到了 `New-AzureRmVMConfig`、`New-AzureRmVmssConfig`、`Update-AzureRmVM` 和 `Update-AzureRmVmss`</span><span class="sxs-lookup"><span data-stu-id="fcda8-270">`-IdentityType` and `-IdentityId` parameters are added to `New-AzureRmVMConfig`, `New-AzureRmVmssConfig`, `Update-AzureRmVM` and `Update-AzureRmVmss`</span></span>
* <span data-ttu-id="fcda8-271">为 `Add-AzureRmVmssNetworkInterfaceConfig` 添加了 `-EnableIPForwarding` 参数</span><span class="sxs-lookup"><span data-stu-id="fcda8-271">Added `-EnableIPForwarding` parameter to `Add-AzureRmVmssNetworkInterfaceConfig`</span></span>
* <span data-ttu-id="fcda8-272">为 `New-AzureRmVmssConfig` 添加了 `-Priority` 参数</span><span class="sxs-lookup"><span data-stu-id="fcda8-272">Added `-Priority` parameter to `New-AzureRmVmssConfig`</span></span>

### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="fcda8-273">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="fcda8-273">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="fcda8-274">更正了 `Login-AzureRmAccount` 的用法以使用 `Connect-AzureRmAccount`</span><span class="sxs-lookup"><span data-stu-id="fcda8-274">Corrected usage of `Login-AzureRmAccount` to use `Connect-AzureRmAccount`</span></span>

### <a name="azurermdatalakestore"></a><span data-ttu-id="fcda8-275">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fcda8-275">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="fcda8-276">更正了 `Login-AzureRmAccount` 的用法以使用 `Connect-AzureRmAccount`</span><span class="sxs-lookup"><span data-stu-id="fcda8-276">Corrected usage of `Login-AzureRmAccount` to use `Connect-AzureRmAccount`</span></span>
* <span data-ttu-id="fcda8-277">更正了未使用 `Login-AzureRmAccount` 登录便运行 `Test-AzureRmDataLakeStoreAccount` 时显示的此 cmdlet 的错误消息</span><span class="sxs-lookup"><span data-stu-id="fcda8-277">Corrected the error message of `Test-AzureRmDataLakeStoreAccount` when running this cmdlet without having logged in with `Login-AzureRmAccount`</span></span>

### <a name="azurermeventgrid"></a><span data-ttu-id="fcda8-278">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="fcda8-278">AzureRM.EventGrid</span></span>
* <span data-ttu-id="fcda8-279">已更新以使用 2018-01-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="fcda8-279">Updated to use the 2018-01-01 API version.</span></span>

### <a name="azurermeventhub"></a><span data-ttu-id="fcda8-280">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="fcda8-280">AzureRM.EventHub</span></span>

* <span data-ttu-id="fcda8-281">添加了以下新命令以便执行异地灾难恢复操作。</span><span class="sxs-lookup"><span data-stu-id="fcda8-281">Added below new commands for Geo Disaster Recovery operations.</span></span>
  - <span data-ttu-id="fcda8-282">创建新别名（灾难恢复配置）：</span><span class="sxs-lookup"><span data-stu-id="fcda8-282">Creating a new Alias (Disaster Recovery configuration):</span></span>
    - `New-AzureRmEventHubGeoDRConfiguration`
  - <span data-ttu-id="fcda8-283">检索别名（灾难恢复配置）：</span><span class="sxs-lookup"><span data-stu-id="fcda8-283">Retrieve Alias (Disaster Recovery configuration) :</span></span>
    - `Get-AzureRmEventHubGeoDRConfiguration`
  - <span data-ttu-id="fcda8-284">禁用灾难恢复，并停止从主命名空间向辅助命名空间复制更改</span><span class="sxs-lookup"><span data-stu-id="fcda8-284">Disabling the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>
    - `Set-AzureRmEventHubGeoDRConfigurationBreakPair`
  - <span data-ttu-id="fcda8-285">调用灾难恢复故障转移并将别名重新配置为指向辅助命名空间</span><span class="sxs-lookup"><span data-stu-id="fcda8-285">Invoking Disaster Recovery failover and reconfigure the alias to point to the secondary namespace</span></span>
    - `Set-AzureRmEventHubGeoDRConfigurationFailOver`
  - <span data-ttu-id="fcda8-286">删除别名（灾难恢复配置）</span><span class="sxs-lookup"><span data-stu-id="fcda8-286">Deleting an Alias(Disaster Recovery configuration)</span></span>
    - `Remove-AzureRmEventHubGeoDRConfiguration`
* <span data-ttu-id="fcda8-287">添加了以下新命令，用于检查命名空间名称和 GeoDr 配置名称 - 别名可用性。</span><span class="sxs-lookup"><span data-stu-id="fcda8-287">Added below new commands for checking the Namespace Name and GeoDr Configuration Name - Alias availability.</span></span>
  - <span data-ttu-id="fcda8-288">检查命名空间名称或别名（灾难恢复配置）名称的可用性：</span><span class="sxs-lookup"><span data-stu-id="fcda8-288">Check the Availability of Namespace name or Alias(Disaster Recovery configuration) name:</span></span>
    - `Test-AzureRmEventHubName`

### <a name="azurerminsights"></a><span data-ttu-id="fcda8-289">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="fcda8-289">AzureRM.Insights</span></span>
* <span data-ttu-id="fcda8-290">更正了 `Login-AzureRmAccount` 的用法以使用 `Connect-AzureRmAccount`</span><span class="sxs-lookup"><span data-stu-id="fcda8-290">Corrected usage of `Login-AzureRmAccount` to use `Connect-AzureRmAccount`</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="fcda8-291">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="fcda8-291">AzureRM.KeyVault</span></span>
* <span data-ttu-id="fcda8-292">更正了 `Login-AzureRmAccount` 的用法以使用 `Connect-AzureRmAccount`</span><span class="sxs-lookup"><span data-stu-id="fcda8-292">Corrected usage of `Login-AzureRmAccount` to use `Connect-AzureRmAccount`</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="fcda8-293">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="fcda8-293">AzureRM.Network</span></span>
* <span data-ttu-id="fcda8-294">修复了覆盖消息“是否确实要覆盖资源”</span><span class="sxs-lookup"><span data-stu-id="fcda8-294">Fix overwrite message 'Are you sure you want to overwriteresource'</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="fcda8-295">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="fcda8-295">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="fcda8-296">通过 `Invoke-AzureRmOperationalInsightsQuery` 添加了对 V2 API 查询的支持。</span><span class="sxs-lookup"><span data-stu-id="fcda8-296">Added support for V2 API querying via `Invoke-AzureRmOperationalInsightsQuery`.</span></span> <span data-ttu-id="fcda8-297">有关新 API 的详细信息，请参阅 [https://dev.loganalytics.io/](https://dev.loganalytics.io/)。</span><span class="sxs-lookup"><span data-stu-id="fcda8-297">See [https://dev.loganalytics.io/](https://dev.loganalytics.io/) for more info on the new API.</span></span>

### <a name="azurermresources"></a><span data-ttu-id="fcda8-298">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="fcda8-298">AzureRM.Resources</span></span>
* <span data-ttu-id="fcda8-299">`Get-AzureRmADServicePrincipal`：从默认 Empty 参数集中删除了 `-ServicePrincipalName`，因为它对于 SPN 参数集是冗余的</span><span class="sxs-lookup"><span data-stu-id="fcda8-299">`Get-AzureRmADServicePrincipal`: Removed `-ServicePrincipalName` from the default Empty parameter set as it was redundant with the SPN parameter set</span></span>

### <a name="azurermservicebus"></a><span data-ttu-id="fcda8-300">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="fcda8-300">AzureRM.ServiceBus</span></span>

* <span data-ttu-id="fcda8-301">为 `Remove-AzureRmServiceBusRule` 和 `Get-AzureRmServiceBusKey` 添加了功能修复</span><span class="sxs-lookup"><span data-stu-id="fcda8-301">Added functionality fix for `Remove-AzureRmServiceBusRule` and `Get-AzureRmServiceBusKey`</span></span>
* <span data-ttu-id="fcda8-302">添加了以下新 cmdlet 以便执行异地灾难恢复操作。</span><span class="sxs-lookup"><span data-stu-id="fcda8-302">Added below new commandlets for Geo Disaster Recovery operations.</span></span>
  - <span data-ttu-id="fcda8-303">创建新别名（灾难恢复配置）：</span><span class="sxs-lookup"><span data-stu-id="fcda8-303">Creating a new Alias (Disaster Recovery configuration):</span></span>
    - `New-AzureRmServiceBusDRConfigurations`
  - <span data-ttu-id="fcda8-304">检索别名（灾难恢复配置）：</span><span class="sxs-lookup"><span data-stu-id="fcda8-304">Retrieve Alias (Disaster Recovery configuration) :</span></span>
    - `Get-AzureRmServiceBusDRConfigurations`
  - <span data-ttu-id="fcda8-305">禁用灾难恢复，并停止从主命名空间向辅助命名空间复制更改</span><span class="sxs-lookup"><span data-stu-id="fcda8-305">Disabling the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>
    - `Set-AzureRmServiceBusDRConfigurationsBreakPairing`
  - <span data-ttu-id="fcda8-306">调用灾难恢复故障转移并将别名重新配置为指向辅助命名空间</span><span class="sxs-lookup"><span data-stu-id="fcda8-306">Invoking Disaster Recovery failover and reconfigure the alias to point to the secondary namespace</span></span>
    - `Set-AzureRmServiceBusDRConfigurationsFailOver`
  - <span data-ttu-id="fcda8-307">删除别名（灾难恢复配置）</span><span class="sxs-lookup"><span data-stu-id="fcda8-307">Deleting an Alias(Disaster Recovery configuration)</span></span>
    - `Remove-AzureRmServiceBusDRConfigurations`
* <span data-ttu-id="fcda8-308">更新了 `Test-AzureRmServiceBusName` cmdlet 以支持异地灾难恢复 - 别名检查可用性操作。</span><span class="sxs-lookup"><span data-stu-id="fcda8-308">Updated `Test-AzureRmServiceBusName` commandlets to support Geo Disaster Recovery - Alias name check availability operations.</span></span>
  - <span data-ttu-id="fcda8-309">检查命名空间名称或别名（灾难恢复配置）名称的可用性：</span><span class="sxs-lookup"><span data-stu-id="fcda8-309">Check the Availability of Namespace name or Alias(Disaster Recovery configuration) name:</span></span>
    - `Test-AzureRmServiceBusName`

### <a name="azurermusageaggregates"></a><span data-ttu-id="fcda8-310">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="fcda8-310">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="fcda8-311">更正了 `Login-AzureRmAccount` 的用法以使用 `Connect-AzureRmAccount`</span><span class="sxs-lookup"><span data-stu-id="fcda8-311">Corrected usage of `Login-AzureRmAccount` to use `Connect-AzureRmAccount`</span></span>

## <a name="520---january-2018"></a><span data-ttu-id="fcda8-312">5.2.0 - 2018 年 1 月</span><span class="sxs-lookup"><span data-stu-id="fcda8-312">5.2.0 - January 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="fcda8-313">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="fcda8-313">AzureRM.Profile</span></span>
* <span data-ttu-id="fcda8-314">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="fcda8-314">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="fcda8-315">Add-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="fcda8-315">Add-AzureRmAccount</span></span>
  * <span data-ttu-id="fcda8-316">添加了 -MSI 登录名，用于通过当前 VM/服务的托管服务标识的凭据进行身份验证</span><span class="sxs-lookup"><span data-stu-id="fcda8-316">Added -MSI login for authenticationg using the credentials of the Managed Service Identity of the current VM / Service</span></span>
  * <span data-ttu-id="fcda8-317">修复了使用用户提供的访问令牌登录时存在的 KeyVault 身份验证问题</span><span class="sxs-lookup"><span data-stu-id="fcda8-317">Fixed KeyVault Authentication when logging in with user-provided access tokens</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="fcda8-318">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="fcda8-318">Azure.Storage</span></span>
* <span data-ttu-id="fcda8-319">添加了 cmdlet 用于获取和设置存储服务属性</span><span class="sxs-lookup"><span data-stu-id="fcda8-319">Add cmdlets to get and set Storage service properties</span></span>
    - <span data-ttu-id="fcda8-320">Get-AzureStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="fcda8-320">Get-AzureStorageServiceProperty</span></span>
    - <span data-ttu-id="fcda8-321">Update-AzureStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="fcda8-321">Update-AzureStorageServiceProperty</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="fcda8-322">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="fcda8-322">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="fcda8-323">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="fcda8-323">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="fcda8-324">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="fcda8-324">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="fcda8-325">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="fcda8-325">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="fcda8-326">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="fcda8-326">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="fcda8-327">已弃用 -Tags，对 New-AzureRmApiManagementProperty、Set-AzureRmApiManagementProperty 和 New-AzureRmApiManagement 改用 -Tag</span><span class="sxs-lookup"><span data-stu-id="fcda8-327">Obsoleted -Tags in favor of -Tag for New-AzureRmApiManagementProperty, Set-AzureRmApiManagementProperty, and New-AzureRmApiManagement</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="fcda8-328">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="fcda8-328">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="fcda8-329">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="fcda8-329">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="fcda8-330">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="fcda8-330">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="fcda8-331">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="fcda8-331">AzureRM.Automation</span></span>
* <span data-ttu-id="fcda8-332">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="fcda8-332">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="fcda8-333">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="fcda8-333">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="fcda8-334">已弃用 -Tags，对 Set-AzureRmAutomationRunbook 改用 -Tag</span><span class="sxs-lookup"><span data-stu-id="fcda8-334">Obsoleted -Tags in favor of -Tag for Set-AzureRmAutomationRunbook</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="fcda8-335">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="fcda8-335">AzureRM.Backup</span></span>
* <span data-ttu-id="fcda8-336">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="fcda8-336">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="fcda8-337">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="fcda8-337">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="fcda8-338">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="fcda8-338">AzureRM.Batch</span></span>
* <span data-ttu-id="fcda8-339">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="fcda8-339">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="fcda8-340">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="fcda8-340">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="fcda8-341">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="fcda8-341">AzureRM.Cdn</span></span>
* <span data-ttu-id="fcda8-342">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="fcda8-342">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="fcda8-343">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="fcda8-343">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="fcda8-344">已弃用 -Tags，对 New-AzureRmCdnEndpoint 和 New-AzureRmCdnProfile 改用 -Tag</span><span class="sxs-lookup"><span data-stu-id="fcda8-344">Obsoleted -Tags in favor of -Tag for New-AzureRmCdnEndpoint and New-AzureRmCdnProfile</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="fcda8-345">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="fcda8-345">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="fcda8-346">与认知服务管理 SDK 版本 3.0.0 集成。</span><span class="sxs-lookup"><span data-stu-id="fcda8-346">Integrate with Cognitive Services Management SDK version 3.0.0.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="fcda8-347">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="fcda8-347">AzureRM.Compute</span></span>
* <span data-ttu-id="fcda8-348">为 New-AzureRmVmss 添加了简化的参数集，用于通过智能默认值创建虚拟机规模集和所有必需的资源</span><span class="sxs-lookup"><span data-stu-id="fcda8-348">Added simplified parameter set to New-AzureRmVmss, which creates a Virtual Machine Scale Set and all required resources using smart defaults</span></span>
* <span data-ttu-id="fcda8-349">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="fcda8-349">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="fcda8-350">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="fcda8-350">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="fcda8-351">已弃用 -Tags，对 New-AzureRmVm 和 Update-AzureRmVm 改用 -Tag</span><span class="sxs-lookup"><span data-stu-id="fcda8-351">Obsoleted -Tags in favor of -Tag for New-AzureRmVm and Update-AzureRmVm</span></span>
* <span data-ttu-id="fcda8-352">修复了 Zone 受限制时的 Get-AzureRmComputeResourceSku cmdlet 问题。</span><span class="sxs-lookup"><span data-stu-id="fcda8-352">Fixed Get-AzureRmComputeResourceSku cmdlet when Zone is included in restriction.</span></span>
* <span data-ttu-id="fcda8-353">为 Azure Monitor 接收器支持更新了诊断代理配置架构。</span><span class="sxs-lookup"><span data-stu-id="fcda8-353">Updated Diagnostics Agent configuration schema for Azure Monitor sink support.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="fcda8-354">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="fcda8-354">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="fcda8-355">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="fcda8-355">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="fcda8-356">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="fcda8-356">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="fcda8-357">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="fcda8-357">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="fcda8-358">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="fcda8-358">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="fcda8-359">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="fcda8-359">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="fcda8-360">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="fcda8-360">AzureRM.DataFactories</span></span>
* <span data-ttu-id="fcda8-361">对所有数据存储链接服务启用了 Azure Key Vault 支持</span><span class="sxs-lookup"><span data-stu-id="fcda8-361">Enabled Azure Key Vault support for all data store linked services</span></span>
* <span data-ttu-id="fcda8-362">添加了 Azure SSIS 集成运行时的许可证类型属性</span><span class="sxs-lookup"><span data-stu-id="fcda8-362">Added license type property for Azure SSIS integration runtime</span></span>
* <span data-ttu-id="fcda8-363">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="fcda8-363">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="fcda8-364">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="fcda8-364">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="fcda8-365">已弃用 -Tags，对 New-AzureRmDataFactory 改用 -Tag</span><span class="sxs-lookup"><span data-stu-id="fcda8-365">Obsoleted -Tags in favor of -Tag for New-AzureRmDataFactory</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="fcda8-366">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="fcda8-366">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="fcda8-367">对所有数据存储链接服务启用了 Azure Key Vault 支持</span><span class="sxs-lookup"><span data-stu-id="fcda8-367">Enabled Azure Key Vault support for all data store linked services</span></span>
* <span data-ttu-id="fcda8-368">添加了 Azure SSIS 集成运行时的许可证类型属性</span><span class="sxs-lookup"><span data-stu-id="fcda8-368">Added license type property for Azure SSIS integration runtime</span></span>
* <span data-ttu-id="fcda8-369">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="fcda8-369">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="fcda8-370">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="fcda8-370">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="fcda8-371">为“Set-AzureRmDataFactoryV2IntegrationRuntime”cmd 添加了参数“LicenseType”，以启用 AHUB 功能</span><span class="sxs-lookup"><span data-stu-id="fcda8-371">Add parameter "LicenseType" for "Set-AzureRmDataFactoryV2IntegrationRuntime" cmd to enable AHUB functionality</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="fcda8-372">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="fcda8-372">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="fcda8-373">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="fcda8-373">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="fcda8-374">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="fcda8-374">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="fcda8-375">已弃用 -Tags，对 New-AzureRmDataLakeAnalyticsAccount 和 Set-AzureRmDataLakeAnalyticsAccount 改用 -Tag</span><span class="sxs-lookup"><span data-stu-id="fcda8-375">Obsoleted -Tags in favor of -Tag for New-AzureRmDataLakeAnalyticsAccount and Set-AzureRmDataLakeAnalyticsAccount</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="fcda8-376">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fcda8-376">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="fcda8-377">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="fcda8-377">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="fcda8-378">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="fcda8-378">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="fcda8-379">已弃用 -Tags，对 New-AzureRmDataLakeStoreAccount 和 Set-AzureRmDataLakeStoreAccount 改用 -Tag</span><span class="sxs-lookup"><span data-stu-id="fcda8-379">Obsoleted -Tags in favor of -Tag for New-AzureRmDataLakeStoreAccount and Set-AzureRmDataLakeStoreAccount</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="fcda8-380">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="fcda8-380">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="fcda8-381">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="fcda8-381">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="fcda8-382">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="fcda8-382">AzureRM.Dns</span></span>
* <span data-ttu-id="fcda8-383">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="fcda8-383">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="fcda8-384">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="fcda8-384">AzureRM.EventGrid</span></span>
* <span data-ttu-id="fcda8-385">添加了以下新的 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="fcda8-385">Added the following new cmdlet:</span></span>
  - <span data-ttu-id="fcda8-386">Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="fcda8-386">Update-AzureRmEventGridSubscription</span></span>
    - <span data-ttu-id="fcda8-387">更新了事件网格事件订阅的属性。</span><span class="sxs-lookup"><span data-stu-id="fcda8-387">Update the properties of an Event Grid event subscription.</span></span>
* <span data-ttu-id="fcda8-388">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="fcda8-388">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="fcda8-389">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="fcda8-389">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="fcda8-390">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="fcda8-390">AzureRM.EventHub</span></span>
* <span data-ttu-id="fcda8-391">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="fcda8-391">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="fcda8-392">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="fcda8-392">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="fcda8-393">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="fcda8-393">AzureRM.HDInsight</span></span>
* <span data-ttu-id="fcda8-394">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="fcda8-394">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="fcda8-395">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="fcda8-395">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="fcda8-396">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="fcda8-396">AzureRM.Insights</span></span>
* <span data-ttu-id="fcda8-397">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="fcda8-397">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="fcda8-398">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="fcda8-398">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="fcda8-399">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="fcda8-399">AzureRM.IotHub</span></span>
* <span data-ttu-id="fcda8-400">添加了对 IoTHub cmdlet 的 Certificate 支持</span><span class="sxs-lookup"><span data-stu-id="fcda8-400">Add Certificate support for IoTHub cmdlets</span></span>
* <span data-ttu-id="fcda8-401">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="fcda8-401">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="fcda8-402">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="fcda8-402">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="fcda8-403">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="fcda8-403">AzureRM.KeyVault</span></span>
* <span data-ttu-id="fcda8-404">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="fcda8-404">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="fcda8-405">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="fcda8-405">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="fcda8-406">添加了对长时间运行的 KeyVault cmdlet 的 -AsJob 支持。</span><span class="sxs-lookup"><span data-stu-id="fcda8-406">Added -AsJob support for long-running KeyVault cmdlets.</span></span> <span data-ttu-id="fcda8-407">允许选定的 cmdlet 在后台运行并返回可跟踪和控制进度的作业。</span><span class="sxs-lookup"><span data-stu-id="fcda8-407">Allows selected cmdlets to run in the background and return a job to track and control progress.</span></span>
  * <span data-ttu-id="fcda8-408">受影响的 cmdlet 为：Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="fcda8-408">Affected cmdlet is: Remove-AzureRmKeyVault</span></span>
* <span data-ttu-id="fcda8-409">修复了 Set-AzureRmKeyVaultAccessPolicy 的 bug：AAD 筛选器将 SPN 设置为提供的 UPN，而不是设置 UPN</span><span class="sxs-lookup"><span data-stu-id="fcda8-409">Fixed bug in Set-AzureRmKeyVaultAccessPolicy where the AAD filter was setting SPN to the provided UPN, rather than setting the UPN</span></span>
  - <span data-ttu-id="fcda8-410">有关详细信息，请参阅以下问题：https://github.com/Azure/azure-powershell/issues/5201</span><span class="sxs-lookup"><span data-stu-id="fcda8-410">See the following issue for more information: https://github.com/Azure/azure-powershell/issues/5201</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="fcda8-411">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="fcda8-411">AzureRM.LogicApp</span></span>
* <span data-ttu-id="fcda8-412">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="fcda8-412">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="fcda8-413">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="fcda8-413">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="fcda8-414">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="fcda8-414">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="fcda8-415">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="fcda8-415">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="fcda8-416">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="fcda8-416">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="fcda8-417">已弃用 -Tags，对 Update-AzureRmMlCommitmentPlan 改用 -Tag</span><span class="sxs-lookup"><span data-stu-id="fcda8-417">Obsoleted -Tags in favor of -Tag for Update-AzureRmMlCommitmentPlan</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="fcda8-418">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="fcda8-418">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="fcda8-419">将 IncludeAllResources 参数添加到了 Remove-AzureRmMlOpCluster cmdlet</span><span class="sxs-lookup"><span data-stu-id="fcda8-419">Add IncludeAllResources parameter to Remove-AzureRmMlOpCluster cmdlet</span></span>
  - <span data-ttu-id="fcda8-420">使用此开关参数会删除最初在群集中创建的所有资源</span><span class="sxs-lookup"><span data-stu-id="fcda8-420">Using this switch parameter will remove all resources that were created with the cluster originally</span></span>
* <span data-ttu-id="fcda8-421">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="fcda8-421">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="fcda8-422">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="fcda8-422">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="fcda8-423">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="fcda8-423">AzureRM.Media</span></span>
* <span data-ttu-id="fcda8-424">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="fcda8-424">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="fcda8-425">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="fcda8-425">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="fcda8-426">已弃用 -Tags，对 Set-AzureRmMediaService 和 New-AzureRmMediaService 改用 -Tag</span><span class="sxs-lookup"><span data-stu-id="fcda8-426">Obsoleted -Tags in favor of -Tag for Set-AzureRmMediaService and New-AzureRmMediaService</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="fcda8-427">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="fcda8-427">AzureRM.Network</span></span>
* <span data-ttu-id="fcda8-428">添加了对长时间运行的 Network cmdlet 的 -AsJob 支持。</span><span class="sxs-lookup"><span data-stu-id="fcda8-428">Added -AsJob support for long-running Network cmdlets.</span></span> <span data-ttu-id="fcda8-429">允许选定的 cmdlet 在后台运行并返回可跟踪和控制进度的作业。</span><span class="sxs-lookup"><span data-stu-id="fcda8-429">Allows selected cmdlets to run in the background and return a job to track and control progress.</span></span>
* <span data-ttu-id="fcda8-430">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="fcda8-430">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="fcda8-431">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="fcda8-431">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="fcda8-432">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="fcda8-432">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="fcda8-433">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="fcda8-433">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="fcda8-434">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="fcda8-434">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="fcda8-435">已弃用 -Tags，对 New-AzureRmNotificationHubsNamespace 和 Set-AzureRmNotificationHubsNamespace 改用 -Tag</span><span class="sxs-lookup"><span data-stu-id="fcda8-435">Obsoleted -Tags in favor of -Tag for New-AzureRmNotificationHubsNamespace and Set-AzureRmNotificationHubsNamespace</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="fcda8-436">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="fcda8-436">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="fcda8-437">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="fcda8-437">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="fcda8-438">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="fcda8-438">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="fcda8-439">已弃用 -Tags，对 New-AzureRmOperationalInsightsSavedSearch、Set-AzureRmOperationalInsightsSavedSearch、New-AzureRmOperationalInsightsWorkspace 和 Set-AzureRmOperationalInsightsWorkspace 改用 -Tag</span><span class="sxs-lookup"><span data-stu-id="fcda8-439">Obsoleted -Tags in favor of -Tag for New-AzureRmOperationalInsightsSavedSearch, Set-AzureRmOperationalInsightsSavedSearch, New-AzureRmOperationalInsightsWorkspace, and Set-AzureRmOperationalInsightsWorkspace</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="fcda8-440">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="fcda8-440">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="fcda8-441">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="fcda8-441">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="fcda8-442">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="fcda8-442">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="fcda8-443">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fcda8-443">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="fcda8-444">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="fcda8-444">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="fcda8-445">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="fcda8-445">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="fcda8-446">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="fcda8-446">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="fcda8-447">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="fcda8-447">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="fcda8-448">为 Restore-AzureRmRecoveryServicesBackupItem cmdlet 添加了 -UseOriginalStorageAccount 选项。</span><span class="sxs-lookup"><span data-stu-id="fcda8-448">Added -UseOriginalStorageAccount option to the Restore-AzureRmRecoveryServicesBackupItem cmdlet.</span></span>
  - <span data-ttu-id="fcda8-449">启用此标志会导致将磁盘还原到其原始存储帐户，从而让用户尽量将还原后的 VM 的配置接近原始 VM。</span><span class="sxs-lookup"><span data-stu-id="fcda8-449">Enabling this flag results in restoring disks to their original storage accounts which allows users to maintain the configuration of restored VM as close to the original VMs as possible.</span></span>
  - <span data-ttu-id="fcda8-450">此外，这还有助于提高还原操作的性能。</span><span class="sxs-lookup"><span data-stu-id="fcda8-450">It also helps in improving the performance of the restore operation.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="fcda8-451">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="fcda8-451">AzureRM.RedisCache</span></span>
* <span data-ttu-id="fcda8-452">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="fcda8-452">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="fcda8-453">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="fcda8-453">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="fcda8-454">为防火墙规则添加了 3 个新的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="fcda8-454">Added  3 new cmdlets for firewall rules</span></span>
* <span data-ttu-id="fcda8-455">为异地复制添加了 3 个新的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="fcda8-455">Added  3 new cmdlets for geo replication</span></span>
* <span data-ttu-id="fcda8-456">添加了对区域和标记的支持</span><span class="sxs-lookup"><span data-stu-id="fcda8-456">Added support for zones and tags</span></span>
* <span data-ttu-id="fcda8-457">尽量将 ResourceGroup 用作可选选项。</span><span class="sxs-lookup"><span data-stu-id="fcda8-457">Make ResourceGroup as optional whenever possible.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="fcda8-458">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="fcda8-458">AzureRM.Relay</span></span>
* <span data-ttu-id="fcda8-459">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="fcda8-459">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="fcda8-460">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="fcda8-460">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="fcda8-461">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="fcda8-461">AzureRM.Resources</span></span>
* <span data-ttu-id="fcda8-462">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="fcda8-462">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="fcda8-463">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="fcda8-463">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="fcda8-464">添加了对长时间运行的 Resources cmdlet 的 -AsJob 支持。</span><span class="sxs-lookup"><span data-stu-id="fcda8-464">Added -AsJob support for long-running Resources cmdlets.</span></span> <span data-ttu-id="fcda8-465">允许选定的 cmdlet 在后台运行并返回可跟踪和控制进度的作业。</span><span class="sxs-lookup"><span data-stu-id="fcda8-465">Allows selected cmdlets to run in the background and return a job to track and control progress.</span></span>
* <span data-ttu-id="fcda8-466">将别名从 Get-AzureRmProviderOperation 更改为 Get-AzureRmResourceProviderAction，以符合命名约定</span><span class="sxs-lookup"><span data-stu-id="fcda8-466">Added alias from Get-AzureRmProviderOperation to Get-AzureRmResourceProviderAction to conform with naming conventions</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="fcda8-467">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="fcda8-467">AzureRM.Scheduler</span></span>
* <span data-ttu-id="fcda8-468">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="fcda8-468">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="fcda8-469">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="fcda8-469">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermservermanagement"></a><span data-ttu-id="fcda8-470">AzureRM.ServerManagement</span><span class="sxs-lookup"><span data-stu-id="fcda8-470">AzureRM.ServerManagement</span></span>
* <span data-ttu-id="fcda8-471">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="fcda8-471">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="fcda8-472">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="fcda8-472">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="fcda8-473">已弃用 -Tags，对 New-AzureRmServerManagementNode 和 New-AzureRmServerManagementGateway 改用 -Tag</span><span class="sxs-lookup"><span data-stu-id="fcda8-473">Obsoleted -Tags in favor of -Tag for New-AzureRmServerManagementNode and New-AzureRmServerManagementGateway</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="fcda8-474">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="fcda8-474">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="fcda8-475">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="fcda8-475">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="fcda8-476">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="fcda8-476">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="fcda8-477">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="fcda8-477">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="fcda8-478">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="fcda8-478">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="fcda8-479">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="fcda8-479">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermsiterecovery"></a><span data-ttu-id="fcda8-480">AzureRM.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="fcda8-480">AzureRM.SiteRecovery</span></span>
* <span data-ttu-id="fcda8-481">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="fcda8-481">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="fcda8-482">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="fcda8-482">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="fcda8-483">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="fcda8-483">AzureRM.Sql</span></span>
* <span data-ttu-id="fcda8-484">更新了 Auditing 命令参数说明</span><span class="sxs-lookup"><span data-stu-id="fcda8-484">Update the Auditing commands parameters description</span></span>
* <span data-ttu-id="fcda8-485">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="fcda8-485">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="fcda8-486">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="fcda8-486">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="fcda8-487">为长时间运行的 cmdlet 添加了 -AsJob 参数</span><span class="sxs-lookup"><span data-stu-id="fcda8-487">Added -AsJob parameter to long running cmdlets</span></span>
* <span data-ttu-id="fcda8-488">已弃用 Get-AzureRmSqlServiceObjective 的 -DatabaseName 参数</span><span class="sxs-lookup"><span data-stu-id="fcda8-488">Obsoleted -DatabaseName parameter from Get-AzureRmSqlServiceObjective</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="fcda8-489">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="fcda8-489">AzureRM.Storage</span></span>
* <span data-ttu-id="fcda8-490">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="fcda8-490">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="fcda8-491">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="fcda8-491">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="fcda8-492">修复了结合 -EnableEncryptionService None 参数运行 cmdlet New-AzureRMStorageAccount 时的空引用问题</span><span class="sxs-lookup"><span data-stu-id="fcda8-492">Fix a null reference issue of run cmdlet New-AzureRMStorageAccount with parameter -EnableEncryptionService None</span></span>
* <span data-ttu-id="fcda8-493">添加了对长时间运行的 Storage cmdlet 的 -AsJob 支持。</span><span class="sxs-lookup"><span data-stu-id="fcda8-493">Added -AsJob support for long-running Storage cmdlets.</span></span> <span data-ttu-id="fcda8-494">允许选定的 cmdlet 在后台运行并返回可跟踪和控制进度的作业。</span><span class="sxs-lookup"><span data-stu-id="fcda8-494">Allows selected cmdlets to run in the background and return a job to track and control progress.</span></span>
    - <span data-ttu-id="fcda8-495">受影响的 cmdlet 为针对存储帐户和存储帐户网络规则的 New-、Remove-、Add- 和 Update-。</span><span class="sxs-lookup"><span data-stu-id="fcda8-495">Affected cmdlets are New-, Remove-, Add-, and Update- for Storage Account and Storage Account Network Rule.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="fcda8-496">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="fcda8-496">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="fcda8-497">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="fcda8-497">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="fcda8-498">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="fcda8-498">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="fcda8-499">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="fcda8-499">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="fcda8-500">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="fcda8-500">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="fcda8-501">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="fcda8-501">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="fcda8-502">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="fcda8-502">AzureRM.Websites</span></span>
* <span data-ttu-id="fcda8-503">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="fcda8-503">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="fcda8-504">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="fcda8-504">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="fcda8-505">添加了对长时间运行的 Websites cmdlet 的 -AsJob 支持。</span><span class="sxs-lookup"><span data-stu-id="fcda8-505">Added -AsJob support for long-running Websites cmdlets.</span></span> <span data-ttu-id="fcda8-506">允许选定的 cmdlet 在后台运行并返回可跟踪和控制进度的作业。</span><span class="sxs-lookup"><span data-stu-id="fcda8-506">Allows selected cmdlets to run in the background and return a job to track and control progress.</span></span>
     - <span data-ttu-id="fcda8-507">受影响的 cmdlet 为针对 Web 应用、应用服务计划和槽位的 New-、Remove-、Add- 和 Set-</span><span class="sxs-lookup"><span data-stu-id="fcda8-507">Affected cmdlets are New-, Remove-, Add-, and Set- for WebApps, AppServicePlan and Slots</span></span>

## <a name="2017128-version-511"></a><span data-ttu-id="fcda8-508">2017.12.8 版本 5.1.1</span><span class="sxs-lookup"><span data-stu-id="fcda8-508">2017.12.8 Version 5.1.1</span></span>
* <span data-ttu-id="fcda8-509">AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="fcda8-509">AnalysisServices</span></span>
  - <span data-ttu-id="fcda8-510">将位置的验证集更改为动态查找，以便支持所有云。</span><span class="sxs-lookup"><span data-stu-id="fcda8-510">Change validate set of location to dynamic lookup so that all clouds are supported.</span></span>
* <span data-ttu-id="fcda8-511">自动化</span><span class="sxs-lookup"><span data-stu-id="fcda8-511">Automation</span></span>
  - <span data-ttu-id="fcda8-512">更新为 Import-AzureRMAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="fcda8-512">Update to Import-AzureRMAutomationRunbook</span></span>
    - <span data-ttu-id="fcda8-513">现在为 Python2 Runbook 提供支持</span><span class="sxs-lookup"><span data-stu-id="fcda8-513">Support is now being provided for Python2 runbooks</span></span>
* <span data-ttu-id="fcda8-514">Batch</span><span class="sxs-lookup"><span data-stu-id="fcda8-514">Batch</span></span>
  - <span data-ttu-id="fcda8-515">修复了没有资源组时帐户操作无法自动检测资源组这一 Bug</span><span class="sxs-lookup"><span data-stu-id="fcda8-515">Fixed a bug where account operations without a resource group failed to auto-detect the resource group</span></span>
* <span data-ttu-id="fcda8-516">计算</span><span class="sxs-lookup"><span data-stu-id="fcda8-516">Compute</span></span>
  - <span data-ttu-id="fcda8-517">Get-AzureRmComputeResourceSku 显示区域信息。</span><span class="sxs-lookup"><span data-stu-id="fcda8-517">Get-AzureRmComputeResourceSku shows zone information.</span></span>
  - <span data-ttu-id="fcda8-518">更新 Disable-AzureRmVmssDiskEncryption 以修复问题 https://github.com/Azure/azure-powershell/issues/5038</span><span class="sxs-lookup"><span data-stu-id="fcda8-518">Update Disable-AzureRmVmssDiskEncryption to fix issue https://github.com/Azure/azure-powershell/issues/5038</span></span>
  - <span data-ttu-id="fcda8-519">添加了对长时间运行的计算 cmdlet 的 -AsJob 支持。</span><span class="sxs-lookup"><span data-stu-id="fcda8-519">Added -AsJob support for long-running Compute cmdlets.</span></span> <span data-ttu-id="fcda8-520">允许选定的 cmdlet 在后台运行并返回可跟踪和控制进度的作业。</span><span class="sxs-lookup"><span data-stu-id="fcda8-520">Allows selected cmdlets to run in the background and return a job to track and control progress.</span></span>
    - <span data-ttu-id="fcda8-521">受影响的 cmdlet 包括适用于虚拟机和虚拟机规模集的 New-、Update-、Set-、Remove-、Start-、Restart-、Stop- cmdlet</span><span class="sxs-lookup"><span data-stu-id="fcda8-521">Affected cmdlets include: New-, Update-, Set-, Remove-, Start-, Restart-, Stop- cmdlets for Virtual Machines and Virtual Machine Scale Sets</span></span>
    - <span data-ttu-id="fcda8-522">向 New-AzureRmVM（可使用智能默认设置创建虚拟机和所有必需的资源）添加了简化的参数集</span><span class="sxs-lookup"><span data-stu-id="fcda8-522">Added simplified parameter set to New-AzureRmVM, which creates a Virtual Machine and all required resources using smart defaults</span></span>
* <span data-ttu-id="fcda8-523">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="fcda8-523">ContainerInstance</span></span>
  - <span data-ttu-id="fcda8-524">应用 Azure 容器实例 SDK 2017-10-01</span><span class="sxs-lookup"><span data-stu-id="fcda8-524">Apply Azure Container Instance SDK 2017-10-01</span></span>
    - <span data-ttu-id="fcda8-525">支持容器 run-to-completion</span><span class="sxs-lookup"><span data-stu-id="fcda8-525">Support container run-to-completion</span></span>
    - <span data-ttu-id="fcda8-526">支持 Azure 文件卷装载</span><span class="sxs-lookup"><span data-stu-id="fcda8-526">Support Azure File volume mount</span></span>
    - <span data-ttu-id="fcda8-527">支持为公共 IP 打开多个端口</span><span class="sxs-lookup"><span data-stu-id="fcda8-527">Support opening multiple ports for public IP</span></span>
* <span data-ttu-id="fcda8-528">ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="fcda8-528">ContainerRegistry</span></span>
  - <span data-ttu-id="fcda8-529">用于异地复制和 Webhook 的新 cmdlet</span><span class="sxs-lookup"><span data-stu-id="fcda8-529">New cmdlets for geo-replication and webhooks</span></span>
    - <span data-ttu-id="fcda8-530">Get/New/Remove-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="fcda8-530">Get/New/Remove-AzureRmContainerRegistryReplication</span></span>
    - <span data-ttu-id="fcda8-531">Get/New/Remove/Test/Update-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="fcda8-531">Get/New/Remove/Test/Update-AzureRmContainerRegistryWebhook</span></span>
* <span data-ttu-id="fcda8-532">数据工厂</span><span class="sxs-lookup"><span data-stu-id="fcda8-532">DataFactories</span></span>
    - <span data-ttu-id="fcda8-533">凭据加密功能现在适用于启用了“远程访问”的操作（通过网络的操作）和禁用了“远程访问”的操作（本地计算机操作）。</span><span class="sxs-lookup"><span data-stu-id="fcda8-533">Credential encryption functionality now works with both "Remote Access" enabled (Over Network) and "Remote Access" disabled (Local Machine).</span></span>
* <span data-ttu-id="fcda8-534">DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="fcda8-534">DataFactoryV2</span></span>
  - <span data-ttu-id="fcda8-535">添加了两个新的 cmdlet：Update-AzureRmDataFactoryV2 和 Stop-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="fcda8-535">Added two new cmdlets: Update-AzureRmDataFactoryV2 and Stop-AzureRmDataFactoryV2PipelineRun</span></span>
* <span data-ttu-id="fcda8-536">DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="fcda8-536">DataLakeAnalytics</span></span>
  - <span data-ttu-id="fcda8-537">向 Submit-AzureRmDataLakeAnalyticsJob 添加了名为 ScriptParameter 的参数</span><span class="sxs-lookup"><span data-stu-id="fcda8-537">Added a parameter called ScriptParameter to Submit-AzureRmDataLakeAnalyticsJob</span></span>
    - <span data-ttu-id="fcda8-538">可以对 Submit-AzureRmDataLakeAnalyticsJob 使用 Get-Help 来查找有关 ScriptParameter 的详细信息</span><span class="sxs-lookup"><span data-stu-id="fcda8-538">Detailed information about ScriptParameter can be found using Get-Help on Submit-AzureRmDataLakeAnalyticsJob</span></span>
  - <span data-ttu-id="fcda8-539">已将 New-AzureRmDataLakeAnalyticsAccount 的参数 MaxDegreeOfParallelism 更改为 MaxAnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="fcda8-539">For New-AzureRmDataLakeAnalyticsAccount, changed the parameter MaxDegreeOfParallelism to MaxAnalyticsUnits</span></span>
    - <span data-ttu-id="fcda8-540">为参数 MaxAnalyticsUnits 添加了别名 MaxDegreeOfParallelism</span><span class="sxs-lookup"><span data-stu-id="fcda8-540">Added an alias for the parameter MaxAnalyticsUnits: MaxDegreeOfParallelism</span></span>
  - <span data-ttu-id="fcda8-541">已将 New-AzureRmDataLakeAnalyticsComputePolicy 的参数 MaxDegreeOfParallelismPerJob 更改为 MaxAnalyticsUnitsPerJob</span><span class="sxs-lookup"><span data-stu-id="fcda8-541">For New-AzureRmDataLakeAnalyticsComputePolicy, changed the parameter MaxDegreeOfParallelismPerJob to MaxAnalyticsUnitsPerJob</span></span>
    - <span data-ttu-id="fcda8-542">为参数 MaxAnalyticsUnitsPerJob 添加了别名 MaxDegreeOfParallelismPerJob</span><span class="sxs-lookup"><span data-stu-id="fcda8-542">Added an alias for the parameter MaxAnalyticsUnitsPerJob: MaxDegreeOfParallelismPerJob</span></span>
  - <span data-ttu-id="fcda8-543">已将 Set-AzureRmDataLakeAnalyticsAccount 的参数 MaxDegreeOfParallelism 更改为 MaxAnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="fcda8-543">For Set-AzureRmDataLakeAnalyticsAccount, changed the parameter MaxDegreeOfParallelism to MaxAnalyticsUnits</span></span>
    - <span data-ttu-id="fcda8-544">为参数 MaxAnalyticsUnits 添加了别名 MaxDegreeOfParallelism</span><span class="sxs-lookup"><span data-stu-id="fcda8-544">Added an alias for the parameter MaxAnalyticsUnits: MaxDegreeOfParallelism</span></span>
  - <span data-ttu-id="fcda8-545">已将 Submit-AzureRmDataLakeAnalyticsJob 的参数 DegreeOfParallelism 更改为 AnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="fcda8-545">For Submit-AzureRmDataLakeAnalyticsJob, changed the parameter DegreeOfParallelism to AnalyticsUnits</span></span>
    - <span data-ttu-id="fcda8-546">为参数 AnalyticsUnits 添加了别名 DegreeOfParallelism</span><span class="sxs-lookup"><span data-stu-id="fcda8-546">Added an alias for the parameter AnalyticsUnits: DegreeOfParallelism</span></span>
  - <span data-ttu-id="fcda8-547">已将 Update-AzureRmDataLakeAnalyticsComputePolicy 的参数 MaxDegreeOfParallelismPerJob 更改为 MaxAnalyticsUnitsPerJob</span><span class="sxs-lookup"><span data-stu-id="fcda8-547">For Update-AzureRmDataLakeAnalyticsComputePolicy, changed the parameter MaxDegreeOfParallelismPerJob to MaxAnalyticsUnitsPerJob</span></span>
    - <span data-ttu-id="fcda8-548">为参数 MaxAnalyticsUnitsPerJob 添加了别名 MaxDegreeOfParallelismPerJob</span><span class="sxs-lookup"><span data-stu-id="fcda8-548">Added an alias for the parameter MaxAnalyticsUnitsPerJob: MaxDegreeOfParallelismPerJob</span></span>
* <span data-ttu-id="fcda8-549">MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="fcda8-549">MachineLearningCompute</span></span>
  - <span data-ttu-id="fcda8-550">添加 Set-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="fcda8-550">Add Set-AzureRmMlOpCluster</span></span>
    - <span data-ttu-id="fcda8-551">更新群集的代理计数或 SSL 配置</span><span class="sxs-lookup"><span data-stu-id="fcda8-551">Update a cluster's agent count or SSL configuration</span></span>
  - <span data-ttu-id="fcda8-552">业务流程协调程序属性为可选</span><span class="sxs-lookup"><span data-stu-id="fcda8-552">Orchestrator properties are optional</span></span>
    - <span data-ttu-id="fcda8-553">此服务会创建服务主体（如果未提供），因此业务流程协调程序属性现在为可选</span><span class="sxs-lookup"><span data-stu-id="fcda8-553">The service will create a service principal if not provided, so the orchestrator properties are now optional</span></span>
* <span data-ttu-id="fcda8-554">PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="fcda8-554">PowerBIEmbedded</span></span>
  - <span data-ttu-id="fcda8-555">添加对 Power BI Embedded 容量 cmdlet 的支持</span><span class="sxs-lookup"><span data-stu-id="fcda8-555">Add support for Power BI Embedded Capacity cmdlets</span></span>
  - <span data-ttu-id="fcda8-556">全新 Cmdlet Get-AzureRmPowerBIEmbeddedCapacity - 获取 PowerBI Embedded 容量的详细信息。</span><span class="sxs-lookup"><span data-stu-id="fcda8-556">New Cmdlet Get-AzureRmPowerBIEmbeddedCapacity - Gets the details of a PowerBI Embedded Capacity.</span></span>
  - <span data-ttu-id="fcda8-557">全新 Cmdlet New-AzureRmPowerBIEmbeddedCapacity - 创建新的 PowerBI Embedded 容量</span><span class="sxs-lookup"><span data-stu-id="fcda8-557">New Cmdlet New-AzureRmPowerBIEmbeddedCapacity - Creates a new PowerBI Embedded Capacity</span></span>
  - <span data-ttu-id="fcda8-558">全新 Cmdlet Remove-AzureRmPowerBIEmbeddedCapacity - 删除 PowerBI Embedded 容量的实例</span><span class="sxs-lookup"><span data-stu-id="fcda8-558">New Cmdlet Remove-AzureRmPowerBIEmbeddedCapacity - Deletes an instance of PowerBI Embedded Capacity</span></span>
  - <span data-ttu-id="fcda8-559">全新 Cmdlet Resume-AzureRmPowerBIEmbeddedCapacity - 恢复 PowerBI Embedded 容量的实例</span><span class="sxs-lookup"><span data-stu-id="fcda8-559">New Cmdlet Resume-AzureRmPowerBIEmbeddedCapacity - Resumes an instance of PowerBI Embedded Capacity</span></span>
  - <span data-ttu-id="fcda8-560">全新 Cmdlet Suspend-AzureRmPowerBIEmbeddedCapacity - 暂停 PowerBI Embedded 容量的实例</span><span class="sxs-lookup"><span data-stu-id="fcda8-560">New Cmdlet Suspend-AzureRmPowerBIEmbeddedCapacity - Suspends an instance of PowerBI Embedded Capacity</span></span>
  - <span data-ttu-id="fcda8-561">全新 Cmdlet Test-AzureRmPowerBIEmbeddedCapacity - 测试 PowerBI Embedded 容量的实例是否存在</span><span class="sxs-lookup"><span data-stu-id="fcda8-561">New Cmdlet Test-AzureRmPowerBIEmbeddedCapacity - Tests the existence of an instance of PowerBI Embedded Capacity</span></span>
  - <span data-ttu-id="fcda8-562">全新 Cmdlet Update-AzureRmPowerBIEmbeddedCapacity - 修改 PowerBI Embedded 容量的实例</span><span class="sxs-lookup"><span data-stu-id="fcda8-562">New Cmdlet Update-AzureRmPowerBIEmbeddedCapacity - Modifies an instance of PowerBI Embedded Capacity</span></span>
* <span data-ttu-id="fcda8-563">配置文件</span><span class="sxs-lookup"><span data-stu-id="fcda8-563">Profile</span></span>
  - <span data-ttu-id="fcda8-564">将 USGovernmentActiveDirectoryEndpoint 更新到了 https://login.microsoftonline.us/</span><span class="sxs-lookup"><span data-stu-id="fcda8-564">Updated USGovernmentActiveDirectoryEndpoint to https://login.microsoftonline.us/</span></span>
    - <span data-ttu-id="fcda8-565">有关 Azure 政府版终结点映射的详细信息，请参阅下文：https://docs.microsoft.com/en-us/azure/azure-government/documentation-government-developer-guide#endpoint-mapping</span><span class="sxs-lookup"><span data-stu-id="fcda8-565">For more information about the Azure Government endpoint mappings, please see the following: https://docs.microsoft.com/en-us/azure/azure-government/documentation-government-developer-guide#endpoint-mapping</span></span>
    - <span data-ttu-id="fcda8-566">添加了对 cmdlet 的 -AsJob 支持，允许所选 cmdlet 在后台执行并返回可跟踪和控制进度的作业</span><span class="sxs-lookup"><span data-stu-id="fcda8-566">Added -AsJob support for cmdlets, enabling selected cmdlets to execute in the background and return a job to track and control progress</span></span>
    - <span data-ttu-id="fcda8-567">向 Get-AzureRmSubscription cmdlet 添加了 -AsJob 参数</span><span class="sxs-lookup"><span data-stu-id="fcda8-567">Added -AsJob parameter to Get-AzureRmSubscription cmdlet</span></span>
* <span data-ttu-id="fcda8-568">RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="fcda8-568">RecoveryServices.Backup</span></span>
  - <span data-ttu-id="fcda8-569">修复了 Bug - Get-AzureRmRecoveryServicesBackupItem 应该为容器名称筛选器执行不区分大小写的比较。</span><span class="sxs-lookup"><span data-stu-id="fcda8-569">Fixed bug - Get-AzureRmRecoveryServicesBackupItem should do case insensitive comparison for container name filter.</span></span>
  - <span data-ttu-id="fcda8-570">修复了 Bug - AzureVmItem 现在有一个可显示上次进行备份操作的时间的属性 - LastBackupTime.</span><span class="sxs-lookup"><span data-stu-id="fcda8-570">Fixed bug - AzureVmItem now has a property that shows the last time a backup operation has happened - LastBackupTime.</span></span>
* <span data-ttu-id="fcda8-571">资源</span><span class="sxs-lookup"><span data-stu-id="fcda8-571">Resources</span></span>
  - <span data-ttu-id="fcda8-572">修复了 Get-AzureRMRoleAssignment 所进行的分配没有为自定义角色提供 roledefiniton 名称的问题</span><span class="sxs-lookup"><span data-stu-id="fcda8-572">Fixed issue where Get-AzureRMRoleAssignment would result in a assignments without roledefiniton name for custom roles</span></span>
    - <span data-ttu-id="fcda8-573">用户现在可以对具有 roledefinition 名称的分配使用 Get-AzureRMRoleAssignment，不管角色类型如何</span><span class="sxs-lookup"><span data-stu-id="fcda8-573">Users can now use Get-AzureRMRoleAssignment with assignments having roledefinition names irrespective of the type of role</span></span>
  - <span data-ttu-id="fcda8-574">修复了在 assignablescopes 中存在新作用域时使用 Set-AzureRMRoleRoleDefinition 引发“找不到 RD”错误的问题</span><span class="sxs-lookup"><span data-stu-id="fcda8-574">Fixed issue where Set-AzureRMRoleRoleDefinition used to throw RD not found error when there was a new scope in assignablescopes</span></span>
    - <span data-ttu-id="fcda8-575">用户现在可以将 Set-AzureRMRoleRoleDefinition 与包括新作用域在内的可分配作用域配合使用，不管作用域的位置如何</span><span class="sxs-lookup"><span data-stu-id="fcda8-575">Users can now use Set-AzureRMRoleRoleDefinition with assignable scopes including new scopes irrespective of the position of the scope</span></span>
  - <span data-ttu-id="fcda8-576">允许作用域以“/”结尾</span><span class="sxs-lookup"><span data-stu-id="fcda8-576">Allow scopes to end with "/"</span></span>
    - <span data-ttu-id="fcda8-577">用户现在可以使用作用域以“/”结尾的 RoleDefinition 和 RoleAssignment cmdlet，与 API 和 CLI 保持一致</span><span class="sxs-lookup"><span data-stu-id="fcda8-577">Users can now use RoleDefinition and RoleAssignment commandlets with scopes ending with "/" ,consistent with API and CLI</span></span>
  - <span data-ttu-id="fcda8-578">允许用户使用委派标志创建 RoleAssignment</span><span class="sxs-lookup"><span data-stu-id="fcda8-578">Allow users to create RoleAssignment using delegation flag</span></span>
    - <span data-ttu-id="fcda8-579">用户现在可以使用 New-AzureRMRoleAssignment，其中的一个选项是添加委派标志</span><span class="sxs-lookup"><span data-stu-id="fcda8-579">Users can now use New-AzureRMRoleAssignment with an option of adding the delegation flag</span></span>
  - <span data-ttu-id="fcda8-580">修复了可接受作用域参数的 RoleAssignment get 的问题</span><span class="sxs-lookup"><span data-stu-id="fcda8-580">Fix RoleAssignment get to respect the scope parameter</span></span>
  - <span data-ttu-id="fcda8-581">在 New-AzureRmRoleAssignment cmdlet 中添加了 ServicePrincipalName 的别名</span><span class="sxs-lookup"><span data-stu-id="fcda8-581">Add an alias for ServicePrincipalName in the New-AzureRmRoleAssignment Commandlet</span></span>
    - <span data-ttu-id="fcda8-582">在使用 New-AzureRmRoleAssignment cmdlet 时，用户现在可以使用 ApplicationId 而非 ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="fcda8-582">Users can now use the ApplicationId instead of the ServicePrincipalName when using the New-AzureRmRoleAssignment commandlet</span></span>
* <span data-ttu-id="fcda8-583">SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="fcda8-583">SiteRecovery</span></span>
  - <span data-ttu-id="fcda8-584">在此模块中添加了针对所有 cmdlet 的弃用警告，为下一次发布重大更改做准备。</span><span class="sxs-lookup"><span data-stu-id="fcda8-584">Add deprecation warnings for all cmdlets in this module in preparation for the next breaking change release.</span></span>
    - <span data-ttu-id="fcda8-585">请参阅即将发布的重大更改指南，详细了解如何从 AzureRM 迁移 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fcda8-585">Please see the upcoming breaking changes guide for more information on how to migrate your cmdlets from AzureRM.</span></span>
* <span data-ttu-id="fcda8-586">Sql</span><span class="sxs-lookup"><span data-stu-id="fcda8-586">Sql</span></span>
  - <span data-ttu-id="fcda8-587">添加了使用 Set-AzureRmSqlDatabase 重命名数据库的功能</span><span class="sxs-lookup"><span data-stu-id="fcda8-587">Added ability to rename database using Set-AzureRmSqlDatabase</span></span>
  - <span data-ttu-id="fcda8-588">修复了问题 https://github.com/Azure/azure-powershell/issues/4974</span><span class="sxs-lookup"><span data-stu-id="fcda8-588">Fixed issue https://github.com/Azure/azure-powershell/issues/4974</span></span>
    - <span data-ttu-id="fcda8-589">为审核 cmdlet 提供无效的 AUDIT_CHANGED_GROUP 值时，不再引发错误。此项将在即将发布的版本中删除。</span><span class="sxs-lookup"><span data-stu-id="fcda8-589">Providing invalid AUDIT_CHANGED_GROUP value for auditing cmdlets no longer throws an error and will be removed in an upcoming release.</span></span>
  - <span data-ttu-id="fcda8-590">修复了问题 https://github.com/Azure/azure-powershell/issues/5046</span><span class="sxs-lookup"><span data-stu-id="fcda8-590">Fixed issue https://github.com/Azure/azure-powershell/issues/5046</span></span>
    - <span data-ttu-id="fcda8-591">不再忽略审核 cmdlet 中的 AuditAction 参数</span><span class="sxs-lookup"><span data-stu-id="fcda8-591">AuditAction parameter in auditing cmdlets is no longer being ignored</span></span>
  - <span data-ttu-id="fcda8-592">修复了提供的 StorageKeyType 为“Secondary”时审核 cmdlet 中存在的问题</span><span class="sxs-lookup"><span data-stu-id="fcda8-592">Fixed an issue in Auditing cmdlets when 'Secondary' StorageKeyType is provided</span></span>
    - <span data-ttu-id="fcda8-593">以前在设置 Blob 审核时，如果为 StorageKeyType 参数提供的值为“Secondary”，会使用主存储帐户密钥而非辅助密钥。</span><span class="sxs-lookup"><span data-stu-id="fcda8-593">When setting blob auditing, the primary storage account key was used instead of the secondary key when providing 'Secondary' value for StorageKeyType parameter.</span></span>
  - <span data-ttu-id="fcda8-594">更改 Set-AzureRmSqlServerTransparentDataEncryptionProtector 中确认消息的措辞</span><span class="sxs-lookup"><span data-stu-id="fcda8-594">Changing the wording for confirmation message from Set-AzureRmSqlServerTransparentDataEncryptionProtector</span></span>
* <span data-ttu-id="fcda8-595">Azure (RDFE)</span><span class="sxs-lookup"><span data-stu-id="fcda8-595">Azure (RDFE)</span></span>
    - <span data-ttu-id="fcda8-596">删除了所有 RemoteApp cmdlet</span><span class="sxs-lookup"><span data-stu-id="fcda8-596">Removed all RemoteApp Cmdles</span></span>
* <span data-ttu-id="fcda8-597">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="fcda8-597">Azure.Storage</span></span>
    - <span data-ttu-id="fcda8-598">升级到 Azure 存储客户端库 8.6.0 和 Azure 存储 DataMovement 库 0.6.5</span><span class="sxs-lookup"><span data-stu-id="fcda8-598">Upgrade to Azure Storage Client Library 8.6.0 and Azure Storage DataMovement Library 0.6.5</span></span>

## <a name="20171110-version-501"></a><span data-ttu-id="fcda8-599">2017.11.10 版本 5.0.1</span><span class="sxs-lookup"><span data-stu-id="fcda8-599">2017.11.10 Version 5.0.1</span></span>
* <span data-ttu-id="fcda8-600">修复了在以下模块中执行时会导致某些 cmdlet 失败的程序集加载问题：</span><span class="sxs-lookup"><span data-stu-id="fcda8-600">Fixed assembly loading issue that caused some cmdlets to fail when executing in the following modules:</span></span>
  - <span data-ttu-id="fcda8-601">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="fcda8-601">AzureRM.ApiManagement</span></span>
  - <span data-ttu-id="fcda8-602">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="fcda8-602">AzureRM.Backup</span></span>
  - <span data-ttu-id="fcda8-603">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="fcda8-603">AzureRM.Batch</span></span>
  - <span data-ttu-id="fcda8-604">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="fcda8-604">AzureRM.Compute</span></span>
  - <span data-ttu-id="fcda8-605">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="fcda8-605">AzureRM.DataFactories</span></span>
  - <span data-ttu-id="fcda8-606">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="fcda8-606">AzureRM.HDInsight</span></span>
  - <span data-ttu-id="fcda8-607">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="fcda8-607">AzureRM.KeyVault</span></span>
  - <span data-ttu-id="fcda8-608">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fcda8-608">AzureRM.RecoveryServices</span></span>
  - <span data-ttu-id="fcda8-609">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="fcda8-609">AzureRM.RecoveryServices.Backup</span></span>
  - <span data-ttu-id="fcda8-610">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="fcda8-610">AzureRM.RecoveryServices.SiteRecovery</span></span>
  - <span data-ttu-id="fcda8-611">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="fcda8-611">AzureRM.RedisCache</span></span>
  - <span data-ttu-id="fcda8-612">AzureRM.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="fcda8-612">AzureRM.SiteRecovery</span></span>
  - <span data-ttu-id="fcda8-613">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="fcda8-613">AzureRM.Sql</span></span>
  - <span data-ttu-id="fcda8-614">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="fcda8-614">AzureRM.Storage</span></span>
  - <span data-ttu-id="fcda8-615">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="fcda8-615">AzureRM.StreamAnalytics</span></span>

## <a name="2017118---version-500"></a><span data-ttu-id="fcda8-616">2017.11.8 - 版本 5.0.0</span><span class="sxs-lookup"><span data-stu-id="fcda8-616">2017.11.8 - Version 5.0.0</span></span>
* <span data-ttu-id="fcda8-617">注意：这是一个有重大更改的版本。</span><span class="sxs-lookup"><span data-stu-id="fcda8-617">NOTE: This is a breaking change release.</span></span> <span data-ttu-id="fcda8-618">有关引入的重大更改的完整列表，请参阅迁移指南 (https://aka.ms/azps-migration-guide)。</span><span class="sxs-lookup"><span data-stu-id="fcda8-618">Please see the migration guide (https://aka.ms/azps-migration-guide) for a full list of introduced breaking changes.</span></span>
* <span data-ttu-id="fcda8-619">AzureRM 中的所有 cmdlet 现在支持联机帮助</span><span class="sxs-lookup"><span data-stu-id="fcda8-619">All cmdlets in AzureRM now support online help</span></span>
  - <span data-ttu-id="fcda8-620">结合 -Online 参数运行 Get-Help 可在默认 Internet 浏览器中打开联机帮助</span><span class="sxs-lookup"><span data-stu-id="fcda8-620">Run Get-Help with the -Online parameter to open the online help in your default Internet browser</span></span>
* <span data-ttu-id="fcda8-621">AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="fcda8-621">AnalysisServices</span></span>
  * <span data-ttu-id="fcda8-622">修复了 Synchronize-AzureAsInstance 命令，现在它可以配合新的 AsAzure REST API 进行同步</span><span class="sxs-lookup"><span data-stu-id="fcda8-622">Fixed Synchronize-AzureAsInstance command to work with new AsAzure REST API for sync</span></span>
* <span data-ttu-id="fcda8-623">ApiManagement</span><span class="sxs-lookup"><span data-stu-id="fcda8-623">ApiManagement</span></span>
  * <span data-ttu-id="fcda8-624">有关此版本中对 ApiManagement 所做的重大更改，参阅迁移指南</span><span class="sxs-lookup"><span data-stu-id="fcda8-624">Please see the migration guide for breaking changes made to ApiManagement this release</span></span>
  * <span data-ttu-id="fcda8-625">更新了 Cmdlet Get-AzureRmApiManagementUser 以修复问题 https://github.com/Azure/azure-powershell/issues/4510</span><span class="sxs-lookup"><span data-stu-id="fcda8-625">Updated Cmdlet Get-AzureRmApiManagementUser to fix issue https://github.com/Azure/azure-powershell/issues/4510</span></span>
  * <span data-ttu-id="fcda8-626">更新了 Cmdlet New-AzureRmApiManagementApi 以创建包含空路径的 API https://github.com/Azure/azure-powershell/issues/4069</span><span class="sxs-lookup"><span data-stu-id="fcda8-626">Updated Cmdlet New-AzureRmApiManagementApi to create Api with Empty Path https://github.com/Azure/azure-powershell/issues/4069</span></span>
* <span data-ttu-id="fcda8-627">ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="fcda8-627">ApplicationInsights</span></span>
  * <span data-ttu-id="fcda8-628">添加用于获取/创建/删除 Applicaiton Insights 资源的命令</span><span class="sxs-lookup"><span data-stu-id="fcda8-628">Add commands to get/create/remove applicaiton insights resource</span></span>
    - <span data-ttu-id="fcda8-629">Get-AzureRmApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="fcda8-629">Get-AzureRmApplicationInsights</span></span>
    - <span data-ttu-id="fcda8-630">New-AzureRmApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="fcda8-630">New-AzureRmApplicationInsights</span></span>
    - <span data-ttu-id="fcda8-631">Remove-AzureRmApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="fcda8-631">Remove-AzureRmApplicationInsights</span></span>
  * <span data-ttu-id="fcda8-632">添加用于获取/更新 Applicaiton Insights 资源定价/每日上限的命令</span><span class="sxs-lookup"><span data-stu-id="fcda8-632">Add commands to get/update pricing/daily cap of applicaiton insights resource</span></span>
    - <span data-ttu-id="fcda8-633">Get-AzureRmApplicationInsights -IncludeDailyCap</span><span class="sxs-lookup"><span data-stu-id="fcda8-633">Get-AzureRmApplicationInsights -IncludeDailyCap</span></span>
    - <span data-ttu-id="fcda8-634">Set-AzureRmApplicationInsightsPricingPlan</span><span class="sxs-lookup"><span data-stu-id="fcda8-634">Set-AzureRmApplicationInsightsPricingPlan</span></span>
    - <span data-ttu-id="fcda8-635">Set-AzureRmApplicationInsightsDailyCap</span><span class="sxs-lookup"><span data-stu-id="fcda8-635">Set-AzureRmApplicationInsightsDailyCap</span></span>
  * <span data-ttu-id="fcda8-636">添加用于获取/创建/更新/删除 Applicaiton Insights 资源连续导出的命令</span><span class="sxs-lookup"><span data-stu-id="fcda8-636">Add commands to get/create/update/remove continuous export of applicaiton insights resource</span></span>
    - <span data-ttu-id="fcda8-637">Get-AzureRmApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="fcda8-637">Get-AzureRmApplicationInsightsContinuousExport</span></span>
    - <span data-ttu-id="fcda8-638">Set-AzureRmApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="fcda8-638">Set-AzureRmApplicationInsightsContinuousExport</span></span>
    - <span data-ttu-id="fcda8-639">New-AzureRmApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="fcda8-639">New-AzureRmApplicationInsightsContinuousExport</span></span>
    - <span data-ttu-id="fcda8-640">Remove-AzureRmApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="fcda8-640">Remove-AzureRmApplicationInsightsContinuousExport</span></span>
  * <span data-ttu-id="fcda8-641">添加用于获取/创建/删除 Applicaiton Insights 资源 API 密钥的命令</span><span class="sxs-lookup"><span data-stu-id="fcda8-641">Add commands to get/create/remove api keys of applicaiton insights resoruce</span></span>
    - <span data-ttu-id="fcda8-642">Get-AzureRmApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="fcda8-642">Get-AzureRmApplicationInsightsApiKey</span></span>
    - <span data-ttu-id="fcda8-643">New-AzureRmApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="fcda8-643">New-AzureRmApplicationInsightsApiKey</span></span>
    - <span data-ttu-id="fcda8-644">Remove-AzureRmApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="fcda8-644">Remove-AzureRmApplicationInsightsApiKey</span></span>
* <span data-ttu-id="fcda8-645">AzureBatch</span><span class="sxs-lookup"><span data-stu-id="fcda8-645">AzureBatch</span></span>
  * <span data-ttu-id="fcda8-646">为 `New-AzureRmBatchAccount` 添加了新参数。</span><span class="sxs-lookup"><span data-stu-id="fcda8-646">Added new parameters to `New-AzureRmBatchAccount`.</span></span>
    - <span data-ttu-id="fcda8-647">`PoolAllocationMode`：用于在 Batch 帐户中创建池的分配模式。</span><span class="sxs-lookup"><span data-stu-id="fcda8-647">`PoolAllocationMode`: The allocation mode to use for creating pools in the Batch account.</span></span> <span data-ttu-id="fcda8-648">若要创建一个可在用户订阅中分配池节点的 Batch 帐户，请将此参数设置为 `UserSubscription`。</span><span class="sxs-lookup"><span data-stu-id="fcda8-648">To create a Batch account which allocates pool nodes in the user's subscription, set this to `UserSubscription`.</span></span>
    - <span data-ttu-id="fcda8-649">`KeyVaultId`：与 Batch 帐户关联的 Azure Key Vault 的资源 ID。</span><span class="sxs-lookup"><span data-stu-id="fcda8-649">`KeyVaultId`: The resource ID of the Azure key vault associated with the Batch account.</span></span>
    - <span data-ttu-id="fcda8-650">`KeyVaultUrl`：与 Batch 帐户关联的 Azure Key Vault 的 URL。</span><span class="sxs-lookup"><span data-stu-id="fcda8-650">`KeyVaultUrl`: The URL of the Azure key vault associated with the Batch account.</span></span>
  * <span data-ttu-id="fcda8-651">更新了 `New-AzureBatchTask` 的参数。</span><span class="sxs-lookup"><span data-stu-id="fcda8-651">Updated parameters to `New-AzureBatchTask`.</span></span>
    - <span data-ttu-id="fcda8-652">删除了 `RunElevated` 开关。</span><span class="sxs-lookup"><span data-stu-id="fcda8-652">Removed the `RunElevated` switch.</span></span> <span data-ttu-id="fcda8-653">已添加 `UserIdentity` 参数来取代 `RunElevated`，可按如下所示，通过构造 `PSUserIdentity` 来实现等效的行为：</span><span class="sxs-lookup"><span data-stu-id="fcda8-653">The `UserIdentity` parameter has been added to replace `RunElevated`, and the equivalent behavior can be achieved by constructing a `PSUserIdentity` as shown below:</span></span>
      - <span data-ttu-id="fcda8-654">$autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")</span><span class="sxs-lookup"><span data-stu-id="fcda8-654">$autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")</span></span>
      - <span data-ttu-id="fcda8-655">$userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser</span><span class="sxs-lookup"><span data-stu-id="fcda8-655">$userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser</span></span>
    - <span data-ttu-id="fcda8-656">添加了 `AuthenticationTokenSettings` 参数。</span><span class="sxs-lookup"><span data-stu-id="fcda8-656">Added the `AuthenticationTokenSettings` parameter.</span></span> <span data-ttu-id="fcda8-657">使用此参数可以请求 Batch 服务向运行的任务提供身份验证令牌，从而无需向该任务传递 Batch 帐户密钥来向 Batch 服务发出请求。</span><span class="sxs-lookup"><span data-stu-id="fcda8-657">This parameter allows you to request the Batch service provide an authentication token to the task when it runs, avoiding the need to pass Batch account keys to the task in order to issue requests to the Batch service.</span></span>
    - <span data-ttu-id="fcda8-658">添加了 `ContainerSettings` 参数。</span><span class="sxs-lookup"><span data-stu-id="fcda8-658">Added the `ContainerSettings` parameter.</span></span>
      - <span data-ttu-id="fcda8-659">使用此参数可以请求 Batch 服务在容器内部运行任务。</span><span class="sxs-lookup"><span data-stu-id="fcda8-659">This parameter allows you to request the Batch service run the task inside a container.</span></span>
    - <span data-ttu-id="fcda8-660">添加了 `OutputFiles` 参数。</span><span class="sxs-lookup"><span data-stu-id="fcda8-660">Added the `OutputFiles` parameter.</span></span>
      - <span data-ttu-id="fcda8-661">使用此参数可以配置任务，以便在完成任务之后将文件上传到 Azure 存储。</span><span class="sxs-lookup"><span data-stu-id="fcda8-661">This parameter allows you to configure the task to upload files to Azure Storage after it has finished.</span></span>
  * <span data-ttu-id="fcda8-662">更新了 `New-AzureBatchPool` 的参数。</span><span class="sxs-lookup"><span data-stu-id="fcda8-662">Updated parameters to `New-AzureBatchPool`.</span></span>
    - <span data-ttu-id="fcda8-663">添加了 `UserAccounts` 参数。</span><span class="sxs-lookup"><span data-stu-id="fcda8-663">Added the `UserAccounts` parameter.</span></span>
      - <span data-ttu-id="fcda8-664">此参数定义在池中每个节点上创建的用户帐户。</span><span class="sxs-lookup"><span data-stu-id="fcda8-664">This parameter defines user accounts created on each node in the pool.</span></span>
    - <span data-ttu-id="fcda8-665">添加了 `TargetLowPriorityComputeNodes`，并已将 `TargetDedicated` 重命名为 `TargetDedicatedComputeNodes`。</span><span class="sxs-lookup"><span data-stu-id="fcda8-665">Added `TargetLowPriorityComputeNodes` and renamed `TargetDedicated` to `TargetDedicatedComputeNodes`.</span></span>
      - <span data-ttu-id="fcda8-666">为 `TargetDedicatedComputeNodes` 参数创建了 `TargetDedicated` 别名。</span><span class="sxs-lookup"><span data-stu-id="fcda8-666">A `TargetDedicated` alias was created for the `TargetDedicatedComputeNodes` parameter.</span></span>
    - <span data-ttu-id="fcda8-667">添加了 `NetworkConfiguration` 参数。</span><span class="sxs-lookup"><span data-stu-id="fcda8-667">Added the `NetworkConfiguration` parameter.</span></span>
      - <span data-ttu-id="fcda8-668">使用此参数可以配置池的网络设置。</span><span class="sxs-lookup"><span data-stu-id="fcda8-668">This parameter allows you to configure the pools network settings.</span></span>
  * <span data-ttu-id="fcda8-669">更新了 `New-AzureBatchCertificate` 的参数。</span><span class="sxs-lookup"><span data-stu-id="fcda8-669">Updated parameters to `New-AzureBatchCertificate`.</span></span>
    - <span data-ttu-id="fcda8-670">`Password` 参数现在是 `SecureString`。</span><span class="sxs-lookup"><span data-stu-id="fcda8-670">The `Password` parameter is now a `SecureString`.</span></span>
  * <span data-ttu-id="fcda8-671">更新了 `New-AzureBatchComputeNodeUser` 的参数。</span><span class="sxs-lookup"><span data-stu-id="fcda8-671">Updated parameters to `New-AzureBatchComputeNodeUser`.</span></span>
    - <span data-ttu-id="fcda8-672">`Password` 参数现在是 `SecureString`。</span><span class="sxs-lookup"><span data-stu-id="fcda8-672">The `Password` parameter is now a `SecureString`.</span></span>
  * <span data-ttu-id="fcda8-673">更新了 `Set-AzureBatchComputeNodeUser` 的参数。</span><span class="sxs-lookup"><span data-stu-id="fcda8-673">Updated parameters to `Set-AzureBatchComputeNodeUser`.</span></span>
    - <span data-ttu-id="fcda8-674">`Password` 参数现在是 `SecureString`。</span><span class="sxs-lookup"><span data-stu-id="fcda8-674">The `Password` parameter is now a `SecureString`.</span></span>
  * <span data-ttu-id="fcda8-675">已将 `Get-AzureBatchNodeFile`、`Get-AzureBatchNodeFileContent` 和 `Remove-AzureBatchNodeFile` 的 `Name` 参数重命名为 `Path`。</span><span class="sxs-lookup"><span data-stu-id="fcda8-675">Renamed the `Name` parameter to `Path` on `Get-AzureBatchNodeFile`, `Get-AzureBatchNodeFileContent`, and `Remove-AzureBatchNodeFile`.</span></span>
    - <span data-ttu-id="fcda8-676">为 `Path` 参数创建了 `Name` 别名。</span><span class="sxs-lookup"><span data-stu-id="fcda8-676">A `Name` alias was created for the `Path` parameter.</span></span>
  * <span data-ttu-id="fcda8-677">对象更改</span><span class="sxs-lookup"><span data-stu-id="fcda8-677">Changes to objects</span></span>
    - <span data-ttu-id="fcda8-678">有关完整列表，参阅 Batch 更改日志</span><span class="sxs-lookup"><span data-stu-id="fcda8-678">Please see the Batch change log for the full list</span></span>
  * <span data-ttu-id="fcda8-679">添加了对基于 Azure Active Directory 的身份验证的支持。</span><span class="sxs-lookup"><span data-stu-id="fcda8-679">Added support for Azure Active Directory based authentication.</span></span>
    - <span data-ttu-id="fcda8-680">若要使用 Azure Active Directory 身份验证，请使用 `Get-AzureRmBatchAccount` cmdlet 检索 `BatchAccountContext` 对象，并将此 `BatchAccountContext` 提供给 Batch 服务 cmdlet 的 `-BatchContext` 参数。</span><span class="sxs-lookup"><span data-stu-id="fcda8-680">To use Azure Active Directory authentication, retrieve a `BatchAccountContext` object using the `Get-AzureRmBatchAccount` cmdlet, and supply this `BatchAccountContext` to the `-BatchContext` parameter of a Batch service cmdlet.</span></span> <span data-ttu-id="fcda8-681">采用 `PoolAllocationMode = UserSubscription` 设置的帐户必须使用 Azure Active Directory 身份验证。</span><span class="sxs-lookup"><span data-stu-id="fcda8-681">Azure Active Directory authentication is mandatory for accounts with `PoolAllocationMode = UserSubscription`.</span></span>
    - <span data-ttu-id="fcda8-682">对于现有帐户或使用 `PoolAllocationMode = BatchService` 创建的新帐户，可通过使用 `Get-AzureRmBatchAccoutKeys` cmdlet 检索 `BatchAccountContext` 对象，来继续使用共享密钥身份验证。</span><span class="sxs-lookup"><span data-stu-id="fcda8-682">For existing accounts or for new accounts created with `PoolAllocationMode = BatchService`, you may continue to use shared key authentication by retrieving a `BatchAccountContext` object using the `Get-AzureRmBatchAccoutKeys` cmdlet.</span></span>
* <span data-ttu-id="fcda8-683">计算</span><span class="sxs-lookup"><span data-stu-id="fcda8-683">Compute</span></span>
  * <span data-ttu-id="fcda8-684">Azure 磁盘加密扩展命令</span><span class="sxs-lookup"><span data-stu-id="fcda8-684">Azure Disk Encryption Extension Commands</span></span>
    - <span data-ttu-id="fcda8-685">“Set-AzureRmVmDiskEncryptionExtension”的新参数“-EncryptFormatAll”可以加密形式格式化数据磁盘</span><span class="sxs-lookup"><span data-stu-id="fcda8-685">New Parameter for 'Set-AzureRmVmDiskEncryptionExtension': '-EncryptFormatAll' encrypt formats data disks</span></span>
    - <span data-ttu-id="fcda8-686">“Set-AzureRmVmDiskEncryptionExtension”的新参数“-ExtensionPublisherName”和“-ExtensionType”可用于切换到扩展的其他版本</span><span class="sxs-lookup"><span data-stu-id="fcda8-686">New Parameters for 'Set-AzureRmVmDiskEncryptionExtension': '-ExtensionPublisherName' and '-ExtensionType' allow switching to other versions of the extension</span></span>
    - <span data-ttu-id="fcda8-687">“Disable-AzureRmVmDiskEncryption”的新参数“-ExtensionPublisherName”和“-ExtensionType”可用于切换到扩展的其他版本</span><span class="sxs-lookup"><span data-stu-id="fcda8-687">New Parameters for 'Disable-AzureRmVmDiskEncryption': '-ExtensionPublisherName' and '-ExtensionType' allow switching to other versions of the extension</span></span>
    - <span data-ttu-id="fcda8-688">“Get-AzureRmVmDiskEncryptionStatus”的新参数“-ExtensionPublisherName”和“-ExtensionType”可用于切换到扩展的其他版本</span><span class="sxs-lookup"><span data-stu-id="fcda8-688">New Parameters for 'Get-AzureRmVmDiskEncryptionStatus': '-ExtensionPublisherName' and '-ExtensionType' allow switching to other versions of the extension</span></span>
* <span data-ttu-id="fcda8-689">DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="fcda8-689">DataLakeAnalytics</span></span>
  * <span data-ttu-id="fcda8-690">有关此版本中对 DataLakeAnalytics 所做的重大更改，参阅迁移指南</span><span class="sxs-lookup"><span data-stu-id="fcda8-690">Please see the migration guide for breaking changes made to DataLakeAnalytics this release</span></span>
  * <span data-ttu-id="fcda8-691">更改了 Get-AzureRmDataLakeAnalyticsAccount 的两个 OutputType 中的一个</span><span class="sxs-lookup"><span data-stu-id="fcda8-691">Changed one of the two OutputTypes of Get-AzureRmDataLakeAnalyticsAccount</span></span>
    - <span data-ttu-id="fcda8-692">List\<DataLakeAnalyticsAccount> 已更改为 List\<PSDataLakeAnalyticsAccountBasic></span><span class="sxs-lookup"><span data-stu-id="fcda8-692">List\<DataLakeAnalyticsAccount> to List\<PSDataLakeAnalyticsAccountBasic></span></span>
    - <span data-ttu-id="fcda8-693">PSDataLakeAnalyticsAccountBasic 的属性是 DataLakeAnalyticsAccount 的属性的严格子集</span><span class="sxs-lookup"><span data-stu-id="fcda8-693">The properties of PSDataLakeAnalyticsAccountBasic is a strict subset of the properties of DataLakeAnalyticsAccount</span></span>
    - <span data-ttu-id="fcda8-694">DataLakeAnalyticsAccount 中的附加属性不会由服务返回。</span><span class="sxs-lookup"><span data-stu-id="fcda8-694">The additional properties that are in DataLakeAnalyticsAccount are not returned by the service.</span></span>  <span data-ttu-id="fcda8-695">因此，此项更改旨在准确反映这种情况。</span><span class="sxs-lookup"><span data-stu-id="fcda8-695">Therefore, this change is to reflect this accurately.</span></span> <span data-ttu-id="fcda8-696">这些附加属性仍在 PSDataLakeAnalyticsAccountBasic 中，但已标记为“已过时”。</span><span class="sxs-lookup"><span data-stu-id="fcda8-696">These additional properties are still in PSDataLakeAnalyticsAccountBasic, but they are tagged as Obsolete.</span></span>
  * <span data-ttu-id="fcda8-697">更改了 Get-AzureRmDataLakeAnalyticsJob 的两个 OutputType 中的一个</span><span class="sxs-lookup"><span data-stu-id="fcda8-697">Changed one of the two OutputTypes of Get-AzureRmDataLakeAnalyticsJob</span></span>
    - <span data-ttu-id="fcda8-698">List\<JobInformation> 已更改为 List\<PSJobInformationBasic></span><span class="sxs-lookup"><span data-stu-id="fcda8-698">List\<JobInformation> to List\<PSJobInformationBasic></span></span>
    - <span data-ttu-id="fcda8-699">PSJobInformationBasic 的属性是 JobInformation 的属性的严格子集</span><span class="sxs-lookup"><span data-stu-id="fcda8-699">The properties of PSJobInformationBasic is a strict subset of the properties of JobInformation</span></span>
    - <span data-ttu-id="fcda8-700">JobInformation 中的附加属性不会由服务返回。</span><span class="sxs-lookup"><span data-stu-id="fcda8-700">The additional properties that are in JobInformation are not returned by the service.</span></span>  <span data-ttu-id="fcda8-701">因此，此项更改旨在准确反映这种情况。</span><span class="sxs-lookup"><span data-stu-id="fcda8-701">Therefore, this change is to reflect this accurately.</span></span> <span data-ttu-id="fcda8-702">这些附加属性仍在 PSJobInformationBasic 中，但已标记为“已过时”。</span><span class="sxs-lookup"><span data-stu-id="fcda8-702">These additional properties are still in PSJobInformationBasic, but they are tagged as Obsolete.</span></span>
* <span data-ttu-id="fcda8-703">DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fcda8-703">DataLakeStore</span></span>
  * <span data-ttu-id="fcda8-704">有关此版本中对 DataLakeStore 所做的重大更改，参阅迁移指南</span><span class="sxs-lookup"><span data-stu-id="fcda8-704">Please see the migration guide for breaking changes made to DataLakeStore this release</span></span>
  * <span data-ttu-id="fcda8-705">更改了 Get-AzureRmDataLakeStoreAccount 的两个 OutputType 中的一个</span><span class="sxs-lookup"><span data-stu-id="fcda8-705">Changed one of the two OutputTypes of Get-AzureRmDataLakeStoreAccount</span></span>
    - <span data-ttu-id="fcda8-706">List\<PSDataLakeStoreAccount> 已更改为 List\<PSDataLakeStoreAccountBasic></span><span class="sxs-lookup"><span data-stu-id="fcda8-706">List\<PSDataLakeStoreAccount> to List\<PSDataLakeStoreAccountBasic></span></span>
    - <span data-ttu-id="fcda8-707">PSDataLakeStoreAccountBasic 的属性是 PSDataLakeStoreAccount 的属性的严格子集</span><span class="sxs-lookup"><span data-stu-id="fcda8-707">The properties of PSDataLakeStoreAccountBasic is a strict subset of the properties of PSDataLakeStoreAccount</span></span>
    - <span data-ttu-id="fcda8-708">PSDataLakeStoreAccount 中的附加属性不会由服务返回。</span><span class="sxs-lookup"><span data-stu-id="fcda8-708">The additional properties that are in PSDataLakeStoreAccount are not returned by the service.</span></span>  <span data-ttu-id="fcda8-709">因此，此项更改旨在准确反映这种情况。</span><span class="sxs-lookup"><span data-stu-id="fcda8-709">Therefore, this change is to reflect this accurately.</span></span> <span data-ttu-id="fcda8-710">这些附加属性仍在 PSDataLakeStoreAccountBasic 中，但已标记为“已过时”。</span><span class="sxs-lookup"><span data-stu-id="fcda8-710">These additional properties are still in PSDataLakeStoreAccountBasic, but they are tagged as Obsolete.</span></span>
* <span data-ttu-id="fcda8-711">Dns</span><span class="sxs-lookup"><span data-stu-id="fcda8-711">Dns</span></span>
  * <span data-ttu-id="fcda8-712">对 Azure DNS 中 CAA 记录类型的支持</span><span class="sxs-lookup"><span data-stu-id="fcda8-712">Support for CAA record types in Azure DNS</span></span>
    - <span data-ttu-id="fcda8-713">支持对 CAA 记录类型执行所有操作</span><span class="sxs-lookup"><span data-stu-id="fcda8-713">Supports all operations on CAA record type</span></span>
* <span data-ttu-id="fcda8-714">EventHub</span><span class="sxs-lookup"><span data-stu-id="fcda8-714">EventHub</span></span>
  * <span data-ttu-id="fcda8-715">有关此版本中对 EventHub 所做的重大更改，参阅迁移指南</span><span class="sxs-lookup"><span data-stu-id="fcda8-715">Please see the migration guide for breaking changes made to EventHub this release</span></span>
* <span data-ttu-id="fcda8-716">洞察力</span><span class="sxs-lookup"><span data-stu-id="fcda8-716">Insights</span></span>
  * <span data-ttu-id="fcda8-717">有关此版本中对 Insights 所做的重大更改，参阅迁移指南</span><span class="sxs-lookup"><span data-stu-id="fcda8-717">Please see the migration guide for breaking changes made to Insights this release</span></span>
* <span data-ttu-id="fcda8-718">网络</span><span class="sxs-lookup"><span data-stu-id="fcda8-718">Network</span></span>
  * <span data-ttu-id="fcda8-719">有关此版本中对 Network 所做的重大更改，参阅迁移指南</span><span class="sxs-lookup"><span data-stu-id="fcda8-719">Please see the migration guide for breaking changes made to Network this release</span></span>
  * <span data-ttu-id="fcda8-720">添加了 cmdlet 用于列出指定 Azure 区域的可用 Internet 服务提供商</span><span class="sxs-lookup"><span data-stu-id="fcda8-720">Added cmdlet to list available internet service providers for a specified Azure region</span></span>
    - <span data-ttu-id="fcda8-721">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="fcda8-721">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>
  * <span data-ttu-id="fcda8-722">添加了 cmdlet 用于获取 Internet 服务提供商从指定位置到 Azure 区域的相对延迟评分</span><span class="sxs-lookup"><span data-stu-id="fcda8-722">Added cmdlet to get the relative latency score for internet service providers from a specified location to Azure regions</span></span>
    - <span data-ttu-id="fcda8-723">Get-AzureRmNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="fcda8-723">Get-AzureRmNetworkWatcherReachabilityReport</span></span>
* <span data-ttu-id="fcda8-724">配置文件</span><span class="sxs-lookup"><span data-stu-id="fcda8-724">Profile</span></span>
  - <span data-ttu-id="fcda8-725">Set-AzureRmDefault</span><span class="sxs-lookup"><span data-stu-id="fcda8-725">Set-AzureRmDefault</span></span>
    - <span data-ttu-id="fcda8-726">使用此 cmdlet 可设置默认资源组。</span><span class="sxs-lookup"><span data-stu-id="fcda8-726">Use this cmdlet to set a default resource group.</span></span>  <span data-ttu-id="fcda8-727">因此，对于某些 cmdlet 可以选择性地使用 -ResourceGroup 参数；如果未指定资源组，将使用默认值</span><span class="sxs-lookup"><span data-stu-id="fcda8-727">This will make the -ResourceGroup parameter optional for some cmdlets, and will use the default when a resource group is not specified</span></span>
    - ```Set-AzureRmDefault -ResourceGroupName "ExampleResourceGroup"```
    - <span data-ttu-id="fcda8-728">如果订阅中存在指定的资源组，此资源组将设置为默认值。</span><span class="sxs-lookup"><span data-stu-id="fcda8-728">If resource group specified exists in the subscription, this resource group will be set to default.</span></span>  <span data-ttu-id="fcda8-729">否则，将创建资源组并将其设置为默认值。</span><span class="sxs-lookup"><span data-stu-id="fcda8-729">Otherwise, the resource group will be created and then set to default.</span></span>
  - <span data-ttu-id="fcda8-730">Get-AzureRmDefault</span><span class="sxs-lookup"><span data-stu-id="fcda8-730">Get-AzureRmDefault</span></span>
    - <span data-ttu-id="fcda8-731">使用此 cmdlet 可获取当前的默认资源组（和将来的其他默认资源组）。</span><span class="sxs-lookup"><span data-stu-id="fcda8-731">Use this cmdlet to get the current default resource group (and other defaults in the future).</span></span>
    - ```Get-AzureRmDefault -ResourceGroup```
  - <span data-ttu-id="fcda8-732">Clear-AzureRmDefault</span><span class="sxs-lookup"><span data-stu-id="fcda8-732">Clear-AzureRmDefault</span></span>
    - <span data-ttu-id="fcda8-733">使用此 cmdlet 可删除当前的默认资源组</span><span class="sxs-lookup"><span data-stu-id="fcda8-733">Use this cmdlet to remove the current default resource group</span></span>
    - ```Clear-AzureRmDefault -ResourceGroup```
  - <span data-ttu-id="fcda8-734">Add-AzureRmEnvironment 和 Set-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="fcda8-734">Add-AzureRmEnvironment and Set-AzureRmEnvironment</span></span>
    - <span data-ttu-id="fcda8-735">添加 BatchAudience 参数，以便指定在获取 Batch 服务的身份验证令牌时要使用的 Azure Batch Active Directory 受众。</span><span class="sxs-lookup"><span data-stu-id="fcda8-735">Add the BatchAudience parameter, which allows you to specify the Azure Batch Active Directory audience to use when acquiring authentication tokens for the Batch service.</span></span>
* <span data-ttu-id="fcda8-736">RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="fcda8-736">RecoveryServices.Backup</span></span>
  * <span data-ttu-id="fcda8-737">添加了 cmdlet 用于执行即时文件恢复。</span><span class="sxs-lookup"><span data-stu-id="fcda8-737">Added cmdlets to perform instant file recovery.</span></span>
    - <span data-ttu-id="fcda8-738">Get-AzureRmRecoveryServicesBackupRPMountScript</span><span class="sxs-lookup"><span data-stu-id="fcda8-738">Get-AzureRmRecoveryServicesBackupRPMountScript</span></span>
    - <span data-ttu-id="fcda8-739">Disable-AzureRmRecoveryServicesBackupRPMountScript</span><span class="sxs-lookup"><span data-stu-id="fcda8-739">Disable-AzureRmRecoveryServicesBackupRPMountScript</span></span>
  * <span data-ttu-id="fcda8-740">已 RecoveryServices.Backup SDK 版本更新到最新版</span><span class="sxs-lookup"><span data-stu-id="fcda8-740">Updated RecoveryServices.Backup SDK version to the latest</span></span>
  * <span data-ttu-id="fcda8-741">更新了 Azure VM 工作负荷的测试，以便测试运行所需的所有设置由测试本身完成。</span><span class="sxs-lookup"><span data-stu-id="fcda8-741">Updated tests for the Azure VM workload so that, all setups needed for test runs are done by the tests themselves.</span></span>
  * <span data-ttu-id="fcda8-742">修复 https://github.com/Azure/azure-powershell/issues/3164</span><span class="sxs-lookup"><span data-stu-id="fcda8-742">Fixes https://github.com/Azure/azure-powershell/issues/3164</span></span>
* <span data-ttu-id="fcda8-743">RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="fcda8-743">RecoveryServices.SiteRecovery</span></span>
  * <span data-ttu-id="fcda8-744">对 ASR VMware 到 Azure Site Recovery 的迁移所做的更改（cmdlet 目前支持企业到企业、企业到 Azure 以及 HyperV 到 Azure 的操作）</span><span class="sxs-lookup"><span data-stu-id="fcda8-744">Changes for ASR VMware to Azure Site Recovery (cmdlets are currently supporting operations for Enterprise to Enterprise, Enterprise to Azure, HyperV to Azure)</span></span>
    - <span data-ttu-id="fcda8-745">New-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="fcda8-745">New-AzureRmRecoveryServicesAsrPolicy</span></span>
    - <span data-ttu-id="fcda8-746">New-AzureRmRecoveryServicesAsrProtectedItem</span><span class="sxs-lookup"><span data-stu-id="fcda8-746">New-AzureRmRecoveryServicesAsrProtectedItem</span></span>
    - <span data-ttu-id="fcda8-747">Update-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="fcda8-747">Update-AzureRmRecoveryServicesAsrPolicy</span></span>
    - <span data-ttu-id="fcda8-748">Update-AzureRmRecoveryServicesAsrProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="fcda8-748">Update-AzureRmRecoveryServicesAsrProtectionDirection</span></span>
  * <span data-ttu-id="fcda8-749">添加了对基于 AAD 的保管库的支持</span><span class="sxs-lookup"><span data-stu-id="fcda8-749">Added support to AAD-based vault</span></span>
  * <span data-ttu-id="fcda8-750">添加了 cmdlet 用于管理 VCenter 资源</span><span class="sxs-lookup"><span data-stu-id="fcda8-750">Added cmdlets to manage VCenter resources</span></span>
    - <span data-ttu-id="fcda8-751">Get-AzureRmRecoveryServicesAsrVCenter</span><span class="sxs-lookup"><span data-stu-id="fcda8-751">Get-AzureRmRecoveryServicesAsrVCenter</span></span>
    - <span data-ttu-id="fcda8-752">New-AzureRmRecoveryServicesAsrVCenter</span><span class="sxs-lookup"><span data-stu-id="fcda8-752">New-AzureRmRecoveryServicesAsrVCenter</span></span>
    - <span data-ttu-id="fcda8-753">Remove-AzureRmRecoveryServicesAsrVCenter</span><span class="sxs-lookup"><span data-stu-id="fcda8-753">Remove-AzureRmRecoveryServicesAsrVCenter</span></span>
    - <span data-ttu-id="fcda8-754">Update-AzureRmRecoveryServicesAsrVCenter</span><span class="sxs-lookup"><span data-stu-id="fcda8-754">Update-AzureRmRecoveryServicesAsrVCenter</span></span>
  * <span data-ttu-id="fcda8-755">添加了其他 cmdlet</span><span class="sxs-lookup"><span data-stu-id="fcda8-755">Added other cmdlets</span></span>
    - <span data-ttu-id="fcda8-756">Get-AzureRmRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="fcda8-756">Get-AzureRmRecoveryServicesAsrAlertSetting</span></span>
    - <span data-ttu-id="fcda8-757">Get-AzureRmRecoveryServicesAsrEvent</span><span class="sxs-lookup"><span data-stu-id="fcda8-757">Get-AzureRmRecoveryServicesAsrEvent</span></span>
    - <span data-ttu-id="fcda8-758">New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="fcda8-758">New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
    - <span data-ttu-id="fcda8-759">Set-AzureRmRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="fcda8-759">Set-AzureRmRecoveryServicesAsrAlertSetting</span></span>
    - <span data-ttu-id="fcda8-760">Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob</span><span class="sxs-lookup"><span data-stu-id="fcda8-760">Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob</span></span>
    - <span data-ttu-id="fcda8-761">Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob</span><span class="sxs-lookup"><span data-stu-id="fcda8-761">Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob</span></span>
    - <span data-ttu-id="fcda8-762">Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob</span><span class="sxs-lookup"><span data-stu-id="fcda8-762">Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob</span></span>
    - <span data-ttu-id="fcda8-763">Update-AzureRmRecoveryServicesAsrMobilityService</span><span class="sxs-lookup"><span data-stu-id="fcda8-763">Update-AzureRmRecoveryServicesAsrMobilityService</span></span>
* <span data-ttu-id="fcda8-764">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="fcda8-764">ServiceBus</span></span>
  - <span data-ttu-id="fcda8-765">有关此版本中对 ServiceBus 所做的重大更改，参阅迁移指南</span><span class="sxs-lookup"><span data-stu-id="fcda8-765">Please see the migration guide for breaking changes made to ServiceBus this release</span></span>
* <span data-ttu-id="fcda8-766">Sql</span><span class="sxs-lookup"><span data-stu-id="fcda8-766">Sql</span></span>
  * <span data-ttu-id="fcda8-767">添加列出和取消对数据库执行的异步 updateslo 操作的支持</span><span class="sxs-lookup"><span data-stu-id="fcda8-767">Adding support for list and cancel the asynchronous updateslo operation on the database</span></span>
    - <span data-ttu-id="fcda8-768">更新现有的 cmdlet Get-AzureRmSqlDatabaseActivity 以返回 DB updateslo 操作状态。</span><span class="sxs-lookup"><span data-stu-id="fcda8-768">update existing cmdlet Get-AzureRmSqlDatabaseActivity to return DB updateslo operation status.</span></span>
    - <span data-ttu-id="fcda8-769">添加新的 cmdlet Stop-AzureRmSqlDatabaseActivity，以取消对数据库执行的 updateslo 异步操作。</span><span class="sxs-lookup"><span data-stu-id="fcda8-769">add new cmdlet Stop-AzureRmSqlDatabaseActivity for cancel the asynchronous updateslo operation on the database.</span></span>
  * <span data-ttu-id="fcda8-770">添加数据库和弹性池区域冗余的支持</span><span class="sxs-lookup"><span data-stu-id="fcda8-770">Adding support for Zone Redundancy for databases and elastic pools</span></span>
    - <span data-ttu-id="fcda8-771">添加 New-AzureRmSqlDatabase 的 ZoneRedundant 开关参数</span><span class="sxs-lookup"><span data-stu-id="fcda8-771">Adding ZoneRedundant switch parameter to New-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="fcda8-772">添加 Set-AzureRmSqlDatabase 的 ZoneRedundant 开关参数</span><span class="sxs-lookup"><span data-stu-id="fcda8-772">Adding ZoneRedundant switch parameter to Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="fcda8-773">添加 New-AzureRmSqlElasticPool 的 ZoneRedundant 开关参数</span><span class="sxs-lookup"><span data-stu-id="fcda8-773">Adding ZoneRedundant switch parameter to New-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="fcda8-774">添加 Set-AzureRmSqlElasticPool 的 ZoneRedundant 开关参数</span><span class="sxs-lookup"><span data-stu-id="fcda8-774">Adding ZoneRedundant switch parameter to Set-AzureRmSqlElasticPool</span></span>
  * <span data-ttu-id="fcda8-775">添加对服务器 DNS 别名的支持</span><span class="sxs-lookup"><span data-stu-id="fcda8-775">Adding support for Server DNS Aliases</span></span>
    - <span data-ttu-id="fcda8-776">添加 Get-AzureRmSqlServerDnsAlias cmdlet，用于根据服务器和别名获取服务器 DNS 别名，或 Azure SQL Server 的一系列服务器 DNS 别名。</span><span class="sxs-lookup"><span data-stu-id="fcda8-776">Adding Get-AzureRmSqlServerDnsAlias cmdlet which gets server dns aliases by server and alias name or a list of server dns aliases for an azure Sql Server.</span></span>
    - <span data-ttu-id="fcda8-777">添加 New-AzureRmSqlServerDnsAlias cmdlet，用于新建给定 Azure SQL Server 的服务器 DNS 别名</span><span class="sxs-lookup"><span data-stu-id="fcda8-777">Adding New-AzureRmSqlServerDnsAlias cmdlet which creates new server dns alias for a given Azure Sql server</span></span>
    - <span data-ttu-id="fcda8-778">添加 Set-AzurermSqlServerDnsAlias cmlet，用于更新服务器 DNS 别名所指向的 Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="fcda8-778">Adding Set-AzurermSqlServerDnsAlias cmlet which allows updating a Azure Sql Server to which server dns alias is pointing</span></span>
    - <span data-ttu-id="fcda8-779">添加 Remove-AzureRmSqlServerDnsAlias cmdlet，用于删除 Azure SQL Server 的服务器 DNS 别名</span><span class="sxs-lookup"><span data-stu-id="fcda8-779">Adding Remove-AzureRmSqlServerDnsAlias cmdlet which removes a server dns alias for a Azure Sql Server</span></span>
* <span data-ttu-id="fcda8-780">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="fcda8-780">Azure.Storage</span></span>
  * <span data-ttu-id="fcda8-781">升级到 Azure 存储客户端库 8.5.0 和 Azure 存储 DataMovement 库 0.6.3</span><span class="sxs-lookup"><span data-stu-id="fcda8-781">Upgrade to Azure Storage Client Library 8.5.0 and Azure Storage DataMovement Library 0.6.3</span></span>
  * <span data-ttu-id="fcda8-782">添加文件共享支持快照</span><span class="sxs-lookup"><span data-stu-id="fcda8-782">Add File Share Snapshot Support Feature</span></span>
    - <span data-ttu-id="fcda8-783">为 Get-AzureStorageShare 添加“SnapshotTime”参数</span><span class="sxs-lookup"><span data-stu-id="fcda8-783">Add 'SnapshotTime' parameter to Get-AzureStorageShare</span></span>
    - <span data-ttu-id="fcda8-784">为 Remove-AzureStorageShare 添加“IncludeAllSnapshot”参数</span><span class="sxs-lookup"><span data-stu-id="fcda8-784">Add 'IncludeAllSnapshot' parameter to Remove-AzureStorageShare</span></span>
