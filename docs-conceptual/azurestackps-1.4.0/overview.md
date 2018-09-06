# <a name="azure-stack-module-140"></a><span data-ttu-id="7a443-101">Azure Stack 模块 1.4.0</span><span class="sxs-lookup"><span data-stu-id="7a443-101">Azure Stack Module 1.4.0</span></span>

## <a name="requirements"></a><span data-ttu-id="7a443-102">要求：</span><span class="sxs-lookup"><span data-stu-id="7a443-102">Requirements:</span></span>
<span data-ttu-id="7a443-103">Azure Stack 最低支持版本为 1804。</span><span class="sxs-lookup"><span data-stu-id="7a443-103">Minimum supported Azure Stack version is 1804.</span></span>

<span data-ttu-id="7a443-104">注意：如果使用的是早期版本，请安装版本 1.2.11</span><span class="sxs-lookup"><span data-stu-id="7a443-104">Note: If you are using an earlier version install version 1.2.11</span></span>

## <a name="known-issues"></a><span data-ttu-id="7a443-105">已知问题：</span><span class="sxs-lookup"><span data-stu-id="7a443-105">Known issues:</span></span>

- <span data-ttu-id="7a443-106">关闭警报需要 Azure Stack 版本 1803</span><span class="sxs-lookup"><span data-stu-id="7a443-106">Close Alert requires Azure Stack version 1803</span></span>
- <span data-ttu-id="7a443-107">New-AzsOffer 不允许创建状态为“公共”的产品/服务。</span><span class="sxs-lookup"><span data-stu-id="7a443-107">New-AzsOffer does not allow to create an offer with state public.</span></span> <span data-ttu-id="7a443-108">随后需调用 Set-AzsOffer cmdlet 来更改状态。</span><span class="sxs-lookup"><span data-stu-id="7a443-108">The Set-AzsOffer cmdlet needs to be called afterwards to change the state.</span></span>
- <span data-ttu-id="7a443-109">在不重新部署的情况下，不能删除 IP 池</span><span class="sxs-lookup"><span data-stu-id="7a443-109">An IP Pool cannot be removed without a redeployment</span></span>

## <a name="breaking-changes"></a><span data-ttu-id="7a443-110">重大更改</span><span class="sxs-lookup"><span data-stu-id="7a443-110">Breaking Changes</span></span>
<span data-ttu-id="7a443-111">自版本 1.3.0 以来没有重大更改。</span><span class="sxs-lookup"><span data-stu-id="7a443-111">There are no breaking changes from the version 1.3.0.</span></span> <span data-ttu-id="7a443-112">从 1.2.11 迁移时，所有重大更改记录在此处： https://aka.ms/azspowershellmigration</span><span class="sxs-lookup"><span data-stu-id="7a443-112">All breaking changes migrating from 1.2.11 are documented here https://aka.ms/azspowershellmigration</span></span>

## <a name="install"></a><span data-ttu-id="7a443-113">安装</span><span class="sxs-lookup"><span data-stu-id="7a443-113">Install</span></span>
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
## <a name="release-notes"></a><span data-ttu-id="7a443-114">发行说明</span><span class="sxs-lookup"><span data-stu-id="7a443-114">Release Notes</span></span>
    * <span data-ttu-id="7a443-115">与前一版本 1.3.0 相比，Azurestack 1.4.0 版没有重大更改</span><span class="sxs-lookup"><span data-stu-id="7a443-115">Azurestack 1.4.0 version has no breaking changes from the previous release 1.3.0</span></span>
    * <span data-ttu-id="7a443-116">Azs.AzureBridge.Admin</span><span class="sxs-lookup"><span data-stu-id="7a443-116">Azs.AzureBridge.Admin</span></span>
        - <span data-ttu-id="7a443-117">修复了在分页结果中仅返回单个页面的 bug</span><span class="sxs-lookup"><span data-stu-id="7a443-117">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="7a443-118">Azs.Backup.Admin</span><span class="sxs-lookup"><span data-stu-id="7a443-118">Azs.Backup.Admin</span></span>
        - <span data-ttu-id="7a443-119">在 cmdlet Set-AzsBackupShare 中添加了新参数 BackupFrequencyInHours、IsBackupSchedulerEnabled、BackupRetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="7a443-119">Added new parameters BackupFrequencyInHours, IsBackupSchedulerEnabled, BackupRetentionPeriodInDays in cmdlet Set-AzsBackupShare</span></span>
        - <span data-ttu-id="7a443-120">添加了 cmdlet New-EncyptionKeyBase64 以便于创建加密密钥</span><span class="sxs-lookup"><span data-stu-id="7a443-120">Added a cmdlet New-EncyptionKeyBase64 to facilitate creating encryption key</span></span>
        - <span data-ttu-id="7a443-121">修复了在分页结果中仅返回单个页面的 bug</span><span class="sxs-lookup"><span data-stu-id="7a443-121">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="7a443-122">Azs.Commerce.Admin</span><span class="sxs-lookup"><span data-stu-id="7a443-122">Azs.Commerce.Admin</span></span>
        - <span data-ttu-id="7a443-123">修复了在分页结果中仅返回单个页面的 bug</span><span class="sxs-lookup"><span data-stu-id="7a443-123">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="7a443-124">Azs.Fabric.Admin</span><span class="sxs-lookup"><span data-stu-id="7a443-124">Azs.Fabric.Admin</span></span>
        - <span data-ttu-id="7a443-125">修复了在分页结果中仅返回单个页面的 bug</span><span class="sxs-lookup"><span data-stu-id="7a443-125">Fix for the bug that returned only a single page in paginated results</span></span>
        - <span data-ttu-id="7a443-126">添加了 cmdlet Add-AzsScaleUnitNode 以使管理员可以将新的缩放单元节点添加到 azurestack 戳记</span><span class="sxs-lookup"><span data-stu-id="7a443-126">Added a cmdlet Add-AzsScaleUnitNode to enable admin to add new scale unit nodes to the azurestack stamp</span></span>
        - <span data-ttu-id="7a443-127">添加了 cmdlet 和 New-AzsScaleUnitNodeObject 以便于创建缩放单元参数对象</span><span class="sxs-lookup"><span data-stu-id="7a443-127">Added cmdlet and New-AzsScaleUnitNodeObject to facilitate the creation scale unit parameter objects</span></span>
    * <span data-ttu-id="7a443-128">Azs.Gallery.Admin</span><span class="sxs-lookup"><span data-stu-id="7a443-128">Azs.Gallery.Admin</span></span>
        - <span data-ttu-id="7a443-129">修复了在分页结果中仅返回单个页面的 bug</span><span class="sxs-lookup"><span data-stu-id="7a443-129">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="7a443-130">Azs.InfrastructureInsights.Admin</span><span class="sxs-lookup"><span data-stu-id="7a443-130">Azs.InfrastructureInsights.Admin</span></span>
        - <span data-ttu-id="7a443-131">修复了在分页结果中仅返回单个页面的 bug</span><span class="sxs-lookup"><span data-stu-id="7a443-131">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="7a443-132">Azs.Network.Admin</span><span class="sxs-lookup"><span data-stu-id="7a443-132">Azs.Network.Admin</span></span>
        - <span data-ttu-id="7a443-133">修复了在分页结果中仅返回单个页面的 bug</span><span class="sxs-lookup"><span data-stu-id="7a443-133">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="7a443-134">Azs.Update.Admin</span><span class="sxs-lookup"><span data-stu-id="7a443-134">Azs.Update.Admin</span></span>
        - <span data-ttu-id="7a443-135">修复了在分页结果中仅返回单个页面的 bug</span><span class="sxs-lookup"><span data-stu-id="7a443-135">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="7a443-136">Azs.Subscriptions</span><span class="sxs-lookup"><span data-stu-id="7a443-136">Azs.Subscriptions</span></span>
        - <span data-ttu-id="7a443-137">修复了在分页结果中仅返回单个页面的 bug</span><span class="sxs-lookup"><span data-stu-id="7a443-137">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="7a443-138">Azs.Subscriptions.Admin</span><span class="sxs-lookup"><span data-stu-id="7a443-138">Azs.Subscriptions.Admin</span></span>
        - <span data-ttu-id="7a443-139">添加了 cmdlet Move-AzsSubscription 以便在委托的提供商产品/服务之间移动订阅</span><span class="sxs-lookup"><span data-stu-id="7a443-139">Added a cmdlet Move-AzsSubscription to move subscriptions between delegated provider offers</span></span>
        - <span data-ttu-id="7a443-140">添加了 cmdlet Test-AzsMoveSubscription 以验证用户订阅是否可以在委托的提供商产品/服务之间移动</span><span class="sxs-lookup"><span data-stu-id="7a443-140">Added a cmdlet Test-AzsMoveSubscription to validate that user subscriptions can be moved between delegated provider offers</span></span>
        - <span data-ttu-id="7a443-141">修复了在分页结果中仅返回单个页面的 bug</span><span class="sxs-lookup"><span data-stu-id="7a443-141">Fix for the bug that returned only a single page in paginated results'</span></span>

## <a name="content"></a><span data-ttu-id="7a443-142">内容：</span><span class="sxs-lookup"><span data-stu-id="7a443-142">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="7a443-143">Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="7a443-143">Azure Bridge</span></span>
<span data-ttu-id="7a443-144">Azure Stack AzureBridge 管理员模块的预览版，用于联合 Azure 提供的映像。</span><span class="sxs-lookup"><span data-stu-id="7a443-144">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="7a443-145">备份</span><span class="sxs-lookup"><span data-stu-id="7a443-145">Backup</span></span>
<span data-ttu-id="7a443-146">备份管理员模块的预览版，允许管理员执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="7a443-146">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="7a443-147">配置备份的存储位置</span><span class="sxs-lookup"><span data-stu-id="7a443-147">Configure where backups are stored</span></span>
- <span data-ttu-id="7a443-148">执行备份</span><span class="sxs-lookup"><span data-stu-id="7a443-148">Perform backups</span></span>
- <span data-ttu-id="7a443-149">列出和还原完成的备份</span><span class="sxs-lookup"><span data-stu-id="7a443-149">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="7a443-150">商务</span><span class="sxs-lookup"><span data-stu-id="7a443-150">Commerce</span></span>
<span data-ttu-id="7a443-151">Azure Stack 商务管理员模块的预览版，用于查看整个 Azure Stack 系统的聚合数据使用情况。</span><span class="sxs-lookup"><span data-stu-id="7a443-151">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="7a443-152">计算</span><span class="sxs-lookup"><span data-stu-id="7a443-152">Compute</span></span>
<span data-ttu-id="7a443-153">Azure Stack 计算管理员模块的预览版，其提供的功能用于管理计算配额、平台映像和虚拟机扩展。</span><span class="sxs-lookup"><span data-stu-id="7a443-153">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="7a443-154">Fabric</span><span class="sxs-lookup"><span data-stu-id="7a443-154">Fabric</span></span>
<span data-ttu-id="7a443-155">Azure Stack Fabric 管理员模块的预览版，允许管理员查看和管理基础结构组件：</span><span class="sxs-lookup"><span data-stu-id="7a443-155">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="7a443-156">停止、启动和关闭缩放单元节点</span><span class="sxs-lookup"><span data-stu-id="7a443-156">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="7a443-157">针对 FRU 相关活动清空和恢复缩放单元节点</span><span class="sxs-lookup"><span data-stu-id="7a443-157">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="7a443-158">修复缩放单元节点</span><span class="sxs-lookup"><span data-stu-id="7a443-158">Repair of scale unit nodes</span></span>
- <span data-ttu-id="7a443-159">重启基础结构角色</span><span class="sxs-lookup"><span data-stu-id="7a443-159">Restart of Infrastructure role</span></span>
- <span data-ttu-id="7a443-160">停止、启动和关闭基础结构角色实例</span><span class="sxs-lookup"><span data-stu-id="7a443-160">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="7a443-161">创建新的 IP 池</span><span class="sxs-lookup"><span data-stu-id="7a443-161">Create new IP Pools</span></span>

### <a name="gallery"></a><span data-ttu-id="7a443-162">库</span><span class="sxs-lookup"><span data-stu-id="7a443-162">Gallery</span></span>
<span data-ttu-id="7a443-163">Azure Stack 库管理员模块的预览版，其提供的功能用于管理 Azure Stack 市场中的库项。</span><span class="sxs-lookup"><span data-stu-id="7a443-163">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="7a443-164">基础结构见解</span><span class="sxs-lookup"><span data-stu-id="7a443-164">Infrastructure Insights</span></span>
<span data-ttu-id="7a443-165">基础结构见解管理员模块的预览版，允许管理员执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="7a443-165">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="7a443-166">查看 Azure Stack 戳资源的运行状况</span><span class="sxs-lookup"><span data-stu-id="7a443-166">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="7a443-167">查看和管理警报</span><span class="sxs-lookup"><span data-stu-id="7a443-167">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="7a443-168">KeyVault</span><span class="sxs-lookup"><span data-stu-id="7a443-168">KeyVault</span></span>
<span data-ttu-id="7a443-169">Azure Stack KeyVault 管理员模块的预览版，允许管理员查看 KeyVault 配额。</span><span class="sxs-lookup"><span data-stu-id="7a443-169">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="7a443-170">网络</span><span class="sxs-lookup"><span data-stu-id="7a443-170">Network</span></span>
<span data-ttu-id="7a443-171">网络管理员模块的预览版，用于执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="7a443-171">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="7a443-172">管理网络配额</span><span class="sxs-lookup"><span data-stu-id="7a443-172">Management of network quotas</span></span>
- <span data-ttu-id="7a443-173">查看分配的网络资源，例如公共 IP 地址、虚拟网络、负载均衡器</span><span class="sxs-lookup"><span data-stu-id="7a443-173">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="7a443-174">提供一个显示管理员概览的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="7a443-174">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="7a443-175">存储</span><span class="sxs-lookup"><span data-stu-id="7a443-175">Storage</span></span>
<span data-ttu-id="7a443-176">Azure Stack 存储管理员模块的预览版。</span><span class="sxs-lookup"><span data-stu-id="7a443-176">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="7a443-177">此版本提供以下功能：</span><span class="sxs-lookup"><span data-stu-id="7a443-177">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="7a443-178">管理存储配额</span><span class="sxs-lookup"><span data-stu-id="7a443-178">Manage storage quotas</span></span>
- <span data-ttu-id="7a443-179">回收删除的存储资源</span><span class="sxs-lookup"><span data-stu-id="7a443-179">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="7a443-180">还原删除的存储帐户</span><span class="sxs-lookup"><span data-stu-id="7a443-180">Restore deleted storage accounts</span></span>
- <span data-ttu-id="7a443-181">将容器从一个共享迁移到另一个共享</span><span class="sxs-lookup"><span data-stu-id="7a443-181">Migrate containers from one share to another</span></span>
- <span data-ttu-id="7a443-182">查看单个存储组件的信息</span><span class="sxs-lookup"><span data-stu-id="7a443-182">View information about the individual storage components</span></span>
- <span data-ttu-id="7a443-183">查看使用情况和性能信息</span><span class="sxs-lookup"><span data-stu-id="7a443-183">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="7a443-184">订阅管理员</span><span class="sxs-lookup"><span data-stu-id="7a443-184">Subscription Admin</span></span>
<span data-ttu-id="7a443-185">Azure Stack 订阅管理员模块的预览版。</span><span class="sxs-lookup"><span data-stu-id="7a443-185">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="7a443-186">此模块提供的功能允许管理员执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="7a443-186">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="7a443-187">管理计划和套餐</span><span class="sxs-lookup"><span data-stu-id="7a443-187">Manage plans and offers</span></span>
- <span data-ttu-id="7a443-188">查看使用情况和性能信息</span><span class="sxs-lookup"><span data-stu-id="7a443-188">View usage and performance information</span></span>
- <span data-ttu-id="7a443-189">管理 RBAC</span><span class="sxs-lookup"><span data-stu-id="7a443-189">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="7a443-190">订阅</span><span class="sxs-lookup"><span data-stu-id="7a443-190">Subscription</span></span>
<span data-ttu-id="7a443-191">Azure Stack 订阅模块的预览版。</span><span class="sxs-lookup"><span data-stu-id="7a443-191">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="7a443-192">此模块提供的功能允许用户执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="7a443-192">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="7a443-193">创建、删除和更新订阅</span><span class="sxs-lookup"><span data-stu-id="7a443-193">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="7a443-194">更新</span><span class="sxs-lookup"><span data-stu-id="7a443-194">Update</span></span>
<span data-ttu-id="7a443-195">Azure Stack 更新管理员模块的预览版。</span><span class="sxs-lookup"><span data-stu-id="7a443-195">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="7a443-196">在此模块中，管理员可以执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="7a443-196">In this module administrators can:</span></span>
- <span data-ttu-id="7a443-197">列出和安装可用更新</span><span class="sxs-lookup"><span data-stu-id="7a443-197">List and install available updates</span></span>
- <span data-ttu-id="7a443-198">恢复中断的更新</span><span class="sxs-lookup"><span data-stu-id="7a443-198">Resume interrupted updates</span></span>
- <span data-ttu-id="7a443-199">查看安装的更新</span><span class="sxs-lookup"><span data-stu-id="7a443-199">View installed updates</span></span>
