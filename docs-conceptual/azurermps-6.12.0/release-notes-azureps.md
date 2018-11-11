---
title: Azure PowerShell 更改日志 | Microsoft Docs
description: 下面提供了对 Azure PowerShell 最新版本所做更改的历史记录。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 08/28/2018
ms.openlocfilehash: 8a7b184ed06eb078956229fa67d02840014e3aaf
ms.sourcegitcommit: ac4b53bb42a25aae013a9d8cd9ae98ada9397274
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/08/2018
ms.locfileid: "51275514"
---
# <a name="release-notes"></a><span data-ttu-id="c1222-103">发行说明</span><span class="sxs-lookup"><span data-stu-id="c1222-103">Release notes</span></span>

<span data-ttu-id="c1222-104">下面是此版本中对 Azure PowerShell 所做的更改列表。</span><span class="sxs-lookup"><span data-stu-id="c1222-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="6120---november-2018"></a><span data-ttu-id="c1222-105">6.12.0 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="c1222-105">6.12.0 - November 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="c1222-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c1222-106">AzureRM.Profile</span></span>
* <span data-ttu-id="c1222-107">更新通用代码以使用最新版本的 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="c1222-107">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="c1222-108">将 Connect-AzureRmAccount cmdlet 中的 TenantId 参数重命名为 Tenant，并为 TenantId 添加别名</span><span class="sxs-lookup"><span data-stu-id="c1222-108">Rename param TenantId in cmdlet Connect-AzureRmAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="c1222-109">更新了 Connect-AzureRmAccount 的 TenantId 说明</span><span class="sxs-lookup"><span data-stu-id="c1222-109">Updated TenantId description for Connect-AzureRmAccount</span></span>
* <span data-ttu-id="c1222-110">修复了在提供租户域时失败的登录的错误消息</span><span class="sxs-lookup"><span data-stu-id="c1222-110">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="c1222-111">为租户中没有订阅的帐户修复了上下文名称冲突的问题</span><span class="sxs-lookup"><span data-stu-id="c1222-111">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="c1222-112">修复了在使用 MSI 时的 DataLake 终结点问题</span><span class="sxs-lookup"><span data-stu-id="c1222-112">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="c1222-113">修复了在未连接时会引发“Disconnect-AzureRmAccount”的问题</span><span class="sxs-lookup"><span data-stu-id="c1222-113">Fix issue where 'Disconnect-AzureRmAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azurermautomation"></a><span data-ttu-id="c1222-114">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="c1222-114">AzureRM.Automation</span></span>
* <span data-ttu-id="c1222-115">已将 cmdlet DLL 文件名重命名为 Microsoft.Azure.Commands.Automation.dll</span><span class="sxs-lookup"><span data-stu-id="c1222-115">Renamed cmdlet DLL filename to Microsoft.Azure.Commands.Automation.dll</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="c1222-116">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c1222-116">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="c1222-117">添加了 Get-AzureRmCognitiveServicesAccountSkus 操作。</span><span class="sxs-lookup"><span data-stu-id="c1222-117">Add Get-AzureRmCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="c1222-118">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c1222-118">AzureRM.Compute</span></span>
* <span data-ttu-id="c1222-119">添加了 Add-AzureRmVmssVMDataDisk 和 Remove-AzureRmVmssVMDataDisk cmdlet</span><span class="sxs-lookup"><span data-stu-id="c1222-119">Add Add-AzureRmVmssVMDataDisk and Remove-AzureRmVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="c1222-120">Get-AzureRmVMImage 显示 AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="c1222-120">Get-AzureRmVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="c1222-121">修复了 SetAzureRmVMChefExtension BootstrapOptions 和 -JsonAttribute 选项值未以 json 格式设置的问题。</span><span class="sxs-lookup"><span data-stu-id="c1222-121">Fixed SetAzureRmVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="c1222-122">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c1222-122">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="c1222-123">将 DataLake 程序包更新至 1.1.10。</span><span class="sxs-lookup"><span data-stu-id="c1222-123">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="c1222-124">将默认并发添加到多线程操作。</span><span class="sxs-lookup"><span data-stu-id="c1222-124">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="c1222-125">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="c1222-125">AzureRM.Insights</span></span>
* <span data-ttu-id="c1222-126">修复了问题 #7267（自动缩放区域）</span><span class="sxs-lookup"><span data-stu-id="c1222-126">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="c1222-127">创建新的自动缩放规则时未正确设置枚举的参数（始终将它们设置为默认值）的问题。</span><span class="sxs-lookup"><span data-stu-id="c1222-127">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="c1222-128">修复了问题 #7513 [见解] Set-AzureRMDiagnosticSetting 在创建设置期间需要显式指定类别</span><span class="sxs-lookup"><span data-stu-id="c1222-128">Fixed issue #7513 [Insights] Set-AzureRMDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="c1222-129">现在该 cmdlet 不需要在创建期间显式指示要启用的类别，即它会按记录工作</span><span class="sxs-lookup"><span data-stu-id="c1222-129">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="c1222-130">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c1222-130">AzureRM.Network</span></span>
* <span data-ttu-id="c1222-131">已将 PeeringType 更改为以下 cmdlet 的必需参数：</span><span class="sxs-lookup"><span data-stu-id="c1222-131">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="c1222-132">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="c1222-132">Get-AzureRmExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="c1222-133">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="c1222-133">Get-AzureRmExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="c1222-134">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="c1222-134">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="c1222-135">Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="c1222-135">Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="c1222-136">Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="c1222-136">Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="c1222-137">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="c1222-137">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="c1222-138">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="c1222-138">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="c1222-139">添加了策略修正 cmdlet</span><span class="sxs-lookup"><span data-stu-id="c1222-139">Added policy remediation cmdlets</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="c1222-140">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="c1222-140">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="c1222-141">添加了对恢复服务中 azure 文件共享的支持。</span><span class="sxs-lookup"><span data-stu-id="c1222-141">Added support for azure file shares in recovery services.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="c1222-142">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="c1222-142">AzureRM.Resources</span></span>
* <span data-ttu-id="c1222-143">https://github.com/Azure/azure-powershell/issues/7402 的修复</span><span class="sxs-lookup"><span data-stu-id="c1222-143">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="c1222-144">允许对“Get-AzureRmResource”使用“-ResourceId”参数来列出资源</span><span class="sxs-lookup"><span data-stu-id="c1222-144">Allow listing resources using the '-ResourceId' parameter for 'Get-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="c1222-145">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c1222-145">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="c1222-146">为 PSServiceBusMigrationConfigurationAttributes 添加了 MigrationState 只读属性，这将有助于了解迁移状态。</span><span class="sxs-lookup"><span data-stu-id="c1222-146">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="c1222-147">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c1222-147">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="c1222-148">修复了将证书添加到 Linux Vmss 的问题。</span><span class="sxs-lookup"><span data-stu-id="c1222-148">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="c1222-149">修复了“Add-AzureRmServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="c1222-149">Fix 'Add-AzureRmServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="c1222-150">使用来自新证书的正确指纹 (Azure/service-fabric-issues#932)。</span><span class="sxs-lookup"><span data-stu-id="c1222-150">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="c1222-151">正确显示异常 (Azure/service-fabric-issues#1054)。</span><span class="sxs-lookup"><span data-stu-id="c1222-151">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="c1222-152">修复了“Update-AzureRmServiceFabricDurability”以在开始 Vmss CreateOrUpdate 操作之前更新群集配置。</span><span class="sxs-lookup"><span data-stu-id="c1222-152">Fix 'Update-AzureRmServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="6110---october-2018"></a><span data-ttu-id="c1222-153">6.11.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="c1222-153">6.11.0 - October 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="c1222-154">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c1222-154">AzureRM.Profile</span></span>
* <span data-ttu-id="c1222-155">修复了 CloudShell 中 Get-AzureRmSubscription 的问题</span><span class="sxs-lookup"><span data-stu-id="c1222-155">Fix issue with Get-AzureRmSubscription in CloudShell</span></span>
* <span data-ttu-id="c1222-156">更新通用代码以使用最新版本的 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="c1222-156">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="c1222-157">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="c1222-157">AzureRM.Backup</span></span>
* <span data-ttu-id="c1222-158">已弃用 Azure 备份 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c1222-158">Deprecated Azure Backup cmdlets.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="c1222-159">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c1222-159">AzureRM.Compute</span></span>
* <span data-ttu-id="c1222-160">向 VM 大小的允许列表添加了新的大小，这样就可以在将简单的参数集用于“New-AzureRmVm”时为这些大小启用加速网络</span><span class="sxs-lookup"><span data-stu-id="c1222-160">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzureRmVm'</span></span>
* <span data-ttu-id="c1222-161">向所有 cmdlet 添加了 ResourceName 参数补全选项。</span><span class="sxs-lookup"><span data-stu-id="c1222-161">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="c1222-162">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c1222-162">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="c1222-163">添加虚拟网络规则的支持</span><span class="sxs-lookup"><span data-stu-id="c1222-163">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="c1222-164">Get-AzureRmDataLakeStoreVirtualNetworkRule：获取或列出 Azure Data Lake Store 虚拟网络规则。</span><span class="sxs-lookup"><span data-stu-id="c1222-164">Get-AzureRmDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="c1222-165">Add-AzureRmDataLakeStoreVirtualNetworkRule：向指定的 Data Lake Store 帐户添加虚拟网络规则。</span><span class="sxs-lookup"><span data-stu-id="c1222-165">Add-AzureRmDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="c1222-166">Set-AzureRmDataLakeStoreVirtualNetworkRule：在指定的 Data Lake Store 帐户中修改指定的虚拟网络规则。</span><span class="sxs-lookup"><span data-stu-id="c1222-166">Set-AzureRmDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="c1222-167">Remove-AzureRmDataLakeStoreVirtualNetworkRule：删除 Azure Data Lake Store 虚拟网络规则。</span><span class="sxs-lookup"><span data-stu-id="c1222-167">Remove-AzureRmDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="c1222-168">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c1222-168">AzureRM.Network</span></span>
* <span data-ttu-id="c1222-169">更新 cmdlet Test-AzureRmNetworkWatcherConnectivity，向后端传递协议值。</span><span class="sxs-lookup"><span data-stu-id="c1222-169">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="c1222-170">向所有 cmdlet 添加了 ResourceName 参数补全选项。</span><span class="sxs-lookup"><span data-stu-id="c1222-170">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="c1222-171">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="c1222-171">AzureRM.Resources</span></span>
* <span data-ttu-id="c1222-172">通过在方案中添加一个有意义的异常，修复了 Get-AzureRMRoleDefinition 在默认配置文件中没有订阅且未指定范围的情况下引发难以理解异常的问题。</span><span class="sxs-lookup"><span data-stu-id="c1222-172">Fix isssue where Get-AzureRMRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="c1222-173">另外，已将默认参数集设置为“RoleDefinitionNameParameterSet”。</span><span class="sxs-lookup"><span data-stu-id="c1222-173">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="6100---october-2018"></a><span data-ttu-id="c1222-174">6.10.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="c1222-174">6.10.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="c1222-175">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="c1222-175">Azure.Storage</span></span>
* <span data-ttu-id="c1222-176">修复了 Copy Blob/File 在目标有元数据问题时不会复制元数据的问题</span><span class="sxs-lookup"><span data-stu-id="c1222-176">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="c1222-177">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="c1222-177">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="c1222-178">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="c1222-178">Start-AzureStorageFileCopy</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="c1222-179">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c1222-179">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="c1222-180">在没有现有帐户的情况下支持 Get-AzureRmCognitiveServicesAccountSkus。</span><span class="sxs-lookup"><span data-stu-id="c1222-180">Support Get-AzureRmCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="c1222-181">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c1222-181">AzureRM.Compute</span></span>
* <span data-ttu-id="c1222-182">修复了 Get-AzureRmVM -ResourceGroupName <rg>，以在需要时返回超过 50 个结果</span><span class="sxs-lookup"><span data-stu-id="c1222-182">Fix Get-AzureRmVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="c1222-183">在 New-AzureRmVmss cmdlet 帮助中添加了“SimpleParameterSet”的示例。</span><span class="sxs-lookup"><span data-stu-id="c1222-183">Added an example of the 'SimpleParameterSet' to New-AzureRmVmss cmdlet help.</span></span>
* <span data-ttu-id="c1222-184">修复了 Azure 磁盘加密进度消息中的拼写错误</span><span class="sxs-lookup"><span data-stu-id="c1222-184">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="c1222-185">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="c1222-185">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="c1222-186">将 ADF .Net SDK 版本更新为 2.3.0。</span><span class="sxs-lookup"><span data-stu-id="c1222-186">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="c1222-187">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c1222-187">AzureRM.Network</span></span>
* <span data-ttu-id="c1222-188">添加了 NetworkProfile 功能。</span><span class="sxs-lookup"><span data-stu-id="c1222-188">Added NetworkProfile functionality.</span></span> <span data-ttu-id="c1222-189">添加了新 cmdlet</span><span class="sxs-lookup"><span data-stu-id="c1222-189">new cmdlets added</span></span>
    - <span data-ttu-id="c1222-190">Get-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c1222-190">Get-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="c1222-191">New-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c1222-191">New-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="c1222-192">Remove-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c1222-192">Remove-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="c1222-193">Set-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c1222-193">Set-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="c1222-194">New-AzureRMContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="c1222-194">New-AzureRMContainerNicConfig</span></span>
    - <span data-ttu-id="c1222-195">New-AzureRmContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="c1222-195">New-AzureRmContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="c1222-196">在子网模型上添加了服务关联链接</span><span class="sxs-lookup"><span data-stu-id="c1222-196">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="c1222-197">添加了 cmdlet New-AzureRmVirtualNetworkTap、Get-AzureRmVirtualNetworkTap、Set-AzureRmVirtualNetworkTap、Remove-AzureRmVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="c1222-197">Added cmdlet New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap</span></span>
* <span data-ttu-id="c1222-198">添加了 cmdlet Set-AzureRmNEtworkInterfaceTapConfig、Get-AzureRmNEtworkInterfaceTapConfig、Remove-AzureRmNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="c1222-198">Added cmdlet Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="c1222-199">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="c1222-199">AzureRM.RedisCache</span></span>
* <span data-ttu-id="c1222-200">今后允许任何字符串作为 Size 参数。</span><span class="sxs-lookup"><span data-stu-id="c1222-200">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="c1222-201">在 PSArgumentCompleter 弹出窗口中添加了 P5</span><span class="sxs-lookup"><span data-stu-id="c1222-201">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="c1222-202">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="c1222-202">AzureRM.Resources</span></span>
* <span data-ttu-id="c1222-203">将缺少的 -Mode 参数添加到 Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c1222-203">Add missing -Mode parameter to Set-AzureRmPolicyDefinition</span></span>
* <span data-ttu-id="c1222-204">对于使用包含用户的源的操作，修复了 Get-AzureRmProviderOperation commandlet bug</span><span class="sxs-lookup"><span data-stu-id="c1222-204">Fix Get-AzureRmProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="c1222-205">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="c1222-205">AzureRM.Sql</span></span>
* <span data-ttu-id="c1222-206">修复了某些备份 cmdlet 无法识别当前 azure 订阅的问题</span><span class="sxs-lookup"><span data-stu-id="c1222-206">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="c1222-207">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="c1222-207">AzureRM.Storage</span></span>
* <span data-ttu-id="c1222-208">支持获取特定位置的存储资源使用情况，并对于获取的全局存储资源使用情况已过时添加警告消息。</span><span class="sxs-lookup"><span data-stu-id="c1222-208">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="c1222-209">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="c1222-209">Get-AzureRmStorageUsage</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="c1222-210">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="c1222-210">AzureRM.Websites</span></span>
* <span data-ttu-id="c1222-211">新 Cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl - 获取容器持续部署 Webhook URL</span><span class="sxs-lookup"><span data-stu-id="c1222-211">New Cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="c1222-212">新 Cmdlet New-AzureRMWebAppContainerPSSession 和 Enter-WebAppContainerPSSession - 在 Windows 容器应用中启动 PowerShell 远程会话</span><span class="sxs-lookup"><span data-stu-id="c1222-212">New Cmdlets New-AzureRMWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="690---september-2018"></a><span data-ttu-id="c1222-213">6.9.0 - 2018 年 9 月</span><span class="sxs-lookup"><span data-stu-id="c1222-213">6.9.0 - September 2018</span></span>
#### <a name="general"></a><span data-ttu-id="c1222-214">常规</span><span class="sxs-lookup"><span data-stu-id="c1222-214">General</span></span>
* <span data-ttu-id="c1222-215">AzureRM.SignalR 已添加到 AzureRM 汇总模块</span><span class="sxs-lookup"><span data-stu-id="c1222-215">AzureRM.SignalR was added to the AzureRM rollup module</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="c1222-216">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c1222-216">AzureRM.Profile</span></span>
* <span data-ttu-id="c1222-217">对存储常用代码进行了细微的更改</span><span class="sxs-lookup"><span data-stu-id="c1222-217">Minor changes to the storage common code</span></span>
* <span data-ttu-id="c1222-218">更新了帮助文件，使之包括完整参数类型。</span><span class="sxs-lookup"><span data-stu-id="c1222-218">Updated help files to include full parameter types.</span></span>
* <span data-ttu-id="c1222-219">已在 ServicePrincipalCertificateWithSubscriptionId 参数集中将 -ServicePrincipal 更改为非强制性项</span><span class="sxs-lookup"><span data-stu-id="c1222-219">Changed -ServicePrincipal to non-mandatory in the ServicePrincipalCertificateWithSubscriptionId parameter set</span></span> 

#### <a name="azurestorage"></a><span data-ttu-id="c1222-220">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="c1222-220">Azure.Storage</span></span>
* <span data-ttu-id="c1222-221">支持使用 OAuth 创建存储上下文。</span><span class="sxs-lookup"><span data-stu-id="c1222-221">Support create Storage Context with OAuth.</span></span> 
    - <span data-ttu-id="c1222-222">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="c1222-222">New-AzureStorageContext</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="c1222-223">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="c1222-223">AzureRM.Cdn</span></span>
* <span data-ttu-id="c1222-224">在 Cdn 定价 sku 中增加了 Standard_Microsoft。</span><span class="sxs-lookup"><span data-stu-id="c1222-224">Added Standard_Microsoft in Cdn pricing sku.</span></span> 

#### <a name="azurermcompute"></a><span data-ttu-id="c1222-225">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c1222-225">AzureRM.Compute</span></span>
* <span data-ttu-id="c1222-226">将 Keyvault 和存储的依赖项移到了常用依赖项中</span><span class="sxs-lookup"><span data-stu-id="c1222-226">Move dependencies on Keyvault and Storage to the common dependencies</span></span>
* <span data-ttu-id="c1222-227">增加了对 AEM cmdlet 的支持，可以使用更多的虚拟机大小</span><span class="sxs-lookup"><span data-stu-id="c1222-227">Add support for more virutal machine sizes to AEM cmdlets</span></span>
* <span data-ttu-id="c1222-228">为 New-AzureRmVmssIpConfig 增加了 PublicIPPrefix 参数</span><span class="sxs-lookup"><span data-stu-id="c1222-228">Add PublicIPPrefix parameter to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="c1222-229">为 Invoke-AzureRmVMRunCommand cmdelt 增加了 ResourceId 参数</span><span class="sxs-lookup"><span data-stu-id="c1222-229">Add ResourceId parameter to Invoke-AzureRmVMRunCommand cmdelt</span></span>
* <span data-ttu-id="c1222-230">增加了 Invoke-AzureRmVmssVMRunCommand cmdlet</span><span class="sxs-lookup"><span data-stu-id="c1222-230">Add Invoke-AzureRmVmssVMRunCommand cmdlet</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="c1222-231">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="c1222-231">AzureRM.Dns</span></span>
* <span data-ttu-id="c1222-232">增加了在创建 dns 记录期间对别名记录的支持</span><span class="sxs-lookup"><span data-stu-id="c1222-232">Added support for alias record during dns record creation</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="c1222-233">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="c1222-233">AzureRM.Insights</span></span>
* <span data-ttu-id="c1222-234">修复了问题 #6833 和 #7102（诊断设置方面）</span><span class="sxs-lookup"><span data-stu-id="c1222-234">Fixed issues #6833 and #7102 (Diagnostic Settings area)</span></span>
    - <span data-ttu-id="c1222-235">在创建和列出/获取诊断设置期间出现的默认名称（即“service”）的问题</span><span class="sxs-lookup"><span data-stu-id="c1222-235">Issues with the default name, i.e. 'service', during creation and listing/getting of diagnostic settings</span></span>
    - <span data-ttu-id="c1222-236">通过类别创建诊断设置的问题</span><span class="sxs-lookup"><span data-stu-id="c1222-236">Issues creating diagnostic settings with categories</span></span>
* <span data-ttu-id="c1222-237">为指标时间粒度参数添加了弃用消息</span><span class="sxs-lookup"><span data-stu-id="c1222-237">Added deprecation message for metrics time grains parameters</span></span>
    - <span data-ttu-id="c1222-238">Timegrains 参数仍然会被接受（这是非重大变更），但在后端会被忽略，因为仅 PT1M 有效</span><span class="sxs-lookup"><span data-stu-id="c1222-238">Timegrains parameters are still being accepted (this is a non-breaking change,) but they are ignored in the backend since only PT1M is valid</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="c1222-239">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c1222-239">AzureRM.Network</span></span>
* <span data-ttu-id="c1222-240">更改了 LoadBalancer cmdlet</span><span class="sxs-lookup"><span data-stu-id="c1222-240">Changes to LoadBalancer cmdlets</span></span>
  - <span data-ttu-id="c1222-241">LoadBalancerInboundNatPoolConfig：增加了 IdleTimeoutInMinutes、EnableFloatingIp 和 EnableTcpReset 参数</span><span class="sxs-lookup"><span data-stu-id="c1222-241">LoadBalancerInboundNatPoolConfig: added parameters IdleTimeoutInMinutes, EnableFloatingIp and EnableTcpReset</span></span>
  - <span data-ttu-id="c1222-242">LoadBalancerInboundNatRuleConfig：增加了 EnableTcpReset 参数</span><span class="sxs-lookup"><span data-stu-id="c1222-242">LoadBalancerInboundNatRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="c1222-243">LoadBalancerRuleConfig：增加了 EnableTcpReset 参数</span><span class="sxs-lookup"><span data-stu-id="c1222-243">LoadBalancerRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="c1222-244">LoadBalancerProbeConfig：增加了对参数 Protocol 的“Https”值的支持</span><span class="sxs-lookup"><span data-stu-id="c1222-244">LoadBalancerProbeConfig: added support for value "Https" for parameter Protocol</span></span>
* <span data-ttu-id="c1222-245">为新 LoadBalancer 的子资源 OutboundRule 增加了新命令</span><span class="sxs-lookup"><span data-stu-id="c1222-245">Added new commands for new LoadBalancer's subresource OutboundRule</span></span>
  - <span data-ttu-id="c1222-246">Add-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c1222-246">Add-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="c1222-247">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c1222-247">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="c1222-248">New-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c1222-248">New-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="c1222-249">Set-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c1222-249">Set-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="c1222-250">Remove-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c1222-250">Remove-AzureRmLoadBalancerOutboundRuleConfig</span></span>
* <span data-ttu-id="c1222-251">为 PSNetworkInterface 增加了新的 HostedWorkloads 属性</span><span class="sxs-lookup"><span data-stu-id="c1222-251">Added new HostedWorkloads property for PSNetworkInterface</span></span>
* <span data-ttu-id="c1222-252">通过 ARM 为 Azure 防火墙功能增加了新的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="c1222-252">Added new cmdlets for feature: Azure Firewall via ARM</span></span>
  - <span data-ttu-id="c1222-253">增加了 Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="c1222-253">Added Get-AzureRmFirewall</span></span>
  - <span data-ttu-id="c1222-254">增加了 Set-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="c1222-254">Added Set-AzureRmFirewall</span></span>
  - <span data-ttu-id="c1222-255">增加了 New-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="c1222-255">Added New-AzureRmFirewall</span></span>
  - <span data-ttu-id="c1222-256">增加了 Remove-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="c1222-256">Added Remove-AzureRmFirewall</span></span>
  - <span data-ttu-id="c1222-257">增加了 New-AzureRmFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="c1222-257">Added New-AzureRmFirewallApplicationRuleCollection</span></span>
  - <span data-ttu-id="c1222-258">增加了 New-AzureRmFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="c1222-258">Added New-AzureRmFirewallApplicationRule</span></span>
  - <span data-ttu-id="c1222-259">增加了 New-AzureRmFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="c1222-259">Added New-AzureRmFirewallNatRuleCollection</span></span>
  - <span data-ttu-id="c1222-260">增加了 New-AzureRmFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="c1222-260">Added New-AzureRmFirewallNatRule</span></span>
  - <span data-ttu-id="c1222-261">增加了 New-AzureRmFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="c1222-261">Added New-AzureRmFirewallNetworkRuleCollection</span></span>
  - <span data-ttu-id="c1222-262">增加了 New-AzureRmFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="c1222-262">Added New-AzureRmFirewallNetworkRule</span></span>
* <span data-ttu-id="c1222-263">在应用程序网关中增加了对受信任根证书和自动缩放配置的支持</span><span class="sxs-lookup"><span data-stu-id="c1222-263">Added support for Trusted Root certificate and Autoscale configuration in Application Gateway</span></span>
  - <span data-ttu-id="c1222-264">增加了新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="c1222-264">New Cmdlets added:</span></span>
      - <span data-ttu-id="c1222-265">Add-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="c1222-265">Add-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="c1222-266">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="c1222-266">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="c1222-267">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="c1222-267">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="c1222-268">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="c1222-268">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="c1222-269">Set-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="c1222-269">Set-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="c1222-270">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="c1222-270">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="c1222-271">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="c1222-271">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="c1222-272">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="c1222-272">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="c1222-273">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="c1222-273">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
  - <span data-ttu-id="c1222-274">使用可选参数 -TrustedRootCertificate 更新了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c1222-274">Cmdlets updated with optonal parameter -TrustedRootCertificate</span></span>
      - <span data-ttu-id="c1222-275">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c1222-275">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="c1222-276">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c1222-276">Set-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="c1222-277">New-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="c1222-277">New-AzureRmApplicationGatewayBackendHttpSetting</span></span>
      - <span data-ttu-id="c1222-278">Set-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="c1222-278">Set-AzureRmApplicationGatewayBackendHttpSetting</span></span>
  - <span data-ttu-id="c1222-279">使用可选参数 -AutoscaleConfiguration 更新了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c1222-279">Cmdlets updated with optonal parameter -AutoscaleConfiguration</span></span>
      - <span data-ttu-id="c1222-280">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c1222-280">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="c1222-281">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c1222-281">Set-AzureRmApplicationGateway</span></span>
* <span data-ttu-id="c1222-282">为接口终结点增加了 cmdlet Get-AzureInterfaceEndpoint</span><span class="sxs-lookup"><span data-stu-id="c1222-282">Add cmdlet for Interface Endpoint Get-AzureInterfaceEndpoint</span></span>
* <span data-ttu-id="c1222-283">在子网中增加了对多个地址前缀的支持。</span><span class="sxs-lookup"><span data-stu-id="c1222-283">Added support for multiple address prefixes in a subnet.</span></span> <span data-ttu-id="c1222-284">更新了 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="c1222-284">Updated cmdlets:</span></span>
  - <span data-ttu-id="c1222-285">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="c1222-285">New-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="c1222-286">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="c1222-286">Set-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="c1222-287">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="c1222-287">Add-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="c1222-288">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="c1222-288">Get-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="c1222-289">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="c1222-289">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>
  - <span data-ttu-id="c1222-290">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="c1222-290">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="c1222-291">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="c1222-291">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="c1222-292">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="c1222-292">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="c1222-293">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c1222-293">Add-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="c1222-294">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c1222-294">New-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="c1222-295">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c1222-295">Set-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="c1222-296">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="c1222-296">Add-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="c1222-297">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="c1222-297">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="c1222-298">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="c1222-298">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="c1222-299">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="c1222-299">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="c1222-300">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="c1222-300">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="c1222-301">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="c1222-301">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="c1222-302">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="c1222-302">New-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="c1222-303">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="c1222-303">New-AzureRmNetworkInterface</span></span>
* <span data-ttu-id="c1222-304">增加了用于子网委派的 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c1222-304">Adding cmdlets for subnet delegation.</span></span>
  - <span data-ttu-id="c1222-305">New-AzureRmDelegation：创建一个可以添加到子网的新委派</span><span class="sxs-lookup"><span data-stu-id="c1222-305">New-AzureRmDelegation: Creates a new delegation, which can be added to a subnet</span></span>
  - <span data-ttu-id="c1222-306">Remove-AzureRmDelegation：获取一个子网，然后从该子网中删除提供的委派名称</span><span class="sxs-lookup"><span data-stu-id="c1222-306">Remove-AzureRmDelegation: Takes in a subnet and removes the provided delegation name from that subnet</span></span>
  - <span data-ttu-id="c1222-307">Add-AzureRmDelegation：获取一个子网，然后向该子网添加提供的服务名称作为委派</span><span class="sxs-lookup"><span data-stu-id="c1222-307">Add-AzureRmDelegation: Takes in a subnet and adds the provided service name as a delegation to that subnet</span></span>
  - <span data-ttu-id="c1222-308">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="c1222-308">Get-AzureRmDelegation</span></span>
  - <span data-ttu-id="c1222-309">Get-AzureRmAvailableServiceDelegations</span><span class="sxs-lookup"><span data-stu-id="c1222-309">Get-AzureRmAvailableServiceDelegations</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="c1222-310">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="c1222-310">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="c1222-311">支持托管磁盘</span><span class="sxs-lookup"><span data-stu-id="c1222-311">Support for managed Managed disk</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="c1222-312">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="c1222-312">AzureRM.RedisCache</span></span>
* <span data-ttu-id="c1222-313">更新了 Insights 依赖项。</span><span class="sxs-lookup"><span data-stu-id="c1222-313">Updated Insights dependency.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="c1222-314">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="c1222-314">AzureRM.Resources</span></span>
* <span data-ttu-id="c1222-315">使用新参数 RollbackAction 更新了 New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="c1222-315">Update New-AzureRmResourceGroupDeployment with new parameter RollbackAction</span></span>
    - <span data-ttu-id="c1222-316">使用新参数增加了对 OnErrorDeployment 的支持。</span><span class="sxs-lookup"><span data-stu-id="c1222-316">Add support for OnErrorDeployment with the new parameter.</span></span>
* <span data-ttu-id="c1222-317">在策略分配方面支持托管标识。</span><span class="sxs-lookup"><span data-stu-id="c1222-317">Support managed identity on policy assignments.</span></span>
* <span data-ttu-id="c1222-318">使用“New-AzureRmPolicyAssignment”来分配策略时，不再需要带默认值的参数</span><span class="sxs-lookup"><span data-stu-id="c1222-318">Parameters with default values are no longer requred when assigning a policy with 'New-AzureRmPolicyAssignment'</span></span>
* <span data-ttu-id="c1222-319">增加了新的 cmdlet Get-AzureRmPolicyAlias，用于检索策略别名</span><span class="sxs-lookup"><span data-stu-id="c1222-319">Add new cmdlet Get-AzureRmPolicyAlias for retrieving policy aliases</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="c1222-320">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c1222-320">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="c1222-321">修复了问题 #7161</span><span class="sxs-lookup"><span data-stu-id="c1222-321">Fixed issue #7161</span></span>

#### <a name="azurermsignalr"></a><span data-ttu-id="c1222-322">AzureRM.SignalR</span><span class="sxs-lookup"><span data-stu-id="c1222-322">AzureRM.SignalR</span></span>
* <span data-ttu-id="c1222-323">将 SKU 名称更新为 Free_F1 和 Standard_S1</span><span class="sxs-lookup"><span data-stu-id="c1222-323">Update SKU names to Free_F1 and Standard_S1</span></span>
* <span data-ttu-id="c1222-324">为 PSSignalRResource 对象增加了版本字段，为 PSSignalRKeys 对象增加了字符串。</span><span class="sxs-lookup"><span data-stu-id="c1222-324">Add version field to the PSSignalRResource object and connection string to the PSSignalRKeys object.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="c1222-325">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="c1222-325">AzureRM.Storage</span></span>
* <span data-ttu-id="c1222-326">在 AzureRm.Storage 中支持不可变性策略</span><span class="sxs-lookup"><span data-stu-id="c1222-326">Support Immutability Policy in AzureRm.Storage</span></span> 
    - <span data-ttu-id="c1222-327">Remove-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="c1222-327">Remove-AzureRmStorageAccountNetworkRule</span></span>
    - <span data-ttu-id="c1222-328">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="c1222-328">Get-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="c1222-329">Update-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="c1222-329">Update-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="c1222-330">New-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="c1222-330">New-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="c1222-331">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="c1222-331">Remove-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="c1222-332">Add-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="c1222-332">Add-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="c1222-333">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="c1222-333">Remove-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="c1222-334">Set-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="c1222-334">Set-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="c1222-335">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="c1222-335">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="c1222-336">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="c1222-336">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="c1222-337">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="c1222-337">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="c1222-338">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="c1222-338">AzureRM.Websites</span></span>
* <span data-ttu-id="c1222-339">增加了两个新的 cmdlet：Get-AzureRmDeletedWebApp 和 Restore-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="c1222-339">Added two new cmdlets: Get-AzureRmDeletedWebApp and Restore-AzureRmDeletedWebApp</span></span>
* <span data-ttu-id="c1222-340">增加了 New-AzureRmAppServicePlan -HyperV 开关，用于通过 Windows 容器创建应用服务计划</span><span class="sxs-lookup"><span data-stu-id="c1222-340">New-AzureRmAppServicePlan -HyperV switch is added for create app service plan with windows container</span></span>
* <span data-ttu-id="c1222-341">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - 增加了新参数 (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment)，用于创建和管理 Windows 容器应用</span><span class="sxs-lookup"><span data-stu-id="c1222-341">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - New parameters (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) added for creating and managing windows container app</span></span>

## <a name="681---august-2018"></a><span data-ttu-id="c1222-342">6.8.1 - 2018 年 8 月</span><span class="sxs-lookup"><span data-stu-id="c1222-342">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="c1222-343">常规</span><span class="sxs-lookup"><span data-stu-id="c1222-343">General</span></span>
* <span data-ttu-id="c1222-344">解决了未设置默认资源组的问题。</span><span class="sxs-lookup"><span data-stu-id="c1222-344">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="c1222-345">更新了公共运行时程序集</span><span class="sxs-lookup"><span data-stu-id="c1222-345">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="c1222-346">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c1222-346">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="c1222-347">解决了未设置默认资源组的问题。</span><span class="sxs-lookup"><span data-stu-id="c1222-347">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="c1222-348">修复了问题 https://github.com/Azure/azure-powershell/issues/6603</span><span class="sxs-lookup"><span data-stu-id="c1222-348">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="c1222-349">Import-AzureRmApiManagementApi 和 \*-AzureRmApiManagementCertificate cmdlet 现在处理相对路径</span><span class="sxs-lookup"><span data-stu-id="c1222-349">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="c1222-350">修复了问题 https://github.com/Azure/azure-powershell/issues/6879</span><span class="sxs-lookup"><span data-stu-id="c1222-350">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="c1222-351">CertificateInformation 是使 Set-AzureRmApiManagement cmdlet 可以正常工作的可设置属性。</span><span class="sxs-lookup"><span data-stu-id="c1222-351">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="c1222-352">通过升级到 4.0.4-preview nuget 进行了修复</span><span class="sxs-lookup"><span data-stu-id="c1222-352">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="c1222-353">修复了问题 https://github.com/Azure/azure-powershell/issues/6853</span><span class="sxs-lookup"><span data-stu-id="c1222-353">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="c1222-354">针对按产品名称进行的搜索修复了 Odata 筛选器</span><span class="sxs-lookup"><span data-stu-id="c1222-354">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="c1222-355">修复了问题 https://github.com/Azure/azure-powershell/issues/6814</span><span class="sxs-lookup"><span data-stu-id="c1222-355">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="c1222-356">针对按 API 名称进行的搜索修复了 Odata 筛选器</span><span class="sxs-lookup"><span data-stu-id="c1222-356">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="c1222-357">添加了对 AzureMonitor 记录器的支持</span><span class="sxs-lookup"><span data-stu-id="c1222-357">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="c1222-358">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c1222-358">AzureRM.Compute</span></span>
* <span data-ttu-id="c1222-359">解决了错误输出中缺少目标的问题。</span><span class="sxs-lookup"><span data-stu-id="c1222-359">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="c1222-360">解决了带有托管磁盘的 VM 的存储帐户类型问题</span><span class="sxs-lookup"><span data-stu-id="c1222-360">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="c1222-361">解决了未设置默认资源组的问题。</span><span class="sxs-lookup"><span data-stu-id="c1222-361">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="c1222-362">解决了在其他环境（例如 Azure 中国）中使用 AEM 扩展 cmdlet 的问题</span><span class="sxs-lookup"><span data-stu-id="c1222-362">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="c1222-363">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c1222-363">AzureRM.Network</span></span>
* <span data-ttu-id="c1222-364">将默认 cmdlet 输出表示形式更改为表视图</span><span class="sxs-lookup"><span data-stu-id="c1222-364">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="c1222-365">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="c1222-365">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="c1222-366">修复了在尝试扩展停用的容量时 Update-AzureRmPowerBIEmbeddedCapacity 中出现的故障</span><span class="sxs-lookup"><span data-stu-id="c1222-366">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="c1222-367">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="c1222-367">AzureRM.Resources</span></span>
* <span data-ttu-id="c1222-368">解决了从市场创建托管应用程序的问题。</span><span class="sxs-lookup"><span data-stu-id="c1222-368">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="c1222-369">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c1222-369">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="c1222-370">修复的问题</span><span class="sxs-lookup"><span data-stu-id="c1222-370">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="c1222-371">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="c1222-371">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="c1222-372">添加了对 MultiValue 路由方法的支持</span><span class="sxs-lookup"><span data-stu-id="c1222-372">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="c1222-373">MultiValue 路由的新参数“MaxReturn”</span><span class="sxs-lookup"><span data-stu-id="c1222-373">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="c1222-374">添加了对 Subnet 路由方法的支持</span><span class="sxs-lookup"><span data-stu-id="c1222-374">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="c1222-375">对终结点中的 IP 地址范围（子网）的支持</span><span class="sxs-lookup"><span data-stu-id="c1222-375">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="c1222-376">添加了对配置文件中的自定义标头的支持</span><span class="sxs-lookup"><span data-stu-id="c1222-376">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="c1222-377">添加了对配置文件中的预期状态代码范围的支持</span><span class="sxs-lookup"><span data-stu-id="c1222-377">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="c1222-378">添加了对终结点中的自定义标头的支持</span><span class="sxs-lookup"><span data-stu-id="c1222-378">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="c1222-379">6.8.0 - 2018 年 8 月</span><span class="sxs-lookup"><span data-stu-id="c1222-379">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="c1222-380">常规</span><span class="sxs-lookup"><span data-stu-id="c1222-380">General</span></span>
* <span data-ttu-id="c1222-381">解决了未设置默认资源组的问题。</span><span class="sxs-lookup"><span data-stu-id="c1222-381">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="c1222-382">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c1222-382">AzureRM.Profile</span></span>
* <span data-ttu-id="c1222-383">为在执行 Connect-AzureRmAccount 期间返回的令牌添加了“过期”属性</span><span class="sxs-lookup"><span data-stu-id="c1222-383">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="c1222-384">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c1222-384">AzureRM.Compute</span></span>
* <span data-ttu-id="c1222-385">解决了错误输出中缺少目标的问题。</span><span class="sxs-lookup"><span data-stu-id="c1222-385">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="c1222-386">解决了带有托管磁盘的 VM 的存储帐户类型问题</span><span class="sxs-lookup"><span data-stu-id="c1222-386">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="c1222-387">解决了在其他环境（例如 Azure 中国）中使用 AEM 扩展 cmdlet 的问题</span><span class="sxs-lookup"><span data-stu-id="c1222-387">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="c1222-388">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="c1222-388">AzureRM.IotHub</span></span>
* <span data-ttu-id="c1222-389">修复了 New-AzureRmIotHubExportDevices 和 New-AzureRmIotHubImportDevices的示例</span><span class="sxs-lookup"><span data-stu-id="c1222-389">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="c1222-390">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c1222-390">AzureRM.Network</span></span>
* <span data-ttu-id="c1222-391">将默认模型表示形式更改为表视图</span><span class="sxs-lookup"><span data-stu-id="c1222-391">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="c1222-392">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="c1222-392">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="c1222-393">修复了在尝试扩展停用的容量时 Update-AzureRmPowerBIEmbeddedCapacity 中出现的故障</span><span class="sxs-lookup"><span data-stu-id="c1222-393">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="c1222-394">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="c1222-394">AzureRM.Resources</span></span>
* <span data-ttu-id="c1222-395">解决了从市场创建托管应用程序的问题。</span><span class="sxs-lookup"><span data-stu-id="c1222-395">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="c1222-396">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c1222-396">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="c1222-397">解决了以下问题</span><span class="sxs-lookup"><span data-stu-id="c1222-397">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="c1222-398">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="c1222-398">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="c1222-399">对 MultiValue 路由方法的支持</span><span class="sxs-lookup"><span data-stu-id="c1222-399">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="c1222-400">MultiValue 路由的新参数“MaxReturn”</span><span class="sxs-lookup"><span data-stu-id="c1222-400">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="c1222-401">对 Subnet 路由方法的支持</span><span class="sxs-lookup"><span data-stu-id="c1222-401">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="c1222-402">对终结点中的 IP 地址范围（子网）的支持</span><span class="sxs-lookup"><span data-stu-id="c1222-402">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="c1222-403">对配置文件中的自定义标头的支持</span><span class="sxs-lookup"><span data-stu-id="c1222-403">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="c1222-404">对配置文件中的预期状态代码范围的支持</span><span class="sxs-lookup"><span data-stu-id="c1222-404">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="c1222-405">对终结点中的自定义标头的支持</span><span class="sxs-lookup"><span data-stu-id="c1222-405">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="c1222-406">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="c1222-406">AzureRM.Websites</span></span>
* <span data-ttu-id="c1222-407">解决了错误地设置默认资源组的问题。</span><span class="sxs-lookup"><span data-stu-id="c1222-407">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="c1222-408">6.7.0 - 2018 年 8 月</span><span class="sxs-lookup"><span data-stu-id="c1222-408">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="c1222-409">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c1222-409">AzureRM.Profile</span></span>
* <span data-ttu-id="c1222-410">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c1222-410">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="c1222-411">向默认的上下文名称添加用户 ID，避免上下文冲突</span><span class="sxs-lookup"><span data-stu-id="c1222-411">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="c1222-412">修复了 Clear-AzureRmContext 在选择上下文 #6398 时出现的问题</span><span class="sxs-lookup"><span data-stu-id="c1222-412">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="c1222-413">允许将租户域传递给“Connect-AzureRmAccount”的“-TenantId”参数</span><span class="sxs-lookup"><span data-stu-id="c1222-413">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="c1222-414">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="c1222-414">Azure.Storage</span></span>
* <span data-ttu-id="c1222-415">去除了 Azure 文件共享配额的 5TB 限制</span><span class="sxs-lookup"><span data-stu-id="c1222-415">Remove the 5TB limitation for Azure File Share quota</span></span>
* <span data-ttu-id="c1222-416">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="c1222-416">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="c1222-417">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="c1222-417">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="c1222-418">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c1222-418">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="c1222-419">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="c1222-419">Azure.AnalysisServices</span></span>
* <span data-ttu-id="c1222-420">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c1222-420">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="c1222-421">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c1222-421">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="c1222-422">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c1222-422">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="c1222-423">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="c1222-423">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="c1222-424">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c1222-424">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="c1222-425">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="c1222-425">AzureRM.Automation</span></span>
* <span data-ttu-id="c1222-426">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c1222-426">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="c1222-427">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="c1222-427">AzureRM.Backup</span></span>
* <span data-ttu-id="c1222-428">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c1222-428">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="c1222-429">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="c1222-429">AzureRM.Batch</span></span>
* <span data-ttu-id="c1222-430">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c1222-430">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="c1222-431">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="c1222-431">AzureRM.Billing</span></span>
* <span data-ttu-id="c1222-432">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c1222-432">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="c1222-433">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="c1222-433">AzureRM.Cdn</span></span>
* <span data-ttu-id="c1222-434">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c1222-434">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="c1222-435">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c1222-435">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="c1222-436">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c1222-436">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="c1222-437">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c1222-437">AzureRM.Compute</span></span>
* <span data-ttu-id="c1222-438">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c1222-438">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="c1222-439">为 New-AzureRmVmssConfig 增加了 EvictionPolicy 参数</span><span class="sxs-lookup"><span data-stu-id="c1222-439">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="c1222-440">在 New-AzureRmVm 的 DiskFileParameterSet 中使用默认位置（如果未指定 Location）</span><span class="sxs-lookup"><span data-stu-id="c1222-440">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="c1222-441">修复了 Save-AzureRmVMImage 中的参数说明</span><span class="sxs-lookup"><span data-stu-id="c1222-441">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="c1222-442">修复了某些单次传递相关方案的 Get-AzureRmVMDiskEncryptionStatus cmdlet</span><span class="sxs-lookup"><span data-stu-id="c1222-442">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="c1222-443">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="c1222-443">AzureRM.Consumption</span></span>
* <span data-ttu-id="c1222-444">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c1222-444">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="c1222-445">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="c1222-445">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="c1222-446">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c1222-446">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="c1222-447">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c1222-447">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="c1222-448">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c1222-448">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="c1222-449">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="c1222-449">AzureRM.DataFactories</span></span>
* <span data-ttu-id="c1222-450">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c1222-450">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="c1222-451">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="c1222-451">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="c1222-452">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c1222-452">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="c1222-453">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="c1222-453">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="c1222-454">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c1222-454">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="c1222-455">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c1222-455">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="c1222-456">修复了从 PowerShell 命令行设置 DebugPreference 时的调试问题</span><span class="sxs-lookup"><span data-stu-id="c1222-456">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="c1222-457">更新了 Set-AzureRmDataLakeStoreItemAcl 的示例</span><span class="sxs-lookup"><span data-stu-id="c1222-457">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="c1222-458">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c1222-458">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="c1222-459">更新了 Set-AzureRmDataLakeStoreItemAclEntry 的示例</span><span class="sxs-lookup"><span data-stu-id="c1222-459">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="c1222-460">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="c1222-460">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="c1222-461">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c1222-461">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="c1222-462">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="c1222-462">AzureRM.Dns</span></span>
* <span data-ttu-id="c1222-463">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c1222-463">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="c1222-464">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="c1222-464">AzureRM.EventGrid</span></span>
* <span data-ttu-id="c1222-465">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c1222-465">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="c1222-466">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="c1222-466">AzureRM.EventHub</span></span>
* <span data-ttu-id="c1222-467">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c1222-467">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="c1222-468">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="c1222-468">AzureRM.HDInsight</span></span>
* <span data-ttu-id="c1222-469">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c1222-469">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="c1222-470">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="c1222-470">AzureRM.Insights</span></span>
* <span data-ttu-id="c1222-471">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c1222-471">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="c1222-472">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="c1222-472">AzureRM.IotHub</span></span>
* <span data-ttu-id="c1222-473">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c1222-473">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="c1222-474">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c1222-474">AzureRM.KeyVault</span></span>
* <span data-ttu-id="c1222-475">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c1222-475">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="c1222-476">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="c1222-476">AzureRM.LogicApp</span></span>
* <span data-ttu-id="c1222-477">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c1222-477">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="c1222-478">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="c1222-478">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="c1222-479">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c1222-479">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="c1222-480">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="c1222-480">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="c1222-481">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c1222-481">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="c1222-482">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="c1222-482">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="c1222-483">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c1222-483">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="c1222-484">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="c1222-484">AzureRM.Media</span></span>
* <span data-ttu-id="c1222-485">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c1222-485">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="c1222-486">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c1222-486">AzureRM.Network</span></span>
* <span data-ttu-id="c1222-487">增加了 Set-AzureRmLocalNetworkGateway 的示例</span><span class="sxs-lookup"><span data-stu-id="c1222-487">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="c1222-488">增加了 Add-AzureRmVirtualNetworkGatewayIpConfig、Get-AzureRmVirtualNetworkGatewayConnectionSharedKey 和 New-AzureRmVirtualNetworkGatewayConnection 的示例和说明</span><span class="sxs-lookup"><span data-stu-id="c1222-488">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="c1222-489">增加了 Remove-AzureRmVirtualNetworkGatewayIpConfig 和 Reset-AzureRmVirtualNetworkGateway 的示例</span><span class="sxs-lookup"><span data-stu-id="c1222-489">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="c1222-490">增加了 Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey 的示例</span><span class="sxs-lookup"><span data-stu-id="c1222-490">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="c1222-491">增加了 Set-AzureRmVirtualNetworkGatewayConnectionSharedKey 的示例</span><span class="sxs-lookup"><span data-stu-id="c1222-491">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="c1222-492">增加了 Set-AzureRmVirtualNetworkGatewayConnection 的示例</span><span class="sxs-lookup"><span data-stu-id="c1222-492">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="c1222-493">使用最新的代码生成器重新生成了 ApplicationSecurityGroup、RouteTable 和 Usage 的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="c1222-493">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="c1222-494">阐明了在尝试获取的子网不存在时 Get-AzureRmVirtualNetworkSubnetConfig 的错误消息</span><span class="sxs-lookup"><span data-stu-id="c1222-494">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="c1222-495">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="c1222-495">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="c1222-496">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c1222-496">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="c1222-497">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="c1222-497">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="c1222-498">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c1222-498">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="c1222-499">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="c1222-499">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="c1222-500">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c1222-500">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="c1222-501">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="c1222-501">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="c1222-502">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c1222-502">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="c1222-503">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c1222-503">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="c1222-504">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c1222-504">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="c1222-505">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="c1222-505">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="c1222-506">为 Get-AzureRmRecoveryServicesBackItem cmdlet 增加了策略筛选器。</span><span class="sxs-lookup"><span data-stu-id="c1222-506">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="c1222-507">此命令返回受给定策略 ID 保护的备份项的列表。</span><span class="sxs-lookup"><span data-stu-id="c1222-507">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="c1222-508">已将 Microsoft.Azure.Management.RecoveryServices.Backup 更新到 3.0.0-preview 版本。</span><span class="sxs-lookup"><span data-stu-id="c1222-508">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="c1222-509">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c1222-509">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="c1222-510">为 Restore-AzureRmRecoveryServicesBackupItem 增加了 TargetResourceGroupName 参数。</span><span class="sxs-lookup"><span data-stu-id="c1222-510">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="c1222-511">托管磁盘还原到的资源组。</span><span class="sxs-lookup"><span data-stu-id="c1222-511">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="c1222-512">适用于包含托管磁盘的 VM 的备份。</span><span class="sxs-lookup"><span data-stu-id="c1222-512">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="c1222-513">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="c1222-513">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="c1222-514">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c1222-514">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="c1222-515">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="c1222-515">AzureRM.RedisCache</span></span>
* <span data-ttu-id="c1222-516">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c1222-516">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="c1222-517">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="c1222-517">AzureRM.Relay</span></span>
* <span data-ttu-id="c1222-518">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c1222-518">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="c1222-519">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="c1222-519">AzureRM.Resources</span></span>
* <span data-ttu-id="c1222-520">支持在订阅范围部署模板。</span><span class="sxs-lookup"><span data-stu-id="c1222-520">Support template deployment at subscription scope.</span></span> <span data-ttu-id="c1222-521">增加了新 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="c1222-521">Add new Cmdlets:</span></span>
    - <span data-ttu-id="c1222-522">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="c1222-522">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="c1222-523">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="c1222-523">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="c1222-524">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="c1222-524">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="c1222-525">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="c1222-525">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="c1222-526">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="c1222-526">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="c1222-527">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="c1222-527">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="c1222-528">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="c1222-528">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="c1222-529">修复了在将上下文传递给 Set-AzureRmResource 时引发错误的问题</span><span class="sxs-lookup"><span data-stu-id="c1222-529">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="c1222-530">修复了 New-AzureRmResourceGroupDeployment 中的示例</span><span class="sxs-lookup"><span data-stu-id="c1222-530">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="c1222-531">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c1222-531">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="c1222-532">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="c1222-532">AzureRM.Scheduler</span></span>
* <span data-ttu-id="c1222-533">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c1222-533">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="c1222-534">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c1222-534">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="c1222-535">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c1222-535">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="c1222-536">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c1222-536">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="c1222-537">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c1222-537">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="c1222-538">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="c1222-538">AzureRM.Sql</span></span>
* <span data-ttu-id="c1222-539">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c1222-539">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="c1222-540">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="c1222-540">AzureRM.Storage</span></span>
* <span data-ttu-id="c1222-541">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c1222-541">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="c1222-542">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="c1222-542">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="c1222-543">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c1222-543">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="c1222-544">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="c1222-544">AzureRM.Tags</span></span>
* <span data-ttu-id="c1222-545">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c1222-545">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="c1222-546">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="c1222-546">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="c1222-547">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c1222-547">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="c1222-548">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="c1222-548">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="c1222-549">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c1222-549">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="c1222-550">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="c1222-550">AzureRM.Websites</span></span>
* <span data-ttu-id="c1222-551">已更新到最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c1222-551">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="c1222-552">6.6.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="c1222-552">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="c1222-553">常规</span><span class="sxs-lookup"><span data-stu-id="c1222-553">General</span></span>
* <span data-ttu-id="c1222-554">更新了所有帮助文件，以包括完整参数类型和正确的输入/输出类型。</span><span class="sxs-lookup"><span data-stu-id="c1222-554">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="c1222-555">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c1222-555">AzureRM.Profile</span></span>
* <span data-ttu-id="c1222-556">更新了 Common.Strategy 库，以便能够验证资源的当前配置是否与目标资源兼容。</span><span class="sxs-lookup"><span data-stu-id="c1222-556">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="c1222-557">在 Common.Storage 中添加了 ps1xml 类型</span><span class="sxs-lookup"><span data-stu-id="c1222-557">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="c1222-558">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="c1222-558">Azure.Storage</span></span>
* <span data-ttu-id="c1222-559">增加了从 DefaultProfile 获取存储上下文的支持</span><span class="sxs-lookup"><span data-stu-id="c1222-559">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="c1222-560">为 cmdlet 输出类型属性增加了 Ps1XmlAttribute。</span><span class="sxs-lookup"><span data-stu-id="c1222-560">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="c1222-561">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c1222-561">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="c1222-562">修复了问题 https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="c1222-562">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="c1222-563">修复了 Automapper 中将 PsApiManagementApi 转换为 ApiContract 的 bug</span><span class="sxs-lookup"><span data-stu-id="c1222-563">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="c1222-564">修复了问题 https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="c1222-564">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="c1222-565">修复了 File.Save 中没有使用编码类型重载的 bug</span><span class="sxs-lookup"><span data-stu-id="c1222-565">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="c1222-566">修复了问题 https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="c1222-566">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="c1222-567">升级到了 4.0.3 Nuget版本，该版本修复了 apiId 上的模式异常</span><span class="sxs-lookup"><span data-stu-id="c1222-567">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="c1222-568">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c1222-568">AzureRM.Compute</span></span>
* <span data-ttu-id="c1222-569">修复因使用 PremiumLRS 存储帐户类型重命名而在 New-AzureRmVm 中使用 DiskFileParameterSet 创建 VM 失败的问题。</span><span class="sxs-lookup"><span data-stu-id="c1222-569">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="c1222-570">修复 Invoke-AzureRmVMRunCommand cmdlet</span><span class="sxs-lookup"><span data-stu-id="c1222-570">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="c1222-571">更新 Get-AzureRmAvailabilitySet 以启用列出订阅中的所有可用性集。</span><span class="sxs-lookup"><span data-stu-id="c1222-571">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="c1222-572">（ResouceGroupName 参数现在是可选的。）</span><span class="sxs-lookup"><span data-stu-id="c1222-572">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="c1222-573">更新“New-AzureRmVm”的 SimpleParameterSet 以在符合条件的 VM 上启用加速网络。</span><span class="sxs-lookup"><span data-stu-id="c1222-573">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="c1222-574">将 New-AzureRmVmss 简单参数集更新为在用户指定的 LB 已存在时创建 vmss 失败。</span><span class="sxs-lookup"><span data-stu-id="c1222-574">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="c1222-575">更新 New-AzureRmDisk 的示例</span><span class="sxs-lookup"><span data-stu-id="c1222-575">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="c1222-576">添加“New-AzureRmVM”的示例</span><span class="sxs-lookup"><span data-stu-id="c1222-576">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="c1222-577">更新 Set-AzureRmVMOSDisk 的说明</span><span class="sxs-lookup"><span data-stu-id="c1222-577">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="c1222-578">更新 Set-AzureRmVMBginfoExtension 的示例 1 以更正拼写和前缀。</span><span class="sxs-lookup"><span data-stu-id="c1222-578">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="c1222-579">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="c1222-579">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="c1222-580">将 ADF .Net SDK 版本更新为 1.1.0。</span><span class="sxs-lookup"><span data-stu-id="c1222-580">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="c1222-581">支持跨数据工厂的自承载集成运行时共享。</span><span class="sxs-lookup"><span data-stu-id="c1222-581">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="c1222-582">将新参数 -SharedIntegrationRuntimeResourceId 添加到 Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c1222-582">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="c1222-583">将新的可选参数 -LinkedDataFactoryName 添加到 Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c1222-583">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="c1222-584">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c1222-584">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="c1222-585">将数据平面 SDK (Microsoft.Azure.DataLake.Store) 版本更新为 1.1.9</span><span class="sxs-lookup"><span data-stu-id="c1222-585">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="c1222-586">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="c1222-586">AzureRM.EventHub</span></span>
* <span data-ttu-id="c1222-587">在删除 cmdlet 中更新了 InputObject 和 ResourceId 的管道</span><span class="sxs-lookup"><span data-stu-id="c1222-587">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="c1222-588">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="c1222-588">AzureRM.Insights</span></span>
* <span data-ttu-id="c1222-589">修复了帮助文件中 OutputType 的格式问题</span><span class="sxs-lookup"><span data-stu-id="c1222-589">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="c1222-590">使用 Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span><span class="sxs-lookup"><span data-stu-id="c1222-590">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="c1222-591">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c1222-591">AzureRM.KeyVault</span></span>
* <span data-ttu-id="c1222-592">修复了 Set-AzureRmKeyVaultAccessPolicy 中的管道问题</span><span class="sxs-lookup"><span data-stu-id="c1222-592">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="c1222-593">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c1222-593">AzureRM.Network</span></span>
* <span data-ttu-id="c1222-594">添加了 LoadBalancerInboundNatPoolConfig cmdlet 的示例。</span><span class="sxs-lookup"><span data-stu-id="c1222-594">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="c1222-595">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="c1222-595">AzureRM.Resources</span></span>
* <span data-ttu-id="c1222-596">修复了为“Get-AzureRmResource”同时提供标记名称和值时出现的问题</span><span class="sxs-lookup"><span data-stu-id="c1222-596">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="c1222-597">使用“Set-AzureRmResource”修复管道方案</span><span class="sxs-lookup"><span data-stu-id="c1222-597">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="c1222-598">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c1222-598">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="c1222-599">在删除 cmdlet 中更新了 InputObject 和 ResourceId 的管道</span><span class="sxs-lookup"><span data-stu-id="c1222-599">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="c1222-600">修复了几个问题</span><span class="sxs-lookup"><span data-stu-id="c1222-600">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="c1222-601">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="c1222-601">AzureRM.Sql</span></span>
* <span data-ttu-id="c1222-602">使用以下 cmdlet 添加服务器高级威胁防护支持：</span><span class="sxs-lookup"><span data-stu-id="c1222-602">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="c1222-603">Enable-AzureRmSqlServerAdvancedThreatProtection；Disable-AzureRmSqlServerAdvancedThreatProtection；Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="c1222-603">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="c1222-604">使用以下 cmdlet 添加漏洞评估支持：</span><span class="sxs-lookup"><span data-stu-id="c1222-604">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="c1222-605">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings；Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings；Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="c1222-605">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="c1222-606">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline；Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline；Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="c1222-606">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="c1222-607">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan；Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord；Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="c1222-607">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="c1222-608">修复了 Remove-AzureRmSqlServerFirewallRule 中的示例</span><span class="sxs-lookup"><span data-stu-id="c1222-608">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="c1222-609">修复了 Get-AzureSqlSyncGroupLog 中非美国基础文化的日期时间处理错误</span><span class="sxs-lookup"><span data-stu-id="c1222-609">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="c1222-610">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="c1222-610">AzureRM.Storage</span></span>
* <span data-ttu-id="c1222-611">将 Ps1XmlAttribute 添加到 cmdlet 输出类型属性</span><span class="sxs-lookup"><span data-stu-id="c1222-611">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="c1222-612">在表视图中显示 StorageAccount cmdlet 输出</span><span class="sxs-lookup"><span data-stu-id="c1222-612">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="c1222-613">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c1222-613">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="c1222-614">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c1222-614">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="c1222-615">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c1222-615">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="c1222-616">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="c1222-616">AzureRM.Tags</span></span>
* <span data-ttu-id="c1222-617">从 Tag cmdlet 帮助中删除不正确的语句</span><span class="sxs-lookup"><span data-stu-id="c1222-617">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="c1222-618">6.5.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="c1222-618">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="c1222-619">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c1222-619">AzureRM.Profile</span></span>
* <span data-ttu-id="c1222-620">更新了“Get-AzureRmContextAutosaveSetting”的帮助</span><span class="sxs-lookup"><span data-stu-id="c1222-620">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="c1222-621">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="c1222-621">Azure.Storage</span></span>
* <span data-ttu-id="c1222-622">支持使用只写 Sas 令牌上传 Blob 或文件</span><span class="sxs-lookup"><span data-stu-id="c1222-622">Support Upload Blob or File with write only Sas token</span></span>
* <span data-ttu-id="c1222-623">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="c1222-623">Set-AzureStorageBlobContent</span></span>
* <span data-ttu-id="c1222-624">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="c1222-624">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="c1222-625">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="c1222-625">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="c1222-626">将所需属性 ResourceGroupName 添加到 AS。</span><span class="sxs-lookup"><span data-stu-id="c1222-626">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="c1222-627">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="c1222-627">AzureRM.Automation</span></span>
* <span data-ttu-id="c1222-628">更新帮助并添加“New-AzureRMAutomationSchedule”的示例</span><span class="sxs-lookup"><span data-stu-id="c1222-628">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="c1222-629">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c1222-629">AzureRM.Compute</span></span>
* <span data-ttu-id="c1222-630">将 -Tag 参数添加到 Update/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="c1222-630">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="c1222-631">添加“Add-AzureRmVmssExtension”的示例</span><span class="sxs-lookup"><span data-stu-id="c1222-631">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="c1222-632">添加“Remove-AzureRmVmssExtension”的示例</span><span class="sxs-lookup"><span data-stu-id="c1222-632">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="c1222-633">更新“Set-AzureRmVMAccessExtension”的帮助</span><span class="sxs-lookup"><span data-stu-id="c1222-633">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="c1222-634">更新 New-AzureRmVmss 的 SimpleParameterSet，以默认情况下将 SinglePlacementGroup 设置为false，并添加开关参数“SinglePlacementGroup”，使用户能够在单个放置组中创建 VMSS。</span><span class="sxs-lookup"><span data-stu-id="c1222-634">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="c1222-635">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="c1222-635">AzureRM.EventHub</span></span>
* <span data-ttu-id="c1222-636">向 PSEventHubDRConfigurationAttributes 类添加了一个只读属性“PendingReplicationOperationsCount”，该属性在复制过程中为挂起的复制操作计数</span><span class="sxs-lookup"><span data-stu-id="c1222-636">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="c1222-637">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c1222-637">AzureRM.KeyVault</span></span>
* <span data-ttu-id="c1222-638">更新了 Set-AzureRmKeyVaultAccessPolicy 的错误消息</span><span class="sxs-lookup"><span data-stu-id="c1222-638">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="c1222-639">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="c1222-639">AzureRM.LogicApp</span></span>
* <span data-ttu-id="c1222-640">修复了 New-AzureRmLogicApp 中的“无法解析参数集”错误</span><span class="sxs-lookup"><span data-stu-id="c1222-640">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="c1222-641">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c1222-641">AzureRM.Network</span></span>
* <span data-ttu-id="c1222-642">在多个租户中为 Set/Add-AzureRmVirtualNetworkPeering 启用跨虚拟网络对等互连</span><span class="sxs-lookup"><span data-stu-id="c1222-642">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="c1222-643">针对应用程序网关更新了以下 cmdlet</span><span class="sxs-lookup"><span data-stu-id="c1222-643">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="c1222-644">New-AzureRmApplicationGateway：添加了 EnableFIPS 标志和区域支持</span><span class="sxs-lookup"><span data-stu-id="c1222-644">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="c1222-645">New-AzureRmApplicationGatewaySku：添加了新的 sku Standard_v2 和 WAF_v2</span><span class="sxs-lookup"><span data-stu-id="c1222-645">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="c1222-646">Set-AzureRmApplicationGatewaySku：添加了新的 sku Standard_v2 和 WAF_v2</span><span class="sxs-lookup"><span data-stu-id="c1222-646">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="c1222-647">使用最新的生成器版本重新生成了 RouteTable cmdlet</span><span class="sxs-lookup"><span data-stu-id="c1222-647">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="c1222-648">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="c1222-648">AzureRM.Relay</span></span>
* <span data-ttu-id="c1222-649">更新了 Markdown 文件，其中修复了示例中的参数名称问题</span><span class="sxs-lookup"><span data-stu-id="c1222-649">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="c1222-650">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="c1222-650">AzureRM.Resources</span></span>
* <span data-ttu-id="c1222-651">更新了 Roleassignment 和 roledefinition cmdlet：</span><span class="sxs-lookup"><span data-stu-id="c1222-651">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="c1222-652">删除了作为分页的一部分完成的额外 roledefinition 调用。</span><span class="sxs-lookup"><span data-stu-id="c1222-652">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="c1222-653">修复了 Get-AzureRmRoleAssignment cmdlet</span><span class="sxs-lookup"><span data-stu-id="c1222-653">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="c1222-654">修复了 -ExpandPrincipalGroups 命令参数功能</span><span class="sxs-lookup"><span data-stu-id="c1222-654">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="c1222-655">修复了“Get-AzureRmResource”的问题，其中“-ResourceType”参数区分大小写</span><span class="sxs-lookup"><span data-stu-id="c1222-655">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="c1222-656">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c1222-656">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="c1222-657">向列表 cmdlet 添加了 top 和 skip 参数</span><span class="sxs-lookup"><span data-stu-id="c1222-657">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="c1222-658">添加了标准到高级命名空间迁移 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="c1222-658">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="c1222-659">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="c1222-659">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="c1222-660">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="c1222-660">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="c1222-661">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="c1222-661">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="c1222-662">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="c1222-662">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="c1222-663">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="c1222-663">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="c1222-664">向 PSServiceBusDRConfigurationAttributes 类添加了一个只读属性“PendingReplicationOperationsCount”，该属性在复制过程中为挂起的复制操作计数</span><span class="sxs-lookup"><span data-stu-id="c1222-664">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="c1222-665">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c1222-665">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="c1222-666">更新了“New-AzureRmServiceFabricCluster”的示例</span><span class="sxs-lookup"><span data-stu-id="c1222-666">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="c1222-667">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="c1222-667">AzureRM.Sql</span></span>
* <span data-ttu-id="c1222-668">为 Management.Sql 添加新的 Cmdlet，以允许客户将 TDE 证书添加到 Sql Server 实例或托管实例</span><span class="sxs-lookup"><span data-stu-id="c1222-668">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="c1222-669">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="c1222-669">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="c1222-670">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="c1222-670">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="c1222-671">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="c1222-671">AzureRM.Websites</span></span>
* <span data-ttu-id="c1222-672">设置为 false 时，`Set-AzureRmWebApp -AssignIdentity` 和 `Set-AzureRmWebAppSlot -AssignIdentity` 现在将从站点对象中删除 Identity 属性。同时移除预览标记。</span><span class="sxs-lookup"><span data-stu-id="c1222-672">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="c1222-673">`Get-AzureRmWebAppMetrics`、`Get-AzureRmAppServicePlanMetrics` 示例已更新</span><span class="sxs-lookup"><span data-stu-id="c1222-673">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="c1222-674">`Set-AzureRmWebApp -PhpVersion` 支持 off 作为有效的 php 版本</span><span class="sxs-lookup"><span data-stu-id="c1222-674">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="c1222-675">6.4.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="c1222-675">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="c1222-676">常规</span><span class="sxs-lookup"><span data-stu-id="c1222-676">General</span></span>
* <span data-ttu-id="c1222-677">修复了大多数模块的帮助文件中的 OutputType 格式问题</span><span class="sxs-lookup"><span data-stu-id="c1222-677">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="c1222-678">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c1222-678">AzureRM.Profile</span></span>
* <span data-ttu-id="c1222-679">已将 Ps1Xml 属性添加到基本输出类型</span><span class="sxs-lookup"><span data-stu-id="c1222-679">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="c1222-680">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c1222-680">AzureRM.Compute</span></span>
* <span data-ttu-id="c1222-681">VMSS 的 IP 标记功能</span><span class="sxs-lookup"><span data-stu-id="c1222-681">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="c1222-682">已添加“New-AzureRmVmssIpTagConfig”cmdlet</span><span class="sxs-lookup"><span data-stu-id="c1222-682">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="c1222-683">已将 IpTag 参数添加到 New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="c1222-683">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="c1222-684">VMSS 的自动 OS 回滚功能</span><span class="sxs-lookup"><span data-stu-id="c1222-684">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="c1222-685">已将 DisableAutoRollback 参数添加到 New-AzureRmVmssConfig 和 Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c1222-685">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="c1222-686">VMSS 的 OS 升级历史记录功能</span><span class="sxs-lookup"><span data-stu-id="c1222-686">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="c1222-687">已将 OSUpgradeHistory 开关参数添加到 Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c1222-687">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="c1222-688">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="c1222-688">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="c1222-689">通过以下命令添加目录 ACL 的支持：</span><span class="sxs-lookup"><span data-stu-id="c1222-689">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="c1222-690">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="c1222-690">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="c1222-691">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="c1222-691">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="c1222-692">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="c1222-692">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="c1222-693">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c1222-693">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="c1222-694">为 Set-AzureRmDataLakeStoreItemAclEntry、Remove-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAcl 添加了取消支持和进度跟踪</span><span class="sxs-lookup"><span data-stu-id="c1222-694">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="c1222-695">为 Export-AzureRmDataLakeStoreChildItemProperties 添加了取消支持</span><span class="sxs-lookup"><span data-stu-id="c1222-695">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="c1222-696">修复了执行递归操作的 cmdlet 的调试消息刷新</span><span class="sxs-lookup"><span data-stu-id="c1222-696">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="c1222-697">修复了 DataLake cmdlet 的测试位置</span><span class="sxs-lookup"><span data-stu-id="c1222-697">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="c1222-698">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="c1222-698">AzureRM.EventHub</span></span>
* <span data-ttu-id="c1222-699">已将可选的 MaxCount 参数添加到“列出操作”cmdlet Get-AzureRmEventHub 和 Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="c1222-699">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="c1222-700">修复了 New-AzureRmEventHub cmdlet 的问题：创建新事件中心时至少需要一个参数。</span><span class="sxs-lookup"><span data-stu-id="c1222-700">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="c1222-701">提供了默认参数集。</span><span class="sxs-lookup"><span data-stu-id="c1222-701">Provided Default Parameter set.</span></span>
* <span data-ttu-id="c1222-702">已将可选参数 -KeyValue 添加到 New-AzureRmEventHubKey cmdlet，该参数可让用户提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="c1222-702">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="c1222-703">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c1222-703">AzureRM.KeyVault</span></span>
* <span data-ttu-id="c1222-704">修复了 Get-AzureRmKeyVault -Tag 返回所有资源的问题</span><span class="sxs-lookup"><span data-stu-id="c1222-704">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="c1222-705">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c1222-705">AzureRM.Network</span></span>
* <span data-ttu-id="c1222-706">为区域冗余的 VirtualNetworkGateways 公开新 SKU</span><span class="sxs-lookup"><span data-stu-id="c1222-706">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="c1222-707">通过 ARM 为以下功能添加了新命令：ExpressRoute 合作伙伴 API</span><span class="sxs-lookup"><span data-stu-id="c1222-707">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="c1222-708">添加了 Get-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="c1222-708">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="c1222-709">添加了 Set-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="c1222-709">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="c1222-710">添加了 Add-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="c1222-710">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="c1222-711">添加了 Get-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="c1222-711">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="c1222-712">添加了 Remove-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="c1222-712">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="c1222-713">添加了 Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="c1222-713">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="c1222-714">添加了 Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="c1222-714">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="c1222-715">添加了 Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="c1222-715">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="c1222-716">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="c1222-716">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="c1222-717">添加了 Get-AzureRmRecoveryServicesBackupStatus cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c1222-717">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="c1222-718">此 cmdlet 采用 VM ID，并检查 VM 是否受订阅中的某个保管库保护。</span><span class="sxs-lookup"><span data-stu-id="c1222-718">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="c1222-719">如果存在此类保管库，该 cmdlet 会输出该保管库的详细信息。</span><span class="sxs-lookup"><span data-stu-id="c1222-719">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="c1222-720">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="c1222-720">AzureRM.Resources</span></span>
* <span data-ttu-id="c1222-721">更新了 Get-AzureRmPolicyAssignment cmdlet：</span><span class="sxs-lookup"><span data-stu-id="c1222-721">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="c1222-722">添加了在管理组级别列出 -Scope 值的支持</span><span class="sxs-lookup"><span data-stu-id="c1222-722">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="c1222-723">添加了在管理组级别使用 -Scope 值检索单个分配的支持</span><span class="sxs-lookup"><span data-stu-id="c1222-723">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="c1222-724">已将 -Effective 和 -All 开关添加到 control 参数</span><span class="sxs-lookup"><span data-stu-id="c1222-724">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="c1222-725">更新了 Get/New/Remove/Set-AzureRmPolicyDefinition cmdlet</span><span class="sxs-lookup"><span data-stu-id="c1222-725">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="c1222-726">添加了 -ManagementGroupName 参数，以将操作应用到给定的管理组</span><span class="sxs-lookup"><span data-stu-id="c1222-726">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="c1222-727">添加了 -SubscriptionId 参数，以将操作应用到给定的订阅</span><span class="sxs-lookup"><span data-stu-id="c1222-727">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="c1222-728">更新了 Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlet</span><span class="sxs-lookup"><span data-stu-id="c1222-728">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="c1222-729">添加了 -ManagementGroupName 参数，以将操作应用到给定的管理组</span><span class="sxs-lookup"><span data-stu-id="c1222-729">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="c1222-730">添加了 -SubscriptionId 参数，以将操作应用到给定的订阅</span><span class="sxs-lookup"><span data-stu-id="c1222-730">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="c1222-731">添加了使用 TemplateParameterObject 时在参数中指定 KeyVault 机密引用的支持</span><span class="sxs-lookup"><span data-stu-id="c1222-731">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="c1222-732">修复了忽略“New-AzureRmADAppCredential”的“-EndDate”参数的问题</span><span class="sxs-lookup"><span data-stu-id="c1222-732">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="c1222-733">修复了“Add-AzureRmADGroupMember”使用错误的 URL 发出请求的问题</span><span class="sxs-lookup"><span data-stu-id="c1222-733">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="c1222-734">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c1222-734">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="c1222-735">已将可选参数 -KeyValue 添加到 New-AzureRmServiceBusKey cmdlet，该参数可让用户提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="c1222-735">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="c1222-736">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="c1222-736">AzureRM.Sql</span></span>
* <span data-ttu-id="c1222-737">在 AzureRmSqlDatabaseRestorePoint 帮助中澄清了 SQLDW 的用户定义还原点</span><span class="sxs-lookup"><span data-stu-id="c1222-737">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="c1222-738">更新了多个 cmdlet 中 -ComputeGeneration 参数的文档</span><span class="sxs-lookup"><span data-stu-id="c1222-738">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="c1222-739">6.3.0 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="c1222-739">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="c1222-740">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c1222-740">AzureRM.Profile</span></span>
* <span data-ttu-id="c1222-741">更新了 Enable-AzureRmContextAutoSave 的错误消息</span><span class="sxs-lookup"><span data-stu-id="c1222-741">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="c1222-742">在运行没有旧上下文的“Connect-AzureRmAccount”时为每个订阅创建一个上下文</span><span class="sxs-lookup"><span data-stu-id="c1222-742">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="c1222-743">Azure.存储</span><span class="sxs-lookup"><span data-stu-id="c1222-743">Azure.Storage</span></span>
* <span data-ttu-id="c1222-744">在帮助文件中增加了关于 -Permissions 参数的其他信息。</span><span class="sxs-lookup"><span data-stu-id="c1222-744">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="c1222-745">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c1222-745">AzureRM.Compute</span></span>
* <span data-ttu-id="c1222-746">“Get-AzureRmVmDiskEncryptionStatus”修复了一个针对没有数据磁盘的 VM 观察到的问题</span><span class="sxs-lookup"><span data-stu-id="c1222-746">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="c1222-747">更新计算客户端库版本以修复以下 cmdlet</span><span class="sxs-lookup"><span data-stu-id="c1222-747">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="c1222-748">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="c1222-748">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="c1222-749">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="c1222-749">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="c1222-750">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="c1222-750">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="c1222-751">修复了以下 cmdlet，因此可以正确地显示“操作 ID”和“操作状态”：</span><span class="sxs-lookup"><span data-stu-id="c1222-751">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="c1222-752">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="c1222-752">Start-AzureRmVM</span></span>
    - <span data-ttu-id="c1222-753">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="c1222-753">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="c1222-754">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="c1222-754">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="c1222-755">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="c1222-755">Set-AzureRmVM</span></span>
    - <span data-ttu-id="c1222-756">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="c1222-756">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="c1222-757">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c1222-757">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="c1222-758">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="c1222-758">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="c1222-759">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="c1222-759">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="c1222-760">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c1222-760">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="c1222-761">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c1222-761">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="c1222-762">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c1222-762">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="c1222-763">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c1222-763">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="c1222-764">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="c1222-764">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="c1222-765">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="c1222-765">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="c1222-766">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="c1222-766">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="c1222-767">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="c1222-767">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="c1222-768">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="c1222-768">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="c1222-769">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="c1222-769">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="c1222-770">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="c1222-770">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="c1222-771">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="c1222-771">AzureRM.EventGrid</span></span>
* <span data-ttu-id="c1222-772">在 Update-AzureRmEventGridSubscription cmdlet 中删除 SubjectBeginsWith/SubjectEndsWith 的 ValidateNotNullOrEmpty 验证条件，允许根据需要将这些参数更改为空字符串。</span><span class="sxs-lookup"><span data-stu-id="c1222-772">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="c1222-773">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c1222-773">AzureRM.KeyVault</span></span>
* <span data-ttu-id="c1222-774">修复运行 Get-AzureRmKeyVault -Tag 时不返回任何标记的问题</span><span class="sxs-lookup"><span data-stu-id="c1222-774">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="c1222-775">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="c1222-775">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="c1222-776">策略见解 cmdlet 的公开发行版</span><span class="sxs-lookup"><span data-stu-id="c1222-776">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="c1222-777">使用 API 版本 2018-04-04</span><span class="sxs-lookup"><span data-stu-id="c1222-777">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="c1222-778">向 Get-AzureRmPolicyStateSummary 的结果添加了 PolicyDefinitionReferenceId</span><span class="sxs-lookup"><span data-stu-id="c1222-778">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="c1222-779">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="c1222-779">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="c1222-780">向 RecoveryServices.Backup cmdlet 添加了 -Vault 参数。</span><span class="sxs-lookup"><span data-stu-id="c1222-780">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="c1222-781">传递时，此项会替代 Set-AzureRmRecoveryServicesContext cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c1222-781">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="c1222-782">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="c1222-782">AzureRM.Sql</span></span>
* <span data-ttu-id="c1222-783">更新了 Get-AzureRmSqlDatabaseExpanded 的帮助文件中的示例</span><span class="sxs-lookup"><span data-stu-id="c1222-783">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="c1222-784">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="c1222-784">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="c1222-785">更新了 Add-AzureRmTrafficManagerEndpointConfig 的帮助文件</span><span class="sxs-lookup"><span data-stu-id="c1222-785">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="c1222-786">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="c1222-786">AzureRM.Websites</span></span>
* <span data-ttu-id="c1222-787">更新了“Set-AzureRmWebApp”，在使用 -AssignIdentity 时不覆盖 AppSettings</span><span class="sxs-lookup"><span data-stu-id="c1222-787">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="c1222-788">更新了“New-AzureRmWebAppSlot”，允许使用 AppServicePlan 作为可选参数</span><span class="sxs-lookup"><span data-stu-id="c1222-788">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="c1222-789">6.2.1 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="c1222-789">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="c1222-790">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="c1222-790">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="c1222-791">更新了 PSWorkspace 模型，允许 Network 使用 type 作为参数</span><span class="sxs-lookup"><span data-stu-id="c1222-791">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="c1222-792">6.2.0 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="c1222-792">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="c1222-793">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c1222-793">AzureRM.Profile</span></span>
* <span data-ttu-id="c1222-794">修复了 Newtonsoft.Json 的版本 10.0.3 在模块导入时无法加载的问题</span><span class="sxs-lookup"><span data-stu-id="c1222-794">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="c1222-795">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c1222-795">AzureRM.Compute</span></span>
* <span data-ttu-id="c1222-796">VMSS VM 更新功能</span><span class="sxs-lookup"><span data-stu-id="c1222-796">VMSS VM Update feature</span></span>
    - <span data-ttu-id="c1222-797">增加了“Update-AzureRmVmssVM”和“New-AzureRmVMDataDisk”cmdlet</span><span class="sxs-lookup"><span data-stu-id="c1222-797">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="c1222-798">为“Add-AzureRmVMDataDisk”cmdlet 增加了 VirtualMachineScaleSetVM 参数，支持向 Vmss VM 添加数据磁盘。</span><span class="sxs-lookup"><span data-stu-id="c1222-798">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="c1222-799">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="c1222-799">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="c1222-800">将 ADF.Net SDK 版本更新到了 0.8.0-preview，其中包含以下更改：</span><span class="sxs-lookup"><span data-stu-id="c1222-800">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="c1222-801">增加了“配置工厂存储库”操作</span><span class="sxs-lookup"><span data-stu-id="c1222-801">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="c1222-802">更新了 QuickBooks LinkedService，可以公开 consumerKey 和 consumerSecret 属性</span><span class="sxs-lookup"><span data-stu-id="c1222-802">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="c1222-803">已将多个模型类型从 SecretBase 更新为 Object</span><span class="sxs-lookup"><span data-stu-id="c1222-803">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="c1222-804">增加了 Blob 事件触发器</span><span class="sxs-lookup"><span data-stu-id="c1222-804">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="c1222-805">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c1222-805">AzureRM.KeyVault</span></span>
* <span data-ttu-id="c1222-806">使用示例输出更新了文档</span><span class="sxs-lookup"><span data-stu-id="c1222-806">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="c1222-807">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c1222-807">AzureRM.Network</span></span>
* <span data-ttu-id="c1222-808">在网络观察程序 cmdlet 上启用了流量分析参数</span><span class="sxs-lookup"><span data-stu-id="c1222-808">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="c1222-809">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="c1222-809">AzureRM.Resources</span></span>
* <span data-ttu-id="c1222-810">修复了从“Get-AzureRmResource”返回的“PSResource”对象的“Properties”属性问题</span><span class="sxs-lookup"><span data-stu-id="c1222-810">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="c1222-811">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="c1222-811">AzureRM.Scheduler</span></span>
* <span data-ttu-id="c1222-812">修复了更新 ServiceBusQueueJob 无法设置新 Auth 值的问题</span><span class="sxs-lookup"><span data-stu-id="c1222-812">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="c1222-813">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="c1222-813">AzureRM.Sql</span></span>
* <span data-ttu-id="c1222-814">使用可选的 LicenseType 参数更新了以下 cmdlet</span><span class="sxs-lookup"><span data-stu-id="c1222-814">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="c1222-815">New-AzureRmSqlDatabase；Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c1222-815">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="c1222-816">New-AzureRmSqlElasticPool；Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="c1222-816">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="c1222-817">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="c1222-817">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="c1222-818">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="c1222-818">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="c1222-819">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c1222-819">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="c1222-820">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="c1222-820">AzureRM.Websites</span></span>
* <span data-ttu-id="c1222-821">更新了“New-AzureRMWebApp”，可以使用策略库中的常用算法。</span><span class="sxs-lookup"><span data-stu-id="c1222-821">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="c1222-822">6.1.0 - 2018 年 5 月</span><span class="sxs-lookup"><span data-stu-id="c1222-822">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="c1222-823">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c1222-823">AzureRM.Profile</span></span>
* <span data-ttu-id="c1222-824">修复了运行“Clear-AzureRmContext”时会保留空上下文的问题，该上下文使用旧的默认上下文的名称，导致用户无法使用旧名称创建新的上下文</span><span class="sxs-lookup"><span data-stu-id="c1222-824">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="c1222-825">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="c1222-825">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="c1222-826">允许在 AS 上执行网关的关联/取消关联操作。</span><span class="sxs-lookup"><span data-stu-id="c1222-826">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="c1222-827">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c1222-827">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="c1222-828">增加了对 ApiVersions、ApiReleases 和 ApiRevisions 的支持</span><span class="sxs-lookup"><span data-stu-id="c1222-828">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="c1222-829">增加了对 ServiceFabric 后端的支持</span><span class="sxs-lookup"><span data-stu-id="c1222-829">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="c1222-830">增加了对 Application Insights Logger 的支持</span><span class="sxs-lookup"><span data-stu-id="c1222-830">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="c1222-831">增加的支持包括认可“基本”SKU 是 API 管理服务的有效 SKU</span><span class="sxs-lookup"><span data-stu-id="c1222-831">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="c1222-832">增加的支持包括允许将专用 CA 颁发的证书作为根证书或 CA 证书安装</span><span class="sxs-lookup"><span data-stu-id="c1222-832">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="c1222-833">增加的支持包括通过 KeyVault 和多个代理主机名接受自定义 SSL 证书</span><span class="sxs-lookup"><span data-stu-id="c1222-833">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="c1222-834">增加了对 MSI 标识的支持</span><span class="sxs-lookup"><span data-stu-id="c1222-834">Added support for MSI identity</span></span>
* <span data-ttu-id="c1222-835">增加的支持包括通过 URL 接受策略 注意：以下 cmdlet 将在未来版本中弃用</span><span class="sxs-lookup"><span data-stu-id="c1222-835">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="c1222-836">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="c1222-836">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="c1222-837">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="c1222-837">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="c1222-838">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="c1222-838">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="c1222-839">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="c1222-839">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="c1222-840">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="c1222-840">AzureRM.Batch</span></span>
* <span data-ttu-id="c1222-841">发布新 cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="c1222-841">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="c1222-842">发布新 cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="c1222-842">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="c1222-843">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="c1222-843">AzureRM.Consumption</span></span>
* <span data-ttu-id="c1222-844">在 Cmdlet Get-AzureRmConsumptionUsageDetail 中增加了新参数 Expand、ResourceGroup、InstanceName、InstanceId、Tags、Top</span><span class="sxs-lookup"><span data-stu-id="c1222-844">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="c1222-845">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c1222-845">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="c1222-846">修复了 Export-AzureRmDataLakeStoreChildItemProperties 的示例</span><span class="sxs-lookup"><span data-stu-id="c1222-846">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="c1222-847">修复了 Set-AzureRmDataLakeStoreItemAclEntry 中 Recurse 用例的 null 参数异常</span><span class="sxs-lookup"><span data-stu-id="c1222-847">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="c1222-848">修复了 Set-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAcl、Remove-AzureRmDataLakeStoreItemAclEntry 的帮助文件</span><span class="sxs-lookup"><span data-stu-id="c1222-848">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="c1222-849">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c1222-849">AzureRM.Network</span></span>
* <span data-ttu-id="c1222-850">将网络 SDK 版本从 18.0.0-preview 升至 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="c1222-850">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="c1222-851">增加了用于创建协议配置的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="c1222-851">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="c1222-852">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="c1222-852">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="c1222-853">增加了用于向现有的快速路由线路添加新的线路连接的 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c1222-853">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="c1222-854">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="c1222-854">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="c1222-855">增加了用于从现有的快速路由线路删除线路连接的 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c1222-855">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="c1222-856">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="c1222-856">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="c1222-857">增加了用于检索线路连接的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="c1222-857">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="c1222-858">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="c1222-858">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="c1222-859">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c1222-859">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="c1222-860">修复了使用生成的证书进行服务器身份验证的问题（问题 5998）</span><span class="sxs-lookup"><span data-stu-id="c1222-860">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="c1222-861">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="c1222-861">AzureRM.Sql</span></span>
* <span data-ttu-id="c1222-862">更新了审核 cmdlet，允许删除 AuditActions 或 AuditActionGroups</span><span class="sxs-lookup"><span data-stu-id="c1222-862">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="c1222-863">修复了设置新的灵活保留策略时使用 Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy 出现的问题。该问题的具体表现是：在命令失败的同时，出现“不再支持使用 Azure 恢复服务保管库和策略配置长期保留策略。</span><span class="sxs-lookup"><span data-stu-id="c1222-863">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="c1222-864">请使用新的灵活保留策略提交请求”错误消息。</span><span class="sxs-lookup"><span data-stu-id="c1222-864">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="c1222-865">更新了与 Azure SQL 数据库/ElasticPool 的创建/更新相关的所有 cmdlet，允许使用新的数据库 API，而这些 cmdlet 支持的 SKU 属性则适用于规模和层相关属性。</span><span class="sxs-lookup"><span data-stu-id="c1222-865">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="c1222-866">更新的 cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="c1222-866">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="c1222-867">New-AzureRmSqlDatabase；Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c1222-867">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="c1222-868">New-AzureRmSqlElasticPool；Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="c1222-868">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="c1222-869">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="c1222-869">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="c1222-870">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="c1222-870">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="c1222-871">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c1222-871">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="c1222-872">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="c1222-872">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="c1222-873">更新了“Get-AzureRmTrafficManagerProfile”的参数，要求在使用 -Name 参数时使用 -ResourceGroupName 参数。</span><span class="sxs-lookup"><span data-stu-id="c1222-873">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
