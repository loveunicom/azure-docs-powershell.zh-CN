---
title: Azure PowerShell 更改日志 | Microsoft Docs
description: 下面提供了对 Azure PowerShell 最新版本所做更改的历史记录。
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 5/1/2018
ms.openlocfilehash: 0b7902155c47f2e6355e9147c203867288caab81
ms.sourcegitcommit: 5971c92cb023bdd1d71fa2ad0a3b378abfbd092a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/23/2018
---
# <a name="release-notes"></a><span data-ttu-id="412e5-103">发行说明</span><span class="sxs-lookup"><span data-stu-id="412e5-103">Release notes</span></span>

<span data-ttu-id="412e5-104">下面是此版本中对 Azure PowerShell 所做的更改列表。</span><span class="sxs-lookup"><span data-stu-id="412e5-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="610---may-2018"></a><span data-ttu-id="412e5-105">6.1.0 - 2018 年 5 月</span><span class="sxs-lookup"><span data-stu-id="412e5-105">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="412e5-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="412e5-106">AzureRM.Profile</span></span>
* <span data-ttu-id="412e5-107">修复了运行“Clear-AzureRmContext”时会保留空上下文的问题，该上下文使用旧的默认上下文的名称，导致用户无法使用旧名称创建新的上下文</span><span class="sxs-lookup"><span data-stu-id="412e5-107">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="412e5-108">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="412e5-108">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="412e5-109">允许在 AS 上执行网关的关联/取消关联操作。</span><span class="sxs-lookup"><span data-stu-id="412e5-109">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="412e5-110">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="412e5-110">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="412e5-111">增加了对 ApiVersions、ApiReleases 和 ApiRevisions 的支持</span><span class="sxs-lookup"><span data-stu-id="412e5-111">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="412e5-112">增加了对 ServiceFabric 后端的支持</span><span class="sxs-lookup"><span data-stu-id="412e5-112">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="412e5-113">增加了对 Application Insights Logger 的支持</span><span class="sxs-lookup"><span data-stu-id="412e5-113">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="412e5-114">增加的支持包括认可“基本”SKU 是 API 管理服务的有效 SKU</span><span class="sxs-lookup"><span data-stu-id="412e5-114">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="412e5-115">增加的支持包括允许将专用 CA 颁发的证书作为根证书或 CA 证书安装</span><span class="sxs-lookup"><span data-stu-id="412e5-115">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="412e5-116">增加的支持包括通过 KeyVault 和多个代理主机名接受自定义 SSL 证书</span><span class="sxs-lookup"><span data-stu-id="412e5-116">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="412e5-117">增加了对 MSI 标识的支持</span><span class="sxs-lookup"><span data-stu-id="412e5-117">Added support for MSI identity</span></span>
* <span data-ttu-id="412e5-118">增加的支持包括通过 URL 接受策略 注意：以下 cmdlet 将在未来版本中弃用</span><span class="sxs-lookup"><span data-stu-id="412e5-118">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="412e5-119">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="412e5-119">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="412e5-120">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="412e5-120">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="412e5-121">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="412e5-121">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="412e5-122">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="412e5-122">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="412e5-123">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="412e5-123">AzureRM.Batch</span></span>
* <span data-ttu-id="412e5-124">发布新 cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="412e5-124">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="412e5-125">发布新 cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="412e5-125">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="412e5-126">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="412e5-126">AzureRM.Consumption</span></span>
* <span data-ttu-id="412e5-127">在 Cmdlet Get-AzureRmConsumptionUsageDetail 中增加了新参数 Expand、ResourceGroup、InstanceName、InstanceId、Tags、Top</span><span class="sxs-lookup"><span data-stu-id="412e5-127">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="412e5-128">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="412e5-128">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="412e5-129">修复了 Export-AzureRmDataLakeStoreChildItemProperties 的示例</span><span class="sxs-lookup"><span data-stu-id="412e5-129">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="412e5-130">修复了 Set-AzureRmDataLakeStoreItemAclEntry 中 Recurse 用例的 null 参数异常</span><span class="sxs-lookup"><span data-stu-id="412e5-130">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="412e5-131">修复了 Set-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAcl、Remove-AzureRmDataLakeStoreItemAclEntry 的帮助文件</span><span class="sxs-lookup"><span data-stu-id="412e5-131">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="412e5-132">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="412e5-132">AzureRM.Network</span></span>
* <span data-ttu-id="412e5-133">将网络 SDK 版本从 18.0.0-preview 升至 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="412e5-133">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="412e5-134">增加了用于创建协议配置的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="412e5-134">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="412e5-135">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="412e5-135">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="412e5-136">增加了用于向现有的快速路由线路添加新的线路连接的 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="412e5-136">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="412e5-137">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="412e5-137">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="412e5-138">增加了用于从现有的快速路由线路删除线路连接的 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="412e5-138">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="412e5-139">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="412e5-139">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="412e5-140">增加了用于检索线路连接的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="412e5-140">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="412e5-141">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="412e5-141">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="412e5-142">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="412e5-142">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="412e5-143">修复了使用生成的证书进行服务器身份验证的问题（问题 5998）</span><span class="sxs-lookup"><span data-stu-id="412e5-143">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="412e5-144">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="412e5-144">AzureRM.Sql</span></span>
* <span data-ttu-id="412e5-145">更新了审核 cmdlet，允许删除 AuditActions 或 AuditActionGroups</span><span class="sxs-lookup"><span data-stu-id="412e5-145">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="412e5-146">修复了设置新的灵活保留策略时使用 Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy 出现的问题。该问题的具体表现是：在命令失败的同时，出现“不再支持使用 Azure 恢复服务保管库和策略配置长期保留策略。</span><span class="sxs-lookup"><span data-stu-id="412e5-146">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="412e5-147">请使用新的灵活保留策略提交请求”错误消息。</span><span class="sxs-lookup"><span data-stu-id="412e5-147">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="412e5-148">更新了与 Azure SQL 数据库/ElasticPool 的创建/更新相关的所有 cmdlet，允许使用新的数据库 API，而这些 cmdlet 支持的 SKU 属性则适用于规模和层相关属性。</span><span class="sxs-lookup"><span data-stu-id="412e5-148">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="412e5-149">更新的 cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="412e5-149">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="412e5-150">New-AzureRmSqlDatabase；Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="412e5-150">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="412e5-151">New-AzureRmSqlElasticPool；Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="412e5-151">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="412e5-152">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="412e5-152">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="412e5-153">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="412e5-153">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="412e5-154">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="412e5-154">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="412e5-155">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="412e5-155">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="412e5-156">更新了“Get-AzureRmTrafficManagerProfile”的参数，要求在使用 -Name 参数时使用 -ResourceGroupName 参数。</span><span class="sxs-lookup"><span data-stu-id="412e5-156">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>