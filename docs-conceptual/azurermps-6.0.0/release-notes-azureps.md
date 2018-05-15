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
ms.date: 5/1/2018
ms.openlocfilehash: 8515a267e80e5d1f7bb97557efa72b9e86b7b45d
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/08/2018
---
# <a name="release-notes"></a><span data-ttu-id="f5437-103">发行说明</span><span class="sxs-lookup"><span data-stu-id="f5437-103">Release notes</span></span>

<span data-ttu-id="f5437-104">下面是此版本中对 Azure PowerShell 所做的更改列表。</span><span class="sxs-lookup"><span data-stu-id="f5437-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---

## <a name="600---may-2018"></a><span data-ttu-id="f5437-105">6.0.0 - 2018 年 5 月</span><span class="sxs-lookup"><span data-stu-id="f5437-105">6.0.0 - May 2018</span></span>

### <a name="general"></a><span data-ttu-id="f5437-106">常规</span><span class="sxs-lookup"><span data-stu-id="f5437-106">General</span></span>
* <span data-ttu-id="f5437-107">将模块的最低依赖项设置为 PowerShell 5.0</span><span class="sxs-lookup"><span data-stu-id="f5437-107">Set minimum dependency of modules to PowerShell 5.0</span></span>

### <a name="azurestorage"></a><span data-ttu-id="f5437-108">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="f5437-108">Azure.Storage</span></span>
* <span data-ttu-id="f5437-109">支持用作存储 Blob 容器名称</span><span class="sxs-lookup"><span data-stu-id="f5437-109">Support  as Storage blob container name</span></span>
    - <span data-ttu-id="f5437-110">New-AzureStorageBlobContainer</span><span class="sxs-lookup"><span data-stu-id="f5437-110">New-AzureStorageBlobContainer</span></span>
    - <span data-ttu-id="f5437-111">Remove-AzureStorageBlobContainer</span><span class="sxs-lookup"><span data-stu-id="f5437-111">Remove-AzureStorageBlobContainer</span></span>
    - <span data-ttu-id="f5437-112">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="f5437-112">Set-AzureStorageBlobContent</span></span>
    - <span data-ttu-id="f5437-113">Get-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="f5437-113">Get-AzureStorageBlobContent</span></span>
* <span data-ttu-id="f5437-114">修复了某些存储 cmdlet 故障输出不包含详细故障信息的问题</span><span class="sxs-lookup"><span data-stu-id="f5437-114">Fix the issue that some Storage cmdlets failure output not contain detail failure information</span></span>

### <a name="azurermapimanagement"></a><span data-ttu-id="f5437-115">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f5437-115">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="f5437-116">引入多项重大更改</span><span class="sxs-lookup"><span data-stu-id="f5437-116">Introduce multiple breaking changes</span></span>
    - <span data-ttu-id="f5437-117">有关详细信息，请参阅迁移指南</span><span class="sxs-lookup"><span data-stu-id="f5437-117">Please refer to the migration guide for more information</span></span>

### <a name="azurermautomation"></a><span data-ttu-id="f5437-118">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="f5437-118">AzureRM.Automation</span></span>
* <span data-ttu-id="f5437-119">从 cmdlet 中删除已弃用的“Tags”别名</span><span class="sxs-lookup"><span data-stu-id="f5437-119">Remove deprecated 'Tags' alias from cmdlets</span></span>
    - <span data-ttu-id="f5437-120">'Set-AzureRmAutomationRunbook'</span><span class="sxs-lookup"><span data-stu-id="f5437-120">'Set-AzureRmAutomationRunbook'</span></span>

### <a name="azurermbatch"></a><span data-ttu-id="f5437-121">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="f5437-121">AzureRM.Batch</span></span>
* <span data-ttu-id="f5437-122">更新了 New-AzureBatchPool 文档，删除了已弃用的示例</span><span class="sxs-lookup"><span data-stu-id="f5437-122">Updated New-AzureBatchPool documentation to remove deprecated example</span></span>

### <a name="azurermcdn"></a><span data-ttu-id="f5437-123">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="f5437-123">AzureRM.Cdn</span></span>
* <span data-ttu-id="f5437-124">引入多项重大更改</span><span class="sxs-lookup"><span data-stu-id="f5437-124">Introduce multiple breaking changes</span></span>
    - <span data-ttu-id="f5437-125">有关详细信息，请参阅迁移指南</span><span class="sxs-lookup"><span data-stu-id="f5437-125">Please refer to the migration guide for more information</span></span>

### <a name="azurermcompute"></a><span data-ttu-id="f5437-126">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="f5437-126">AzureRM.Compute</span></span>
* <span data-ttu-id="f5437-127">“New-AzureRmVm”和“New-AzureRmVmss”支持参数的详细输出。</span><span class="sxs-lookup"><span data-stu-id="f5437-127">'New-AzureRmVm' and 'New-AzureRmVmss' support verbose output of parameters</span></span>
* <span data-ttu-id="f5437-128">“New-AzureRmVm”和“New-AzureRmVmss”（简单参数集）支持向 VM 分配用户定义的和（或）系统定义的标识。</span><span class="sxs-lookup"><span data-stu-id="f5437-128">'New-AzureRmVm' and 'New-AzureRmVmss' (simple parameter set) support assigning user defined and(or) system defined identities to the VM(s).</span></span>
* <span data-ttu-id="f5437-129">VMSS Redeploy 和 PerformMaintenance 功能</span><span class="sxs-lookup"><span data-stu-id="f5437-129">VMSS Redeploy and PerformMaintenance feature</span></span>
    -  <span data-ttu-id="f5437-130">向“Set-AzureRmVmss”和“Set-AzureRmVmssVM”添加新的开关参数 -Redeploy 和 -PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="f5437-130">Add new switch parameter -Redeploy and -PerformMaintenance to 'Set-AzureRmVmss' and 'Set-AzureRmVmssVM'</span></span>
* <span data-ttu-id="f5437-131">向“Set-AzureRmVMOperatingSystem”cmdlet 添加 DisableVMAgent 开关参数</span><span class="sxs-lookup"><span data-stu-id="f5437-131">Add DisableVMAgent switch parameter to 'Set-AzureRmVMOperatingSystem' cmdlet</span></span>
* <span data-ttu-id="f5437-132">“New-AzureRmVm”和“New-AzureRmVmss”（简单参数集）支持“Win10”映像。</span><span class="sxs-lookup"><span data-stu-id="f5437-132">'New-AzureRmVm' and 'New-AzureRmVmss' (simple parameter set) support a 'Win10' image.</span></span>
* <span data-ttu-id="f5437-133">添加了“Repair-AzureRmVmssServiceFabricUpdateDomain”cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f5437-133">'Repair-AzureRmVmssServiceFabricUpdateDomain' cmdlet is added.</span></span>
* <span data-ttu-id="f5437-134">引入多项重大更改</span><span class="sxs-lookup"><span data-stu-id="f5437-134">Introduce multiple breaking changes</span></span>
    - <span data-ttu-id="f5437-135">如需更多详细信息，请参阅迁移指南</span><span class="sxs-lookup"><span data-stu-id="f5437-135">Please refer to the migration guide for more details</span></span>
* <span data-ttu-id="f5437-136">“Set-AzureRmVmDiskEncryptionExtension”使 AAD 参数变为可选</span><span class="sxs-lookup"><span data-stu-id="f5437-136">'Set-AzureRmVmDiskEncryptionExtension' makes AAD parameters optional</span></span>

### <a name="azurermdatafactories"></a><span data-ttu-id="f5437-137">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="f5437-137">AzureRM.DataFactories</span></span>
* <span data-ttu-id="f5437-138">从 cmdlet 中删除已弃用的“Tags”别名</span><span class="sxs-lookup"><span data-stu-id="f5437-138">Remove deprecated 'Tags' alias from cmdlets</span></span>
    - <span data-ttu-id="f5437-139">New-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="f5437-139">New-AzureRmDataFactory</span></span>

### <a name="azurermdatafactoryv2"></a><span data-ttu-id="f5437-140">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="f5437-140">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="f5437-141">将 ADF.Net SDK 版本更新到了 0.7.0-preview，其中包含以下更改：</span><span class="sxs-lookup"><span data-stu-id="f5437-141">Updated the ADF .Net SDK version to 0.7.0-preview containing following changes:</span></span>
    - <span data-ttu-id="f5437-142">在 ExecuteSSISPackage 活动上添加了执行参数和连接管理器属性</span><span class="sxs-lookup"><span data-stu-id="f5437-142">Added execution parameters and connection managers property on ExecuteSSISPackage Activity</span></span>
    - <span data-ttu-id="f5437-143">更新了 PostgreSql 和 MySql 链接服务，使用完整的连接字符串而不是服务器、数据库、架构、用户名和密码</span><span class="sxs-lookup"><span data-stu-id="f5437-143">Updated PostgreSql, MySql llinked service to use full connection string instead of server, database, schema, username and password</span></span>
    - <span data-ttu-id="f5437-144">从 DB2 链接服务中删除了架构</span><span class="sxs-lookup"><span data-stu-id="f5437-144">Removed the schema from DB2 linked service</span></span>
    - <span data-ttu-id="f5437-145">从 Teradata 链接服务中删除了架构属性</span><span class="sxs-lookup"><span data-stu-id="f5437-145">Removed schema property from Teradata linked service</span></span>
    - <span data-ttu-id="f5437-146">为 Responsys 添加了 LinkedService、Dataset、CopySource</span><span class="sxs-lookup"><span data-stu-id="f5437-146">Added LinkedService, Dataset, CopySource for Responsys</span></span>

### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="f5437-147">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="f5437-147">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="f5437-148">从 cmdlet 中删除已弃用的“Tags”别名</span><span class="sxs-lookup"><span data-stu-id="f5437-148">Remove deprecated 'Tags' alias from cmdlets</span></span>
    - <span data-ttu-id="f5437-149">'New-AzureRmDataLakeAnalyticsAccount'</span><span class="sxs-lookup"><span data-stu-id="f5437-149">'New-AzureRmDataLakeAnalyticsAccount'</span></span>
    - <span data-ttu-id="f5437-150">'Set-AzureRmDataLakeAnalyticsAccount'</span><span class="sxs-lookup"><span data-stu-id="f5437-150">'Set-AzureRmDataLakeAnalyticsAccount'</span></span>

### <a name="azurermdatalakestore"></a><span data-ttu-id="f5437-151">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f5437-151">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="f5437-152">向 Remove-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAcl 添加递归 Acl 更改这一新功能</span><span class="sxs-lookup"><span data-stu-id="f5437-152">Add new feature of recursive Acl Change to Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="f5437-153">添加用于在目录下检索内容摘要的新 cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5437-153">Add new cmdlet for retrieving the content summary under a directory</span></span>
* <span data-ttu-id="f5437-154">添加用于检索磁盘使用情况和 Acl 转储的新 cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5437-154">Add new cmdlet for retrieving the disk usage and Acl dump</span></span>
* <span data-ttu-id="f5437-155">将返回类型 Set-AzureRmDataLakeStoreItemAcl bool 更正为 IEnumerable<DataLakeStoreItemAce></span><span class="sxs-lookup"><span data-stu-id="f5437-155">Correct return type of Set-AzureRmDataLakeStoreItemAcl bool to IEnumerable<DataLakeStoreItemAce></span></span>
* <span data-ttu-id="f5437-156">将返回类型 Set-AzureRmDataLakeStoreItemAclEntry bool 更正为 IEnumerable<DataLakeStoreItemAce></span><span class="sxs-lookup"><span data-stu-id="f5437-156">Correct return type of Set-AzureRmDataLakeStoreItemAclEntry bool to IEnumerable<DataLakeStoreItemAce></span></span>
* <span data-ttu-id="f5437-157">Export-AzureRmDataLakeStoreItem、Import-AzureRmDataLakeStoreItem、Remove-AzureRmDataLakeStoreItem 中的重大更改</span><span class="sxs-lookup"><span data-stu-id="f5437-157">Breaking changes in Export-AzureRmDataLakeStoreItem, Import-AzureRmDataLakeStoreItem, Remove-AzureRmDataLakeStoreItem</span></span>

### <a name="azurermdns"></a><span data-ttu-id="f5437-158">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="f5437-158">AzureRM.Dns</span></span>
* <span data-ttu-id="f5437-159">引入多项重大更改</span><span class="sxs-lookup"><span data-stu-id="f5437-159">Introduce multiple breaking changes</span></span>
    - <span data-ttu-id="f5437-160">有关详细信息，请参阅迁移指南</span><span class="sxs-lookup"><span data-stu-id="f5437-160">Please refer to the migration guide for more information</span></span>

### <a name="azurermeventhub"></a><span data-ttu-id="f5437-161">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="f5437-161">AzureRM.EventHub</span></span>
* <span data-ttu-id="f5437-162">更新了 cmdlet 的帮助文档，增加了缺失的示例</span><span class="sxs-lookup"><span data-stu-id="f5437-162">Updated Help for cmdlets with missing examples</span></span>

### <a name="azurerminsights"></a><span data-ttu-id="f5437-163">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="f5437-163">AzureRM.Insights</span></span>
* <span data-ttu-id="f5437-164">引入了多项重大更改</span><span class="sxs-lookup"><span data-stu-id="f5437-164">Introduced multiple breaking changes</span></span>
    - <span data-ttu-id="f5437-165">有关详细信息，请参阅迁移指南</span><span class="sxs-lookup"><span data-stu-id="f5437-165">Please refer to the migration guide for more information</span></span>

### <a name="azurermiothub"></a><span data-ttu-id="f5437-166">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="f5437-166">AzureRM.IotHub</span></span>
* <span data-ttu-id="f5437-167">启用 IotHub 的标记和基本 SKU</span><span class="sxs-lookup"><span data-stu-id="f5437-167">Enable tags and Basic Sku to the IotHub</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="f5437-168">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f5437-168">AzureRM.KeyVault</span></span>
* <span data-ttu-id="f5437-169">管道方案支持方面的重大更改</span><span class="sxs-lookup"><span data-stu-id="f5437-169">Breaking changes to support piping scenarios</span></span>
* <span data-ttu-id="f5437-170">添加了新 cmdlet：Backup/Restore-AzureKeyVaultManagedStorageAccount、Backup/Restore-AzureKeyVaultCertificate、Undo-AzureKeyVaultManagedStorageSasDefinitionRemoval、Undo-AzureKeyVaultManagedStorageAccountRemoval</span><span class="sxs-lookup"><span data-stu-id="f5437-170">Added new cmdlets: Backup/Restore-AzureKeyVaultManagedStorageAccount, Backup/Restore-AzureKeyVaultCertificate, Undo-AzureKeyVaultManagedStorageSasDefinitionRemoval, and Undo-AzureKeyVaultManagedStorageAccountRemoval</span></span>

### <a name="azurermmachinelearning"></a><span data-ttu-id="f5437-171">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="f5437-171">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="f5437-172">从 cmdlet 中删除已弃用的“Tags”别名</span><span class="sxs-lookup"><span data-stu-id="f5437-172">Remove deprecated 'Tags' alias from cmdlets</span></span>
    - <span data-ttu-id="f5437-173">Update-AzureRmMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="f5437-173">Update-AzureRmMlCommitmentPlan</span></span>

### <a name="azurermmedia"></a><span data-ttu-id="f5437-174">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="f5437-174">AzureRM.Media</span></span>
* <span data-ttu-id="f5437-175">从 cmdlet 中删除已弃用的“Tags”别名</span><span class="sxs-lookup"><span data-stu-id="f5437-175">Remove deprecated 'Tags' alias from cmdlets</span></span>
    - <span data-ttu-id="f5437-176">'Set-AzureRmMediaService'</span><span class="sxs-lookup"><span data-stu-id="f5437-176">'Set-AzureRmMediaService'</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="f5437-177">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="f5437-177">AzureRM.Network</span></span>
* <span data-ttu-id="f5437-178">增加对 DDoS 防护计划资源的支持</span><span class="sxs-lookup"><span data-stu-id="f5437-178">Add support for DDoS protection plan resource</span></span>
* <span data-ttu-id="f5437-179">引入了多项重大更改</span><span class="sxs-lookup"><span data-stu-id="f5437-179">Introduced multiple breaking changes</span></span>
    - <span data-ttu-id="f5437-180">有关详细信息，请参阅迁移指南</span><span class="sxs-lookup"><span data-stu-id="f5437-180">Please refer to the migration guide for more information</span></span>

### <a name="azurermnotificationhubs"></a><span data-ttu-id="f5437-181">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="f5437-181">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="f5437-182">引入多项重大更改</span><span class="sxs-lookup"><span data-stu-id="f5437-182">Introduce multiple breaking changes</span></span>
    - <span data-ttu-id="f5437-183">有关详细信息，请参阅迁移指南</span><span class="sxs-lookup"><span data-stu-id="f5437-183">Please refer to the migration guide for more information</span></span>

### <a name="azurermoperationalinsights"></a><span data-ttu-id="f5437-184">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f5437-184">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="f5437-185">引入多项重大更改</span><span class="sxs-lookup"><span data-stu-id="f5437-185">Introduce multiple breaking changes</span></span>
    - <span data-ttu-id="f5437-186">有关详细信息，请参阅迁移指南</span><span class="sxs-lookup"><span data-stu-id="f5437-186">Please refer to the migration guide for more information</span></span>

### <a name="azurermprofile"></a><span data-ttu-id="f5437-187">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="f5437-187">AzureRM.Profile</span></span>
* <span data-ttu-id="f5437-188">默认启用上下文自动保存功能</span><span class="sxs-lookup"><span data-stu-id="f5437-188">Enable context autosave by default</span></span>
* <span data-ttu-id="f5437-189">向 Azure 环境美国政府版添加 USGovernmentOperationalInsightsEndpoint 和 USGovernmentOperationalInsightsEndpointResourceId 属性。</span><span class="sxs-lookup"><span data-stu-id="f5437-189">Add USGovernmentOperationalInsightsEndpoint and USGovernmentOperationalInsightsEndpointResourceId properties to Azure environment for US Gov.</span></span>

### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="f5437-190">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="f5437-190">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="f5437-191">修复了 SiteRecovery 方案中的身份验证标头</span><span class="sxs-lookup"><span data-stu-id="f5437-191">Fixed Authentication Header in SiteRecovery scenarios</span></span>

### <a name="azurermrediscache"></a><span data-ttu-id="f5437-192">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="f5437-192">AzureRM.RedisCache</span></span>
* <span data-ttu-id="f5437-193">引入了多项重大更改</span><span class="sxs-lookup"><span data-stu-id="f5437-193">Introduced multiple breaking changes</span></span>
    - <span data-ttu-id="f5437-194">有关详细信息，请参阅迁移指南</span><span class="sxs-lookup"><span data-stu-id="f5437-194">Please refer to the migration guide for more information</span></span>

### <a name="azurermresources"></a><span data-ttu-id="f5437-195">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="f5437-195">AzureRM.Resources</span></span>
* <span data-ttu-id="f5437-196">从 Get-AzureRmRoledefinition 调用中删除过时的参数 -AtScopeAndBelow</span><span class="sxs-lookup"><span data-stu-id="f5437-196">Remove obsolete parameter -AtScopeAndBelow from Get-AzureRmRoledefinition call</span></span>
* <span data-ttu-id="f5437-197">在 Get-AzureRmRoleAssignment 结果中包括针对已删除的 USers/Groups/ServicePrincipals 的分配</span><span class="sxs-lookup"><span data-stu-id="f5437-197">Include assignments to deleted USers/Groups/ServicePrincipals in Get-AzureRmRoleAssignment result</span></span>
* <span data-ttu-id="f5437-198">为 Scope 和 ResourceType 添加了 Tab 补全选项</span><span class="sxs-lookup"><span data-stu-id="f5437-198">Add Tab completers for Scope and ResourceType</span></span>
* <span data-ttu-id="f5437-199">添加用于创建 ServicePrincipals 的便捷 cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5437-199">Add convenience cmdlet for creating ServicePrincipals</span></span>
* <span data-ttu-id="f5437-200">在 Get-AzureRmResource 中合并 Get- 和 Find- 功能</span><span class="sxs-lookup"><span data-stu-id="f5437-200">Merge Get- and Find- functionality in Get-AzureRmResource</span></span>
* <span data-ttu-id="f5437-201">添加 AD Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="f5437-201">Add AD Cmdlets:</span></span>
  - <span data-ttu-id="f5437-202">Remove-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="f5437-202">Remove-AzureRmADGroupMember</span></span>
  - <span data-ttu-id="f5437-203">Get-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="f5437-203">Get-AzureRmADGroup</span></span>
  - <span data-ttu-id="f5437-204">New-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="f5437-204">New-AzureRmADGroup</span></span>
  - <span data-ttu-id="f5437-205">Remove-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="f5437-205">Remove-AzureRmADGroup</span></span>
  - <span data-ttu-id="f5437-206">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="f5437-206">Remove-AzureRmADUser</span></span>
  - <span data-ttu-id="f5437-207">Update-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="f5437-207">Update-AzureRmADApplication</span></span>
  - <span data-ttu-id="f5437-208">Update-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="f5437-208">Update-AzureRmADServicePrincipal</span></span>
  - <span data-ttu-id="f5437-209">Update-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="f5437-209">Update-AzureRmADUser</span></span>

### <a name="azurermservicefabric"></a><span data-ttu-id="f5437-210">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f5437-210">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="f5437-211">更新默认的 Linux 映像版本 SKU</span><span class="sxs-lookup"><span data-stu-id="f5437-211">Update default Linux image version sku</span></span>
  - <span data-ttu-id="f5437-212">NewAzureServiceFabricCluster.cs 默认 UbuntuServer1604 SKU 更新</span><span class="sxs-lookup"><span data-stu-id="f5437-212">NewAzureServiceFabricCluster.cs default UbuntuServer1604 Sku update</span></span>

### <a name="azurermstorage"></a><span data-ttu-id="f5437-213">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="f5437-213">AzureRM.Storage</span></span>
* <span data-ttu-id="f5437-214">引入了多项重大更改</span><span class="sxs-lookup"><span data-stu-id="f5437-214">Introduced multiple breaking changes</span></span>
    - <span data-ttu-id="f5437-215">有关详细信息，请参阅迁移指南</span><span class="sxs-lookup"><span data-stu-id="f5437-215">Please refer to the migration guide for more information</span></span>

### <a name="azurermwebsites"></a><span data-ttu-id="f5437-216">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="f5437-216">AzureRM.Websites</span></span>
* <span data-ttu-id="f5437-217">升级到最新版本的网站 SDK</span><span class="sxs-lookup"><span data-stu-id="f5437-217">Upgrade to latest version of the Websites SDK</span></span>
* <span data-ttu-id="f5437-218">为 Set-AzureRmWebApp 和 Set-AzureRmWebAppSlot 增加了 -AssignIdentity 和 -Httpsonly 属性</span><span class="sxs-lookup"><span data-stu-id="f5437-218">Added -AssignIdentity & -Httpsonly properties for Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
* <span data-ttu-id="f5437-219">增加了两个新的 cmdlet：Get-AzureRmWebAppSnapshots 和 Restore-AzureRmWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="f5437-219">Added two new cmdlets: Get-AzureRmWebAppSnapshots and Restore-AzureRmWebAppSnapshot</span></span>
