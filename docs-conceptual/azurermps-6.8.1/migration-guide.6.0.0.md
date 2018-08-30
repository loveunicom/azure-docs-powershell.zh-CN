---
title: Microsoft Azure PowerShell 6.0.0 的重大更改
description: 本迁移指南包含一个列表，列出了在发行的版本 6 中对 Azure PowerShell 所做的重大更改。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 5/1/2018
ms.openlocfilehash: 4f9c99152fd6ddc23aec005c8e8957e545e65246
ms.sourcegitcommit: dca906e73e943aac207cee23b79915773419c673
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/30/2018
ms.locfileid: "43250168"
---
# <a name="breaking-changes-for-microsoft-azure-powershell-600"></a><span data-ttu-id="e2c8c-103">Microsoft Azure PowerShell 6.0.0 的重大更改</span><span class="sxs-lookup"><span data-stu-id="e2c8c-103">Breaking changes for Microsoft Azure PowerShell 6.0.0</span></span>

<span data-ttu-id="e2c8c-104">本文档是面向 Microsoft Azure PowerShell cmdlet 的使用者的重大更改通知和迁移指南。</span><span class="sxs-lookup"><span data-stu-id="e2c8c-104">This document serves as both a breaking change notification and migration guide for consumers of the Microsoft Azure PowerShell cmdlets.</span></span> <span data-ttu-id="e2c8c-105">每部分都介绍了重大更改的影响和最简便的迁移路径。</span><span class="sxs-lookup"><span data-stu-id="e2c8c-105">Each section describes both the impetus for the breaking change and the migration path of least resistance.</span></span> <span data-ttu-id="e2c8c-106">有关深入的上下文，请参考与每个更改关联的拉取请求。</span><span class="sxs-lookup"><span data-stu-id="e2c8c-106">For in-depth context, please refer to the pull request associated with each change.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="e2c8c-107">目录</span><span class="sxs-lookup"><span data-stu-id="e2c8c-107">Table of Contents</span></span>

- [<span data-ttu-id="e2c8c-108">常规重大更改</span><span class="sxs-lookup"><span data-stu-id="e2c8c-108">General breaking changes</span></span>](#general-breaking-changes)
    - [<span data-ttu-id="e2c8c-109">PowerShell 最低版本要求升至 5.0</span><span class="sxs-lookup"><span data-stu-id="e2c8c-109">Minimum PowerShell version required bumped to 5.0</span></span>](#minimum-powershell-version-required-bumped-to-50)
    - [<span data-ttu-id="e2c8c-110">默认启用上下文自动保存功能</span><span class="sxs-lookup"><span data-stu-id="e2c8c-110">Context autosaved enabled by default</span></span>](#context-autosaved-enabled-by-default)
    - [<span data-ttu-id="e2c8c-111">删除标记别名</span><span class="sxs-lookup"><span data-stu-id="e2c8c-111">Removal of Tags alias</span></span>](#removal-of-tags-alias)
- [<span data-ttu-id="e2c8c-112">AzureRM.Compute cmdlet 的重大更改</span><span class="sxs-lookup"><span data-stu-id="e2c8c-112">Breaking changes to AzureRM.Compute cmdlets</span></span>](#breaking-changes-to-azurermcompute-cmdlets)
- [<span data-ttu-id="e2c8c-113">AzureRM.DataLakeStore cmdlet 的重大更改</span><span class="sxs-lookup"><span data-stu-id="e2c8c-113">Breaking changes to AzureRM.DataLakeStore cmdlets</span></span>](#breaking-changes-to-azurermdatalakestore-cmdlets)
- [<span data-ttu-id="e2c8c-114">AzureRM.Dns cmdlet 的重大更改</span><span class="sxs-lookup"><span data-stu-id="e2c8c-114">Breaking changes to AzureRM.Dns cmdlets</span></span>](#breaking-changes-to-azurermdns-cmdlets)
- [<span data-ttu-id="e2c8c-115">AzureRM.Insights cmdlet 的重大更改</span><span class="sxs-lookup"><span data-stu-id="e2c8c-115">Breaking changes to AzureRM.Insights cmdlets</span></span>](#breaking-changes-to-azurerminsights-cmdlets)
- [<span data-ttu-id="e2c8c-116">AzureRM.KeyVault cmdlet 的重大更改</span><span class="sxs-lookup"><span data-stu-id="e2c8c-116">Breaking changes to AzureRM.KeyVault cmdlets</span></span>](#breaking-changes-to-azurermkeyvault-cmdlets)
- [<span data-ttu-id="e2c8c-117">AzureRM.Network cmdlet 的重大更改</span><span class="sxs-lookup"><span data-stu-id="e2c8c-117">Breaking changes to AzureRM.Network cmdlets</span></span>](#breaking-changes-to-azurermnetwork-cmdlets)
- [<span data-ttu-id="e2c8c-118">AzureRM.RedisCache cmdlet 的重大更改</span><span class="sxs-lookup"><span data-stu-id="e2c8c-118">Breaking changes to AzureRM.RedisCache cmdlets</span></span>](#breaking-changes-to-azurermrediscache-cmdlets)
- [<span data-ttu-id="e2c8c-119">AzureRM.Resources cmdlet 的重大更改</span><span class="sxs-lookup"><span data-stu-id="e2c8c-119">Breaking changes to AzureRM.Resources cmdlets</span></span>](#breaking-changes-to-azurermresources-cmdlets)
- [<span data-ttu-id="e2c8c-120">AzureRM.Storage cmdlet 的重大更改</span><span class="sxs-lookup"><span data-stu-id="e2c8c-120">Breaking changes to AzureRM.Storage cmdlets</span></span>](#breaking-changes-to-azurermstorage-cmdlets)
- [<span data-ttu-id="e2c8c-121">删除的模块</span><span class="sxs-lookup"><span data-stu-id="e2c8c-121">Removed modules</span></span>](#removed-modules)
    - [`AzureRM.ServerManagement`](#azurermservermanagement)
    - [`AzureRM.SiteRecovery`](#azurermsiterecovery)

## <a name="general-breaking-changes"></a><span data-ttu-id="e2c8c-122">常规重大更改</span><span class="sxs-lookup"><span data-stu-id="e2c8c-122">General breaking changes</span></span>

### <a name="minimum-powershell-version-required-bumped-to-50"></a><span data-ttu-id="e2c8c-123">PowerShell 最低版本要求升至 5.0</span><span class="sxs-lookup"><span data-stu-id="e2c8c-123">Minimum PowerShell version required bumped to 5.0</span></span>

<span data-ttu-id="e2c8c-124">Azure PowerShell 以前要求使用至少 3.0 版的 PowerShell 来运行 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e2c8c-124">Previously, Azure PowerShell required _at least_ version 3.0 of PowerShell to run any cmdlet.</span></span> <span data-ttu-id="e2c8c-125">此要求以后会提高到 5.0 版的 PowerShell。</span><span class="sxs-lookup"><span data-stu-id="e2c8c-125">Moving forward, this requirement will be raised to version 5.0 of PowerShell.</span></span> <span data-ttu-id="e2c8c-126">若要了解如何升级到 PowerShell 5.0，请查看[此表](https://docs.microsoft.com/en-us/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell)。</span><span class="sxs-lookup"><span data-stu-id="e2c8c-126">For information on upgrading to PowerShell 5.0, please see [this table](https://docs.microsoft.com/en-us/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).</span></span>

### <a name="context-autosave-enabled-by-default"></a><span data-ttu-id="e2c8c-127">默认启用上下文自动保存功能</span><span class="sxs-lookup"><span data-stu-id="e2c8c-127">Context autosave enabled by default</span></span>

<span data-ttu-id="e2c8c-128">上下文自动保存是指存储可以在新的和不同的 PowerShell 会话之间使用的 Azure 登录信息。</span><span class="sxs-lookup"><span data-stu-id="e2c8c-128">Context autosave is the storage of Azure sign in information that can be used between new and different PowerShell sessions.</span></span> <span data-ttu-id="e2c8c-129">有关上下文自动保存的详细信息，请参阅[此文档](https://docs.microsoft.com/en-us/powershell/azure/context-persistence)。</span><span class="sxs-lookup"><span data-stu-id="e2c8c-129">For more information on context autosave, please see [this document](https://docs.microsoft.com/en-us/powershell/azure/context-persistence).</span></span>

<span data-ttu-id="e2c8c-130">在以前，上下文自动保存功能是禁用的，这意味着在两次会话之间不会存储用户的 Azure 身份验证信息，除非用户通过运行 `Enable-AzureRmContextAutosave` cmdlet 启用了上下文保存功能。</span><span class="sxs-lookup"><span data-stu-id="e2c8c-130">Previously by default, context autosave was disabled, which meant the user's Azure authentication information was not stored between sessions until they ran the `Enable-AzureRmContextAutosave` cmdlet to turn on context persistence.</span></span> <span data-ttu-id="e2c8c-131">在以后，上下文自动保存功能会默认启用，这意味着即使用户的自动保存设置是不保存上下文，他们在下次登录时系统也会存储其上下文。</span><span class="sxs-lookup"><span data-stu-id="e2c8c-131">Moving forward, context autosave will be enabled by default, which means that users _with no saved context autosave settings_ will have their context stored the next time they sign in.</span></span> <span data-ttu-id="e2c8c-132">用户可以选择使用 `Disable-AzureRmContextAutosave` cmdlet 来退出此功能。</span><span class="sxs-lookup"><span data-stu-id="e2c8c-132">Users can opt out of this functionality by using the `Disable-AzureRmContextAutosave` cmdlet.</span></span>

<span data-ttu-id="e2c8c-133">_注意_：如果用户以前禁用了上下文自动保存，或者在启用上下文自动保存后使用的是现有的上下文，则不受此更改的影响</span><span class="sxs-lookup"><span data-stu-id="e2c8c-133">_Note_: users that previously disabled context autosave or users with context autosave enabled and existing contexts will not be affected by this change</span></span>

### <a name="removal-of-tags-alias"></a><span data-ttu-id="e2c8c-134">删除标记别名</span><span class="sxs-lookup"><span data-stu-id="e2c8c-134">Removal of Tags alias</span></span>

<span data-ttu-id="e2c8c-135">`Tag` 参数的别名 `Tags` 已在多个 cmdlet 中删除。</span><span class="sxs-lookup"><span data-stu-id="e2c8c-135">The alias `Tags` for the `Tag` parameter has been removed across numerous cmdlets.</span></span> <span data-ttu-id="e2c8c-136">下面是受此影响的模块（以及相应的 cmdlet）的列表：</span><span class="sxs-lookup"><span data-stu-id="e2c8c-136">Below is a list of modules (and the corresponding cmdlets) affected by this:</span></span>

#### `AzureRM.ApiManagement`

- `New-AzureRmApiManagement`
- `New-AzureRmApiManagementProperty`
- `Set-AzureRmApiManagementProperty`

#### `AzureRM.Automation`
- `Set-AzureRmAutomationRunbook`

#### `AzureRM.Cdn`
- `New-AzureRmCdnEndpoint`
- `New-AzureRmCdnProfile`

#### `AzureRM.Compute`
- `New-AzureRmVM`
- `Update-AzureRmVM`

#### `AzureRM.DataFactories`
- `New-AzureRmDataFactories`

#### `AzureRM.DataLakeAnalytics`
- `New-AzureRmDataLakeAnalyticsAccount`

#### `AzureRM.DataLakeStore`
- `New-AzureRmDataLakeStoreAccount`
- `Set-AzureRmDataLakeStoreAccount`

#### `AzureRM.MachineLearning`
- `Update-AzureRmMlCommitmentPlan`

#### `AzureRM.Media`
- `Set-AzureRmMediaService`

#### `AzureRM.OperationalInsights`
- `New-AzureRmOperationalInsightsSavedSearch`
- `New-AzureRmOperationalInsightsWorkspace`
- `Set-AzureRmOperationalInsightsSavedSearch`
- `Set-AzureRmOperationalInsightsWorkspace`

## <a name="breaking-changes-to-azurermcompute-cmdlets"></a><span data-ttu-id="e2c8c-137">AzureRM.Compute cmdlet 的重大更改</span><span class="sxs-lookup"><span data-stu-id="e2c8c-137">Breaking changes to AzureRM.Compute cmdlets</span></span>

<span data-ttu-id="e2c8c-138">**其他**</span><span class="sxs-lookup"><span data-stu-id="e2c8c-138">**Miscellaneous**</span></span>
- <span data-ttu-id="e2c8c-139">嵌套在类型 `PSDisk` 和 `PSSnapshot` 中的 SKU 名称属性已分别从 `StandardLRS` 和 `PremiumLRS` 更改为 `Standard_LRS` 和 `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="e2c8c-139">The sku name property nested in types `PSDisk` and `PSSnapshot` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

```powershell
$disk = Get-AzureRmDisk -ResourceGroupName "MyResourceGroup" -DiskName "MyDiskName"
$disk.Sku.Name       # This will now return Standard_LRS or Premium_LRS

$snapshot = Get-AzureRmSnapshot -ResourceGroupName "MyResourceGroup" -SnapshotName "MySnapshotName"
$snapshot.Sku.Name   # This will now return Standard_LRS or Premium_LRS
```

- <span data-ttu-id="e2c8c-140">嵌套在类型 `PSVirtualMachine`、`PSVirtualMachineScaleSet`、`PSImage` 中的存储帐户类型属性已分别从 `StandardLRS` 和 `PremiumLRS` 更改为 `Standard_LRS` 和 `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="e2c8c-140">The storage account type property nested in types `PSVirtualMachine`, `PSVirtualMachineScaleSet` and `PSImage` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

```powershell
$vm = Get-AzureRmVM -ResourceGroupName "MyResourceGroup" -Name "MyVM"
$vm.StorageProfile.DataDisks[0].ManagedDisk.StorageAccountType   # This will now return Standard_LRS or Premium_LRS
```

<span data-ttu-id="e2c8c-141">**Add-AzureRmImageDataDisk**</span><span class="sxs-lookup"><span data-stu-id="e2c8c-141">**Add-AzureRmImageDataDisk**</span></span>
- <span data-ttu-id="e2c8c-142">参数 `StorageAccountType` 接受的值已分别从 `StandardLRS` 和 `PremiumLRS` 更改为 `Standard_LRS` 和 `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="e2c8c-142">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="e2c8c-143">**Add-AzureRmVMDataDisk**</span><span class="sxs-lookup"><span data-stu-id="e2c8c-143">**Add-AzureRmVMDataDisk**</span></span>
- <span data-ttu-id="e2c8c-144">参数 `StorageAccountType` 接受的值已分别从 `StandardLRS` 和 `PremiumLRS` 更改为 `Standard_LRS` 和 `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="e2c8c-144">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="e2c8c-145">**Add-AzureRmVmssDataDisk**</span><span class="sxs-lookup"><span data-stu-id="e2c8c-145">**Add-AzureRmVmssDataDisk**</span></span>
- <span data-ttu-id="e2c8c-146">参数 `StorageAccountType` 接受的值已分别从 `StandardLRS` 和 `PremiumLRS` 更改为 `Standard_LRS` 和 `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="e2c8c-146">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="e2c8c-147">**New-AzureRmAvailabilitySet**</span><span class="sxs-lookup"><span data-stu-id="e2c8c-147">**New-AzureRmAvailabilitySet**</span></span>
- <span data-ttu-id="e2c8c-148">参数 `Managed` 已删除，改用 `Sku`</span><span class="sxs-lookup"><span data-stu-id="e2c8c-148">The parameter `Managed` was removed in favor of `Sku`</span></span>

```powershell
# Old
New-AzureRmAvailabilitySet -ResourceGroupName "MyRG" -Name "MyAvailabilitySet" -Location "West US" -Managed

# New
New-AzureRmAvailabilitySet -ResourceGroupName "MyRG" -Name "MyAvailabilitySet" -Location "West US" -Sku "Aligned"
```

<span data-ttu-id="e2c8c-149">**New-AzureRmDiskConfig**</span><span class="sxs-lookup"><span data-stu-id="e2c8c-149">**New-AzureRmDiskConfig**</span></span>
- <span data-ttu-id="e2c8c-150">参数 `SkuName` 接受的值已分别从 `StandardLRS` 和 `PremiumLRS` 更改为 `Standard_LRS` 和 `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="e2c8c-150">The accepted values for parameter `SkuName` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="e2c8c-151">**New-AzureRmDiskUpdateConfig**</span><span class="sxs-lookup"><span data-stu-id="e2c8c-151">**New-AzureRmDiskUpdateConfig**</span></span>
- <span data-ttu-id="e2c8c-152">参数 `SkuName` 接受的值已分别从 `StandardLRS` 和 `PremiumLRS` 更改为 `Standard_LRS` 和 `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="e2c8c-152">The accepted values for parameter `SkuName` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="e2c8c-153">**New-AzureRmSnapshotConfig**</span><span class="sxs-lookup"><span data-stu-id="e2c8c-153">**New-AzureRmSnapshotConfig**</span></span>
- <span data-ttu-id="e2c8c-154">参数 `SkuName` 接受的值已分别从 `StandardLRS` 和 `PremiumLRS` 更改为 `Standard_LRS` 和 `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="e2c8c-154">The accepted values for parameter `SkuName` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="e2c8c-155">**New-AzureRmSnapshotUpdateConfig**</span><span class="sxs-lookup"><span data-stu-id="e2c8c-155">**New-AzureRmSnapshotUpdateConfig**</span></span>
- <span data-ttu-id="e2c8c-156">参数 `SkuName` 接受的值已分别从 `StandardLRS` 和 `PremiumLRS` 更改为 `Standard_LRS` 和 `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="e2c8c-156">The accepted values for parameter `SkuName` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="e2c8c-157">**Set-AzureRmImageOsDisk**</span><span class="sxs-lookup"><span data-stu-id="e2c8c-157">**Set-AzureRmImageOsDisk**</span></span>
- <span data-ttu-id="e2c8c-158">参数 `StorageAccountType` 接受的值已分别从 `StandardLRS` 和 `PremiumLRS` 更改为 `Standard_LRS` 和 `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="e2c8c-158">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="e2c8c-159">**Set-AzureRmVMAEMExtension**</span><span class="sxs-lookup"><span data-stu-id="e2c8c-159">**Set-AzureRmVMAEMExtension**</span></span>
- <span data-ttu-id="e2c8c-160">参数 `DisableWAD` 已删除</span><span class="sxs-lookup"><span data-stu-id="e2c8c-160">The parameter `DisableWAD` was removed</span></span>
    -  <span data-ttu-id="e2c8c-161">默认禁用 Windows Azure 诊断</span><span class="sxs-lookup"><span data-stu-id="e2c8c-161">Windows Azure Diagnostics is disabled by default</span></span>

<span data-ttu-id="e2c8c-162">**Set-AzureRmVMDataDisk**</span><span class="sxs-lookup"><span data-stu-id="e2c8c-162">**Set-AzureRmVMDataDisk**</span></span>
- <span data-ttu-id="e2c8c-163">参数 `StorageAccountType` 接受的值已分别从 `StandardLRS` 和 `PremiumLRS` 更改为 `Standard_LRS` 和 `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="e2c8c-163">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="e2c8c-164">**Set-AzureRmVMOSDisk**</span><span class="sxs-lookup"><span data-stu-id="e2c8c-164">**Set-AzureRmVMOSDisk**</span></span>
- <span data-ttu-id="e2c8c-165">参数 `StorageAccountType` 接受的值已分别从 `StandardLRS` 和 `PremiumLRS` 更改为 `Standard_LRS` 和 `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="e2c8c-165">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="e2c8c-166">**Set-AzureRmVmssStorageProfile**</span><span class="sxs-lookup"><span data-stu-id="e2c8c-166">**Set-AzureRmVmssStorageProfile**</span></span>
- <span data-ttu-id="e2c8c-167">参数 `ManagedDisk` 接受的值已分别从 `StandardLRS` 和 `PremiumLRS` 更改为 `Standard_LRS` 和 `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="e2c8c-167">The accepted values for parameter `ManagedDisk` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="e2c8c-168">**Update-AzureRmVmss**</span><span class="sxs-lookup"><span data-stu-id="e2c8c-168">**Update-AzureRmVmss**</span></span>
- <span data-ttu-id="e2c8c-169">参数 `ManagedDiskStorageAccountType` 接受的值已分别从 `StandardLRS` 和 `PremiumLRS` 更改为 `Standard_LRS` 和 `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="e2c8c-169">The accepted values for parameter `ManagedDiskStorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

## <a name="breaking-changes-to-azurermdatalakestore-cmdlets"></a><span data-ttu-id="e2c8c-170">AzureRM.DataLakeStore cmdlet 的重大更改</span><span class="sxs-lookup"><span data-stu-id="e2c8c-170">Breaking changes to AzureRM.DataLakeStore cmdlets</span></span>

<span data-ttu-id="e2c8c-171">**Export-AzureRmDataLakeStoreItem**</span><span class="sxs-lookup"><span data-stu-id="e2c8c-171">**Export-AzureRmDataLakeStoreItem**</span></span>
- <span data-ttu-id="e2c8c-172">参数 `PerFileThreadCount` 和 `ConcurrentFileCount` 已删除。</span><span class="sxs-lookup"><span data-stu-id="e2c8c-172">Parameters `PerFileThreadCount` and `ConcurrentFileCount` were removed.</span></span> <span data-ttu-id="e2c8c-173">以后请使用 `Concurrency` 参数</span><span class="sxs-lookup"><span data-stu-id="e2c8c-173">Please use the `Concurrency` parameter moving forward</span></span>

```powershell
# Old
Export-AzureRmDataLakeStoreItem -Account contoso -Path /test -Destination C:\test -Recurse -Resume -PerFileThreadCount 2 -ConcurrentFileCount 80

# New
Export-AzureRmDataLakeStoreItem -Account contoso -Path /test -Destination C:\test -Recurse -Resume -Concurrency 160
```

<span data-ttu-id="e2c8c-174">**Import-AzureRmDataLakeStoreItem**</span><span class="sxs-lookup"><span data-stu-id="e2c8c-174">**Import-AzureRmDataLakeStoreItem**</span></span>
- <span data-ttu-id="e2c8c-175">参数 `PerFileThreadCount` 和 `ConcurrentFileCount` 已删除。</span><span class="sxs-lookup"><span data-stu-id="e2c8c-175">Parameters `PerFileThreadCount` and `ConcurrentFileCount` were removed.</span></span> <span data-ttu-id="e2c8c-176">以后请使用 `Concurrency` 参数</span><span class="sxs-lookup"><span data-stu-id="e2c8c-176">Please use the `Concurrency` parameter moving forward</span></span>

```powershell
# Old
Import-AzureRmDataLakeStoreItem -Account contoso -Path C:\test -Destination /test -Recurse -Resume -ForceBinary -PerFileThreadCount 2 -ConcurrentFileCount 80

# New
Import-AzureRmDataLakeStoreItem -Account contoso -Path C:\test -Destination /test -Recurse -Resume -ForceBinary -Concurrency 160
```

<span data-ttu-id="e2c8c-177">**Remove-AzureRmDataLakeStoreItem**</span><span class="sxs-lookup"><span data-stu-id="e2c8c-177">**Remove-AzureRmDataLakeStoreItem**</span></span>
- <span data-ttu-id="e2c8c-178">参数 `Clean` 已删除</span><span class="sxs-lookup"><span data-stu-id="e2c8c-178">Parameter `Clean` was removed</span></span>

```powershell
# Old
Remove-AzureRmDataLakeStoreItem -Account "ContosoADL" -path /myFolder -Recurse -Clean

# New
Remove-AzureRmDataLakeStoreItem -Account "ContosoADL" -path /myFolder -Recurse
```

## <a name="breaking-changes-to-azurermdns-cmdlets"></a><span data-ttu-id="e2c8c-179">AzureRM.Dns cmdlet 的重大更改</span><span class="sxs-lookup"><span data-stu-id="e2c8c-179">Breaking changes to AzureRM.Dns cmdlets</span></span>

<span data-ttu-id="e2c8c-180">**New-AzureRmDnsRecordSet**</span><span class="sxs-lookup"><span data-stu-id="e2c8c-180">**New-AzureRmDnsRecordSet**</span></span>
- <span data-ttu-id="e2c8c-181">参数 `Force` 已删除</span><span class="sxs-lookup"><span data-stu-id="e2c8c-181">The parameter `Force` was removed</span></span>

<span data-ttu-id="e2c8c-182">**Remove-AzureRmDnsRecordSet**</span><span class="sxs-lookup"><span data-stu-id="e2c8c-182">**Remove-AzureRmDnsRecordSet**</span></span>
- <span data-ttu-id="e2c8c-183">参数 `Force` 已删除</span><span class="sxs-lookup"><span data-stu-id="e2c8c-183">The parameter `Force` was removed</span></span>

<span data-ttu-id="e2c8c-184">**Remove-AzureRmDnsZone**</span><span class="sxs-lookup"><span data-stu-id="e2c8c-184">**Remove-AzureRmDnsZone**</span></span>
- <span data-ttu-id="e2c8c-185">参数 `Force` 已删除</span><span class="sxs-lookup"><span data-stu-id="e2c8c-185">The parameter `Force` was removed</span></span>

## <a name="breaking-changes-to-azurerminsights-cmdlets"></a><span data-ttu-id="e2c8c-186">AzureRM.Insights cmdlet 的重大更改</span><span class="sxs-lookup"><span data-stu-id="e2c8c-186">Breaking changes to AzureRM.Insights cmdlets</span></span>

<span data-ttu-id="e2c8c-187">**Add-AzureRmAutoscaleSetting**</span><span class="sxs-lookup"><span data-stu-id="e2c8c-187">**Add-AzureRmAutoscaleSetting**</span></span>
- <span data-ttu-id="e2c8c-188">参数别名 `AutoscaleProfiles` 和 `Notifications` 已删除</span><span class="sxs-lookup"><span data-stu-id="e2c8c-188">The parameter aliases `AutoscaleProfiles` and `Notifications` were removed</span></span>

<span data-ttu-id="e2c8c-189">**Add-AzureRmLogProfile**</span><span class="sxs-lookup"><span data-stu-id="e2c8c-189">**Add-AzureRmLogProfile**</span></span>
- <span data-ttu-id="e2c8c-190">参数别名 `Categories` 和 `Locations` 已删除</span><span class="sxs-lookup"><span data-stu-id="e2c8c-190">The parameter aliases `Categories` and `Locations` were removed</span></span>

<span data-ttu-id="e2c8c-191">**Add-AzureRmMetricAlertRule**</span><span class="sxs-lookup"><span data-stu-id="e2c8c-191">**Add-AzureRmMetricAlertRule**</span></span>
- <span data-ttu-id="e2c8c-192">参数别名 `Actions` 已删除</span><span class="sxs-lookup"><span data-stu-id="e2c8c-192">The parameter alias `Actions` was removed</span></span>

<span data-ttu-id="e2c8c-193">**Add-AzureRmWebtestAlertRule**</span><span class="sxs-lookup"><span data-stu-id="e2c8c-193">**Add-AzureRmWebtestAlertRule**</span></span>
- <span data-ttu-id="e2c8c-194">参数别名 `Actions` 已删除</span><span class="sxs-lookup"><span data-stu-id="e2c8c-194">The parameter alias `Actions` was removed</span></span>

<span data-ttu-id="e2c8c-195">**Get-AzureRmLog**</span><span class="sxs-lookup"><span data-stu-id="e2c8c-195">**Get-AzureRmLog**</span></span>
- <span data-ttu-id="e2c8c-196">参数别名 `MaxRecords` 和 `MaxEvents` 已删除</span><span class="sxs-lookup"><span data-stu-id="e2c8c-196">The parameter aliases `MaxRecords` and `MaxEvents` were removed</span></span>

<span data-ttu-id="e2c8c-197">**Get-AzureRmMetricDefinition**</span><span class="sxs-lookup"><span data-stu-id="e2c8c-197">**Get-AzureRmMetricDefinition**</span></span>
- <span data-ttu-id="e2c8c-198">参数别名 `MetricNames` 已删除</span><span class="sxs-lookup"><span data-stu-id="e2c8c-198">The parameter alias `MetricNames` was removed</span></span>

<span data-ttu-id="e2c8c-199">**New-AzureRmAlertRuleEmail**</span><span class="sxs-lookup"><span data-stu-id="e2c8c-199">**New-AzureRmAlertRuleEmail**</span></span>
- <span data-ttu-id="e2c8c-200">参数别名 `CustomEmails` 和 `SendToServiceOwners` 已删除</span><span class="sxs-lookup"><span data-stu-id="e2c8c-200">The parameter aliases `CustomEmails` and `SendToServiceOwners` were removed</span></span>

<span data-ttu-id="e2c8c-201">**New-AzureRmAlertRuleWebhook**</span><span class="sxs-lookup"><span data-stu-id="e2c8c-201">**New-AzureRmAlertRuleWebhook**</span></span>
- <span data-ttu-id="e2c8c-202">参数别名 `Properties` 已删除</span><span class="sxs-lookup"><span data-stu-id="e2c8c-202">The parameter alias `Properties` was removed</span></span>

<span data-ttu-id="e2c8c-203">**New-AzureRmAutoscaleNotification**</span><span class="sxs-lookup"><span data-stu-id="e2c8c-203">**New-AzureRmAutoscaleNotification**</span></span>
- <span data-ttu-id="e2c8c-204">参数别名 `CustomEmails`、`SendEmailToSubscriptionCoAdministrators`、`Webhooks` 已删除</span><span class="sxs-lookup"><span data-stu-id="e2c8c-204">The parameter aliases `CustomEmails`, `SendEmailToSubscriptionCoAdministrators` and `Webhooks` were removed</span></span>

<span data-ttu-id="e2c8c-205">**New-AzureRmAutoscaleProfile**</span><span class="sxs-lookup"><span data-stu-id="e2c8c-205">**New-AzureRmAutoscaleProfile**</span></span>
- <span data-ttu-id="e2c8c-206">参数别名 `Rules`、`ScheduleDays`、`ScheduleHours`、`ScheduleMinutes` 已删除</span><span class="sxs-lookup"><span data-stu-id="e2c8c-206">The parameter aliases `Rules`, `ScheduleDays`, `ScheduleHours` and `ScheduleMinutes` were removed</span></span>

<span data-ttu-id="e2c8c-207">**New-AzureRmAutoscaleWebhook**</span><span class="sxs-lookup"><span data-stu-id="e2c8c-207">**New-AzureRmAutoscaleWebhook**</span></span>
- <span data-ttu-id="e2c8c-208">参数别名 `Properties` 已删除</span><span class="sxs-lookup"><span data-stu-id="e2c8c-208">The parameter alias `Properties` was removed</span></span>

## <a name="breaking-changes-to-azurermkeyvault-cmdlets"></a><span data-ttu-id="e2c8c-209">AzureRM.KeyVault cmdlet 的重大更改</span><span class="sxs-lookup"><span data-stu-id="e2c8c-209">Breaking changes to AzureRM.KeyVault cmdlets</span></span>

<span data-ttu-id="e2c8c-210">**Add-AzureKeyVaultCertificate**</span><span class="sxs-lookup"><span data-stu-id="e2c8c-210">**Add-AzureKeyVaultCertificate**</span></span>
- <span data-ttu-id="e2c8c-211">`CertificatePolicy` 参数已变为必选。</span><span class="sxs-lookup"><span data-stu-id="e2c8c-211">The `CertificatePolicy` parameter has become mandatory.</span></span>

<span data-ttu-id="e2c8c-212">**Set-AzureKeyVaultManagedStorageSasDefinition**</span><span class="sxs-lookup"><span data-stu-id="e2c8c-212">**Set-AzureKeyVaultManagedStorageSasDefinition**</span></span>
- <span data-ttu-id="e2c8c-213">此 cmdlet 不再接受组成访问令牌的单个参数，而是将显式令牌参数（例如 `Service` 或 `Permissions`）替换为泛型 `TemplateUri` 参数，后者对应于在其他位置定义的示例访问令牌（假定使用存储 PowerShell cmdlet，或者根据存储文档手动进行组合）。此 cmdlet 保留 `ValidityPeriod` 参数。</span><span class="sxs-lookup"><span data-stu-id="e2c8c-213">The cmdlet no longer accepts individual parameters that compose the access token; instead, the cmdlet replaces explicit token parameters, such as `Service` or `Permissions`, with a generic `TemplateUri` parameter, corresponding to a sample access token defined elsewhere (presumably using Storage PowerShell cmdlets, or composed manually according to the Storage documentation.) The cmdlet retains the `ValidityPeriod` parameter.</span></span>

<span data-ttu-id="e2c8c-214">若要详细了解如何为 Azure 存储组合共享访问令牌，请参阅相应的文档页：</span><span class="sxs-lookup"><span data-stu-id="e2c8c-214">For more information on composing shared access tokens for Azure Storage, please refer to the documentation pages, respectively:</span></span>
- <span data-ttu-id="e2c8c-215">[Constructing a Service SAS] (https://docs.microsoft.com/en-us/rest/api/storageservices/Constructing-a-Service-SAS)（构造服务 SAS）</span><span class="sxs-lookup"><span data-stu-id="e2c8c-215">[Constructing a Service SAS] (https://docs.microsoft.com/en-us/rest/api/storageservices/Constructing-a-Service-SAS)</span></span>
- <span data-ttu-id="e2c8c-216">[Constructing an Account SAS] (https://docs.microsoft.com/en-us/rest/api/storageservices/constructing-an-account-sas)（构造帐户 SAS）</span><span class="sxs-lookup"><span data-stu-id="e2c8c-216">[Constructing an Account SAS] (https://docs.microsoft.com/en-us/rest/api/storageservices/constructing-an-account-sas)</span></span>

```powershell
# Old
$sas = Set-AzureKeyVaultManagedStorageSasDefinition -VaultName myVault -Name myKey -Service Blob -Permissions 'rcw' -ValidityPeriod 180d

# New
$sctx=New-AzureStorageContext -StorageAccountName $sa.StorageAccountName -Protocol Https -StorageAccountKey Key1
$start=[System.DateTime]::Now.AddDays(-1)
$end=[System.DateTime]::Now.AddMonths(1)
$at=New-AzureStorageAccountSasToken -Service blob -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -StartTime $start -ExpiryTime $end -Context $sctx
$sas=Set-AzureKeyVaultManagedStorageSasDefinition -AccountName $sa.StorageAccountName -VaultName $kv.VaultName -Name accountsas -TemplateUri $at -SasType 'account' -ValidityPeriod ([System.Timespan]::FromDays(30))
```

<span data-ttu-id="e2c8c-217">**Set-AzureKeyVaultCertificateIssuer**</span><span class="sxs-lookup"><span data-stu-id="e2c8c-217">**Set-AzureKeyVaultCertificateIssuer**</span></span>
- <span data-ttu-id="e2c8c-218">`IssuerProvider` 参数已变为必选。</span><span class="sxs-lookup"><span data-stu-id="e2c8c-218">The `IssuerProvider` parameter has become mandatory.</span></span>

<span data-ttu-id="e2c8c-219">**Undo-AzureKeyVaultCertificateRemoval**</span><span class="sxs-lookup"><span data-stu-id="e2c8c-219">**Undo-AzureKeyVaultCertificateRemoval**</span></span>
- <span data-ttu-id="e2c8c-220">此 cmdlet 的输出已从 `CertificateBundle` 更改为 `PSKeyVaultCertificate`。</span><span class="sxs-lookup"><span data-stu-id="e2c8c-220">The output of this cmdlet has changed from `CertificateBundle` to `PSKeyVaultCertificate`.</span></span>

<span data-ttu-id="e2c8c-221">**Undo-AzureRmKeyVaultRemoval**</span><span class="sxs-lookup"><span data-stu-id="e2c8c-221">**Undo-AzureRmKeyVaultRemoval**</span></span>
- <span data-ttu-id="e2c8c-222">`ResourceGroupName` 已从 `InputObject` 参数集中删除，改为从 `InputObject` 参数的 `ResourceId` 属性中获取。</span><span class="sxs-lookup"><span data-stu-id="e2c8c-222">`ResourceGroupName` has been removed from the `InputObject` parameter set, and is instead obtained from the `InputObject` parameter's `ResourceId` property.</span></span>

<span data-ttu-id="e2c8c-223">**Set-AzureRmKeyVaultAccessPolicy**</span><span class="sxs-lookup"><span data-stu-id="e2c8c-223">**Set-AzureRmKeyVaultAccessPolicy**</span></span>
- <span data-ttu-id="e2c8c-224">`all` 权限已从 `PermissionsToKeys`、`PermissionsToSecrets`、`PermissionsToCertificates` 中删除。</span><span class="sxs-lookup"><span data-stu-id="e2c8c-224">The `all` permission was removed from `PermissionsToKeys`, `PermissionsToSecrets`, and `PermissionsToCertificates`.</span></span>

<span data-ttu-id="e2c8c-225">**常规**</span><span class="sxs-lookup"><span data-stu-id="e2c8c-225">**General**</span></span>
- <span data-ttu-id="e2c8c-226">`ValueFromPipelineByPropertyName` 属性已从所有允许通过 `InputObject` 进行管道操作的 cmdlet 中删除。</span><span class="sxs-lookup"><span data-stu-id="e2c8c-226">The `ValueFromPipelineByPropertyName` property was removed from all cmdlets where piping by `InputObject` was enabled.</span></span>  <span data-ttu-id="e2c8c-227">受影响的 cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="e2c8c-227">The cmdlets affected are:</span></span>
    - `Add-AzureKeyVaultCertificate`
    - `Add-AzureKeyVaultCertificateContact`
    - `Add-AzureKeyVaultKey`
    - `Backup-AzureKeyVaultKey`
    - `Backup-AzureKeyVaultSecret`
    - `Get-AzureKeyVaultCertficate`
    - `Get-AzureKeyVaultCertificateContact`
    - `Get-AzureKeyVaultCertificateIssuer`
    - `Get-AzureKeyVaultCertificateOperation`
    - `Get-AzureKeyVaultCertificatePolicy`
    - `Get-AzureKeyVaultKey`
    - `Get-AzureKeyVaultManagedStorageAccount`
    - `Get-AzureKeyVaultManagedStorageSasDefinition`
    - `Get-AzureKeyVaultSecret`
    - `Remove-AzureRmKeyVault`
    - `Remove-AzureRmKeyVaultAccessPolicy`
    - `Remove-AzureKeyVaultCertificate`
    - `Remove-AzureKeyVaultCertificateContact`
    - `Remove-AzureKeyVaultCertificateIssuer`
    - `Remove-AzureKeyVaultCertificateOperation`
    - `Remove-AzureKeyVaultKey`
    - `Remove-AzureKeyVaultManagedStorageAccount`
    - `Remove-AzureKeyVaultManagedStorageSasDefinition`
    - `Remove-AzureKeyVaultSecret`
    - `Restore-AzureKeyVaultKey`
    - `Restore-AzureKeyVaultSecret`
    - `Set-AzureRmKeyVaultAccessPolicy`
    - `Set-AzureKeyVaultCertificateAttribute`
    - `Set-AzureKeyVaultCertificateIssuer`
    - `Set-AzureKeyVaultCertificatePolicy`
    - `Set-AzureKeyVaultKeyAttribute`
    - `Set-AzureKeyVaultManagedStorageSasDefinition`
    - `Set-AzureKeyVaultSecret`
    - `Set-AzureKeyVaultSecretAttribute`
    - `Stop-AzureKeyVaultCertificateOperation`
    - `Undo-AzureKeyVaultCertificateRemoval`
    - `Undo-AzureKeyVaultKeyRemoval`
    - `Undo-AzureRmKeyVaultRemoval`
    - `Undo-AzureKeyVaultSecretRemoval`
    - `Update-AzureKeyVaultManagedStorageAccount`
    - `Update-AzureKeyVaultManagedStorageAccountKey`

- <span data-ttu-id="e2c8c-228">`ConfirmImpact` 级别已从所有 cmdlet 中删除。</span><span class="sxs-lookup"><span data-stu-id="e2c8c-228">`ConfirmImpact` levels were removed from all cmdlets.</span></span>  <span data-ttu-id="e2c8c-229">受影响的 cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="e2c8c-229">The cmdlets affected are:</span></span>
    - `Remove-AzureRmKeyVault`
    - `Remove-AzureKeyVaultCertificate`
    - `Remove-AzureKeyVaultCertificateIssuer`
    - `Remove-AzureKeyVaultCertificateOperation`
    - `Remove-AzureKeyVaultKey`
    - `Remove-AzureKeyVaultManagedStorageAccount`
    - `Remove-AzureKeyVaultManagedStorageSasDefinition`
    - `Remove-AzureKeyVaultSecret`
    - `Stop-AzureKeyVaultCertificateOperation`
    - `Update-AzureKeyVaultManagedStorageAccountKey`

- <span data-ttu-id="e2c8c-230">对 `IKeyVaultDataServiceClient` 进行了更新，因此所有证书操作返回 PSTypes 而不是 SDK 类型。</span><span class="sxs-lookup"><span data-stu-id="e2c8c-230">The `IKeyVaultDataServiceClient` was updated so all Certificate operations return PSTypes instead of SDK types.</span></span> <span data-ttu-id="e2c8c-231">这包括：</span><span class="sxs-lookup"><span data-stu-id="e2c8c-231">This includes:</span></span>
    - `SetCertificateContacts`
    - `GetCertificateContacts`
    - `GetCertificate`
    - `GetDeletedCertificate`
    - `MergeCertificate`
    - `ImportCertificate`
    - `DeleteCertificate`
    - `RecoverCertificate`
    - `EnrollCertificate`
    - `UpdateCertificate`
    - `GetCertificateOperation`
    - `DeleteCertificateOperation`
    - `CancelCertificateOperation`
    - `GetCertificatePolicy`
    - `UpdateCertificatePolicy`
    - `GetCertificateIssuer`
    - `SetCertificateIssuer`
    - `DeleteCertificateIssuer`

## <a name="breaking-changes-to-azurermnetwork-cmdlets"></a><span data-ttu-id="e2c8c-232">AzureRM.Network cmdlet 的重大更改</span><span class="sxs-lookup"><span data-stu-id="e2c8c-232">Breaking changes to AzureRM.Network cmdlets</span></span>


<span data-ttu-id="e2c8c-233">**Add-AzureRmApplicationGatewayBackendHttpSettings**</span><span class="sxs-lookup"><span data-stu-id="e2c8c-233">**Add-AzureRmApplicationGatewayBackendHttpSettings**</span></span>
- <span data-ttu-id="e2c8c-234">参数 `ProbeEnabled` 已删除</span><span class="sxs-lookup"><span data-stu-id="e2c8c-234">The parameter `ProbeEnabled` was removed</span></span>

<span data-ttu-id="e2c8c-235">**Add-AzureRmVirtualNetworkPeering**</span><span class="sxs-lookup"><span data-stu-id="e2c8c-235">**Add-AzureRmVirtualNetworkPeering**</span></span>
- <span data-ttu-id="e2c8c-236">参数别名 `AlloowGatewayTransit` 已删除</span><span class="sxs-lookup"><span data-stu-id="e2c8c-236">The parameter alias `AlloowGatewayTransit` was removed</span></span>

<span data-ttu-id="e2c8c-237">**New-AzureRmApplicationGatewayBackendHttpSettings**</span><span class="sxs-lookup"><span data-stu-id="e2c8c-237">**New-AzureRmApplicationGatewayBackendHttpSettings**</span></span>
- <span data-ttu-id="e2c8c-238">参数 `ProbeEnabled` 已删除</span><span class="sxs-lookup"><span data-stu-id="e2c8c-238">The parameter `ProbeEnabled` was removed</span></span>

<span data-ttu-id="e2c8c-239">**Set-AzureRmApplicationGatewayBackendHttpSettings**</span><span class="sxs-lookup"><span data-stu-id="e2c8c-239">**Set-AzureRmApplicationGatewayBackendHttpSettings**</span></span>
- <span data-ttu-id="e2c8c-240">参数 `ProbeEnabled` 已删除</span><span class="sxs-lookup"><span data-stu-id="e2c8c-240">The parameter `ProbeEnabled` was removed</span></span>

## <a name="breaking-changes-to-azurermrediscache-cmdlets"></a><span data-ttu-id="e2c8c-241">AzureRM.RedisCache cmdlet 的重大更改</span><span class="sxs-lookup"><span data-stu-id="e2c8c-241">Breaking changes to AzureRM.RedisCache cmdlets</span></span>

<span data-ttu-id="e2c8c-242">**New-AzureRmRedisCache**</span><span class="sxs-lookup"><span data-stu-id="e2c8c-242">**New-AzureRmRedisCache**</span></span>
- <span data-ttu-id="e2c8c-243">参数 `Subnet` 和 `VirtualNetwork` 已删除，改用 `SubnetId`</span><span class="sxs-lookup"><span data-stu-id="e2c8c-243">The parameters `Subnet` and `VirtualNetwork` were removed in favor of `SubnetId`</span></span>
- <span data-ttu-id="e2c8c-244">参数 `RedisVersion` 已删除</span><span class="sxs-lookup"><span data-stu-id="e2c8c-244">The parameter `RedisVersion` was removed</span></span>
- <span data-ttu-id="e2c8c-245">参数 `MaxMemoryPolicy` 已删除，改用 `RedisConfiguration`</span><span class="sxs-lookup"><span data-stu-id="e2c8c-245">The parameter `MaxMemoryPolicy` was removed in favor of `RedisConfiguration`</span></span>

```powershell
# Old
New-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -Location "North Central US" -MaxMemoryPolicy "allkeys-lru"

# New
New-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -Location "North Central US" -RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}
```

<span data-ttu-id="e2c8c-246">**Set-AzureRmRedisCache**</span><span class="sxs-lookup"><span data-stu-id="e2c8c-246">**Set-AzureRmRedisCache**</span></span>
- <span data-ttu-id="e2c8c-247">参数 `MaxMemoryPolicy` 已删除，改用 `RedisConfiguration`</span><span class="sxs-lookup"><span data-stu-id="e2c8c-247">The parameter `MaxMemoryPolicy` was removed in favor of `RedisConfiguration`</span></span>

```powershell
# Old
Set-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -MaxMemoryPolicy "allkeys-lru"

# New
Set-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}
```

## <a name="breaking-changes-to-azurermresources-cmdlets"></a><span data-ttu-id="e2c8c-248">AzureRM.Resources cmdlet 的重大更改</span><span class="sxs-lookup"><span data-stu-id="e2c8c-248">Breaking changes to AzureRM.Resources cmdlets</span></span>

<span data-ttu-id="e2c8c-249">**Find-AzureRmResource**</span><span class="sxs-lookup"><span data-stu-id="e2c8c-249">**Find-AzureRmResource**</span></span>
- <span data-ttu-id="e2c8c-250">此 cmdlet 已删除，相关功能已移到 `Get-AzureRmResource` 中</span><span class="sxs-lookup"><span data-stu-id="e2c8c-250">This cmdlet was removed and the functionality was moved into `Get-AzureRmResource`</span></span>

```powershell
# Old
Find-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceGroupNameContains "ResourceGroup"
Find-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceNameContains "test"

# New
Get-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceGroupName "*ResourceGroup*"
Get-AzureRmResource -ResourceType "Microsoft.Web/sites" -Name "*test*"
```

<span data-ttu-id="e2c8c-251">**Find-AzureRmResourceGroup**</span><span class="sxs-lookup"><span data-stu-id="e2c8c-251">**Find-AzureRmResourceGroup**</span></span>
- <span data-ttu-id="e2c8c-252">此 cmdlet 已删除，相关功能已移到 `Get-AzureRmResourceGroup` 中</span><span class="sxs-lookup"><span data-stu-id="e2c8c-252">This cmdlet was removed and the functionality was moved into `Get-AzureRmResourceGroup`</span></span>

```powershell
# Old
Find-AzureRmResourceGroup
Find-AzureRmResourceGroup -Tag @{ "testtag" = $null }
Find-AzureRmResourceGroup -Tag @{ "testtag" = "testval" }

# New
Get-AzureRmResourceGroup
Get-AzureRmResourceGroup -Tag @{ "testtag" = $null }
Get-AzureRmResourceGroup -Tag @{ "testtag" = "testval" }
```

<span data-ttu-id="e2c8c-253">**Get-AzureRmRoleDefinition**</span><span class="sxs-lookup"><span data-stu-id="e2c8c-253">**Get-AzureRmRoleDefinition**</span></span>
- <span data-ttu-id="e2c8c-254">参数 `AtScopeAndBelow` 已删除</span><span class="sxs-lookup"><span data-stu-id="e2c8c-254">Parameter `AtScopeAndBelow` was removed.</span></span>

```powershell

# Old
Get-AzureRmRoleDefinition [other required parameters] -AtScopeAndBelow

# New
Get-AzureRmRoleDefinition [other required parameters]
```

## <a name="breaking-changes-to-azurermstorage-cmdlets"></a><span data-ttu-id="e2c8c-255">AzureRM.Storage cmdlet 的重大更改</span><span class="sxs-lookup"><span data-stu-id="e2c8c-255">Breaking changes to AzureRM.Storage cmdlets</span></span>

<span data-ttu-id="e2c8c-256">**New-AzureRmStorageAccount**</span><span class="sxs-lookup"><span data-stu-id="e2c8c-256">**New-AzureRmStorageAccount**</span></span>
- <span data-ttu-id="e2c8c-257">参数 `EnableEncryptionService` 已删除</span><span class="sxs-lookup"><span data-stu-id="e2c8c-257">The parameter `EnableEncryptionService` was removed</span></span>

<span data-ttu-id="e2c8c-258">**Set-AzureRmStorageAccount**</span><span class="sxs-lookup"><span data-stu-id="e2c8c-258">**Set-AzureRmStorageAccount**</span></span>
- <span data-ttu-id="e2c8c-259">参数 `EnableEncryptionService` 和 `DisableEncryptionService` 已删除</span><span class="sxs-lookup"><span data-stu-id="e2c8c-259">The parameters `EnableEncryptionService` and `DisableEncryptionService` were removed</span></span>

## <a name="removed-modules"></a><span data-ttu-id="e2c8c-260">删除的模块</span><span class="sxs-lookup"><span data-stu-id="e2c8c-260">Removed modules</span></span>

### `AzureRM.ServerManagement`

<span data-ttu-id="e2c8c-261">服务器管理工具服务[去年停用](https://blogs.technet.microsoft.com/servermanagement/2017/05/17/smt-preview-service-is-being-retired-on-june-30-2017/)，因此，SMT 的相应模块 `AzureRM.ServerManagement` 已从 `AzureRM` 中删除，以后将停止寄送。</span><span class="sxs-lookup"><span data-stu-id="e2c8c-261">The Server Management Tools service was [retired last year](https://blogs.technet.microsoft.com/servermanagement/2017/05/17/smt-preview-service-is-being-retired-on-june-30-2017/), and as a result, the corresponding module for SMT, `AzureRM.ServerManagement`, was removed from `AzureRM` and will stop shipping moving forward.</span></span>

### `AzureRM.SiteRecovery`

<span data-ttu-id="e2c8c-262">`AzureRM.SiteRecovery` 模块将被 `AzureRM.RecoveryServices.SiteRecovery` 取代，后者是 `AzureRM.SiteRecovery` 模块在功能上的超级组合，包括新的等效 cmdlet 组合。</span><span class="sxs-lookup"><span data-stu-id="e2c8c-262">The `AzureRM.SiteRecovery` module is being superseded by `AzureRM.RecoveryServices.SiteRecovery`, which is a functional superset of the `AzureRM.SiteRecovery` module and includes a new set of equivalent cmdlets.</span></span> <span data-ttu-id="e2c8c-263">下面是从旧 cmdlet 到新 cmdlet 的映射的完整列表：</span><span class="sxs-lookup"><span data-stu-id="e2c8c-263">The full list of mappings from old to new cmdlets can be found below:</span></span>

| <span data-ttu-id="e2c8c-264">已弃用的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="e2c8c-264">Deprecated cmdlet</span></span>                                        | <span data-ttu-id="e2c8c-265">等效 cmdlet</span><span class="sxs-lookup"><span data-stu-id="e2c8c-265">Equivalent cmdlet</span></span>                                                | <span data-ttu-id="e2c8c-266">别名</span><span class="sxs-lookup"><span data-stu-id="e2c8c-266">Aliases</span></span>                                  |
|----------------------------------------------------------|------------------------------------------------------------------|------------------------------------------|
| `Edit-AzureRmSiteRecoveryRecoveryPlan`                   | `Edit-AzureRmRecoveryServicesAsrRecoveryPlan`                    | `Edit-ASRRecoveryPlan`                   |
| `Get-AzureRmSiteRecoveryFabric`                          | `Get-AzureRmRecoveryServicesAsrFabric`                           | `Get-ASRFabric`                          |
| `Get-AzureRmSiteRecoveryJob`                             | `Get-AzureRmRecoveryServicesAsrJob`                              | `Get-ASRJob`                             |
| `Get-AzureRmSiteRecoveryNetwork`                         | `Get-AzureRmRecoveryServicesAsrNetwork`                          | `Get-ASRNetwork`                         |
| `Get-AzureRmSiteRecoveryNetworkMapping`                  | `Get-AzureRmRecoveryServicesAsrNetworkMapping`                   | `Get-ASRNetworkMapping`                  |
| `Get-AzureRmSiteRecoveryPolicy`                          | `Get-AzureRmRecoveryServicesAsrPolicy`                           | `Get-ASRPolicy`                          |
| `Get-AzureRmSiteRecoveryProtectableItem`                 | `Get-AzureRmRecoveryServicesAsrProtectableItem`                  | `Get-ASRProtectableItem`                 |
| `Get-AzureRmSiteRecoveryProtectionContainer`             | `Get-AzureRmRecoveryServicesAsrProtectionContainer`              | `Get-ASRProtectionContainer`             |
| `Get-AzureRmSiteRecoveryProtectionContainerMapping`      | `Get-AzureRmRecoveryServicesAsrProtectionContainerMapping`       | `Get-ASRProtectionContainerMapping`      |
| `Get-AzureRmSiteRecoveryProtectionEntity`                | `Get-AzureRmRecoveryServicesAsrProtectableItem`                  | `Get-ASRProtectableItem`                 |
| `Get-AzureRmSiteRecoveryRecoveryPlan`                    | `Get-AzureRmRecoveryServicesAsrRecoveryPlan`                     | `Get-ASRRecoveryPlan`                    |
| `Get-AzureRmSiteRecoveryRecoveryPoint`                   | `Get-AzureRmRecoveryServicesAsrRecoveryPoint`                    | `Get-ASRRecoveryPoint`                   |
| `Get-AzureRmSiteRecoveryReplicationProtectedItem`        | `Get-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Get-ASRReplicationProtectedItem`        |
| `Get-AzureRmSiteRecoveryServer`                          | `Get-AzureRmRecoveryServicesAsrServicesProvider`                 | `Get-ASRServicesProvider`                |
| `Get-AzureRmSiteRecoveryServicesProvider`                | `Get-AzureRmRecoveryServicesAsrServicesProvider`                 | `Get-ASRServicesProvider`                |
| `Get-AzureRmSiteRecoverySite`                            | `Get-AzureRmRecoveryServicesAsrFabric`                           | `Get-ASRFabric`                          |
| `Get-AzureRmSiteRecoveryStorageClassification`           | `Get-AzureRmRecoveryServicesAsrStorageClassification`            | `Get-ASRStorageClassification`           |
| `Get-AzureRmSiteRecoveryStorageClassificationMapping`    | `Get-AzureRmRecoveryServicesAsrStorageClassificationMapping`     | `Get-ASRStorageClassificationMapping`    |
| `Get-AzureRmSiteRecoveryVault`                           | `Get-AzureRmRecoveryServicesVault`                               |                                          |
| `Get-AzureRmSiteRecoveryVaultSettings`                   | `Get-AzureRmRecoveryServicesAsrVaultContext`                     |                                          |
| `Get-AzureRmSiteRecoveryVaultSettingsFile`               | `Get-AzureRmRecoveryServicesVaultSettingsFile`                   |                                          |
| `Get-AzureRmSiteRecoveryVM`                              | `Get-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Get-ASRReplicationProtectedItem`        |
| `Import-AzureRmSiteRecoveryVaultSettingsFile`            | `Import-AzureRmRecoveryServicesAsrVaultSettingsFile`             |                                          |
| `New-AzureRmSiteRecoveryFabric`                          | `New-AzureRmRecoveryServicesAsrFabric`                           | `New-ASRFabric`                          |
| `New-AzureRmSiteRecoveryNetworkMapping`                  | `New-AzureRmRecoveryServicesAsrNetworkMapping`                   | `New-ASRNetworkMapping`                  |
| `New-AzureRmSiteRecoveryPolicy`                          | `New-AzureRmRecoveryServicesAsrPolicy`                           | `New-ASRPolicy`                          |
| `New-AzureRmSiteRecoveryProtectionContainerMapping`      | `New-AzureRmRecoveryServicesAsrProtectionContainerMapping`       | `New-ASRProtectionContainerMapping`      |
| `New-AzureRmSiteRecoveryRecoveryPlan`                    | `New-AzureRmRecoveryServicesAsrRecoveryPlan`                     | `New-ASRRecoveryPlan`                    |
| `New-AzureRmSiteRecoveryReplicationProtectedItem`        | `New-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `New-ASRReplicationProtectedItem`        |
| `New-AzureRmSiteRecoverySite`                            | `New-AzureRmRecoveryServicesAsrFabric`                           | `New-ASRFabric`                          |
| `New-AzureRmSiteRecoveryStorageClassificationMapping`    | `New-AzureRmRecoveryServicesAsrStorageClassificationMapping`     | `New-ASRStorageClassificationMapping`    |
| `New-AzureRmSiteRecoveryVault`                           | `New-AzureRmRecoveryServicesVault`                               |                                          |
| `Remove-AzureRmSiteRecoveryFabric`                       | `Remove-AzureRmRecoveryServicesAsrFabric`                        | `Remove-ASRFabric`                       |
| `Remove-AzureRmSiteRecoveryNetworkMapping`               | `Remove-AzureRmRecoveryServicesAsrNetworkMapping`                | `Remove-ASRNetworkMapping`               |
| `Remove-AzureRmSiteRecoveryPolicy`                       | `Remove-AzureRmRecoveryServicesAsrPolicy`                        | `Remove-ASRPolicy`                       |
| `Remove-AzureRmSiteRecoveryProtectionContainerMapping`   | `Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping`    | `Remove-ASRProtectionContainerMapping`   |
| `Remove-AzureRmSiteRecoveryRecoveryPlan`                 | `Remove-AzureRmRecoveryServicesAsrRecoveryPlan`                  | `Remove-ASRRecoveryPlan`                 |
| `Remove-AzureRmSiteRecoveryReplicationProtectedItem`     | `Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem`      | `Remove-ASRReplicationProtectedItem`     |
| `Remove-AzureRmSiteRecoveryServer`                       | `Remove-AzureRmRecoveryServicesAsrServicesProvider`              |                                          |
| `Remove-AzureRmSiteRecoveryServicesProvider`             | `Remove-AzureRmRecoveryServicesAsrServicesProvider`              | `Remove-ASRServicesProvider`             |
| `Remove-AzureRmSiteRecoverySite`                         | `Remove-AzureRmRecoveryServicesAsrFabric`                        | `Remove-ASRFabric`                       |
| `Remove-AzureRmSiteRecoveryStorageClassificationMapping` | `Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping`  | `Remove-ASRStorageClassificationMapping` |
| `Remove-AzureRmSiteRecoveryVault`                        | `Remove-AzureRmRecoveryServicesVault`                            |                                          |
| `Restart-AzureRmSiteRecoveryJob`                         | `Restart-AzureRmRecoveryServicesAsrJob`                          | `Restart-ASRJob`                         |
| `Resume-AzureRmSiteRecoveryJob`                          | `Resume-AzureRmRecoveryServicesAsrJob`                           | `Resume-ASRJob`                          |
| `Set-AzureRmSiteRecoveryProtectionEntity`                | `New-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `New-ASRReplicationProtectedItem`        |
| `Set-AzureRmSiteRecoveryReplicationProtectedItem`        | `Set-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Set-ASRReplicationProtectedItem`        |
| `Set-AzureRmSiteRecoveryVaultSettings`                   | `Set-AzureRmRecoveryServicesAsrVaultContext`                     | `Set-ASRVaultContext`                    |
| `Set-AzureRmSiteRecoveryVM`                              | `Set-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Set-ASRReplicationProtectedItem`        |
| `Start-AzureRmSiteRecoveryApplyRecoveryPoint`            | `Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint`             | `Start-ASRApplyRecoveryPoint`            |
| `Start-AzureRmSiteRecoveryCommitFailoverJob`             | `Start-AzureRmRecoveryServicesAsrCommitFailoverJob`              | `Start-ASRCommitFailoverJob`             |
| `Start-AzureRmSiteRecoveryPlannedFailoverJob`            | `Start-AzureRmRecoveryServicesAsrPlannedFailoverJob`             | `Start-ASRPlannedFailoverJob`            |
| `Start-AzureRmSiteRecoveryPolicyAssociationJob`          | `New-AzureRmRecoveryServicesAsrProtectionContainerMapping`       | `New-ASRProtectionContainerMapping`      |
| `Start-AzureRmSiteRecoveryPolicyDissociationJob`         | `Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping`    | `Remove-ASRProtectionContainerMapping`   |
| `Start-AzureRmSiteRecoveryTestFailoverJob`               | `Start-AzureRmRecoveryServicesAsrTestFailoverJob`                | `Start-ASRTestFailoverJob`               |
| `Start-AzureRmSiteRecoveryUnplannedFailoverJob`          | `Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob`           | `Start-ASRUnplannedFailoverJob`          |
| `Stop-AzureRmSiteRecoveryJob`                            | `Stop-AzureRmRecoveryServicesAsrJob`                             | `Stop-ASRJob`                            |
| `Update-AzureRmSiteRecoveryPolicy`                       | `Update-AzureRmRecoveryServicesAsrPolicy`                        | `Update-ASRPolicy`                       |
| `Update-AzureRmSiteRecoveryProtectionDirection`          | `Update-AzureRmRecoveryServicesAsrProtectionDirection`           | `Update-ASRProtectionDirection`          |
| `Update-AzureRmSiteRecoveryRecoveryPlan`                 | `Update-AzureRmRecoveryServicesAsrRecoveryPlan`                  | `Update-ASRRecoveryPlan`                 |
| `Update-AzureRmSiteRecoveryServer`                       | `Update-AzureRmRecoveryServicesAsrServicesProvider`              | `Update-ASRServicesProvider`             |
| `Update-AzureRmSiteRecoveryServicesProvider`             | `Update-AzureRmRecoveryServicesAsrvCenter`                       | `Update-ASRvCenter`                      |
