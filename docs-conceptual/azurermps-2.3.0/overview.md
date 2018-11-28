---
title: Azure Stack PowerShell 概述 | Microsoft Docs
description: 概述 Azure Stack PowerShell 并提供安装和配置说明。
author: bganapa
ms.author: bganapa
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 09/21/2018
ms.openlocfilehash: cd415e862bfaa2b767cce108689ebaf34ef74305
ms.sourcegitcommit: 80a3da199954d0ab78765715fb49793e89a30f12
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/22/2018
ms.locfileid: "52259176"
---
# <a name="azurerm-module-230"></a><span data-ttu-id="99edd-103">AzureRM 模块 2.3.0</span><span class="sxs-lookup"><span data-stu-id="99edd-103">AzureRM Module 2.3.0</span></span>

## <a name="requirements"></a><span data-ttu-id="99edd-104">要求：</span><span class="sxs-lookup"><span data-stu-id="99edd-104">Requirements:</span></span>
<span data-ttu-id="99edd-105">Azure Stack 最低支持版本为 1808。</span><span class="sxs-lookup"><span data-stu-id="99edd-105">Minimum supported Azure Stack version is 1808.</span></span>

<span data-ttu-id="99edd-106">注意：如果使用的是早期版本，请安装版本 1.2.11</span><span class="sxs-lookup"><span data-stu-id="99edd-106">Note: If you are using an earlier version install version 1.2.11</span></span>


## <a name="install"></a><span data-ttu-id="99edd-107">安装</span><span class="sxs-lookup"><span data-stu-id="99edd-107">Install</span></span>
```powershell-interactive
# Remove previous versions of AzureStack modules
Uninstall-Module -Name AzureStack -Force 
Uninstall-Module -Name AzureRM -Force 
Uninstall-Module AzureRM.AzureStackAdmin -Force -ErrorAction Continue
Uninstall-Module AzureRM.AzureStackStorage -Force -ErrorAction Continue
Get-Module Azs.* -ListAvailable | Uninstall-Module -Force
Get-Module Azure.* -ListAvailable | Uninstall-Module -Force


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2018-03-01-hybrid -Force

```

## <a name="release-notes"></a><span data-ttu-id="99edd-108">发行说明</span><span class="sxs-lookup"><span data-stu-id="99edd-108">Release Notes</span></span>
* <span data-ttu-id="99edd-109">发行版 2.3.0 附带一系列重大变更。</span><span class="sxs-lookup"><span data-stu-id="99edd-109">The release 2.3.0 comes with a list of breaking changes.</span></span> <span data-ttu-id="99edd-110">若要从 1.2.11 版升级，请使用我们在 https://aka.ms/azspowershellmigration 创建的迁移指南</span><span class="sxs-lookup"><span data-stu-id="99edd-110">To upgrade from the 1.2.11 version, we have created a migration guide at https://aka.ms/azspowershellmigration</span></span>
* <span data-ttu-id="99edd-111">此发行版对应于特定于 azurestack 的 API 配置文件 2018-03-01-hybrid</span><span class="sxs-lookup"><span data-stu-id="99edd-111">This release corresponds to the azurestack specific api profile 2018-03-01-hybrid</span></span>
* <span data-ttu-id="99edd-112">所有模块都会采用高于或等于 AzureRm.Profile 模块依赖项的版本。</span><span class="sxs-lookup"><span data-stu-id="99edd-112">All the modules are taking greater than or equal to dependency on the AzureRm.Profile module.</span></span>
* <span data-ttu-id="99edd-113">每个模块支持的 API 版本都会更新。</span><span class="sxs-lookup"><span data-stu-id="99edd-113">Api version suppoerted by  each of the modules are updated.</span></span> 
    * <span data-ttu-id="99edd-114">计算 - 2017-03-30</span><span class="sxs-lookup"><span data-stu-id="99edd-114">Compute - 2017-03-30</span></span>
    * <span data-ttu-id="99edd-115">网络 - 2017-10-01</span><span class="sxs-lookup"><span data-stu-id="99edd-115">Network - 2017-10-01</span></span>
    * <span data-ttu-id="99edd-116">存储 - 2016-01-01</span><span class="sxs-lookup"><span data-stu-id="99edd-116">Storage - 2016-01-01</span></span>
    * <span data-ttu-id="99edd-117">资源 - 2018-02-01</span><span class="sxs-lookup"><span data-stu-id="99edd-117">Resources - 2018-02-01</span></span>
    * <span data-ttu-id="99edd-118">Keyvault - 2016-10-01</span><span class="sxs-lookup"><span data-stu-id="99edd-118">Keyvault - 2016-10-01</span></span>
    * <span data-ttu-id="99edd-119">Dns - 2016-04-01</span><span class="sxs-lookup"><span data-stu-id="99edd-119">Dns - 2016-04-01</span></span>
* <span data-ttu-id="99edd-120">[https://github.com/Azure/azure-rest-api-specs/blob/master/profile/2018-03-01-hybrid.json](https://github.com/Azure/azure-rest-api-specs/blob/master/profile/2018-03-01-hybrid.json)  提供每个资源类型的完整 API 版本映射</span><span class="sxs-lookup"><span data-stu-id="99edd-120">The complete api version map for each of the resource types can be found at https://github.com/Azure/azure-rest-api-specs/blob/master/profile/2018-03-01-hybrid.json</span></span>

## <a name="content"></a><span data-ttu-id="99edd-121">内容：</span><span class="sxs-lookup"><span data-stu-id="99edd-121">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="99edd-122">Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="99edd-122">Azure Bridge</span></span>
<span data-ttu-id="99edd-123">Azure Stack AzureBridge 管理员模块的预览版，用于联合 Azure 提供的映像。</span><span class="sxs-lookup"><span data-stu-id="99edd-123">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="99edd-124">备份</span><span class="sxs-lookup"><span data-stu-id="99edd-124">Backup</span></span>
<span data-ttu-id="99edd-125">备份管理员模块的预览版，允许管理员执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="99edd-125">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="99edd-126">配置备份的存储位置</span><span class="sxs-lookup"><span data-stu-id="99edd-126">Configure where backups are stored</span></span>
- <span data-ttu-id="99edd-127">执行备份</span><span class="sxs-lookup"><span data-stu-id="99edd-127">Perform backups</span></span>
- <span data-ttu-id="99edd-128">列出和还原完成的备份</span><span class="sxs-lookup"><span data-stu-id="99edd-128">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="99edd-129">商务</span><span class="sxs-lookup"><span data-stu-id="99edd-129">Commerce</span></span>
<span data-ttu-id="99edd-130">Azure Stack 商务管理员模块的预览版，用于查看整个 Azure Stack 系统的聚合数据使用情况。</span><span class="sxs-lookup"><span data-stu-id="99edd-130">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="99edd-131">计算</span><span class="sxs-lookup"><span data-stu-id="99edd-131">Compute</span></span>
<span data-ttu-id="99edd-132">Azure Stack 计算管理员模块的预览版，其提供的功能用于管理计算配额、平台映像、托管磁盘和虚拟机扩展。</span><span class="sxs-lookup"><span data-stu-id="99edd-132">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, managed disks and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="99edd-133">Fabric</span><span class="sxs-lookup"><span data-stu-id="99edd-133">Fabric</span></span>
<span data-ttu-id="99edd-134">Azure Stack Fabric 管理员模块的预览版，允许管理员查看和管理基础结构组件：</span><span class="sxs-lookup"><span data-stu-id="99edd-134">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="99edd-135">停止、启动和关闭缩放单元节点</span><span class="sxs-lookup"><span data-stu-id="99edd-135">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="99edd-136">针对 FRU 相关活动清空和恢复缩放单元节点</span><span class="sxs-lookup"><span data-stu-id="99edd-136">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="99edd-137">修复缩放单元节点</span><span class="sxs-lookup"><span data-stu-id="99edd-137">Repair of scale unit nodes</span></span>
- <span data-ttu-id="99edd-138">重启基础结构角色</span><span class="sxs-lookup"><span data-stu-id="99edd-138">Restart of Infrastructure role</span></span>
- <span data-ttu-id="99edd-139">停止、启动和关闭基础结构角色实例</span><span class="sxs-lookup"><span data-stu-id="99edd-139">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="99edd-140">创建新的 IP 池</span><span class="sxs-lookup"><span data-stu-id="99edd-140">Create new IP Pools</span></span>


### <a name="gallery"></a><span data-ttu-id="99edd-141">库</span><span class="sxs-lookup"><span data-stu-id="99edd-141">Gallery</span></span>
<span data-ttu-id="99edd-142">Azure Stack 库管理员模块的预览版，其提供的功能用于管理 Azure Stack 市场中的库项。</span><span class="sxs-lookup"><span data-stu-id="99edd-142">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="99edd-143">基础结构见解</span><span class="sxs-lookup"><span data-stu-id="99edd-143">Infrastructure Insights</span></span>
<span data-ttu-id="99edd-144">基础结构见解管理员模块的预览版，允许管理员执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="99edd-144">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="99edd-145">查看 Azure Stack 戳资源的运行状况</span><span class="sxs-lookup"><span data-stu-id="99edd-145">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="99edd-146">查看和管理警报</span><span class="sxs-lookup"><span data-stu-id="99edd-146">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="99edd-147">KeyVault</span><span class="sxs-lookup"><span data-stu-id="99edd-147">KeyVault</span></span>
<span data-ttu-id="99edd-148">Azure Stack KeyVault 管理员模块的预览版，允许管理员查看 KeyVault 配额。</span><span class="sxs-lookup"><span data-stu-id="99edd-148">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="99edd-149">网络</span><span class="sxs-lookup"><span data-stu-id="99edd-149">Network</span></span>
<span data-ttu-id="99edd-150">网络管理员模块的预览版，用于执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="99edd-150">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="99edd-151">管理网络配额</span><span class="sxs-lookup"><span data-stu-id="99edd-151">Management of network quotas</span></span>
- <span data-ttu-id="99edd-152">查看分配的网络资源，例如公共 IP 地址、虚拟网络、负载均衡器</span><span class="sxs-lookup"><span data-stu-id="99edd-152">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="99edd-153">提供一个显示管理员概览的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="99edd-153">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="99edd-154">存储</span><span class="sxs-lookup"><span data-stu-id="99edd-154">Storage</span></span>
<span data-ttu-id="99edd-155">Azure Stack 存储管理员模块的预览版。</span><span class="sxs-lookup"><span data-stu-id="99edd-155">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="99edd-156">此版本提供以下功能：</span><span class="sxs-lookup"><span data-stu-id="99edd-156">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="99edd-157">管理存储配额</span><span class="sxs-lookup"><span data-stu-id="99edd-157">Manage storage quotas</span></span>
- <span data-ttu-id="99edd-158">回收删除的存储资源</span><span class="sxs-lookup"><span data-stu-id="99edd-158">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="99edd-159">还原删除的存储帐户</span><span class="sxs-lookup"><span data-stu-id="99edd-159">Restore deleted storage accounts</span></span>
- <span data-ttu-id="99edd-160">将容器从一个共享迁移到另一个共享</span><span class="sxs-lookup"><span data-stu-id="99edd-160">Migrate containers from one share to another</span></span>
- <span data-ttu-id="99edd-161">查看单个存储组件的信息</span><span class="sxs-lookup"><span data-stu-id="99edd-161">View information about the individual storage components</span></span>
- <span data-ttu-id="99edd-162">查看使用情况和性能信息</span><span class="sxs-lookup"><span data-stu-id="99edd-162">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="99edd-163">订阅管理员</span><span class="sxs-lookup"><span data-stu-id="99edd-163">Subscription Admin</span></span>
<span data-ttu-id="99edd-164">Azure Stack 订阅管理员模块的预览版。</span><span class="sxs-lookup"><span data-stu-id="99edd-164">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="99edd-165">此模块提供的功能允许管理员执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="99edd-165">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="99edd-166">管理计划和套餐</span><span class="sxs-lookup"><span data-stu-id="99edd-166">Manage plans and offers</span></span>
- <span data-ttu-id="99edd-167">查看使用情况和性能信息</span><span class="sxs-lookup"><span data-stu-id="99edd-167">View usage and performance information</span></span>
- <span data-ttu-id="99edd-168">管理 RBAC</span><span class="sxs-lookup"><span data-stu-id="99edd-168">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="99edd-169">订阅</span><span class="sxs-lookup"><span data-stu-id="99edd-169">Subscription</span></span>
<span data-ttu-id="99edd-170">Azure Stack 订阅模块的预览版。</span><span class="sxs-lookup"><span data-stu-id="99edd-170">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="99edd-171">此模块提供的功能允许用户执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="99edd-171">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="99edd-172">创建、删除和更新订阅</span><span class="sxs-lookup"><span data-stu-id="99edd-172">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="99edd-173">更新</span><span class="sxs-lookup"><span data-stu-id="99edd-173">Update</span></span>
<span data-ttu-id="99edd-174">Azure Stack 更新管理员模块的预览版。</span><span class="sxs-lookup"><span data-stu-id="99edd-174">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="99edd-175">在此模块中，管理员可以执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="99edd-175">In this module administrators can:</span></span>
- <span data-ttu-id="99edd-176">列出和安装可用更新</span><span class="sxs-lookup"><span data-stu-id="99edd-176">List and install available updates</span></span>
- <span data-ttu-id="99edd-177">恢复中断的更新</span><span class="sxs-lookup"><span data-stu-id="99edd-177">Resume interrupted updates</span></span>
- <span data-ttu-id="99edd-178">查看安装的更新</span><span class="sxs-lookup"><span data-stu-id="99edd-178">View installed updates</span></span>
