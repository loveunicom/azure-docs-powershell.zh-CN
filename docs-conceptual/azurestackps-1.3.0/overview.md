# <a name="azure-stack-module-130"></a><span data-ttu-id="648d5-101">Azure Stack 模块 1.3.0</span><span class="sxs-lookup"><span data-stu-id="648d5-101">Azure Stack Module 1.3.0</span></span>

## <a name="requirements"></a><span data-ttu-id="648d5-102">要求：</span><span class="sxs-lookup"><span data-stu-id="648d5-102">Requirements:</span></span>
<span data-ttu-id="648d5-103">Azure Stack 最低支持版本为 1804。</span><span class="sxs-lookup"><span data-stu-id="648d5-103">Minimum supported Azure Stack version is 1804.</span></span>

<span data-ttu-id="648d5-104">注意：如果使用的是早期版本，请安装版本 1.2.11</span><span class="sxs-lookup"><span data-stu-id="648d5-104">Note: If you are using an earlier version install version 1.2.11</span></span>

## <a name="known-issues"></a><span data-ttu-id="648d5-105">已知问题：</span><span class="sxs-lookup"><span data-stu-id="648d5-105">Known issues:</span></span>

- <span data-ttu-id="648d5-106">关闭警报需要 Azure Stack 版本 1803</span><span class="sxs-lookup"><span data-stu-id="648d5-106">Close Alert requires Azure Stack version 1803</span></span>
- <span data-ttu-id="648d5-107">某些存储 cmdlet 需要 Azure Stack 版本 1804</span><span class="sxs-lookup"><span data-stu-id="648d5-107">Some Storage cmdlets do require Azure Stack version 1804</span></span>
- <span data-ttu-id="648d5-108">New-AzsOffer 不允许创建状态为“公共”的产品/服务。</span><span class="sxs-lookup"><span data-stu-id="648d5-108">New-AzsOffer does not allow to create an offer with state public.</span></span> <span data-ttu-id="648d5-109">随后需调用 Set-AzsOffer cmdlet 来更改状态。</span><span class="sxs-lookup"><span data-stu-id="648d5-109">The Set-AzsOffer cmdlet needs to be called afterwards to change the state.</span></span>
- <span data-ttu-id="648d5-110">在不重新部署的情况下，不能删除 IP 池</span><span class="sxs-lookup"><span data-stu-id="648d5-110">An IP Pool cannot be removed without a redeployment</span></span>

## <a name="breaking-changes"></a><span data-ttu-id="648d5-111">重大更改</span><span class="sxs-lookup"><span data-stu-id="648d5-111">Breaking Changes</span></span>
<span data-ttu-id="648d5-112">从 1.2.11 迁移时，所有重大更改记录在此处：https://aka.ms/azspowershellmigration</span><span class="sxs-lookup"><span data-stu-id="648d5-112">All breaking changes migrating from 1.2.11 are documented here https://aka.ms/azspowershellmigration</span></span>

## <a name="install"></a><span data-ttu-id="648d5-113">安装</span><span class="sxs-lookup"><span data-stu-id="648d5-113">Install</span></span>
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
## <a name="content"></a><span data-ttu-id="648d5-114">内容：</span><span class="sxs-lookup"><span data-stu-id="648d5-114">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="648d5-115">Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="648d5-115">Azure Bridge</span></span>
<span data-ttu-id="648d5-116">Azure Stack AzureBridge 管理员模块的预览版，用于联合 Azure 提供的映像。</span><span class="sxs-lookup"><span data-stu-id="648d5-116">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="648d5-117">备份</span><span class="sxs-lookup"><span data-stu-id="648d5-117">Backup</span></span>
<span data-ttu-id="648d5-118">备份管理员模块的预览版，允许管理员执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="648d5-118">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="648d5-119">配置备份的存储位置</span><span class="sxs-lookup"><span data-stu-id="648d5-119">Configure where backups are stored</span></span>
- <span data-ttu-id="648d5-120">执行备份</span><span class="sxs-lookup"><span data-stu-id="648d5-120">Perform backups</span></span>
- <span data-ttu-id="648d5-121">列出和还原完成的备份</span><span class="sxs-lookup"><span data-stu-id="648d5-121">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="648d5-122">商务</span><span class="sxs-lookup"><span data-stu-id="648d5-122">Commerce</span></span>
<span data-ttu-id="648d5-123">Azure Stack 商务管理员模块的预览版，用于查看整个 Azure Stack 系统的聚合数据使用情况。</span><span class="sxs-lookup"><span data-stu-id="648d5-123">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="648d5-124">计算</span><span class="sxs-lookup"><span data-stu-id="648d5-124">Compute</span></span>
<span data-ttu-id="648d5-125">Azure Stack 计算管理员模块的预览版，其提供的功能用于管理计算配额、平台映像和虚拟机扩展。</span><span class="sxs-lookup"><span data-stu-id="648d5-125">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="648d5-126">Fabric</span><span class="sxs-lookup"><span data-stu-id="648d5-126">Fabric</span></span>
<span data-ttu-id="648d5-127">Azure Stack Fabric 管理员模块的预览版，允许管理员查看和管理基础结构组件：</span><span class="sxs-lookup"><span data-stu-id="648d5-127">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="648d5-128">停止、启动和关闭缩放单元节点</span><span class="sxs-lookup"><span data-stu-id="648d5-128">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="648d5-129">针对 FRU 相关活动清空和恢复缩放单元节点</span><span class="sxs-lookup"><span data-stu-id="648d5-129">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="648d5-130">修复缩放单元节点</span><span class="sxs-lookup"><span data-stu-id="648d5-130">Repair of scale unit nodes</span></span>
- <span data-ttu-id="648d5-131">重启基础结构角色</span><span class="sxs-lookup"><span data-stu-id="648d5-131">Restart of Infrastructure role</span></span>
- <span data-ttu-id="648d5-132">停止、启动和关闭基础结构角色实例</span><span class="sxs-lookup"><span data-stu-id="648d5-132">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="648d5-133">创建新的 IP 池</span><span class="sxs-lookup"><span data-stu-id="648d5-133">Create new IP Pools</span></span>


### <a name="gallery"></a><span data-ttu-id="648d5-134">库</span><span class="sxs-lookup"><span data-stu-id="648d5-134">Gallery</span></span>
<span data-ttu-id="648d5-135">Azure Stack 库管理员模块的预览版，其提供的功能用于管理 Azure Stack 商城中的库项。</span><span class="sxs-lookup"><span data-stu-id="648d5-135">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="648d5-136">基础结构见解</span><span class="sxs-lookup"><span data-stu-id="648d5-136">Infrastructure Insights</span></span>
<span data-ttu-id="648d5-137">基础结构见解管理员模块的预览版，允许管理员执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="648d5-137">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="648d5-138">查看 Azure Stack 戳资源的运行状况</span><span class="sxs-lookup"><span data-stu-id="648d5-138">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="648d5-139">查看和管理警报</span><span class="sxs-lookup"><span data-stu-id="648d5-139">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="648d5-140">KeyVault</span><span class="sxs-lookup"><span data-stu-id="648d5-140">KeyVault</span></span>
<span data-ttu-id="648d5-141">Azure Stack KeyVault 管理员模块的预览版，允许管理员查看 KeyVault 配额。</span><span class="sxs-lookup"><span data-stu-id="648d5-141">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="648d5-142">网络</span><span class="sxs-lookup"><span data-stu-id="648d5-142">Network</span></span>
<span data-ttu-id="648d5-143">网络管理员模块的预览版，用于执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="648d5-143">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="648d5-144">管理网络配额</span><span class="sxs-lookup"><span data-stu-id="648d5-144">Management of network quotas</span></span>
- <span data-ttu-id="648d5-145">查看分配的网络资源，例如公共 IP 地址、虚拟网络、负载均衡器</span><span class="sxs-lookup"><span data-stu-id="648d5-145">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="648d5-146">提供一个显示管理员概览的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="648d5-146">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="648d5-147">存储</span><span class="sxs-lookup"><span data-stu-id="648d5-147">Storage</span></span>
<span data-ttu-id="648d5-148">Azure Stack 存储管理员模块的预览版。</span><span class="sxs-lookup"><span data-stu-id="648d5-148">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="648d5-149">此版本提供以下功能：</span><span class="sxs-lookup"><span data-stu-id="648d5-149">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="648d5-150">管理存储配额</span><span class="sxs-lookup"><span data-stu-id="648d5-150">Manage storage quotas</span></span>
- <span data-ttu-id="648d5-151">回收删除的存储资源</span><span class="sxs-lookup"><span data-stu-id="648d5-151">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="648d5-152">还原删除的存储帐户</span><span class="sxs-lookup"><span data-stu-id="648d5-152">Restore deleted storage accounts</span></span>
- <span data-ttu-id="648d5-153">将容器从一个共享迁移到另一个共享</span><span class="sxs-lookup"><span data-stu-id="648d5-153">Migrate containers from one share to another</span></span>
- <span data-ttu-id="648d5-154">查看单个存储组件的信息</span><span class="sxs-lookup"><span data-stu-id="648d5-154">View information about the individual storage components</span></span>
- <span data-ttu-id="648d5-155">查看使用情况和性能信息</span><span class="sxs-lookup"><span data-stu-id="648d5-155">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="648d5-156">订阅管理员</span><span class="sxs-lookup"><span data-stu-id="648d5-156">Subscription Admin</span></span>
<span data-ttu-id="648d5-157">Azure Stack 订阅管理员模块的预览版。</span><span class="sxs-lookup"><span data-stu-id="648d5-157">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="648d5-158">此模块提供的功能允许管理员执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="648d5-158">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="648d5-159">管理计划和产品/服务</span><span class="sxs-lookup"><span data-stu-id="648d5-159">Manage plans and offers</span></span>
- <span data-ttu-id="648d5-160">查看使用情况和性能信息</span><span class="sxs-lookup"><span data-stu-id="648d5-160">View usage and performance information</span></span>
- <span data-ttu-id="648d5-161">管理 RBAC</span><span class="sxs-lookup"><span data-stu-id="648d5-161">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="648d5-162">订阅</span><span class="sxs-lookup"><span data-stu-id="648d5-162">Subscription</span></span>
<span data-ttu-id="648d5-163">Azure Stack 订阅模块的预览版。</span><span class="sxs-lookup"><span data-stu-id="648d5-163">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="648d5-164">此模块提供的功能允许用户执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="648d5-164">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="648d5-165">创建、删除和更新订阅</span><span class="sxs-lookup"><span data-stu-id="648d5-165">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="648d5-166">更新</span><span class="sxs-lookup"><span data-stu-id="648d5-166">Update</span></span>
<span data-ttu-id="648d5-167">Azure Stack 更新管理员模块的预览版。</span><span class="sxs-lookup"><span data-stu-id="648d5-167">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="648d5-168">在此模块中，管理员可以执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="648d5-168">In this module administrators can:</span></span>
- <span data-ttu-id="648d5-169">列出和安装可用更新</span><span class="sxs-lookup"><span data-stu-id="648d5-169">List and install available updates</span></span>
- <span data-ttu-id="648d5-170">恢复中断的更新</span><span class="sxs-lookup"><span data-stu-id="648d5-170">Resume interrupted updates</span></span>
- <span data-ttu-id="648d5-171">查看安装的更新</span><span class="sxs-lookup"><span data-stu-id="648d5-171">View installed updates</span></span>
