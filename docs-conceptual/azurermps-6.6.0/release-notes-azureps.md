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
ms.openlocfilehash: 340c1d2d28e1b97cdd2ec98033361eb00b4302da
ms.sourcegitcommit: 72086f8d368ec84bd403e802305acfc336c08978
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/14/2018
ms.locfileid: "43019078"
---
# <a name="release-notes"></a><span data-ttu-id="2d59d-103">发行说明</span><span class="sxs-lookup"><span data-stu-id="2d59d-103">Release notes</span></span>

<span data-ttu-id="2d59d-104">下面是此版本中对 Azure PowerShell 所做的更改列表。</span><span class="sxs-lookup"><span data-stu-id="2d59d-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="660---july-2018"></a><span data-ttu-id="2d59d-105">6.6.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="2d59d-105">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="2d59d-106">常规</span><span class="sxs-lookup"><span data-stu-id="2d59d-106">General</span></span>
* <span data-ttu-id="2d59d-107">更新了所有帮助文件，以包括完整参数类型和正确的输入/输出类型。</span><span class="sxs-lookup"><span data-stu-id="2d59d-107">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="2d59d-108">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="2d59d-108">AzureRM.Profile</span></span>
* <span data-ttu-id="2d59d-109">更新了 Common.Strategy 库，以便能够验证资源的当前配置是否与目标资源兼容。</span><span class="sxs-lookup"><span data-stu-id="2d59d-109">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="2d59d-110">在 Common.Storage 中添加了 ps1xml 类型</span><span class="sxs-lookup"><span data-stu-id="2d59d-110">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="2d59d-111">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="2d59d-111">Azure.Storage</span></span>
* <span data-ttu-id="2d59d-112">增加了从 DefaultProfile 获取存储上下文的支持</span><span class="sxs-lookup"><span data-stu-id="2d59d-112">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="2d59d-113">为 cmdlet 输出类型属性增加了 Ps1XmlAttribute。</span><span class="sxs-lookup"><span data-stu-id="2d59d-113">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="2d59d-114">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2d59d-114">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="2d59d-115">修复了问题 https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="2d59d-115">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="2d59d-116">修复了 Automapper 中将 PsApiManagementApi 转换为 ApiContract 的 bug</span><span class="sxs-lookup"><span data-stu-id="2d59d-116">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="2d59d-117">修复了问题 https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="2d59d-117">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="2d59d-118">修复了 File.Save 中没有使用编码类型重载的 bug</span><span class="sxs-lookup"><span data-stu-id="2d59d-118">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="2d59d-119">修复了问题 https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="2d59d-119">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="2d59d-120">升级到了 4.0.3 Nuget版本，该版本修复了 apiId 上的模式异常</span><span class="sxs-lookup"><span data-stu-id="2d59d-120">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="2d59d-121">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="2d59d-121">AzureRM.Compute</span></span>
* <span data-ttu-id="2d59d-122">修复因使用 PremiumLRS 存储帐户类型重命名而在 New-AzureRmVm 中使用 DiskFileParameterSet 创建 VM 失败的问题。</span><span class="sxs-lookup"><span data-stu-id="2d59d-122">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="2d59d-123">修复 Invoke-AzureRmVMRunCommand cmdlet</span><span class="sxs-lookup"><span data-stu-id="2d59d-123">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="2d59d-124">更新 Get-AzureRmAvailabilitySet 以启用列出订阅中的所有可用性集。</span><span class="sxs-lookup"><span data-stu-id="2d59d-124">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="2d59d-125">（ResouceGroupName 参数现在是可选的。）</span><span class="sxs-lookup"><span data-stu-id="2d59d-125">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="2d59d-126">更新“New-AzureRmVm”的 SimpleParameterSet 以在符合条件的 VM 上启用加速网络。</span><span class="sxs-lookup"><span data-stu-id="2d59d-126">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="2d59d-127">将 New-AzureRmVmss 简单参数集更新为在用户指定的 LB 已存在时创建 vmss 失败。</span><span class="sxs-lookup"><span data-stu-id="2d59d-127">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="2d59d-128">更新 New-AzureRmDisk 的示例</span><span class="sxs-lookup"><span data-stu-id="2d59d-128">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="2d59d-129">添加“New-AzureRmVM”的示例</span><span class="sxs-lookup"><span data-stu-id="2d59d-129">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="2d59d-130">更新 Set-AzureRmVMOSDisk 的说明</span><span class="sxs-lookup"><span data-stu-id="2d59d-130">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="2d59d-131">更新 Set-AzureRmVMBginfoExtension 的示例 1 以更正拼写和前缀。</span><span class="sxs-lookup"><span data-stu-id="2d59d-131">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="2d59d-132">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="2d59d-132">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="2d59d-133">将 ADF .Net SDK 版本更新为 1.1.0。</span><span class="sxs-lookup"><span data-stu-id="2d59d-133">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="2d59d-134">支持跨数据工厂的自承载集成运行时共享。</span><span class="sxs-lookup"><span data-stu-id="2d59d-134">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="2d59d-135">将新参数 -SharedIntegrationRuntimeResourceId 添加到 Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2d59d-135">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="2d59d-136">将新的可选参数 -LinkedDataFactoryName 添加到 Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2d59d-136">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="2d59d-137">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2d59d-137">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="2d59d-138">将数据平面 SDK (Microsoft.Azure.DataLake.Store) 版本更新为 1.1.9</span><span class="sxs-lookup"><span data-stu-id="2d59d-138">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="2d59d-139">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="2d59d-139">AzureRM.EventHub</span></span>
* <span data-ttu-id="2d59d-140">在删除 cmdlet 中更新了 InputObject 和 ResourceId 的管道</span><span class="sxs-lookup"><span data-stu-id="2d59d-140">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="2d59d-141">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="2d59d-141">AzureRM.Insights</span></span>
* <span data-ttu-id="2d59d-142">修复了帮助文件中 OutputType 的格式问题</span><span class="sxs-lookup"><span data-stu-id="2d59d-142">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="2d59d-143">使用 Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span><span class="sxs-lookup"><span data-stu-id="2d59d-143">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="2d59d-144">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2d59d-144">AzureRM.KeyVault</span></span>
* <span data-ttu-id="2d59d-145">修复了 Set-AzureRmKeyVaultAccessPolicy 中的管道问题</span><span class="sxs-lookup"><span data-stu-id="2d59d-145">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="2d59d-146">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="2d59d-146">AzureRM.Network</span></span>
* <span data-ttu-id="2d59d-147">添加了 LoadBalancerInboundNatPoolConfig cmdlet 的示例。</span><span class="sxs-lookup"><span data-stu-id="2d59d-147">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="2d59d-148">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="2d59d-148">AzureRM.Resources</span></span>
* <span data-ttu-id="2d59d-149">修复了为“Get-AzureRmResource”同时提供标记名称和值时出现的问题</span><span class="sxs-lookup"><span data-stu-id="2d59d-149">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="2d59d-150">使用“Set-AzureRmResource”修复管道方案</span><span class="sxs-lookup"><span data-stu-id="2d59d-150">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="2d59d-151">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2d59d-151">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="2d59d-152">在删除 cmdlet 中更新了 InputObject 和 ResourceId 的管道</span><span class="sxs-lookup"><span data-stu-id="2d59d-152">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="2d59d-153">修复了几个问题</span><span class="sxs-lookup"><span data-stu-id="2d59d-153">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="2d59d-154">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="2d59d-154">AzureRM.Sql</span></span>
* <span data-ttu-id="2d59d-155">使用以下 cmdlet 添加服务器高级威胁防护支持：</span><span class="sxs-lookup"><span data-stu-id="2d59d-155">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="2d59d-156">Enable-AzureRmSqlServerAdvancedThreatProtection；Disable-AzureRmSqlServerAdvancedThreatProtection；Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="2d59d-156">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="2d59d-157">使用以下 cmdlet 添加漏洞评估支持：</span><span class="sxs-lookup"><span data-stu-id="2d59d-157">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="2d59d-158">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings；Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings；Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="2d59d-158">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="2d59d-159">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline；Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline；Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="2d59d-159">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="2d59d-160">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan；Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord；Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="2d59d-160">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="2d59d-161">修复了 Remove-AzureRmSqlServerFirewallRule 中的示例</span><span class="sxs-lookup"><span data-stu-id="2d59d-161">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="2d59d-162">修复了 Get-AzureSqlSyncGroupLog 中非美国基础文化的日期时间处理错误</span><span class="sxs-lookup"><span data-stu-id="2d59d-162">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="2d59d-163">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="2d59d-163">AzureRM.Storage</span></span>
* <span data-ttu-id="2d59d-164">将 Ps1XmlAttribute 添加到 cmdlet 输出类型属性</span><span class="sxs-lookup"><span data-stu-id="2d59d-164">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="2d59d-165">在表视图中显示 StorageAccount cmdlet 输出</span><span class="sxs-lookup"><span data-stu-id="2d59d-165">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="2d59d-166">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2d59d-166">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="2d59d-167">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2d59d-167">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="2d59d-168">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2d59d-168">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="2d59d-169">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="2d59d-169">AzureRM.Tags</span></span>
* <span data-ttu-id="2d59d-170">从 Tag cmdlet 帮助中删除不正确的语句</span><span class="sxs-lookup"><span data-stu-id="2d59d-170">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="2d59d-171">6.5.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="2d59d-171">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="2d59d-172">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="2d59d-172">AzureRM.Profile</span></span>
* <span data-ttu-id="2d59d-173">更新了“Get-AzureRmContextAutosaveSetting”的帮助</span><span class="sxs-lookup"><span data-stu-id="2d59d-173">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="2d59d-174">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="2d59d-174">Azure.Storage</span></span>
* <span data-ttu-id="2d59d-175">支持使用只写 Sas 令牌上传 Blob 或文件</span><span class="sxs-lookup"><span data-stu-id="2d59d-175">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="2d59d-176">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="2d59d-176">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="2d59d-177">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="2d59d-177">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="2d59d-178">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="2d59d-178">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="2d59d-179">将所需属性 ResourceGroupName 添加到 AS。</span><span class="sxs-lookup"><span data-stu-id="2d59d-179">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="2d59d-180">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="2d59d-180">AzureRM.Automation</span></span>
* <span data-ttu-id="2d59d-181">更新帮助并添加“New-AzureRMAutomationSchedule”的示例</span><span class="sxs-lookup"><span data-stu-id="2d59d-181">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="2d59d-182">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="2d59d-182">AzureRM.Compute</span></span>
* <span data-ttu-id="2d59d-183">将 -Tag 参数添加到 Update/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="2d59d-183">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="2d59d-184">添加“Add-AzureRmVmssExtension”的示例</span><span class="sxs-lookup"><span data-stu-id="2d59d-184">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="2d59d-185">添加“Remove-AzureRmVmssExtension”的示例</span><span class="sxs-lookup"><span data-stu-id="2d59d-185">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="2d59d-186">更新“Set-AzureRmVMAccessExtension”的帮助</span><span class="sxs-lookup"><span data-stu-id="2d59d-186">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="2d59d-187">更新 New-AzureRmVmss 的 SimpleParameterSet，以默认情况下将 SinglePlacementGroup 设置为false，并添加开关参数“SinglePlacementGroup”，使用户能够在单个放置组中创建 VMSS。</span><span class="sxs-lookup"><span data-stu-id="2d59d-187">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="2d59d-188">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="2d59d-188">AzureRM.EventHub</span></span>
* <span data-ttu-id="2d59d-189">向 PSEventHubDRConfigurationAttributes 类添加了一个只读属性“PendingReplicationOperationsCount”，该属性在复制过程中为挂起的复制操作计数</span><span class="sxs-lookup"><span data-stu-id="2d59d-189">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="2d59d-190">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2d59d-190">AzureRM.KeyVault</span></span>
* <span data-ttu-id="2d59d-191">更新了 Set-AzureRmKeyVaultAccessPolicy 的错误消息</span><span class="sxs-lookup"><span data-stu-id="2d59d-191">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="2d59d-192">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="2d59d-192">AzureRM.LogicApp</span></span>
* <span data-ttu-id="2d59d-193">修复了 New-AzureRmLogicApp 中的“无法解析参数集”错误</span><span class="sxs-lookup"><span data-stu-id="2d59d-193">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="2d59d-194">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="2d59d-194">AzureRM.Network</span></span>
* <span data-ttu-id="2d59d-195">在多个租户中为 Set/Add-AzureRmVirtualNetworkPeering 启用跨虚拟网络对等互连</span><span class="sxs-lookup"><span data-stu-id="2d59d-195">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="2d59d-196">针对应用程序网关更新了以下 cmdlet</span><span class="sxs-lookup"><span data-stu-id="2d59d-196">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="2d59d-197">New-AzureRmApplicationGateway：添加了 EnableFIPS 标志和区域支持</span><span class="sxs-lookup"><span data-stu-id="2d59d-197">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="2d59d-198">New-AzureRmApplicationGatewaySku：添加了新的 sku Standard_v2 和 WAF_v2</span><span class="sxs-lookup"><span data-stu-id="2d59d-198">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="2d59d-199">Set-AzureRmApplicationGatewaySku：添加了新的 sku Standard_v2 和 WAF_v2</span><span class="sxs-lookup"><span data-stu-id="2d59d-199">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="2d59d-200">使用最新的生成器版本重新生成了 RouteTable cmdlet</span><span class="sxs-lookup"><span data-stu-id="2d59d-200">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="2d59d-201">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="2d59d-201">AzureRM.Relay</span></span>
* <span data-ttu-id="2d59d-202">更新了 Markdown 文件，其中修复了示例中的参数名称问题</span><span class="sxs-lookup"><span data-stu-id="2d59d-202">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="2d59d-203">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="2d59d-203">AzureRM.Resources</span></span>
* <span data-ttu-id="2d59d-204">更新了 Roleassignment 和 roledefinition cmdlet：</span><span class="sxs-lookup"><span data-stu-id="2d59d-204">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="2d59d-205">删除了作为分页的一部分完成的额外 roledefinition 调用。</span><span class="sxs-lookup"><span data-stu-id="2d59d-205">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="2d59d-206">修复了 Get-AzureRmRoleAssignment cmdlet</span><span class="sxs-lookup"><span data-stu-id="2d59d-206">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="2d59d-207">修复了 -ExpandPrincipalGroups 命令参数功能</span><span class="sxs-lookup"><span data-stu-id="2d59d-207">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="2d59d-208">修复了“Get-AzureRmResource”的问题，其中“-ResourceType”参数区分大小写</span><span class="sxs-lookup"><span data-stu-id="2d59d-208">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="2d59d-209">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2d59d-209">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="2d59d-210">向列表 cmdlet 添加了 top 和 skip 参数</span><span class="sxs-lookup"><span data-stu-id="2d59d-210">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="2d59d-211">添加了标准到高级命名空间迁移 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="2d59d-211">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="2d59d-212">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="2d59d-212">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="2d59d-213">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="2d59d-213">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="2d59d-214">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="2d59d-214">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="2d59d-215">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="2d59d-215">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="2d59d-216">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="2d59d-216">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="2d59d-217">向 PSServiceBusDRConfigurationAttributes 类添加了一个只读属性“PendingReplicationOperationsCount”，该属性在复制过程中为挂起的复制操作计数</span><span class="sxs-lookup"><span data-stu-id="2d59d-217">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="2d59d-218">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2d59d-218">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="2d59d-219">更新了“New-AzureRmServiceFabricCluster”的示例</span><span class="sxs-lookup"><span data-stu-id="2d59d-219">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="2d59d-220">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="2d59d-220">AzureRM.Sql</span></span>
* <span data-ttu-id="2d59d-221">为 Management.Sql 添加新的 Cmdlet，以允许客户将 TDE 证书添加到 Sql Server 实例或托管实例</span><span class="sxs-lookup"><span data-stu-id="2d59d-221">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="2d59d-222">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="2d59d-222">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="2d59d-223">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="2d59d-223">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="2d59d-224">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="2d59d-224">AzureRM.Websites</span></span>
* <span data-ttu-id="2d59d-225">设置为 false 时，`Set-AzureRmWebApp -AssignIdentity` 和 `Set-AzureRmWebAppSlot -AssignIdentity` 现在将从站点对象中删除 Identity 属性。同时移除预览标记。</span><span class="sxs-lookup"><span data-stu-id="2d59d-225">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="2d59d-226">`Get-AzureRmWebAppMetrics`、`Get-AzureRmAppServicePlanMetrics` 示例已更新</span><span class="sxs-lookup"><span data-stu-id="2d59d-226">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="2d59d-227">`Set-AzureRmWebApp -PhpVersion` 支持 off 作为有效的 php 版本</span><span class="sxs-lookup"><span data-stu-id="2d59d-227">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="2d59d-228">6.4.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="2d59d-228">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="2d59d-229">常规</span><span class="sxs-lookup"><span data-stu-id="2d59d-229">General</span></span>
* <span data-ttu-id="2d59d-230">修复了大多数模块的帮助文件中的 OutputType 格式问题</span><span class="sxs-lookup"><span data-stu-id="2d59d-230">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="2d59d-231">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="2d59d-231">AzureRM.Profile</span></span>
* <span data-ttu-id="2d59d-232">已将 Ps1Xml 属性添加到基本输出类型</span><span class="sxs-lookup"><span data-stu-id="2d59d-232">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="2d59d-233">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="2d59d-233">AzureRM.Compute</span></span>
* <span data-ttu-id="2d59d-234">VMSS 的 IP 标记功能</span><span class="sxs-lookup"><span data-stu-id="2d59d-234">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="2d59d-235">已添加“New-AzureRmVmssIpTagConfig”cmdlet</span><span class="sxs-lookup"><span data-stu-id="2d59d-235">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="2d59d-236">已将 IpTag 参数添加到 New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="2d59d-236">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="2d59d-237">VMSS 的自动 OS 回滚功能</span><span class="sxs-lookup"><span data-stu-id="2d59d-237">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="2d59d-238">已将 DisableAutoRollback 参数添加到 New-AzureRmVmssConfig 和 Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2d59d-238">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="2d59d-239">VMSS 的 OS 升级历史记录功能</span><span class="sxs-lookup"><span data-stu-id="2d59d-239">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="2d59d-240">已将 OSUpgradeHistory 开关参数添加到 Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2d59d-240">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="2d59d-241">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="2d59d-241">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="2d59d-242">通过以下命令添加目录 ACL 的支持：</span><span class="sxs-lookup"><span data-stu-id="2d59d-242">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="2d59d-243">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="2d59d-243">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="2d59d-244">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="2d59d-244">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="2d59d-245">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="2d59d-245">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="2d59d-246">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2d59d-246">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="2d59d-247">为 Set-AzureRmDataLakeStoreItemAclEntry、Remove-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAcl 添加了取消支持和进度跟踪</span><span class="sxs-lookup"><span data-stu-id="2d59d-247">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="2d59d-248">为 Export-AzureRmDataLakeStoreChildItemProperties 添加了取消支持</span><span class="sxs-lookup"><span data-stu-id="2d59d-248">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="2d59d-249">修复了执行递归操作的 cmdlet 的调试消息刷新</span><span class="sxs-lookup"><span data-stu-id="2d59d-249">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="2d59d-250">修复了 DataLake cmdlet 的测试位置</span><span class="sxs-lookup"><span data-stu-id="2d59d-250">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="2d59d-251">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="2d59d-251">AzureRM.EventHub</span></span>
* <span data-ttu-id="2d59d-252">已将可选的 MaxCount 参数添加到“列出操作”cmdlet Get-AzureRmEventHub 和 Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="2d59d-252">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="2d59d-253">修复了 New-AzureRmEventHub cmdlet 的问题：创建新事件中心时至少需要一个参数。</span><span class="sxs-lookup"><span data-stu-id="2d59d-253">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="2d59d-254">提供了默认参数集。</span><span class="sxs-lookup"><span data-stu-id="2d59d-254">Provided Default Parameter set.</span></span>
* <span data-ttu-id="2d59d-255">已将可选参数 -KeyValue 添加到 New-AzureRmEventHubKey cmdlet，该参数可让用户提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="2d59d-255">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="2d59d-256">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2d59d-256">AzureRM.KeyVault</span></span>
* <span data-ttu-id="2d59d-257">修复了 Get-AzureRmKeyVault -Tag 返回所有资源的问题</span><span class="sxs-lookup"><span data-stu-id="2d59d-257">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="2d59d-258">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="2d59d-258">AzureRM.Network</span></span>
* <span data-ttu-id="2d59d-259">为区域冗余的 VirtualNetworkGateways 公开新 SKU</span><span class="sxs-lookup"><span data-stu-id="2d59d-259">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="2d59d-260">通过 ARM 为以下功能添加了新命令：ExpressRoute 合作伙伴 API</span><span class="sxs-lookup"><span data-stu-id="2d59d-260">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="2d59d-261">添加了 Get-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="2d59d-261">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="2d59d-262">添加了 Set-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="2d59d-262">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="2d59d-263">添加了 Add-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="2d59d-263">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="2d59d-264">添加了 Get-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="2d59d-264">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="2d59d-265">添加了 Remove-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="2d59d-265">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="2d59d-266">添加了 Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="2d59d-266">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="2d59d-267">添加了 Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="2d59d-267">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="2d59d-268">添加了 Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="2d59d-268">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="2d59d-269">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="2d59d-269">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="2d59d-270">添加了 Get-AzureRmRecoveryServicesBackupStatus cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2d59d-270">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="2d59d-271">此 cmdlet 采用 VM ID，并检查 VM 是否受订阅中的某个保管库保护。</span><span class="sxs-lookup"><span data-stu-id="2d59d-271">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="2d59d-272">如果存在此类保管库，该 cmdlet 会输出该保管库的详细信息。</span><span class="sxs-lookup"><span data-stu-id="2d59d-272">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="2d59d-273">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="2d59d-273">AzureRM.Resources</span></span>
* <span data-ttu-id="2d59d-274">更新了 Get-AzureRmPolicyAssignment cmdlet：</span><span class="sxs-lookup"><span data-stu-id="2d59d-274">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="2d59d-275">添加了在管理组级别列出 -Scope 值的支持</span><span class="sxs-lookup"><span data-stu-id="2d59d-275">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="2d59d-276">添加了在管理组级别使用 -Scope 值检索单个分配的支持</span><span class="sxs-lookup"><span data-stu-id="2d59d-276">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="2d59d-277">已将 -Effective 和 -All 开关添加到 control 参数</span><span class="sxs-lookup"><span data-stu-id="2d59d-277">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="2d59d-278">更新了 Get/New/Remove/Set-AzureRmPolicyDefinition cmdlet</span><span class="sxs-lookup"><span data-stu-id="2d59d-278">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="2d59d-279">添加了 -ManagementGroupName 参数，以将操作应用到给定的管理组</span><span class="sxs-lookup"><span data-stu-id="2d59d-279">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="2d59d-280">添加了 -SubscriptionId 参数，以将操作应用到给定的订阅</span><span class="sxs-lookup"><span data-stu-id="2d59d-280">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="2d59d-281">更新了 Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlet</span><span class="sxs-lookup"><span data-stu-id="2d59d-281">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="2d59d-282">添加了 -ManagementGroupName 参数，以将操作应用到给定的管理组</span><span class="sxs-lookup"><span data-stu-id="2d59d-282">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="2d59d-283">添加了 -SubscriptionId 参数，以将操作应用到给定的订阅</span><span class="sxs-lookup"><span data-stu-id="2d59d-283">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="2d59d-284">添加了使用 TemplateParameterObject 时在参数中指定 KeyVault 机密引用的支持</span><span class="sxs-lookup"><span data-stu-id="2d59d-284">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="2d59d-285">修复了忽略“New-AzureRmADAppCredential”的“-EndDate”参数的问题</span><span class="sxs-lookup"><span data-stu-id="2d59d-285">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="2d59d-286">修复了“Add-AzureRmADGroupMember”使用错误的 URL 发出请求的问题</span><span class="sxs-lookup"><span data-stu-id="2d59d-286">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="2d59d-287">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2d59d-287">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="2d59d-288">已将可选参数 -KeyValue 添加到 New-AzureRmServiceBusKey cmdlet，该参数可让用户提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="2d59d-288">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="2d59d-289">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="2d59d-289">AzureRM.Sql</span></span>
* <span data-ttu-id="2d59d-290">在 AzureRmSqlDatabaseRestorePoint 帮助中澄清了 SQLDW 的用户定义还原点</span><span class="sxs-lookup"><span data-stu-id="2d59d-290">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="2d59d-291">更新了多个 cmdlet 中 -ComputeGeneration 参数的文档</span><span class="sxs-lookup"><span data-stu-id="2d59d-291">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="2d59d-292">6.3.0 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="2d59d-292">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="2d59d-293">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="2d59d-293">AzureRM.Profile</span></span>
* <span data-ttu-id="2d59d-294">更新了 Enable-AzureRmContextAutoSave 的错误消息</span><span class="sxs-lookup"><span data-stu-id="2d59d-294">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="2d59d-295">在运行没有旧上下文的“Connect-AzureRmAccount”时为每个订阅创建一个上下文</span><span class="sxs-lookup"><span data-stu-id="2d59d-295">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="2d59d-296">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="2d59d-296">Azure.Storage</span></span>
* <span data-ttu-id="2d59d-297">在帮助文件中增加了关于 -Permissions 参数的其他信息。</span><span class="sxs-lookup"><span data-stu-id="2d59d-297">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="2d59d-298">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="2d59d-298">AzureRM.Compute</span></span>
* <span data-ttu-id="2d59d-299">“Get-AzureRmVmDiskEncryptionStatus”修复了一个针对没有数据磁盘的 VM 观察到的问题</span><span class="sxs-lookup"><span data-stu-id="2d59d-299">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="2d59d-300">更新计算客户端库版本以修复以下 cmdlet</span><span class="sxs-lookup"><span data-stu-id="2d59d-300">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="2d59d-301">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="2d59d-301">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="2d59d-302">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="2d59d-302">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="2d59d-303">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="2d59d-303">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="2d59d-304">修复了以下 cmdlet，因此可以正确地显示“操作 ID”和“操作状态”：</span><span class="sxs-lookup"><span data-stu-id="2d59d-304">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="2d59d-305">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="2d59d-305">Start-AzureRmVM</span></span>
    - <span data-ttu-id="2d59d-306">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="2d59d-306">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="2d59d-307">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="2d59d-307">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="2d59d-308">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="2d59d-308">Set-AzureRmVM</span></span>
    - <span data-ttu-id="2d59d-309">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="2d59d-309">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="2d59d-310">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2d59d-310">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="2d59d-311">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="2d59d-311">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="2d59d-312">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="2d59d-312">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="2d59d-313">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2d59d-313">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="2d59d-314">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2d59d-314">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="2d59d-315">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2d59d-315">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="2d59d-316">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2d59d-316">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="2d59d-317">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="2d59d-317">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="2d59d-318">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="2d59d-318">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="2d59d-319">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="2d59d-319">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="2d59d-320">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="2d59d-320">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="2d59d-321">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="2d59d-321">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="2d59d-322">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="2d59d-322">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="2d59d-323">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="2d59d-323">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="2d59d-324">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="2d59d-324">AzureRM.EventGrid</span></span>
* <span data-ttu-id="2d59d-325">在 Update-AzureRmEventGridSubscription cmdlet 中删除 SubjectBeginsWith/SubjectEndsWith 的 ValidateNotNullOrEmpty 验证条件，允许根据需要将这些参数更改为空字符串。</span><span class="sxs-lookup"><span data-stu-id="2d59d-325">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="2d59d-326">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2d59d-326">AzureRM.KeyVault</span></span>
* <span data-ttu-id="2d59d-327">修复运行 Get-AzureRmKeyVault -Tag 时不返回任何标记的问题</span><span class="sxs-lookup"><span data-stu-id="2d59d-327">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="2d59d-328">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="2d59d-328">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="2d59d-329">策略见解 cmdlet 的公开发行版</span><span class="sxs-lookup"><span data-stu-id="2d59d-329">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="2d59d-330">使用 API 版本 2018-04-04</span><span class="sxs-lookup"><span data-stu-id="2d59d-330">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="2d59d-331">向 Get-AzureRmPolicyStateSummary 的结果添加了 PolicyDefinitionReferenceId</span><span class="sxs-lookup"><span data-stu-id="2d59d-331">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="2d59d-332">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="2d59d-332">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="2d59d-333">向 RecoveryServices.Backup cmdlet 添加了 -Vault 参数。</span><span class="sxs-lookup"><span data-stu-id="2d59d-333">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="2d59d-334">传递时，此项会替代 Set-AzureRmRecoveryServicesContext cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2d59d-334">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="2d59d-335">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="2d59d-335">AzureRM.Sql</span></span>
* <span data-ttu-id="2d59d-336">更新了 Get-AzureRmSqlDatabaseExpanded 的帮助文件中的示例</span><span class="sxs-lookup"><span data-stu-id="2d59d-336">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="2d59d-337">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="2d59d-337">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="2d59d-338">更新了 Add-AzureRmTrafficManagerEndpointConfig 的帮助文件</span><span class="sxs-lookup"><span data-stu-id="2d59d-338">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="2d59d-339">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="2d59d-339">AzureRM.Websites</span></span>
* <span data-ttu-id="2d59d-340">更新了“Set-AzureRmWebApp”，在使用 -AssignIdentity 时不覆盖 AppSettings</span><span class="sxs-lookup"><span data-stu-id="2d59d-340">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="2d59d-341">更新了“New-AzureRmWebAppSlot”，允许使用 AppServicePlan 作为可选参数</span><span class="sxs-lookup"><span data-stu-id="2d59d-341">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="2d59d-342">6.2.1 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="2d59d-342">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="2d59d-343">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2d59d-343">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="2d59d-344">更新了 PSWorkspace 模型，允许 Network 使用 type 作为参数</span><span class="sxs-lookup"><span data-stu-id="2d59d-344">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="2d59d-345">6.2.0 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="2d59d-345">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="2d59d-346">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="2d59d-346">AzureRM.Profile</span></span>
* <span data-ttu-id="2d59d-347">修复了 Newtonsoft.Json 的版本 10.0.3 在模块导入时无法加载的问题</span><span class="sxs-lookup"><span data-stu-id="2d59d-347">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="2d59d-348">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="2d59d-348">AzureRM.Compute</span></span>
* <span data-ttu-id="2d59d-349">VMSS VM 更新功能</span><span class="sxs-lookup"><span data-stu-id="2d59d-349">VMSS VM Update feature</span></span>
    - <span data-ttu-id="2d59d-350">增加了“Update-AzureRmVmssVM”和“New-AzureRmVMDataDisk”cmdlet</span><span class="sxs-lookup"><span data-stu-id="2d59d-350">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="2d59d-351">为“Add-AzureRmVMDataDisk”cmdlet 增加了 VirtualMachineScaleSetVM 参数，支持向 Vmss VM 添加数据磁盘。</span><span class="sxs-lookup"><span data-stu-id="2d59d-351">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="2d59d-352">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="2d59d-352">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="2d59d-353">将 ADF.Net SDK 版本更新到了 0.8.0-preview，其中包含以下更改：</span><span class="sxs-lookup"><span data-stu-id="2d59d-353">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="2d59d-354">增加了“配置工厂存储库”操作</span><span class="sxs-lookup"><span data-stu-id="2d59d-354">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="2d59d-355">更新了 QuickBooks LinkedService，可以公开 consumerKey 和 consumerSecret 属性</span><span class="sxs-lookup"><span data-stu-id="2d59d-355">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="2d59d-356">已将多个模型类型从 SecretBase 更新为 Object</span><span class="sxs-lookup"><span data-stu-id="2d59d-356">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="2d59d-357">增加了 Blob 事件触发器</span><span class="sxs-lookup"><span data-stu-id="2d59d-357">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="2d59d-358">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2d59d-358">AzureRM.KeyVault</span></span>
* <span data-ttu-id="2d59d-359">使用示例输出更新了文档</span><span class="sxs-lookup"><span data-stu-id="2d59d-359">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="2d59d-360">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="2d59d-360">AzureRM.Network</span></span>
* <span data-ttu-id="2d59d-361">在网络观察程序 cmdlet 上启用了流量分析参数</span><span class="sxs-lookup"><span data-stu-id="2d59d-361">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="2d59d-362">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="2d59d-362">AzureRM.Resources</span></span>
* <span data-ttu-id="2d59d-363">修复了从“Get-AzureRmResource”返回的“PSResource”对象的“Properties”属性问题</span><span class="sxs-lookup"><span data-stu-id="2d59d-363">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="2d59d-364">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="2d59d-364">AzureRM.Scheduler</span></span>
* <span data-ttu-id="2d59d-365">修复了更新 ServiceBusQueueJob 无法设置新 Auth 值的问题</span><span class="sxs-lookup"><span data-stu-id="2d59d-365">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="2d59d-366">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="2d59d-366">AzureRM.Sql</span></span>
* <span data-ttu-id="2d59d-367">使用可选的 LicenseType 参数更新了以下 cmdlet</span><span class="sxs-lookup"><span data-stu-id="2d59d-367">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="2d59d-368">New-AzureRmSqlDatabase；Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2d59d-368">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="2d59d-369">New-AzureRmSqlElasticPool；Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="2d59d-369">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="2d59d-370">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="2d59d-370">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="2d59d-371">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="2d59d-371">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="2d59d-372">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2d59d-372">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="2d59d-373">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="2d59d-373">AzureRM.Websites</span></span>
* <span data-ttu-id="2d59d-374">更新了“New-AzureRMWebApp”，可以使用策略库中的常用算法。</span><span class="sxs-lookup"><span data-stu-id="2d59d-374">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="2d59d-375">6.1.0 - 2018 年 5 月</span><span class="sxs-lookup"><span data-stu-id="2d59d-375">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="2d59d-376">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="2d59d-376">AzureRM.Profile</span></span>
* <span data-ttu-id="2d59d-377">修复了运行“Clear-AzureRmContext”时会保留空上下文的问题，该上下文使用旧的默认上下文的名称，导致用户无法使用旧名称创建新的上下文</span><span class="sxs-lookup"><span data-stu-id="2d59d-377">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="2d59d-378">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="2d59d-378">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="2d59d-379">允许在 AS 上执行网关的关联/取消关联操作。</span><span class="sxs-lookup"><span data-stu-id="2d59d-379">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="2d59d-380">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2d59d-380">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="2d59d-381">增加了对 ApiVersions、ApiReleases 和 ApiRevisions 的支持</span><span class="sxs-lookup"><span data-stu-id="2d59d-381">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="2d59d-382">增加了对 ServiceFabric 后端的支持</span><span class="sxs-lookup"><span data-stu-id="2d59d-382">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="2d59d-383">增加了对 Application Insights Logger 的支持</span><span class="sxs-lookup"><span data-stu-id="2d59d-383">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="2d59d-384">增加的支持包括认可“基本”SKU 是 API 管理服务的有效 SKU</span><span class="sxs-lookup"><span data-stu-id="2d59d-384">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="2d59d-385">增加的支持包括允许将专用 CA 颁发的证书作为根证书或 CA 证书安装</span><span class="sxs-lookup"><span data-stu-id="2d59d-385">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="2d59d-386">增加的支持包括通过 KeyVault 和多个代理主机名接受自定义 SSL 证书</span><span class="sxs-lookup"><span data-stu-id="2d59d-386">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="2d59d-387">增加了对 MSI 标识的支持</span><span class="sxs-lookup"><span data-stu-id="2d59d-387">Added support for MSI identity</span></span>
* <span data-ttu-id="2d59d-388">增加的支持包括通过 URL 接受策略 注意：以下 cmdlet 将在未来版本中弃用</span><span class="sxs-lookup"><span data-stu-id="2d59d-388">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="2d59d-389">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="2d59d-389">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="2d59d-390">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d59d-390">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="2d59d-391">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="2d59d-391">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="2d59d-392">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="2d59d-392">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="2d59d-393">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="2d59d-393">AzureRM.Batch</span></span>
* <span data-ttu-id="2d59d-394">发布新 cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="2d59d-394">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="2d59d-395">发布新 cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="2d59d-395">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="2d59d-396">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="2d59d-396">AzureRM.Consumption</span></span>
* <span data-ttu-id="2d59d-397">在 Cmdlet Get-AzureRmConsumptionUsageDetail 中增加了新参数 Expand、ResourceGroup、InstanceName、InstanceId、Tags、Top</span><span class="sxs-lookup"><span data-stu-id="2d59d-397">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="2d59d-398">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2d59d-398">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="2d59d-399">修复了 Export-AzureRmDataLakeStoreChildItemProperties 的示例</span><span class="sxs-lookup"><span data-stu-id="2d59d-399">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="2d59d-400">修复了 Set-AzureRmDataLakeStoreItemAclEntry 中 Recurse 用例的 null 参数异常</span><span class="sxs-lookup"><span data-stu-id="2d59d-400">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="2d59d-401">修复了 Set-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAcl、Remove-AzureRmDataLakeStoreItemAclEntry 的帮助文件</span><span class="sxs-lookup"><span data-stu-id="2d59d-401">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="2d59d-402">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="2d59d-402">AzureRM.Network</span></span>
* <span data-ttu-id="2d59d-403">将网络 SDK 版本从 18.0.0-preview 升至 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="2d59d-403">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="2d59d-404">增加了用于创建协议配置的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="2d59d-404">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="2d59d-405">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d59d-405">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="2d59d-406">增加了用于向现有的快速路由线路添加新的线路连接的 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2d59d-406">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="2d59d-407">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="2d59d-407">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="2d59d-408">增加了用于从现有的快速路由线路删除线路连接的 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2d59d-408">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="2d59d-409">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="2d59d-409">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="2d59d-410">增加了用于检索线路连接的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="2d59d-410">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="2d59d-411">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="2d59d-411">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="2d59d-412">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2d59d-412">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="2d59d-413">修复了使用生成的证书进行服务器身份验证的问题（问题 5998）</span><span class="sxs-lookup"><span data-stu-id="2d59d-413">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="2d59d-414">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="2d59d-414">AzureRM.Sql</span></span>
* <span data-ttu-id="2d59d-415">更新了审核 cmdlet，允许删除 AuditActions 或 AuditActionGroups</span><span class="sxs-lookup"><span data-stu-id="2d59d-415">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="2d59d-416">修复了设置新的灵活保留策略时使用 Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy 出现的问题。该问题的具体表现是：在命令失败的同时，出现“不再支持使用 Azure 恢复服务保管库和策略配置长期保留策略。</span><span class="sxs-lookup"><span data-stu-id="2d59d-416">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="2d59d-417">请使用新的灵活保留策略提交请求”错误消息。</span><span class="sxs-lookup"><span data-stu-id="2d59d-417">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="2d59d-418">更新了与 Azure SQL 数据库/ElasticPool 的创建/更新相关的所有 cmdlet，允许使用新的数据库 API，而这些 cmdlet 支持的 SKU 属性则适用于规模和层相关属性。</span><span class="sxs-lookup"><span data-stu-id="2d59d-418">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="2d59d-419">更新的 cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="2d59d-419">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="2d59d-420">New-AzureRmSqlDatabase；Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2d59d-420">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="2d59d-421">New-AzureRmSqlElasticPool；Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="2d59d-421">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="2d59d-422">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="2d59d-422">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="2d59d-423">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="2d59d-423">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="2d59d-424">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2d59d-424">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="2d59d-425">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="2d59d-425">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="2d59d-426">更新了“Get-AzureRmTrafficManagerProfile”的参数，要求在使用 -Name 参数时使用 -ResourceGroupName 参数。</span><span class="sxs-lookup"><span data-stu-id="2d59d-426">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
