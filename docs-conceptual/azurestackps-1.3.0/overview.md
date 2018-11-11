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
ms.openlocfilehash: fb892daeafb1365ea62324392ac806cf9f3d39cf
ms.sourcegitcommit: ac4b53bb42a25aae013a9d8cd9ae98ada9397274
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/08/2018
ms.locfileid: "51274324"
---
# <a name="azure-stack-module-130"></a><span data-ttu-id="84db5-103">Azure Stack 模块 1.3.0</span><span class="sxs-lookup"><span data-stu-id="84db5-103">Azure Stack Module 1.3.0</span></span>

## <a name="requirements"></a><span data-ttu-id="84db5-104">要求：</span><span class="sxs-lookup"><span data-stu-id="84db5-104">Requirements:</span></span>
<span data-ttu-id="84db5-105">Azure Stack 最低支持版本为 1804。</span><span class="sxs-lookup"><span data-stu-id="84db5-105">Minimum supported Azure Stack version is 1804.</span></span>

<span data-ttu-id="84db5-106">注意：如果使用的是早期版本，请安装版本 1.2.11</span><span class="sxs-lookup"><span data-stu-id="84db5-106">Note: If you are using an earlier version install version 1.2.11</span></span>

## <a name="known-issues"></a><span data-ttu-id="84db5-107">已知问题：</span><span class="sxs-lookup"><span data-stu-id="84db5-107">Known issues:</span></span>

- <span data-ttu-id="84db5-108">关闭警报需要 Azure Stack 版本 1803</span><span class="sxs-lookup"><span data-stu-id="84db5-108">Close Alert requires Azure Stack version 1803</span></span>
- <span data-ttu-id="84db5-109">某些存储 cmdlet 需要 Azure Stack 版本 1804</span><span class="sxs-lookup"><span data-stu-id="84db5-109">Some Storage cmdlets do require Azure Stack version 1804</span></span>
- <span data-ttu-id="84db5-110">New-AzsOffer 不允许创建状态为“公共”的产品/服务。</span><span class="sxs-lookup"><span data-stu-id="84db5-110">New-AzsOffer does not allow to create an offer with state public.</span></span> <span data-ttu-id="84db5-111">随后需调用 Set-AzsOffer cmdlet 来更改状态。</span><span class="sxs-lookup"><span data-stu-id="84db5-111">The Set-AzsOffer cmdlet needs to be called afterwards to change the state.</span></span>
- <span data-ttu-id="84db5-112">在不重新部署的情况下，不能删除 IP 池</span><span class="sxs-lookup"><span data-stu-id="84db5-112">An IP Pool cannot be removed without a redeployment</span></span>

## <a name="breaking-changes"></a><span data-ttu-id="84db5-113">重大更改</span><span class="sxs-lookup"><span data-stu-id="84db5-113">Breaking Changes</span></span>
<span data-ttu-id="84db5-114">从 1.2.11 迁移时，所有重大更改记录在此处： https://aka.ms/azspowershellmigration</span><span class="sxs-lookup"><span data-stu-id="84db5-114">All breaking changes migrating from 1.2.11 are documented here https://aka.ms/azspowershellmigration</span></span>

## <a name="install"></a><span data-ttu-id="84db5-115">安装</span><span class="sxs-lookup"><span data-stu-id="84db5-115">Install</span></span>
```
# Remove previous Versions
Uninstall-Module AzureRM.AzureStackAdmin -Force
Uninstall-Module AzureRM.AzureStackStorage -Force
Uninstall-Module -Name AzureStack -Force 


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2017-03-09-profile -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.3.0
```
## <a name="content"></a><span data-ttu-id="84db5-116">内容：</span><span class="sxs-lookup"><span data-stu-id="84db5-116">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="84db5-117">Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="84db5-117">Azure Bridge</span></span>
<span data-ttu-id="84db5-118">Azure Stack AzureBridge 管理员模块的预览版，用于联合 Azure 提供的映像。</span><span class="sxs-lookup"><span data-stu-id="84db5-118">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="84db5-119">备份</span><span class="sxs-lookup"><span data-stu-id="84db5-119">Backup</span></span>
<span data-ttu-id="84db5-120">备份管理员模块的预览版，允许管理员执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="84db5-120">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="84db5-121">配置备份的存储位置</span><span class="sxs-lookup"><span data-stu-id="84db5-121">Configure where backups are stored</span></span>
- <span data-ttu-id="84db5-122">执行备份</span><span class="sxs-lookup"><span data-stu-id="84db5-122">Perform backups</span></span>
- <span data-ttu-id="84db5-123">列出和还原完成的备份</span><span class="sxs-lookup"><span data-stu-id="84db5-123">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="84db5-124">商务</span><span class="sxs-lookup"><span data-stu-id="84db5-124">Commerce</span></span>
<span data-ttu-id="84db5-125">Azure Stack 商务管理员模块的预览版，用于查看整个 Azure Stack 系统的聚合数据使用情况。</span><span class="sxs-lookup"><span data-stu-id="84db5-125">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="84db5-126">计算</span><span class="sxs-lookup"><span data-stu-id="84db5-126">Compute</span></span>
<span data-ttu-id="84db5-127">Azure Stack 计算管理员模块的预览版，其提供的功能用于管理计算配额、平台映像和虚拟机扩展。</span><span class="sxs-lookup"><span data-stu-id="84db5-127">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="84db5-128">Fabric</span><span class="sxs-lookup"><span data-stu-id="84db5-128">Fabric</span></span>
<span data-ttu-id="84db5-129">Azure Stack Fabric 管理员模块的预览版，允许管理员查看和管理基础结构组件：</span><span class="sxs-lookup"><span data-stu-id="84db5-129">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="84db5-130">停止、启动和关闭缩放单元节点</span><span class="sxs-lookup"><span data-stu-id="84db5-130">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="84db5-131">针对 FRU 相关活动清空和恢复缩放单元节点</span><span class="sxs-lookup"><span data-stu-id="84db5-131">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="84db5-132">修复缩放单元节点</span><span class="sxs-lookup"><span data-stu-id="84db5-132">Repair of scale unit nodes</span></span>
- <span data-ttu-id="84db5-133">重启基础结构角色</span><span class="sxs-lookup"><span data-stu-id="84db5-133">Restart of Infrastructure role</span></span>
- <span data-ttu-id="84db5-134">停止、启动和关闭基础结构角色实例</span><span class="sxs-lookup"><span data-stu-id="84db5-134">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="84db5-135">创建新的 IP 池</span><span class="sxs-lookup"><span data-stu-id="84db5-135">Create new IP Pools</span></span>


### <a name="gallery"></a><span data-ttu-id="84db5-136">库</span><span class="sxs-lookup"><span data-stu-id="84db5-136">Gallery</span></span>
<span data-ttu-id="84db5-137">Azure Stack 库管理员模块的预览版，其提供的功能用于管理 Azure Stack 市场中的库项。</span><span class="sxs-lookup"><span data-stu-id="84db5-137">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="84db5-138">基础结构见解</span><span class="sxs-lookup"><span data-stu-id="84db5-138">Infrastructure Insights</span></span>
<span data-ttu-id="84db5-139">基础结构见解管理员模块的预览版，允许管理员执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="84db5-139">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="84db5-140">查看 Azure Stack 戳资源的运行状况</span><span class="sxs-lookup"><span data-stu-id="84db5-140">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="84db5-141">查看和管理警报</span><span class="sxs-lookup"><span data-stu-id="84db5-141">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="84db5-142">KeyVault</span><span class="sxs-lookup"><span data-stu-id="84db5-142">KeyVault</span></span>
<span data-ttu-id="84db5-143">Azure Stack KeyVault 管理员模块的预览版，允许管理员查看 KeyVault 配额。</span><span class="sxs-lookup"><span data-stu-id="84db5-143">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="84db5-144">网络</span><span class="sxs-lookup"><span data-stu-id="84db5-144">Network</span></span>
<span data-ttu-id="84db5-145">网络管理员模块的预览版，用于执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="84db5-145">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="84db5-146">管理网络配额</span><span class="sxs-lookup"><span data-stu-id="84db5-146">Management of network quotas</span></span>
- <span data-ttu-id="84db5-147">查看分配的网络资源，例如公共 IP 地址、虚拟网络、负载均衡器</span><span class="sxs-lookup"><span data-stu-id="84db5-147">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="84db5-148">提供一个显示管理员概览的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="84db5-148">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="84db5-149">存储</span><span class="sxs-lookup"><span data-stu-id="84db5-149">Storage</span></span>
<span data-ttu-id="84db5-150">Azure Stack 存储管理员模块的预览版。</span><span class="sxs-lookup"><span data-stu-id="84db5-150">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="84db5-151">此版本提供以下功能：</span><span class="sxs-lookup"><span data-stu-id="84db5-151">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="84db5-152">管理存储配额</span><span class="sxs-lookup"><span data-stu-id="84db5-152">Manage storage quotas</span></span>
- <span data-ttu-id="84db5-153">回收删除的存储资源</span><span class="sxs-lookup"><span data-stu-id="84db5-153">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="84db5-154">还原删除的存储帐户</span><span class="sxs-lookup"><span data-stu-id="84db5-154">Restore deleted storage accounts</span></span>
- <span data-ttu-id="84db5-155">将容器从一个共享迁移到另一个共享</span><span class="sxs-lookup"><span data-stu-id="84db5-155">Migrate containers from one share to another</span></span>
- <span data-ttu-id="84db5-156">查看单个存储组件的信息</span><span class="sxs-lookup"><span data-stu-id="84db5-156">View information about the individual storage components</span></span>
- <span data-ttu-id="84db5-157">查看使用情况和性能信息</span><span class="sxs-lookup"><span data-stu-id="84db5-157">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="84db5-158">订阅管理员</span><span class="sxs-lookup"><span data-stu-id="84db5-158">Subscription Admin</span></span>
<span data-ttu-id="84db5-159">Azure Stack 订阅管理员模块的预览版。</span><span class="sxs-lookup"><span data-stu-id="84db5-159">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="84db5-160">此模块提供的功能允许管理员执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="84db5-160">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="84db5-161">管理计划和套餐</span><span class="sxs-lookup"><span data-stu-id="84db5-161">Manage plans and offers</span></span>
- <span data-ttu-id="84db5-162">查看使用情况和性能信息</span><span class="sxs-lookup"><span data-stu-id="84db5-162">View usage and performance information</span></span>
- <span data-ttu-id="84db5-163">管理 RBAC</span><span class="sxs-lookup"><span data-stu-id="84db5-163">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="84db5-164">订阅</span><span class="sxs-lookup"><span data-stu-id="84db5-164">Subscription</span></span>
<span data-ttu-id="84db5-165">Azure Stack 订阅模块的预览版。</span><span class="sxs-lookup"><span data-stu-id="84db5-165">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="84db5-166">此模块提供的功能允许用户执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="84db5-166">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="84db5-167">创建、删除和更新订阅</span><span class="sxs-lookup"><span data-stu-id="84db5-167">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="84db5-168">更新</span><span class="sxs-lookup"><span data-stu-id="84db5-168">Update</span></span>
<span data-ttu-id="84db5-169">Azure Stack 更新管理员模块的预览版。</span><span class="sxs-lookup"><span data-stu-id="84db5-169">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="84db5-170">在此模块中，管理员可以执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="84db5-170">In this module administrators can:</span></span>
- <span data-ttu-id="84db5-171">列出和安装可用更新</span><span class="sxs-lookup"><span data-stu-id="84db5-171">List and install available updates</span></span>
- <span data-ttu-id="84db5-172">恢复中断的更新</span><span class="sxs-lookup"><span data-stu-id="84db5-172">Resume interrupted updates</span></span>
- <span data-ttu-id="84db5-173">查看安装的更新</span><span class="sxs-lookup"><span data-stu-id="84db5-173">View installed updates</span></span>
