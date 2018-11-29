---
title: Azure Stack 管理员 PowerShell 概述 | Microsoft Docs
description: 概述 Azure Stack 管理员 PowerShell 并提供安装和配置说明。
author: bganapa
ms.author: bganapa
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 09/21/2018
ms.openlocfilehash: 72d147f5bc9c882083dda6b33b1c89663fd2eb34
ms.sourcegitcommit: 558436c824d9b59731aa9b963cdc8df4dea932e7
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/29/2018
ms.locfileid: "52588241"
---
# <a name="azure-stack-module-140"></a><span data-ttu-id="57a40-103">Azure Stack 模块 1.4.0</span><span class="sxs-lookup"><span data-stu-id="57a40-103">Azure Stack Module 1.4.0</span></span>

## <a name="requirements"></a><span data-ttu-id="57a40-104">要求：</span><span class="sxs-lookup"><span data-stu-id="57a40-104">Requirements:</span></span>
<span data-ttu-id="57a40-105">Azure Stack 最低支持版本为 1804。</span><span class="sxs-lookup"><span data-stu-id="57a40-105">Minimum supported Azure Stack version is 1804.</span></span>

<span data-ttu-id="57a40-106">注意：如果使用的是早期版本，请安装版本 1.2.11</span><span class="sxs-lookup"><span data-stu-id="57a40-106">Note: If you are using an earlier version install version 1.2.11</span></span>

## <a name="known-issues"></a><span data-ttu-id="57a40-107">已知问题：</span><span class="sxs-lookup"><span data-stu-id="57a40-107">Known issues:</span></span>

- <span data-ttu-id="57a40-108">关闭警报需要 Azure Stack 版本 1803</span><span class="sxs-lookup"><span data-stu-id="57a40-108">Close Alert requires Azure Stack version 1803</span></span>
- <span data-ttu-id="57a40-109">New-AzsOffer 不允许创建状态为“公共”的产品/服务。</span><span class="sxs-lookup"><span data-stu-id="57a40-109">New-AzsOffer does not allow to create an offer with state public.</span></span> <span data-ttu-id="57a40-110">随后需调用 Set-AzsOffer cmdlet 来更改状态。</span><span class="sxs-lookup"><span data-stu-id="57a40-110">The Set-AzsOffer cmdlet needs to be called afterwards to change the state.</span></span>
- <span data-ttu-id="57a40-111">在不重新部署的情况下，不能删除 IP 池</span><span class="sxs-lookup"><span data-stu-id="57a40-111">An IP Pool cannot be removed without a redeployment</span></span>

## <a name="breaking-changes"></a><span data-ttu-id="57a40-112">重大更改</span><span class="sxs-lookup"><span data-stu-id="57a40-112">Breaking Changes</span></span>
<span data-ttu-id="57a40-113">自版本 1.3.0 以来没有重大更改。</span><span class="sxs-lookup"><span data-stu-id="57a40-113">There are no breaking changes from the version 1.3.0.</span></span> <span data-ttu-id="57a40-114">从 1.2.11 迁移时，所有重大更改记录在此处： https://aka.ms/azspowershellmigration</span><span class="sxs-lookup"><span data-stu-id="57a40-114">All breaking changes migrating from 1.2.11 are documented here https://aka.ms/azspowershellmigration</span></span>

## <a name="install"></a><span data-ttu-id="57a40-115">安装</span><span class="sxs-lookup"><span data-stu-id="57a40-115">Install</span></span>
```
# Remove previous versions of AzureStack modules
Uninstall-Module -Name AzureStack -Force 
Uninstall-Module AzureRM.AzureStackAdmin -Force
Uninstall-Module AzureRM.AzureStackStorage -Force
Get-Module Azs.* -ListAvailable | Uninstall-Module -Force


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2017-03-09-profile -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.4.0
```
## <a name="release-notes"></a><span data-ttu-id="57a40-116">发行说明</span><span class="sxs-lookup"><span data-stu-id="57a40-116">Release Notes</span></span>
    * <span data-ttu-id="57a40-117">与前一版本 1.3.0 相比，Azurestack 1.4.0 版没有重大更改</span><span class="sxs-lookup"><span data-stu-id="57a40-117">Azurestack 1.4.0 version has no breaking changes from the previous release 1.3.0</span></span>
    * <span data-ttu-id="57a40-118">Azs.AzureBridge.Admin</span><span class="sxs-lookup"><span data-stu-id="57a40-118">Azs.AzureBridge.Admin</span></span>
        - <span data-ttu-id="57a40-119">修复了在分页结果中仅返回单个页面的 bug</span><span class="sxs-lookup"><span data-stu-id="57a40-119">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="57a40-120">Azs.Backup.Admin</span><span class="sxs-lookup"><span data-stu-id="57a40-120">Azs.Backup.Admin</span></span>
        - <span data-ttu-id="57a40-121">在 cmdlet Set-AzsBackupShare 中添加了新参数 BackupFrequencyInHours、IsBackupSchedulerEnabled、BackupRetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="57a40-121">Added new parameters BackupFrequencyInHours, IsBackupSchedulerEnabled, BackupRetentionPeriodInDays in cmdlet Set-AzsBackupShare</span></span>
        - <span data-ttu-id="57a40-122">添加了 cmdlet New-EncyptionKeyBase64 以便于创建加密密钥</span><span class="sxs-lookup"><span data-stu-id="57a40-122">Added a cmdlet New-EncyptionKeyBase64 to facilitate creating encryption key</span></span>
        - <span data-ttu-id="57a40-123">修复了在分页结果中仅返回单个页面的 bug</span><span class="sxs-lookup"><span data-stu-id="57a40-123">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="57a40-124">Azs.Commerce.Admin</span><span class="sxs-lookup"><span data-stu-id="57a40-124">Azs.Commerce.Admin</span></span>
        - <span data-ttu-id="57a40-125">修复了在分页结果中仅返回单个页面的 bug</span><span class="sxs-lookup"><span data-stu-id="57a40-125">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="57a40-126">Azs.Fabric.Admin</span><span class="sxs-lookup"><span data-stu-id="57a40-126">Azs.Fabric.Admin</span></span>
        - <span data-ttu-id="57a40-127">修复了在分页结果中仅返回单个页面的 bug</span><span class="sxs-lookup"><span data-stu-id="57a40-127">Fix for the bug that returned only a single page in paginated results</span></span>
        - <span data-ttu-id="57a40-128">添加了 cmdlet Add-AzsScaleUnitNode 以使管理员可以将新的缩放单元节点添加到 azurestack 戳记</span><span class="sxs-lookup"><span data-stu-id="57a40-128">Added a cmdlet Add-AzsScaleUnitNode to enable admin to add new scale unit nodes to the azurestack stamp</span></span>
        - <span data-ttu-id="57a40-129">添加了 cmdlet 和 New-AzsScaleUnitNodeObject 以便于创建缩放单元参数对象</span><span class="sxs-lookup"><span data-stu-id="57a40-129">Added cmdlet and New-AzsScaleUnitNodeObject to facilitate the creation scale unit parameter objects</span></span>
    * <span data-ttu-id="57a40-130">Azs.Gallery.Admin</span><span class="sxs-lookup"><span data-stu-id="57a40-130">Azs.Gallery.Admin</span></span>
        - <span data-ttu-id="57a40-131">修复了在分页结果中仅返回单个页面的 bug</span><span class="sxs-lookup"><span data-stu-id="57a40-131">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="57a40-132">Azs.InfrastructureInsights.Admin</span><span class="sxs-lookup"><span data-stu-id="57a40-132">Azs.InfrastructureInsights.Admin</span></span>
        - <span data-ttu-id="57a40-133">修复了在分页结果中仅返回单个页面的 bug</span><span class="sxs-lookup"><span data-stu-id="57a40-133">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="57a40-134">Azs.Network.Admin</span><span class="sxs-lookup"><span data-stu-id="57a40-134">Azs.Network.Admin</span></span>
        - <span data-ttu-id="57a40-135">修复了在分页结果中仅返回单个页面的 bug</span><span class="sxs-lookup"><span data-stu-id="57a40-135">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="57a40-136">Azs.Update.Admin</span><span class="sxs-lookup"><span data-stu-id="57a40-136">Azs.Update.Admin</span></span>
        - <span data-ttu-id="57a40-137">修复了在分页结果中仅返回单个页面的 bug</span><span class="sxs-lookup"><span data-stu-id="57a40-137">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="57a40-138">Azs.Subscriptions</span><span class="sxs-lookup"><span data-stu-id="57a40-138">Azs.Subscriptions</span></span>
        - <span data-ttu-id="57a40-139">修复了在分页结果中仅返回单个页面的 bug</span><span class="sxs-lookup"><span data-stu-id="57a40-139">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="57a40-140">Azs.Subscriptions.Admin</span><span class="sxs-lookup"><span data-stu-id="57a40-140">Azs.Subscriptions.Admin</span></span>
        - <span data-ttu-id="57a40-141">添加了 cmdlet Move-AzsSubscription 以便在委托的提供商产品/服务之间移动订阅</span><span class="sxs-lookup"><span data-stu-id="57a40-141">Added a cmdlet Move-AzsSubscription to move subscriptions between delegated provider offers</span></span>
        - <span data-ttu-id="57a40-142">添加了 cmdlet Test-AzsMoveSubscription 以验证用户订阅是否可以在委托的提供商产品/服务之间移动</span><span class="sxs-lookup"><span data-stu-id="57a40-142">Added a cmdlet Test-AzsMoveSubscription to validate that user subscriptions can be moved between delegated provider offers</span></span>
        - <span data-ttu-id="57a40-143">修复了在分页结果中仅返回单个页面的 bug</span><span class="sxs-lookup"><span data-stu-id="57a40-143">Fix for the bug that returned only a single page in paginated results'</span></span>

## <a name="content"></a><span data-ttu-id="57a40-144">内容：</span><span class="sxs-lookup"><span data-stu-id="57a40-144">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="57a40-145">Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="57a40-145">Azure Bridge</span></span>
<span data-ttu-id="57a40-146">Azure Stack AzureBridge 管理员模块的预览版，用于联合 Azure 提供的映像。</span><span class="sxs-lookup"><span data-stu-id="57a40-146">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="57a40-147">备份</span><span class="sxs-lookup"><span data-stu-id="57a40-147">Backup</span></span>
<span data-ttu-id="57a40-148">备份管理员模块的预览版，允许管理员执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="57a40-148">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="57a40-149">配置备份的存储位置</span><span class="sxs-lookup"><span data-stu-id="57a40-149">Configure where backups are stored</span></span>
- <span data-ttu-id="57a40-150">执行备份</span><span class="sxs-lookup"><span data-stu-id="57a40-150">Perform backups</span></span>
- <span data-ttu-id="57a40-151">列出和还原完成的备份</span><span class="sxs-lookup"><span data-stu-id="57a40-151">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="57a40-152">商务</span><span class="sxs-lookup"><span data-stu-id="57a40-152">Commerce</span></span>
<span data-ttu-id="57a40-153">Azure Stack 商务管理员模块的预览版，用于查看整个 Azure Stack 系统的聚合数据使用情况。</span><span class="sxs-lookup"><span data-stu-id="57a40-153">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="57a40-154">计算</span><span class="sxs-lookup"><span data-stu-id="57a40-154">Compute</span></span>
<span data-ttu-id="57a40-155">Azure Stack 计算管理员模块的预览版，其提供的功能用于管理计算配额、平台映像和虚拟机扩展。</span><span class="sxs-lookup"><span data-stu-id="57a40-155">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="57a40-156">Fabric</span><span class="sxs-lookup"><span data-stu-id="57a40-156">Fabric</span></span>
<span data-ttu-id="57a40-157">Azure Stack Fabric 管理员模块的预览版，允许管理员查看和管理基础结构组件：</span><span class="sxs-lookup"><span data-stu-id="57a40-157">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="57a40-158">停止、启动和关闭缩放单元节点</span><span class="sxs-lookup"><span data-stu-id="57a40-158">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="57a40-159">针对 FRU 相关活动清空和恢复缩放单元节点</span><span class="sxs-lookup"><span data-stu-id="57a40-159">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="57a40-160">修复缩放单元节点</span><span class="sxs-lookup"><span data-stu-id="57a40-160">Repair of scale unit nodes</span></span>
- <span data-ttu-id="57a40-161">重启基础结构角色</span><span class="sxs-lookup"><span data-stu-id="57a40-161">Restart of Infrastructure role</span></span>
- <span data-ttu-id="57a40-162">停止、启动和关闭基础结构角色实例</span><span class="sxs-lookup"><span data-stu-id="57a40-162">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="57a40-163">创建新的 IP 池</span><span class="sxs-lookup"><span data-stu-id="57a40-163">Create new IP Pools</span></span>

### <a name="gallery"></a><span data-ttu-id="57a40-164">库</span><span class="sxs-lookup"><span data-stu-id="57a40-164">Gallery</span></span>
<span data-ttu-id="57a40-165">Azure Stack 库管理员模块的预览版，其提供的功能用于管理 Azure Stack 市场中的库项。</span><span class="sxs-lookup"><span data-stu-id="57a40-165">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="57a40-166">基础结构见解</span><span class="sxs-lookup"><span data-stu-id="57a40-166">Infrastructure Insights</span></span>
<span data-ttu-id="57a40-167">基础结构见解管理员模块的预览版，允许管理员执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="57a40-167">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="57a40-168">查看 Azure Stack 戳资源的运行状况</span><span class="sxs-lookup"><span data-stu-id="57a40-168">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="57a40-169">查看和管理警报</span><span class="sxs-lookup"><span data-stu-id="57a40-169">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="57a40-170">KeyVault</span><span class="sxs-lookup"><span data-stu-id="57a40-170">KeyVault</span></span>
<span data-ttu-id="57a40-171">Azure Stack KeyVault 管理员模块的预览版，允许管理员查看 KeyVault 配额。</span><span class="sxs-lookup"><span data-stu-id="57a40-171">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="57a40-172">网络</span><span class="sxs-lookup"><span data-stu-id="57a40-172">Network</span></span>
<span data-ttu-id="57a40-173">网络管理员模块的预览版，用于执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="57a40-173">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="57a40-174">管理网络配额</span><span class="sxs-lookup"><span data-stu-id="57a40-174">Management of network quotas</span></span>
- <span data-ttu-id="57a40-175">查看分配的网络资源，例如公共 IP 地址、虚拟网络、负载均衡器</span><span class="sxs-lookup"><span data-stu-id="57a40-175">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="57a40-176">提供一个显示管理员概览的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="57a40-176">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="57a40-177">存储</span><span class="sxs-lookup"><span data-stu-id="57a40-177">Storage</span></span>
<span data-ttu-id="57a40-178">Azure Stack 存储管理员模块的预览版。</span><span class="sxs-lookup"><span data-stu-id="57a40-178">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="57a40-179">此版本提供以下功能：</span><span class="sxs-lookup"><span data-stu-id="57a40-179">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="57a40-180">管理存储配额</span><span class="sxs-lookup"><span data-stu-id="57a40-180">Manage storage quotas</span></span>
- <span data-ttu-id="57a40-181">回收删除的存储资源</span><span class="sxs-lookup"><span data-stu-id="57a40-181">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="57a40-182">还原删除的存储帐户</span><span class="sxs-lookup"><span data-stu-id="57a40-182">Restore deleted storage accounts</span></span>
- <span data-ttu-id="57a40-183">将容器从一个共享迁移到另一个共享</span><span class="sxs-lookup"><span data-stu-id="57a40-183">Migrate containers from one share to another</span></span>
- <span data-ttu-id="57a40-184">查看单个存储组件的信息</span><span class="sxs-lookup"><span data-stu-id="57a40-184">View information about the individual storage components</span></span>
- <span data-ttu-id="57a40-185">查看使用情况和性能信息</span><span class="sxs-lookup"><span data-stu-id="57a40-185">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="57a40-186">订阅管理员</span><span class="sxs-lookup"><span data-stu-id="57a40-186">Subscription Admin</span></span>
<span data-ttu-id="57a40-187">Azure Stack 订阅管理员模块的预览版。</span><span class="sxs-lookup"><span data-stu-id="57a40-187">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="57a40-188">此模块提供的功能允许管理员执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="57a40-188">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="57a40-189">管理计划和套餐</span><span class="sxs-lookup"><span data-stu-id="57a40-189">Manage plans and offers</span></span>
- <span data-ttu-id="57a40-190">查看使用情况和性能信息</span><span class="sxs-lookup"><span data-stu-id="57a40-190">View usage and performance information</span></span>
- <span data-ttu-id="57a40-191">管理 RBAC</span><span class="sxs-lookup"><span data-stu-id="57a40-191">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="57a40-192">订阅</span><span class="sxs-lookup"><span data-stu-id="57a40-192">Subscription</span></span>
<span data-ttu-id="57a40-193">Azure Stack 订阅模块的预览版。</span><span class="sxs-lookup"><span data-stu-id="57a40-193">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="57a40-194">此模块提供的功能允许用户执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="57a40-194">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="57a40-195">创建、删除和更新订阅</span><span class="sxs-lookup"><span data-stu-id="57a40-195">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="57a40-196">更新</span><span class="sxs-lookup"><span data-stu-id="57a40-196">Update</span></span>
<span data-ttu-id="57a40-197">Azure Stack 更新管理员模块的预览版。</span><span class="sxs-lookup"><span data-stu-id="57a40-197">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="57a40-198">在此模块中，管理员可以执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="57a40-198">In this module administrators can:</span></span>
- <span data-ttu-id="57a40-199">列出和安装可用更新</span><span class="sxs-lookup"><span data-stu-id="57a40-199">List and install available updates</span></span>
- <span data-ttu-id="57a40-200">恢复中断的更新</span><span class="sxs-lookup"><span data-stu-id="57a40-200">Resume interrupted updates</span></span>
- <span data-ttu-id="57a40-201">查看安装的更新</span><span class="sxs-lookup"><span data-stu-id="57a40-201">View installed updates</span></span>
