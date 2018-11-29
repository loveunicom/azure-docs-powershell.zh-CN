---
title: Azure PowerShell 更改日志 | Microsoft Docs
description: 下面提供了对 Azure PowerShell 最新版本所做更改的历史记录。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 2/20/2018
ms.openlocfilehash: 1a9d38cd60ba596c085e5ee9f8d815e238362b1f
ms.sourcegitcommit: 558436c824d9b59731aa9b963cdc8df4dea932e7
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/29/2018
ms.locfileid: "52586711"
---
# <a name="release-notes"></a><span data-ttu-id="2afac-103">发行说明</span><span class="sxs-lookup"><span data-stu-id="2afac-103">Release notes</span></span>

<span data-ttu-id="2afac-104">下面是此版本中对 Azure PowerShell 所做的更改列表。</span><span class="sxs-lookup"><span data-stu-id="2afac-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---

# <a name="azure-powershell-570"></a><span data-ttu-id="2afac-105">Azure PowerShell 5.7.0</span><span class="sxs-lookup"><span data-stu-id="2afac-105">Azure PowerShell 5.7.0</span></span>

<span data-ttu-id="2afac-106">Azure PowerShell 5.7.0 安装程序：[链接](https://github.com/Azure/azure-powershell/releases/download/v5.7.0-April2018/azure-powershell.5.7.0.msi)</span><span class="sxs-lookup"><span data-stu-id="2afac-106">Azure PowerShell 5.7.0 Installer: [link](https://github.com/Azure/azure-powershell/releases/download/v5.7.0-April2018/azure-powershell.5.7.0.msi)</span></span>

<span data-ttu-id="2afac-107">ARM Cmdlet 的库模块：[链接](https://www.powershellgallery.com/packages/AzureRM/5.7.0)</span><span class="sxs-lookup"><span data-stu-id="2afac-107">Gallery Module for ARM Cmdlets: [link](https://www.powershellgallery.com/packages/AzureRM/5.7.0)</span></span>

<span data-ttu-id="2afac-108">若要从 PowerShell 库安装 `AzureRM`，请运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="2afac-108">To install `AzureRM` from the PowerShell Gallery, run the following command:</span></span>

```powershell-interactive
Install-Module -Name AzureRM -Repository PSGallery -Force
```

<span data-ttu-id="2afac-109">若要从旧版 `AzureRM` 更新，请运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="2afac-109">To update from an older version of `AzureRM`, run the following command:</span></span>

```powershell-interactive
Update-Module -Name AzureRM
```

## <a name="changes-since-last-release"></a><span data-ttu-id="2afac-110">自上次发布以来的更改</span><span class="sxs-lookup"><span data-stu-id="2afac-110">Changes Since Last Release</span></span>

#### <a name="general"></a><span data-ttu-id="2afac-111">常规</span><span class="sxs-lookup"><span data-stu-id="2afac-111">General</span></span>
* <span data-ttu-id="2afac-112">已更新到最新版本的 Azure ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="2afac-112">Updated to the latest version of the Azure ClientRuntime</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="2afac-113">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="2afac-113">Azure.Storage</span></span>
* <span data-ttu-id="2afac-114">解决了已启用 FIPS 策略的计算机上发生上传 Blob 和上传文件 cmdlet 失败的问题</span><span class="sxs-lookup"><span data-stu-id="2afac-114">Fix the issue that upload Blob and upload File cmdlets fail on FIPS policy enabled machines</span></span>
    - <span data-ttu-id="2afac-115">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="2afac-115">Set-AzureStorageBlobContent</span></span>
    - <span data-ttu-id="2afac-116">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="2afac-116">Set-AzureStorageFileContent</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="2afac-117">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="2afac-117">AzureRM.Billing</span></span>
* <span data-ttu-id="2afac-118">新 Cmdlet Get-AzureRmEnrollmentAccount</span><span class="sxs-lookup"><span data-stu-id="2afac-118">New Cmdlet Get-AzureRmEnrollmentAccount</span></span>
  - <span data-ttu-id="2afac-119">用于检索登记帐户的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="2afac-119">cmdlet to retrieve enrollment accounts</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="2afac-120">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2afac-120">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="2afac-121">与认知服务管理 SDK 版本 4.0.0 集成。</span><span class="sxs-lookup"><span data-stu-id="2afac-121">Integrate with Cognitive Services Management SDK version 4.0.0.</span></span>
* <span data-ttu-id="2afac-122">添加了 Get-AzureRmCognitiveServicesAccountUsage 操作。</span><span class="sxs-lookup"><span data-stu-id="2afac-122">Add Get-AzureRmCognitiveServicesAccountUsage operation.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="2afac-123">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="2afac-123">AzureRM.Compute</span></span>
* <span data-ttu-id="2afac-124">`Get-AzureRmVmssDiskEncryptionStatus` 支持数据磁盘级别的加密状态</span><span class="sxs-lookup"><span data-stu-id="2afac-124">`Get-AzureRmVmssDiskEncryptionStatus` supports encryption status at data disk level</span></span>
* <span data-ttu-id="2afac-125">`Get-AzureRmVmssVmDiskEncryptionStatus` 支持数据磁盘级别的加密状态</span><span class="sxs-lookup"><span data-stu-id="2afac-125">`Get-AzureRmVmssVmDiskEncryptionStatus` supports encryption status at data disk level</span></span>
* <span data-ttu-id="2afac-126">区域复原能力的更新</span><span class="sxs-lookup"><span data-stu-id="2afac-126">Update for Zone Resilient</span></span>
* <span data-ttu-id="2afac-127">“New-AzureRmVm”和“New-AzureRmVmss”（简单参数集）支持可用性区域。</span><span class="sxs-lookup"><span data-stu-id="2afac-127">'New-AzureRmVm' and 'New-AzureRmVmss' (simple parameter set) support availability zones.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="2afac-128">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="2afac-128">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="2afac-129">分解了对 Commands.Resources.Rest 和 ARM/存储 SDK 的依赖。</span><span class="sxs-lookup"><span data-stu-id="2afac-129">Decouple reliance on Commands.Resources.Rest and ARM/Storage SDKs.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="2afac-130">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2afac-130">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="2afac-131">添加了调试功能</span><span class="sxs-lookup"><span data-stu-id="2afac-131">Add debug functionality</span></span>
* <span data-ttu-id="2afac-132">已将 ADLS 数据平面 SDK 的版本更新为 1.1.2</span><span class="sxs-lookup"><span data-stu-id="2afac-132">Update the version of the ADLS dataplane SDK to 1.1.2</span></span>
* <span data-ttu-id="2afac-133">Export-AzureRmDataLakeStoreItem - 已弃用参数 PerFileThreadCount 和 ConcurrentFileCount，并引入了参数 Concurrency</span><span class="sxs-lookup"><span data-stu-id="2afac-133">Export-AzureRmDataLakeStoreItem - Deprecated parameters PerFileThreadCount, ConcurrentFileCount and introduced parameter Concurrency</span></span>
* <span data-ttu-id="2afac-134">Import-AzureRMDataLakeStoreItem - 已弃用参数 PerFileThreadCount 和 ConcurrentFileCount，并引入了参数 Concurrency</span><span class="sxs-lookup"><span data-stu-id="2afac-134">Import-AzureRMDataLakeStoreItem - Deprecated parametersPerFileThreadCount, ConcurrentFileCount and introduced parameter Concurrency</span></span>
* <span data-ttu-id="2afac-135">Get-AzureRMDataLakeStoreItemContent - 修复了大于 4MB 的内容的尾部行为</span><span class="sxs-lookup"><span data-stu-id="2afac-135">Get-AzureRMDataLakeStoreItemContent - Fixed the tail behavior for contents greater than 4MB</span></span>
* <span data-ttu-id="2afac-136">Set-AzureRMDataLakeStoreItemExpiry - 引入了新参数集 SetRelativeExpiry 用于设置相对过期时间</span><span class="sxs-lookup"><span data-stu-id="2afac-136">Set-AzureRMDataLakeStoreItemExpiry - Introduced new parameter set SetRelativeExpiry for setting relative expiration time</span></span>
* <span data-ttu-id="2afac-137">Remove-AzureRmDataLakeStoreItem - 已弃用参数 Clean。</span><span class="sxs-lookup"><span data-stu-id="2afac-137">Remove-AzureRmDataLakeStoreItem - Deprecated parameter Clean.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="2afac-138">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="2afac-138">AzureRM.EventHub</span></span>
* <span data-ttu-id="2afac-139">修复了 New-AzureRmEventHubGeoDRConfiguration 中的 AlternameName</span><span class="sxs-lookup"><span data-stu-id="2afac-139">Fixed AlternameName in New-AzureRmEventHubGeoDRConfiguration</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="2afac-140">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2afac-140">AzureRM.KeyVault</span></span>
* <span data-ttu-id="2afac-141">更新了 cmdlet 以包含管道场景</span><span class="sxs-lookup"><span data-stu-id="2afac-141">Updated cmdlets to include piping scenarios</span></span>
* <span data-ttu-id="2afac-142">由于有重大更改的版本即将发布，添加了弃用消息</span><span class="sxs-lookup"><span data-stu-id="2afac-142">Add deprecation messages for upcoming breaking change release</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="2afac-143">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="2afac-143">AzureRM.Network</span></span>
* <span data-ttu-id="2afac-144">修复了 Network cmdlet 的错误消息</span><span class="sxs-lookup"><span data-stu-id="2afac-144">Fix error message with Network cmdlets</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="2afac-145">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2afac-145">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="2afac-146">在 Rules 的 CorrelationFilter 中添加了“properties”，以支持 customproperties</span><span class="sxs-lookup"><span data-stu-id="2afac-146">Added 'properties' in CorrelationFilter of Rules to support customproperties</span></span>
* <span data-ttu-id="2afac-147">更新了 New-AzureRmServiceBusGeoDRConfiguration 帮助，并修复了 Rules cmdlet 的输出</span><span class="sxs-lookup"><span data-stu-id="2afac-147">updated New-AzureRmServiceBusGeoDRConfiguration help and fixed Rules cmdlet output</span></span>
* <span data-ttu-id="2afac-148">修复了 New-AzureRmServiceBusQueue 和 New-AzureRmServiceBusSubscription cmdlet 中的 auto-forward 属性</span><span class="sxs-lookup"><span data-stu-id="2afac-148">Fixed auto-forward properties in New-AzureRmServiceBusQueue and New-AzureRmServiceBusSubscription cmdlet</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="2afac-149">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="2afac-149">AzureRM.Sql</span></span>
* <span data-ttu-id="2afac-150">添加了新 cmdlet“Stop-AzureRmSqlElasticPoolActivity”，以支持取消对弹性池的异步操作</span><span class="sxs-lookup"><span data-stu-id="2afac-150">Add new cmdlet 'Stop-AzureRmSqlElasticPoolActivity' to support canceling the asynchronous operations on elastic pool</span></span>
* <span data-ttu-id="2afac-151">更新了 cmdlet Get-AzureRmSqlDatabaseActivity 和 Get-AzureRmSqlElasticPoolActivity 的响应，以便在响应中反映更多信息</span><span class="sxs-lookup"><span data-stu-id="2afac-151">Update the response for cmdlets Get-AzureRmSqlDatabaseActivity and Get-AzureRmSqlElasticPoolActivity to reflect more information in the response</span></span>

<span data-ttu-id="2afac-152">自上次发布以来的更改： https://github.com/Azure/azure-powershell/compare/v5.6.0-March2018...v5.7.0-April2018</span><span class="sxs-lookup"><span data-stu-id="2afac-152">Changes since last release: https://github.com/Azure/azure-powershell/compare/v5.6.0-March2018...v5.7.0-April2018</span></span>

## <a name="560---march-2018"></a><span data-ttu-id="2afac-153">5.6.0 - 2018 年 3 月</span><span class="sxs-lookup"><span data-stu-id="2afac-153">5.6.0 - March 2018</span></span>

#### <a name="general"></a><span data-ttu-id="2afac-154">常规</span><span class="sxs-lookup"><span data-stu-id="2afac-154">General</span></span>
* <span data-ttu-id="2afac-155">修复了 CloudShell 中的默认资源组的问题</span><span class="sxs-lookup"><span data-stu-id="2afac-155">Fix issue with Default Resource Group in CloudShell</span></span>
* <span data-ttu-id="2afac-156">修复了在模块导入过程中执行错误启动脚本的问题</span><span class="sxs-lookup"><span data-stu-id="2afac-156">Fix issue where incorrect startup scripts were being executed during module import</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="2afac-157">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="2afac-157">AzureRM.Profile</span></span>
* <span data-ttu-id="2afac-158">在不支持的方案中启用 MSI 身份验证</span><span class="sxs-lookup"><span data-stu-id="2afac-158">Enable MSI authentication in unsupported scenarios</span></span>
* <span data-ttu-id="2afac-159">添加对用户定义的托管服务标识的支持</span><span class="sxs-lookup"><span data-stu-id="2afac-159">Add support for user-defined Managed Service Identity</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="2afac-160">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="2afac-160">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="2afac-161">修复了在生成时清理脚本的问题</span><span class="sxs-lookup"><span data-stu-id="2afac-161">Fixed issue with cleaning up scripts in build</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="2afac-162">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="2afac-162">AzureRM.Cdn</span></span>
* <span data-ttu-id="2afac-163">修复了在生成时清理脚本的问题</span><span class="sxs-lookup"><span data-stu-id="2afac-163">Fixed issue with cleaning up scripts in build</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="2afac-164">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="2afac-164">AzureRM.Compute</span></span>
* <span data-ttu-id="2afac-165">“New-AzureRmVM”和“New-AzureRmVMSS”支持数据磁盘。</span><span class="sxs-lookup"><span data-stu-id="2afac-165">'New-AzureRmVM' and 'New-AzureRmVMSS' support data disks.</span></span>
* <span data-ttu-id="2afac-166">“New-AzureRmVM”和“New-AzureRmVMSS”支持按名称或按 ID 指定自定义映像。</span><span class="sxs-lookup"><span data-stu-id="2afac-166">'New-AzureRmVM' and 'New-AzureRmVMSS' support custom image by name or by id.</span></span>
* <span data-ttu-id="2afac-167">日志分析功能</span><span class="sxs-lookup"><span data-stu-id="2afac-167">Log analytic feature</span></span>
    - <span data-ttu-id="2afac-168">添加了“Export-AzureRmLogAnalyticRequestRateByInterval”cmdlet</span><span class="sxs-lookup"><span data-stu-id="2afac-168">Added 'Export-AzureRmLogAnalyticRequestRateByInterval' cmdlet</span></span>
    - <span data-ttu-id="2afac-169">添加了“Export-AzureRmLogAnalyticThrottledRequests”cmdlet</span><span class="sxs-lookup"><span data-stu-id="2afac-169">Added 'Export-AzureRmLogAnalyticThrottledRequests' cmdlet</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="2afac-170">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="2afac-170">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="2afac-171">修复了容器注册表和 azure 文件卷装载的参数集问题</span><span class="sxs-lookup"><span data-stu-id="2afac-171">Fix parameter sets issue for container registry and azure file volume mount</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="2afac-172">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="2afac-172">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="2afac-173">将 ADF.Net SDK 更新到了版本 0.6.0-preview，其中包含以下更改：</span><span class="sxs-lookup"><span data-stu-id="2afac-173">Updated the ADF .Net SDK to version 0.6.0-preview containing the following changes:</span></span>
    - <span data-ttu-id="2afac-174">添加了新的 AzureDatabricks LinkedService 和 DatabricksNotebook 活动</span><span class="sxs-lookup"><span data-stu-id="2afac-174">Added new AzureDatabricks LinkedService and DatabricksNotebook Activity</span></span>
    - <span data-ttu-id="2afac-175">在 HDInsightOnDemand LinkedService 中添加了 headNodeSize 和 dataNodeSize 属性</span><span class="sxs-lookup"><span data-stu-id="2afac-175">Added headNodeSize and dataNodeSize properties in HDInsightOnDemand LinkedService</span></span>
    - <span data-ttu-id="2afac-176">为 SalesforceMarketingCloud 添加了 LinkedService、Dataset、CopySource</span><span class="sxs-lookup"><span data-stu-id="2afac-176">Added LinkedService, Dataset, CopySource for SalesforceMarketingCloud</span></span>
    - <span data-ttu-id="2afac-177">在所有活动上添加了对 SecureOutput 的支持</span><span class="sxs-lookup"><span data-stu-id="2afac-177">Added support for SecureOutput on all activities</span></span>
    - <span data-ttu-id="2afac-178">在 ForEach 活动上添加了新的 BatchCount 属性，以控制要运行的并发活动数量</span><span class="sxs-lookup"><span data-stu-id="2afac-178">Added new BatchCount property on ForEach activity which control how many concurrent activities to run</span></span>
    - <span data-ttu-id="2afac-179">添加了新的 Filter 活动</span><span class="sxs-lookup"><span data-stu-id="2afac-179">Added new Filter Activity</span></span>
    - <span data-ttu-id="2afac-180">添加了链接服务参数支持</span><span class="sxs-lookup"><span data-stu-id="2afac-180">Added Linked Service Parameters support</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="2afac-181">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="2afac-181">AzureRM.Dns</span></span>
* <span data-ttu-id="2afac-182">对专用 DNS 区域的支持（公共预览版）</span><span class="sxs-lookup"><span data-stu-id="2afac-182">Support for Private DNS Zones (Public Preview)</span></span>
    - <span data-ttu-id="2afac-183">添加了创建仅对关联虚拟网络可见的 DNS 区域的功能</span><span class="sxs-lookup"><span data-stu-id="2afac-183">Adds ability to create DNS zones that are visible only to the associated virtual networks</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="2afac-184">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="2afac-184">AzureRM.Network</span></span>
* <span data-ttu-id="2afac-185">更新模型类型以便与 DNS cmdlet 兼容。</span><span class="sxs-lookup"><span data-stu-id="2afac-185">Updating model types for compatibility with DNS cmdlets.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="2afac-186">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="2afac-186">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="2afac-187">对 ASR Azure 到 Azure Site Recovery 的迁移所做的更改（cmdlet 目前支持企业到企业、企业到 Azure、HyperV 到 Azure 以及 VMware 到 Azure 的操作）</span><span class="sxs-lookup"><span data-stu-id="2afac-187">Changes for ASR Azure to Azure Site Recovery (cmdlets are currently supporting operations for Enterprise to Enterprise, Enterprise to Azure, HyperV to Azure,VMware to Azure)</span></span>
    - <span data-ttu-id="2afac-188">New-AzureRmRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="2afac-188">New-AzureRmRecoveryServicesAsrProtectionContainer</span></span>
    - <span data-ttu-id="2afac-189">New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="2afac-189">New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span></span>
    - <span data-ttu-id="2afac-190">Remove-AzureRmRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="2afac-190">Remove-AzureRmRecoveryServicesAsrProtectionContainer</span></span>
    - <span data-ttu-id="2afac-191">Update-AzureRmRecoveryServicesAsrProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="2afac-191">Update-AzureRmRecoveryServicesAsrProtectionDirection</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="2afac-192">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="2afac-192">AzureRM.Storage</span></span>
* <span data-ttu-id="2afac-193">在用于新建和设置存储帐户的 cmdlet（EnableEncryptionService 和 DisableEncryptionService）中废弃以下参数，因为静态加密在默认情况下处于启用状态，并且不能禁用。</span><span class="sxs-lookup"><span data-stu-id="2afac-193">Obsolete following parameters in new and set Storage Account cmdlets: EnableEncryptionService and DisableEncryptionService, since Encryption at Rest is enabled by default and can't be disabled.</span></span>
    - <span data-ttu-id="2afac-194">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2afac-194">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="2afac-195">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2afac-195">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="2afac-196">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="2afac-196">AzureRM.Websites</span></span>
* <span data-ttu-id="2afac-197">修复了 Remove-AzureRmWebAppSlot 的帮助</span><span class="sxs-lookup"><span data-stu-id="2afac-197">Fixed the help for Remove-AzureRmWebAppSlot</span></span>

## <a name="550---march-2018"></a><span data-ttu-id="2afac-198">5.5.0 - 2018 年 3 月</span><span class="sxs-lookup"><span data-stu-id="2afac-198">5.5.0 - March 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="2afac-199">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="2afac-199">AzureRM.Profile</span></span>
* <span data-ttu-id="2afac-200">修复了导入别名的问题</span><span class="sxs-lookup"><span data-stu-id="2afac-200">Fixed issue with importing aliases</span></span>
* <span data-ttu-id="2afac-201">将 Newtonsoft.Json 的 10.0.3 版随 6.0.8 版一起加载</span><span class="sxs-lookup"><span data-stu-id="2afac-201">Load version 10.0.3 of Newtonsoft.Json side-by-side with version 6.0.8</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="2afac-202">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="2afac-202">Azure.Storage</span></span>
* <span data-ttu-id="2afac-203">支持软删除功能</span><span class="sxs-lookup"><span data-stu-id="2afac-203">Support Soft-Delete feature</span></span>
    - <span data-ttu-id="2afac-204">Enable-AzureStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="2afac-204">Enable-AzureStorageDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="2afac-205">Disable-AzureStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="2afac-205">Disable-AzureStorageDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="2afac-206">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="2afac-206">Get-AzureStorageBlob</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="2afac-207">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="2afac-207">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="2afac-208">修复了导入别名的问题</span><span class="sxs-lookup"><span data-stu-id="2afac-208">Fixed issue with importing aliases</span></span>
* <span data-ttu-id="2afac-209">添加对防火墙和查询向外扩展功能的支持，以及对 2017-08-01 api 版本的支持。</span><span class="sxs-lookup"><span data-stu-id="2afac-209">Add support of firewall and query scaleout feature, as well as support of 2017-08-01 api version.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="2afac-210">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="2afac-210">AzureRM.Automation</span></span>
* <span data-ttu-id="2afac-211">修复了导入别名的问题</span><span class="sxs-lookup"><span data-stu-id="2afac-211">Fixed issue with importing aliases</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="2afac-212">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="2afac-212">AzureRM.Cdn</span></span>
* <span data-ttu-id="2afac-213">修复了导入别名的问题</span><span class="sxs-lookup"><span data-stu-id="2afac-213">Fixed issue with importing aliases</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="2afac-214">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2afac-214">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="2afac-215">更新 notice.txt 和通知消息。</span><span class="sxs-lookup"><span data-stu-id="2afac-215">Update notice.txt and notice message.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="2afac-216">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="2afac-216">AzureRM.Compute</span></span>
* <span data-ttu-id="2afac-217">'New-AzureRmVMSS' 以详细模式打印连接字符串。</span><span class="sxs-lookup"><span data-stu-id="2afac-217">'New-AzureRmVMSS' prints connection strings in verbose mode.</span></span>
* <span data-ttu-id="2afac-218">'New-AzureRmVmss' 支持公共 IP 地址、负载均衡规则、入站 NAT 规则。</span><span class="sxs-lookup"><span data-stu-id="2afac-218">'New-AzureRmVmss' supports public IP address, load balancing rules, inbound NAT rules.</span></span>
* <span data-ttu-id="2afac-219">WriteAccelerator 功能</span><span class="sxs-lookup"><span data-stu-id="2afac-219">WriteAccelerator feature</span></span>
    - <span data-ttu-id="2afac-220">将 WriteAccelerator 开关参数添加到了以下 cmdlet：Set-AzureRmVMOSDisk Set-AzureRmVMDataDisk Add-AzureRmVMDataDisk Add-AzureRmVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="2afac-220">Added WriteAccelerator switch parameter to the following cmdlets: Set-AzureRmVMOSDisk Set-AzureRmVMDataDisk Add-AzureRmVMDataDisk Add-AzureRmVmssDataDisk</span></span>
    - <span data-ttu-id="2afac-221">将 OsDiskWriteAccelerator 开关参数添加到了以下 cmdlet：     Set-AzureRmVmssStorageProfile。</span><span class="sxs-lookup"><span data-stu-id="2afac-221">Added OsDiskWriteAccelerator switch parameter to the following cmdlet:     Set-AzureRmVmssStorageProfile.</span></span>
    - <span data-ttu-id="2afac-222">将 OsDiskWriteAccelerator 布尔参数添加到了以下 cmdlet：     Update-AzureRmVM     Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2afac-222">Added OsDiskWriteAccelerator Boolean parameter to the following cmdlets:     Update-AzureRmVM     Update-AzureRmVmss</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="2afac-223">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="2afac-223">AzureRM.DataFactories</span></span>
* <span data-ttu-id="2afac-224">修复了导致某些加密操作没有有意义错误的凭据加密问题</span><span class="sxs-lookup"><span data-stu-id="2afac-224">Fix credential encryption issue that caused no meaningful error for some encryption operations</span></span>
* <span data-ttu-id="2afac-225">允许跨数据工厂共享集成运行时</span><span class="sxs-lookup"><span data-stu-id="2afac-225">Enable integration runtime to be shared across data factory</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="2afac-226">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="2afac-226">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="2afac-227">为 "Set-AzureRmDataFactoryV2IntegrationRuntime" cmd 添加了参数 "SetupScriptContainerSasUri" 和 "Edition" 以启用自定义安装和版本选择功能</span><span class="sxs-lookup"><span data-stu-id="2afac-227">Add parameter "SetupScriptContainerSasUri" and "Edition" for "Set-AzureRmDataFactoryV2IntegrationRuntime" cmd to enable custom setup and edition selection functionality</span></span>
* <span data-ttu-id="2afac-228">修复了导致某些加密操作没有有意义错误的凭据加密问题。</span><span class="sxs-lookup"><span data-stu-id="2afac-228">Fix credential encryption issue that caused no meaningful error for some encryption operations.</span></span>
* <span data-ttu-id="2afac-229">允许跨数据工厂共享集成运行时</span><span class="sxs-lookup"><span data-stu-id="2afac-229">Enable integration runtime to be shared across data factory</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="2afac-230">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="2afac-230">AzureRM.HDInsight</span></span>
* <span data-ttu-id="2afac-231">修复了导入别名的问题</span><span class="sxs-lookup"><span data-stu-id="2afac-231">Fixed issue with importing aliases</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="2afac-232">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2afac-232">AzureRM.KeyVault</span></span>
* <span data-ttu-id="2afac-233">修复了 Set-AzureRmKeyVaultAccessPolicy 的示例</span><span class="sxs-lookup"><span data-stu-id="2afac-233">Fixed example for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="2afac-234">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="2afac-234">AzureRM.Network</span></span>
* <span data-ttu-id="2afac-235">修复了导入别名的问题</span><span class="sxs-lookup"><span data-stu-id="2afac-235">Fixed issue with importing aliases</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="2afac-236">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2afac-236">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="2afac-237">修复了导入别名的问题</span><span class="sxs-lookup"><span data-stu-id="2afac-237">Fixed issue with importing aliases</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="2afac-238">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2afac-238">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="2afac-239">修复了导入别名的问题</span><span class="sxs-lookup"><span data-stu-id="2afac-239">Fixed issue with importing aliases</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="2afac-240">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="2afac-240">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="2afac-241">修复了导入别名的问题</span><span class="sxs-lookup"><span data-stu-id="2afac-241">Fixed issue with importing aliases</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="2afac-242">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="2afac-242">AzureRM.Resources</span></span>
* <span data-ttu-id="2afac-243">修复了导入别名的问题</span><span class="sxs-lookup"><span data-stu-id="2afac-243">Fixed issue with importing aliases</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="2afac-244">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2afac-244">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="2afac-245">为 Queue 添加了 EnableBatchedOperations 属性</span><span class="sxs-lookup"><span data-stu-id="2afac-245">Added EnableBatchedOperations property to Queue</span></span>
* <span data-ttu-id="2afac-246">为 Subscriptions 添加了 DeadLetteringOnFilterEvaluationExceptions 属性</span><span class="sxs-lookup"><span data-stu-id="2afac-246">Added DeadLetteringOnFilterEvaluationExceptions property to Subscriptions</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="2afac-247">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2afac-247">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="2afac-248">Service Fabric cmdlet 刷新</span><span class="sxs-lookup"><span data-stu-id="2afac-248">Service Fabric cmdlet refresh</span></span>
  - <span data-ttu-id="2afac-249">更新了 ARM 模板</span><span class="sxs-lookup"><span data-stu-id="2afac-249">Updated ARM templates</span></span>
  - <span data-ttu-id="2afac-250">失败的操作不再回滚</span><span class="sxs-lookup"><span data-stu-id="2afac-250">Failed operations no longer rollback</span></span>
  - <span data-ttu-id="2afac-251">Add-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="2afac-251">Add-AzureRmServiceFabricNodeType</span></span>
    - <span data-ttu-id="2afac-252">VM 默认为托管磁盘</span><span class="sxs-lookup"><span data-stu-id="2afac-252">VMs default to managed disks</span></span>
    - <span data-ttu-id="2afac-253">使用了现有 VMSS 子网</span><span class="sxs-lookup"><span data-stu-id="2afac-253">Existing VMSS subnet used</span></span>
    - <span data-ttu-id="2afac-254">所有操作都是幂等的</span><span class="sxs-lookup"><span data-stu-id="2afac-254">All operations are idempotent</span></span>
  - <span data-ttu-id="2afac-255">Remove-AzureRmServiceFabricNodeType 清除部分创建的 VMSS 和/或群集节点类型</span><span class="sxs-lookup"><span data-stu-id="2afac-255">Remove-AzureRmServiceFabricNodeType cleans up partially created VMSS and/or cluster node types</span></span>
  - <span data-ttu-id="2afac-256">修复了复杂属性类型的 PSCluster 对象输出</span><span class="sxs-lookup"><span data-stu-id="2afac-256">Fixed output of PSCluster object for complex property types</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="2afac-257">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="2afac-257">AzureRM.Sql</span></span>
* <span data-ttu-id="2afac-258">修复了导入别名的问题</span><span class="sxs-lookup"><span data-stu-id="2afac-258">Fixed issue with importing aliases</span></span>
* <span data-ttu-id="2afac-259">Get-AzureRmSqlServer、New-AzureRmSqlServer 和 Remove-AzureRmSqlServer 响应现在包括 FullyQualifiedDomainName 属性。</span><span class="sxs-lookup"><span data-stu-id="2afac-259">Get-AzureRmSqlServer, New-AzureRmSqlServer, and Remove-AzureRmSqlServer response now includes FullyQualifiedDomainName property.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="2afac-260">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="2afac-260">AzureRM.Websites</span></span>
* <span data-ttu-id="2afac-261">修复了导入别名的问题</span><span class="sxs-lookup"><span data-stu-id="2afac-261">Fixed issue with importing aliases</span></span>
* <span data-ttu-id="2afac-262">New-AzureRMWebApp - 添加了参数集以用于简化的 WebApp 创建，并提供本地 Git 存储库支持。</span><span class="sxs-lookup"><span data-stu-id="2afac-262">New-AzureRMWebApp - added parameter set for simplified WebApp creation, with local git repository support.</span></span>

## <a name="540---february-2018"></a><span data-ttu-id="2afac-263">5.4.0 - 2018 年 2 月</span><span class="sxs-lookup"><span data-stu-id="2afac-263">5.4.0 - February 2018</span></span>
#### <a name="azurermautomation"></a><span data-ttu-id="2afac-264">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="2afac-264">AzureRM.Automation</span></span>
* <span data-ttu-id="2afac-265">从 New-AzureRmAutomationModule 到 Import-AzureRmAutomationModule 添加了别名</span><span class="sxs-lookup"><span data-stu-id="2afac-265">Added alias from New-AzureRmAutomationModule to Import-AzureRmAutomationModule</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="2afac-266">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="2afac-266">AzureRM.Compute</span></span>
* <span data-ttu-id="2afac-267">解决某些 Get cmdlet 的 ErrorAction 问题。</span><span class="sxs-lookup"><span data-stu-id="2afac-267">Fix ErrorAction issue for some of Get cmdlets.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="2afac-268">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="2afac-268">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="2afac-269">应用 Azure 容器实例 SDK 2018-02-01</span><span class="sxs-lookup"><span data-stu-id="2afac-269">Apply Azure Container Instance SDK 2018-02-01</span></span>
    - <span data-ttu-id="2afac-270">支持 DNS 名称标签</span><span class="sxs-lookup"><span data-stu-id="2afac-270">Support DNS name label</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="2afac-271">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="2afac-271">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="2afac-272">修复了以前无法正常运行的所有 GET cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2afac-272">Fixed all of the GET cmdlets which previously weren't working.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="2afac-273">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="2afac-273">AzureRM.EventHub</span></span>
* <span data-ttu-id="2afac-274">修复 Get-AzureRmEventHubGeoDRConfiguration 帮助中的 bug</span><span class="sxs-lookup"><span data-stu-id="2afac-274">Fix bug in Get-AzureRmEventHubGeoDRConfiguration help</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="2afac-275">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="2afac-275">AzureRM.Network</span></span>
* <span data-ttu-id="2afac-276">添加了 cmdlet 以创建新的连接监视器</span><span class="sxs-lookup"><span data-stu-id="2afac-276">Added cmdlet to create a new connection monitor</span></span>
    - <span data-ttu-id="2afac-277">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2afac-277">New-AzureRmNetworkWatcherConnectionMonitor</span></span>
* <span data-ttu-id="2afac-278">添加了 cmdlet 以更新连接监视器</span><span class="sxs-lookup"><span data-stu-id="2afac-278">Added cmdlet to update a connection monitor</span></span>
    - <span data-ttu-id="2afac-279">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2afac-279">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>
* <span data-ttu-id="2afac-280">添加了 cmdlet 来获取连接监视器或连接监视器列表</span><span class="sxs-lookup"><span data-stu-id="2afac-280">Added cmdlet to get connection monitor or connection monitor list</span></span>
    - <span data-ttu-id="2afac-281">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2afac-281">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>
* <span data-ttu-id="2afac-282">添加了 cmdlet 以查询连接监视器</span><span class="sxs-lookup"><span data-stu-id="2afac-282">Added cmdlet to query connection monitor</span></span>
    - <span data-ttu-id="2afac-283">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="2afac-283">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>
* <span data-ttu-id="2afac-284">添加了 cmdlet 以启动连接监视器</span><span class="sxs-lookup"><span data-stu-id="2afac-284">Added cmdlet to start connection monitor</span></span>
    - <span data-ttu-id="2afac-285">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2afac-285">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>
* <span data-ttu-id="2afac-286">添加了 cmdlet 以停止连接监视器</span><span class="sxs-lookup"><span data-stu-id="2afac-286">Added cmdlet to stop connection monitor</span></span>
    - <span data-ttu-id="2afac-287">Stop-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2afac-287">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>
* <span data-ttu-id="2afac-288">添加了 cmdlet 以删除连接监视器</span><span class="sxs-lookup"><span data-stu-id="2afac-288">Added cmdlet to remove connection monitor</span></span>
    - <span data-ttu-id="2afac-289">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2afac-289">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>
* <span data-ttu-id="2afac-290">更新了 Set-AzureRmApplicationGatewayBackendAddressPool 文档以删除弃用的示例</span><span class="sxs-lookup"><span data-stu-id="2afac-290">Updated Set-AzureRmApplicationGatewayBackendAddressPool documentation to remove deprecated example</span></span>
* <span data-ttu-id="2afac-291">将 EnableHttp2 标志添加到了应用程序网关</span><span class="sxs-lookup"><span data-stu-id="2afac-291">Added EnableHttp2 flag to Application Gateway</span></span>
    - <span data-ttu-id="2afac-292">更新了 New-AzureRmApplicationGateway：添加了可选参数 -EnableHttp2</span><span class="sxs-lookup"><span data-stu-id="2afac-292">Updated New-AzureRmApplicationGateway: Added optional parameter -EnableHttp2</span></span>
* <span data-ttu-id="2afac-293">将 IpTags 添加到 PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="2afac-293">Add IpTags to PublicIpAddress</span></span>
    - <span data-ttu-id="2afac-294">更新了 New-AzureRmPublicIpAddress：添加了 IpTags</span><span class="sxs-lookup"><span data-stu-id="2afac-294">Updated New-AzureRmPublicIpAddress: Added IpTags</span></span>
    - <span data-ttu-id="2afac-295">用于添加 Iptag 的 New-AzureRmPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="2afac-295">New-AzureRmPublicIpTag to add Iptag</span></span>
* <span data-ttu-id="2afac-296">在 RouteTable 和 effectiveRoute 中添加 DisableBgpRoutePropagation 属性。</span><span class="sxs-lookup"><span data-stu-id="2afac-296">Add DisableBgpRoutePropagation property in RouteTable and effectiveRoute.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="2afac-297">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="2afac-297">AzureRM.Resources</span></span>
* <span data-ttu-id="2afac-298">Register-AzureRmProviderFeature：添加了文档中缺少的示例</span><span class="sxs-lookup"><span data-stu-id="2afac-298">Register-AzureRmProviderFeature: Added missing example in the docs</span></span>
* <span data-ttu-id="2afac-299">Register-AzureRmResourceProvider：添加了文档中缺少的示例</span><span class="sxs-lookup"><span data-stu-id="2afac-299">Register-AzureRmResourceProvider: Added missing example in the docs</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="2afac-300">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="2afac-300">AzureRM.Storage</span></span>
* <span data-ttu-id="2afac-301">在用于新建和设置存储帐户的 cmdlet（EnableEncryptionService 和 DisableEncryptionService）中废弃以下参数，因为静态加密在默认情况下处于启用状态，并且不能禁用。</span><span class="sxs-lookup"><span data-stu-id="2afac-301">Obsolete following parameters in new and set Storage Account cmdlets: EnableEncryptionService and DisableEncryptionService, since Encryption at Rest is enabled by default and can't be disabled.</span></span>
    - <span data-ttu-id="2afac-302">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2afac-302">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="2afac-303">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2afac-303">Set-AzureRmStorageAccount</span></span>


## <a name="530---february-2018"></a><span data-ttu-id="2afac-304">5.3.0 - 2018 年 2 月</span><span class="sxs-lookup"><span data-stu-id="2afac-304">5.3.0 - February 2018</span></span>
### <a name="azurermprofile"></a><span data-ttu-id="2afac-305">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="2afac-305">AzureRM.Profile</span></span>
* <span data-ttu-id="2afac-306">对 PowerShell 3 和 PowerShell 4 添加了弃用警告</span><span class="sxs-lookup"><span data-stu-id="2afac-306">Added deprecation warning for PowerShell 3 and 4</span></span>
* <span data-ttu-id="2afac-307">`Add-AzureRmAccount` 已重命名为 `Connect-AzureRmAccount`；为旧的 cmdlet 名称添加了别名，并将其他别名（`Login-AzAccount` 和 `Login-AzureRmAccount`）重定向到了新的 cmdlet 名称。</span><span class="sxs-lookup"><span data-stu-id="2afac-307">`Add-AzureRmAccount` has been renamed as `Connect-AzureRmAccount`; an alias has been added for the old cmdlet name, and other aliases (`Login-AzAccount` and `Login-AzureRmAccount`) have been redirected to the new cmdlet name.</span></span>
* <span data-ttu-id="2afac-308">`Remove-AzureRmAccount` 已重命名为 `Disconnect-AzureRmAccount`；为旧的 cmdlet 名称添加了别名，并将其他别名（`Logout-AzAccount` 和 `Logout-AzureRmAccount`）重定向到了新的 cmdlet 名称。</span><span class="sxs-lookup"><span data-stu-id="2afac-308">`Remove-AzureRmAccount` has been renamed as `Disconnect-AzureRmAccount`; an alias has been added for the old cmdlet name, and other aliases (`Logout-AzAccount` and `Logout-AzureRmAccount`) have been redirected to the new cmdlet name.</span></span>
* <span data-ttu-id="2afac-309">更正了资源字符串以使用 `Connect-AzureRmAccount` 而不是 `Login-AzureRmAccount`</span><span class="sxs-lookup"><span data-stu-id="2afac-309">Corrected Resource Strings to use `Connect-AzureRmAccount` instead of `Login-AzureRmAccount`</span></span>
* <span data-ttu-id="2afac-310">`Add-AzureRmEnvironment` 和 `Set-AzureRmEnvironment`</span><span class="sxs-lookup"><span data-stu-id="2afac-310">`Add-AzureRmEnvironment` and `Set-AzureRmEnvironment`</span></span>
  - <span data-ttu-id="2afac-311">添加了 `-AzureOperationalInsightsEndpoint` 和 `-AzureOperationalInsightsEndpointResourceId` 作为要用于 OperationalInsights 数据平面 RP 的参数。</span><span class="sxs-lookup"><span data-stu-id="2afac-311">Added `-AzureOperationalInsightsEndpoint` and `-AzureOperationalInsightsEndpointResourceId` as parameters for use with OperationalInsights data plane RP.</span></span>

### <a name="azurermanalysisservices"></a><span data-ttu-id="2afac-312">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="2afac-312">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="2afac-313">更正了 `Login-AzureRmAccount` 的用法以使用 `Connect-AzureRmAccount`</span><span class="sxs-lookup"><span data-stu-id="2afac-313">Corrected usage of `Login-AzureRmAccount` to use `Connect-AzureRmAccount`</span></span>

### <a name="azurermcompute"></a><span data-ttu-id="2afac-314">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="2afac-314">AzureRM.Compute</span></span>
* <span data-ttu-id="2afac-315">向 `New-AzureRmVM` 的简化参数集添加了 `-AvailabilitySetName` 参数。</span><span class="sxs-lookup"><span data-stu-id="2afac-315">Added `-AvailabilitySetName` parameter to the simplified parameterset of `New-AzureRmVM`.</span></span>
* <span data-ttu-id="2afac-316">更正了 `Login-AzureRmAccount` 的用法以使用 `Connect-AzureRmAccount`</span><span class="sxs-lookup"><span data-stu-id="2afac-316">Corrected usage of `Login-AzureRmAccount` to use `Connect-AzureRmAccount`</span></span>
* <span data-ttu-id="2afac-317">对 VM 和 VM 规模集的用户分配标识支持</span><span class="sxs-lookup"><span data-stu-id="2afac-317">User assigned identity support for VM and VM scale set</span></span>
    - <span data-ttu-id="2afac-318">将 `-IdentityType` 和 `-IdentityId` 参数添加到了 `New-AzureRmVMConfig`、`New-AzureRmVmssConfig`、`Update-AzureRmVM` 和 `Update-AzureRmVmss`</span><span class="sxs-lookup"><span data-stu-id="2afac-318">`-IdentityType` and `-IdentityId` parameters are added to `New-AzureRmVMConfig`, `New-AzureRmVmssConfig`, `Update-AzureRmVM` and `Update-AzureRmVmss`</span></span>
* <span data-ttu-id="2afac-319">为 `Add-AzureRmVmssNetworkInterfaceConfig` 添加了 `-EnableIPForwarding` 参数</span><span class="sxs-lookup"><span data-stu-id="2afac-319">Added `-EnableIPForwarding` parameter to `Add-AzureRmVmssNetworkInterfaceConfig`</span></span>
* <span data-ttu-id="2afac-320">为 `New-AzureRmVmssConfig` 添加了 `-Priority` 参数</span><span class="sxs-lookup"><span data-stu-id="2afac-320">Added `-Priority` parameter to `New-AzureRmVmssConfig`</span></span>

### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="2afac-321">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="2afac-321">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="2afac-322">更正了 `Login-AzureRmAccount` 的用法以使用 `Connect-AzureRmAccount`</span><span class="sxs-lookup"><span data-stu-id="2afac-322">Corrected usage of `Login-AzureRmAccount` to use `Connect-AzureRmAccount`</span></span>

### <a name="azurermdatalakestore"></a><span data-ttu-id="2afac-323">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2afac-323">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="2afac-324">更正了 `Login-AzureRmAccount` 的用法以使用 `Connect-AzureRmAccount`</span><span class="sxs-lookup"><span data-stu-id="2afac-324">Corrected usage of `Login-AzureRmAccount` to use `Connect-AzureRmAccount`</span></span>
* <span data-ttu-id="2afac-325">更正了未使用 `Login-AzureRmAccount` 登录便运行 `Test-AzureRmDataLakeStoreAccount` 时显示的此 cmdlet 的错误消息</span><span class="sxs-lookup"><span data-stu-id="2afac-325">Corrected the error message of `Test-AzureRmDataLakeStoreAccount` when running this cmdlet without having logged in with `Login-AzureRmAccount`</span></span>

### <a name="azurermeventgrid"></a><span data-ttu-id="2afac-326">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="2afac-326">AzureRM.EventGrid</span></span>
* <span data-ttu-id="2afac-327">已更新以使用 2018-01-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="2afac-327">Updated to use the 2018-01-01 API version.</span></span>

### <a name="azurermeventhub"></a><span data-ttu-id="2afac-328">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="2afac-328">AzureRM.EventHub</span></span>

* <span data-ttu-id="2afac-329">添加了以下新命令以便执行异地灾难恢复操作。</span><span class="sxs-lookup"><span data-stu-id="2afac-329">Added below new commands for Geo Disaster Recovery operations.</span></span>
  - <span data-ttu-id="2afac-330">创建新别名（灾难恢复配置）：</span><span class="sxs-lookup"><span data-stu-id="2afac-330">Creating a new Alias (Disaster Recovery configuration):</span></span>
    - `New-AzureRmEventHubGeoDRConfiguration`
  - <span data-ttu-id="2afac-331">检索别名（灾难恢复配置）：</span><span class="sxs-lookup"><span data-stu-id="2afac-331">Retrieve Alias (Disaster Recovery configuration) :</span></span>
    - `Get-AzureRmEventHubGeoDRConfiguration`
  - <span data-ttu-id="2afac-332">禁用灾难恢复，并停止从主命名空间向辅助命名空间复制更改</span><span class="sxs-lookup"><span data-stu-id="2afac-332">Disabling the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>
    - `Set-AzureRmEventHubGeoDRConfigurationBreakPair`
  - <span data-ttu-id="2afac-333">调用灾难恢复故障转移并将别名重新配置为指向辅助命名空间</span><span class="sxs-lookup"><span data-stu-id="2afac-333">Invoking Disaster Recovery failover and reconfigure the alias to point to the secondary namespace</span></span>
    - `Set-AzureRmEventHubGeoDRConfigurationFailOver`
  - <span data-ttu-id="2afac-334">删除别名（灾难恢复配置）</span><span class="sxs-lookup"><span data-stu-id="2afac-334">Deleting an Alias(Disaster Recovery configuration)</span></span>
    - `Remove-AzureRmEventHubGeoDRConfiguration`
* <span data-ttu-id="2afac-335">添加了以下新命令，用于检查命名空间名称和 GeoDr 配置名称 - 别名可用性。</span><span class="sxs-lookup"><span data-stu-id="2afac-335">Added below new commands for checking the Namespace Name and GeoDr Configuration Name - Alias availability.</span></span>
  - <span data-ttu-id="2afac-336">检查命名空间名称或别名（灾难恢复配置）名称的可用性：</span><span class="sxs-lookup"><span data-stu-id="2afac-336">Check the Availability of Namespace name or Alias(Disaster Recovery configuration) name:</span></span>
    - `Test-AzureRmEventHubName`

### <a name="azurerminsights"></a><span data-ttu-id="2afac-337">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="2afac-337">AzureRM.Insights</span></span>
* <span data-ttu-id="2afac-338">更正了 `Login-AzureRmAccount` 的用法以使用 `Connect-AzureRmAccount`</span><span class="sxs-lookup"><span data-stu-id="2afac-338">Corrected usage of `Login-AzureRmAccount` to use `Connect-AzureRmAccount`</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="2afac-339">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2afac-339">AzureRM.KeyVault</span></span>
* <span data-ttu-id="2afac-340">更正了 `Login-AzureRmAccount` 的用法以使用 `Connect-AzureRmAccount`</span><span class="sxs-lookup"><span data-stu-id="2afac-340">Corrected usage of `Login-AzureRmAccount` to use `Connect-AzureRmAccount`</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="2afac-341">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="2afac-341">AzureRM.Network</span></span>
* <span data-ttu-id="2afac-342">修复了覆盖消息“是否确实要覆盖资源”</span><span class="sxs-lookup"><span data-stu-id="2afac-342">Fix overwrite message 'Are you sure you want to overwriteresource'</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="2afac-343">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2afac-343">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="2afac-344">通过 `Invoke-AzureRmOperationalInsightsQuery` 添加了对 V2 API 查询的支持。</span><span class="sxs-lookup"><span data-stu-id="2afac-344">Added support for V2 API querying via `Invoke-AzureRmOperationalInsightsQuery`.</span></span> <span data-ttu-id="2afac-345">有关新 API 的详细信息，请参阅 [https://dev.loganalytics.io/](https://dev.loganalytics.io/)。</span><span class="sxs-lookup"><span data-stu-id="2afac-345">See [https://dev.loganalytics.io/](https://dev.loganalytics.io/) for more info on the new API.</span></span>

### <a name="azurermresources"></a><span data-ttu-id="2afac-346">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="2afac-346">AzureRM.Resources</span></span>
* <span data-ttu-id="2afac-347">`Get-AzureRmADServicePrincipal`：从默认 Empty 参数集中删除了 `-ServicePrincipalName`，因为它对于 SPN 参数集是冗余的</span><span class="sxs-lookup"><span data-stu-id="2afac-347">`Get-AzureRmADServicePrincipal`: Removed `-ServicePrincipalName` from the default Empty parameter set as it was redundant with the SPN parameter set</span></span>

### <a name="azurermservicebus"></a><span data-ttu-id="2afac-348">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2afac-348">AzureRM.ServiceBus</span></span>

* <span data-ttu-id="2afac-349">为 `Remove-AzureRmServiceBusRule` 和 `Get-AzureRmServiceBusKey` 添加了功能修复</span><span class="sxs-lookup"><span data-stu-id="2afac-349">Added functionality fix for `Remove-AzureRmServiceBusRule` and `Get-AzureRmServiceBusKey`</span></span>
* <span data-ttu-id="2afac-350">添加了以下新 cmdlet 以便执行异地灾难恢复操作。</span><span class="sxs-lookup"><span data-stu-id="2afac-350">Added below new commandlets for Geo Disaster Recovery operations.</span></span>
  - <span data-ttu-id="2afac-351">创建新别名（灾难恢复配置）：</span><span class="sxs-lookup"><span data-stu-id="2afac-351">Creating a new Alias (Disaster Recovery configuration):</span></span>
    - `New-AzureRmServiceBusDRConfigurations`
  - <span data-ttu-id="2afac-352">检索别名（灾难恢复配置）：</span><span class="sxs-lookup"><span data-stu-id="2afac-352">Retrieve Alias (Disaster Recovery configuration) :</span></span>
    - `Get-AzureRmServiceBusDRConfigurations`
  - <span data-ttu-id="2afac-353">禁用灾难恢复，并停止从主命名空间向辅助命名空间复制更改</span><span class="sxs-lookup"><span data-stu-id="2afac-353">Disabling the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>
    - `Set-AzureRmServiceBusDRConfigurationsBreakPairing`
  - <span data-ttu-id="2afac-354">调用灾难恢复故障转移并将别名重新配置为指向辅助命名空间</span><span class="sxs-lookup"><span data-stu-id="2afac-354">Invoking Disaster Recovery failover and reconfigure the alias to point to the secondary namespace</span></span>
    - `Set-AzureRmServiceBusDRConfigurationsFailOver`
  - <span data-ttu-id="2afac-355">删除别名（灾难恢复配置）</span><span class="sxs-lookup"><span data-stu-id="2afac-355">Deleting an Alias(Disaster Recovery configuration)</span></span>
    - `Remove-AzureRmServiceBusDRConfigurations`
* <span data-ttu-id="2afac-356">更新了 `Test-AzureRmServiceBusName` cmdlet 以支持异地灾难恢复 - 别名检查可用性操作。</span><span class="sxs-lookup"><span data-stu-id="2afac-356">Updated `Test-AzureRmServiceBusName` commandlets to support Geo Disaster Recovery - Alias name check availability operations.</span></span>
  - <span data-ttu-id="2afac-357">检查命名空间名称或别名（灾难恢复配置）名称的可用性：</span><span class="sxs-lookup"><span data-stu-id="2afac-357">Check the Availability of Namespace name or Alias(Disaster Recovery configuration) name:</span></span>
    - `Test-AzureRmServiceBusName`

### <a name="azurermusageaggregates"></a><span data-ttu-id="2afac-358">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="2afac-358">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="2afac-359">更正了 `Login-AzureRmAccount` 的用法以使用 `Connect-AzureRmAccount`</span><span class="sxs-lookup"><span data-stu-id="2afac-359">Corrected usage of `Login-AzureRmAccount` to use `Connect-AzureRmAccount`</span></span>

## <a name="520---january-2018"></a><span data-ttu-id="2afac-360">5.2.0 - 2018 年 1 月</span><span class="sxs-lookup"><span data-stu-id="2afac-360">5.2.0 - January 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="2afac-361">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="2afac-361">AzureRM.Profile</span></span>
* <span data-ttu-id="2afac-362">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="2afac-362">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="2afac-363">Add-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="2afac-363">Add-AzureRmAccount</span></span>
  * <span data-ttu-id="2afac-364">添加了 -MSI 登录名，用于通过当前 VM/服务的托管服务标识的凭据进行身份验证</span><span class="sxs-lookup"><span data-stu-id="2afac-364">Added -MSI login for authenticationg using the credentials of the Managed Service Identity of the current VM / Service</span></span>
  * <span data-ttu-id="2afac-365">修复了使用用户提供的访问令牌登录时存在的 KeyVault 身份验证问题</span><span class="sxs-lookup"><span data-stu-id="2afac-365">Fixed KeyVault Authentication when logging in with user-provided access tokens</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="2afac-366">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="2afac-366">Azure.Storage</span></span>
* <span data-ttu-id="2afac-367">添加了 cmdlet 用于获取和设置存储服务属性</span><span class="sxs-lookup"><span data-stu-id="2afac-367">Add cmdlets to get and set Storage service properties</span></span>
    - <span data-ttu-id="2afac-368">Get-AzureStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="2afac-368">Get-AzureStorageServiceProperty</span></span>
    - <span data-ttu-id="2afac-369">Update-AzureStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="2afac-369">Update-AzureStorageServiceProperty</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="2afac-370">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="2afac-370">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="2afac-371">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="2afac-371">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="2afac-372">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2afac-372">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="2afac-373">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="2afac-373">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="2afac-374">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="2afac-374">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="2afac-375">已弃用 -Tags，对 New-AzureRmApiManagementProperty、Set-AzureRmApiManagementProperty 和 New-AzureRmApiManagement 改用 -Tag</span><span class="sxs-lookup"><span data-stu-id="2afac-375">Obsoleted -Tags in favor of -Tag for New-AzureRmApiManagementProperty, Set-AzureRmApiManagementProperty, and New-AzureRmApiManagement</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="2afac-376">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="2afac-376">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="2afac-377">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="2afac-377">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="2afac-378">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="2afac-378">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="2afac-379">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="2afac-379">AzureRM.Automation</span></span>
* <span data-ttu-id="2afac-380">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="2afac-380">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="2afac-381">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="2afac-381">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="2afac-382">已弃用 -Tags，对 Set-AzureRmAutomationRunbook 改用 -Tag</span><span class="sxs-lookup"><span data-stu-id="2afac-382">Obsoleted -Tags in favor of -Tag for Set-AzureRmAutomationRunbook</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="2afac-383">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="2afac-383">AzureRM.Backup</span></span>
* <span data-ttu-id="2afac-384">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="2afac-384">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="2afac-385">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="2afac-385">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="2afac-386">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="2afac-386">AzureRM.Batch</span></span>
* <span data-ttu-id="2afac-387">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="2afac-387">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="2afac-388">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="2afac-388">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="2afac-389">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="2afac-389">AzureRM.Cdn</span></span>
* <span data-ttu-id="2afac-390">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="2afac-390">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="2afac-391">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="2afac-391">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="2afac-392">已弃用 -Tags，对 New-AzureRmCdnEndpoint 和 New-AzureRmCdnProfile 改用 -Tag</span><span class="sxs-lookup"><span data-stu-id="2afac-392">Obsoleted -Tags in favor of -Tag for New-AzureRmCdnEndpoint and New-AzureRmCdnProfile</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="2afac-393">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2afac-393">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="2afac-394">与认知服务管理 SDK 版本 3.0.0 集成。</span><span class="sxs-lookup"><span data-stu-id="2afac-394">Integrate with Cognitive Services Management SDK version 3.0.0.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="2afac-395">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="2afac-395">AzureRM.Compute</span></span>
* <span data-ttu-id="2afac-396">为 New-AzureRmVmss 添加了简化的参数集，用于通过智能默认值创建虚拟机规模集和所有必需的资源</span><span class="sxs-lookup"><span data-stu-id="2afac-396">Added simplified parameter set to New-AzureRmVmss, which creates a Virtual Machine Scale Set and all required resources using smart defaults</span></span>
* <span data-ttu-id="2afac-397">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="2afac-397">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="2afac-398">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="2afac-398">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="2afac-399">已弃用 -Tags，对 New-AzureRmVm 和 Update-AzureRmVm 改用 -Tag</span><span class="sxs-lookup"><span data-stu-id="2afac-399">Obsoleted -Tags in favor of -Tag for New-AzureRmVm and Update-AzureRmVm</span></span>
* <span data-ttu-id="2afac-400">修复了 Zone 受限制时的 Get-AzureRmComputeResourceSku cmdlet 问题。</span><span class="sxs-lookup"><span data-stu-id="2afac-400">Fixed Get-AzureRmComputeResourceSku cmdlet when Zone is included in restriction.</span></span>
* <span data-ttu-id="2afac-401">为 Azure Monitor 接收器支持更新了诊断代理配置架构。</span><span class="sxs-lookup"><span data-stu-id="2afac-401">Updated Diagnostics Agent configuration schema for Azure Monitor sink support.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="2afac-402">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="2afac-402">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="2afac-403">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="2afac-403">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="2afac-404">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="2afac-404">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="2afac-405">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="2afac-405">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="2afac-406">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="2afac-406">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="2afac-407">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="2afac-407">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="2afac-408">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="2afac-408">AzureRM.DataFactories</span></span>
* <span data-ttu-id="2afac-409">对所有数据存储链接服务启用了 Azure Key Vault 支持</span><span class="sxs-lookup"><span data-stu-id="2afac-409">Enabled Azure Key Vault support for all data store linked services</span></span>
* <span data-ttu-id="2afac-410">添加了 Azure SSIS 集成运行时的许可证类型属性</span><span class="sxs-lookup"><span data-stu-id="2afac-410">Added license type property for Azure SSIS integration runtime</span></span>
* <span data-ttu-id="2afac-411">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="2afac-411">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="2afac-412">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="2afac-412">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="2afac-413">已弃用 -Tags，对 New-AzureRmDataFactory 改用 -Tag</span><span class="sxs-lookup"><span data-stu-id="2afac-413">Obsoleted -Tags in favor of -Tag for New-AzureRmDataFactory</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="2afac-414">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="2afac-414">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="2afac-415">对所有数据存储链接服务启用了 Azure Key Vault 支持</span><span class="sxs-lookup"><span data-stu-id="2afac-415">Enabled Azure Key Vault support for all data store linked services</span></span>
* <span data-ttu-id="2afac-416">添加了 Azure SSIS 集成运行时的许可证类型属性</span><span class="sxs-lookup"><span data-stu-id="2afac-416">Added license type property for Azure SSIS integration runtime</span></span>
* <span data-ttu-id="2afac-417">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="2afac-417">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="2afac-418">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="2afac-418">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="2afac-419">为“Set-AzureRmDataFactoryV2IntegrationRuntime”cmd 添加了参数“LicenseType”，以启用 AHUB 功能</span><span class="sxs-lookup"><span data-stu-id="2afac-419">Add parameter "LicenseType" for "Set-AzureRmDataFactoryV2IntegrationRuntime" cmd to enable AHUB functionality</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="2afac-420">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="2afac-420">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="2afac-421">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="2afac-421">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="2afac-422">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="2afac-422">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="2afac-423">已弃用 -Tags，对 New-AzureRmDataLakeAnalyticsAccount 和 Set-AzureRmDataLakeAnalyticsAccount 改用 -Tag</span><span class="sxs-lookup"><span data-stu-id="2afac-423">Obsoleted -Tags in favor of -Tag for New-AzureRmDataLakeAnalyticsAccount and Set-AzureRmDataLakeAnalyticsAccount</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="2afac-424">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2afac-424">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="2afac-425">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="2afac-425">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="2afac-426">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="2afac-426">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="2afac-427">已弃用 -Tags，对 New-AzureRmDataLakeStoreAccount 和 Set-AzureRmDataLakeStoreAccount 改用 -Tag</span><span class="sxs-lookup"><span data-stu-id="2afac-427">Obsoleted -Tags in favor of -Tag for New-AzureRmDataLakeStoreAccount and Set-AzureRmDataLakeStoreAccount</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="2afac-428">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="2afac-428">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="2afac-429">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="2afac-429">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="2afac-430">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="2afac-430">AzureRM.Dns</span></span>
* <span data-ttu-id="2afac-431">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="2afac-431">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="2afac-432">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="2afac-432">AzureRM.EventGrid</span></span>
* <span data-ttu-id="2afac-433">添加了以下新的 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="2afac-433">Added the following new cmdlet:</span></span>
  - <span data-ttu-id="2afac-434">Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="2afac-434">Update-AzureRmEventGridSubscription</span></span>
    - <span data-ttu-id="2afac-435">更新了事件网格事件订阅的属性。</span><span class="sxs-lookup"><span data-stu-id="2afac-435">Update the properties of an Event Grid event subscription.</span></span>
* <span data-ttu-id="2afac-436">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="2afac-436">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="2afac-437">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="2afac-437">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="2afac-438">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="2afac-438">AzureRM.EventHub</span></span>
* <span data-ttu-id="2afac-439">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="2afac-439">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="2afac-440">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="2afac-440">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="2afac-441">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="2afac-441">AzureRM.HDInsight</span></span>
* <span data-ttu-id="2afac-442">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="2afac-442">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="2afac-443">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="2afac-443">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="2afac-444">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="2afac-444">AzureRM.Insights</span></span>
* <span data-ttu-id="2afac-445">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="2afac-445">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="2afac-446">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="2afac-446">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="2afac-447">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="2afac-447">AzureRM.IotHub</span></span>
* <span data-ttu-id="2afac-448">添加了对 IoTHub cmdlet 的 Certificate 支持</span><span class="sxs-lookup"><span data-stu-id="2afac-448">Add Certificate support for IoTHub cmdlets</span></span>
* <span data-ttu-id="2afac-449">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="2afac-449">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="2afac-450">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="2afac-450">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="2afac-451">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2afac-451">AzureRM.KeyVault</span></span>
* <span data-ttu-id="2afac-452">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="2afac-452">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="2afac-453">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="2afac-453">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="2afac-454">添加了对长时间运行的 KeyVault cmdlet 的 -AsJob 支持。</span><span class="sxs-lookup"><span data-stu-id="2afac-454">Added -AsJob support for long-running KeyVault cmdlets.</span></span> <span data-ttu-id="2afac-455">允许选定的 cmdlet 在后台运行并返回可跟踪和控制进度的作业。</span><span class="sxs-lookup"><span data-stu-id="2afac-455">Allows selected cmdlets to run in the background and return a job to track and control progress.</span></span>
  * <span data-ttu-id="2afac-456">受影响的 cmdlet 为：Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="2afac-456">Affected cmdlet is: Remove-AzureRmKeyVault</span></span>
* <span data-ttu-id="2afac-457">修复了 Set-AzureRmKeyVaultAccessPolicy 的 bug：AAD 筛选器将 SPN 设置为提供的 UPN，而不是设置 UPN</span><span class="sxs-lookup"><span data-stu-id="2afac-457">Fixed bug in Set-AzureRmKeyVaultAccessPolicy where the AAD filter was setting SPN to the provided UPN, rather than setting the UPN</span></span>
  - <span data-ttu-id="2afac-458">有关详细信息，请参阅以下问题： https://github.com/Azure/azure-powershell/issues/5201</span><span class="sxs-lookup"><span data-stu-id="2afac-458">See the following issue for more information: https://github.com/Azure/azure-powershell/issues/5201</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="2afac-459">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="2afac-459">AzureRM.LogicApp</span></span>
* <span data-ttu-id="2afac-460">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="2afac-460">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="2afac-461">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="2afac-461">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="2afac-462">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="2afac-462">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="2afac-463">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="2afac-463">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="2afac-464">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="2afac-464">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="2afac-465">已弃用 -Tags，对 Update-AzureRmMlCommitmentPlan 改用 -Tag</span><span class="sxs-lookup"><span data-stu-id="2afac-465">Obsoleted -Tags in favor of -Tag for Update-AzureRmMlCommitmentPlan</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="2afac-466">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="2afac-466">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="2afac-467">将 IncludeAllResources 参数添加到了 Remove-AzureRmMlOpCluster cmdlet</span><span class="sxs-lookup"><span data-stu-id="2afac-467">Add IncludeAllResources parameter to Remove-AzureRmMlOpCluster cmdlet</span></span>
  - <span data-ttu-id="2afac-468">使用此开关参数会删除最初在群集中创建的所有资源</span><span class="sxs-lookup"><span data-stu-id="2afac-468">Using this switch parameter will remove all resources that were created with the cluster originally</span></span>
* <span data-ttu-id="2afac-469">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="2afac-469">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="2afac-470">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="2afac-470">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="2afac-471">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="2afac-471">AzureRM.Media</span></span>
* <span data-ttu-id="2afac-472">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="2afac-472">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="2afac-473">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="2afac-473">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="2afac-474">已弃用 -Tags，对 Set-AzureRmMediaService 和 New-AzureRmMediaService 改用 -Tag</span><span class="sxs-lookup"><span data-stu-id="2afac-474">Obsoleted -Tags in favor of -Tag for Set-AzureRmMediaService and New-AzureRmMediaService</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="2afac-475">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="2afac-475">AzureRM.Network</span></span>
* <span data-ttu-id="2afac-476">添加了对长时间运行的 Network cmdlet 的 -AsJob 支持。</span><span class="sxs-lookup"><span data-stu-id="2afac-476">Added -AsJob support for long-running Network cmdlets.</span></span> <span data-ttu-id="2afac-477">允许选定的 cmdlet 在后台运行并返回可跟踪和控制进度的作业。</span><span class="sxs-lookup"><span data-stu-id="2afac-477">Allows selected cmdlets to run in the background and return a job to track and control progress.</span></span>
* <span data-ttu-id="2afac-478">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="2afac-478">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="2afac-479">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="2afac-479">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="2afac-480">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="2afac-480">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="2afac-481">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="2afac-481">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="2afac-482">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="2afac-482">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="2afac-483">已弃用 -Tags，对 New-AzureRmNotificationHubsNamespace 和 Set-AzureRmNotificationHubsNamespace 改用 -Tag</span><span class="sxs-lookup"><span data-stu-id="2afac-483">Obsoleted -Tags in favor of -Tag for New-AzureRmNotificationHubsNamespace and Set-AzureRmNotificationHubsNamespace</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="2afac-484">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2afac-484">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="2afac-485">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="2afac-485">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="2afac-486">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="2afac-486">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="2afac-487">已弃用 -Tags，对 New-AzureRmOperationalInsightsSavedSearch、Set-AzureRmOperationalInsightsSavedSearch、New-AzureRmOperationalInsightsWorkspace 和 Set-AzureRmOperationalInsightsWorkspace 改用 -Tag</span><span class="sxs-lookup"><span data-stu-id="2afac-487">Obsoleted -Tags in favor of -Tag for New-AzureRmOperationalInsightsSavedSearch, Set-AzureRmOperationalInsightsSavedSearch, New-AzureRmOperationalInsightsWorkspace, and Set-AzureRmOperationalInsightsWorkspace</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="2afac-488">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="2afac-488">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="2afac-489">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="2afac-489">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="2afac-490">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="2afac-490">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="2afac-491">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2afac-491">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="2afac-492">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="2afac-492">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="2afac-493">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="2afac-493">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="2afac-494">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="2afac-494">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="2afac-495">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="2afac-495">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="2afac-496">为 Restore-AzureRmRecoveryServicesBackupItem cmdlet 添加了 -UseOriginalStorageAccount 选项。</span><span class="sxs-lookup"><span data-stu-id="2afac-496">Added -UseOriginalStorageAccount option to the Restore-AzureRmRecoveryServicesBackupItem cmdlet.</span></span>
  - <span data-ttu-id="2afac-497">启用此标志会导致将磁盘还原到其原始存储帐户，从而让用户尽量将还原后的 VM 的配置接近原始 VM。</span><span class="sxs-lookup"><span data-stu-id="2afac-497">Enabling this flag results in restoring disks to their original storage accounts which allows users to maintain the configuration of restored VM as close to the original VMs as possible.</span></span>
  - <span data-ttu-id="2afac-498">此外，这还有助于提高还原操作的性能。</span><span class="sxs-lookup"><span data-stu-id="2afac-498">It also helps in improving the performance of the restore operation.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="2afac-499">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="2afac-499">AzureRM.RedisCache</span></span>
* <span data-ttu-id="2afac-500">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="2afac-500">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="2afac-501">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="2afac-501">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="2afac-502">为防火墙规则添加了 3 个新的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="2afac-502">Added  3 new cmdlets for firewall rules</span></span>
* <span data-ttu-id="2afac-503">为异地复制添加了 3 个新的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="2afac-503">Added  3 new cmdlets for geo replication</span></span>
* <span data-ttu-id="2afac-504">添加了对区域和标记的支持</span><span class="sxs-lookup"><span data-stu-id="2afac-504">Added support for zones and tags</span></span>
* <span data-ttu-id="2afac-505">尽量将 ResourceGroup 用作可选选项。</span><span class="sxs-lookup"><span data-stu-id="2afac-505">Make ResourceGroup as optional whenever possible.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="2afac-506">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="2afac-506">AzureRM.Relay</span></span>
* <span data-ttu-id="2afac-507">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="2afac-507">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="2afac-508">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="2afac-508">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="2afac-509">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="2afac-509">AzureRM.Resources</span></span>
* <span data-ttu-id="2afac-510">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="2afac-510">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="2afac-511">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="2afac-511">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="2afac-512">添加了对长时间运行的 Resources cmdlet 的 -AsJob 支持。</span><span class="sxs-lookup"><span data-stu-id="2afac-512">Added -AsJob support for long-running Resources cmdlets.</span></span> <span data-ttu-id="2afac-513">允许选定的 cmdlet 在后台运行并返回可跟踪和控制进度的作业。</span><span class="sxs-lookup"><span data-stu-id="2afac-513">Allows selected cmdlets to run in the background and return a job to track and control progress.</span></span>
* <span data-ttu-id="2afac-514">将别名从 Get-AzureRmProviderOperation 更改为 Get-AzureRmResourceProviderAction，以符合命名约定</span><span class="sxs-lookup"><span data-stu-id="2afac-514">Added alias from Get-AzureRmProviderOperation to Get-AzureRmResourceProviderAction to conform with naming conventions</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="2afac-515">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="2afac-515">AzureRM.Scheduler</span></span>
* <span data-ttu-id="2afac-516">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="2afac-516">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="2afac-517">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="2afac-517">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermservermanagement"></a><span data-ttu-id="2afac-518">AzureRM.ServerManagement</span><span class="sxs-lookup"><span data-stu-id="2afac-518">AzureRM.ServerManagement</span></span>
* <span data-ttu-id="2afac-519">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="2afac-519">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="2afac-520">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="2afac-520">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="2afac-521">已弃用 -Tags，对 New-AzureRmServerManagementNode 和 New-AzureRmServerManagementGateway 改用 -Tag</span><span class="sxs-lookup"><span data-stu-id="2afac-521">Obsoleted -Tags in favor of -Tag for New-AzureRmServerManagementNode and New-AzureRmServerManagementGateway</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="2afac-522">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2afac-522">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="2afac-523">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="2afac-523">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="2afac-524">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="2afac-524">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="2afac-525">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2afac-525">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="2afac-526">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="2afac-526">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="2afac-527">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="2afac-527">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermsiterecovery"></a><span data-ttu-id="2afac-528">AzureRM.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="2afac-528">AzureRM.SiteRecovery</span></span>
* <span data-ttu-id="2afac-529">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="2afac-529">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="2afac-530">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="2afac-530">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="2afac-531">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="2afac-531">AzureRM.Sql</span></span>
* <span data-ttu-id="2afac-532">更新了 Auditing 命令参数说明</span><span class="sxs-lookup"><span data-stu-id="2afac-532">Update the Auditing commands parameters description</span></span>
* <span data-ttu-id="2afac-533">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="2afac-533">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="2afac-534">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="2afac-534">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="2afac-535">为长时间运行的 cmdlet 添加了 -AsJob 参数</span><span class="sxs-lookup"><span data-stu-id="2afac-535">Added -AsJob parameter to long running cmdlets</span></span>
* <span data-ttu-id="2afac-536">已弃用 Get-AzureRmSqlServiceObjective 的 -DatabaseName 参数</span><span class="sxs-lookup"><span data-stu-id="2afac-536">Obsoleted -DatabaseName parameter from Get-AzureRmSqlServiceObjective</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="2afac-537">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="2afac-537">AzureRM.Storage</span></span>
* <span data-ttu-id="2afac-538">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="2afac-538">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="2afac-539">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="2afac-539">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="2afac-540">修复了结合 -EnableEncryptionService None 参数运行 cmdlet New-AzureRMStorageAccount 时的空引用问题</span><span class="sxs-lookup"><span data-stu-id="2afac-540">Fix a null reference issue of run cmdlet New-AzureRMStorageAccount with parameter -EnableEncryptionService None</span></span>
* <span data-ttu-id="2afac-541">添加了对长时间运行的 Storage cmdlet 的 -AsJob 支持。</span><span class="sxs-lookup"><span data-stu-id="2afac-541">Added -AsJob support for long-running Storage cmdlets.</span></span> <span data-ttu-id="2afac-542">允许选定的 cmdlet 在后台运行并返回可跟踪和控制进度的作业。</span><span class="sxs-lookup"><span data-stu-id="2afac-542">Allows selected cmdlets to run in the background and return a job to track and control progress.</span></span>
    - <span data-ttu-id="2afac-543">受影响的 cmdlet 为针对存储帐户和存储帐户网络规则的 New-、Remove-、Add- 和 Update-。</span><span class="sxs-lookup"><span data-stu-id="2afac-543">Affected cmdlets are New-, Remove-, Add-, and Update- for Storage Account and Storage Account Network Rule.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="2afac-544">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="2afac-544">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="2afac-545">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="2afac-545">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="2afac-546">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="2afac-546">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="2afac-547">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="2afac-547">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="2afac-548">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="2afac-548">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="2afac-549">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="2afac-549">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="2afac-550">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="2afac-550">AzureRM.Websites</span></span>
* <span data-ttu-id="2afac-551">为 -Location 参数添加了 Location 补全选项，用于通过 Tab 键补全有效的位置</span><span class="sxs-lookup"><span data-stu-id="2afac-551">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="2afac-552">为 -ResourceGroup 参数添加了 ResourceGroup 补全选项，用于通过 Tab 键补全当前订阅中的资源组</span><span class="sxs-lookup"><span data-stu-id="2afac-552">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="2afac-553">添加了对长时间运行的 Websites cmdlet 的 -AsJob 支持。</span><span class="sxs-lookup"><span data-stu-id="2afac-553">Added -AsJob support for long-running Websites cmdlets.</span></span> <span data-ttu-id="2afac-554">允许选定的 cmdlet 在后台运行并返回可跟踪和控制进度的作业。</span><span class="sxs-lookup"><span data-stu-id="2afac-554">Allows selected cmdlets to run in the background and return a job to track and control progress.</span></span>
     - <span data-ttu-id="2afac-555">受影响的 cmdlet 为针对 Web 应用、应用服务计划和槽位的 New-、Remove-、Add- 和 Set-</span><span class="sxs-lookup"><span data-stu-id="2afac-555">Affected cmdlets are New-, Remove-, Add-, and Set- for WebApps, AppServicePlan and Slots</span></span>

## <a name="2017128-version-511"></a><span data-ttu-id="2afac-556">2017.12.8 版本 5.1.1</span><span class="sxs-lookup"><span data-stu-id="2afac-556">2017.12.8 Version 5.1.1</span></span>
* <span data-ttu-id="2afac-557">AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="2afac-557">AnalysisServices</span></span>
  - <span data-ttu-id="2afac-558">将位置的验证集更改为动态查找，以便支持所有云。</span><span class="sxs-lookup"><span data-stu-id="2afac-558">Change validate set of location to dynamic lookup so that all clouds are supported.</span></span>
* <span data-ttu-id="2afac-559">自动化</span><span class="sxs-lookup"><span data-stu-id="2afac-559">Automation</span></span>
  - <span data-ttu-id="2afac-560">更新为 Import-AzureRMAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2afac-560">Update to Import-AzureRMAutomationRunbook</span></span>
    - <span data-ttu-id="2afac-561">现在为 Python2 Runbook 提供支持</span><span class="sxs-lookup"><span data-stu-id="2afac-561">Support is now being provided for Python2 runbooks</span></span>
* <span data-ttu-id="2afac-562">Batch</span><span class="sxs-lookup"><span data-stu-id="2afac-562">Batch</span></span>
  - <span data-ttu-id="2afac-563">修复了没有资源组时帐户操作无法自动检测资源组这一 Bug</span><span class="sxs-lookup"><span data-stu-id="2afac-563">Fixed a bug where account operations without a resource group failed to auto-detect the resource group</span></span>
* <span data-ttu-id="2afac-564">计算</span><span class="sxs-lookup"><span data-stu-id="2afac-564">Compute</span></span>
  - <span data-ttu-id="2afac-565">Get-AzureRmComputeResourceSku 显示区域信息。</span><span class="sxs-lookup"><span data-stu-id="2afac-565">Get-AzureRmComputeResourceSku shows zone information.</span></span>
  - <span data-ttu-id="2afac-566">更新 Disable-AzureRmVmssDiskEncryption 以修复问题 https://github.com/Azure/azure-powershell/issues/5038</span><span class="sxs-lookup"><span data-stu-id="2afac-566">Update Disable-AzureRmVmssDiskEncryption to fix issue https://github.com/Azure/azure-powershell/issues/5038</span></span>
  - <span data-ttu-id="2afac-567">添加了对长时间运行的计算 cmdlet 的 -AsJob 支持。</span><span class="sxs-lookup"><span data-stu-id="2afac-567">Added -AsJob support for long-running Compute cmdlets.</span></span> <span data-ttu-id="2afac-568">允许选定的 cmdlet 在后台运行并返回可跟踪和控制进度的作业。</span><span class="sxs-lookup"><span data-stu-id="2afac-568">Allows selected cmdlets to run in the background and return a job to track and control progress.</span></span>
    - <span data-ttu-id="2afac-569">受影响的 cmdlet 包括适用于虚拟机和虚拟机规模集的 New-、Update-、Set-、Remove-、Start-、Restart-、Stop- cmdlet</span><span class="sxs-lookup"><span data-stu-id="2afac-569">Affected cmdlets include: New-, Update-, Set-, Remove-, Start-, Restart-, Stop- cmdlets for Virtual Machines and Virtual Machine Scale Sets</span></span>
    - <span data-ttu-id="2afac-570">向 New-AzureRmVM（可使用智能默认设置创建虚拟机和所有必需的资源）添加了简化的参数集</span><span class="sxs-lookup"><span data-stu-id="2afac-570">Added simplified parameter set to New-AzureRmVM, which creates a Virtual Machine and all required resources using smart defaults</span></span>
* <span data-ttu-id="2afac-571">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="2afac-571">ContainerInstance</span></span>
  - <span data-ttu-id="2afac-572">应用 Azure 容器实例 SDK 2017-10-01</span><span class="sxs-lookup"><span data-stu-id="2afac-572">Apply Azure Container Instance SDK 2017-10-01</span></span>
    - <span data-ttu-id="2afac-573">支持容器 run-to-completion</span><span class="sxs-lookup"><span data-stu-id="2afac-573">Support container run-to-completion</span></span>
    - <span data-ttu-id="2afac-574">支持 Azure 文件卷装载</span><span class="sxs-lookup"><span data-stu-id="2afac-574">Support Azure File volume mount</span></span>
    - <span data-ttu-id="2afac-575">支持为公共 IP 打开多个端口</span><span class="sxs-lookup"><span data-stu-id="2afac-575">Support opening multiple ports for public IP</span></span>
* <span data-ttu-id="2afac-576">ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="2afac-576">ContainerRegistry</span></span>
  - <span data-ttu-id="2afac-577">用于异地复制和 Webhook 的新 cmdlet</span><span class="sxs-lookup"><span data-stu-id="2afac-577">New cmdlets for geo-replication and webhooks</span></span>
    - <span data-ttu-id="2afac-578">Get/New/Remove-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="2afac-578">Get/New/Remove-AzureRmContainerRegistryReplication</span></span>
    - <span data-ttu-id="2afac-579">Get/New/Remove/Test/Update-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="2afac-579">Get/New/Remove/Test/Update-AzureRmContainerRegistryWebhook</span></span>
* <span data-ttu-id="2afac-580">数据工厂</span><span class="sxs-lookup"><span data-stu-id="2afac-580">DataFactories</span></span>
    - <span data-ttu-id="2afac-581">凭据加密功能现在适用于启用了“远程访问”的操作（通过网络的操作）和禁用了“远程访问”的操作（本地计算机操作）。</span><span class="sxs-lookup"><span data-stu-id="2afac-581">Credential encryption functionality now works with both "Remote Access" enabled (Over Network) and "Remote Access" disabled (Local Machine).</span></span>
* <span data-ttu-id="2afac-582">DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="2afac-582">DataFactoryV2</span></span>
  - <span data-ttu-id="2afac-583">添加了两个新的 cmdlet：Update-AzureRmDataFactoryV2 和 Stop-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="2afac-583">Added two new cmdlets: Update-AzureRmDataFactoryV2 and Stop-AzureRmDataFactoryV2PipelineRun</span></span>
* <span data-ttu-id="2afac-584">DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="2afac-584">DataLakeAnalytics</span></span>
  - <span data-ttu-id="2afac-585">向 Submit-AzureRmDataLakeAnalyticsJob 添加了名为 ScriptParameter 的参数</span><span class="sxs-lookup"><span data-stu-id="2afac-585">Added a parameter called ScriptParameter to Submit-AzureRmDataLakeAnalyticsJob</span></span>
    - <span data-ttu-id="2afac-586">可以对 Submit-AzureRmDataLakeAnalyticsJob 使用 Get-Help 来查找有关 ScriptParameter 的详细信息</span><span class="sxs-lookup"><span data-stu-id="2afac-586">Detailed information about ScriptParameter can be found using Get-Help on Submit-AzureRmDataLakeAnalyticsJob</span></span>
  - <span data-ttu-id="2afac-587">已将 New-AzureRmDataLakeAnalyticsAccount 的参数 MaxDegreeOfParallelism 更改为 MaxAnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="2afac-587">For New-AzureRmDataLakeAnalyticsAccount, changed the parameter MaxDegreeOfParallelism to MaxAnalyticsUnits</span></span>
    - <span data-ttu-id="2afac-588">为参数 MaxAnalyticsUnits 添加了别名 MaxDegreeOfParallelism</span><span class="sxs-lookup"><span data-stu-id="2afac-588">Added an alias for the parameter MaxAnalyticsUnits: MaxDegreeOfParallelism</span></span>
  - <span data-ttu-id="2afac-589">已将 New-AzureRmDataLakeAnalyticsComputePolicy 的参数 MaxDegreeOfParallelismPerJob 更改为 MaxAnalyticsUnitsPerJob</span><span class="sxs-lookup"><span data-stu-id="2afac-589">For New-AzureRmDataLakeAnalyticsComputePolicy, changed the parameter MaxDegreeOfParallelismPerJob to MaxAnalyticsUnitsPerJob</span></span>
    - <span data-ttu-id="2afac-590">为参数 MaxAnalyticsUnitsPerJob 添加了别名 MaxDegreeOfParallelismPerJob</span><span class="sxs-lookup"><span data-stu-id="2afac-590">Added an alias for the parameter MaxAnalyticsUnitsPerJob: MaxDegreeOfParallelismPerJob</span></span>
  - <span data-ttu-id="2afac-591">已将 Set-AzureRmDataLakeAnalyticsAccount 的参数 MaxDegreeOfParallelism 更改为 MaxAnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="2afac-591">For Set-AzureRmDataLakeAnalyticsAccount, changed the parameter MaxDegreeOfParallelism to MaxAnalyticsUnits</span></span>
    - <span data-ttu-id="2afac-592">为参数 MaxAnalyticsUnits 添加了别名 MaxDegreeOfParallelism</span><span class="sxs-lookup"><span data-stu-id="2afac-592">Added an alias for the parameter MaxAnalyticsUnits: MaxDegreeOfParallelism</span></span>
  - <span data-ttu-id="2afac-593">已将 Submit-AzureRmDataLakeAnalyticsJob 的参数 DegreeOfParallelism 更改为 AnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="2afac-593">For Submit-AzureRmDataLakeAnalyticsJob, changed the parameter DegreeOfParallelism to AnalyticsUnits</span></span>
    - <span data-ttu-id="2afac-594">为参数 AnalyticsUnits 添加了别名 DegreeOfParallelism</span><span class="sxs-lookup"><span data-stu-id="2afac-594">Added an alias for the parameter AnalyticsUnits: DegreeOfParallelism</span></span>
  - <span data-ttu-id="2afac-595">已将 Update-AzureRmDataLakeAnalyticsComputePolicy 的参数 MaxDegreeOfParallelismPerJob 更改为 MaxAnalyticsUnitsPerJob</span><span class="sxs-lookup"><span data-stu-id="2afac-595">For Update-AzureRmDataLakeAnalyticsComputePolicy, changed the parameter MaxDegreeOfParallelismPerJob to MaxAnalyticsUnitsPerJob</span></span>
    - <span data-ttu-id="2afac-596">为参数 MaxAnalyticsUnitsPerJob 添加了别名 MaxDegreeOfParallelismPerJob</span><span class="sxs-lookup"><span data-stu-id="2afac-596">Added an alias for the parameter MaxAnalyticsUnitsPerJob: MaxDegreeOfParallelismPerJob</span></span>
* <span data-ttu-id="2afac-597">MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="2afac-597">MachineLearningCompute</span></span>
  - <span data-ttu-id="2afac-598">添加 Set-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="2afac-598">Add Set-AzureRmMlOpCluster</span></span>
    - <span data-ttu-id="2afac-599">更新群集的代理计数或 SSL 配置</span><span class="sxs-lookup"><span data-stu-id="2afac-599">Update a cluster's agent count or SSL configuration</span></span>
  - <span data-ttu-id="2afac-600">业务流程协调程序属性为可选</span><span class="sxs-lookup"><span data-stu-id="2afac-600">Orchestrator properties are optional</span></span>
    - <span data-ttu-id="2afac-601">此服务会创建服务主体（如果未提供），因此业务流程协调程序属性现在为可选</span><span class="sxs-lookup"><span data-stu-id="2afac-601">The service will create a service principal if not provided, so the orchestrator properties are now optional</span></span>
* <span data-ttu-id="2afac-602">PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="2afac-602">PowerBIEmbedded</span></span>
  - <span data-ttu-id="2afac-603">添加对 Power BI Embedded 容量 cmdlet 的支持</span><span class="sxs-lookup"><span data-stu-id="2afac-603">Add support for Power BI Embedded Capacity cmdlets</span></span>
  - <span data-ttu-id="2afac-604">全新 Cmdlet Get-AzureRmPowerBIEmbeddedCapacity - 获取 PowerBI Embedded 容量的详细信息。</span><span class="sxs-lookup"><span data-stu-id="2afac-604">New Cmdlet Get-AzureRmPowerBIEmbeddedCapacity - Gets the details of a PowerBI Embedded Capacity.</span></span>
  - <span data-ttu-id="2afac-605">全新 Cmdlet New-AzureRmPowerBIEmbeddedCapacity - 创建新的 PowerBI Embedded 容量</span><span class="sxs-lookup"><span data-stu-id="2afac-605">New Cmdlet New-AzureRmPowerBIEmbeddedCapacity - Creates a new PowerBI Embedded Capacity</span></span>
  - <span data-ttu-id="2afac-606">全新 Cmdlet Remove-AzureRmPowerBIEmbeddedCapacity - 删除 PowerBI Embedded 容量的实例</span><span class="sxs-lookup"><span data-stu-id="2afac-606">New Cmdlet Remove-AzureRmPowerBIEmbeddedCapacity - Deletes an instance of PowerBI Embedded Capacity</span></span>
  - <span data-ttu-id="2afac-607">全新 Cmdlet Resume-AzureRmPowerBIEmbeddedCapacity - 恢复 PowerBI Embedded 容量的实例</span><span class="sxs-lookup"><span data-stu-id="2afac-607">New Cmdlet Resume-AzureRmPowerBIEmbeddedCapacity - Resumes an instance of PowerBI Embedded Capacity</span></span>
  - <span data-ttu-id="2afac-608">全新 Cmdlet Suspend-AzureRmPowerBIEmbeddedCapacity - 暂停 PowerBI Embedded 容量的实例</span><span class="sxs-lookup"><span data-stu-id="2afac-608">New Cmdlet Suspend-AzureRmPowerBIEmbeddedCapacity - Suspends an instance of PowerBI Embedded Capacity</span></span>
  - <span data-ttu-id="2afac-609">全新 Cmdlet Test-AzureRmPowerBIEmbeddedCapacity - 测试 PowerBI Embedded 容量的实例是否存在</span><span class="sxs-lookup"><span data-stu-id="2afac-609">New Cmdlet Test-AzureRmPowerBIEmbeddedCapacity - Tests the existence of an instance of PowerBI Embedded Capacity</span></span>
  - <span data-ttu-id="2afac-610">全新 Cmdlet Update-AzureRmPowerBIEmbeddedCapacity - 修改 PowerBI Embedded 容量的实例</span><span class="sxs-lookup"><span data-stu-id="2afac-610">New Cmdlet Update-AzureRmPowerBIEmbeddedCapacity - Modifies an instance of PowerBI Embedded Capacity</span></span>
* <span data-ttu-id="2afac-611">配置文件</span><span class="sxs-lookup"><span data-stu-id="2afac-611">Profile</span></span>
  - <span data-ttu-id="2afac-612">将 USGovernmentActiveDirectoryEndpoint 更新到了 https://login.microsoftonline.us/</span><span class="sxs-lookup"><span data-stu-id="2afac-612">Updated USGovernmentActiveDirectoryEndpoint to https://login.microsoftonline.us/</span></span>
    - <span data-ttu-id="2afac-613">有关 Azure 政府版终结点映射的详细信息，请参阅下文： https://docs.microsoft.com/en-us/azure/azure-government/documentation-government-developer-guide#endpoint-mapping</span><span class="sxs-lookup"><span data-stu-id="2afac-613">For more information about the Azure Government endpoint mappings, please see the following: https://docs.microsoft.com/en-us/azure/azure-government/documentation-government-developer-guide#endpoint-mapping</span></span>
    - <span data-ttu-id="2afac-614">添加了对 cmdlet 的 -AsJob 支持，允许所选 cmdlet 在后台执行并返回可跟踪和控制进度的作业</span><span class="sxs-lookup"><span data-stu-id="2afac-614">Added -AsJob support for cmdlets, enabling selected cmdlets to execute in the background and return a job to track and control progress</span></span>
    - <span data-ttu-id="2afac-615">向 Get-AzureRmSubscription cmdlet 添加了 -AsJob 参数</span><span class="sxs-lookup"><span data-stu-id="2afac-615">Added -AsJob parameter to Get-AzureRmSubscription cmdlet</span></span>
* <span data-ttu-id="2afac-616">RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="2afac-616">RecoveryServices.Backup</span></span>
  - <span data-ttu-id="2afac-617">修复了 Bug - Get-AzureRmRecoveryServicesBackupItem 应该为容器名称筛选器执行不区分大小写的比较。</span><span class="sxs-lookup"><span data-stu-id="2afac-617">Fixed bug - Get-AzureRmRecoveryServicesBackupItem should do case insensitive comparison for container name filter.</span></span>
  - <span data-ttu-id="2afac-618">修复了 Bug - AzureVmItem 现在有一个可显示上次进行备份操作的时间的属性 - LastBackupTime.</span><span class="sxs-lookup"><span data-stu-id="2afac-618">Fixed bug - AzureVmItem now has a property that shows the last time a backup operation has happened - LastBackupTime.</span></span>
* <span data-ttu-id="2afac-619">资源</span><span class="sxs-lookup"><span data-stu-id="2afac-619">Resources</span></span>
  - <span data-ttu-id="2afac-620">修复了 Get-AzureRMRoleAssignment 所进行的分配没有为自定义角色提供 roledefiniton 名称的问题</span><span class="sxs-lookup"><span data-stu-id="2afac-620">Fixed issue where Get-AzureRMRoleAssignment would result in a assignments without roledefiniton name for custom roles</span></span>
    - <span data-ttu-id="2afac-621">用户现在可以对具有 roledefinition 名称的分配使用 Get-AzureRMRoleAssignment，不管角色类型如何</span><span class="sxs-lookup"><span data-stu-id="2afac-621">Users can now use Get-AzureRMRoleAssignment with assignments having roledefinition names irrespective of the type of role</span></span>
  - <span data-ttu-id="2afac-622">修复了在 assignablescopes 中存在新作用域时使用 Set-AzureRMRoleRoleDefinition 引发“找不到 RD”错误的问题</span><span class="sxs-lookup"><span data-stu-id="2afac-622">Fixed issue where Set-AzureRMRoleRoleDefinition used to throw RD not found error when there was a new scope in assignablescopes</span></span>
    - <span data-ttu-id="2afac-623">用户现在可以将 Set-AzureRMRoleRoleDefinition 与包括新作用域在内的可分配作用域配合使用，不管作用域的位置如何</span><span class="sxs-lookup"><span data-stu-id="2afac-623">Users can now use Set-AzureRMRoleRoleDefinition with assignable scopes including new scopes irrespective of the position of the scope</span></span>
  - <span data-ttu-id="2afac-624">允许作用域以“/”结尾</span><span class="sxs-lookup"><span data-stu-id="2afac-624">Allow scopes to end with "/"</span></span>
    - <span data-ttu-id="2afac-625">用户现在可以使用作用域以“/”结尾的 RoleDefinition 和 RoleAssignment cmdlet，与 API 和 CLI 保持一致</span><span class="sxs-lookup"><span data-stu-id="2afac-625">Users can now use RoleDefinition and RoleAssignment commandlets with scopes ending with "/" ,consistent with API and CLI</span></span>
  - <span data-ttu-id="2afac-626">允许用户使用委派标志创建 RoleAssignment</span><span class="sxs-lookup"><span data-stu-id="2afac-626">Allow users to create RoleAssignment using delegation flag</span></span>
    - <span data-ttu-id="2afac-627">用户现在可以使用 New-AzureRMRoleAssignment，其中的一个选项是添加委派标志</span><span class="sxs-lookup"><span data-stu-id="2afac-627">Users can now use New-AzureRMRoleAssignment with an option of adding the delegation flag</span></span>
  - <span data-ttu-id="2afac-628">修复了可接受作用域参数的 RoleAssignment get 的问题</span><span class="sxs-lookup"><span data-stu-id="2afac-628">Fix RoleAssignment get to respect the scope parameter</span></span>
  - <span data-ttu-id="2afac-629">在 New-AzureRmRoleAssignment cmdlet 中添加了 ServicePrincipalName 的别名</span><span class="sxs-lookup"><span data-stu-id="2afac-629">Add an alias for ServicePrincipalName in the New-AzureRmRoleAssignment Commandlet</span></span>
    - <span data-ttu-id="2afac-630">在使用 New-AzureRmRoleAssignment cmdlet 时，用户现在可以使用 ApplicationId 而非 ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="2afac-630">Users can now use the ApplicationId instead of the ServicePrincipalName when using the New-AzureRmRoleAssignment commandlet</span></span>
* <span data-ttu-id="2afac-631">SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="2afac-631">SiteRecovery</span></span>
  - <span data-ttu-id="2afac-632">在此模块中添加了针对所有 cmdlet 的弃用警告，为下一次发布重大更改做准备。</span><span class="sxs-lookup"><span data-stu-id="2afac-632">Add deprecation warnings for all cmdlets in this module in preparation for the next breaking change release.</span></span>
    - <span data-ttu-id="2afac-633">请参阅即将发布的重大更改指南，详细了解如何从 AzureRM 迁移 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2afac-633">Please see the upcoming breaking changes guide for more information on how to migrate your cmdlets from AzureRM.</span></span>
* <span data-ttu-id="2afac-634">Sql</span><span class="sxs-lookup"><span data-stu-id="2afac-634">Sql</span></span>
  - <span data-ttu-id="2afac-635">添加了使用 Set-AzureRmSqlDatabase 重命名数据库的功能</span><span class="sxs-lookup"><span data-stu-id="2afac-635">Added ability to rename database using Set-AzureRmSqlDatabase</span></span>
  - <span data-ttu-id="2afac-636">修复了问题 https://github.com/Azure/azure-powershell/issues/4974</span><span class="sxs-lookup"><span data-stu-id="2afac-636">Fixed issue https://github.com/Azure/azure-powershell/issues/4974</span></span>
    - <span data-ttu-id="2afac-637">为审核 cmdlet 提供无效的 AUDIT_CHANGED_GROUP 值时，不再引发错误。此项将在即将发布的版本中删除。</span><span class="sxs-lookup"><span data-stu-id="2afac-637">Providing invalid AUDIT_CHANGED_GROUP value for auditing cmdlets no longer throws an error and will be removed in an upcoming release.</span></span>
  - <span data-ttu-id="2afac-638">修复了问题 https://github.com/Azure/azure-powershell/issues/5046</span><span class="sxs-lookup"><span data-stu-id="2afac-638">Fixed issue https://github.com/Azure/azure-powershell/issues/5046</span></span>
    - <span data-ttu-id="2afac-639">不再忽略审核 cmdlet 中的 AuditAction 参数</span><span class="sxs-lookup"><span data-stu-id="2afac-639">AuditAction parameter in auditing cmdlets is no longer being ignored</span></span>
  - <span data-ttu-id="2afac-640">修复了提供的 StorageKeyType 为“Secondary”时审核 cmdlet 中存在的问题</span><span class="sxs-lookup"><span data-stu-id="2afac-640">Fixed an issue in Auditing cmdlets when 'Secondary' StorageKeyType is provided</span></span>
    - <span data-ttu-id="2afac-641">以前在设置 Blob 审核时，如果为 StorageKeyType 参数提供的值为“Secondary”，会使用主存储帐户密钥而非辅助密钥。</span><span class="sxs-lookup"><span data-stu-id="2afac-641">When setting blob auditing, the primary storage account key was used instead of the secondary key when providing 'Secondary' value for StorageKeyType parameter.</span></span>
  - <span data-ttu-id="2afac-642">更改 Set-AzureRmSqlServerTransparentDataEncryptionProtector 中确认消息的措辞</span><span class="sxs-lookup"><span data-stu-id="2afac-642">Changing the wording for confirmation message from Set-AzureRmSqlServerTransparentDataEncryptionProtector</span></span>
* <span data-ttu-id="2afac-643">Azure (RDFE)</span><span class="sxs-lookup"><span data-stu-id="2afac-643">Azure (RDFE)</span></span>
    - <span data-ttu-id="2afac-644">删除了所有 RemoteApp cmdlet</span><span class="sxs-lookup"><span data-stu-id="2afac-644">Removed all RemoteApp Cmdles</span></span>
* <span data-ttu-id="2afac-645">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="2afac-645">Azure.Storage</span></span>
    - <span data-ttu-id="2afac-646">升级到 Azure 存储客户端库 8.6.0 和 Azure 存储 DataMovement 库 0.6.5</span><span class="sxs-lookup"><span data-stu-id="2afac-646">Upgrade to Azure Storage Client Library 8.6.0 and Azure Storage DataMovement Library 0.6.5</span></span>

## <a name="20171110-version-501"></a><span data-ttu-id="2afac-647">2017.11.10 版本 5.0.1</span><span class="sxs-lookup"><span data-stu-id="2afac-647">2017.11.10 Version 5.0.1</span></span>
* <span data-ttu-id="2afac-648">修复了在以下模块中执行时会导致某些 cmdlet 失败的程序集加载问题：</span><span class="sxs-lookup"><span data-stu-id="2afac-648">Fixed assembly loading issue that caused some cmdlets to fail when executing in the following modules:</span></span>
  - <span data-ttu-id="2afac-649">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2afac-649">AzureRM.ApiManagement</span></span>
  - <span data-ttu-id="2afac-650">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="2afac-650">AzureRM.Backup</span></span>
  - <span data-ttu-id="2afac-651">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="2afac-651">AzureRM.Batch</span></span>
  - <span data-ttu-id="2afac-652">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="2afac-652">AzureRM.Compute</span></span>
  - <span data-ttu-id="2afac-653">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="2afac-653">AzureRM.DataFactories</span></span>
  - <span data-ttu-id="2afac-654">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="2afac-654">AzureRM.HDInsight</span></span>
  - <span data-ttu-id="2afac-655">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2afac-655">AzureRM.KeyVault</span></span>
  - <span data-ttu-id="2afac-656">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2afac-656">AzureRM.RecoveryServices</span></span>
  - <span data-ttu-id="2afac-657">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="2afac-657">AzureRM.RecoveryServices.Backup</span></span>
  - <span data-ttu-id="2afac-658">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="2afac-658">AzureRM.RecoveryServices.SiteRecovery</span></span>
  - <span data-ttu-id="2afac-659">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="2afac-659">AzureRM.RedisCache</span></span>
  - <span data-ttu-id="2afac-660">AzureRM.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="2afac-660">AzureRM.SiteRecovery</span></span>
  - <span data-ttu-id="2afac-661">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="2afac-661">AzureRM.Sql</span></span>
  - <span data-ttu-id="2afac-662">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="2afac-662">AzureRM.Storage</span></span>
  - <span data-ttu-id="2afac-663">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="2afac-663">AzureRM.StreamAnalytics</span></span>

## <a name="2017118---version-500"></a><span data-ttu-id="2afac-664">2017.11.8 - 版本 5.0.0</span><span class="sxs-lookup"><span data-stu-id="2afac-664">2017.11.8 - Version 5.0.0</span></span>
* <span data-ttu-id="2afac-665">注意：这是一个有重大更改的版本。</span><span class="sxs-lookup"><span data-stu-id="2afac-665">NOTE: This is a breaking change release.</span></span> <span data-ttu-id="2afac-666">有关引入的重大更改的完整列表，请参阅迁移指南 (https://aka.ms/azps-migration-guide)。</span><span class="sxs-lookup"><span data-stu-id="2afac-666">Please see the migration guide (https://aka.ms/azps-migration-guide) for a full list of introduced breaking changes.</span></span>
* <span data-ttu-id="2afac-667">AzureRM 中的所有 cmdlet 现在支持联机帮助</span><span class="sxs-lookup"><span data-stu-id="2afac-667">All cmdlets in AzureRM now support online help</span></span>
  - <span data-ttu-id="2afac-668">结合 -Online 参数运行 Get-Help 可在默认 Internet 浏览器中打开联机帮助</span><span class="sxs-lookup"><span data-stu-id="2afac-668">Run Get-Help with the -Online parameter to open the online help in your default Internet browser</span></span>
* <span data-ttu-id="2afac-669">AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="2afac-669">AnalysisServices</span></span>
  * <span data-ttu-id="2afac-670">修复了 Synchronize-AzureAsInstance 命令，现在它可以配合新的 AsAzure REST API 进行同步</span><span class="sxs-lookup"><span data-stu-id="2afac-670">Fixed Synchronize-AzureAsInstance command to work with new AsAzure REST API for sync</span></span>
* <span data-ttu-id="2afac-671">ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2afac-671">ApiManagement</span></span>
  * <span data-ttu-id="2afac-672">有关此版本中对 ApiManagement 所做的重大更改，参阅迁移指南</span><span class="sxs-lookup"><span data-stu-id="2afac-672">Please see the migration guide for breaking changes made to ApiManagement this release</span></span>
  * <span data-ttu-id="2afac-673">更新了 Cmdlet Get-AzureRmApiManagementUser 以修复问题 https://github.com/Azure/azure-powershell/issues/4510</span><span class="sxs-lookup"><span data-stu-id="2afac-673">Updated Cmdlet Get-AzureRmApiManagementUser to fix issue https://github.com/Azure/azure-powershell/issues/4510</span></span>
  * <span data-ttu-id="2afac-674">更新了 Cmdlet New-AzureRmApiManagementApi 以创建包含空路径的 API https://github.com/Azure/azure-powershell/issues/4069</span><span class="sxs-lookup"><span data-stu-id="2afac-674">Updated Cmdlet New-AzureRmApiManagementApi to create Api with Empty Path https://github.com/Azure/azure-powershell/issues/4069</span></span>
* <span data-ttu-id="2afac-675">ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="2afac-675">ApplicationInsights</span></span>
  * <span data-ttu-id="2afac-676">添加用于获取/创建/删除 Applicaiton Insights 资源的命令</span><span class="sxs-lookup"><span data-stu-id="2afac-676">Add commands to get/create/remove applicaiton insights resource</span></span>
    - <span data-ttu-id="2afac-677">Get-AzureRmApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="2afac-677">Get-AzureRmApplicationInsights</span></span>
    - <span data-ttu-id="2afac-678">New-AzureRmApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="2afac-678">New-AzureRmApplicationInsights</span></span>
    - <span data-ttu-id="2afac-679">Remove-AzureRmApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="2afac-679">Remove-AzureRmApplicationInsights</span></span>
  * <span data-ttu-id="2afac-680">添加用于获取/更新 Applicaiton Insights 资源定价/每日上限的命令</span><span class="sxs-lookup"><span data-stu-id="2afac-680">Add commands to get/update pricing/daily cap of applicaiton insights resource</span></span>
    - <span data-ttu-id="2afac-681">Get-AzureRmApplicationInsights -IncludeDailyCap</span><span class="sxs-lookup"><span data-stu-id="2afac-681">Get-AzureRmApplicationInsights -IncludeDailyCap</span></span>
    - <span data-ttu-id="2afac-682">Set-AzureRmApplicationInsightsPricingPlan</span><span class="sxs-lookup"><span data-stu-id="2afac-682">Set-AzureRmApplicationInsightsPricingPlan</span></span>
    - <span data-ttu-id="2afac-683">Set-AzureRmApplicationInsightsDailyCap</span><span class="sxs-lookup"><span data-stu-id="2afac-683">Set-AzureRmApplicationInsightsDailyCap</span></span>
  * <span data-ttu-id="2afac-684">添加用于获取/创建/更新/删除 Applicaiton Insights 资源连续导出的命令</span><span class="sxs-lookup"><span data-stu-id="2afac-684">Add commands to get/create/update/remove continuous export of applicaiton insights resource</span></span>
    - <span data-ttu-id="2afac-685">Get-AzureRmApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="2afac-685">Get-AzureRmApplicationInsightsContinuousExport</span></span>
    - <span data-ttu-id="2afac-686">Set-AzureRmApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="2afac-686">Set-AzureRmApplicationInsightsContinuousExport</span></span>
    - <span data-ttu-id="2afac-687">New-AzureRmApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="2afac-687">New-AzureRmApplicationInsightsContinuousExport</span></span>
    - <span data-ttu-id="2afac-688">Remove-AzureRmApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="2afac-688">Remove-AzureRmApplicationInsightsContinuousExport</span></span>
  * <span data-ttu-id="2afac-689">添加用于获取/创建/删除 Applicaiton Insights 资源 API 密钥的命令</span><span class="sxs-lookup"><span data-stu-id="2afac-689">Add commands to get/create/remove api keys of applicaiton insights resoruce</span></span>
    - <span data-ttu-id="2afac-690">Get-AzureRmApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="2afac-690">Get-AzureRmApplicationInsightsApiKey</span></span>
    - <span data-ttu-id="2afac-691">New-AzureRmApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="2afac-691">New-AzureRmApplicationInsightsApiKey</span></span>
    - <span data-ttu-id="2afac-692">Remove-AzureRmApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="2afac-692">Remove-AzureRmApplicationInsightsApiKey</span></span>
* <span data-ttu-id="2afac-693">AzureBatch</span><span class="sxs-lookup"><span data-stu-id="2afac-693">AzureBatch</span></span>
  * <span data-ttu-id="2afac-694">为 `New-AzureRmBatchAccount` 添加了新参数。</span><span class="sxs-lookup"><span data-stu-id="2afac-694">Added new parameters to `New-AzureRmBatchAccount`.</span></span>
    - <span data-ttu-id="2afac-695">`PoolAllocationMode`：用于在 Batch 帐户中创建池的分配模式。</span><span class="sxs-lookup"><span data-stu-id="2afac-695">`PoolAllocationMode`: The allocation mode to use for creating pools in the Batch account.</span></span> <span data-ttu-id="2afac-696">若要创建一个可在用户订阅中分配池节点的 Batch 帐户，请将此参数设置为 `UserSubscription`。</span><span class="sxs-lookup"><span data-stu-id="2afac-696">To create a Batch account which allocates pool nodes in the user's subscription, set this to `UserSubscription`.</span></span>
    - <span data-ttu-id="2afac-697">`KeyVaultId`：与 Batch 帐户关联的 Azure Key Vault 的资源 ID。</span><span class="sxs-lookup"><span data-stu-id="2afac-697">`KeyVaultId`: The resource ID of the Azure key vault associated with the Batch account.</span></span>
    - <span data-ttu-id="2afac-698">`KeyVaultUrl`：与 Batch 帐户关联的 Azure Key Vault 的 URL。</span><span class="sxs-lookup"><span data-stu-id="2afac-698">`KeyVaultUrl`: The URL of the Azure key vault associated with the Batch account.</span></span>
  * <span data-ttu-id="2afac-699">更新了 `New-AzureBatchTask` 的参数。</span><span class="sxs-lookup"><span data-stu-id="2afac-699">Updated parameters to `New-AzureBatchTask`.</span></span>
    - <span data-ttu-id="2afac-700">删除了 `RunElevated` 开关。</span><span class="sxs-lookup"><span data-stu-id="2afac-700">Removed the `RunElevated` switch.</span></span> <span data-ttu-id="2afac-701">已添加 `UserIdentity` 参数来取代 `RunElevated`，可按如下所示，通过构造 `PSUserIdentity` 来实现等效的行为：</span><span class="sxs-lookup"><span data-stu-id="2afac-701">The `UserIdentity` parameter has been added to replace `RunElevated`, and the equivalent behavior can be achieved by constructing a `PSUserIdentity` as shown below:</span></span>
      - <span data-ttu-id="2afac-702">$autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")</span><span class="sxs-lookup"><span data-stu-id="2afac-702">$autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")</span></span>
      - <span data-ttu-id="2afac-703">$userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser</span><span class="sxs-lookup"><span data-stu-id="2afac-703">$userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser</span></span>
    - <span data-ttu-id="2afac-704">添加了 `AuthenticationTokenSettings` 参数。</span><span class="sxs-lookup"><span data-stu-id="2afac-704">Added the `AuthenticationTokenSettings` parameter.</span></span> <span data-ttu-id="2afac-705">使用此参数可以请求 Batch 服务向运行的任务提供身份验证令牌，从而无需向该任务传递 Batch 帐户密钥来向 Batch 服务发出请求。</span><span class="sxs-lookup"><span data-stu-id="2afac-705">This parameter allows you to request the Batch service provide an authentication token to the task when it runs, avoiding the need to pass Batch account keys to the task in order to issue requests to the Batch service.</span></span>
    - <span data-ttu-id="2afac-706">添加了 `ContainerSettings` 参数。</span><span class="sxs-lookup"><span data-stu-id="2afac-706">Added the `ContainerSettings` parameter.</span></span>
      - <span data-ttu-id="2afac-707">使用此参数可以请求 Batch 服务在容器内部运行任务。</span><span class="sxs-lookup"><span data-stu-id="2afac-707">This parameter allows you to request the Batch service run the task inside a container.</span></span>
    - <span data-ttu-id="2afac-708">添加了 `OutputFiles` 参数。</span><span class="sxs-lookup"><span data-stu-id="2afac-708">Added the `OutputFiles` parameter.</span></span>
      - <span data-ttu-id="2afac-709">使用此参数可以配置任务，以便在完成任务之后将文件上传到 Azure 存储。</span><span class="sxs-lookup"><span data-stu-id="2afac-709">This parameter allows you to configure the task to upload files to Azure Storage after it has finished.</span></span>
  * <span data-ttu-id="2afac-710">更新了 `New-AzureBatchPool` 的参数。</span><span class="sxs-lookup"><span data-stu-id="2afac-710">Updated parameters to `New-AzureBatchPool`.</span></span>
    - <span data-ttu-id="2afac-711">添加了 `UserAccounts` 参数。</span><span class="sxs-lookup"><span data-stu-id="2afac-711">Added the `UserAccounts` parameter.</span></span>
      - <span data-ttu-id="2afac-712">此参数定义在池中每个节点上创建的用户帐户。</span><span class="sxs-lookup"><span data-stu-id="2afac-712">This parameter defines user accounts created on each node in the pool.</span></span>
    - <span data-ttu-id="2afac-713">添加了 `TargetLowPriorityComputeNodes`，并已将 `TargetDedicated` 重命名为 `TargetDedicatedComputeNodes`。</span><span class="sxs-lookup"><span data-stu-id="2afac-713">Added `TargetLowPriorityComputeNodes` and renamed `TargetDedicated` to `TargetDedicatedComputeNodes`.</span></span>
      - <span data-ttu-id="2afac-714">为 `TargetDedicatedComputeNodes` 参数创建了 `TargetDedicated` 别名。</span><span class="sxs-lookup"><span data-stu-id="2afac-714">A `TargetDedicated` alias was created for the `TargetDedicatedComputeNodes` parameter.</span></span>
    - <span data-ttu-id="2afac-715">添加了 `NetworkConfiguration` 参数。</span><span class="sxs-lookup"><span data-stu-id="2afac-715">Added the `NetworkConfiguration` parameter.</span></span>
      - <span data-ttu-id="2afac-716">使用此参数可以配置池的网络设置。</span><span class="sxs-lookup"><span data-stu-id="2afac-716">This parameter allows you to configure the pools network settings.</span></span>
  * <span data-ttu-id="2afac-717">更新了 `New-AzureBatchCertificate` 的参数。</span><span class="sxs-lookup"><span data-stu-id="2afac-717">Updated parameters to `New-AzureBatchCertificate`.</span></span>
    - <span data-ttu-id="2afac-718">`Password` 参数现在是 `SecureString`。</span><span class="sxs-lookup"><span data-stu-id="2afac-718">The `Password` parameter is now a `SecureString`.</span></span>
  * <span data-ttu-id="2afac-719">更新了 `New-AzureBatchComputeNodeUser` 的参数。</span><span class="sxs-lookup"><span data-stu-id="2afac-719">Updated parameters to `New-AzureBatchComputeNodeUser`.</span></span>
    - <span data-ttu-id="2afac-720">`Password` 参数现在是 `SecureString`。</span><span class="sxs-lookup"><span data-stu-id="2afac-720">The `Password` parameter is now a `SecureString`.</span></span>
  * <span data-ttu-id="2afac-721">更新了 `Set-AzureBatchComputeNodeUser` 的参数。</span><span class="sxs-lookup"><span data-stu-id="2afac-721">Updated parameters to `Set-AzureBatchComputeNodeUser`.</span></span>
    - <span data-ttu-id="2afac-722">`Password` 参数现在是 `SecureString`。</span><span class="sxs-lookup"><span data-stu-id="2afac-722">The `Password` parameter is now a `SecureString`.</span></span>
  * <span data-ttu-id="2afac-723">已将 `Get-AzureBatchNodeFile`、`Get-AzureBatchNodeFileContent` 和 `Remove-AzureBatchNodeFile` 的 `Name` 参数重命名为 `Path`。</span><span class="sxs-lookup"><span data-stu-id="2afac-723">Renamed the `Name` parameter to `Path` on `Get-AzureBatchNodeFile`, `Get-AzureBatchNodeFileContent`, and `Remove-AzureBatchNodeFile`.</span></span>
    - <span data-ttu-id="2afac-724">为 `Path` 参数创建了 `Name` 别名。</span><span class="sxs-lookup"><span data-stu-id="2afac-724">A `Name` alias was created for the `Path` parameter.</span></span>
  * <span data-ttu-id="2afac-725">对象更改</span><span class="sxs-lookup"><span data-stu-id="2afac-725">Changes to objects</span></span>
    - <span data-ttu-id="2afac-726">有关完整列表，参阅 Batch 更改日志</span><span class="sxs-lookup"><span data-stu-id="2afac-726">Please see the Batch change log for the full list</span></span>
  * <span data-ttu-id="2afac-727">添加了对基于 Azure Active Directory 的身份验证的支持。</span><span class="sxs-lookup"><span data-stu-id="2afac-727">Added support for Azure Active Directory based authentication.</span></span>
    - <span data-ttu-id="2afac-728">若要使用 Azure Active Directory 身份验证，请使用 `Get-AzureRmBatchAccount` cmdlet 检索 `BatchAccountContext` 对象，并将此 `BatchAccountContext` 提供给 Batch 服务 cmdlet 的 `-BatchContext` 参数。</span><span class="sxs-lookup"><span data-stu-id="2afac-728">To use Azure Active Directory authentication, retrieve a `BatchAccountContext` object using the `Get-AzureRmBatchAccount` cmdlet, and supply this `BatchAccountContext` to the `-BatchContext` parameter of a Batch service cmdlet.</span></span> <span data-ttu-id="2afac-729">采用 `PoolAllocationMode = UserSubscription` 设置的帐户必须使用 Azure Active Directory 身份验证。</span><span class="sxs-lookup"><span data-stu-id="2afac-729">Azure Active Directory authentication is mandatory for accounts with `PoolAllocationMode = UserSubscription`.</span></span>
    - <span data-ttu-id="2afac-730">对于现有帐户或使用 `PoolAllocationMode = BatchService` 创建的新帐户，可通过使用 `Get-AzureRmBatchAccoutKeys` cmdlet 检索 `BatchAccountContext` 对象，来继续使用共享密钥身份验证。</span><span class="sxs-lookup"><span data-stu-id="2afac-730">For existing accounts or for new accounts created with `PoolAllocationMode = BatchService`, you may continue to use shared key authentication by retrieving a `BatchAccountContext` object using the `Get-AzureRmBatchAccoutKeys` cmdlet.</span></span>
* <span data-ttu-id="2afac-731">计算</span><span class="sxs-lookup"><span data-stu-id="2afac-731">Compute</span></span>
  * <span data-ttu-id="2afac-732">Azure 磁盘加密扩展命令</span><span class="sxs-lookup"><span data-stu-id="2afac-732">Azure Disk Encryption Extension Commands</span></span>
    - <span data-ttu-id="2afac-733">“Set-AzureRmVmDiskEncryptionExtension”的新参数“-EncryptFormatAll”可以加密形式格式化数据磁盘</span><span class="sxs-lookup"><span data-stu-id="2afac-733">New Parameter for 'Set-AzureRmVmDiskEncryptionExtension': '-EncryptFormatAll' encrypt formats data disks</span></span>
    - <span data-ttu-id="2afac-734">“Set-AzureRmVmDiskEncryptionExtension”的新参数“-ExtensionPublisherName”和“-ExtensionType”可用于切换到扩展的其他版本</span><span class="sxs-lookup"><span data-stu-id="2afac-734">New Parameters for 'Set-AzureRmVmDiskEncryptionExtension': '-ExtensionPublisherName' and '-ExtensionType' allow switching to other versions of the extension</span></span>
    - <span data-ttu-id="2afac-735">“Disable-AzureRmVmDiskEncryption”的新参数“-ExtensionPublisherName”和“-ExtensionType”可用于切换到扩展的其他版本</span><span class="sxs-lookup"><span data-stu-id="2afac-735">New Parameters for 'Disable-AzureRmVmDiskEncryption': '-ExtensionPublisherName' and '-ExtensionType' allow switching to other versions of the extension</span></span>
    - <span data-ttu-id="2afac-736">“Get-AzureRmVmDiskEncryptionStatus”的新参数“-ExtensionPublisherName”和“-ExtensionType”可用于切换到扩展的其他版本</span><span class="sxs-lookup"><span data-stu-id="2afac-736">New Parameters for 'Get-AzureRmVmDiskEncryptionStatus': '-ExtensionPublisherName' and '-ExtensionType' allow switching to other versions of the extension</span></span>
* <span data-ttu-id="2afac-737">DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="2afac-737">DataLakeAnalytics</span></span>
  * <span data-ttu-id="2afac-738">有关此版本中对 DataLakeAnalytics 所做的重大更改，参阅迁移指南</span><span class="sxs-lookup"><span data-stu-id="2afac-738">Please see the migration guide for breaking changes made to DataLakeAnalytics this release</span></span>
  * <span data-ttu-id="2afac-739">更改了 Get-AzureRmDataLakeAnalyticsAccount 的两个 OutputType 中的一个</span><span class="sxs-lookup"><span data-stu-id="2afac-739">Changed one of the two OutputTypes of Get-AzureRmDataLakeAnalyticsAccount</span></span>
    - <span data-ttu-id="2afac-740">List\<DataLakeAnalyticsAccount> 已更改为 List\<PSDataLakeAnalyticsAccountBasic></span><span class="sxs-lookup"><span data-stu-id="2afac-740">List\<DataLakeAnalyticsAccount> to List\<PSDataLakeAnalyticsAccountBasic></span></span>
    - <span data-ttu-id="2afac-741">PSDataLakeAnalyticsAccountBasic 的属性是 DataLakeAnalyticsAccount 的属性的严格子集</span><span class="sxs-lookup"><span data-stu-id="2afac-741">The properties of PSDataLakeAnalyticsAccountBasic is a strict subset of the properties of DataLakeAnalyticsAccount</span></span>
    - <span data-ttu-id="2afac-742">DataLakeAnalyticsAccount 中的附加属性不会由服务返回。</span><span class="sxs-lookup"><span data-stu-id="2afac-742">The additional properties that are in DataLakeAnalyticsAccount are not returned by the service.</span></span>  <span data-ttu-id="2afac-743">因此，此项更改旨在准确反映这种情况。</span><span class="sxs-lookup"><span data-stu-id="2afac-743">Therefore, this change is to reflect this accurately.</span></span> <span data-ttu-id="2afac-744">这些附加属性仍在 PSDataLakeAnalyticsAccountBasic 中，但已标记为“已过时”。</span><span class="sxs-lookup"><span data-stu-id="2afac-744">These additional properties are still in PSDataLakeAnalyticsAccountBasic, but they are tagged as Obsolete.</span></span>
  * <span data-ttu-id="2afac-745">更改了 Get-AzureRmDataLakeAnalyticsJob 的两个 OutputType 中的一个</span><span class="sxs-lookup"><span data-stu-id="2afac-745">Changed one of the two OutputTypes of Get-AzureRmDataLakeAnalyticsJob</span></span>
    - <span data-ttu-id="2afac-746">List\<JobInformation> 已更改为 List\<PSJobInformationBasic></span><span class="sxs-lookup"><span data-stu-id="2afac-746">List\<JobInformation> to List\<PSJobInformationBasic></span></span>
    - <span data-ttu-id="2afac-747">PSJobInformationBasic 的属性是 JobInformation 的属性的严格子集</span><span class="sxs-lookup"><span data-stu-id="2afac-747">The properties of PSJobInformationBasic is a strict subset of the properties of JobInformation</span></span>
    - <span data-ttu-id="2afac-748">JobInformation 中的附加属性不会由服务返回。</span><span class="sxs-lookup"><span data-stu-id="2afac-748">The additional properties that are in JobInformation are not returned by the service.</span></span>  <span data-ttu-id="2afac-749">因此，此项更改旨在准确反映这种情况。</span><span class="sxs-lookup"><span data-stu-id="2afac-749">Therefore, this change is to reflect this accurately.</span></span> <span data-ttu-id="2afac-750">这些附加属性仍在 PSJobInformationBasic 中，但已标记为“已过时”。</span><span class="sxs-lookup"><span data-stu-id="2afac-750">These additional properties are still in PSJobInformationBasic, but they are tagged as Obsolete.</span></span>
* <span data-ttu-id="2afac-751">DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2afac-751">DataLakeStore</span></span>
  * <span data-ttu-id="2afac-752">有关此版本中对 DataLakeStore 所做的重大更改，参阅迁移指南</span><span class="sxs-lookup"><span data-stu-id="2afac-752">Please see the migration guide for breaking changes made to DataLakeStore this release</span></span>
  * <span data-ttu-id="2afac-753">更改了 Get-AzureRmDataLakeStoreAccount 的两个 OutputType 中的一个</span><span class="sxs-lookup"><span data-stu-id="2afac-753">Changed one of the two OutputTypes of Get-AzureRmDataLakeStoreAccount</span></span>
    - <span data-ttu-id="2afac-754">List\<PSDataLakeStoreAccount> 已更改为 List\<PSDataLakeStoreAccountBasic></span><span class="sxs-lookup"><span data-stu-id="2afac-754">List\<PSDataLakeStoreAccount> to List\<PSDataLakeStoreAccountBasic></span></span>
    - <span data-ttu-id="2afac-755">PSDataLakeStoreAccountBasic 的属性是 PSDataLakeStoreAccount 的属性的严格子集</span><span class="sxs-lookup"><span data-stu-id="2afac-755">The properties of PSDataLakeStoreAccountBasic is a strict subset of the properties of PSDataLakeStoreAccount</span></span>
    - <span data-ttu-id="2afac-756">PSDataLakeStoreAccount 中的附加属性不会由服务返回。</span><span class="sxs-lookup"><span data-stu-id="2afac-756">The additional properties that are in PSDataLakeStoreAccount are not returned by the service.</span></span>  <span data-ttu-id="2afac-757">因此，此项更改旨在准确反映这种情况。</span><span class="sxs-lookup"><span data-stu-id="2afac-757">Therefore, this change is to reflect this accurately.</span></span> <span data-ttu-id="2afac-758">这些附加属性仍在 PSDataLakeStoreAccountBasic 中，但已标记为“已过时”。</span><span class="sxs-lookup"><span data-stu-id="2afac-758">These additional properties are still in PSDataLakeStoreAccountBasic, but they are tagged as Obsolete.</span></span>
* <span data-ttu-id="2afac-759">Dns</span><span class="sxs-lookup"><span data-stu-id="2afac-759">Dns</span></span>
  * <span data-ttu-id="2afac-760">对 Azure DNS 中 CAA 记录类型的支持</span><span class="sxs-lookup"><span data-stu-id="2afac-760">Support for CAA record types in Azure DNS</span></span>
    - <span data-ttu-id="2afac-761">支持对 CAA 记录类型执行所有操作</span><span class="sxs-lookup"><span data-stu-id="2afac-761">Supports all operations on CAA record type</span></span>
* <span data-ttu-id="2afac-762">EventHub</span><span class="sxs-lookup"><span data-stu-id="2afac-762">EventHub</span></span>
  * <span data-ttu-id="2afac-763">有关此版本中对 EventHub 所做的重大更改，参阅迁移指南</span><span class="sxs-lookup"><span data-stu-id="2afac-763">Please see the migration guide for breaking changes made to EventHub this release</span></span>
* <span data-ttu-id="2afac-764">洞察力</span><span class="sxs-lookup"><span data-stu-id="2afac-764">Insights</span></span>
  * <span data-ttu-id="2afac-765">有关此版本中对 Insights 所做的重大更改，参阅迁移指南</span><span class="sxs-lookup"><span data-stu-id="2afac-765">Please see the migration guide for breaking changes made to Insights this release</span></span>
* <span data-ttu-id="2afac-766">网络</span><span class="sxs-lookup"><span data-stu-id="2afac-766">Network</span></span>
  * <span data-ttu-id="2afac-767">有关此版本中对 Network 所做的重大更改，参阅迁移指南</span><span class="sxs-lookup"><span data-stu-id="2afac-767">Please see the migration guide for breaking changes made to Network this release</span></span>
  * <span data-ttu-id="2afac-768">添加了 cmdlet 用于列出指定 Azure 区域的可用 Internet 服务提供商</span><span class="sxs-lookup"><span data-stu-id="2afac-768">Added cmdlet to list available internet service providers for a specified Azure region</span></span>
    - <span data-ttu-id="2afac-769">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="2afac-769">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>
  * <span data-ttu-id="2afac-770">添加了 cmdlet 用于获取 Internet 服务提供商从指定位置到 Azure 区域的相对延迟评分</span><span class="sxs-lookup"><span data-stu-id="2afac-770">Added cmdlet to get the relative latency score for internet service providers from a specified location to Azure regions</span></span>
    - <span data-ttu-id="2afac-771">Get-AzureRmNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="2afac-771">Get-AzureRmNetworkWatcherReachabilityReport</span></span>
* <span data-ttu-id="2afac-772">配置文件</span><span class="sxs-lookup"><span data-stu-id="2afac-772">Profile</span></span>
  - <span data-ttu-id="2afac-773">Set-AzureRmDefault</span><span class="sxs-lookup"><span data-stu-id="2afac-773">Set-AzureRmDefault</span></span>
    - <span data-ttu-id="2afac-774">使用此 cmdlet 可设置默认资源组。</span><span class="sxs-lookup"><span data-stu-id="2afac-774">Use this cmdlet to set a default resource group.</span></span>  <span data-ttu-id="2afac-775">因此，对于某些 cmdlet 可以选择性地使用 -ResourceGroup 参数；如果未指定资源组，将使用默认值</span><span class="sxs-lookup"><span data-stu-id="2afac-775">This will make the -ResourceGroup parameter optional for some cmdlets, and will use the default when a resource group is not specified</span></span>
    - ```Set-AzureRmDefault -ResourceGroupName "ExampleResourceGroup"```
    - <span data-ttu-id="2afac-776">如果订阅中存在指定的资源组，此资源组将设置为默认值。</span><span class="sxs-lookup"><span data-stu-id="2afac-776">If resource group specified exists in the subscription, this resource group will be set to default.</span></span>  <span data-ttu-id="2afac-777">否则，将创建资源组并将其设置为默认值。</span><span class="sxs-lookup"><span data-stu-id="2afac-777">Otherwise, the resource group will be created and then set to default.</span></span>
  - <span data-ttu-id="2afac-778">Get-AzureRmDefault</span><span class="sxs-lookup"><span data-stu-id="2afac-778">Get-AzureRmDefault</span></span>
    - <span data-ttu-id="2afac-779">使用此 cmdlet 可获取当前的默认资源组（和将来的其他默认资源组）。</span><span class="sxs-lookup"><span data-stu-id="2afac-779">Use this cmdlet to get the current default resource group (and other defaults in the future).</span></span>
    - ```Get-AzureRmDefault -ResourceGroup```
  - <span data-ttu-id="2afac-780">Clear-AzureRmDefault</span><span class="sxs-lookup"><span data-stu-id="2afac-780">Clear-AzureRmDefault</span></span>
    - <span data-ttu-id="2afac-781">使用此 cmdlet 可删除当前的默认资源组</span><span class="sxs-lookup"><span data-stu-id="2afac-781">Use this cmdlet to remove the current default resource group</span></span>
    - ```Clear-AzureRmDefault -ResourceGroup```
  - <span data-ttu-id="2afac-782">Add-AzureRmEnvironment 和 Set-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="2afac-782">Add-AzureRmEnvironment and Set-AzureRmEnvironment</span></span>
    - <span data-ttu-id="2afac-783">添加 BatchAudience 参数，以便指定在获取 Batch 服务的身份验证令牌时要使用的 Azure Batch Active Directory 受众。</span><span class="sxs-lookup"><span data-stu-id="2afac-783">Add the BatchAudience parameter, which allows you to specify the Azure Batch Active Directory audience to use when acquiring authentication tokens for the Batch service.</span></span>
* <span data-ttu-id="2afac-784">RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="2afac-784">RecoveryServices.Backup</span></span>
  * <span data-ttu-id="2afac-785">添加了 cmdlet 用于执行即时文件恢复。</span><span class="sxs-lookup"><span data-stu-id="2afac-785">Added cmdlets to perform instant file recovery.</span></span>
    - <span data-ttu-id="2afac-786">Get-AzureRmRecoveryServicesBackupRPMountScript</span><span class="sxs-lookup"><span data-stu-id="2afac-786">Get-AzureRmRecoveryServicesBackupRPMountScript</span></span>
    - <span data-ttu-id="2afac-787">Disable-AzureRmRecoveryServicesBackupRPMountScript</span><span class="sxs-lookup"><span data-stu-id="2afac-787">Disable-AzureRmRecoveryServicesBackupRPMountScript</span></span>
  * <span data-ttu-id="2afac-788">已 RecoveryServices.Backup SDK 版本更新到最新版</span><span class="sxs-lookup"><span data-stu-id="2afac-788">Updated RecoveryServices.Backup SDK version to the latest</span></span>
  * <span data-ttu-id="2afac-789">更新了 Azure VM 工作负荷的测试，以便测试运行所需的所有设置由测试本身完成。</span><span class="sxs-lookup"><span data-stu-id="2afac-789">Updated tests for the Azure VM workload so that, all setups needed for test runs are done by the tests themselves.</span></span>
  * <span data-ttu-id="2afac-790">修复 https://github.com/Azure/azure-powershell/issues/3164</span><span class="sxs-lookup"><span data-stu-id="2afac-790">Fixes https://github.com/Azure/azure-powershell/issues/3164</span></span>
* <span data-ttu-id="2afac-791">RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="2afac-791">RecoveryServices.SiteRecovery</span></span>
  * <span data-ttu-id="2afac-792">对 ASR VMware 到 Azure Site Recovery 的迁移所做的更改（cmdlet 目前支持企业到企业、企业到 Azure 以及 HyperV 到 Azure 的操作）</span><span class="sxs-lookup"><span data-stu-id="2afac-792">Changes for ASR VMware to Azure Site Recovery (cmdlets are currently supporting operations for Enterprise to Enterprise, Enterprise to Azure, HyperV to Azure)</span></span>
    - <span data-ttu-id="2afac-793">New-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="2afac-793">New-AzureRmRecoveryServicesAsrPolicy</span></span>
    - <span data-ttu-id="2afac-794">New-AzureRmRecoveryServicesAsrProtectedItem</span><span class="sxs-lookup"><span data-stu-id="2afac-794">New-AzureRmRecoveryServicesAsrProtectedItem</span></span>
    - <span data-ttu-id="2afac-795">Update-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="2afac-795">Update-AzureRmRecoveryServicesAsrPolicy</span></span>
    - <span data-ttu-id="2afac-796">Update-AzureRmRecoveryServicesAsrProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="2afac-796">Update-AzureRmRecoveryServicesAsrProtectionDirection</span></span>
  * <span data-ttu-id="2afac-797">添加了对基于 AAD 的保管库的支持</span><span class="sxs-lookup"><span data-stu-id="2afac-797">Added support to AAD-based vault</span></span>
  * <span data-ttu-id="2afac-798">添加了 cmdlet 用于管理 VCenter 资源</span><span class="sxs-lookup"><span data-stu-id="2afac-798">Added cmdlets to manage VCenter resources</span></span>
    - <span data-ttu-id="2afac-799">Get-AzureRmRecoveryServicesAsrVCenter</span><span class="sxs-lookup"><span data-stu-id="2afac-799">Get-AzureRmRecoveryServicesAsrVCenter</span></span>
    - <span data-ttu-id="2afac-800">New-AzureRmRecoveryServicesAsrVCenter</span><span class="sxs-lookup"><span data-stu-id="2afac-800">New-AzureRmRecoveryServicesAsrVCenter</span></span>
    - <span data-ttu-id="2afac-801">Remove-AzureRmRecoveryServicesAsrVCenter</span><span class="sxs-lookup"><span data-stu-id="2afac-801">Remove-AzureRmRecoveryServicesAsrVCenter</span></span>
    - <span data-ttu-id="2afac-802">Update-AzureRmRecoveryServicesAsrVCenter</span><span class="sxs-lookup"><span data-stu-id="2afac-802">Update-AzureRmRecoveryServicesAsrVCenter</span></span>
  * <span data-ttu-id="2afac-803">添加了其他 cmdlet</span><span class="sxs-lookup"><span data-stu-id="2afac-803">Added other cmdlets</span></span>
    - <span data-ttu-id="2afac-804">Get-AzureRmRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="2afac-804">Get-AzureRmRecoveryServicesAsrAlertSetting</span></span>
    - <span data-ttu-id="2afac-805">Get-AzureRmRecoveryServicesAsrEvent</span><span class="sxs-lookup"><span data-stu-id="2afac-805">Get-AzureRmRecoveryServicesAsrEvent</span></span>
    - <span data-ttu-id="2afac-806">New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="2afac-806">New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
    - <span data-ttu-id="2afac-807">Set-AzureRmRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="2afac-807">Set-AzureRmRecoveryServicesAsrAlertSetting</span></span>
    - <span data-ttu-id="2afac-808">Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob</span><span class="sxs-lookup"><span data-stu-id="2afac-808">Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob</span></span>
    - <span data-ttu-id="2afac-809">Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob</span><span class="sxs-lookup"><span data-stu-id="2afac-809">Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob</span></span>
    - <span data-ttu-id="2afac-810">Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob</span><span class="sxs-lookup"><span data-stu-id="2afac-810">Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob</span></span>
    - <span data-ttu-id="2afac-811">Update-AzureRmRecoveryServicesAsrMobilityService</span><span class="sxs-lookup"><span data-stu-id="2afac-811">Update-AzureRmRecoveryServicesAsrMobilityService</span></span>
* <span data-ttu-id="2afac-812">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2afac-812">ServiceBus</span></span>
  - <span data-ttu-id="2afac-813">有关此版本中对 ServiceBus 所做的重大更改，参阅迁移指南</span><span class="sxs-lookup"><span data-stu-id="2afac-813">Please see the migration guide for breaking changes made to ServiceBus this release</span></span>
* <span data-ttu-id="2afac-814">Sql</span><span class="sxs-lookup"><span data-stu-id="2afac-814">Sql</span></span>
  * <span data-ttu-id="2afac-815">添加列出和取消对数据库执行的异步 updateslo 操作的支持</span><span class="sxs-lookup"><span data-stu-id="2afac-815">Adding support for list and cancel the asynchronous updateslo operation on the database</span></span>
    - <span data-ttu-id="2afac-816">更新现有的 cmdlet Get-AzureRmSqlDatabaseActivity 以返回 DB updateslo 操作状态。</span><span class="sxs-lookup"><span data-stu-id="2afac-816">update existing cmdlet Get-AzureRmSqlDatabaseActivity to return DB updateslo operation status.</span></span>
    - <span data-ttu-id="2afac-817">添加新的 cmdlet Stop-AzureRmSqlDatabaseActivity，以取消对数据库执行的 updateslo 异步操作。</span><span class="sxs-lookup"><span data-stu-id="2afac-817">add new cmdlet Stop-AzureRmSqlDatabaseActivity for cancel the asynchronous updateslo operation on the database.</span></span>
  * <span data-ttu-id="2afac-818">添加数据库和弹性池区域冗余的支持</span><span class="sxs-lookup"><span data-stu-id="2afac-818">Adding support for Zone Redundancy for databases and elastic pools</span></span>
    - <span data-ttu-id="2afac-819">添加 New-AzureRmSqlDatabase 的 ZoneRedundant 开关参数</span><span class="sxs-lookup"><span data-stu-id="2afac-819">Adding ZoneRedundant switch parameter to New-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="2afac-820">添加 Set-AzureRmSqlDatabase 的 ZoneRedundant 开关参数</span><span class="sxs-lookup"><span data-stu-id="2afac-820">Adding ZoneRedundant switch parameter to Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="2afac-821">添加 New-AzureRmSqlElasticPool 的 ZoneRedundant 开关参数</span><span class="sxs-lookup"><span data-stu-id="2afac-821">Adding ZoneRedundant switch parameter to New-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="2afac-822">添加 Set-AzureRmSqlElasticPool 的 ZoneRedundant 开关参数</span><span class="sxs-lookup"><span data-stu-id="2afac-822">Adding ZoneRedundant switch parameter to Set-AzureRmSqlElasticPool</span></span>
  * <span data-ttu-id="2afac-823">添加对服务器 DNS 别名的支持</span><span class="sxs-lookup"><span data-stu-id="2afac-823">Adding support for Server DNS Aliases</span></span>
    - <span data-ttu-id="2afac-824">添加 Get-AzureRmSqlServerDnsAlias cmdlet，用于根据服务器和别名获取服务器 DNS 别名，或 Azure SQL Server 的一系列服务器 DNS 别名。</span><span class="sxs-lookup"><span data-stu-id="2afac-824">Adding Get-AzureRmSqlServerDnsAlias cmdlet which gets server dns aliases by server and alias name or a list of server dns aliases for an azure Sql Server.</span></span>
    - <span data-ttu-id="2afac-825">添加 New-AzureRmSqlServerDnsAlias cmdlet，用于新建给定 Azure SQL Server 的服务器 DNS 别名</span><span class="sxs-lookup"><span data-stu-id="2afac-825">Adding New-AzureRmSqlServerDnsAlias cmdlet which creates new server dns alias for a given Azure Sql server</span></span>
    - <span data-ttu-id="2afac-826">添加 Set-AzurermSqlServerDnsAlias cmlet，用于更新服务器 DNS 别名所指向的 Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="2afac-826">Adding Set-AzurermSqlServerDnsAlias cmlet which allows updating a Azure Sql Server to which server dns alias is pointing</span></span>
    - <span data-ttu-id="2afac-827">添加 Remove-AzureRmSqlServerDnsAlias cmdlet，用于删除 Azure SQL Server 的服务器 DNS 别名</span><span class="sxs-lookup"><span data-stu-id="2afac-827">Adding Remove-AzureRmSqlServerDnsAlias cmdlet which removes a server dns alias for a Azure Sql Server</span></span>
* <span data-ttu-id="2afac-828">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="2afac-828">Azure.Storage</span></span>
  * <span data-ttu-id="2afac-829">升级到 Azure 存储客户端库 8.5.0 和 Azure 存储 DataMovement 库 0.6.3</span><span class="sxs-lookup"><span data-stu-id="2afac-829">Upgrade to Azure Storage Client Library 8.5.0 and Azure Storage DataMovement Library 0.6.3</span></span>
  * <span data-ttu-id="2afac-830">添加文件共享支持快照</span><span class="sxs-lookup"><span data-stu-id="2afac-830">Add File Share Snapshot Support Feature</span></span>
    - <span data-ttu-id="2afac-831">为 Get-AzureStorageShare 添加“SnapshotTime”参数</span><span class="sxs-lookup"><span data-stu-id="2afac-831">Add 'SnapshotTime' parameter to Get-AzureStorageShare</span></span>
    - <span data-ttu-id="2afac-832">为 Remove-AzureStorageShare 添加“IncludeAllSnapshot”参数</span><span class="sxs-lookup"><span data-stu-id="2afac-832">Add 'IncludeAllSnapshot' parameter to Remove-AzureStorageShare</span></span>
