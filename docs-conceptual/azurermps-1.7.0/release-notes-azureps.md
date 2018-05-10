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
ms.date: 05/18/2017
ms.openlocfilehash: 0a3f152751fee569d3ac5fba6bcff8c1737f7b8c
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/08/2018
---
# <a name="release-notes"></a><span data-ttu-id="91f8f-103">发行说明</span><span class="sxs-lookup"><span data-stu-id="91f8f-103">Release notes</span></span>

<span data-ttu-id="91f8f-104">下面是此版本中对 Azure PowerShell 所做的更改列表。</span><span class="sxs-lookup"><span data-stu-id="91f8f-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

## <a name="version-170"></a><span data-ttu-id="91f8f-105">版本 1.7.0</span><span class="sxs-lookup"><span data-stu-id="91f8f-105">Version 1.7.0</span></span>

* <span data-ttu-id="91f8f-106">**所有 cmdlet 的 -Force、–Confirm 和 $ConfirmPreference 参数的行为更改。我们正在根据 PowerShell 准则更改此实现。对于大多数 cmdlet，这意味着删除 Force 参数，并且若要跳过 ShouldProcess 提示，用户需要在其 PowerShell 脚本中包含“-Confirm:$false”参数。**</span><span class="sxs-lookup"><span data-stu-id="91f8f-106">**Behavioral change for -Force, –Confirm and $ConfirmPreference parameters for all cmdlets. We are changing this implementation to be in line with PowerShell guidelines. For most cmdlets, this means removing the Force parameter and to skip the ShouldProcess prompt, users will need to include the parameter: ‘-Confirm:$false’ in their PowerShell scripts.**</span></span> <span data-ttu-id="91f8f-107">此更改将解决以下问题：</span><span class="sxs-lookup"><span data-stu-id="91f8f-107">This changes are addressing following issues:</span></span>
  - <span data-ttu-id="91f8f-108">正确实现 -WhatIf 功能，允许用户确定 cmdlet 或脚本的影响，而无需进行任何实际更改</span><span class="sxs-lookup"><span data-stu-id="91f8f-108">Correct implementation of –WhatIf functionality, allowing a user to determine the effects of a cmdlet or script without making any actual changes</span></span>
  - <span data-ttu-id="91f8f-109">使用会话范围的 $ConfirmPreference 控制提示，以便根据预期更改的影响（在 cmdlet 的 ConfirmImpact 设置中报告）提示用户</span><span class="sxs-lookup"><span data-stu-id="91f8f-109">Control over prompting using a session-wide $ConfirmPreference, so that the user is prompted based on the impact of a prospective change (as reported in the ConfirmImpact setting in the cmdlet)</span></span>
  - <span data-ttu-id="91f8f-110">使用 –Confirm 参数对确认提示进行 Cmdlet 特定的控制</span><span class="sxs-lookup"><span data-stu-id="91f8f-110">Cmdlet-specific control over confirmation prompts using the –Confirm parameter</span></span>
  - <span data-ttu-id="91f8f-111">在各个 cmdlet 之间一致使用 ShouldContinue 和 –Force 参数，仅针对由于更改的特殊性质（例如，删除隐藏的文件）而需要用户提示的操作</span><span class="sxs-lookup"><span data-stu-id="91f8f-111">Consistent use of ShouldContinue and the –Force parameter across cmdlets, for only those actions that would require prompting from the user due to the special nature of the changes (for example, deleting hidden files)</span></span>
  - <span data-ttu-id="91f8f-112">与其他 PowerShell cmdlet 保持一致，使其他 cmdlet 的 PowerShell 脚本知识可立即适用于 Azure PowerShell cmdlet。</span><span class="sxs-lookup"><span data-stu-id="91f8f-112">Consistency with other PowerShell cmdlets, so that PowerShell scripting knowledge from other cmdlets is immediately applicable to the Azure PowerShell cmdlets.</span></span>

<span data-ttu-id="91f8f-113">**请注意，现在为了*在所有情况下跳过所有提示*，Azure PowerShell cmdlet 要求用户提供两个参数：**</span><span class="sxs-lookup"><span data-stu-id="91f8f-113">**Notice that now to *automatically skip all Prompts in all Circumstances* Azure PowerShell cmdlets require the user to supply two parameters:**</span></span>
```powershell
My-CmdletWithConfirmation –Confirm:$false -Force
```
* <span data-ttu-id="91f8f-114">Azure 计算</span><span class="sxs-lookup"><span data-stu-id="91f8f-114">Azure Compute</span></span>
  - <span data-ttu-id="91f8f-115">Set-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="91f8f-115">Set-AzureRmVMADDomainExtension</span></span>
  - <span data-ttu-id="91f8f-116">Get-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="91f8f-116">Get-AzureRmVMADDomainExtension</span></span>
  - <span data-ttu-id="91f8f-117">Restart-AzureVM 的 -Redeploy 参数</span><span class="sxs-lookup"><span data-stu-id="91f8f-117">-Redeploy parameter for Restart-AzureVM</span></span>
  - <span data-ttu-id="91f8f-118">Move-AzureService、Move-AzureStorageAccount 和 Move-AzureVirtualNetwork 的 -Validate 参数</span><span class="sxs-lookup"><span data-stu-id="91f8f-118">-Validate parameter for Move-AzureService, Move-AzureStorageAccount, and Move-AzureVirtualNetwork</span></span>
  - <span data-ttu-id="91f8f-119">像以前一样，扩展 cmdlet 的名称和版本参数是可选的。</span><span class="sxs-lookup"><span data-stu-id="91f8f-119">Name and version parameters for extension cmdlets are optional as before.</span></span>
  - <span data-ttu-id="91f8f-120">New-AzureVM 可从 VM 对象中获取许可证类型。</span><span class="sxs-lookup"><span data-stu-id="91f8f-120">New-AzureVM can get a license type from VM object.</span></span>
* <span data-ttu-id="91f8f-121">Azure 存储</span><span class="sxs-lookup"><span data-stu-id="91f8f-121">Azure Storage</span></span>
  - <span data-ttu-id="91f8f-122">将 Tags 参数更改为 Tag，并添加了参数别名 Tags</span><span class="sxs-lookup"><span data-stu-id="91f8f-122">Change Tags Parameter to Tag, and add parameter alias Tags</span></span>
    + <span data-ttu-id="91f8f-123">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="91f8f-123">New-AzureRmStorageAccount</span></span>
    + <span data-ttu-id="91f8f-124">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="91f8f-124">Set-AzureRmStorageAccount</span></span>
* <span data-ttu-id="91f8f-125">Azure 网络</span><span class="sxs-lookup"><span data-stu-id="91f8f-125">Azure Network</span></span>
  - <span data-ttu-id="91f8f-126">为虚拟网络对等互连添加了新的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="91f8f-126">New cmdlet added for Virtual Network Peering</span></span>
* <span data-ttu-id="91f8f-127">Azure Redis Cache</span><span class="sxs-lookup"><span data-stu-id="91f8f-127">Azure Redis Cache</span></span>
  - <span data-ttu-id="91f8f-128">为 Reset-AzureRmRedisCache 添加了新的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="91f8f-128">New cmdlet added for Reset-AzureRmRedisCache</span></span>
  - <span data-ttu-id="91f8f-129">为 Export-AzureRmRedisCache 添加了新的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="91f8f-129">New cmdlet added for Export-AzureRmRedisCache</span></span>
  - <span data-ttu-id="91f8f-130">为 Import-AzureRmRedisCache 添加了新的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="91f8f-130">New cmdlet added for Import-AzureRmRedisCache</span></span>
  - <span data-ttu-id="91f8f-131">修改了 cmdlet New-AzureRmRedisCache，在其中包含了 vNet 的参数更改</span><span class="sxs-lookup"><span data-stu-id="91f8f-131">Modified cmdlet New-AzureRmRedisCache to include parameter change for vNet</span></span>
* <span data-ttu-id="91f8f-132">Azure SQL 数据库备份/还原</span><span class="sxs-lookup"><span data-stu-id="91f8f-132">Azure SQL DB Backup/Restore</span></span>
  - <span data-ttu-id="91f8f-133">LTR（长期保留）备份功能的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="91f8f-133">Cmdlets for LTR (Long Term Retention) backup feature</span></span>
  - <span data-ttu-id="91f8f-134">Get-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="91f8f-134">Get-AzureRmSqlServerBackupLongTermRetentionVault</span></span>
  - <span data-ttu-id="91f8f-135">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="91f8f-135">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>
  - <span data-ttu-id="91f8f-136">Set-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="91f8f-136">Set-AzureRmSqlServerBackupLongTermRetentionVault</span></span>
  - <span data-ttu-id="91f8f-137">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="91f8f-137">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>
  - <span data-ttu-id="91f8f-138">Restore-AzureRmSqlDatabase 现在支持已删除的数据库的时间点还原</span><span class="sxs-lookup"><span data-stu-id="91f8f-138">Restore-AzureRmSqlDatabase now supports point-in-time restore of a deleted database</span></span>
  - <span data-ttu-id="91f8f-139">Restore-AzureRmSqlDatabase 现在支持从长期保留备份中还原</span><span class="sxs-lookup"><span data-stu-id="91f8f-139">Restore-AzureRmSqlDatabase now supports restoring from a Long Term Retention backup</span></span>
* <span data-ttu-id="91f8f-140">Azure 逻辑应用</span><span class="sxs-lookup"><span data-stu-id="91f8f-140">Azure LogicApp</span></span>
  - <span data-ttu-id="91f8f-141">添加了逻辑应用集成帐户 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="91f8f-141">Added LogicApp Integration accounts cmdlets.</span></span>
  - <span data-ttu-id="91f8f-142">Get-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="91f8f-142">Get-AzureRmIntegrationAccountAgreement</span></span>
  - <span data-ttu-id="91f8f-143">Get-AzureRmIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="91f8f-143">Get-AzureRmIntegrationAccountCallbackUrl</span></span>
  - <span data-ttu-id="91f8f-144">Get-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="91f8f-144">Get-AzureRmIntegrationAccountCertificate</span></span>
  - <span data-ttu-id="91f8f-145">Get-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="91f8f-145">Get-AzureRmIntegrationAccount</span></span>
  - <span data-ttu-id="91f8f-146">Get-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="91f8f-146">Get-AzureRmIntegrationAccountMap</span></span>
  - <span data-ttu-id="91f8f-147">Get-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="91f8f-147">Get-AzureRmIntegrationAccountPartner</span></span>
  - <span data-ttu-id="91f8f-148">Get-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="91f8f-148">Get-AzureRmIntegrationAccountSchema</span></span>
  - <span data-ttu-id="91f8f-149">New-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="91f8f-149">New-AzureRmIntegrationAccountAgreement</span></span>
  - <span data-ttu-id="91f8f-150">New-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="91f8f-150">New-AzureRmIntegrationAccountCertificate</span></span>
  - <span data-ttu-id="91f8f-151">New-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="91f8f-151">New-AzureRmIntegrationAccount</span></span>
  - <span data-ttu-id="91f8f-152">New-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="91f8f-152">New-AzureRmIntegrationAccountMap</span></span>
  - <span data-ttu-id="91f8f-153">New-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="91f8f-153">New-AzureRmIntegrationAccountPartner</span></span>
  - <span data-ttu-id="91f8f-154">New-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="91f8f-154">New-AzureRmIntegrationAccountSchema</span></span>
  - <span data-ttu-id="91f8f-155">Remove-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="91f8f-155">Remove-AzureRmIntegrationAccountAgreement</span></span>
  - <span data-ttu-id="91f8f-156">Remove-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="91f8f-156">Remove-AzureRmIntegrationAccountCertificate</span></span>
  - <span data-ttu-id="91f8f-157">Remove-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="91f8f-157">Remove-AzureRmIntegrationAccount</span></span>
  - <span data-ttu-id="91f8f-158">Remove-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="91f8f-158">Remove-AzureRmIntegrationAccountMap</span></span>
  - <span data-ttu-id="91f8f-159">Remove-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="91f8f-159">Remove-AzureRmIntegrationAccountPartner</span></span>
  - <span data-ttu-id="91f8f-160">Remove-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="91f8f-160">Remove-AzureRmIntegrationAccountSchema</span></span>
  - <span data-ttu-id="91f8f-161">Set-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="91f8f-161">Set-AzureRmIntegrationAccountAgreement</span></span>
  - <span data-ttu-id="91f8f-162">Set-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="91f8f-162">Set-AzureRmIntegrationAccountCertificate</span></span>
  - <span data-ttu-id="91f8f-163">Set-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="91f8f-163">Set-AzureRmIntegrationAccount</span></span>
  - <span data-ttu-id="91f8f-164">Set-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="91f8f-164">Set-AzureRmIntegrationAccountMap</span></span>
  - <span data-ttu-id="91f8f-165">Set-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="91f8f-165">Set-AzureRmIntegrationAccountPartner</span></span>
  - <span data-ttu-id="91f8f-166">Set-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="91f8f-166">Set-AzureRmIntegrationAccountSchema</span></span>
* <span data-ttu-id="91f8f-167">Azure Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="91f8f-167">Azure Data Lake Store</span></span>
  - <span data-ttu-id="91f8f-168">大幅提高了文件和文件夹上传与下载的性能。</span><span class="sxs-lookup"><span data-stu-id="91f8f-168">Drastically improve performance of file and folder upload and download.</span></span>
  - <span data-ttu-id="91f8f-169">这包括对用于下载的参数名称的轻微更改，并包含用于上传的两个新参数：</span><span class="sxs-lookup"><span data-stu-id="91f8f-169">This includes a slight change to the parameter names for download and inclusion of two new parameters for upload:</span></span>
    + <span data-ttu-id="91f8f-170">NumThreads -> PerFileThreadCount，用于指示要在单个文件中使用的线程数</span><span class="sxs-lookup"><span data-stu-id="91f8f-170">NumThreads -> PerFileThreadCount, used to indicate the number of threads to use in a single file</span></span>
    + <span data-ttu-id="91f8f-171">ConcurrentFileCount，用于指示上传/下载文件夹的过程中同时上传/下载的文件数。</span><span class="sxs-lookup"><span data-stu-id="91f8f-171">ConcurrentFileCount, used to indicate the number of files to upload/download in parallel for folder upload/download.</span></span>
  - <span data-ttu-id="91f8f-172">默认线程值现已设计为针对大多数文件大小全面改善吞吐量。</span><span class="sxs-lookup"><span data-stu-id="91f8f-172">Default threading values are now designed to give a better all around throughput for most file sizes.</span></span> <span data-ttu-id="91f8f-173">如果性能不符合要求，可以修改上述值来满足要求。</span><span class="sxs-lookup"><span data-stu-id="91f8f-173">If performance is not as desired, the values above can be modified to meet requirements.</span></span>
* <span data-ttu-id="91f8f-174">Azure Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="91f8f-174">Azure Data Lake Analytics</span></span>
  - <span data-ttu-id="91f8f-175">在不结合任何参数调用的情况下，Get-AzureRMDataLakeAnalyticsDataSource 现在返回所有数据源。</span><span class="sxs-lookup"><span data-stu-id="91f8f-175">Get-AzureRMDataLakeAnalyticsDataSource now returns all data sources when called with no arguments.</span></span>
  - <span data-ttu-id="91f8f-176">此更改还从 cmdlet 中删除了数据源类型参数。</span><span class="sxs-lookup"><span data-stu-id="91f8f-176">This change also removes the data source type parameter from the cmdlet.</span></span>
  - <span data-ttu-id="91f8f-177">此更改导致针对列表操作返回包含以下属性的新对象：</span><span class="sxs-lookup"><span data-stu-id="91f8f-177">This change results in a new object being returned for the list operation with the following properties:</span></span>
    + <span data-ttu-id="91f8f-178">Type：数据源的类型</span><span class="sxs-lookup"><span data-stu-id="91f8f-178">Type, the type of data source</span></span>
    + <span data-ttu-id="91f8f-179">Name：数据源的名称</span><span class="sxs-lookup"><span data-stu-id="91f8f-179">Name, the name of the data source</span></span>
    + <span data-ttu-id="91f8f-180">IsDefault：如果这是帐户的默认数据源，则设置为 true</span><span class="sxs-lookup"><span data-stu-id="91f8f-180">IsDefault, set to true if this is the default data source for the account</span></span>
  - <span data-ttu-id="91f8f-181">Get-AzureRMDataLakeAnalyticsJob 已修复。根据 submittedBefore 和 submittedAfter 筛选时，可以正常返回某些日期时间偏移值的列表。</span><span class="sxs-lookup"><span data-stu-id="91f8f-181">Get-AzureRMDataLakeAnalyticsJob fixed for list for certain date time offset values when filtering on submittedBefore and submittedAfter.</span></span>
* <span data-ttu-id="91f8f-182">Web 应用</span><span class="sxs-lookup"><span data-stu-id="91f8f-182">Web Apps</span></span>
  - <span data-ttu-id="91f8f-183">为常规交换和包含预览的交换添加了 Swap-AzureRmWebAppSlot cmdlet</span><span class="sxs-lookup"><span data-stu-id="91f8f-183">Add Swap-AzureRmWebAppSlot cmdlet for regular swap and swap with preview</span></span>
  - <span data-ttu-id="91f8f-184">扩展了 AzureRmWebAppSlot cmdlet 以支持自动交换</span><span class="sxs-lookup"><span data-stu-id="91f8f-184">Extend Set-AzureRmWebAppSlot cmdlet to support auto swap</span></span>
* <span data-ttu-id="91f8f-185">Azure API 管理</span><span class="sxs-lookup"><span data-stu-id="91f8f-185">Azure API Management</span></span>
  - <span data-ttu-id="91f8f-186">修复了 AzureChinaCloud 的 Azure API 管理部署 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="91f8f-186">Fixed Azure Api Management Deployment cmdlets for AzureChinaCloud.</span></span>
  - <span data-ttu-id="91f8f-187">删除了 cmdlet Set-AzureRmApiManagementTenantGitAccess，因为 Git 访问默认已启用。</span><span class="sxs-lookup"><span data-stu-id="91f8f-187">Removed cmdlet Set-AzureRmApiManagementTenantGitAccess as Git Access is enabled by Default.</span></span>
* <span data-ttu-id="91f8f-188">Azure 恢复服务备份</span><span class="sxs-lookup"><span data-stu-id="91f8f-188">Azure Recovery Services Backup</span></span>
  - <span data-ttu-id="91f8f-189">添加了对 Azure SQL 工作负荷的支持</span><span class="sxs-lookup"><span data-stu-id="91f8f-189">Added support for the Azure SQL workload</span></span>
  - <span data-ttu-id="91f8f-190">添加了对备份和还原已加密 Azure VM 的支持</span><span class="sxs-lookup"><span data-stu-id="91f8f-190">Added support for backing up and restoring encrypted Azure VMs</span></span>
  - <span data-ttu-id="91f8f-191">Backup-AzureRmRecoveryServicesBackupItem - 为恢复点添加了可选的保留时间功能</span><span class="sxs-lookup"><span data-stu-id="91f8f-191">Backup-AzureRmRecoveryServicesBackupItem - Added optional retention time feature for recovery points</span></span>
  - <span data-ttu-id="91f8f-192">在 Get-AzureRmRecoveryServicesBackupContainer 和 Get-AzureRmRecoveryServicesBackupItem cmdlet 中进行了轻微的筛选器相关 bug 修复</span><span class="sxs-lookup"><span data-stu-id="91f8f-192">Minor filter-related bug fixes in Get-AzureRmRecoveryServicesBackupContainer and Get-AzureRmRecoveryServicesBackupItem cmdlets</span></span>
* <span data-ttu-id="91f8f-193">Azure 自动化</span><span class="sxs-lookup"><span data-stu-id="91f8f-193">Azure Automation</span></span>
  - <span data-ttu-id="91f8f-194">添加了 Get-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="91f8f-194">Added Get-AzureRmAutomationHybridWorkerGroup</span></span>
