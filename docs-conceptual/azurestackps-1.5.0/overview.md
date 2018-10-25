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
ms.openlocfilehash: 18861f0e5232e0b505767aa9609099afe88f9477
ms.sourcegitcommit: 5f946a535eccca0b3ddf3db8f617b32564a88938
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/25/2018
ms.locfileid: "50001807"
---
# <a name="azure-stack-module-150"></a><span data-ttu-id="3fa1a-103">Azure Stack 模块 1.5.0</span><span class="sxs-lookup"><span data-stu-id="3fa1a-103">Azure Stack Module 1.5.0</span></span>

## <a name="requirements"></a><span data-ttu-id="3fa1a-104">要求：</span><span class="sxs-lookup"><span data-stu-id="3fa1a-104">Requirements:</span></span>
<span data-ttu-id="3fa1a-105">Azure Stack 最低支持版本为 1808。</span><span class="sxs-lookup"><span data-stu-id="3fa1a-105">Minimum supported Azure Stack version is 1808.</span></span>

<span data-ttu-id="3fa1a-106">注意：如果使用的是早期版本，请安装版本 1.4.0</span><span class="sxs-lookup"><span data-stu-id="3fa1a-106">Note: If you are using an earlier version install version 1.4.0</span></span>

## <a name="known-issues"></a><span data-ttu-id="3fa1a-107">已知问题：</span><span class="sxs-lookup"><span data-stu-id="3fa1a-107">Known issues:</span></span>

- <span data-ttu-id="3fa1a-108">New-AzsOffer 不允许创建状态为“公共”的产品/服务。</span><span class="sxs-lookup"><span data-stu-id="3fa1a-108">New-AzsOffer does not allow to create an offer with state public.</span></span> <span data-ttu-id="3fa1a-109">随后需调用 Set-AzsOffer cmdlet 来更改状态。</span><span class="sxs-lookup"><span data-stu-id="3fa1a-109">The Set-AzsOffer cmdlet needs to be called afterwards to change the state.</span></span>
- <span data-ttu-id="3fa1a-110">在不重新部署的情况下，不能删除 IP 池</span><span class="sxs-lookup"><span data-stu-id="3fa1a-110">An IP Pool cannot be removed without a redeployment</span></span>

## <a name="install"></a><span data-ttu-id="3fa1a-111">安装</span><span class="sxs-lookup"><span data-stu-id="3fa1a-111">Install</span></span>
```
# Remove previous versions of AzureStack modules
Uninstall-Module -Name AzureStack -Force 
Uninstall-Module AzureRM.AzureStackAdmin -Force
Uninstall-Module AzureRM.AzureStackStorage -Force
Get-Module Azs.* -ListAvailable | Uninstall-Module -Force


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2018-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.5.0
```

##<a name="release-notes"></a><span data-ttu-id="3fa1a-112">发行说明</span><span class="sxs-lookup"><span data-stu-id="3fa1a-112">Release Notes</span></span>
* <span data-ttu-id="3fa1a-113">所有 Azure Stack 管理员模块都会进行更新，使其版本高于或等于 AzureRm.Profile 模块依赖项</span><span class="sxs-lookup"><span data-stu-id="3fa1a-113">All the Azure Stack Admin modules are updated for greater than or equal to dependency on the AzureRm.Profile module</span></span>
* <span data-ttu-id="3fa1a-114">支持处理所有模块中的嵌套资源名称</span><span class="sxs-lookup"><span data-stu-id="3fa1a-114">Support for handling nested resource names in all the modules</span></span>
* <span data-ttu-id="3fa1a-115">修复了 ErrorActionPreference 被重写为 Stop 的所有模块中的 Bug</span><span class="sxs-lookup"><span data-stu-id="3fa1a-115">Bug fix in all the modules where ErrorActionPreference is being overridden to be Stop</span></span>
* <span data-ttu-id="3fa1a-116">Azs.Compute.Admin 模块</span><span class="sxs-lookup"><span data-stu-id="3fa1a-116">Azs.Compute.Admin Module</span></span>
    * <span data-ttu-id="3fa1a-117">增加了新的支持托管磁盘的配额属性</span><span class="sxs-lookup"><span data-stu-id="3fa1a-117">New quota properties added for the support of manged disk</span></span>
    * <span data-ttu-id="3fa1a-118">增加了与磁盘迁移相关的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="3fa1a-118">Addition of disk migration related cmdlets</span></span>
    * <span data-ttu-id="3fa1a-119">在平台映像和 VM 扩展对象中增加了属性</span><span class="sxs-lookup"><span data-stu-id="3fa1a-119">Additional properties in the Platform Image and VM extesnion objects</span></span>
* <span data-ttu-id="3fa1a-120">Azs.Fabric.Admin</span><span class="sxs-lookup"><span data-stu-id="3fa1a-120">Azs.Fabric.Admin</span></span> 
    * <span data-ttu-id="3fa1a-121">新增了用于添加缩放单元节点的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="3fa1a-121">New cmdlet for adding scale unit node</span></span>
* <span data-ttu-id="3fa1a-122">Azs.Backup.Admin</span><span class="sxs-lookup"><span data-stu-id="3fa1a-122">Azs.Backup.Admin</span></span>
    * <span data-ttu-id="3fa1a-123">现在，Set-AzsBackupShare 是 cmdlet Set-AzsBackupConfiguration 的别名</span><span class="sxs-lookup"><span data-stu-id="3fa1a-123">Set-AzsBackupShare is an alias now to the cmdlet Set-AzsBackupConfiguration</span></span>
    * <span data-ttu-id="3fa1a-124">现在，Get-AzsBackupLocation 是 cmdlet Get-AzsBackupConfiguration 的别名</span><span class="sxs-lookup"><span data-stu-id="3fa1a-124">Get-AzsBackupLocation is an alias now to the cmdlet Get-AzsBackupConfiguration</span></span>
    * <span data-ttu-id="3fa1a-125">现在，Set-AzsBackupConfiguration（参数 BackupShare）是参数 path 的别名</span><span class="sxs-lookup"><span data-stu-id="3fa1a-125">Set-AzsBackupConfiguration, the parameter BackupShare is an alias now for the parameter path</span></span>
* <span data-ttu-id="3fa1a-126">Azs.Subscriptions</span><span class="sxs-lookup"><span data-stu-id="3fa1a-126">Azs.Subscriptions</span></span>
    * <span data-ttu-id="3fa1a-127">现在，Get-AzsDelegatedProviderOffer（参数 OfferName）是 Offer 的别名</span><span class="sxs-lookup"><span data-stu-id="3fa1a-127">Get-AzsDelegatedProviderOffer, the parameter OfferName is now an alias for Offer</span></span>
* <span data-ttu-id="3fa1a-128">Azs.Subscriptions.Admin</span><span class="sxs-lookup"><span data-stu-id="3fa1a-128">Azs.Subscriptions.Admin</span></span>
    * <span data-ttu-id="3fa1a-129">现在，Get-AzsDelegatedProviderOffer（参数 OfferName）是 Offer 的别名</span><span class="sxs-lookup"><span data-stu-id="3fa1a-129">Get-AzsDelegatedProviderOffer, the parameter OfferName is now an alias for Offer</span></span>

## <a name="content"></a><span data-ttu-id="3fa1a-130">内容：</span><span class="sxs-lookup"><span data-stu-id="3fa1a-130">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="3fa1a-131">Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="3fa1a-131">Azure Bridge</span></span>
<span data-ttu-id="3fa1a-132">Azure Stack AzureBridge 管理员模块的预览版，用于联合 Azure 提供的映像。</span><span class="sxs-lookup"><span data-stu-id="3fa1a-132">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="3fa1a-133">备份</span><span class="sxs-lookup"><span data-stu-id="3fa1a-133">Backup</span></span>
<span data-ttu-id="3fa1a-134">备份管理员模块的预览版，允许管理员执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="3fa1a-134">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="3fa1a-135">配置备份的存储位置</span><span class="sxs-lookup"><span data-stu-id="3fa1a-135">Configure where backups are stored</span></span>
- <span data-ttu-id="3fa1a-136">执行备份</span><span class="sxs-lookup"><span data-stu-id="3fa1a-136">Perform backups</span></span>
- <span data-ttu-id="3fa1a-137">列出和还原完成的备份</span><span class="sxs-lookup"><span data-stu-id="3fa1a-137">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="3fa1a-138">商务</span><span class="sxs-lookup"><span data-stu-id="3fa1a-138">Commerce</span></span>
<span data-ttu-id="3fa1a-139">Azure Stack 商务管理员模块的预览版，用于查看整个 Azure Stack 系统的聚合数据使用情况。</span><span class="sxs-lookup"><span data-stu-id="3fa1a-139">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="3fa1a-140">计算</span><span class="sxs-lookup"><span data-stu-id="3fa1a-140">Compute</span></span>
<span data-ttu-id="3fa1a-141">Azure Stack 计算管理员模块的预览版，其提供的功能用于管理计算配额、平台映像、托管磁盘和虚拟机扩展。</span><span class="sxs-lookup"><span data-stu-id="3fa1a-141">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, managed disks and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="3fa1a-142">Fabric</span><span class="sxs-lookup"><span data-stu-id="3fa1a-142">Fabric</span></span>
<span data-ttu-id="3fa1a-143">Azure Stack Fabric 管理员模块的预览版，允许管理员查看和管理基础结构组件：</span><span class="sxs-lookup"><span data-stu-id="3fa1a-143">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="3fa1a-144">停止、启动和关闭缩放单元节点</span><span class="sxs-lookup"><span data-stu-id="3fa1a-144">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="3fa1a-145">针对 FRU 相关活动清空和恢复缩放单元节点</span><span class="sxs-lookup"><span data-stu-id="3fa1a-145">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="3fa1a-146">修复缩放单元节点</span><span class="sxs-lookup"><span data-stu-id="3fa1a-146">Repair of scale unit nodes</span></span>
- <span data-ttu-id="3fa1a-147">重启基础结构角色</span><span class="sxs-lookup"><span data-stu-id="3fa1a-147">Restart of Infrastructure role</span></span>
- <span data-ttu-id="3fa1a-148">停止、启动和关闭基础结构角色实例</span><span class="sxs-lookup"><span data-stu-id="3fa1a-148">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="3fa1a-149">创建新的 IP 池</span><span class="sxs-lookup"><span data-stu-id="3fa1a-149">Create new IP Pools</span></span>


### <a name="gallery"></a><span data-ttu-id="3fa1a-150">库</span><span class="sxs-lookup"><span data-stu-id="3fa1a-150">Gallery</span></span>
<span data-ttu-id="3fa1a-151">Azure Stack 库管理员模块的预览版，其提供的功能用于管理 Azure Stack 市场中的库项。</span><span class="sxs-lookup"><span data-stu-id="3fa1a-151">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="3fa1a-152">基础结构见解</span><span class="sxs-lookup"><span data-stu-id="3fa1a-152">Infrastructure Insights</span></span>
<span data-ttu-id="3fa1a-153">基础结构见解管理员模块的预览版，允许管理员执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="3fa1a-153">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="3fa1a-154">查看 Azure Stack 戳资源的运行状况</span><span class="sxs-lookup"><span data-stu-id="3fa1a-154">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="3fa1a-155">查看和管理警报</span><span class="sxs-lookup"><span data-stu-id="3fa1a-155">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="3fa1a-156">KeyVault</span><span class="sxs-lookup"><span data-stu-id="3fa1a-156">KeyVault</span></span>
<span data-ttu-id="3fa1a-157">Azure Stack KeyVault 管理员模块的预览版，允许管理员查看 KeyVault 配额。</span><span class="sxs-lookup"><span data-stu-id="3fa1a-157">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="3fa1a-158">网络</span><span class="sxs-lookup"><span data-stu-id="3fa1a-158">Network</span></span>
<span data-ttu-id="3fa1a-159">网络管理员模块的预览版，用于执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="3fa1a-159">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="3fa1a-160">管理网络配额</span><span class="sxs-lookup"><span data-stu-id="3fa1a-160">Management of network quotas</span></span>
- <span data-ttu-id="3fa1a-161">查看分配的网络资源，例如公共 IP 地址、虚拟网络、负载均衡器</span><span class="sxs-lookup"><span data-stu-id="3fa1a-161">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="3fa1a-162">提供一个显示管理员概览的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="3fa1a-162">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="3fa1a-163">存储</span><span class="sxs-lookup"><span data-stu-id="3fa1a-163">Storage</span></span>
<span data-ttu-id="3fa1a-164">Azure Stack 存储管理员模块的预览版。</span><span class="sxs-lookup"><span data-stu-id="3fa1a-164">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="3fa1a-165">此版本提供以下功能：</span><span class="sxs-lookup"><span data-stu-id="3fa1a-165">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="3fa1a-166">管理存储配额</span><span class="sxs-lookup"><span data-stu-id="3fa1a-166">Manage storage quotas</span></span>
- <span data-ttu-id="3fa1a-167">回收删除的存储资源</span><span class="sxs-lookup"><span data-stu-id="3fa1a-167">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="3fa1a-168">还原删除的存储帐户</span><span class="sxs-lookup"><span data-stu-id="3fa1a-168">Restore deleted storage accounts</span></span>
- <span data-ttu-id="3fa1a-169">将容器从一个共享迁移到另一个共享</span><span class="sxs-lookup"><span data-stu-id="3fa1a-169">Migrate containers from one share to another</span></span>
- <span data-ttu-id="3fa1a-170">查看单个存储组件的信息</span><span class="sxs-lookup"><span data-stu-id="3fa1a-170">View information about the individual storage components</span></span>
- <span data-ttu-id="3fa1a-171">查看使用情况和性能信息</span><span class="sxs-lookup"><span data-stu-id="3fa1a-171">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="3fa1a-172">订阅管理员</span><span class="sxs-lookup"><span data-stu-id="3fa1a-172">Subscription Admin</span></span>
<span data-ttu-id="3fa1a-173">Azure Stack 订阅管理员模块的预览版。</span><span class="sxs-lookup"><span data-stu-id="3fa1a-173">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="3fa1a-174">此模块提供的功能允许管理员执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="3fa1a-174">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="3fa1a-175">管理计划和套餐</span><span class="sxs-lookup"><span data-stu-id="3fa1a-175">Manage plans and offers</span></span>
- <span data-ttu-id="3fa1a-176">查看使用情况和性能信息</span><span class="sxs-lookup"><span data-stu-id="3fa1a-176">View usage and performance information</span></span>
- <span data-ttu-id="3fa1a-177">管理 RBAC</span><span class="sxs-lookup"><span data-stu-id="3fa1a-177">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="3fa1a-178">订阅</span><span class="sxs-lookup"><span data-stu-id="3fa1a-178">Subscription</span></span>
<span data-ttu-id="3fa1a-179">Azure Stack 订阅模块的预览版。</span><span class="sxs-lookup"><span data-stu-id="3fa1a-179">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="3fa1a-180">此模块提供的功能允许用户执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="3fa1a-180">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="3fa1a-181">创建、删除和更新订阅</span><span class="sxs-lookup"><span data-stu-id="3fa1a-181">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="3fa1a-182">更新</span><span class="sxs-lookup"><span data-stu-id="3fa1a-182">Update</span></span>
<span data-ttu-id="3fa1a-183">Azure Stack 更新管理员模块的预览版。</span><span class="sxs-lookup"><span data-stu-id="3fa1a-183">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="3fa1a-184">在此模块中，管理员可以执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="3fa1a-184">In this module administrators can:</span></span>
- <span data-ttu-id="3fa1a-185">列出和安装可用更新</span><span class="sxs-lookup"><span data-stu-id="3fa1a-185">List and install available updates</span></span>
- <span data-ttu-id="3fa1a-186">恢复中断的更新</span><span class="sxs-lookup"><span data-stu-id="3fa1a-186">Resume interrupted updates</span></span>
- <span data-ttu-id="3fa1a-187">查看安装的更新</span><span class="sxs-lookup"><span data-stu-id="3fa1a-187">View installed updates</span></span>
