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
ms.date: 07/26/2017
ms.openlocfilehash: cc2fe75f498f9043e5a4b632c144877af0143173
ms.sourcegitcommit: 20bcef86db4e4869125bb63085fcffd009c19280
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/27/2017
---
# <a name="release-notes"></a><span data-ttu-id="325e0-103">发行说明</span><span class="sxs-lookup"><span data-stu-id="325e0-103">Release notes</span></span>

<span data-ttu-id="325e0-104">下面是此版本中对 Azure PowerShell 所做的更改列表。</span><span class="sxs-lookup"><span data-stu-id="325e0-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

## <a name="20170717---version-421"></a><span data-ttu-id="325e0-105">2017.07.17 - 版本 4.2.1</span><span class="sxs-lookup"><span data-stu-id="325e0-105">2017.07.17 - Version 4.2.1</span></span>
* <span data-ttu-id="325e0-106">计算</span><span class="sxs-lookup"><span data-stu-id="325e0-106">Compute</span></span>
    - <span data-ttu-id="325e0-107">修复 VM 磁盘和 VM 磁盘快照创建和更新 cmdlet 的问题，（链接）[https://github.com/azure/azure-powershell/issues/4309]</span><span class="sxs-lookup"><span data-stu-id="325e0-107">Fix issue with VM DIsk and VM Disk snapshot create and update cmdlets, (link)[https://github.com/azure/azure-powershell/issues/4309]</span></span>
      - <span data-ttu-id="325e0-108">New-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="325e0-108">New-AzureRmDisk</span></span>
      - <span data-ttu-id="325e0-109">New-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="325e0-109">New-AzureRmSnapshot</span></span>
      - <span data-ttu-id="325e0-110">Update-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="325e0-110">Update-AzureRmDisk</span></span>
      - <span data-ttu-id="325e0-111">Update-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="325e0-111">Update-AzureRmSnapshot</span></span>
* <span data-ttu-id="325e0-112">配置文件</span><span class="sxs-lookup"><span data-stu-id="325e0-112">Profile</span></span>
    - <span data-ttu-id="325e0-113">修复 RDFE 中非交互用户身份验证的问题（链接）[https://github.com/Azure/azure-powershell/issues/4299]</span><span class="sxs-lookup"><span data-stu-id="325e0-113">Fix issue with non-interactive user authentication in RDFE (link)[https://github.com/Azure/azure-powershell/issues/4299]</span></span>
* <span data-ttu-id="325e0-114">ServiceManagement</span><span class="sxs-lookup"><span data-stu-id="325e0-114">ServiceManagement</span></span>
    - <span data-ttu-id="325e0-115">修复非交互用户身份验证的问题（链接）[https://github.com/Azure/azure-powershell/issues/4299]</span><span class="sxs-lookup"><span data-stu-id="325e0-115">Fix issue with non-interactive user authentication (link)[https://github.com/Azure/azure-powershell/issues/4299]</span></span>

## <a name="2017711---version-420"></a><span data-ttu-id="325e0-116">2017.7.11 - 版本 4.2.0</span><span class="sxs-lookup"><span data-stu-id="325e0-116">2017.7.11 - Version 4.2.0</span></span>
* <span data-ttu-id="325e0-117">AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="325e0-117">AnalysisServices</span></span>
    * <span data-ttu-id="325e0-118">添加新的 dataplane API</span><span class="sxs-lookup"><span data-stu-id="325e0-118">Add new dataplane API</span></span>
        - <span data-ttu-id="325e0-119">引入了 API，提取 AS 服务器日志 Export-AzureAnalysisServicesInstanceLog</span><span class="sxs-lookup"><span data-stu-id="325e0-119">Introduced API to fetch AS server log, Export-AzureAnalysisServicesInstanceLog</span></span>
* <span data-ttu-id="325e0-120">自动化</span><span class="sxs-lookup"><span data-stu-id="325e0-120">Automation</span></span>
    * <span data-ttu-id="325e0-121">正确设置 New-AzureRmAutomationSchedule“每周”和“每月”计划的时区值</span><span class="sxs-lookup"><span data-stu-id="325e0-121">Properly setting TimeZone value for Weekly and Monthly schedules for New-AzureRmAutomationSchedule</span></span>
        - <span data-ttu-id="325e0-122">此问题中提供详细信息：https://github.com/Azure/azure-powershell/issues/3043</span><span class="sxs-lookup"><span data-stu-id="325e0-122">More information can be found in this issue: https://github.com/Azure/azure-powershell/issues/3043</span></span>
* <span data-ttu-id="325e0-123">AzureBatch</span><span class="sxs-lookup"><span data-stu-id="325e0-123">AzureBatch</span></span>
    - <span data-ttu-id="325e0-124">添加了新的 Get-AzureBatchJobPreparationAndReleaseTaskStatus cmdlet。</span><span class="sxs-lookup"><span data-stu-id="325e0-124">Added new Get-AzureBatchJobPreparationAndReleaseTaskStatus cmdlet.</span></span>
    - <span data-ttu-id="325e0-125">向 Get-AzureBatchNodeFileContent 参数添加了字节范围开始和结束。</span><span class="sxs-lookup"><span data-stu-id="325e0-125">Added byte range start and end to Get-AzureBatchNodeFileContent parameters.</span></span>
* <span data-ttu-id="325e0-126">认知服务</span><span class="sxs-lookup"><span data-stu-id="325e0-126">CognitiveServices</span></span>
    * <span data-ttu-id="325e0-127">与认知服务管理 SDK 版本 1.0.0 集成。</span><span class="sxs-lookup"><span data-stu-id="325e0-127">Integrate with Cognitive Services Management SDK version 1.0.0.</span></span>
    * <span data-ttu-id="325e0-128">修复帐户名称长度检查 bug。</span><span class="sxs-lookup"><span data-stu-id="325e0-128">Fix an account name length checking bug.</span></span>
* <span data-ttu-id="325e0-129">计算</span><span class="sxs-lookup"><span data-stu-id="325e0-129">Compute</span></span>
    * <span data-ttu-id="325e0-130">映像磁盘的存储帐户类型支持：</span><span class="sxs-lookup"><span data-stu-id="325e0-130">Storage account type support for Image disk:</span></span>
        - <span data-ttu-id="325e0-131">已将“StorageAccountType”参数添加到 Set-AzureRmImageOsDisk 和 Add-AzureRmImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="325e0-131">'StorageAccountType' parameter is added to Set-AzureRmImageOsDisk and Add-AzureRmImageDataDisk</span></span>
    * <span data-ttu-id="325e0-132">Vmss Ip 配置中的 PrivateIP 和 PublicIP 功能：</span><span class="sxs-lookup"><span data-stu-id="325e0-132">PrivateIP and PublicIP feature in Vmss Ip Configuration:</span></span>
        - <span data-ttu-id="325e0-133">已将“PrivateIPAddressVersion”、“PublicIPAddressConfigurationName”、“PublicIPAddressConfigurationIdleTimeoutInMinutes”、“DnsSetting”名称添加到 New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="325e0-133">'PrivateIPAddressVersion', 'PublicIPAddressConfigurationName', 'PublicIPAddressConfigurationIdleTimeoutInMinutes', 'DnsSetting' names are added to New-AzureRmVmssIpConfig</span></span>
        - <span data-ttu-id="325e0-134">已将用于指定 IPv4 或 IPv6 的“PrivateIPAddressVersion”参数添加到 New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="325e0-134">'PrivateIPAddressVersion' parameter for specifying IPv4 or IPv6 is added to New-AzureRmVmssIpConfig</span></span>
    * <span data-ttu-id="325e0-135">性能维护功能：</span><span class="sxs-lookup"><span data-stu-id="325e0-135">Performance Maintenance feature:</span></span>
        - <span data-ttu-id="325e0-136">已将“PerformMaintenance”开关参数添加到 Restart-AzureRmVM。</span><span class="sxs-lookup"><span data-stu-id="325e0-136">'PerformMaintenance' switch parameter is added to Restart-AzureRmVM.</span></span>
        - <span data-ttu-id="325e0-137">Get-AzureRmVM -Status 显示给定 VM 性能维护的信息</span><span class="sxs-lookup"><span data-stu-id="325e0-137">Get-AzureRmVM -Status shows the information of performance maintenance of the given VM</span></span>
    * <span data-ttu-id="325e0-138">虚拟机标识功能：</span><span class="sxs-lookup"><span data-stu-id="325e0-138">Virtual Machine Identity feature:</span></span>
        - <span data-ttu-id="325e0-139">已将“IdentityType”参数添加到 New-AzureRmVMConfig 和 UpdateAzureRmVM</span><span class="sxs-lookup"><span data-stu-id="325e0-139">'IdentityType' parameter is added to New-AzureRmVMConfig and UpdateAzureRmVM</span></span>
        - <span data-ttu-id="325e0-140">Get AzureRmVM 显示给定 VM 的标识信息</span><span class="sxs-lookup"><span data-stu-id="325e0-140">Get-AzureRmVM shows the information of the identity of the given VM</span></span>
    * <span data-ttu-id="325e0-141">Vmss 标识功能：</span><span class="sxs-lookup"><span data-stu-id="325e0-141">Vmss Identity feature:</span></span>
        - <span data-ttu-id="325e0-142">已将“IdentityType”参数添加到 New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="325e0-142">'IdentityType' parameter is added to to New-AzureRmVmssConfig</span></span>
        - <span data-ttu-id="325e0-143">Get-AzureRmVmss 显示给定 Vmss 的标识信息</span><span class="sxs-lookup"><span data-stu-id="325e0-143">Get-AzureRmVmss shows the information of the identity of the given Vmss</span></span>
    * <span data-ttu-id="325e0-144">Vmss 启动诊断功能：</span><span class="sxs-lookup"><span data-stu-id="325e0-144">Vmss Boot Diagnostics feature:</span></span>
        - <span data-ttu-id="325e0-145">用于设置 Vmss 对象的启动诊断的新 cmdlet：Set-AzureRmVmssBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="325e0-145">New cmdlet for setting boot diagnostics of Vmss object: Set-AzureRmVmssBootDiagnostics</span></span>
        - <span data-ttu-id="325e0-146">已将“BootDiagnostic”参数添加到 New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="325e0-146">'BootDiagnostic' parameter is added to New-AzureRmVmssConfig</span></span>
    * <span data-ttu-id="325e0-147">Vmss LicenseType 功能：</span><span class="sxs-lookup"><span data-stu-id="325e0-147">Vmss LicenseType feature:</span></span>
        - <span data-ttu-id="325e0-148">已将“LicenseType”参数添加到 New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="325e0-148">'LicenseType' parameter is added to New-AzureRmVmssConfig</span></span>
    * <span data-ttu-id="325e0-149">RecoveryPolicyMode 支持：</span><span class="sxs-lookup"><span data-stu-id="325e0-149">RecoveryPolicyMode support:</span></span>
        - <span data-ttu-id="325e0-150">已将“RecoveryPolicyMode”参数添加到 New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="325e0-150">'RecoveryPolicyMode' paramter is added to New-AzureRmVmssConfig</span></span>
    * <span data-ttu-id="325e0-151">计算资源 Sku 功能：</span><span class="sxs-lookup"><span data-stu-id="325e0-151">Compute Resource Sku feature:</span></span>
        - <span data-ttu-id="325e0-152">新的 cmdlet“Get AzureRmComputeResourceSku”列出所有计算资源 sku</span><span class="sxs-lookup"><span data-stu-id="325e0-152">New cmdlet 'Get-AzureRmComputeResourceSku' list all compute resource skus</span></span>
* <span data-ttu-id="325e0-153">数据工厂</span><span class="sxs-lookup"><span data-stu-id="325e0-153">DataFactories</span></span>
    * <span data-ttu-id="325e0-154">弃用 New-AzureRmDataFactoryGatewayKey</span><span class="sxs-lookup"><span data-stu-id="325e0-154">Deprecate New-AzureRmDataFactoryGatewayKey</span></span>
    * <span data-ttu-id="325e0-155">通过添加 New-AzureRmDataFactoryGatewayAuthKey 和 Get-AzureRmDataFactoryGatewayAuthKey 引入网关身份验证密钥功能</span><span class="sxs-lookup"><span data-stu-id="325e0-155">Introduce gateway auth key feature by adding New-AzureRmDataFactoryGatewayAuthKey and Get-AzureRmDataFactoryGatewayAuthKey</span></span>
* <span data-ttu-id="325e0-156">DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="325e0-156">DataLakeAnalytics</span></span>
    * <span data-ttu-id="325e0-157">通过以下命令添加对计算策略 CRUD 的支持：</span><span class="sxs-lookup"><span data-stu-id="325e0-157">Add support for Compute Policy CRUD through the following commands:</span></span>
        - <span data-ttu-id="325e0-158">New-AzureRMDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="325e0-158">New-AzureRMDataLakeAnalyticsComputePolicy</span></span>
        - <span data-ttu-id="325e0-159">Get-AzureRMDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="325e0-159">Get-AzureRMDataLakeAnalyticsComputePolicy</span></span>
        - <span data-ttu-id="325e0-160">Remove-AzureRMDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="325e0-160">Remove-AzureRMDataLakeAnalyticsComputePolicy</span></span>
        - <span data-ttu-id="325e0-161">Update-AzureRMDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="325e0-161">Update-AzureRMDataLakeAnalyticsComputePolicy</span></span>
    * <span data-ttu-id="325e0-162">添加对作业关系元数据的支持，为定期作业和作业管道提供帮助。</span><span class="sxs-lookup"><span data-stu-id="325e0-162">Add support for job relationship metadata for help with recurring jobs and job pipelines.</span></span> <span data-ttu-id="325e0-163">已更新或已添加以下命令：</span><span class="sxs-lookup"><span data-stu-id="325e0-163">The following commands were updated or added:</span></span>
        - <span data-ttu-id="325e0-164">Submit-AzureRMDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="325e0-164">Submit-AzureRMDataLakeAnalyticsJob</span></span>
        - <span data-ttu-id="325e0-165">Get-AzureRMDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="325e0-165">Get-AzureRMDataLakeAnalyticsJob</span></span>
        - <span data-ttu-id="325e0-166">Get-AzureRMDataLakeAnalyticsJobRecurrence</span><span class="sxs-lookup"><span data-stu-id="325e0-166">Get-AzureRMDataLakeAnalyticsJobRecurrence</span></span>
        - <span data-ttu-id="325e0-167">Get-AzureRMDataLakeAnalyticsJobPipeline</span><span class="sxs-lookup"><span data-stu-id="325e0-167">Get-AzureRMDataLakeAnalyticsJobPipeline</span></span>
    * <span data-ttu-id="325e0-168">已更新作业和目录 API 的令牌受众，使用正确的 Data Lake 特定受众而不是 Azure 资源受众。</span><span class="sxs-lookup"><span data-stu-id="325e0-168">Updated the token audience for job and catalog APIs to use the correct Data Lake specific audience instead of the Azure Resource audience.</span></span>
* <span data-ttu-id="325e0-169">DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="325e0-169">DataLakeStore</span></span>
    * <span data-ttu-id="325e0-170">在 Set-AzureRMDataLakeStoreAccount cmdlet 中添加了对用户托管 KeyVault 密钥轮换的支持</span><span class="sxs-lookup"><span data-stu-id="325e0-170">Added support for user managed KeyVault key rotations in the Set-AzureRMDataLakeStoreAccount cmdlet</span></span>
    * <span data-ttu-id="325e0-171">添加了生命周期质量更新，在添加用户托管 KeyVault 或轮换密钥时自动触发 `enableKeyVault` 调用。</span><span class="sxs-lookup"><span data-stu-id="325e0-171">Added a quality of life update to automatically trigger an `enableKeyVault` call when a user managed KeyVault is added or a key is rotated.</span></span>
    * <span data-ttu-id="325e0-172">已更新作业和目录 API 的令牌受众，使用正确的 Data Lake 特定受众而不是 Azure 资源受众。</span><span class="sxs-lookup"><span data-stu-id="325e0-172">Updated the token audience for job and catalog APIs to use the correct Data Lake specific audience instead of the Azure Resource audience.</span></span>
    * <span data-ttu-id="325e0-173">使用以下 cmdlet 修复了限制已创建/追加文件的大小 bug：</span><span class="sxs-lookup"><span data-stu-id="325e0-173">Fixed a bug limiting the size of files created/appended using the following cmdlets:</span></span>
        - <span data-ttu-id="325e0-174">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="325e0-174">New-AzureRmDataLakeStoreItem</span></span>
        - <span data-ttu-id="325e0-175">Add-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="325e0-175">Add-AzureRmDataLakeStoreItemContent</span></span>
* <span data-ttu-id="325e0-176">Dns</span><span class="sxs-lookup"><span data-stu-id="325e0-176">Dns</span></span>
    * <span data-ttu-id="325e0-177">修复 Get AzureRmDnsZone 的管道方案中的 bug</span><span class="sxs-lookup"><span data-stu-id="325e0-177">Fix bug in the piping scenario for Get-AzureRmDnsZone</span></span>
        - <span data-ttu-id="325e0-178">此处提供详细信息：https://github.com/Azure/azure-powershell/issues/4203</span><span class="sxs-lookup"><span data-stu-id="325e0-178">More information can be found here: https://github.com/Azure/azure-powershell/issues/4203</span></span>
* <span data-ttu-id="325e0-179">HDInsight</span><span class="sxs-lookup"><span data-stu-id="325e0-179">HDInsight</span></span>
    * <span data-ttu-id="325e0-180">添加了支持以启用/禁用 Operations Management Suite (OMS)</span><span class="sxs-lookup"><span data-stu-id="325e0-180">Added support to enable / disable Operations Management Suite(OMS)</span></span>
    * <span data-ttu-id="325e0-181">新 cmdlet</span><span class="sxs-lookup"><span data-stu-id="325e0-181">New cmdlets</span></span>
        - <span data-ttu-id="325e0-182">Enable-AzureRmHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="325e0-182">Enable-AzureRmHDInsightOperationsManagementSuite</span></span>
        - <span data-ttu-id="325e0-183">Disable-AzureRmHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="325e0-183">Disable-AzureRmHDInsightOperationsManagementSuite</span></span>
        - <span data-ttu-id="325e0-184">Get-AzureRmHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="325e0-184">Get-AzureRmHDInsightOperationsManagementSuite</span></span>
    * <span data-ttu-id="325e0-185">添加新参数，将 Spark 自定义配置设置为 Add-AzureRmHDInsightConfigValues</span><span class="sxs-lookup"><span data-stu-id="325e0-185">Add new parameters to set Spark custom configurations to Add-AzureRmHDInsightConfigValues</span></span>
        - <span data-ttu-id="325e0-186">适用于 Spark 1.6 的参数 SparkDefaults 和 SparkThriftConf</span><span class="sxs-lookup"><span data-stu-id="325e0-186">Parameters SparkDefaults and SparkThriftConf for Spark 1.6</span></span>
        - <span data-ttu-id="325e0-187">适用于 Spark 2.0 的参数 Spark2Defaults 和 Spark2ThriftConf</span><span class="sxs-lookup"><span data-stu-id="325e0-187">Parameters Spark2Defaults and Spark2ThriftConf for Spark 2.0</span></span>
* <span data-ttu-id="325e0-188">洞察力</span><span class="sxs-lookup"><span data-stu-id="325e0-188">Insights</span></span>
    * <span data-ttu-id="325e0-189">问题 #4215（更改请求）删除了 Get-AzureRmLog cmdlet 时间范围中的 15 天限制。</span><span class="sxs-lookup"><span data-stu-id="325e0-189">Issue #4215 (change request) remove the 15 days limit in the time window for the Get-AzureRmLog cmdlet.</span></span> <span data-ttu-id="325e0-190">此外还对单元测试名称进行了细微的更改。</span><span class="sxs-lookup"><span data-stu-id="325e0-190">Also minor changes to the unit test names.</span></span>
    * <span data-ttu-id="325e0-191">已为 Get-AzureRmLog 修复了问题 #3957</span><span class="sxs-lookup"><span data-stu-id="325e0-191">Issue #3957 fixed for Get-AzureRmLog</span></span>
        - <span data-ttu-id="325e0-192">问题 #1：后端以每页 200 条记录的形式返回记录，由继续标记链接到下一页。</span><span class="sxs-lookup"><span data-stu-id="325e0-192">Issue #1: The backend returns the records in pages of 200 records each, linked by the continuation token to the next page.</span></span> <span data-ttu-id="325e0-193">客户看到该 cmdlet 仅返回 200 条记录，但他们知道还有更多记录。</span><span class="sxs-lookup"><span data-stu-id="325e0-193">The customers were seeing the cmdlet returning only 200 records when they knew there were more.</span></span> <span data-ttu-id="325e0-194">无论对 MaxEvents 设置何值（除非该值小于 200）都会出现这种情况。</span><span class="sxs-lookup"><span data-stu-id="325e0-194">This was happening regardless of the value they set for MaxEvents, unless that value was less than 200.</span></span>
        - <span data-ttu-id="325e0-195">问题 2：文档包含此 cmdlet 相关的错误数据，例如：默认时间范围为 1 小时。</span><span class="sxs-lookup"><span data-stu-id="325e0-195">Issue #2: The documentation contained incorrect data about this cmdlet, e.g.: the default timewindow was 1 hour.</span></span>
        - <span data-ttu-id="325e0-196">修复 #1：cmdlet 现遵循后端返回的继续标记，直到它达到 MaxEvents 值或该组的末尾。</span><span class="sxs-lookup"><span data-stu-id="325e0-196">Fix #1: The cmdlet now follows the continuation token returned by the backend until it reaches MaxEvents or the end of the set.</span></span><br><span data-ttu-id="325e0-197">MaxEvents 的默认值为 1000，其最大值为 100000。</span><span class="sxs-lookup"><span data-stu-id="325e0-197">The default value for MaxEvents is 1000 and its maximum is 100000.</span></span> <span data-ttu-id="325e0-198">将忽略小于 1 的任何 MaxEvents 值，改用默认值。</span><span class="sxs-lookup"><span data-stu-id="325e0-198">Any value for MaxEvents that is less than 1 is ignored and the default is used instead.</span></span> <span data-ttu-id="325e0-199">这些值和行为没有更改，现在可以正确记录它们。</span><span class="sxs-lookup"><span data-stu-id="325e0-199">These values and behavior did not change, now they are correctly documented.</span></span><br><span data-ttu-id="325e0-200">已添加 MaxEvents 的别名 - MaxRecords，因为该 cmdlet 的名称没有再提及事件，只提及日志。</span><span class="sxs-lookup"><span data-stu-id="325e0-200">An alias for MaxEvents has been added -MaxRecords- since the name of the cmdlet does not speak about events anymore, but only about Logs.</span></span>
        - <span data-ttu-id="325e0-201">修复 #2：文档包含正确信息以及更多详细信息：新别名、正确的时间范围、正确的默认值、最小值和最大值。</span><span class="sxs-lookup"><span data-stu-id="325e0-201">Fix #2: The documentation contains correct and more detailed information: new alias, correct time window, correct default, minimum, and maximum values.</span></span>
* <span data-ttu-id="325e0-202">KeyVault</span><span class="sxs-lookup"><span data-stu-id="325e0-202">KeyVault</span></span>
    * <span data-ttu-id="325e0-203">将 -UserPrincipalName 指定为 Set-AzureRMKeyVaultAccessPolicy 和 Remove-AzureRMKeyVaultAccessPolicy cmdlet 时，从目录查询中删除电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="325e0-203">Remove email address from the directory query when -UserPrincipalName is specified to the Set-AzureRMKeyVaultAccessPolicy and Remove-AzureRMKeyVaultAccessPolicy cmdlets.</span></span>
      - <span data-ttu-id="325e0-204">这两个 Cmdlet 现拥有在适合查询电子邮件地址时，可使用的 -EmailAddress 参数（而不是 -UserPrincipalName 参数）。</span><span class="sxs-lookup"><span data-stu-id="325e0-204">Both Cmdlets now have an -EmailAddress parameter that can be used instead of the -UserPrincipalName parameter when querying for email address is appropriate.</span></span>  <span data-ttu-id="325e0-205">如果目录中存在多个匹配的电子邮件地址，Cmdlet 将失败。</span><span class="sxs-lookup"><span data-stu-id="325e0-205">If there are more than one matching email addresses in the directory then the Cmdlet will fail.</span></span>
* <span data-ttu-id="325e0-206">网络</span><span class="sxs-lookup"><span data-stu-id="325e0-206">Network</span></span>
    * <span data-ttu-id="325e0-207">New-AzureRmIpsecPolicy：SALifeTimeSeconds 和 SADataSizeKilobytes 不再是必需参数</span><span class="sxs-lookup"><span data-stu-id="325e0-207">New-AzureRmIpsecPolicy: SALifeTimeSeconds and SADataSizeKilobytes are no longer mandatory parameters</span></span>
        - <span data-ttu-id="325e0-208">SALifeTimeSeconds 默认值为 27000 秒</span><span class="sxs-lookup"><span data-stu-id="325e0-208">SALifeTimeSeconds defaults to 27000 seconds</span></span>
        - <span data-ttu-id="325e0-209">SADataSizeKilobytes 默认值为 102400000 KB</span><span class="sxs-lookup"><span data-stu-id="325e0-209">SADataSizeKilobytes defaults to 102400000 KB</span></span>
    * <span data-ttu-id="325e0-210">通过使用 ssl 策略并列出应用程序网关中的所有 ssl 选项 api，添加了对自定义密码套件配置的支持</span><span class="sxs-lookup"><span data-stu-id="325e0-210">Added support for custom cipher suite configuration using ssl policy and listing all ssl options api in Application Gateway</span></span>
        - <span data-ttu-id="325e0-211">添加了可选参数 -PolicyType、-PolicyName、-MinProtocolVersion、-Ciphersuite</span><span class="sxs-lookup"><span data-stu-id="325e0-211">Added optional parameter -PolicyType, -PolicyName, -MinProtocolVersion, -Ciphersuite</span></span>
            - <span data-ttu-id="325e0-212">Add-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="325e0-212">Add-AzureRmApplicationGatewaySslPolicy</span></span>
            - <span data-ttu-id="325e0-213">New-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="325e0-213">New-AzureRmApplicationGatewaySslPolicy</span></span>
            - <span data-ttu-id="325e0-214">Set-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="325e0-214">Set-AzureRmApplicationGatewaySslPolicy</span></span>
        - <span data-ttu-id="325e0-215">添加了 Get-AzureRmApplicationGatewayAvailableSslOptions（别名：List-AzureRmApplicationGatewayAvailableSslOptions）</span><span class="sxs-lookup"><span data-stu-id="325e0-215">Added Get-AzureRmApplicationGatewayAvailableSslOptions (Alias: List-AzureRmApplicationGatewayAvailableSslOptions)</span></span>
        - <span data-ttu-id="325e0-216">添加了 Get AzureRmApplicationGatewaySslPredefinedPolicy（别名：List-AzureRmApplicationGatewaySslPredefinedPolicy）</span><span class="sxs-lookup"><span data-stu-id="325e0-216">Added Get-AzureRmApplicationGatewaySslPredefinedPolicy (Alias: List-AzureRmApplicationGatewaySslPredefinedPolicy)</span></span>
    * <span data-ttu-id="325e0-217">在应用程序网关中添加了重定向支持</span><span class="sxs-lookup"><span data-stu-id="325e0-217">Added redirect support in Application Gateway</span></span>
        - <span data-ttu-id="325e0-218">添加了 Add-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="325e0-218">Added Add-AzureRmApplicationGatewayRedirectConfiguration</span></span>
        - <span data-ttu-id="325e0-219">添加了 Get-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="325e0-219">Added Get-AzureRmApplicationGatewayRedirectConfiguration</span></span>
        - <span data-ttu-id="325e0-220">添加了 New-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="325e0-220">Added New-AzureRmApplicationGatewayRedirectConfiguration</span></span>
        - <span data-ttu-id="325e0-221">添加了 Remove-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="325e0-221">Added Remove-AzureRmApplicationGatewayRedirectConfiguration</span></span>
        - <span data-ttu-id="325e0-222">添加了 Set-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="325e0-222">Added Set-AzureRmApplicationGatewayRedirectConfiguration</span></span>
        - <span data-ttu-id="325e0-223">添加了可选参数 -RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="325e0-223">Added optional parameter -RedirectConfiguration</span></span>
            - <span data-ttu-id="325e0-224">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="325e0-224">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
            - <span data-ttu-id="325e0-225">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="325e0-225">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
            - <span data-ttu-id="325e0-226">Set-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="325e0-226">Set-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="325e0-227">添加了可选参数 -DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="325e0-227">Added optional parameter -DefaultRedirectConfiguration</span></span>
            - <span data-ttu-id="325e0-228">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="325e0-228">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
            - <span data-ttu-id="325e0-229">New-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="325e0-229">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
            - <span data-ttu-id="325e0-230">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="325e0-230">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="325e0-231">添加了可选参数 -RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="325e0-231">Added optional parameter -RedirectConfiguration</span></span>
            - <span data-ttu-id="325e0-232">Add-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="325e0-232">Add-AzureRmApplicationGatewayPathRuleConfig</span></span>
            - <span data-ttu-id="325e0-233">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="325e0-233">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
            - <span data-ttu-id="325e0-234">Set-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="325e0-234">Set-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="325e0-235">添加了可选参数 -RedirectConfigurations</span><span class="sxs-lookup"><span data-stu-id="325e0-235">Added optional parameter -RedirectConfigurations</span></span>
            - <span data-ttu-id="325e0-236">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="325e0-236">New-AzureRmApplicationGateway</span></span>
            - <span data-ttu-id="325e0-237">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="325e0-237">Set-AzureRmApplicationGateway</span></span>
    * <span data-ttu-id="325e0-238">添加了在应用程序网关中对 Azure 网站的支持</span><span class="sxs-lookup"><span data-stu-id="325e0-238">Added support for azure websites in Application Gateway</span></span>
        - <span data-ttu-id="325e0-239">添加了 New-AzureRmApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="325e0-239">Added New-AzureRmApplicationGatewayProbeHealthResponseMatch</span></span>
        - <span data-ttu-id="325e0-240">添加了可选参数 -PickHostNameFromBackendHttpSettings、-MinServers、-Match</span><span class="sxs-lookup"><span data-stu-id="325e0-240">Added optional parameters -PickHostNameFromBackendHttpSettings, -MinServers, -Match</span></span>
            - <span data-ttu-id="325e0-241">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="325e0-241">Add-AzureRmApplicationGatewayProbeConfig</span></span>
            - <span data-ttu-id="325e0-242">New-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="325e0-242">New-AzureRmApplicationGatewayProbeConfig</span></span>
            - <span data-ttu-id="325e0-243">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="325e0-243">Set-AzureRmApplicationGatewayProbeConfig</span></span>
        - <span data-ttu-id="325e0-244">添加了可选参数 -PickHostNameFromBackendAddress、-AffinityCookieName、-ProbeEnabled、-Path</span><span class="sxs-lookup"><span data-stu-id="325e0-244">Added optional parameters -PickHostNameFromBackendAddress, -AffinityCookieName, -ProbeEnabled, -Path</span></span>
            - <span data-ttu-id="325e0-245">Add-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="325e0-245">Add-AzureRmApplicationGatewayBackendHttpSettings</span></span>
            - <span data-ttu-id="325e0-246">New-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="325e0-246">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>
            - <span data-ttu-id="325e0-247">Set-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="325e0-247">Set-AzureRmApplicationGatewayBackendHttpSettings</span></span>
    * <span data-ttu-id="325e0-248">更新 Get-AzureRmPublicIPaddress，检索通过 VM 规模集创建的 publicipaddress 资源</span><span class="sxs-lookup"><span data-stu-id="325e0-248">Update Get-AzureRmPublicIPaddress to retrieve publicipaddress resources created via VM Scale Set</span></span>
    * <span data-ttu-id="325e0-249">添加了 cmdlet 来获取虚拟网络当前的使用情况</span><span class="sxs-lookup"><span data-stu-id="325e0-249">Added cmdlet to get virtual network current usage</span></span>
        - <span data-ttu-id="325e0-250">Get-AzureRmVirtualNetworkUsageList</span><span class="sxs-lookup"><span data-stu-id="325e0-250">Get-AzureRmVirtualNetworkUsageList</span></span>
* <span data-ttu-id="325e0-251">配置文件</span><span class="sxs-lookup"><span data-stu-id="325e0-251">Profile</span></span>
    * <span data-ttu-id="325e0-252">修复了使用 Import-AzureRmContext 或 Save-AzureRmContext 时的错误</span><span class="sxs-lookup"><span data-stu-id="325e0-252">Fixed error when using Import-AzureRmContext or Save-AzureRmContext</span></span>
        - <span data-ttu-id="325e0-253">此问题中提供详细信息：https://github.com/Azure/azure-powershell/issues/3954</span><span class="sxs-lookup"><span data-stu-id="325e0-253">More information can be found in this issue: https://github.com/Azure/azure-powershell/issues/3954</span></span>
* <span data-ttu-id="325e0-254">RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="325e0-254">RecoveryServices.SiteRecovery</span></span>
    * <span data-ttu-id="325e0-255">为 Azure Site Recovery 操作引入新模块。</span><span class="sxs-lookup"><span data-stu-id="325e0-255">Introducing a new module for Azure Site Recovery operations.</span></span>
        - <span data-ttu-id="325e0-256">所有 cmdlet 都以 AzureRmRecoveryServicesAsr* 开头</span><span class="sxs-lookup"><span data-stu-id="325e0-256">All cmdlets begin with AzureRmRecoveryServicesAsr*</span></span>
* <span data-ttu-id="325e0-257">Sql</span><span class="sxs-lookup"><span data-stu-id="325e0-257">Sql</span></span>
    * <span data-ttu-id="325e0-258">将数据同步 PowerShell Cmdlet 添加到 AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="325e0-258">Add Data Sync PowerShell Cmdlets to AzureRM.Sql</span></span>
    * <span data-ttu-id="325e0-259">更新了 AzureRmSqlServer cmdlet，使用创建服务器时可避免超时的 REST API 新版本。</span><span class="sxs-lookup"><span data-stu-id="325e0-259">Updated AzureRmSqlServer cmdlets to use new REST API version that avoids timeouts when creating server.</span></span>
    * <span data-ttu-id="325e0-260">已弃用服务器升级 cmdlet，因为旧版服务器 (2.0) 不再存在。</span><span class="sxs-lookup"><span data-stu-id="325e0-260">Deprecated server upgrade cmdlets because the old server version (2.0) no longer exists.</span></span>
    * <span data-ttu-id="325e0-261">将新的可选开关参数“AssignIdentity”添加到 New-AzureRmSqlServer 和 Set-AzureRmSqlServer cmdlet 中，支持预配 SQL Server 资源的资源标识</span><span class="sxs-lookup"><span data-stu-id="325e0-261">Add new optional switch paramter "AssignIdentity" to New-AzureRmSqlServer and Set-AzureRmSqlServer cmdlets to support provisioning of a resource identity for the SQL server resource</span></span>
    * <span data-ttu-id="325e0-262">参数 ResourceGroupName 现对于 Get AzureRmSqlServer 来说可选</span><span class="sxs-lookup"><span data-stu-id="325e0-262">The parameter ResourceGroupName is now optional for Get-AzureRmSqlServer</span></span>
        - <span data-ttu-id="325e0-263">以下问题中提供详细信息：https://github.com/Azure/azure-powershell/issues/635</span><span class="sxs-lookup"><span data-stu-id="325e0-263">More information can be found in the following issue: https://github.com/Azure/azure-powershell/issues/635</span></span>
* <span data-ttu-id="325e0-264">ExpressRoute 的 ServiceManagement：</span><span class="sxs-lookup"><span data-stu-id="325e0-264">ServiceManagement   For ExpressRoute:</span></span>
    * <span data-ttu-id="325e0-265">更新了 New-AzureBgpPeering cmdlet 以添加以下选项：</span><span class="sxs-lookup"><span data-stu-id="325e0-265">Updated New-AzureBgpPeering cmdlet to add following new options :</span></span>
        - <span data-ttu-id="325e0-266">PeerAddressType：可指定值“IPv4”或“IPv6”，创建相应地址系列类型的 BGP 对等互连</span><span class="sxs-lookup"><span data-stu-id="325e0-266">PeerAddressType : Values of "IPv4" or "IPv6" can be specified to create a BGP Peering of the corresponding address family type</span></span>
    * <span data-ttu-id="325e0-267">更新了 Set-AzureBgpPeering cmdlet 以添加以下选项：</span><span class="sxs-lookup"><span data-stu-id="325e0-267">Updated Set-AzureBgpPeering cmdlet to add following new options :</span></span>
        - <span data-ttu-id="325e0-268">PeerAddressType：可指定值“IPv4”或“IPv6”，以更新相应地址系列类型的 BGP 对等互连</span><span class="sxs-lookup"><span data-stu-id="325e0-268">PeerAddressType : Values of "IPv4" or "IPv6" can be specified to update BGP Peering of the corresponding address family type</span></span>
    * <span data-ttu-id="325e0-269">更新了 Remove-AzureBgpPeering cmdlet 以添加以下选项：</span><span class="sxs-lookup"><span data-stu-id="325e0-269">Updated Remove-AzureBgpPeering cmdlet to add following new options :</span></span>
        - <span data-ttu-id="325e0-270">PeerAddressType：可指定值“IPv4”、“IPv6”或“全部”，以删除相应地址或全部地址系列类型的 BGP 对等互连</span><span class="sxs-lookup"><span data-stu-id="325e0-270">PeerAddressType : Values of "IPv4", "IPv6" or All can be specified to remove BGP Peering of the corresponding address family type or all of them</span></span>

## <a name="20170607---version-410"></a><span data-ttu-id="325e0-271">2017.06.07 - 版本 4.1.0</span><span class="sxs-lookup"><span data-stu-id="325e0-271">2017.06.07 - Version 4.1.0</span></span>
* <span data-ttu-id="325e0-272">AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="325e0-272">AnalysisServices</span></span>
    * <span data-ttu-id="325e0-273">新增 SKU：B1、B2、S0</span><span class="sxs-lookup"><span data-stu-id="325e0-273">New SKUs added: B1, B2, S0</span></span>
    * <span data-ttu-id="325e0-274">添加了增加/减少支持</span><span class="sxs-lookup"><span data-stu-id="325e0-274">Scale up/down support added</span></span>
* <span data-ttu-id="325e0-275">认知服务</span><span class="sxs-lookup"><span data-stu-id="325e0-275">CognitiveServices</span></span>
    * <span data-ttu-id="325e0-276">更新创建认知服务资源时许可协议的详细显示</span><span class="sxs-lookup"><span data-stu-id="325e0-276">Update detailed display of license agreements when creating Cognitive Services resources</span></span>
* <span data-ttu-id="325e0-277">计算</span><span class="sxs-lookup"><span data-stu-id="325e0-277">Compute</span></span>
    * <span data-ttu-id="325e0-278">为含多个托管磁盘的虚拟机修复 Test-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="325e0-278">Fix Test-AzureRmVMAEMExtension for virtual machines with multiple managed disks</span></span>
    * <span data-ttu-id="325e0-279">更新了 Set-AzureRmVMAEMExtension：添加高级托管磁盘的缓存信息</span><span class="sxs-lookup"><span data-stu-id="325e0-279">Updated Set-AzureRmVMAEMExtension: Add caching information for Premium managed disks</span></span>
    * <span data-ttu-id="325e0-280">Add-AzureRmVhd：对 vhd 的大小限制增加到了 4 TB。</span><span class="sxs-lookup"><span data-stu-id="325e0-280">Add-AzureRmVhd: The size limit on vhd is increased to 4TB.</span></span>
    * <span data-ttu-id="325e0-281">Stop-AzureRmVM：阐明 STayProvisioned 参数的文档</span><span class="sxs-lookup"><span data-stu-id="325e0-281">Stop-AzureRmVM: Clarify documentation for STayProvisioned parameter</span></span>
    * <span data-ttu-id="325e0-282">New-AzureRmDiskUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="325e0-282">New-AzureRmDiskUpdateConfig</span></span>
      * <span data-ttu-id="325e0-283">已弃用参数 CreateOption、StorageAccountId、ImageReference、SourceUri、SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="325e0-283">Deprecated parameters CreateOption, StorageAccountId, ImageReference, SourceUri, SourceResourceId</span></span>
    * <span data-ttu-id="325e0-284">Set-AzureRmDiskUpdateImageReference：已弃用 cmdlet</span><span class="sxs-lookup"><span data-stu-id="325e0-284">Set-AzureRmDiskUpdateImageReference: Deprecated cmdlet</span></span>
    * <span data-ttu-id="325e0-285">New-AzureRmSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="325e0-285">New-AzureRmSnapshotUpdateConfig</span></span>
      * <span data-ttu-id="325e0-286">已弃用参数 CreateOption、StorageAccountId、ImageReference、SourceUri、SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="325e0-286">Deprecated parameters CreateOption, StorageAccountId, ImageReference, SourceUri, SourceResourceId</span></span>
    * <span data-ttu-id="325e0-287">Set-AzureRmSnapshotUpdateImageReference：已弃用 cmdlet</span><span class="sxs-lookup"><span data-stu-id="325e0-287">Set-AzureRmSnapshotUpdateImageReference: Deprecated Cmdlet</span></span>
* <span data-ttu-id="325e0-288">DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="325e0-288">DataLakeStore</span></span>
    * <span data-ttu-id="325e0-289">Enable-AzureRmDataLakeStoreKeyVault (Enable-AdlStoreKeyVault)</span><span class="sxs-lookup"><span data-stu-id="325e0-289">Enable-AzureRmDataLakeStoreKeyVault (Enable-AdlStoreKeyVault)</span></span>
      * <span data-ttu-id="325e0-290">为 DataLake Store 启用 KeyVault 托管加密</span><span class="sxs-lookup"><span data-stu-id="325e0-290">Enable KeyVault managed encryption for a DataLake Store</span></span>
* <span data-ttu-id="325e0-291">DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="325e0-291">DevTestLabs</span></span>
    * <span data-ttu-id="325e0-292">更新 cmdlet，使其与当前版本和更新的开发测试实验室 API 版本一起使用。</span><span class="sxs-lookup"><span data-stu-id="325e0-292">Update cmdlets to work with current and updated DevTest Labs API version.</span></span>
* <span data-ttu-id="325e0-293">IotHub</span><span class="sxs-lookup"><span data-stu-id="325e0-293">IotHub</span></span>
    * <span data-ttu-id="325e0-294">添加对 IoTHub cmdlet 的路由支持</span><span class="sxs-lookup"><span data-stu-id="325e0-294">Add Routing support for IoTHub cmdlets</span></span>
* <span data-ttu-id="325e0-295">KeyVault</span><span class="sxs-lookup"><span data-stu-id="325e0-295">KeyVault</span></span>
  * <span data-ttu-id="325e0-296">支持 KeyVault 托管存储帐户密钥的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="325e0-296">New Cmdlets to support KeyVault Managed Storage Account Keys</span></span>
    * <span data-ttu-id="325e0-297">Get-AzureKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="325e0-297">Get-AzureKeyVaultManagedStorageAccount</span></span>
    * <span data-ttu-id="325e0-298">Add-AzureKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="325e0-298">Add-AzureKeyVaultManagedStorageAccount</span></span>
    * <span data-ttu-id="325e0-299">Remove-AzureKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="325e0-299">Remove-AzureKeyVaultManagedStorageAccount</span></span>
    * <span data-ttu-id="325e0-300">Update-AzureKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="325e0-300">Update-AzureKeyVaultManagedStorageAccount</span></span>
    * <span data-ttu-id="325e0-301">Update-AzureKeyVaultManagedStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="325e0-301">Update-AzureKeyVaultManagedStorageAccountKey</span></span>
    * <span data-ttu-id="325e0-302">Get-AzureKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="325e0-302">Get-AzureKeyVaultManagedStorageSasDefinition</span></span>
    * <span data-ttu-id="325e0-303">Set-AzureKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="325e0-303">Set-AzureKeyVaultManagedStorageSasDefinition</span></span>
    * <span data-ttu-id="325e0-304">Remove-AzureKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="325e0-304">Remove-AzureKeyVaultManagedStorageSasDefinition</span></span>
* <span data-ttu-id="325e0-305">网络</span><span class="sxs-lookup"><span data-stu-id="325e0-305">Network</span></span>
    * <span data-ttu-id="325e0-306">Get AzureRmNetworkUsage：显示网络使用情况和容量详细信息的新 cmdlet</span><span class="sxs-lookup"><span data-stu-id="325e0-306">Get-AzureRmNetworkUsage: New cmdlet to show network usage and capacity details</span></span>
    * <span data-ttu-id="325e0-307">为 VirtualNetworkGateways 添加了新的 GatewaySku 选项</span><span class="sxs-lookup"><span data-stu-id="325e0-307">Added new GatewaySku options for VirtualNetworkGateways</span></span>
        * <span data-ttu-id="325e0-308">VpnGw1、VpnGw2、VpnGw3 是为 Vpn 网关添加的新 Sku</span><span class="sxs-lookup"><span data-stu-id="325e0-308">VpnGw1, VpnGw2, VpnGw3 are the new Skus added for Vpn gateways</span></span>
    * <span data-ttu-id="325e0-309">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="325e0-309">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>
      * <span data-ttu-id="325e0-310">已修复的帮助示例</span><span class="sxs-lookup"><span data-stu-id="325e0-310">Fixed  help examples</span></span>
* <span data-ttu-id="325e0-311">通知中心</span><span class="sxs-lookup"><span data-stu-id="325e0-311">NotificationHubs</span></span>
    * <span data-ttu-id="325e0-312">新 API 的 NotificationHubs cmdlet 的透明更新</span><span class="sxs-lookup"><span data-stu-id="325e0-312">Transparent Update to NotificationHubs cmdlets for new API</span></span>
* <span data-ttu-id="325e0-313">配置文件</span><span class="sxs-lookup"><span data-stu-id="325e0-313">Profile</span></span>
    * <span data-ttu-id="325e0-314">Resolve-AzureRmError</span><span class="sxs-lookup"><span data-stu-id="325e0-314">Resolve-AzureRmError</span></span>
      * <span data-ttu-id="325e0-315">显示 cmdlet 引发的错误和异常的详细信息（包括服务器请求/响应数据）的新 cmdlet</span><span class="sxs-lookup"><span data-stu-id="325e0-315">New cmdlet to show details of errors and exceptions thrown by cmdlets, including server request/response data</span></span>
    * <span data-ttu-id="325e0-316">Send-Feedback</span><span class="sxs-lookup"><span data-stu-id="325e0-316">Send-Feedback</span></span>
      * <span data-ttu-id="325e0-317">已启用在不登录的情况下发送反馈的功能</span><span class="sxs-lookup"><span data-stu-id="325e0-317">Enabled sending feedback without logging in</span></span>
    * <span data-ttu-id="325e0-318">Get-AzureRmSubscription</span><span class="sxs-lookup"><span data-stu-id="325e0-318">Get-AzureRmSubscription</span></span>
      * <span data-ttu-id="325e0-319">修复检索 CSP 订阅时的 bug</span><span class="sxs-lookup"><span data-stu-id="325e0-319">Fix bug in retreiving CSP subscriptions</span></span>
* <span data-ttu-id="325e0-320">资源</span><span class="sxs-lookup"><span data-stu-id="325e0-320">Resources</span></span>
    * <span data-ttu-id="325e0-321">已修复以下问题：如果 roleassignments 数大于 1000，Get-AzureRMRoleAssignment 将导致错误请求</span><span class="sxs-lookup"><span data-stu-id="325e0-321">Fixed issue where Get-AzureRMRoleAssignment would result in a Bad Request if the number of roleassignments where greater than 1000</span></span>
        * <span data-ttu-id="325e0-322">现在，即使要返回的 roleassignments 数大于 1000，用户也可使用 Get-AzureRMRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="325e0-322">Users can now use Get-AzureRMRoleAssignment even if the roleassignments to be returned is greater than 1000</span></span>
* <span data-ttu-id="325e0-323">Sql</span><span class="sxs-lookup"><span data-stu-id="325e0-323">Sql</span></span>
    * <span data-ttu-id="325e0-324">Restore-AzureRmSqlDatabase：更新文档示例</span><span class="sxs-lookup"><span data-stu-id="325e0-324">Restore-AzureRmSqlDatabase: Update documentation example</span></span>
* <span data-ttu-id="325e0-325">存储</span><span class="sxs-lookup"><span data-stu-id="325e0-325">Storage</span></span>
    * <span data-ttu-id="325e0-326">将 AssignIdentity 设置支持添加到资源模式存储帐户 cmdlet</span><span class="sxs-lookup"><span data-stu-id="325e0-326">Add AssignIdentity setting support to resource mode storage account cmdlets</span></span>
        * <span data-ttu-id="325e0-327">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="325e0-327">New-AzureRmStorageAccount</span></span>
        * <span data-ttu-id="325e0-328">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="325e0-328">Set-AzureRmStorageAccount</span></span>
    * <span data-ttu-id="325e0-329">将客户密钥支持添加到资源模式存储帐户 cmdlet</span><span class="sxs-lookup"><span data-stu-id="325e0-329">Add Customer Key Support to resource mode storage account cmdlets</span></span>
        * <span data-ttu-id="325e0-330">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="325e0-330">Set-AzureRmStorageAccount</span></span>
        * <span data-ttu-id="325e0-331">New-AzureRmStorageAccountEncryptionKeySource</span><span class="sxs-lookup"><span data-stu-id="325e0-331">New-AzureRmStorageAccountEncryptionKeySource</span></span>
* <span data-ttu-id="325e0-332">TrafficManager</span><span class="sxs-lookup"><span data-stu-id="325e0-332">TrafficManager</span></span>

    * <span data-ttu-id="325e0-333">新的监视设置“MonitorIntervalInSeconds”、“MonitorTimeoutInSeconds”、“MonitorToleratedNumberOfFailures”</span><span class="sxs-lookup"><span data-stu-id="325e0-333">New Monitor settings 'MonitorIntervalInSeconds', 'MonitorTimeoutInSeconds', 'MonitorToleratedNumberOfFailures'</span></span>
    * <span data-ttu-id="325e0-334">新监视协议“TCP”</span><span class="sxs-lookup"><span data-stu-id="325e0-334">New Monitor protocol 'TCP'</span></span>
* <span data-ttu-id="325e0-335">ServiceManagement</span><span class="sxs-lookup"><span data-stu-id="325e0-335">ServiceManagement</span></span>
    * <span data-ttu-id="325e0-336">Add-AzureVhd：对 vhd 的大小限制增加到了 4 TB。</span><span class="sxs-lookup"><span data-stu-id="325e0-336">Add-AzureVhd: The size limit on vhd is increased to 4TB.</span></span>
    * <span data-ttu-id="325e0-337">New-AzureBGPPeering：支持 LegacyMode</span><span class="sxs-lookup"><span data-stu-id="325e0-337">New-AzureBGPPeering: Support LegacyMode</span></span>
* <span data-ttu-id="325e0-338">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="325e0-338">Azure.Storage</span></span>
    * <span data-ttu-id="325e0-339">更新针对接受通配符的参数的帮助并更新 StorageContext 类型</span><span class="sxs-lookup"><span data-stu-id="325e0-339">Update help for parameters that accept wildcard characters and update StorageContext type</span></span>

## <a name="20170523---version-402"></a><span data-ttu-id="325e0-340">2017.05.23 - 版本 4.0.2</span><span class="sxs-lookup"><span data-stu-id="325e0-340">2017.05.23 - Version 4.0.2</span></span>
* <span data-ttu-id="325e0-341">配置文件</span><span class="sxs-lookup"><span data-stu-id="325e0-341">Profile</span></span>
    * <span data-ttu-id="325e0-342">Add-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="325e0-342">Add-AzureRmAccount</span></span>
      * <span data-ttu-id="325e0-343">添加了 `-EnvironmentName` 参数别名，实现与 AzureRM.profile 2.x 版的后向兼容性</span><span class="sxs-lookup"><span data-stu-id="325e0-343">Added `-EnvironmentName` parameter alis for backward compatibility with 2.x versions of AzureRM.profile</span></span>

## <a name="20170512---version-401"></a><span data-ttu-id="325e0-344">2017.05.12 - 版本 4.0.1</span><span class="sxs-lookup"><span data-stu-id="325e0-344">2017.05.12 - Version 4.0.1</span></span>
 * <span data-ttu-id="325e0-345">修复了 New-AzureStorageContext 在脱机情况下的问题：https://github.com/Azure/azure-powershell/issues/3939</span><span class="sxs-lookup"><span data-stu-id="325e0-345">Fix issue with New-AzureStorageContext in offline scenarios: https://github.com/Azure/azure-powershell/issues/3939</span></span>

## <a name="20170510---version-400"></a><span data-ttu-id="325e0-346">2017.05.10 - 版本 4.0.0</span><span class="sxs-lookup"><span data-stu-id="325e0-346">2017.05.10 - Version 4.0.0</span></span>


* <span data-ttu-id="325e0-347">此版本包含重大更改。</span><span class="sxs-lookup"><span data-stu-id="325e0-347">This release contains breaking changes.</span></span> <span data-ttu-id="325e0-348">请参阅[迁移指南](https://aka.ms/azps-migration-guide)，了解有关更改的详细信息及其对现有脚本的影响。</span><span class="sxs-lookup"><span data-stu-id="325e0-348">Please see [the migration guide](https://aka.ms/azps-migration-guide) for change details and the impact on existing scripts.</span></span>
* <span data-ttu-id="325e0-349">ApiManagement</span><span class="sxs-lookup"><span data-stu-id="325e0-349">ApiManagement</span></span>
  - <span data-ttu-id="325e0-350">添加了在 New-AzureRmApiManagementGroup 中配置外部组的支持。</span><span class="sxs-lookup"><span data-stu-id="325e0-350">Added support for configuring external groups in New-AzureRmApiManagementGroup.</span></span>
* <span data-ttu-id="325e0-351">计费</span><span class="sxs-lookup"><span data-stu-id="325e0-351">Billing</span></span>
  - <span data-ttu-id="325e0-352">全新 Cmdlet Get-AzureRmBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="325e0-352">New Cmdlet Get-AzureRmBillingPeriod</span></span>
    + <span data-ttu-id="325e0-353">用于检索订阅的 Azure 计费周期的 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="325e0-353">cmdlet to retrieve azure billing periods of the subscription.</span></span>
  - <span data-ttu-id="325e0-354">更新 Cmdlet Get-AzureRmBillingInvoice</span><span class="sxs-lookup"><span data-stu-id="325e0-354">Update Cmdlet Get-AzureRmBillingInvoice</span></span>
  - <span data-ttu-id="325e0-355">新属性 BillingPeriodNames</span><span class="sxs-lookup"><span data-stu-id="325e0-355">new property BillingPeriodNames</span></span>
  - <span data-ttu-id="325e0-356">列表视图中的输出</span><span class="sxs-lookup"><span data-stu-id="325e0-356">output in list view</span></span>
* <span data-ttu-id="325e0-357">计算</span><span class="sxs-lookup"><span data-stu-id="325e0-357">Compute</span></span>
  - <span data-ttu-id="325e0-358">更新了 Set-AzureRmVMAEMExtension 和 Test-AzureRmVMAEMExtension cmdlet，以支持高级托管磁盘</span><span class="sxs-lookup"><span data-stu-id="325e0-358">Updated Set-AzureRmVMAEMExtension and Test-AzureRmVMAEMExtension cmdlets to support Premium managed disks</span></span>
  - <span data-ttu-id="325e0-359">用于 IaaS VM 和故障还原的备份加密设置</span><span class="sxs-lookup"><span data-stu-id="325e0-359">Backup encryption settings for IaaS VMs and restore on failure</span></span>
  - <span data-ttu-id="325e0-360">ChefServiceInterval 选项现已重命名为 ChefDaemonInterval。</span><span class="sxs-lookup"><span data-stu-id="325e0-360">ChefServiceInterval option is renamed to ChefDaemonInterval now.</span></span> <span data-ttu-id="325e0-361">但旧名称仍可继续使用。</span><span class="sxs-lookup"><span data-stu-id="325e0-361">Old one will continue to work however.</span></span>
  - <span data-ttu-id="325e0-362">从 PS VM 对象中删除重复的 DataDiskNames 和 NetworkInterfaceIDs 属性。</span><span class="sxs-lookup"><span data-stu-id="325e0-362">Remove duplicated DataDiskNames and NetworkInterfaceIDs properties from PS VM object.</span></span>
  - <span data-ttu-id="325e0-363">让 DataDiskNames 参数在 Remove-AzureRmVMDataDisk 中、NetworkInterfaceIDs 参数在 Remove-AzureRmVMNetworkInterface 中变为可选。</span><span class="sxs-lookup"><span data-stu-id="325e0-363">Make DataDiskNames and NetworkInterfaceIDs parameters optional in Remove-AzureRmVMDataDisk and Remove-AzureRmVMNetworkInterface, respectively.</span></span>
  - <span data-ttu-id="325e0-364">修复 Get cmdlet 返回列表对象时的 Get cmdlet 管道问题。</span><span class="sxs-lookup"><span data-stu-id="325e0-364">Fix the piping issue of Get cmdlets when the Get cmdlets return a list object.</span></span>
  - <span data-ttu-id="325e0-365">已重命名与 RDFE cmdlet 冲突的 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="325e0-365">Cmdlets that conflicted with RDFE cmdlets have been renamed.</span></span> <span data-ttu-id="325e0-366">有关详细信息，请参阅“问题”https://github.com/Azure/azure-powershell/issues/2917</span><span class="sxs-lookup"><span data-stu-id="325e0-366">See issue https://github.com/Azure/azure-powershell/issues/2917 for more details</span></span>
    + <span data-ttu-id="325e0-367">`New-AzureVMSqlServerAutoBackupConfig` 已重名为 `New-AzureRmVMSqlServerAutoBackupConfig`</span><span class="sxs-lookup"><span data-stu-id="325e0-367">`New-AzureVMSqlServerAutoBackupConfig` has been renamed to `New-AzureRmVMSqlServerAutoBackupConfig`</span></span>
    + <span data-ttu-id="325e0-368">`New-AzureVMSqlServerAutoPatchingConfig` 已重名为 `New-AzureRmVMSqlServerAutoPatchingConfig`</span><span class="sxs-lookup"><span data-stu-id="325e0-368">`New-AzureVMSqlServerAutoPatchingConfig` has been renamed to `New-AzureRmVMSqlServerAutoPatchingConfig`</span></span>
    + <span data-ttu-id="325e0-369">`New-AzureVMSqlServerKeyVaultCredentialConfig` 已重名为 `New-AzureRmVMSqlServerKeyVaultCredentialConfig`</span><span class="sxs-lookup"><span data-stu-id="325e0-369">`New-AzureVMSqlServerKeyVaultCredentialConfig` has been renamed to `New-AzureRmVMSqlServerKeyVaultCredentialConfig`</span></span>
* <span data-ttu-id="325e0-370">消耗</span><span class="sxs-lookup"><span data-stu-id="325e0-370">Consumption</span></span>
  - <span data-ttu-id="325e0-371">新 Cmdlet Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="325e0-371">New Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>
    + <span data-ttu-id="325e0-372">用于检索订阅详细使用情况的 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="325e0-372">cmdlet to retrieve usage details of the subscription.</span></span>
* <span data-ttu-id="325e0-373">ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="325e0-373">ContainerRegistry</span></span>
  - <span data-ttu-id="325e0-374">为 Azure 容器注册表添加 PowerShell cmdlet</span><span class="sxs-lookup"><span data-stu-id="325e0-374">Add PowerShell cmdlets for Azure Container Registry</span></span>
    + <span data-ttu-id="325e0-375">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="325e0-375">New-AzureRmContainerRegistry</span></span>
    + <span data-ttu-id="325e0-376">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="325e0-376">Get-AzureRmContainerRegistry</span></span>
    + <span data-ttu-id="325e0-377">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="325e0-377">Update-AzureRmContainerRegistry</span></span>
    + <span data-ttu-id="325e0-378">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="325e0-378">Remove-AzureRmContainerRegistry</span></span>
    + <span data-ttu-id="325e0-379">Get-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="325e0-379">Get-AzureRmContainerRegistryCredential</span></span>
    + <span data-ttu-id="325e0-380">Update-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="325e0-380">Update-AzureRmContainerRegistryCredential</span></span>
    + <span data-ttu-id="325e0-381">Test-AzureRmContainerRegistryNameAvailability</span><span class="sxs-lookup"><span data-stu-id="325e0-381">Test-AzureRmContainerRegistryNameAvailability</span></span>
* <span data-ttu-id="325e0-382">DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="325e0-382">DataLakeAnalytics</span></span>
  - <span data-ttu-id="325e0-383">添加对获取和列出目录包的支持</span><span class="sxs-lookup"><span data-stu-id="325e0-383">Add support for catalog package get and list</span></span>
  - <span data-ttu-id="325e0-384">添加了从更深上级列出以下目录项的支持：</span><span class="sxs-lookup"><span data-stu-id="325e0-384">Add support for listing the following catalog items from deeper ancestors:</span></span>
    + <span data-ttu-id="325e0-385">表</span><span class="sxs-lookup"><span data-stu-id="325e0-385">Table</span></span>
    + <span data-ttu-id="325e0-386">TVF</span><span class="sxs-lookup"><span data-stu-id="325e0-386">TVF</span></span>
    + <span data-ttu-id="325e0-387">查看</span><span class="sxs-lookup"><span data-stu-id="325e0-387">View</span></span>
    + <span data-ttu-id="325e0-388">统计信息</span><span class="sxs-lookup"><span data-stu-id="325e0-388">Statistics</span></span>
* <span data-ttu-id="325e0-389">DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="325e0-389">DataLakeStore</span></span>
  - <span data-ttu-id="325e0-390">对于 `Import-AzureRMDataLakeStoreItem` 和 `Export-AzureRMDataLakeStoreItem`，默认情况下禁用跟踪日志记录功能以提高性能。</span><span class="sxs-lookup"><span data-stu-id="325e0-390">For `Import-AzureRMDataLakeStoreItem` and `Export-AzureRMDataLakeStoreItem` trace logging has been disabled by default to improve performance.</span></span> <span data-ttu-id="325e0-391">如果需要跟踪日志记录，请使用 `-DiagnosticLogLevel` 和 `-DiagnosticLogPath` 参数</span><span class="sxs-lookup"><span data-stu-id="325e0-391">If trace logging is desired please use the `-DiagnosticLogLevel` and `-DiagnosticLogPath` parameters</span></span>
  - <span data-ttu-id="325e0-392">修复了向 ADLS 上传大量小文件时可能导致 PowerShell 崩溃的 bug。</span><span class="sxs-lookup"><span data-stu-id="325e0-392">Fixed a bug that would sometimes cause PowerShell to crash when uploading lots of small file to ADLS.</span></span>
* <span data-ttu-id="325e0-393">EventHub</span><span class="sxs-lookup"><span data-stu-id="325e0-393">EventHub</span></span>
  - <span data-ttu-id="325e0-394">Bug 修复：</span><span class="sxs-lookup"><span data-stu-id="325e0-394">Bug fix :</span></span>
    + <span data-ttu-id="325e0-395">修复 Set-AzureRmEventHubNamespace cmdlet 错误 -“层”不能为 null，应为“SkuName”</span><span class="sxs-lookup"><span data-stu-id="325e0-395">Fix for Set-AzureRmEventHubNamespace cmdlet error  - 'Tier' cannot be null, where it should be 'SkuName'</span></span>
    + <span data-ttu-id="325e0-396">Set-AzureRmEventHub - 修复更新 EventHub 时出现的“未将对象引用设置为对象的实例”错误</span><span class="sxs-lookup"><span data-stu-id="325e0-396">Set-AzureRmEventHub - Fix 'Object reference not set to an instance of an object' error while updating EventHub</span></span>
* <span data-ttu-id="325e0-397">洞察力</span><span class="sxs-lookup"><span data-stu-id="325e0-397">Insights</span></span>
  - <span data-ttu-id="325e0-398">Add-AzureRm*AlertRule</span><span class="sxs-lookup"><span data-stu-id="325e0-398">Add-AzureRm*AlertRule</span></span>
    + <span data-ttu-id="325e0-399">返回单个对象：newResource、statusCode、requestId</span><span class="sxs-lookup"><span data-stu-id="325e0-399">Returns a single object: newResource, statusCode, requestId</span></span>
  - <span data-ttu-id="325e0-400">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="325e0-400">Get-AzureRmAlertRule</span></span>
    + <span data-ttu-id="325e0-401">现会枚举输出，而不是将其视作单个对象。</span><span class="sxs-lookup"><span data-stu-id="325e0-401">The output is now enumerated instead of considered a single object.</span></span> <span data-ttu-id="325e0-402">其类型未发生更改，仍为列表。</span><span class="sxs-lookup"><span data-stu-id="325e0-402">Its type did not change, it is still a list.</span></span>
  - <span data-ttu-id="325e0-403">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="325e0-403">Remove-AzureRmAlertRule</span></span>
    + <span data-ttu-id="325e0-404">statusCode 遵循请求返回的状态代码，而之前其状态始终为“确定”。</span><span class="sxs-lookup"><span data-stu-id="325e0-404">The statusCode follows the status code returned by the request, before it was Ok always.</span></span>
  - <span data-ttu-id="325e0-405">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="325e0-405">Add-AzureRmAutoscaleSetting</span></span>
    + <span data-ttu-id="325e0-406">现在返回单个对象（以前返回列表），其中包含 statusCode、requestId 和新创建/更新的资源。</span><span class="sxs-lookup"><span data-stu-id="325e0-406">Returns now a single object (not a list as before) containing statusCode, requestId, and the newly created/updated resource.</span></span>
    + <span data-ttu-id="325e0-407">状态代码遵循请求返回的状态，之前其状态始终为“确定”。</span><span class="sxs-lookup"><span data-stu-id="325e0-407">The status code follows the status returned by the request, before it was always Ok.</span></span>
  - <span data-ttu-id="325e0-408">New-AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="325e0-408">New-AzureRmAutoscaleRule</span></span>
    + <span data-ttu-id="325e0-409">已扩展参数 ScaleActionType，该参数现接收以下值：ChangeCount、PercentChangeCount、ExactCount。</span><span class="sxs-lookup"><span data-stu-id="325e0-409">The parameter ScaleActionType has been extended, it receives the following values now: ChangeCount, PercentChangeCount, ExactCount.</span></span>
  - <span data-ttu-id="325e0-410">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="325e0-410">Remove-AzureRmAutoscaleSetting</span></span>
    + <span data-ttu-id="325e0-411">输出中的 statusCode 遵循请求返回的状态代码。</span><span class="sxs-lookup"><span data-stu-id="325e0-411">The statusCode in the output follows the statusCode returned by the request.</span></span> <span data-ttu-id="325e0-412">之前其状态始终为“确定”。</span><span class="sxs-lookup"><span data-stu-id="325e0-412">Before it was always Ok.</span></span>
  - <span data-ttu-id="325e0-413">Get-AzureRMLogProfile</span><span class="sxs-lookup"><span data-stu-id="325e0-413">Get-AzureRMLogProfile</span></span>
    + <span data-ttu-id="325e0-414">现会枚举输出。</span><span class="sxs-lookup"><span data-stu-id="325e0-414">The output is now enumerated.</span></span> <span data-ttu-id="325e0-415">以前将其视作单个对象。</span><span class="sxs-lookup"><span data-stu-id="325e0-415">Before it was considered a single object.</span></span> <span data-ttu-id="325e0-416">和以前一样，输出类型仍为列表。</span><span class="sxs-lookup"><span data-stu-id="325e0-416">The type of the output remains a list as before.</span></span>
  - <span data-ttu-id="325e0-417">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="325e0-417">Remove-AzureRmLogProfile</span></span>
    + <span data-ttu-id="325e0-418">已实现 PassThru 参数。</span><span class="sxs-lookup"><span data-stu-id="325e0-418">The PassThru parameter has been implemented.</span></span>
  - <span data-ttu-id="325e0-419">指标 API</span><span class="sxs-lookup"><span data-stu-id="325e0-419">Metrics API</span></span>
    + <span data-ttu-id="325e0-420">SDK 现从 MDM 检索指标。</span><span class="sxs-lookup"><span data-stu-id="325e0-420">The SDK now retrieves metrics from MDM.</span></span>
  - <span data-ttu-id="325e0-421">Get-AzureRmMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="325e0-421">Get-AzureRmMetricDefinition</span></span>
    + <span data-ttu-id="325e0-422">输出仍为列表，但列表的结构有所更改。</span><span class="sxs-lookup"><span data-stu-id="325e0-422">The output is still a list, but the structure of the list changed.</span></span>
  - <span data-ttu-id="325e0-423">Get-AzureRmMetric</span><span class="sxs-lookup"><span data-stu-id="325e0-423">Get-AzureRmMetric</span></span>
    + <span data-ttu-id="325e0-424">已更改调用。</span><span class="sxs-lookup"><span data-stu-id="325e0-424">The call has changed.</span></span> <span data-ttu-id="325e0-425">新语法为： Get-AzureRmMetric ResourceId [MetricNames [TimeGrain] [AggregationType] [StartTime] [EndTime]] [DetailedOutput]</span><span class="sxs-lookup"><span data-stu-id="325e0-425">This is the new syntax: Get-AzureRmMetric ResourceId [MetricNames [TimeGrain] [AggregationType] [StartTime] [EndTime]] [DetailedOutput]</span></span>
    + <span data-ttu-id="325e0-426">输出为列表，其元素的结构有所更改。</span><span class="sxs-lookup"><span data-stu-id="325e0-426">The output is a list, and the structure of its elements has changed.</span></span>
* <span data-ttu-id="325e0-427">KeyVault</span><span class="sxs-lookup"><span data-stu-id="325e0-427">KeyVault</span></span>
  - <span data-ttu-id="325e0-428">添加对 KeyVault 机密的备份/还原支持</span><span class="sxs-lookup"><span data-stu-id="325e0-428">Adding backup/restore support for KeyVault secrets</span></span>
    + <span data-ttu-id="325e0-429">可备份和还原机密，这与当前支持的密钥功能相符</span><span class="sxs-lookup"><span data-stu-id="325e0-429">Secrets can be backed up and restored, matching the functionality currently supported for Keys</span></span>

  - <span data-ttu-id="325e0-430">密钥和机密的备份 cmdlet 现在接受相应对象作为输入参数</span><span class="sxs-lookup"><span data-stu-id="325e0-430">Backup cmdlets for Keys and Secrets now accept a corresponding object as an input parameter</span></span>
    + <span data-ttu-id="325e0-431">调用方可能捆绑检索和备份操作：Get-AzureKeyVaultKey -VaultName myVault -Name myKey | Backup-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="325e0-431">The caller may chain retrieval and backup operations: Get-AzureKeyVaultKey -VaultName myVault -Name myKey | Backup-AzureKeyVaultKey</span></span>

  - <span data-ttu-id="325e0-432">备份 cmdlet 现支持 -Force 开关以覆盖现有文件</span><span class="sxs-lookup"><span data-stu-id="325e0-432">Backup cmdlets now support a -Force switch to overwrite an existing file</span></span>
    + <span data-ttu-id="325e0-433">请注意：尝试覆盖现有文件这一操作不再引发，而是提示用户选择继续操作的方式。</span><span class="sxs-lookup"><span data-stu-id="325e0-433">Note that attempting to overwrite an existing file will no longer throw, and will instead prompt the user for a choice on how to proceed.</span></span>
* <span data-ttu-id="325e0-434">LogicApp</span><span class="sxs-lookup"><span data-stu-id="325e0-434">LogicApp</span></span>
  - <span data-ttu-id="325e0-435">交换控制编号灾难恢复 cmdlet 的新参数：</span><span class="sxs-lookup"><span data-stu-id="325e0-435">New parameters for Interchange Control Number disaster recovery cmdlets:</span></span>
    + <span data-ttu-id="325e0-436">可选 - 用于指定相关控制编号的 AgreementType 参数（“X12”或“Edifact”）</span><span class="sxs-lookup"><span data-stu-id="325e0-436">Optional -AgreementType parameter ("X12", or "Edifact") to specify the relevant control numbers</span></span>
* <span data-ttu-id="325e0-437">MachineLearning</span><span class="sxs-lookup"><span data-stu-id="325e0-437">MachineLearning</span></span>
  - <span data-ttu-id="325e0-438">使用新版 Azure 机器学习 .Net SDK 并添加新 cmdlet</span><span class="sxs-lookup"><span data-stu-id="325e0-438">Consume new version of Azure Machine Learning .Net SDK and add a new cmdlet</span></span>
    + <span data-ttu-id="325e0-439">Add-AzureRmMlWebServiceRegionalProperty</span><span class="sxs-lookup"><span data-stu-id="325e0-439">Add-AzureRmMlWebServiceRegionalProperty</span></span>
  - <span data-ttu-id="325e0-440">帮助文本中的措词小修复。</span><span class="sxs-lookup"><span data-stu-id="325e0-440">Minor wording fixes in help text.</span></span>
* <span data-ttu-id="325e0-441">网络</span><span class="sxs-lookup"><span data-stu-id="325e0-441">Network</span></span>
  - <span data-ttu-id="325e0-442">添加了 Test-AzureRmNetworkWatcherConnectivity cmdlet</span><span class="sxs-lookup"><span data-stu-id="325e0-442">Added Test-AzureRmNetworkWatcherConnectivity cmdlet</span></span>
    + <span data-ttu-id="325e0-443">返回有关指定源 VM 和目标的连接信息</span><span class="sxs-lookup"><span data-stu-id="325e0-443">Returns connectivity information for a specified source VM and a destination</span></span>
    + <span data-ttu-id="325e0-444">如果源和目标之间无法建立连接，则该 cmdlet 返回问题相关详细信息</span><span class="sxs-lookup"><span data-stu-id="325e0-444">If connectivity between the source and destination cannot be established, the cmdlet returns details about the issue</span></span>
* <span data-ttu-id="325e0-445">配置文件</span><span class="sxs-lookup"><span data-stu-id="325e0-445">Profile</span></span>
  - <span data-ttu-id="325e0-446">添加了 \`Send-Feedback' cmdlet：允许用户启动一组会向 Azure PowerShell 团队发送反馈的提示。</span><span class="sxs-lookup"><span data-stu-id="325e0-446">Added \`Send-Feedback' cmdlet: allows a user to initiate a set of prompts which sends feedback to the Azure PowerShell team.</span></span>
  - <span data-ttu-id="325e0-447">已删除以下别名，因为它们与 Azure 模块中的现有 cmdlet 名称冲突：</span><span class="sxs-lookup"><span data-stu-id="325e0-447">The following aliases have been removed as they conflicted with existing cmdlet names in the Azure module:</span></span>
    + <span data-ttu-id="325e0-448">`Enable-AzureDataCollection`（由 `Enable-AzureRmDataCollection` 支持）</span><span class="sxs-lookup"><span data-stu-id="325e0-448">`Enable-AzureDataCollection` (supported by `Enable-AzureRmDataCollection`)</span></span>
    + <span data-ttu-id="325e0-449">`Disable-AzureDataCollection`（由 `Disable-AzureRmDataCollection` 支持）</span><span class="sxs-lookup"><span data-stu-id="325e0-449">`Disable-AzureDataCollection` (supported by `Disable-AzureRmDataCollection`)</span></span>
* <span data-ttu-id="325e0-450">中继</span><span class="sxs-lookup"><span data-stu-id="325e0-450">Relay</span></span>
  - <span data-ttu-id="325e0-451">为 Azure 中继添加 cmdlet，让用户能够创建和管理所有 Azure 中继资源。</span><span class="sxs-lookup"><span data-stu-id="325e0-451">Adds cmdlets for the Azure Relay which allows users to create and manage all Azure Relay resources.</span></span>
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
* <span data-ttu-id="325e0-452">资源</span><span class="sxs-lookup"><span data-stu-id="325e0-452">Resources</span></span>
  - <span data-ttu-id="325e0-453">支持 New-AzureRmResourceGroupDeployment 的跨资源组部署</span><span class="sxs-lookup"><span data-stu-id="325e0-453">Support cross-resource-group deployments for New-AzureRmResourceGroupDeployment</span></span>
    + <span data-ttu-id="325e0-454">现在，用户可使用嵌套部署在不同资源组之间进行部署。</span><span class="sxs-lookup"><span data-stu-id="325e0-454">Users can now use nested deployments to deploy to different resource groups.</span></span>
* <span data-ttu-id="325e0-455">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="325e0-455">ServiceBus</span></span>

  - <span data-ttu-id="325e0-456">Bug 修复：ServiceBus 队列对象属性值设置为 null，该对象用作 Set-AzureRmServiceBusQueue cmdlet 中的输入参数，用于更新队列。</span><span class="sxs-lookup"><span data-stu-id="325e0-456">Bug Fix: ServiceBus Queue object property values were set to null, the object is used as input parameter in Set-AzureRmServiceBusQueue cmdlet to update Queue.</span></span>
   - <span data-ttu-id="325e0-457">受影响的属性为 LockDuration、EntityAvailabilityStatus、DuplicateDetectionHistoryTimeWindow、MaxDeliveryCount and MessageCount</span><span class="sxs-lookup"><span data-stu-id="325e0-457">Properties affected are LockDuration, EntityAvailabilityStatus, DuplicateDetectionHistoryTimeWindow, MaxDeliveryCount and MessageCount</span></span>
* <span data-ttu-id="325e0-458">ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="325e0-458">ServiceFabric</span></span>

  - <span data-ttu-id="325e0-459">添加了适用于 Service Fabric 的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="325e0-459">Added cmdlets for service fabric</span></span>
    + <span data-ttu-id="325e0-460">Add-AzureRmServiceFabricApplicationCertificate 添加将用作应用程序证书的证书</span><span class="sxs-lookup"><span data-stu-id="325e0-460">Add-AzureRmServiceFabricApplicationCertificate       Add a certificate which will be used as application certificate</span></span>
    + <span data-ttu-id="325e0-461">Add-AzureRmServiceFabricClientCertificate 向群集设置添加公用名或指纹，以便进行客户端身份验证</span><span class="sxs-lookup"><span data-stu-id="325e0-461">Add-AzureRmServiceFabricClientCertificate       Add a common name or thumbprint to the cluster settings for client authentication</span></span>
    + <span data-ttu-id="325e0-462">Add-AzureRmServiceFabricClusterCertificate 向群集添加辅助群集证书，以便滚动显示现有证书</span><span class="sxs-lookup"><span data-stu-id="325e0-462">Add-AzureRmServiceFabricClusterCertificate       Add a secondary cluster certificate to the cluster for rolling over the existing certificate</span></span>
    + <span data-ttu-id="325e0-463">Add-AzureRmServiceFabricNodes 向群集添加特定节点类型的节点/VM</span><span class="sxs-lookup"><span data-stu-id="325e0-463">Add-AzureRmServiceFabricNodes       Add nodes/VMs of a specific node type to a cluster</span></span>
    + <span data-ttu-id="325e0-464">Add-AzureRmServiceFabricNodeType 向现有群集添加节点类型/VM</span><span class="sxs-lookup"><span data-stu-id="325e0-464">Add-AzureRmServiceFabricNodeType       Add a node type/VMs to an existing cluster</span></span>
    + <span data-ttu-id="325e0-465">Get-AzureRmServiceFabricCluster 获取群集资源的详细信息</span><span class="sxs-lookup"><span data-stu-id="325e0-465">Get-AzureRmServiceFabricCluster       Get the details of the cluster resource</span></span>
    + <span data-ttu-id="325e0-466">New-AzureRmServiceFabricCluster 新建 ServiceFabric 群集。</span><span class="sxs-lookup"><span data-stu-id="325e0-466">New-AzureRmServiceFabricCluster Create a new ServiceFabric cluster.</span></span> <span data-ttu-id="325e0-467">此命令包含许多重载，适用于各种方案</span><span class="sxs-lookup"><span data-stu-id="325e0-467">This command has many overloads to cover various scenarios</span></span>
    + <span data-ttu-id="325e0-468">Remove-AzureRmServiceFabricClientCertificate 删除用于访问群集的客户端证书</span><span class="sxs-lookup"><span data-stu-id="325e0-468">Remove-AzureRmServiceFabricClientCertificate       Remove a client certificate from being used to access a cluster</span></span>
    + <span data-ttu-id="325e0-469">Remove-AzureRmServiceFabricClusterCertificate 删除用于确保群集安全性的群集证书</span><span class="sxs-lookup"><span data-stu-id="325e0-469">Remove-AzureRmServiceFabricClusterCertificate       Remove a cluster certificate from being used for cluster security</span></span>
    + <span data-ttu-id="325e0-470">Remove-AzureRmServiceFabricNodes 从群集中删除特定节点类型的节点</span><span class="sxs-lookup"><span data-stu-id="325e0-470">Remove-AzureRmServiceFabricNodes       Remove nodes from a specific node type from a cluster</span></span>
    + <span data-ttu-id="325e0-471">Remove-AzureRmServiceFabricNodeType 从群集中删除节点类型</span><span class="sxs-lookup"><span data-stu-id="325e0-471">Remove-AzureRmServiceFabricNodeType       Remove a node type from a cluster</span></span>
    + <span data-ttu-id="325e0-472">Remove-AzureRmServiceFabricSettings 从群集中删除一个或多个 ServiceFabric 设置</span><span class="sxs-lookup"><span data-stu-id="325e0-472">Remove-AzureRmServiceFabricSettings       Remove one or more ServiceFabric settings from a cluster</span></span>
    + <span data-ttu-id="325e0-473">Set-AzureRmServiceFabricSettings 添加或更新群集的一个或多个 ServiceFabric 设置</span><span class="sxs-lookup"><span data-stu-id="325e0-473">Set-AzureRmServiceFabricSettings       Add or update one or more ServiceFabric settings of a cluster</span></span>
    + <span data-ttu-id="325e0-474">Set-AzureRmServiceFabricUpgradeType 更改群集的 ServiceFabric 升级类型</span><span class="sxs-lookup"><span data-stu-id="325e0-474">Set-AzureRmServiceFabricUpgradeType       Change the ServiceFabric upgrade type of a cluster</span></span>
    + <span data-ttu-id="325e0-475">Update-AzureRmServiceFabricDurability 更改群集的持久性层</span><span class="sxs-lookup"><span data-stu-id="325e0-475">Update-AzureRmServiceFabricDurability       Change the durability tier of a cluster</span></span>
    + <span data-ttu-id="325e0-476">Update-AzureRmServiceFabricReliability 更改群集的可靠性层</span><span class="sxs-lookup"><span data-stu-id="325e0-476">Update-AzureRmServiceFabricReliability       Change the reliability tier of a cluster</span></span>
* <span data-ttu-id="325e0-477">Sql</span><span class="sxs-lookup"><span data-stu-id="325e0-477">Sql</span></span>
  - <span data-ttu-id="325e0-478">向 New-AzureRmSqlDatabase 添加了 -SampleName 参数</span><span class="sxs-lookup"><span data-stu-id="325e0-478">Added -SampleName parameter to New-AzureRmSqlDatabase</span></span>
  - <span data-ttu-id="325e0-479">更新了故障转移组 cmdlet</span><span class="sxs-lookup"><span data-stu-id="325e0-479">Updates to Failover Group cmdlets</span></span>
  - <span data-ttu-id="325e0-480">删除“Tag”参数</span><span class="sxs-lookup"><span data-stu-id="325e0-480">Remove 'Tag' parameters</span></span>
  - <span data-ttu-id="325e0-481">从 Remove-AzureRmSqlDatabaseFailoverGroup cmdlet 中删除“PartnerResourceGroupName”和“PartnerServerName”参数</span><span class="sxs-lookup"><span data-stu-id="325e0-481">Remove 'PartnerResourceGroupName' and 'PartnerServerName' parameters from Remove-AzureRmSqlDatabaseFailoverGroup cmdlet</span></span>
  - <span data-ttu-id="325e0-482">向 New-cmdlet 和 Set- cmdlet 添加“GracePeriodWithDataLossHours”参数，此参数最终将取代“GracePeriodWithDataLossHour”</span><span class="sxs-lookup"><span data-stu-id="325e0-482">Add 'GracePeriodWithDataLossHours' parameter to New- and Set- cmdlets, which shall eventually replace 'GracePeriodWithDataLossHour'</span></span>
  - <span data-ttu-id="325e0-483">已完善并更新文档</span><span class="sxs-lookup"><span data-stu-id="325e0-483">Documentation has been fleshed out and updated</span></span>
  - <span data-ttu-id="325e0-484">更改返回对象的格式，并修复一些有关漏填字段的 Bug</span><span class="sxs-lookup"><span data-stu-id="325e0-484">Change formatting of returned objects and fix some bugs where fields were not always populated</span></span>
  - <span data-ttu-id="325e0-485">向故障转移组对象添加“DatabaseNames”和“PartnerLocation”属性</span><span class="sxs-lookup"><span data-stu-id="325e0-485">Add 'DatabaseNames' and 'PartnerLocation' properties to Failover Group object</span></span>
  - <span data-ttu-id="325e0-486">修复导致 Switch- cmdlet 立即返回而不是等待操作完成的 bug</span><span class="sxs-lookup"><span data-stu-id="325e0-486">Fix bug causing Switch- cmdlet to return immediately rather than waiting for operation to complete</span></span>
  - <span data-ttu-id="325e0-487">修复使用高宽限期值时出现的整数溢出 bug</span><span class="sxs-lookup"><span data-stu-id="325e0-487">Fix integer overflow bug when high grace period values are used</span></span>
  - <span data-ttu-id="325e0-488">如果提供的宽限期低于最小值 1 小时，则将其调整为最小值 1 小时</span><span class="sxs-lookup"><span data-stu-id="325e0-488">Adjust grace period to a minimum of 1 hour if a lower one is provided</span></span>
  - <span data-ttu-id="325e0-489">从 Set-AzureRmSqlDatabaseThreatDetectionPolicy cmdlet 和 Set-AzureRmSqlServerThreatDetectionPolicy cmdlet 的“ExcludedDetectionType”参数的接受值中删除“Usage_Anomaly”。</span><span class="sxs-lookup"><span data-stu-id="325e0-489">Remove "Usage_Anomaly" from the accepted values for "ExcludedDetectionType" parameter of Set-AzureRmSqlDatabaseThreatDetectionPolicy cmdlet and Set-AzureRmSqlServerThreatDetectionPolicy cmdlet.</span></span>
* <span data-ttu-id="325e0-490">存储</span><span class="sxs-lookup"><span data-stu-id="325e0-490">Storage</span></span>
  - <span data-ttu-id="325e0-491">将 SRP SDK 升级到 6.3.0</span><span class="sxs-lookup"><span data-stu-id="325e0-491">Upgrade SRP SDK to 6.3.0</span></span>
  - <span data-ttu-id="325e0-492">New/Set-AzureRmStorageAccount：添加新参数，用于支持 EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="325e0-492">New/Set-AzureRmStorageAccount:Add a new parameter to support EnableHttpsTrafficOnly</span></span>
  - <span data-ttu-id="325e0-493">New/Set/Get-AzureRmStorageAccount：返回的存储帐户包含新属性 EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="325e0-493">New/Set/Get-AzureRmStorageAccount: Returned Storage Account contains a new attribute EnableHttpsTrafficOnly</span></span>
* <span data-ttu-id="325e0-494">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="325e0-494">Azure.Storage</span></span>
  - <span data-ttu-id="325e0-495">升级到 Azure 存储客户端库 8.1.1 和 Azure 存储 DataMovement 库 0.5.1</span><span class="sxs-lookup"><span data-stu-id="325e0-495">Upgrade to Azure Storage Client Library 8.1.1 and Azure Storage DataMovement Library 0.5.1</span></span>
  - <span data-ttu-id="325e0-496">添加一个新 cmdlet，用于支持 blob 增量复制功能</span><span class="sxs-lookup"><span data-stu-id="325e0-496">Add a new cmdlet to support blob Incremental Copy feature</span></span>
