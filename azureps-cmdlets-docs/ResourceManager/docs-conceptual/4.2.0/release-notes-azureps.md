---
title: "Azure PowerShell 更改日志 | Microsoft Docs"
description: "下面提供了对 Azure PowerShell 最新版本所做更改的历史记录。"
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.service: azure-resource-manager
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: 
ms.date: 05/18/2017
ms.openlocfilehash: 5c8fa2a5a8f94cd24b66f42c237749a7b89af3b3
ms.sourcegitcommit: ec0b3565264ff7c9f03315ded182f3d5cce534fc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/13/2017
---
# <a name="release-notes"></a><span data-ttu-id="477e7-103">发行说明</span><span class="sxs-lookup"><span data-stu-id="477e7-103">Release notes</span></span>

<span data-ttu-id="477e7-104">下面是此版本中对 Azure PowerShell 所做的更改列表。</span><span class="sxs-lookup"><span data-stu-id="477e7-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

## <a name="version-400"></a><span data-ttu-id="477e7-105">版本 4.0.0</span><span class="sxs-lookup"><span data-stu-id="477e7-105">Version 4.0.0</span></span>

* <span data-ttu-id="477e7-106">此版本包含重大更改。</span><span class="sxs-lookup"><span data-stu-id="477e7-106">This release contains breaking changes.</span></span> <span data-ttu-id="477e7-107">请参阅[迁移指南](https://aka.ms/azps-migration-guide)，了解有关更改的详细信息及其对现有脚本的影响。</span><span class="sxs-lookup"><span data-stu-id="477e7-107">Please see [the migration guide](https://aka.ms/azps-migration-guide) for change details and the impact on existing scripts.</span></span>
* <span data-ttu-id="477e7-108">ApiManagement</span><span class="sxs-lookup"><span data-stu-id="477e7-108">ApiManagement</span></span>
  - <span data-ttu-id="477e7-109">添加了在 New-AzureRmApiManagementGroup 中配置外部组的支持。</span><span class="sxs-lookup"><span data-stu-id="477e7-109">Added support for configuring external groups in New-AzureRmApiManagementGroup.</span></span>
* <span data-ttu-id="477e7-110">计费</span><span class="sxs-lookup"><span data-stu-id="477e7-110">Billing</span></span>
  - <span data-ttu-id="477e7-111">全新 Cmdlet Get-AzureRmBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="477e7-111">New Cmdlet Get-AzureRmBillingPeriod</span></span>
    + <span data-ttu-id="477e7-112">用于检索订阅的 Azure 计费周期的 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="477e7-112">cmdlet to retrieve azure billing periods of the subscription.</span></span>
  - <span data-ttu-id="477e7-113">更新 Cmdlet Get-AzureRmBillingInvoice</span><span class="sxs-lookup"><span data-stu-id="477e7-113">Update Cmdlet Get-AzureRmBillingInvoice</span></span>
  - <span data-ttu-id="477e7-114">新属性 BillingPeriodNames</span><span class="sxs-lookup"><span data-stu-id="477e7-114">new property BillingPeriodNames</span></span>
  - <span data-ttu-id="477e7-115">列表视图中的输出</span><span class="sxs-lookup"><span data-stu-id="477e7-115">output in list view</span></span>
* <span data-ttu-id="477e7-116">计算</span><span class="sxs-lookup"><span data-stu-id="477e7-116">Compute</span></span>
  - <span data-ttu-id="477e7-117">更新了 Set-AzureRmVMAEMExtension 和 Test-AzureRmVMAEMExtension cmdlet，以支持高级托管磁盘</span><span class="sxs-lookup"><span data-stu-id="477e7-117">Updated Set-AzureRmVMAEMExtension and Test-AzureRmVMAEMExtension cmdlets to support Premium managed disks</span></span>
  - <span data-ttu-id="477e7-118">用于 IaaS VM 和故障还原的备份加密设置</span><span class="sxs-lookup"><span data-stu-id="477e7-118">Backup encryption settings for IaaS VMs and restore on failure</span></span>
  - <span data-ttu-id="477e7-119">ChefServiceInterval 选项现已重命名为 ChefDaemonInterval。</span><span class="sxs-lookup"><span data-stu-id="477e7-119">ChefServiceInterval option is renamed to ChefDaemonInterval now.</span></span> <span data-ttu-id="477e7-120">但旧名称仍可继续使用。</span><span class="sxs-lookup"><span data-stu-id="477e7-120">Old one will continue to work however.</span></span>
  - <span data-ttu-id="477e7-121">从 PS VM 对象中删除重复的 DataDiskNames 和 NetworkInterfaceIDs 属性。</span><span class="sxs-lookup"><span data-stu-id="477e7-121">Remove duplicated DataDiskNames and NetworkInterfaceIDs properties from PS VM object.</span></span>
  - <span data-ttu-id="477e7-122">让 DataDiskNames 参数在 Remove-AzureRmVMDataDisk 中、NetworkInterfaceIDs 参数在 Remove-AzureRmVMNetworkInterface 中变为可选。</span><span class="sxs-lookup"><span data-stu-id="477e7-122">Make DataDiskNames and NetworkInterfaceIDs parameters optional in Remove-AzureRmVMDataDisk and Remove-AzureRmVMNetworkInterface, respectively.</span></span>
  - <span data-ttu-id="477e7-123">修复 Get cmdlet 返回列表对象时的 Get cmdlet 管道问题。</span><span class="sxs-lookup"><span data-stu-id="477e7-123">Fix the piping issue of Get cmdlets when the Get cmdlets return a list object.</span></span>
  - <span data-ttu-id="477e7-124">已重命名与 RDFE cmdlet 冲突的 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="477e7-124">Cmdlets that conflicted with RDFE cmdlets have been renamed.</span></span> <span data-ttu-id="477e7-125">有关详细信息，请参阅“问题”https://github.com/Azure/azure-powershell/issues/2917</span><span class="sxs-lookup"><span data-stu-id="477e7-125">See issue https://github.com/Azure/azure-powershell/issues/2917 for more details</span></span>
    + <span data-ttu-id="477e7-126">`New-AzureVMSqlServerAutoBackupConfig` 已重名为 `New-AzureRmVMSqlServerAutoBackupConfig`</span><span class="sxs-lookup"><span data-stu-id="477e7-126">`New-AzureVMSqlServerAutoBackupConfig` has been renamed to `New-AzureRmVMSqlServerAutoBackupConfig`</span></span>
    + <span data-ttu-id="477e7-127">`New-AzureVMSqlServerAutoPatchingConfig` 已重名为 `New-AzureRmVMSqlServerAutoPatchingConfig`</span><span class="sxs-lookup"><span data-stu-id="477e7-127">`New-AzureVMSqlServerAutoPatchingConfig` has been renamed to `New-AzureRmVMSqlServerAutoPatchingConfig`</span></span>
    + <span data-ttu-id="477e7-128">`New-AzureVMSqlServerKeyVaultCredentialConfig` 已重名为 `New-AzureRmVMSqlServerKeyVaultCredentialConfig`</span><span class="sxs-lookup"><span data-stu-id="477e7-128">`New-AzureVMSqlServerKeyVaultCredentialConfig` has been renamed to `New-AzureRmVMSqlServerKeyVaultCredentialConfig`</span></span>
* <span data-ttu-id="477e7-129">消耗</span><span class="sxs-lookup"><span data-stu-id="477e7-129">Consumption</span></span>
  - <span data-ttu-id="477e7-130">新 Cmdlet Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="477e7-130">New Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>
    + <span data-ttu-id="477e7-131">用于检索订阅详细使用情况的 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="477e7-131">cmdlet to retrieve usage details of the subscription.</span></span>
* <span data-ttu-id="477e7-132">ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="477e7-132">ContainerRegistry</span></span>
  - <span data-ttu-id="477e7-133">为 Azure 容器注册表添加 PowerShell cmdlet</span><span class="sxs-lookup"><span data-stu-id="477e7-133">Add PowerShell cmdlets for Azure Container Registry</span></span>
    + <span data-ttu-id="477e7-134">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="477e7-134">New-AzureRmContainerRegistry</span></span>
    + <span data-ttu-id="477e7-135">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="477e7-135">Get-AzureRmContainerRegistry</span></span>
    + <span data-ttu-id="477e7-136">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="477e7-136">Update-AzureRmContainerRegistry</span></span>
    + <span data-ttu-id="477e7-137">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="477e7-137">Remove-AzureRmContainerRegistry</span></span>
    + <span data-ttu-id="477e7-138">Get-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="477e7-138">Get-AzureRmContainerRegistryCredential</span></span>
    + <span data-ttu-id="477e7-139">Update-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="477e7-139">Update-AzureRmContainerRegistryCredential</span></span>
    + <span data-ttu-id="477e7-140">Test-AzureRmContainerRegistryNameAvailability</span><span class="sxs-lookup"><span data-stu-id="477e7-140">Test-AzureRmContainerRegistryNameAvailability</span></span>
* <span data-ttu-id="477e7-141">DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="477e7-141">DataLakeAnalytics</span></span>
  - <span data-ttu-id="477e7-142">添加对获取和列出目录包的支持</span><span class="sxs-lookup"><span data-stu-id="477e7-142">Add support for catalog package get and list</span></span>
  - <span data-ttu-id="477e7-143">添加了从更深上级列出以下目录项的支持：</span><span class="sxs-lookup"><span data-stu-id="477e7-143">Add support for listing the following catalog items from deeper ancestors:</span></span>
    + <span data-ttu-id="477e7-144">表</span><span class="sxs-lookup"><span data-stu-id="477e7-144">Table</span></span>
    + <span data-ttu-id="477e7-145">TVF</span><span class="sxs-lookup"><span data-stu-id="477e7-145">TVF</span></span>
    + <span data-ttu-id="477e7-146">查看</span><span class="sxs-lookup"><span data-stu-id="477e7-146">View</span></span>
    + <span data-ttu-id="477e7-147">统计信息</span><span class="sxs-lookup"><span data-stu-id="477e7-147">Statistics</span></span>
* <span data-ttu-id="477e7-148">DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="477e7-148">DataLakeStore</span></span>
  - <span data-ttu-id="477e7-149">对于 `Import-AzureRMDataLakeStoreItem` 和 `Export-AzureRMDataLakeStoreItem`，默认情况下禁用跟踪日志记录功能以提高性能。</span><span class="sxs-lookup"><span data-stu-id="477e7-149">For `Import-AzureRMDataLakeStoreItem` and `Export-AzureRMDataLakeStoreItem` trace logging has been disabled by default to improve performance.</span></span> <span data-ttu-id="477e7-150">如果需要跟踪日志记录，请使用 `-DiagnosticLogLevel` 和 `-DiagnosticLogPath` 参数</span><span class="sxs-lookup"><span data-stu-id="477e7-150">If trace logging is desired please use the `-DiagnosticLogLevel` and `-DiagnosticLogPath` parameters</span></span>
  - <span data-ttu-id="477e7-151">修复了向 ADLS 上传大量小文件时可能导致 PowerShell 崩溃的 bug。</span><span class="sxs-lookup"><span data-stu-id="477e7-151">Fixed a bug that would sometimes cause PowerShell to crash when uploading lots of small file to ADLS.</span></span>
* <span data-ttu-id="477e7-152">EventHub</span><span class="sxs-lookup"><span data-stu-id="477e7-152">EventHub</span></span>
  - <span data-ttu-id="477e7-153">Bug 修复：</span><span class="sxs-lookup"><span data-stu-id="477e7-153">Bug fix :</span></span>
    + <span data-ttu-id="477e7-154">修复 Set-AzureRmEventHubNamespace cmdlet 错误 -“层”不能为 null，应为“SkuName”</span><span class="sxs-lookup"><span data-stu-id="477e7-154">Fix for Set-AzureRmEventHubNamespace cmdlet error  - 'Tier' cannot be null, where it should be 'SkuName'</span></span>
    + <span data-ttu-id="477e7-155">Set-AzureRmEventHub - 修复更新 EventHub 时出现的“未将对象引用设置为对象的实例”错误</span><span class="sxs-lookup"><span data-stu-id="477e7-155">Set-AzureRmEventHub - Fix 'Object reference not set to an instance of an object' error while updating EventHub</span></span>
* <span data-ttu-id="477e7-156">洞察力</span><span class="sxs-lookup"><span data-stu-id="477e7-156">Insights</span></span>
  - <span data-ttu-id="477e7-157">Add-AzureRm*AlertRule</span><span class="sxs-lookup"><span data-stu-id="477e7-157">Add-AzureRm*AlertRule</span></span>
    + <span data-ttu-id="477e7-158">返回单个对象：newResource、statusCode、requestId</span><span class="sxs-lookup"><span data-stu-id="477e7-158">Returns a single object: newResource, statusCode, requestId</span></span>
  - <span data-ttu-id="477e7-159">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="477e7-159">Get-AzureRmAlertRule</span></span>
    + <span data-ttu-id="477e7-160">现会枚举输出，而不是将其视作单个对象。</span><span class="sxs-lookup"><span data-stu-id="477e7-160">The output is now enumerated instead of considered a single object.</span></span> <span data-ttu-id="477e7-161">其类型未发生更改，仍为列表。</span><span class="sxs-lookup"><span data-stu-id="477e7-161">Its type did not change, it is still a list.</span></span>
  - <span data-ttu-id="477e7-162">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="477e7-162">Remove-AzureRmAlertRule</span></span>
    + <span data-ttu-id="477e7-163">statusCode 遵循请求返回的状态代码，而之前其状态始终为“确定”。</span><span class="sxs-lookup"><span data-stu-id="477e7-163">The statusCode follows the status code returned by the request, before it was Ok always.</span></span>
  - <span data-ttu-id="477e7-164">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="477e7-164">Add-AzureRmAutoscaleSetting</span></span>
    + <span data-ttu-id="477e7-165">现在返回单个对象（以前返回列表），其中包含 statusCode、requestId 和新创建/更新的资源。</span><span class="sxs-lookup"><span data-stu-id="477e7-165">Returns now a single object (not a list as before) containing statusCode, requestId, and the newly created/updated resource.</span></span>
    + <span data-ttu-id="477e7-166">状态代码遵循请求返回的状态，之前其状态始终为“确定”。</span><span class="sxs-lookup"><span data-stu-id="477e7-166">The status code follows the status returned by the request, before it was always Ok.</span></span>
  - <span data-ttu-id="477e7-167">New-AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="477e7-167">New-AzureRmAutoscaleRule</span></span>
    + <span data-ttu-id="477e7-168">已扩展参数 ScaleActionType，该参数现接收以下值：ChangeCount、PercentChangeCount、ExactCount。</span><span class="sxs-lookup"><span data-stu-id="477e7-168">The parameter ScaleActionType has been extended, it receives the following values now: ChangeCount, PercentChangeCount, ExactCount.</span></span>
  - <span data-ttu-id="477e7-169">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="477e7-169">Remove-AzureRmAutoscaleSetting</span></span>
    + <span data-ttu-id="477e7-170">输出中的 statusCode 遵循请求返回的状态代码。</span><span class="sxs-lookup"><span data-stu-id="477e7-170">The statusCode in the output follows the statusCode returned by the request.</span></span> <span data-ttu-id="477e7-171">之前其状态始终为“确定”。</span><span class="sxs-lookup"><span data-stu-id="477e7-171">Before it was always Ok.</span></span>
  - <span data-ttu-id="477e7-172">Get-AzureRMLogProfile</span><span class="sxs-lookup"><span data-stu-id="477e7-172">Get-AzureRMLogProfile</span></span>
    + <span data-ttu-id="477e7-173">现会枚举输出。</span><span class="sxs-lookup"><span data-stu-id="477e7-173">The output is now enumerated.</span></span> <span data-ttu-id="477e7-174">以前将其视作单个对象。</span><span class="sxs-lookup"><span data-stu-id="477e7-174">Before it was considered a single object.</span></span> <span data-ttu-id="477e7-175">和以前一样，输出类型仍为列表。</span><span class="sxs-lookup"><span data-stu-id="477e7-175">The type of the output remains a list as before.</span></span>
  - <span data-ttu-id="477e7-176">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="477e7-176">Remove-AzureRmLogProfile</span></span>
    + <span data-ttu-id="477e7-177">已实现 PassThru 参数。</span><span class="sxs-lookup"><span data-stu-id="477e7-177">The PassThru parameter has been implemented.</span></span>
  - <span data-ttu-id="477e7-178">指标 API</span><span class="sxs-lookup"><span data-stu-id="477e7-178">Metrics API</span></span>
    + <span data-ttu-id="477e7-179">SDK 现从 MDM 检索指标。</span><span class="sxs-lookup"><span data-stu-id="477e7-179">The SDK now retrieves metrics from MDM.</span></span>
  - <span data-ttu-id="477e7-180">Get-AzureRmMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="477e7-180">Get-AzureRmMetricDefinition</span></span>
    + <span data-ttu-id="477e7-181">输出仍为列表，但列表的结构有所更改。</span><span class="sxs-lookup"><span data-stu-id="477e7-181">The output is still a list, but the structure of the list changed.</span></span>
  - <span data-ttu-id="477e7-182">Get-AzureRmMetric</span><span class="sxs-lookup"><span data-stu-id="477e7-182">Get-AzureRmMetric</span></span>
    + <span data-ttu-id="477e7-183">已更改调用。</span><span class="sxs-lookup"><span data-stu-id="477e7-183">The call has changed.</span></span> <span data-ttu-id="477e7-184">新语法为： Get-AzureRmMetric ResourceId [MetricNames [TimeGrain] [AggregationType] [StartTime] [EndTime]] [DetailedOutput]</span><span class="sxs-lookup"><span data-stu-id="477e7-184">This is the new syntax: Get-AzureRmMetric ResourceId [MetricNames [TimeGrain] [AggregationType] [StartTime] [EndTime]] [DetailedOutput]</span></span>
    + <span data-ttu-id="477e7-185">输出为列表，其元素的结构有所更改。</span><span class="sxs-lookup"><span data-stu-id="477e7-185">The output is a list, and the structure of its elements has changed.</span></span>
* <span data-ttu-id="477e7-186">KeyVault</span><span class="sxs-lookup"><span data-stu-id="477e7-186">KeyVault</span></span>
  - <span data-ttu-id="477e7-187">添加对 KeyVault 机密的备份/还原支持</span><span class="sxs-lookup"><span data-stu-id="477e7-187">Adding backup/restore support for KeyVault secrets</span></span>
    + <span data-ttu-id="477e7-188">可备份和还原机密，这与当前支持的密钥功能相符</span><span class="sxs-lookup"><span data-stu-id="477e7-188">Secrets can be backed up and restored, matching the functionality currently supported for Keys</span></span>

  - <span data-ttu-id="477e7-189">密钥和机密的备份 cmdlet 现在接受相应对象作为输入参数</span><span class="sxs-lookup"><span data-stu-id="477e7-189">Backup cmdlets for Keys and Secrets now accept a corresponding object as an input parameter</span></span>
    + <span data-ttu-id="477e7-190">调用方可能捆绑检索和备份操作：Get-AzureKeyVaultKey -VaultName myVault -Name myKey | Backup-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="477e7-190">The caller may chain retrieval and backup operations: Get-AzureKeyVaultKey -VaultName myVault -Name myKey | Backup-AzureKeyVaultKey</span></span>

  - <span data-ttu-id="477e7-191">备份 cmdlet 现支持 -Force 开关以覆盖现有文件</span><span class="sxs-lookup"><span data-stu-id="477e7-191">Backup cmdlets now support a -Force switch to overwrite an existing file</span></span>
    + <span data-ttu-id="477e7-192">请注意：尝试覆盖现有文件这一操作不再引发，而是提示用户选择继续操作的方式。</span><span class="sxs-lookup"><span data-stu-id="477e7-192">Note that attempting to overwrite an existing file will no longer throw, and will instead prompt the user for a choice on how to proceed.</span></span>
* <span data-ttu-id="477e7-193">LogicApp</span><span class="sxs-lookup"><span data-stu-id="477e7-193">LogicApp</span></span>
  - <span data-ttu-id="477e7-194">交换控制编号灾难恢复 cmdlet 的新参数：</span><span class="sxs-lookup"><span data-stu-id="477e7-194">New parameters for Interchange Control Number disaster recovery cmdlets:</span></span>
    + <span data-ttu-id="477e7-195">可选 - 用于指定相关控制编号的 AgreementType 参数（“X12”或“Edifact”）</span><span class="sxs-lookup"><span data-stu-id="477e7-195">Optional -AgreementType parameter ("X12", or "Edifact") to specify the relevant control numbers</span></span>
* <span data-ttu-id="477e7-196">MachineLearning</span><span class="sxs-lookup"><span data-stu-id="477e7-196">MachineLearning</span></span>
  - <span data-ttu-id="477e7-197">使用新版 Azure 机器学习 .Net SDK 并添加新 cmdlet</span><span class="sxs-lookup"><span data-stu-id="477e7-197">Consume new version of Azure Machine Learning .Net SDK and add a new cmdlet</span></span>
    + <span data-ttu-id="477e7-198">Add-AzureRmMlWebServiceRegionalProperty</span><span class="sxs-lookup"><span data-stu-id="477e7-198">Add-AzureRmMlWebServiceRegionalProperty</span></span>
  - <span data-ttu-id="477e7-199">帮助文本中的措词小修复。</span><span class="sxs-lookup"><span data-stu-id="477e7-199">Minor wording fixes in help text.</span></span>
* <span data-ttu-id="477e7-200">网络</span><span class="sxs-lookup"><span data-stu-id="477e7-200">Network</span></span>
  - <span data-ttu-id="477e7-201">添加了 Test-AzureRmNetworkWatcherConnectivity cmdlet</span><span class="sxs-lookup"><span data-stu-id="477e7-201">Added Test-AzureRmNetworkWatcherConnectivity cmdlet</span></span>
    + <span data-ttu-id="477e7-202">返回有关指定源 VM 和目标的连接信息</span><span class="sxs-lookup"><span data-stu-id="477e7-202">Returns connectivity information for a specified source VM and a destination</span></span>
    + <span data-ttu-id="477e7-203">如果源和目标之间无法建立连接，则该 cmdlet 返回问题相关详细信息</span><span class="sxs-lookup"><span data-stu-id="477e7-203">If connectivity between the source and destination cannot be established, the cmdlet returns details about the issue</span></span>
* <span data-ttu-id="477e7-204">配置文件</span><span class="sxs-lookup"><span data-stu-id="477e7-204">Profile</span></span>
  - <span data-ttu-id="477e7-205">添加了 \`Send-Feedback' cmdlet：允许用户启动一组会向 Azure PowerShell 团队发送反馈的提示。</span><span class="sxs-lookup"><span data-stu-id="477e7-205">Added \`Send-Feedback' cmdlet: allows a user to initiate a set of prompts which sends feedback to the Azure PowerShell team.</span></span>
  - <span data-ttu-id="477e7-206">已删除以下别名，因为它们与 Azure 模块中的现有 cmdlet 名称冲突：</span><span class="sxs-lookup"><span data-stu-id="477e7-206">The following aliases have been removed as they conflicted with existing cmdlet names in the Azure module:</span></span>
    + <span data-ttu-id="477e7-207">`Enable-AzureDataCollection`（由 `Enable-AzureRmDataCollection` 支持）</span><span class="sxs-lookup"><span data-stu-id="477e7-207">`Enable-AzureDataCollection` (supported by `Enable-AzureRmDataCollection`)</span></span>
    + <span data-ttu-id="477e7-208">`Disable-AzureDataCollection`（由 `Disable-AzureRmDataCollection` 支持）</span><span class="sxs-lookup"><span data-stu-id="477e7-208">`Disable-AzureDataCollection` (supported by `Disable-AzureRmDataCollection`)</span></span>
* <span data-ttu-id="477e7-209">中继</span><span class="sxs-lookup"><span data-stu-id="477e7-209">Relay</span></span>
  - <span data-ttu-id="477e7-210">为 Azure 中继添加 cmdlet，让用户能够创建和管理所有 Azure 中继资源。</span><span class="sxs-lookup"><span data-stu-id="477e7-210">Adds cmdlets for the Azure Relay which allows users to create and manage all Azure Relay resources.</span></span>
    + `New-AzureRmRelayNamespace`
    + `Get-AzureRmRelayNamespace`
    + `Set-AzureRmRelayNamespace`
    + `Remove-AzureRmRelayNamespace`
    + `New-AzureRmWcfRelay`
    + `Get-AzureRmWcfRelay`
    + `Set-AzureRmWcfRelay`
    + `Remove-AzureRmWcfRelay`
    + `New-AzureRmRelayHybridConnection`
    + `Get-AzureRmRelayHybridConnection`
    + `Set-AzureRmRelayHybridConnection`
    + `Remove-AzureRmRelayHybridConnection`
    + `Test-AzureRmRelayName`
    + `Get-AzureRmRelayOperation`
    + `New-AzureRmRelayKey`
    + `Get-AzureRmRelayKey`
    + `New-AzureRmRelayAuthorizationRule`
    + `Get-AzureRmRelayAuthorizationRule`
    + `Set-AzureRmRelayAuthorizationRule`
    + `Remove-AzureRmRelayAuthorizationRule`
* <span data-ttu-id="477e7-211">资源</span><span class="sxs-lookup"><span data-stu-id="477e7-211">Resources</span></span>
  - <span data-ttu-id="477e7-212">支持 New-AzureRmResourceGroupDeployment 的跨资源组部署</span><span class="sxs-lookup"><span data-stu-id="477e7-212">Support cross-resource-group deployments for New-AzureRmResourceGroupDeployment</span></span>
    + <span data-ttu-id="477e7-213">现在，用户可使用嵌套部署在不同资源组之间进行部署。</span><span class="sxs-lookup"><span data-stu-id="477e7-213">Users can now use nested deployments to deploy to different resource groups.</span></span>
* <span data-ttu-id="477e7-214">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="477e7-214">ServiceBus</span></span>

  - <span data-ttu-id="477e7-215">Bug 修复：ServiceBus 队列对象属性值设置为 null，该对象用作 Set-AzureRmServiceBusQueue cmdlet 中的输入参数，用于更新队列。</span><span class="sxs-lookup"><span data-stu-id="477e7-215">Bug Fix: ServiceBus Queue object property values were set to null, the object is used as input parameter in Set-AzureRmServiceBusQueue cmdlet to update Queue.</span></span>
   - <span data-ttu-id="477e7-216">受影响的属性为 LockDuration、EntityAvailabilityStatus、DuplicateDetectionHistoryTimeWindow、MaxDeliveryCount and MessageCount</span><span class="sxs-lookup"><span data-stu-id="477e7-216">Properties affected are LockDuration, EntityAvailabilityStatus, DuplicateDetectionHistoryTimeWindow, MaxDeliveryCount and MessageCount</span></span>
* <span data-ttu-id="477e7-217">ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="477e7-217">ServiceFabric</span></span>

  - <span data-ttu-id="477e7-218">添加了适用于 Service Fabric 的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="477e7-218">Added cmdlets for service fabric</span></span>
    + <span data-ttu-id="477e7-219">Add-AzureRmServiceFabricApplicationCertificate 添加将用作应用程序证书的证书</span><span class="sxs-lookup"><span data-stu-id="477e7-219">Add-AzureRmServiceFabricApplicationCertificate       Add a certificate which will be used as application certificate</span></span>
    + <span data-ttu-id="477e7-220">Add-AzureRmServiceFabricClientCertificate 向群集设置添加公用名或指纹，以便进行客户端身份验证</span><span class="sxs-lookup"><span data-stu-id="477e7-220">Add-AzureRmServiceFabricClientCertificate       Add a common name or thumbprint to the cluster settings for client authentication</span></span>
    + <span data-ttu-id="477e7-221">Add-AzureRmServiceFabricClusterCertificate 向群集添加辅助群集证书，以便滚动显示现有证书</span><span class="sxs-lookup"><span data-stu-id="477e7-221">Add-AzureRmServiceFabricClusterCertificate       Add a secondary cluster certificate to the cluster for rolling over the existing certificate</span></span>
    + <span data-ttu-id="477e7-222">Add-AzureRmServiceFabricNodes 向群集添加特定节点类型的节点/VM</span><span class="sxs-lookup"><span data-stu-id="477e7-222">Add-AzureRmServiceFabricNodes       Add nodes/VMs of a specific node type to a cluster</span></span>
    + <span data-ttu-id="477e7-223">Add-AzureRmServiceFabricNodeType 向现有群集添加节点类型/VM</span><span class="sxs-lookup"><span data-stu-id="477e7-223">Add-AzureRmServiceFabricNodeType       Add a node type/VMs to an existing cluster</span></span>
    + <span data-ttu-id="477e7-224">Get-AzureRmServiceFabricCluster 获取群集资源的详细信息</span><span class="sxs-lookup"><span data-stu-id="477e7-224">Get-AzureRmServiceFabricCluster       Get the details of the cluster resource</span></span>
    + <span data-ttu-id="477e7-225">New-AzureRmServiceFabricCluster 新建 ServiceFabric 群集。</span><span class="sxs-lookup"><span data-stu-id="477e7-225">New-AzureRmServiceFabricCluster Create a new ServiceFabric cluster.</span></span> <span data-ttu-id="477e7-226">此命令包含许多重载，适用于各种方案</span><span class="sxs-lookup"><span data-stu-id="477e7-226">This command has many overloads to cover various scenarios</span></span>
    + <span data-ttu-id="477e7-227">Remove-AzureRmServiceFabricClientCertificate 删除用于访问群集的客户端证书</span><span class="sxs-lookup"><span data-stu-id="477e7-227">Remove-AzureRmServiceFabricClientCertificate       Remove a client certificate from being used to access a cluster</span></span>
    + <span data-ttu-id="477e7-228">Remove-AzureRmServiceFabricClusterCertificate 删除用于确保群集安全性的群集证书</span><span class="sxs-lookup"><span data-stu-id="477e7-228">Remove-AzureRmServiceFabricClusterCertificate       Remove a cluster certificate from being used for cluster security</span></span>
    + <span data-ttu-id="477e7-229">Remove-AzureRmServiceFabricNodes 从群集中删除特定节点类型的节点</span><span class="sxs-lookup"><span data-stu-id="477e7-229">Remove-AzureRmServiceFabricNodes       Remove nodes from a specific node type from a cluster</span></span>
    + <span data-ttu-id="477e7-230">Remove-AzureRmServiceFabricNodeType 从群集中删除节点类型</span><span class="sxs-lookup"><span data-stu-id="477e7-230">Remove-AzureRmServiceFabricNodeType       Remove a node type from a cluster</span></span>
    + <span data-ttu-id="477e7-231">Remove-AzureRmServiceFabricSettings 从群集中删除一个或多个 ServiceFabric 设置</span><span class="sxs-lookup"><span data-stu-id="477e7-231">Remove-AzureRmServiceFabricSettings       Remove one or more ServiceFabric settings from a cluster</span></span>
    + <span data-ttu-id="477e7-232">Set-AzureRmServiceFabricSettings 添加或更新群集的一个或多个 ServiceFabric 设置</span><span class="sxs-lookup"><span data-stu-id="477e7-232">Set-AzureRmServiceFabricSettings       Add or update one or more ServiceFabric settings of a cluster</span></span>
    + <span data-ttu-id="477e7-233">Set-AzureRmServiceFabricUpgradeType 更改群集的 ServiceFabric 升级类型</span><span class="sxs-lookup"><span data-stu-id="477e7-233">Set-AzureRmServiceFabricUpgradeType       Change the ServiceFabric upgrade type of a cluster</span></span>
    + <span data-ttu-id="477e7-234">Update-AzureRmServiceFabricDurability 更改群集的持久性层</span><span class="sxs-lookup"><span data-stu-id="477e7-234">Update-AzureRmServiceFabricDurability       Change the durability tier of a cluster</span></span>
    + <span data-ttu-id="477e7-235">Update-AzureRmServiceFabricReliability 更改群集的可靠性层</span><span class="sxs-lookup"><span data-stu-id="477e7-235">Update-AzureRmServiceFabricReliability       Change the reliability tier of a cluster</span></span>
* <span data-ttu-id="477e7-236">Sql</span><span class="sxs-lookup"><span data-stu-id="477e7-236">Sql</span></span>
  - <span data-ttu-id="477e7-237">向 New-AzureRmSqlDatabase 添加了 -SampleName 参数</span><span class="sxs-lookup"><span data-stu-id="477e7-237">Added -SampleName parameter to New-AzureRmSqlDatabase</span></span>
  - <span data-ttu-id="477e7-238">更新了故障转移组 cmdlet</span><span class="sxs-lookup"><span data-stu-id="477e7-238">Updates to Failover Group cmdlets</span></span>
  - <span data-ttu-id="477e7-239">删除“Tag”参数</span><span class="sxs-lookup"><span data-stu-id="477e7-239">Remove 'Tag' parameters</span></span>
  - <span data-ttu-id="477e7-240">从 Remove-AzureRmSqlDatabaseFailoverGroup cmdlet 中删除“PartnerResourceGroupName”和“PartnerServerName”参数</span><span class="sxs-lookup"><span data-stu-id="477e7-240">Remove 'PartnerResourceGroupName' and 'PartnerServerName' parameters from Remove-AzureRmSqlDatabaseFailoverGroup cmdlet</span></span>
  - <span data-ttu-id="477e7-241">向 New-cmdlet 和 Set- cmdlet 添加“GracePeriodWithDataLossHours”参数，此参数最终将取代“GracePeriodWithDataLossHour”</span><span class="sxs-lookup"><span data-stu-id="477e7-241">Add 'GracePeriodWithDataLossHours' parameter to New- and Set- cmdlets, which shall eventually replace 'GracePeriodWithDataLossHour'</span></span>
  - <span data-ttu-id="477e7-242">已完善并更新文档</span><span class="sxs-lookup"><span data-stu-id="477e7-242">Documentation has been fleshed out and updated</span></span>
  - <span data-ttu-id="477e7-243">更改返回对象的格式，并修复一些有关漏填字段的 Bug</span><span class="sxs-lookup"><span data-stu-id="477e7-243">Change formatting of returned objects and fix some bugs where fields were not always populated</span></span>
  - <span data-ttu-id="477e7-244">向故障转移组对象添加“DatabaseNames”和“PartnerLocation”属性</span><span class="sxs-lookup"><span data-stu-id="477e7-244">Add 'DatabaseNames' and 'PartnerLocation' properties to Failover Group object</span></span>
  - <span data-ttu-id="477e7-245">修复导致 Switch- cmdlet 立即返回而不是等待操作完成的 bug</span><span class="sxs-lookup"><span data-stu-id="477e7-245">Fix bug causing Switch- cmdlet to return immediately rather than waiting for operation to complete</span></span>
  - <span data-ttu-id="477e7-246">修复使用高宽限期值时出现的整数溢出 bug</span><span class="sxs-lookup"><span data-stu-id="477e7-246">Fix integer overflow bug when high grace period values are used</span></span>
  - <span data-ttu-id="477e7-247">如果提供的宽限期低于最小值 1 小时，则将其调整为最小值 1 小时</span><span class="sxs-lookup"><span data-stu-id="477e7-247">Adjust grace period to a minimum of 1 hour if a lower one is provided</span></span>
  - <span data-ttu-id="477e7-248">从 Set-AzureRmSqlDatabaseThreatDetectionPolicy cmdlet 和 Set-AzureRmSqlServerThreatDetectionPolicy cmdlet 的“ExcludedDetectionType”参数的接受值中删除“Usage_Anomaly”。</span><span class="sxs-lookup"><span data-stu-id="477e7-248">Remove "Usage_Anomaly" from the accepted values for "ExcludedDetectionType" parameter of Set-AzureRmSqlDatabaseThreatDetectionPolicy cmdlet and Set-AzureRmSqlServerThreatDetectionPolicy cmdlet.</span></span>
* <span data-ttu-id="477e7-249">存储</span><span class="sxs-lookup"><span data-stu-id="477e7-249">Storage</span></span>
  - <span data-ttu-id="477e7-250">将 SRP SDK 升级到 6.3.0</span><span class="sxs-lookup"><span data-stu-id="477e7-250">Upgrade SRP SDK to 6.3.0</span></span>
  - <span data-ttu-id="477e7-251">New/Set-AzureRmStorageAccount：添加新参数，用于支持 EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="477e7-251">New/Set-AzureRmStorageAccount:Add a new parameter to support EnableHttpsTrafficOnly</span></span>
  - <span data-ttu-id="477e7-252">New/Set/Get-AzureRmStorageAccount：返回的存储帐户包含新属性 EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="477e7-252">New/Set/Get-AzureRmStorageAccount: Returned Storage Account contains a new attribute EnableHttpsTrafficOnly</span></span>
* <span data-ttu-id="477e7-253">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="477e7-253">Azure.Storage</span></span>
  - <span data-ttu-id="477e7-254">升级到 Azure 存储客户端库 8.1.1 和 Azure 存储 DataMovement 库 0.5.1</span><span class="sxs-lookup"><span data-stu-id="477e7-254">Upgrade to Azure Storage Client Library 8.1.1 and Azure Storage DataMovement Library 0.5.1</span></span>
  - <span data-ttu-id="477e7-255">添加一个新 cmdlet，用于支持 blob 增量复制功能</span><span class="sxs-lookup"><span data-stu-id="477e7-255">Add a new cmdlet to support blob Incremental Copy feature</span></span>
