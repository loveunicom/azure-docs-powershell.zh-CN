---
title: Azure PowerShell 更改日志 | Microsoft Docs
description: 下面提供了对 Azure PowerShell 最新版本所做更改的历史记录。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 5/1/2018
ms.openlocfilehash: 3811e28dda69d194d23934943fb47d562f869fc4
ms.sourcegitcommit: 5a5b6dd216d5f805204244146cf6f88ad2f34fb4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/19/2018
ms.locfileid: "36237590"
---
# <a name="release-notes"></a><span data-ttu-id="39cd8-103">发行说明</span><span class="sxs-lookup"><span data-stu-id="39cd8-103">Release notes</span></span>

<span data-ttu-id="39cd8-104">下面是此版本中对 Azure PowerShell 所做的更改列表。</span><span class="sxs-lookup"><span data-stu-id="39cd8-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="630---june-2018"></a><span data-ttu-id="39cd8-105">6.3.0 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="39cd8-105">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="39cd8-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="39cd8-106">AzureRM.Profile</span></span>
* <span data-ttu-id="39cd8-107">更新了 Enable-AzureRmContextAutoSave 的错误消息</span><span class="sxs-lookup"><span data-stu-id="39cd8-107">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="39cd8-108">在运行没有旧上下文的“Connect-AzureRmAccount”时为每个订阅创建一个上下文</span><span class="sxs-lookup"><span data-stu-id="39cd8-108">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="39cd8-109">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="39cd8-109">Azure.Storage</span></span>
* <span data-ttu-id="39cd8-110">在帮助文件中增加了关于 -Permissions 参数的其他信息。</span><span class="sxs-lookup"><span data-stu-id="39cd8-110">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="39cd8-111">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="39cd8-111">AzureRM.Compute</span></span>
* <span data-ttu-id="39cd8-112">“Get-AzureRmVmDiskEncryptionStatus”修复了一个针对没有数据磁盘的 VM 观察到的问题</span><span class="sxs-lookup"><span data-stu-id="39cd8-112">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="39cd8-113">更新计算客户端库版本以修复以下 cmdlet</span><span class="sxs-lookup"><span data-stu-id="39cd8-113">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="39cd8-114">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="39cd8-114">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="39cd8-115">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="39cd8-115">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="39cd8-116">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="39cd8-116">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="39cd8-117">修复了以下 cmdlet，因此可以正确地显示“操作 ID”和“操作状态”：</span><span class="sxs-lookup"><span data-stu-id="39cd8-117">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="39cd8-118">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="39cd8-118">Start-AzureRmVM</span></span>
    - <span data-ttu-id="39cd8-119">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="39cd8-119">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="39cd8-120">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="39cd8-120">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="39cd8-121">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="39cd8-121">Set-AzureRmVM</span></span>
    - <span data-ttu-id="39cd8-122">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="39cd8-122">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="39cd8-123">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="39cd8-123">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="39cd8-124">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="39cd8-124">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="39cd8-125">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="39cd8-125">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="39cd8-126">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="39cd8-126">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="39cd8-127">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="39cd8-127">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="39cd8-128">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="39cd8-128">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="39cd8-129">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="39cd8-129">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="39cd8-130">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="39cd8-130">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="39cd8-131">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="39cd8-131">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="39cd8-132">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="39cd8-132">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="39cd8-133">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="39cd8-133">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="39cd8-134">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="39cd8-134">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="39cd8-135">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="39cd8-135">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="39cd8-136">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="39cd8-136">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="39cd8-137">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="39cd8-137">AzureRM.EventGrid</span></span>
* <span data-ttu-id="39cd8-138">在 Update-AzureRmEventGridSubscription cmdlet 中删除 SubjectBeginsWith/SubjectEndsWith 的 ValidateNotNullOrEmpty 验证条件，允许根据需要将这些参数更改为空字符串。</span><span class="sxs-lookup"><span data-stu-id="39cd8-138">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="39cd8-139">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="39cd8-139">AzureRM.KeyVault</span></span>
* <span data-ttu-id="39cd8-140">修复运行 Get-AzureRmKeyVault -Tag 时不返回任何标记的问题</span><span class="sxs-lookup"><span data-stu-id="39cd8-140">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="39cd8-141">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="39cd8-141">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="39cd8-142">策略见解 cmdlet 的公开发行版</span><span class="sxs-lookup"><span data-stu-id="39cd8-142">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="39cd8-143">使用 API 版本 2018-04-04</span><span class="sxs-lookup"><span data-stu-id="39cd8-143">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="39cd8-144">向 Get-AzureRmPolicyStateSummary 的结果添加了 PolicyDefinitionReferenceId</span><span class="sxs-lookup"><span data-stu-id="39cd8-144">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="39cd8-145">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="39cd8-145">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="39cd8-146">向 RecoveryServices.Backup cmdlet 添加了 -Vault 参数。</span><span class="sxs-lookup"><span data-stu-id="39cd8-146">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="39cd8-147">传递时，此项会替代 Set-AzureRmRecoveryServicesContext cmdlet。</span><span class="sxs-lookup"><span data-stu-id="39cd8-147">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="39cd8-148">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="39cd8-148">AzureRM.Sql</span></span>
* <span data-ttu-id="39cd8-149">更新了 Get-AzureRmSqlDatabaseExpanded 的帮助文件中的示例</span><span class="sxs-lookup"><span data-stu-id="39cd8-149">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="39cd8-150">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="39cd8-150">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="39cd8-151">更新了 Add-AzureRmTrafficManagerEndpointConfig 的帮助文件</span><span class="sxs-lookup"><span data-stu-id="39cd8-151">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="39cd8-152">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="39cd8-152">AzureRM.Websites</span></span>
* <span data-ttu-id="39cd8-153">更新了“Set-AzureRmWebApp”，在使用 -AssignIdentity 时不覆盖 AppSettings</span><span class="sxs-lookup"><span data-stu-id="39cd8-153">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="39cd8-154">更新了“New-AzureRmWebAppSlot”，允许使用 AppServicePlan 作为可选参数</span><span class="sxs-lookup"><span data-stu-id="39cd8-154">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="39cd8-155">6.2.1 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="39cd8-155">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="39cd8-156">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="39cd8-156">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="39cd8-157">更新了 PSWorkspace 模型，允许 Network 使用 type 作为参数</span><span class="sxs-lookup"><span data-stu-id="39cd8-157">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="39cd8-158">6.2.0 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="39cd8-158">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="39cd8-159">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="39cd8-159">AzureRM.Profile</span></span>
* <span data-ttu-id="39cd8-160">修复了 Newtonsoft.Json 的版本 10.0.3 在模块导入时无法加载的问题</span><span class="sxs-lookup"><span data-stu-id="39cd8-160">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="39cd8-161">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="39cd8-161">AzureRM.Compute</span></span>
* <span data-ttu-id="39cd8-162">VMSS VM 更新功能</span><span class="sxs-lookup"><span data-stu-id="39cd8-162">VMSS VM Update feature</span></span>
    - <span data-ttu-id="39cd8-163">增加了“Update-AzureRmVmssVM”和“New-AzureRmVMDataDisk”cmdlet</span><span class="sxs-lookup"><span data-stu-id="39cd8-163">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="39cd8-164">为“Add-AzureRmVMDataDisk”cmdlet 增加了 VirtualMachineScaleSetVM 参数，支持向 Vmss VM 添加数据磁盘。</span><span class="sxs-lookup"><span data-stu-id="39cd8-164">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="39cd8-165">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="39cd8-165">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="39cd8-166">将 ADF.Net SDK 版本更新到了 0.8.0-preview，其中包含以下更改：</span><span class="sxs-lookup"><span data-stu-id="39cd8-166">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="39cd8-167">增加了“配置工厂存储库”操作</span><span class="sxs-lookup"><span data-stu-id="39cd8-167">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="39cd8-168">更新了 QuickBooks LinkedService，可以公开 consumerKey 和 consumerSecret 属性</span><span class="sxs-lookup"><span data-stu-id="39cd8-168">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="39cd8-169">已将多个模型类型从 SecretBase 更新为 Object</span><span class="sxs-lookup"><span data-stu-id="39cd8-169">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="39cd8-170">增加了 Blob 事件触发器</span><span class="sxs-lookup"><span data-stu-id="39cd8-170">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="39cd8-171">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="39cd8-171">AzureRM.KeyVault</span></span>
* <span data-ttu-id="39cd8-172">使用示例输出更新了文档</span><span class="sxs-lookup"><span data-stu-id="39cd8-172">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="39cd8-173">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="39cd8-173">AzureRM.Network</span></span>
* <span data-ttu-id="39cd8-174">在网络观察程序 cmdlet 上启用了流量分析参数</span><span class="sxs-lookup"><span data-stu-id="39cd8-174">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="39cd8-175">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="39cd8-175">AzureRM.Resources</span></span>
* <span data-ttu-id="39cd8-176">修复了从“Get-AzureRmResource”返回的“PSResource”对象的“Properties”属性问题</span><span class="sxs-lookup"><span data-stu-id="39cd8-176">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="39cd8-177">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="39cd8-177">AzureRM.Scheduler</span></span>
* <span data-ttu-id="39cd8-178">修复了更新 ServiceBusQueueJob 无法设置新 Auth 值的问题</span><span class="sxs-lookup"><span data-stu-id="39cd8-178">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="39cd8-179">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="39cd8-179">AzureRM.Sql</span></span>
* <span data-ttu-id="39cd8-180">使用可选的 LicenseType 参数更新了以下 cmdlet</span><span class="sxs-lookup"><span data-stu-id="39cd8-180">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="39cd8-181">New-AzureRmSqlDatabase；Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="39cd8-181">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="39cd8-182">New-AzureRmSqlElasticPool；Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="39cd8-182">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="39cd8-183">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="39cd8-183">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="39cd8-184">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="39cd8-184">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="39cd8-185">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="39cd8-185">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="39cd8-186">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="39cd8-186">AzureRM.Websites</span></span>
* <span data-ttu-id="39cd8-187">更新了“New-AzureRMWebApp”，可以使用策略库中的常用算法。</span><span class="sxs-lookup"><span data-stu-id="39cd8-187">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="39cd8-188">6.1.0 - 2018 年 5 月</span><span class="sxs-lookup"><span data-stu-id="39cd8-188">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="39cd8-189">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="39cd8-189">AzureRM.Profile</span></span>
* <span data-ttu-id="39cd8-190">修复了运行“Clear-AzureRmContext”时会保留空上下文的问题，该上下文使用旧的默认上下文的名称，导致用户无法使用旧名称创建新的上下文</span><span class="sxs-lookup"><span data-stu-id="39cd8-190">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="39cd8-191">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="39cd8-191">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="39cd8-192">允许在 AS 上执行网关的关联/取消关联操作。</span><span class="sxs-lookup"><span data-stu-id="39cd8-192">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="39cd8-193">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="39cd8-193">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="39cd8-194">增加了对 ApiVersions、ApiReleases 和 ApiRevisions 的支持</span><span class="sxs-lookup"><span data-stu-id="39cd8-194">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="39cd8-195">增加了对 ServiceFabric 后端的支持</span><span class="sxs-lookup"><span data-stu-id="39cd8-195">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="39cd8-196">增加了对 Application Insights Logger 的支持</span><span class="sxs-lookup"><span data-stu-id="39cd8-196">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="39cd8-197">增加的支持包括认可“基本”SKU 是 API 管理服务的有效 SKU</span><span class="sxs-lookup"><span data-stu-id="39cd8-197">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="39cd8-198">增加的支持包括允许将专用 CA 颁发的证书作为根证书或 CA 证书安装</span><span class="sxs-lookup"><span data-stu-id="39cd8-198">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="39cd8-199">增加的支持包括通过 KeyVault 和多个代理主机名接受自定义 SSL 证书</span><span class="sxs-lookup"><span data-stu-id="39cd8-199">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="39cd8-200">增加了对 MSI 标识的支持</span><span class="sxs-lookup"><span data-stu-id="39cd8-200">Added support for MSI identity</span></span>
* <span data-ttu-id="39cd8-201">增加的支持包括通过 URL 接受策略 注意：以下 cmdlet 将在未来版本中弃用</span><span class="sxs-lookup"><span data-stu-id="39cd8-201">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="39cd8-202">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="39cd8-202">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="39cd8-203">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="39cd8-203">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="39cd8-204">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="39cd8-204">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="39cd8-205">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="39cd8-205">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="39cd8-206">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="39cd8-206">AzureRM.Batch</span></span>
* <span data-ttu-id="39cd8-207">发布新 cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="39cd8-207">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="39cd8-208">发布新 cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="39cd8-208">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="39cd8-209">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="39cd8-209">AzureRM.Consumption</span></span>
* <span data-ttu-id="39cd8-210">在 Cmdlet Get-AzureRmConsumptionUsageDetail 中增加了新参数 Expand、ResourceGroup、InstanceName、InstanceId、Tags、Top</span><span class="sxs-lookup"><span data-stu-id="39cd8-210">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="39cd8-211">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="39cd8-211">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="39cd8-212">修复了 Export-AzureRmDataLakeStoreChildItemProperties 的示例</span><span class="sxs-lookup"><span data-stu-id="39cd8-212">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="39cd8-213">修复了 Set-AzureRmDataLakeStoreItemAclEntry 中 Recurse 用例的 null 参数异常</span><span class="sxs-lookup"><span data-stu-id="39cd8-213">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="39cd8-214">修复了 Set-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAcl、Remove-AzureRmDataLakeStoreItemAclEntry 的帮助文件</span><span class="sxs-lookup"><span data-stu-id="39cd8-214">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="39cd8-215">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="39cd8-215">AzureRM.Network</span></span>
* <span data-ttu-id="39cd8-216">将网络 SDK 版本从 18.0.0-preview 升至 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="39cd8-216">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="39cd8-217">增加了用于创建协议配置的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="39cd8-217">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="39cd8-218">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="39cd8-218">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="39cd8-219">增加了用于向现有的快速路由线路添加新的线路连接的 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="39cd8-219">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="39cd8-220">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="39cd8-220">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="39cd8-221">增加了用于从现有的快速路由线路删除线路连接的 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="39cd8-221">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="39cd8-222">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="39cd8-222">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="39cd8-223">增加了用于检索线路连接的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="39cd8-223">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="39cd8-224">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="39cd8-224">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="39cd8-225">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="39cd8-225">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="39cd8-226">修复了使用生成的证书进行服务器身份验证的问题（问题 5998）</span><span class="sxs-lookup"><span data-stu-id="39cd8-226">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="39cd8-227">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="39cd8-227">AzureRM.Sql</span></span>
* <span data-ttu-id="39cd8-228">更新了审核 cmdlet，允许删除 AuditActions 或 AuditActionGroups</span><span class="sxs-lookup"><span data-stu-id="39cd8-228">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="39cd8-229">修复了设置新的灵活保留策略时使用 Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy 出现的问题。该问题的具体表现是：在命令失败的同时，出现“不再支持使用 Azure 恢复服务保管库和策略配置长期保留策略。</span><span class="sxs-lookup"><span data-stu-id="39cd8-229">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="39cd8-230">请使用新的灵活保留策略提交请求”错误消息。</span><span class="sxs-lookup"><span data-stu-id="39cd8-230">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="39cd8-231">更新了与 Azure SQL 数据库/ElasticPool 的创建/更新相关的所有 cmdlet，允许使用新的数据库 API，而这些 cmdlet 支持的 SKU 属性则适用于规模和层相关属性。</span><span class="sxs-lookup"><span data-stu-id="39cd8-231">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="39cd8-232">更新的 cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="39cd8-232">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="39cd8-233">New-AzureRmSqlDatabase；Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="39cd8-233">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="39cd8-234">New-AzureRmSqlElasticPool；Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="39cd8-234">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="39cd8-235">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="39cd8-235">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="39cd8-236">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="39cd8-236">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="39cd8-237">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="39cd8-237">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="39cd8-238">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="39cd8-238">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="39cd8-239">更新了“Get-AzureRmTrafficManagerProfile”的参数，要求在使用 -Name 参数时使用 -ResourceGroupName 参数。</span><span class="sxs-lookup"><span data-stu-id="39cd8-239">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>