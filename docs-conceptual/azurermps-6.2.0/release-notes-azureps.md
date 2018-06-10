---
title: Azure PowerShell 更改日志 | Microsoft Docs
description: 下面提供了对 Azure PowerShell 最新版本所做更改的历史记录。
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 5/1/2018
ms.openlocfilehash: f90c77d8c9cd78315264fb0a0a58e047aefc5041
ms.sourcegitcommit: 2eea03b7ac19ad6d7c8097743d33c7ddb9c4df77
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/06/2018
ms.locfileid: "34821864"
---
# <a name="release-notes"></a><span data-ttu-id="26203-103">发行说明</span><span class="sxs-lookup"><span data-stu-id="26203-103">Release notes</span></span>

<span data-ttu-id="26203-104">下面是此版本中对 Azure PowerShell 所做的更改列表。</span><span class="sxs-lookup"><span data-stu-id="26203-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="620---june-2018"></a><span data-ttu-id="26203-105">6.2.0 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="26203-105">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="26203-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="26203-106">AzureRM.Profile</span></span>
* <span data-ttu-id="26203-107">修复了 Newtonsoft.Json 的版本 10.0.3 在模块导入时无法加载的问题</span><span class="sxs-lookup"><span data-stu-id="26203-107">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="26203-108">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="26203-108">AzureRM.Compute</span></span>
* <span data-ttu-id="26203-109">VMSS VM 更新功能</span><span class="sxs-lookup"><span data-stu-id="26203-109">VMSS VM Update feature</span></span>
    - <span data-ttu-id="26203-110">增加了“Update-AzureRmVmssVM”和“New-AzureRmVMDataDisk”cmdlet</span><span class="sxs-lookup"><span data-stu-id="26203-110">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="26203-111">为“Add-AzureRmVMDataDisk”cmdlet 增加了 VirtualMachineScaleSetVM 参数，支持向 Vmss VM 添加数据磁盘。</span><span class="sxs-lookup"><span data-stu-id="26203-111">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="26203-112">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="26203-112">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="26203-113">将 ADF.Net SDK 版本更新到了 0.8.0-preview，其中包含以下更改：</span><span class="sxs-lookup"><span data-stu-id="26203-113">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="26203-114">增加了“配置工厂存储库”操作</span><span class="sxs-lookup"><span data-stu-id="26203-114">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="26203-115">更新了 QuickBooks LinkedService，可以公开 consumerKey 和 consumerSecret 属性</span><span class="sxs-lookup"><span data-stu-id="26203-115">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="26203-116">已将多个模型类型从 SecretBase 更新为 Object</span><span class="sxs-lookup"><span data-stu-id="26203-116">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="26203-117">增加了 Blob 事件触发器</span><span class="sxs-lookup"><span data-stu-id="26203-117">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="26203-118">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="26203-118">AzureRM.KeyVault</span></span>
* <span data-ttu-id="26203-119">使用示例输出更新了文档</span><span class="sxs-lookup"><span data-stu-id="26203-119">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="26203-120">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="26203-120">AzureRM.Network</span></span>
* <span data-ttu-id="26203-121">在网络观察程序 cmdlet 上启用了流量分析参数</span><span class="sxs-lookup"><span data-stu-id="26203-121">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="26203-122">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="26203-122">AzureRM.Resources</span></span>
* <span data-ttu-id="26203-123">修复了从“Get-AzureRmResource”返回的“PSResource”对象的“Properties”属性问题</span><span class="sxs-lookup"><span data-stu-id="26203-123">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="26203-124">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="26203-124">AzureRM.Scheduler</span></span>
* <span data-ttu-id="26203-125">修复了更新 ServiceBusQueueJob 无法设置新 Auth 值的问题</span><span class="sxs-lookup"><span data-stu-id="26203-125">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="26203-126">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="26203-126">AzureRM.Sql</span></span>
* <span data-ttu-id="26203-127">使用可选的 LicenseType 参数更新了以下 cmdlet</span><span class="sxs-lookup"><span data-stu-id="26203-127">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="26203-128">New-AzureRmSqlDatabase；Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="26203-128">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="26203-129">New-AzureRmSqlElasticPool；Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="26203-129">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="26203-130">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="26203-130">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="26203-131">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="26203-131">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="26203-132">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="26203-132">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="26203-133">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="26203-133">AzureRM.Websites</span></span>
* <span data-ttu-id="26203-134">更新了“New-AzureRMWebApp”，可以使用策略库中的常用算法。</span><span class="sxs-lookup"><span data-stu-id="26203-134">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="26203-135">6.1.0 - 2018 年 5 月</span><span class="sxs-lookup"><span data-stu-id="26203-135">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="26203-136">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="26203-136">AzureRM.Profile</span></span>
* <span data-ttu-id="26203-137">修复了运行“Clear-AzureRmContext”时会保留空上下文的问题，该上下文使用旧的默认上下文的名称，导致用户无法使用旧名称创建新的上下文</span><span class="sxs-lookup"><span data-stu-id="26203-137">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="26203-138">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="26203-138">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="26203-139">允许在 AS 上执行网关的关联/取消关联操作。</span><span class="sxs-lookup"><span data-stu-id="26203-139">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="26203-140">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="26203-140">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="26203-141">增加了对 ApiVersions、ApiReleases 和 ApiRevisions 的支持</span><span class="sxs-lookup"><span data-stu-id="26203-141">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="26203-142">增加了对 ServiceFabric 后端的支持</span><span class="sxs-lookup"><span data-stu-id="26203-142">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="26203-143">增加了对 Application Insights Logger 的支持</span><span class="sxs-lookup"><span data-stu-id="26203-143">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="26203-144">增加的支持包括认可“基本”SKU 是 API 管理服务的有效 SKU</span><span class="sxs-lookup"><span data-stu-id="26203-144">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="26203-145">增加的支持包括允许将专用 CA 颁发的证书作为根证书或 CA 证书安装</span><span class="sxs-lookup"><span data-stu-id="26203-145">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="26203-146">增加的支持包括通过 KeyVault 和多个代理主机名接受自定义 SSL 证书</span><span class="sxs-lookup"><span data-stu-id="26203-146">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="26203-147">增加了对 MSI 标识的支持</span><span class="sxs-lookup"><span data-stu-id="26203-147">Added support for MSI identity</span></span>
* <span data-ttu-id="26203-148">增加的支持包括通过 URL 接受策略 注意：以下 cmdlet 将在未来版本中弃用</span><span class="sxs-lookup"><span data-stu-id="26203-148">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="26203-149">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="26203-149">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="26203-150">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="26203-150">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="26203-151">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="26203-151">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="26203-152">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="26203-152">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="26203-153">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="26203-153">AzureRM.Batch</span></span>
* <span data-ttu-id="26203-154">发布新 cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="26203-154">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="26203-155">发布新 cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="26203-155">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="26203-156">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="26203-156">AzureRM.Consumption</span></span>
* <span data-ttu-id="26203-157">在 Cmdlet Get-AzureRmConsumptionUsageDetail 中增加了新参数 Expand、ResourceGroup、InstanceName、InstanceId、Tags、Top</span><span class="sxs-lookup"><span data-stu-id="26203-157">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="26203-158">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="26203-158">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="26203-159">修复了 Export-AzureRmDataLakeStoreChildItemProperties 的示例</span><span class="sxs-lookup"><span data-stu-id="26203-159">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="26203-160">修复了 Set-AzureRmDataLakeStoreItemAclEntry 中 Recurse 用例的 null 参数异常</span><span class="sxs-lookup"><span data-stu-id="26203-160">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="26203-161">修复了 Set-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAcl、Remove-AzureRmDataLakeStoreItemAclEntry 的帮助文件</span><span class="sxs-lookup"><span data-stu-id="26203-161">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="26203-162">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="26203-162">AzureRM.Network</span></span>
* <span data-ttu-id="26203-163">将网络 SDK 版本从 18.0.0-preview 升至 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="26203-163">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="26203-164">增加了用于创建协议配置的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="26203-164">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="26203-165">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="26203-165">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="26203-166">增加了用于向现有的快速路由线路添加新的线路连接的 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="26203-166">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="26203-167">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="26203-167">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="26203-168">增加了用于从现有的快速路由线路删除线路连接的 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="26203-168">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="26203-169">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="26203-169">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="26203-170">增加了用于检索线路连接的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="26203-170">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="26203-171">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="26203-171">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="26203-172">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="26203-172">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="26203-173">修复了使用生成的证书进行服务器身份验证的问题（问题 5998）</span><span class="sxs-lookup"><span data-stu-id="26203-173">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="26203-174">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="26203-174">AzureRM.Sql</span></span>
* <span data-ttu-id="26203-175">更新了审核 cmdlet，允许删除 AuditActions 或 AuditActionGroups</span><span class="sxs-lookup"><span data-stu-id="26203-175">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="26203-176">修复了设置新的灵活保留策略时使用 Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy 出现的问题。该问题的具体表现是：在命令失败的同时，出现“不再支持使用 Azure 恢复服务保管库和策略配置长期保留策略。</span><span class="sxs-lookup"><span data-stu-id="26203-176">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="26203-177">请使用新的灵活保留策略提交请求”错误消息。</span><span class="sxs-lookup"><span data-stu-id="26203-177">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="26203-178">更新了与 Azure SQL 数据库/ElasticPool 的创建/更新相关的所有 cmdlet，允许使用新的数据库 API，而这些 cmdlet 支持的 SKU 属性则适用于规模和层相关属性。</span><span class="sxs-lookup"><span data-stu-id="26203-178">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="26203-179">更新的 cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="26203-179">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="26203-180">New-AzureRmSqlDatabase；Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="26203-180">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="26203-181">New-AzureRmSqlElasticPool；Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="26203-181">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="26203-182">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="26203-182">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="26203-183">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="26203-183">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="26203-184">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="26203-184">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="26203-185">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="26203-185">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="26203-186">更新了“Get-AzureRmTrafficManagerProfile”的参数，要求在使用 -Name 参数时使用 -ResourceGroupName 参数。</span><span class="sxs-lookup"><span data-stu-id="26203-186">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>