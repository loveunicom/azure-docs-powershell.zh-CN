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
ms.openlocfilehash: 3961f5c37869d0dc877b85bad535f399181040db
ms.sourcegitcommit: fd11600079ee3844986552bccc4e274a231332b6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/02/2018
ms.locfileid: "39368171"
---
# <a name="release-notes"></a><span data-ttu-id="93e86-103">发行说明</span><span class="sxs-lookup"><span data-stu-id="93e86-103">Release notes</span></span>

<span data-ttu-id="93e86-104">下面是此版本中对 Azure PowerShell 所做的更改列表。</span><span class="sxs-lookup"><span data-stu-id="93e86-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="660---july-2018"></a><span data-ttu-id="93e86-105">6.6.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="93e86-105">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="93e86-106">常规</span><span class="sxs-lookup"><span data-stu-id="93e86-106">General</span></span>
* <span data-ttu-id="93e86-107">更新了所有帮助文件，以包括完整参数类型和正确的输入/输出类型。</span><span class="sxs-lookup"><span data-stu-id="93e86-107">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="93e86-108">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="93e86-108">AzureRM.Profile</span></span>
* <span data-ttu-id="93e86-109">更新了 Common.Strategy 库，以便能够验证资源的当前配置是否与目标资源兼容。</span><span class="sxs-lookup"><span data-stu-id="93e86-109">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span> <span data-ttu-id="93e86-110">默认值始终为 true，单个资源并覆盖默认值。</span><span class="sxs-lookup"><span data-stu-id="93e86-110">Default is always true, individual resources and overridet the default.</span></span>
* <span data-ttu-id="93e86-111">在 Common.Storage 中添加了 ps1xml 类型</span><span class="sxs-lookup"><span data-stu-id="93e86-111">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="93e86-112">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="93e86-112">Azure.Storage</span></span>
* <span data-ttu-id="93e86-113">支持从 DefaulfProfile 获取存储上下文</span><span class="sxs-lookup"><span data-stu-id="93e86-113">Support get Storage Context from DefaulfProfile</span></span>
* <span data-ttu-id="93e86-114">将 Ps1XmlAttribute 添加到 cmdlet 输出类型属性。</span><span class="sxs-lookup"><span data-stu-id="93e86-114">Add Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="93e86-115">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="93e86-115">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="93e86-116">修复了问题 https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="93e86-116">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="93e86-117">修复了 Automapper 中将 PsApiManagementApi 转换为 ApiContract 的 bug</span><span class="sxs-lookup"><span data-stu-id="93e86-117">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="93e86-118">修复了问题 https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="93e86-118">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="93e86-119">修复了 File.Save 中没有使用编码类型重载的 bug</span><span class="sxs-lookup"><span data-stu-id="93e86-119">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="93e86-120">修复了问题 https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="93e86-120">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="93e86-121">升级到了 4.0.3 Nuget版本，该版本修复了 apiId 上的模式异常</span><span class="sxs-lookup"><span data-stu-id="93e86-121">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="93e86-122">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="93e86-122">AzureRM.Compute</span></span>
* <span data-ttu-id="93e86-123">修复因使用 PremiumLRS 存储帐户类型重命名而在 New-AzureRmVm 中使用 DiskFileParameterSet 创建 VM 失败的问题。</span><span class="sxs-lookup"><span data-stu-id="93e86-123">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="93e86-124">修复 Invoke-AzureRmVMRunCommand cmdlet</span><span class="sxs-lookup"><span data-stu-id="93e86-124">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="93e86-125">更新 Get-AzureRmAvailabilitySet 以启用列出订阅中的所有可用性集。</span><span class="sxs-lookup"><span data-stu-id="93e86-125">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="93e86-126">（ResouceGroupName 参数现在是可选的。）</span><span class="sxs-lookup"><span data-stu-id="93e86-126">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="93e86-127">更新“New-AzureRmVm”的 SimpleParameterSet 以在符合条件的 VM 上启用加速网络。</span><span class="sxs-lookup"><span data-stu-id="93e86-127">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="93e86-128">将 New-AzureRmVmss 简单参数集更新为在用户指定的 LB 已存在时创建 vmss 失败。</span><span class="sxs-lookup"><span data-stu-id="93e86-128">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="93e86-129">更新 New-AzureRmDisk 的示例</span><span class="sxs-lookup"><span data-stu-id="93e86-129">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="93e86-130">添加“New-AzureRmVM”的示例</span><span class="sxs-lookup"><span data-stu-id="93e86-130">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="93e86-131">更新 Set-AzureRmVMOSDisk 的说明</span><span class="sxs-lookup"><span data-stu-id="93e86-131">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="93e86-132">更新 Set-AzureRmVMBginfoExtension 的示例 1 以更正拼写和前缀。</span><span class="sxs-lookup"><span data-stu-id="93e86-132">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="93e86-133">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="93e86-133">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="93e86-134">将 ADF .Net SDK 版本更新为 1.1.0。</span><span class="sxs-lookup"><span data-stu-id="93e86-134">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="93e86-135">支持跨数据工厂的自承载集成运行时共享。</span><span class="sxs-lookup"><span data-stu-id="93e86-135">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="93e86-136">将新参数 -SharedIntegrationRuntimeResourceId 添加到 Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet。</span><span class="sxs-lookup"><span data-stu-id="93e86-136">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="93e86-137">将新的可选参数 -LinkedDataFactoryName 添加到 Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet。</span><span class="sxs-lookup"><span data-stu-id="93e86-137">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="93e86-138">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="93e86-138">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="93e86-139">将数据平面 SDK (Microsoft.Azure.DataLake.Store) 版本更新为 1.1.9</span><span class="sxs-lookup"><span data-stu-id="93e86-139">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="93e86-140">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="93e86-140">AzureRM.EventHub</span></span>
* <span data-ttu-id="93e86-141">在删除 cmdlet 中更新了 InputObject 和 ResourceId 的管道</span><span class="sxs-lookup"><span data-stu-id="93e86-141">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="93e86-142">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="93e86-142">AzureRM.Insights</span></span>
* <span data-ttu-id="93e86-143">修复了帮助文件中 OutputType 的格式问题</span><span class="sxs-lookup"><span data-stu-id="93e86-143">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="93e86-144">使用 Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span><span class="sxs-lookup"><span data-stu-id="93e86-144">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="93e86-145">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="93e86-145">AzureRM.KeyVault</span></span>
* <span data-ttu-id="93e86-146">修复了 Set-AzureRmKeyVaultAccessPolicy 中的管道问题</span><span class="sxs-lookup"><span data-stu-id="93e86-146">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="93e86-147">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="93e86-147">AzureRM.Network</span></span>
* <span data-ttu-id="93e86-148">添加了 LoadBalancerInboundNatPoolConfig cmdlet 的示例。</span><span class="sxs-lookup"><span data-stu-id="93e86-148">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="93e86-149">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="93e86-149">AzureRM.Resources</span></span>
* <span data-ttu-id="93e86-150">修复了为“Get-AzureRmResource”同时提供标记名称和值时出现的问题</span><span class="sxs-lookup"><span data-stu-id="93e86-150">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="93e86-151">使用“Set-AzureRmResource”修复管道方案</span><span class="sxs-lookup"><span data-stu-id="93e86-151">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="93e86-152">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="93e86-152">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="93e86-153">在删除 cmdlet 中更新了 InputObject 和 ResourceId 的管道</span><span class="sxs-lookup"><span data-stu-id="93e86-153">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="93e86-154">修复了几个问题</span><span class="sxs-lookup"><span data-stu-id="93e86-154">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="93e86-155">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="93e86-155">AzureRM.Sql</span></span>
* <span data-ttu-id="93e86-156">使用以下 cmdlet 添加服务器高级威胁防护支持：</span><span class="sxs-lookup"><span data-stu-id="93e86-156">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="93e86-157">Enable-AzureRmSqlServerAdvancedThreatProtection；Disable-AzureRmSqlServerAdvancedThreatProtection；Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="93e86-157">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="93e86-158">使用以下 cmdlet 添加漏洞评估支持：</span><span class="sxs-lookup"><span data-stu-id="93e86-158">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="93e86-159">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings；Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings；Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="93e86-159">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="93e86-160">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline；Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline；Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="93e86-160">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="93e86-161">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan；Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord；Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="93e86-161">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="93e86-162">修复了 Remove-AzureRmSqlServerFirewallRule 中的示例</span><span class="sxs-lookup"><span data-stu-id="93e86-162">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="93e86-163">修复了 Get-AzureSqlSyncGroupLog 中非美国基础文化的日期时间处理错误</span><span class="sxs-lookup"><span data-stu-id="93e86-163">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="93e86-164">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="93e86-164">AzureRM.Storage</span></span>
* <span data-ttu-id="93e86-165">将 Ps1XmlAttribute 添加到 cmdlet 输出类型属性</span><span class="sxs-lookup"><span data-stu-id="93e86-165">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="93e86-166">在表视图中显示 StorageAccount cmdlet 输出</span><span class="sxs-lookup"><span data-stu-id="93e86-166">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="93e86-167">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="93e86-167">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="93e86-168">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="93e86-168">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="93e86-169">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="93e86-169">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="93e86-170">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="93e86-170">AzureRM.Tags</span></span>
* <span data-ttu-id="93e86-171">从 Tag cmdlet 帮助中删除不正确的语句</span><span class="sxs-lookup"><span data-stu-id="93e86-171">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="93e86-172">6.5.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="93e86-172">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="93e86-173">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="93e86-173">AzureRM.Profile</span></span>
* <span data-ttu-id="93e86-174">更新了“Get-AzureRmContextAutosaveSetting”的帮助</span><span class="sxs-lookup"><span data-stu-id="93e86-174">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="93e86-175">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="93e86-175">Azure.Storage</span></span>
* <span data-ttu-id="93e86-176">支持使用只写 Sas 令牌上传 Blob 或文件</span><span class="sxs-lookup"><span data-stu-id="93e86-176">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="93e86-177">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="93e86-177">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="93e86-178">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="93e86-178">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="93e86-179">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="93e86-179">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="93e86-180">将所需属性 ResourceGroupName 添加到 AS。</span><span class="sxs-lookup"><span data-stu-id="93e86-180">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="93e86-181">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="93e86-181">AzureRM.Automation</span></span>
* <span data-ttu-id="93e86-182">更新帮助并添加“New-AzureRMAutomationSchedule”的示例</span><span class="sxs-lookup"><span data-stu-id="93e86-182">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="93e86-183">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="93e86-183">AzureRM.Compute</span></span>
* <span data-ttu-id="93e86-184">将 -Tag 参数添加到 Update/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="93e86-184">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="93e86-185">添加“Add-AzureRmVmssExtension”的示例</span><span class="sxs-lookup"><span data-stu-id="93e86-185">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="93e86-186">添加“Remove-AzureRmVmssExtension”的示例</span><span class="sxs-lookup"><span data-stu-id="93e86-186">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="93e86-187">更新“Set-AzureRmVMAccessExtension”的帮助</span><span class="sxs-lookup"><span data-stu-id="93e86-187">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="93e86-188">更新 New-AzureRmVmss 的 SimpleParameterSet，以默认情况下将 SinglePlacementGroup 设置为false，并添加开关参数“SinglePlacementGroup”，使用户能够在单个放置组中创建 VMSS。</span><span class="sxs-lookup"><span data-stu-id="93e86-188">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="93e86-189">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="93e86-189">AzureRM.EventHub</span></span>
* <span data-ttu-id="93e86-190">向 PSEventHubDRConfigurationAttributes 类添加了一个只读属性“PendingReplicationOperationsCount”，该属性在复制过程中为挂起的复制操作计数</span><span class="sxs-lookup"><span data-stu-id="93e86-190">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="93e86-191">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="93e86-191">AzureRM.KeyVault</span></span>
* <span data-ttu-id="93e86-192">更新了 Set-AzureRmKeyVaultAccessPolicy 的错误消息</span><span class="sxs-lookup"><span data-stu-id="93e86-192">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="93e86-193">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="93e86-193">AzureRM.LogicApp</span></span>
* <span data-ttu-id="93e86-194">修复了 New-AzureRmLogicApp 中的“无法解析参数集”错误</span><span class="sxs-lookup"><span data-stu-id="93e86-194">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="93e86-195">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="93e86-195">AzureRM.Network</span></span>
* <span data-ttu-id="93e86-196">在多个租户中为 Set/Add-AzureRmVirtualNetworkPeering 启用跨虚拟网络对等互连</span><span class="sxs-lookup"><span data-stu-id="93e86-196">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="93e86-197">针对应用程序网关更新了以下 cmdlet</span><span class="sxs-lookup"><span data-stu-id="93e86-197">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="93e86-198">New-AzureRmApplicationGateway：添加了 EnableFIPS 标志和区域支持</span><span class="sxs-lookup"><span data-stu-id="93e86-198">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="93e86-199">New-AzureRmApplicationGatewaySku：添加了新的 sku Standard_v2 和 WAF_v2</span><span class="sxs-lookup"><span data-stu-id="93e86-199">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="93e86-200">Set-AzureRmApplicationGatewaySku：添加了新的 sku Standard_v2 和 WAF_v2</span><span class="sxs-lookup"><span data-stu-id="93e86-200">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="93e86-201">使用最新的生成器版本重新生成了 RouteTable cmdlet</span><span class="sxs-lookup"><span data-stu-id="93e86-201">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="93e86-202">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="93e86-202">AzureRM.Relay</span></span>
* <span data-ttu-id="93e86-203">更新了 Markdown 文件，其中修复了示例中的参数名称问题</span><span class="sxs-lookup"><span data-stu-id="93e86-203">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="93e86-204">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="93e86-204">AzureRM.Resources</span></span>
* <span data-ttu-id="93e86-205">更新了 Roleassignment 和 roledefinition cmdlet：</span><span class="sxs-lookup"><span data-stu-id="93e86-205">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="93e86-206">删除了作为分页的一部分完成的额外 roledefinition 调用。</span><span class="sxs-lookup"><span data-stu-id="93e86-206">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="93e86-207">修复了 Get-AzureRmRoleAssignment cmdlet</span><span class="sxs-lookup"><span data-stu-id="93e86-207">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="93e86-208">修复了 -ExpandPrincipalGroups 命令参数功能</span><span class="sxs-lookup"><span data-stu-id="93e86-208">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="93e86-209">修复了“Get-AzureRmResource”的问题，其中“-ResourceType”参数区分大小写</span><span class="sxs-lookup"><span data-stu-id="93e86-209">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="93e86-210">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="93e86-210">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="93e86-211">向列表 cmdlet 添加了 top 和 skip 参数</span><span class="sxs-lookup"><span data-stu-id="93e86-211">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="93e86-212">添加了标准到高级命名空间迁移 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="93e86-212">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="93e86-213">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="93e86-213">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="93e86-214">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="93e86-214">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="93e86-215">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="93e86-215">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="93e86-216">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="93e86-216">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="93e86-217">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="93e86-217">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="93e86-218">向 PSServiceBusDRConfigurationAttributes 类添加了一个只读属性“PendingReplicationOperationsCount”，该属性在复制过程中为挂起的复制操作计数</span><span class="sxs-lookup"><span data-stu-id="93e86-218">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="93e86-219">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="93e86-219">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="93e86-220">更新了“New-AzureRmServiceFabricCluster”的示例</span><span class="sxs-lookup"><span data-stu-id="93e86-220">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="93e86-221">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="93e86-221">AzureRM.Sql</span></span>
* <span data-ttu-id="93e86-222">为 Management.Sql 添加新的 Cmdlet，以允许客户将 TDE 证书添加到 Sql Server 实例或托管实例</span><span class="sxs-lookup"><span data-stu-id="93e86-222">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="93e86-223">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="93e86-223">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="93e86-224">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="93e86-224">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="93e86-225">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="93e86-225">AzureRM.Websites</span></span>
* <span data-ttu-id="93e86-226">设置为 false 时，`Set-AzureRmWebApp -AssignIdentity` 和 `Set-AzureRmWebAppSlot -AssignIdentity` 现在将从站点对象中删除 Identity 属性。同时移除预览标记。</span><span class="sxs-lookup"><span data-stu-id="93e86-226">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="93e86-227">`Get-AzureRmWebAppMetrics`、`Get-AzureRmAppServicePlanMetrics` 示例已更新</span><span class="sxs-lookup"><span data-stu-id="93e86-227">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="93e86-228">`Set-AzureRmWebApp -PhpVersion` 支持 off 作为有效的 php 版本</span><span class="sxs-lookup"><span data-stu-id="93e86-228">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="93e86-229">6.4.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="93e86-229">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="93e86-230">常规</span><span class="sxs-lookup"><span data-stu-id="93e86-230">General</span></span>
* <span data-ttu-id="93e86-231">修复了大多数模块的帮助文件中的 OutputType 格式问题</span><span class="sxs-lookup"><span data-stu-id="93e86-231">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="93e86-232">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="93e86-232">AzureRM.Profile</span></span>
* <span data-ttu-id="93e86-233">已将 Ps1Xml 属性添加到基本输出类型</span><span class="sxs-lookup"><span data-stu-id="93e86-233">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="93e86-234">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="93e86-234">AzureRM.Compute</span></span>
* <span data-ttu-id="93e86-235">VMSS 的 IP 标记功能</span><span class="sxs-lookup"><span data-stu-id="93e86-235">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="93e86-236">已添加“New-AzureRmVmssIpTagConfig”cmdlet</span><span class="sxs-lookup"><span data-stu-id="93e86-236">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="93e86-237">已将 IpTag 参数添加到 New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="93e86-237">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="93e86-238">VMSS 的自动 OS 回滚功能</span><span class="sxs-lookup"><span data-stu-id="93e86-238">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="93e86-239">已将 DisableAutoRollback 参数添加到 New-AzureRmVmssConfig 和 Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="93e86-239">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="93e86-240">VMSS 的 OS 升级历史记录功能</span><span class="sxs-lookup"><span data-stu-id="93e86-240">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="93e86-241">已将 OSUpgradeHistory 开关参数添加到 Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="93e86-241">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="93e86-242">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="93e86-242">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="93e86-243">通过以下命令添加目录 ACL 的支持：</span><span class="sxs-lookup"><span data-stu-id="93e86-243">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="93e86-244">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="93e86-244">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="93e86-245">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="93e86-245">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="93e86-246">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="93e86-246">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="93e86-247">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="93e86-247">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="93e86-248">为 Set-AzureRmDataLakeStoreItemAclEntry、Remove-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAcl 添加了取消支持和进度跟踪</span><span class="sxs-lookup"><span data-stu-id="93e86-248">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="93e86-249">为 Export-AzureRmDataLakeStoreChildItemProperties 添加了取消支持</span><span class="sxs-lookup"><span data-stu-id="93e86-249">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="93e86-250">修复了执行递归操作的 cmdlet 的调试消息刷新</span><span class="sxs-lookup"><span data-stu-id="93e86-250">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="93e86-251">修复了 DataLake cmdlet 的测试位置</span><span class="sxs-lookup"><span data-stu-id="93e86-251">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="93e86-252">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="93e86-252">AzureRM.EventHub</span></span>
* <span data-ttu-id="93e86-253">已将可选的 MaxCount 参数添加到“列出操作”cmdlet Get-AzureRmEventHub 和 Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="93e86-253">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="93e86-254">修复了 New-AzureRmEventHub cmdlet 的问题：创建新事件中心时至少需要一个参数。</span><span class="sxs-lookup"><span data-stu-id="93e86-254">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="93e86-255">提供了默认参数集。</span><span class="sxs-lookup"><span data-stu-id="93e86-255">Provided Default Parameter set.</span></span>
* <span data-ttu-id="93e86-256">已将可选参数 -KeyValue 添加到 New-AzureRmEventHubKey cmdlet，该参数可让用户提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="93e86-256">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="93e86-257">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="93e86-257">AzureRM.KeyVault</span></span>
* <span data-ttu-id="93e86-258">修复了 Get-AzureRmKeyVault -Tag 返回所有资源的问题</span><span class="sxs-lookup"><span data-stu-id="93e86-258">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="93e86-259">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="93e86-259">AzureRM.Network</span></span>
* <span data-ttu-id="93e86-260">为区域冗余的 VirtualNetworkGateways 公开新 SKU</span><span class="sxs-lookup"><span data-stu-id="93e86-260">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="93e86-261">通过 ARM 为以下功能添加了新命令：ExpressRoute 合作伙伴 API</span><span class="sxs-lookup"><span data-stu-id="93e86-261">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="93e86-262">添加了 Get-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="93e86-262">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="93e86-263">添加了 Set-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="93e86-263">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="93e86-264">添加了 Add-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="93e86-264">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="93e86-265">添加了 Get-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="93e86-265">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="93e86-266">添加了 Remove-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="93e86-266">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="93e86-267">添加了 Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="93e86-267">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="93e86-268">添加了 Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="93e86-268">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="93e86-269">添加了 Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="93e86-269">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="93e86-270">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="93e86-270">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="93e86-271">添加了 Get-AzureRmRecoveryServicesBackupStatus cmdlet。</span><span class="sxs-lookup"><span data-stu-id="93e86-271">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="93e86-272">此 cmdlet 采用 VM ID，并检查 VM 是否受订阅中的某个保管库保护。</span><span class="sxs-lookup"><span data-stu-id="93e86-272">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="93e86-273">如果存在此类保管库，该 cmdlet 会输出该保管库的详细信息。</span><span class="sxs-lookup"><span data-stu-id="93e86-273">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="93e86-274">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="93e86-274">AzureRM.Resources</span></span>
* <span data-ttu-id="93e86-275">更新了 Get-AzureRmPolicyAssignment cmdlet：</span><span class="sxs-lookup"><span data-stu-id="93e86-275">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="93e86-276">添加了在管理组级别列出 -Scope 值的支持</span><span class="sxs-lookup"><span data-stu-id="93e86-276">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="93e86-277">添加了在管理组级别使用 -Scope 值检索单个分配的支持</span><span class="sxs-lookup"><span data-stu-id="93e86-277">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="93e86-278">已将 -Effective 和 -All 开关添加到 control 参数</span><span class="sxs-lookup"><span data-stu-id="93e86-278">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="93e86-279">更新了 Get/New/Remove/Set-AzureRmPolicyDefinition cmdlet</span><span class="sxs-lookup"><span data-stu-id="93e86-279">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="93e86-280">添加了 -ManagementGroupName 参数，以将操作应用到给定的管理组</span><span class="sxs-lookup"><span data-stu-id="93e86-280">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="93e86-281">添加了 -SubscriptionId 参数，以将操作应用到给定的订阅</span><span class="sxs-lookup"><span data-stu-id="93e86-281">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="93e86-282">更新了 Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlet</span><span class="sxs-lookup"><span data-stu-id="93e86-282">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="93e86-283">添加了 -ManagementGroupName 参数，以将操作应用到给定的管理组</span><span class="sxs-lookup"><span data-stu-id="93e86-283">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="93e86-284">添加了 -SubscriptionId 参数，以将操作应用到给定的订阅</span><span class="sxs-lookup"><span data-stu-id="93e86-284">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="93e86-285">添加了使用 TemplateParameterObject 时在参数中指定 KeyVault 机密引用的支持</span><span class="sxs-lookup"><span data-stu-id="93e86-285">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="93e86-286">修复了忽略“New-AzureRmADAppCredential”的“-EndDate”参数的问题</span><span class="sxs-lookup"><span data-stu-id="93e86-286">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="93e86-287">修复了“Add-AzureRmADGroupMember”使用错误的 URL 发出请求的问题</span><span class="sxs-lookup"><span data-stu-id="93e86-287">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="93e86-288">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="93e86-288">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="93e86-289">已将可选参数 -KeyValue 添加到 New-AzureRmServiceBusKey cmdlet，该参数可让用户提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="93e86-289">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="93e86-290">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="93e86-290">AzureRM.Sql</span></span>
* <span data-ttu-id="93e86-291">在 AzureRmSqlDatabaseRestorePoint 帮助中澄清了 SQLDW 的用户定义还原点</span><span class="sxs-lookup"><span data-stu-id="93e86-291">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="93e86-292">更新了多个 cmdlet 中 -ComputeGeneration 参数的文档</span><span class="sxs-lookup"><span data-stu-id="93e86-292">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="93e86-293">6.3.0 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="93e86-293">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="93e86-294">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="93e86-294">AzureRM.Profile</span></span>
* <span data-ttu-id="93e86-295">更新了 Enable-AzureRmContextAutoSave 的错误消息</span><span class="sxs-lookup"><span data-stu-id="93e86-295">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="93e86-296">在运行没有旧上下文的“Connect-AzureRmAccount”时为每个订阅创建一个上下文</span><span class="sxs-lookup"><span data-stu-id="93e86-296">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="93e86-297">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="93e86-297">Azure.Storage</span></span>
* <span data-ttu-id="93e86-298">在帮助文件中增加了关于 -Permissions 参数的其他信息。</span><span class="sxs-lookup"><span data-stu-id="93e86-298">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="93e86-299">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="93e86-299">AzureRM.Compute</span></span>
* <span data-ttu-id="93e86-300">“Get-AzureRmVmDiskEncryptionStatus”修复了一个针对没有数据磁盘的 VM 观察到的问题</span><span class="sxs-lookup"><span data-stu-id="93e86-300">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="93e86-301">更新计算客户端库版本以修复以下 cmdlet</span><span class="sxs-lookup"><span data-stu-id="93e86-301">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="93e86-302">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="93e86-302">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="93e86-303">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="93e86-303">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="93e86-304">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="93e86-304">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="93e86-305">修复了以下 cmdlet，因此可以正确地显示“操作 ID”和“操作状态”：</span><span class="sxs-lookup"><span data-stu-id="93e86-305">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="93e86-306">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="93e86-306">Start-AzureRmVM</span></span>
    - <span data-ttu-id="93e86-307">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="93e86-307">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="93e86-308">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="93e86-308">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="93e86-309">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="93e86-309">Set-AzureRmVM</span></span>
    - <span data-ttu-id="93e86-310">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="93e86-310">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="93e86-311">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="93e86-311">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="93e86-312">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="93e86-312">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="93e86-313">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="93e86-313">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="93e86-314">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="93e86-314">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="93e86-315">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="93e86-315">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="93e86-316">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="93e86-316">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="93e86-317">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="93e86-317">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="93e86-318">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="93e86-318">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="93e86-319">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="93e86-319">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="93e86-320">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="93e86-320">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="93e86-321">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="93e86-321">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="93e86-322">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="93e86-322">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="93e86-323">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="93e86-323">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="93e86-324">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="93e86-324">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="93e86-325">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="93e86-325">AzureRM.EventGrid</span></span>
* <span data-ttu-id="93e86-326">在 Update-AzureRmEventGridSubscription cmdlet 中删除 SubjectBeginsWith/SubjectEndsWith 的 ValidateNotNullOrEmpty 验证条件，允许根据需要将这些参数更改为空字符串。</span><span class="sxs-lookup"><span data-stu-id="93e86-326">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="93e86-327">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="93e86-327">AzureRM.KeyVault</span></span>
* <span data-ttu-id="93e86-328">修复运行 Get-AzureRmKeyVault -Tag 时不返回任何标记的问题</span><span class="sxs-lookup"><span data-stu-id="93e86-328">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="93e86-329">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="93e86-329">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="93e86-330">策略见解 cmdlet 的公开发行版</span><span class="sxs-lookup"><span data-stu-id="93e86-330">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="93e86-331">使用 API 版本 2018-04-04</span><span class="sxs-lookup"><span data-stu-id="93e86-331">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="93e86-332">向 Get-AzureRmPolicyStateSummary 的结果添加了 PolicyDefinitionReferenceId</span><span class="sxs-lookup"><span data-stu-id="93e86-332">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="93e86-333">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="93e86-333">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="93e86-334">向 RecoveryServices.Backup cmdlet 添加了 -Vault 参数。</span><span class="sxs-lookup"><span data-stu-id="93e86-334">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="93e86-335">传递时，此项会替代 Set-AzureRmRecoveryServicesContext cmdlet。</span><span class="sxs-lookup"><span data-stu-id="93e86-335">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="93e86-336">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="93e86-336">AzureRM.Sql</span></span>
* <span data-ttu-id="93e86-337">更新了 Get-AzureRmSqlDatabaseExpanded 的帮助文件中的示例</span><span class="sxs-lookup"><span data-stu-id="93e86-337">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="93e86-338">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="93e86-338">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="93e86-339">更新了 Add-AzureRmTrafficManagerEndpointConfig 的帮助文件</span><span class="sxs-lookup"><span data-stu-id="93e86-339">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="93e86-340">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="93e86-340">AzureRM.Websites</span></span>
* <span data-ttu-id="93e86-341">更新了“Set-AzureRmWebApp”，在使用 -AssignIdentity 时不覆盖 AppSettings</span><span class="sxs-lookup"><span data-stu-id="93e86-341">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="93e86-342">更新了“New-AzureRmWebAppSlot”，允许使用 AppServicePlan 作为可选参数</span><span class="sxs-lookup"><span data-stu-id="93e86-342">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="93e86-343">6.2.1 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="93e86-343">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="93e86-344">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="93e86-344">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="93e86-345">更新了 PSWorkspace 模型，允许 Network 使用 type 作为参数</span><span class="sxs-lookup"><span data-stu-id="93e86-345">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="93e86-346">6.2.0 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="93e86-346">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="93e86-347">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="93e86-347">AzureRM.Profile</span></span>
* <span data-ttu-id="93e86-348">修复了 Newtonsoft.Json 的版本 10.0.3 在模块导入时无法加载的问题</span><span class="sxs-lookup"><span data-stu-id="93e86-348">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="93e86-349">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="93e86-349">AzureRM.Compute</span></span>
* <span data-ttu-id="93e86-350">VMSS VM 更新功能</span><span class="sxs-lookup"><span data-stu-id="93e86-350">VMSS VM Update feature</span></span>
    - <span data-ttu-id="93e86-351">增加了“Update-AzureRmVmssVM”和“New-AzureRmVMDataDisk”cmdlet</span><span class="sxs-lookup"><span data-stu-id="93e86-351">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="93e86-352">为“Add-AzureRmVMDataDisk”cmdlet 增加了 VirtualMachineScaleSetVM 参数，支持向 Vmss VM 添加数据磁盘。</span><span class="sxs-lookup"><span data-stu-id="93e86-352">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="93e86-353">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="93e86-353">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="93e86-354">将 ADF.Net SDK 版本更新到了 0.8.0-preview，其中包含以下更改：</span><span class="sxs-lookup"><span data-stu-id="93e86-354">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="93e86-355">增加了“配置工厂存储库”操作</span><span class="sxs-lookup"><span data-stu-id="93e86-355">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="93e86-356">更新了 QuickBooks LinkedService，可以公开 consumerKey 和 consumerSecret 属性</span><span class="sxs-lookup"><span data-stu-id="93e86-356">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="93e86-357">已将多个模型类型从 SecretBase 更新为 Object</span><span class="sxs-lookup"><span data-stu-id="93e86-357">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="93e86-358">增加了 Blob 事件触发器</span><span class="sxs-lookup"><span data-stu-id="93e86-358">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="93e86-359">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="93e86-359">AzureRM.KeyVault</span></span>
* <span data-ttu-id="93e86-360">使用示例输出更新了文档</span><span class="sxs-lookup"><span data-stu-id="93e86-360">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="93e86-361">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="93e86-361">AzureRM.Network</span></span>
* <span data-ttu-id="93e86-362">在网络观察程序 cmdlet 上启用了流量分析参数</span><span class="sxs-lookup"><span data-stu-id="93e86-362">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="93e86-363">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="93e86-363">AzureRM.Resources</span></span>
* <span data-ttu-id="93e86-364">修复了从“Get-AzureRmResource”返回的“PSResource”对象的“Properties”属性问题</span><span class="sxs-lookup"><span data-stu-id="93e86-364">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="93e86-365">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="93e86-365">AzureRM.Scheduler</span></span>
* <span data-ttu-id="93e86-366">修复了更新 ServiceBusQueueJob 无法设置新 Auth 值的问题</span><span class="sxs-lookup"><span data-stu-id="93e86-366">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="93e86-367">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="93e86-367">AzureRM.Sql</span></span>
* <span data-ttu-id="93e86-368">使用可选的 LicenseType 参数更新了以下 cmdlet</span><span class="sxs-lookup"><span data-stu-id="93e86-368">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="93e86-369">New-AzureRmSqlDatabase；Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="93e86-369">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="93e86-370">New-AzureRmSqlElasticPool；Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="93e86-370">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="93e86-371">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="93e86-371">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="93e86-372">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="93e86-372">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="93e86-373">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="93e86-373">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="93e86-374">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="93e86-374">AzureRM.Websites</span></span>
* <span data-ttu-id="93e86-375">更新了“New-AzureRMWebApp”，可以使用策略库中的常用算法。</span><span class="sxs-lookup"><span data-stu-id="93e86-375">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="93e86-376">6.1.0 - 2018 年 5 月</span><span class="sxs-lookup"><span data-stu-id="93e86-376">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="93e86-377">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="93e86-377">AzureRM.Profile</span></span>
* <span data-ttu-id="93e86-378">修复了运行“Clear-AzureRmContext”时会保留空上下文的问题，该上下文使用旧的默认上下文的名称，导致用户无法使用旧名称创建新的上下文</span><span class="sxs-lookup"><span data-stu-id="93e86-378">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="93e86-379">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="93e86-379">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="93e86-380">允许在 AS 上执行网关的关联/取消关联操作。</span><span class="sxs-lookup"><span data-stu-id="93e86-380">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="93e86-381">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="93e86-381">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="93e86-382">增加了对 ApiVersions、ApiReleases 和 ApiRevisions 的支持</span><span class="sxs-lookup"><span data-stu-id="93e86-382">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="93e86-383">增加了对 ServiceFabric 后端的支持</span><span class="sxs-lookup"><span data-stu-id="93e86-383">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="93e86-384">增加了对 Application Insights Logger 的支持</span><span class="sxs-lookup"><span data-stu-id="93e86-384">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="93e86-385">增加的支持包括认可“基本”SKU 是 API 管理服务的有效 SKU</span><span class="sxs-lookup"><span data-stu-id="93e86-385">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="93e86-386">增加的支持包括允许将专用 CA 颁发的证书作为根证书或 CA 证书安装</span><span class="sxs-lookup"><span data-stu-id="93e86-386">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="93e86-387">增加的支持包括通过 KeyVault 和多个代理主机名接受自定义 SSL 证书</span><span class="sxs-lookup"><span data-stu-id="93e86-387">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="93e86-388">增加了对 MSI 标识的支持</span><span class="sxs-lookup"><span data-stu-id="93e86-388">Added support for MSI identity</span></span>
* <span data-ttu-id="93e86-389">增加的支持包括通过 URL 接受策略 注意：以下 cmdlet 将在未来版本中弃用</span><span class="sxs-lookup"><span data-stu-id="93e86-389">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="93e86-390">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="93e86-390">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="93e86-391">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="93e86-391">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="93e86-392">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="93e86-392">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="93e86-393">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="93e86-393">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="93e86-394">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="93e86-394">AzureRM.Batch</span></span>
* <span data-ttu-id="93e86-395">发布新 cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="93e86-395">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="93e86-396">发布新 cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="93e86-396">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="93e86-397">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="93e86-397">AzureRM.Consumption</span></span>
* <span data-ttu-id="93e86-398">在 Cmdlet Get-AzureRmConsumptionUsageDetail 中增加了新参数 Expand、ResourceGroup、InstanceName、InstanceId、Tags、Top</span><span class="sxs-lookup"><span data-stu-id="93e86-398">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="93e86-399">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="93e86-399">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="93e86-400">修复了 Export-AzureRmDataLakeStoreChildItemProperties 的示例</span><span class="sxs-lookup"><span data-stu-id="93e86-400">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="93e86-401">修复了 Set-AzureRmDataLakeStoreItemAclEntry 中 Recurse 用例的 null 参数异常</span><span class="sxs-lookup"><span data-stu-id="93e86-401">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="93e86-402">修复了 Set-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAcl、Remove-AzureRmDataLakeStoreItemAclEntry 的帮助文件</span><span class="sxs-lookup"><span data-stu-id="93e86-402">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="93e86-403">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="93e86-403">AzureRM.Network</span></span>
* <span data-ttu-id="93e86-404">将网络 SDK 版本从 18.0.0-preview 升至 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="93e86-404">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="93e86-405">增加了用于创建协议配置的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="93e86-405">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="93e86-406">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="93e86-406">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="93e86-407">增加了用于向现有的快速路由线路添加新的线路连接的 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="93e86-407">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="93e86-408">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="93e86-408">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="93e86-409">增加了用于从现有的快速路由线路删除线路连接的 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="93e86-409">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="93e86-410">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="93e86-410">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="93e86-411">增加了用于检索线路连接的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="93e86-411">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="93e86-412">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="93e86-412">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="93e86-413">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="93e86-413">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="93e86-414">修复了使用生成的证书进行服务器身份验证的问题（问题 5998）</span><span class="sxs-lookup"><span data-stu-id="93e86-414">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="93e86-415">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="93e86-415">AzureRM.Sql</span></span>
* <span data-ttu-id="93e86-416">更新了审核 cmdlet，允许删除 AuditActions 或 AuditActionGroups</span><span class="sxs-lookup"><span data-stu-id="93e86-416">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="93e86-417">修复了设置新的灵活保留策略时使用 Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy 出现的问题。该问题的具体表现是：在命令失败的同时，出现“不再支持使用 Azure 恢复服务保管库和策略配置长期保留策略。</span><span class="sxs-lookup"><span data-stu-id="93e86-417">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="93e86-418">请使用新的灵活保留策略提交请求”错误消息。</span><span class="sxs-lookup"><span data-stu-id="93e86-418">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="93e86-419">更新了与 Azure SQL 数据库/ElasticPool 的创建/更新相关的所有 cmdlet，允许使用新的数据库 API，而这些 cmdlet 支持的 SKU 属性则适用于规模和层相关属性。</span><span class="sxs-lookup"><span data-stu-id="93e86-419">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="93e86-420">更新的 cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="93e86-420">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="93e86-421">New-AzureRmSqlDatabase；Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="93e86-421">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="93e86-422">New-AzureRmSqlElasticPool；Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="93e86-422">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="93e86-423">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="93e86-423">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="93e86-424">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="93e86-424">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="93e86-425">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="93e86-425">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="93e86-426">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="93e86-426">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="93e86-427">更新了“Get-AzureRmTrafficManagerProfile”的参数，要求在使用 -Name 参数时使用 -ResourceGroupName 参数。</span><span class="sxs-lookup"><span data-stu-id="93e86-427">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>