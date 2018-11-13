---
title: 将 Azure PowerShell 脚本从 AzureRM 迁移到 Az
description: 了解有关将脚本从 AzureRM 模块迁移到新 Az 模块的步骤和工具。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/07/2018
ms.openlocfilehash: 0c73e7ac1d47a2a97b6136fa481d0adce8de33db
ms.sourcegitcommit: ac4b53bb42a25aae013a9d8cd9ae98ada9397274
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/08/2018
ms.locfileid: "51274886"
---
# <a name="migrate-from-azurerm-to-azure-powershell-az"></a><span data-ttu-id="0b551-103">从 AzureRM 迁移到 Azure PowerShell Az</span><span class="sxs-lookup"><span data-stu-id="0b551-103">Migrate from AzureRM to Azure PowerShell Az</span></span>

<span data-ttu-id="0b551-104">Az 模块与 AzureRM 具有功能奇偶一致性，但 Az 模块使用更短且更一致的 cmdlet 名称。</span><span class="sxs-lookup"><span data-stu-id="0b551-104">The Az module has feature parity with AzureRM, but uses shorter and more consistent cmdlet names.</span></span>
<span data-ttu-id="0b551-105">为 AzureRM cmdlet 编写的脚本不会自动与新模块配合工作。</span><span class="sxs-lookup"><span data-stu-id="0b551-105">Scripts written for the AzureRM cmdlets won't automatically work with the new module.</span></span> <span data-ttu-id="0b551-106">为了简化转换，Az 提供了工具，以便你可以使用 AzureRM 运行现有的脚本。</span><span class="sxs-lookup"><span data-stu-id="0b551-106">To make the transition easier, Az offers tools to allow you to run your existing scripts using AzureRM.</span></span> <span data-ttu-id="0b551-107">不迁移到新的命令集十分省事，但本文将帮助你开始转换到新的模块。</span><span class="sxs-lookup"><span data-stu-id="0b551-107">No migration to a new command set is ever convenient, but this article will help you get started on transitioning to the new module.</span></span>

## <a name="ensure-your-existing-scripts-work-with-the-latest-azurerm-release"></a><span data-ttu-id="0b551-108">请确保现有的脚本与最新的 AzureRM 版本配合工作</span><span class="sxs-lookup"><span data-stu-id="0b551-108">Ensure your existing scripts work with the latest AzureRM release</span></span>

<span data-ttu-id="0b551-109">这是最重要的步骤！</span><span class="sxs-lookup"><span data-stu-id="0b551-109">This is the most important step!</span></span> <span data-ttu-id="0b551-110">运行现有的脚本，并确保它们与最新版本的 AzureRM (__6.12.0__) 配合工作。</span><span class="sxs-lookup"><span data-stu-id="0b551-110">Run your existing scripts, and make sure that they work with the _latest_ release of AzureRM (__6.12.0__).</span></span> <span data-ttu-id="0b551-111">如果脚本不起作用，请务必阅读 [AzureRM 迁移指南](migration-guide.6.0.0.md)。</span><span class="sxs-lookup"><span data-stu-id="0b551-111">If your scripts don't work, make sure to read the [AzureRM migration guide](migration-guide.6.0.0.md).</span></span>

## <a name="install-the-azure-powershell-az-module"></a><span data-ttu-id="0b551-112">安装 Azure Powershell Az 模块</span><span class="sxs-lookup"><span data-stu-id="0b551-112">Install the Azure PowerShell Az module</span></span>

<span data-ttu-id="0b551-113">第一步是在平台上安装 Az 模块。</span><span class="sxs-lookup"><span data-stu-id="0b551-113">The first step is to install the Az module on your platform.</span></span> <span data-ttu-id="0b551-114">若要安装 Az，需要卸载 AzureRM。</span><span class="sxs-lookup"><span data-stu-id="0b551-114">To install Az, you need to uninstall AzureRM.</span></span>
<span data-ttu-id="0b551-115">以下步骤将介绍如何继续运行现有脚本并为旧 cmdlet 名称启用兼容性。</span><span class="sxs-lookup"><span data-stu-id="0b551-115">In the following steps, you'll learn how to keep running your existing scripts and enable compatibility for old cmdlet names.</span></span>

<span data-ttu-id="0b551-116">若要安装 Azure PowerShell Az 模块，请执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="0b551-116">To install the Azure PowerShell Az module, follow these steps:</span></span>

* <span data-ttu-id="0b551-117">[卸载 AzureRM 模块](uninstall-azurerm-ps.md)。</span><span class="sxs-lookup"><span data-stu-id="0b551-117">[Uninstall the AzureRM module](uninstall-azurerm-ps.md).</span></span> <span data-ttu-id="0b551-118">请确保删除所有已安装的 AzureRM 版本，不只是最新版本。</span><span class="sxs-lookup"><span data-stu-id="0b551-118">Make sure that you remove _all_ installed versions of AzureRM, not just the most recent version.</span></span>
* [<span data-ttu-id="0b551-119">安装 Az 模块</span><span class="sxs-lookup"><span data-stu-id="0b551-119">Install the Az module</span></span>](install-az-ps.md)

## <a name="a-namealiasesenable-azurerm-alias-mode"></a><span data-ttu-id="0b551-120"><a name="aliases"/>启用 AzureRM 别名模式</span><span class="sxs-lookup"><span data-stu-id="0b551-120"><a name="aliases"/>Enable AzureRM alias mode</span></span>

<span data-ttu-id="0b551-121">卸载了 AzureRM 并且脚本已与最新的 AzureRM 版本配合工作，现在可以为 Az 模块启用兼容性模式。</span><span class="sxs-lookup"><span data-stu-id="0b551-121">With AzureRM uninstalled and your scripts working with the latest AzureRM version, now is the time to enable the compatibility mode for the Az module.</span></span> <span data-ttu-id="0b551-122">使用以下命令启用兼容性：</span><span class="sxs-lookup"><span data-stu-id="0b551-122">Compatibility is enabled with the command:</span></span>

```powershell-interactive
Enable-AzureRmAlias -Scope CurrentUser
```

<span data-ttu-id="0b551-123">在安装了 `Az` 模块的情况下，通过别名可以使用旧 cmdlet 名称。</span><span class="sxs-lookup"><span data-stu-id="0b551-123">Aliases enable the ability to use old cmdlet names with the `Az` module installed.</span></span> <span data-ttu-id="0b551-124">这些别名会写入到所选范围的用户配置文件。</span><span class="sxs-lookup"><span data-stu-id="0b551-124">These aliases are written to the user profile for the selected scope.</span></span> <span data-ttu-id="0b551-125">如果不存在用户配置文件，则会创建一个。</span><span class="sxs-lookup"><span data-stu-id="0b551-125">If no user profile exists, one is created.</span></span>

> [!WARNING]
>
> <span data-ttu-id="0b551-126">可以为此命令使用其他 `-Scope`，但不建议这样做！</span><span class="sxs-lookup"><span data-stu-id="0b551-126">You can use a different `-Scope` for this command, but it's not recommended!</span></span> <span data-ttu-id="0b551-127">别名会写入到所选范围的用户配置文件，因此请保持将其启用到尽可能有限的范围。</span><span class="sxs-lookup"><span data-stu-id="0b551-127">Aliases are written to the user profile for the selected scope, so keep enabling them to as limited a scope as possible.</span></span> <span data-ttu-id="0b551-128">在系统范围内启用别名也可能会导致已在其本地范围内安装 `AzureRM` 的其他用户出现问题。</span><span class="sxs-lookup"><span data-stu-id="0b551-128">Enabling aliases system-wide could also cause issues for other users which have `AzureRM` installed in their local scope.</span></span>

<span data-ttu-id="0b551-129">启用别名模式后，请再次运行脚本以确认它们仍然正常运行。</span><span class="sxs-lookup"><span data-stu-id="0b551-129">Once the alias mode is enabled, run your scripts again to confirm that they still function as expected.</span></span> 

## <a name="change-module-imports-and-cmdlet-names"></a><span data-ttu-id="0b551-130">更改模块导入和 cmdlet 名称</span><span class="sxs-lookup"><span data-stu-id="0b551-130">Change module imports and cmdlet names</span></span>

<span data-ttu-id="0b551-131">一般情况下，模块名称已更改，以便 `AzureRM` 和 `Azure` 变为 `Az`，对于 cmdlet 也是如此。</span><span class="sxs-lookup"><span data-stu-id="0b551-131">In general, the module names have been changed so that `AzureRM` and `Azure` become `Az`, and the same for cmdlets.</span></span>
<span data-ttu-id="0b551-132">例如，`AzureRM.Compute` 模块已重命名为 `Az.Compute`。</span><span class="sxs-lookup"><span data-stu-id="0b551-132">For example, the `AzureRM.Compute` module has been renamed to `Az.Compute`.</span></span> <span data-ttu-id="0b551-133">`New-AzureRmVM` 已变为 `New-AzVM`，并且 `Get-AzureStorageBlob` 现在为 `Get-AzStorageBlob`。</span><span class="sxs-lookup"><span data-stu-id="0b551-133">`New-AzureRmVM` has become `New-AzVM`, and `Get-AzureStorageBlob` is now `Get-AzStorageBlob`.</span></span>

<span data-ttu-id="0b551-134">执行任何重命名之前，应注意此命名更改有一些例外：</span><span class="sxs-lookup"><span data-stu-id="0b551-134">There are exceptions to this naming change that you should be aware of before doing any renaming:</span></span>

| <span data-ttu-id="0b551-135">AzureRM 模块</span><span class="sxs-lookup"><span data-stu-id="0b551-135">AzureRM module</span></span> | <span data-ttu-id="0b551-136">Az 模块</span><span class="sxs-lookup"><span data-stu-id="0b551-136">Az module</span></span> |
|----------------|-----------|
| <span data-ttu-id="0b551-137">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="0b551-137">AzureRM.DataFactories</span></span> | <span data-ttu-id="0b551-138">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0b551-138">Az.DataFactory</span></span> |
| <span data-ttu-id="0b551-139">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="0b551-139">AzureRM.DataFactoryV2</span></span> | <span data-ttu-id="0b551-140">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0b551-140">Az.DataFactory</span></span> |
| <span data-ttu-id="0b551-141">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="0b551-141">AzureRM.RecoveryServices.Backup</span></span> | <span data-ttu-id="0b551-142">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0b551-142">Az.RecoveryServices</span></span> |
| <span data-ttu-id="0b551-143">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="0b551-143">AzureRM.RecoveryServices.SiteRecovery</span></span> | <span data-ttu-id="0b551-144">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0b551-144">Az.RecoveryServices</span></span> |

## <a name="summary"></a><span data-ttu-id="0b551-145">摘要</span><span class="sxs-lookup"><span data-stu-id="0b551-145">Summary</span></span>

<span data-ttu-id="0b551-146">按照以下步骤操作，可以更新所有现有脚本以使用新模块。</span><span class="sxs-lookup"><span data-stu-id="0b551-146">By following these steps, you can update all of your existing scripts to use the new module.</span></span> <span data-ttu-id="0b551-147">如果对这些步骤有任何疑问或问题，使得迁移难于执行，请对本文发表评论，以便我们可以改进说明。</span><span class="sxs-lookup"><span data-stu-id="0b551-147">If you have any questions or problems with these steps that made your migration difficult, please comment on this article so that we can improve the instructions.</span></span>