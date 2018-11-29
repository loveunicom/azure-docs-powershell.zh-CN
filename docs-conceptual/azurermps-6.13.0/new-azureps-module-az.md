---
title: Azure Powershell Az 模块简介
description: 介绍新的 Azure PowerShell 模块 Az（AzureRM 模块的替代品）。
ms.date: 11/07/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: b0f31341d4344bdac5b4d657a1f66acfd9984dda
ms.sourcegitcommit: 558436c824d9b59731aa9b963cdc8df4dea932e7
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/29/2018
ms.locfileid: "52587306"
---
# <a name="introducing-the-new-azure-powershell-az-module"></a><span data-ttu-id="8fb4b-103">新 Azure Powershell Az 模块简介</span><span class="sxs-lookup"><span data-stu-id="8fb4b-103">Introducing the new Azure PowerShell Az module</span></span>

<span data-ttu-id="8fb4b-104">从 2018 年 11 月起，Azure PowerShell `Az` 模块在完整公共预览版中提供。</span><span class="sxs-lookup"><span data-stu-id="8fb4b-104">Starting in November 2018, the Azure PowerShell `Az` module is available for full public preview.</span></span>
<span data-ttu-id="8fb4b-105">Az 提供更短的命令，提高了稳定性，还支持 Windows、macOS 和 Linux。</span><span class="sxs-lookup"><span data-stu-id="8fb4b-105">Az offers shorter commands, improved stability, and supports Windows, macOS, and Linux.</span></span> <span data-ttu-id="8fb4b-106">Az 还提供与 AzureRM 的功能奇偶一致性以及轻松从 AzureRM 执行迁移的途径。</span><span class="sxs-lookup"><span data-stu-id="8fb4b-106">Az also offers feature parity and an easy migration path from AzureRM.</span></span>

<span data-ttu-id="8fb4b-107">Az 使用 .NET Standard 库，这意味着它在 PowerShell 5.x 和 PowerShell 6.x 上运行。</span><span class="sxs-lookup"><span data-stu-id="8fb4b-107">Az uses the .NET Standard library, which means it runs on PowerShell 5.x and PowerShell 6.x.</span></span>
<span data-ttu-id="8fb4b-108">由于 PowerShell 6.x 可以在 Linux、 macOS 和 Windows 上运行，因此这意味着 Az 对所有平台均可用。</span><span class="sxs-lookup"><span data-stu-id="8fb4b-108">Since PowerShell 6.x can run on Linux, macOS, and Windows, that means Az is available for all platforms.</span></span>
<span data-ttu-id="8fb4b-109">使用 .NET Standard，我们可以在将对用户的影响降至最低的情况下统一 Azure PowerShell 的代码库。</span><span class="sxs-lookup"><span data-stu-id="8fb4b-109">Using .NET Standard allows us to unify the code base of Azure PowerShell with minimal impact on users.</span></span>

<span data-ttu-id="8fb4b-110">Az 是新模块，因此版本已重置。</span><span class="sxs-lookup"><span data-stu-id="8fb4b-110">Az is a new module, so the version has been reset.</span></span> <span data-ttu-id="8fb4b-111">第一个稳定版本将是 1.0，但该模块与到 2018 年 11 月为止的 AzureRm 具有功能奇偶一致性。</span><span class="sxs-lookup"><span data-stu-id="8fb4b-111">The first stable release will be 1.0, but the module has feature parity with AzureRm as of November 2018.</span></span>

## <a name="upgrade-to-az"></a><span data-ttu-id="8fb4b-112">升级到 Az</span><span class="sxs-lookup"><span data-stu-id="8fb4b-112">Upgrade to Az</span></span>

<span data-ttu-id="8fb4b-113">我们建议用户升级到新的 `Az` 模块。</span><span class="sxs-lookup"><span data-stu-id="8fb4b-113">It's recommended that users upgrade to the new `Az` module.</span></span> <span data-ttu-id="8fb4b-114">为此，请执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="8fb4b-114">To do so:</span></span>

* [<span data-ttu-id="8fb4b-115">卸载 Azure PowerShell AzureRM 模块</span><span class="sxs-lookup"><span data-stu-id="8fb4b-115">Uninstall the Azure PowerShell AzureRM module</span></span>](/powershell/azure/uninstall-azurerm-ps)
* [<span data-ttu-id="8fb4b-116">安装 Azure PowerShell Az 模块</span><span class="sxs-lookup"><span data-stu-id="8fb4b-116">Install the Azure PowerShell Az module</span></span>](/powershell/azure/install-az-ps)
* <span data-ttu-id="8fb4b-117">熟悉了新的命令集时，请使用 `Enable-AzureRMAlias` 为 AzureRM 启用兼容性模式。</span><span class="sxs-lookup"><span data-stu-id="8fb4b-117">Enable compatibility mode for AzureRM with `Enable-AzureRMAlias` while you become familiar with the new command set.</span></span>

## <a name="migrate-existing-scripts-to-az"></a><span data-ttu-id="8fb4b-118">将现有脚本迁移到 Az</span><span class="sxs-lookup"><span data-stu-id="8fb4b-118">Migrate existing scripts to Az</span></span>

<span data-ttu-id="8fb4b-119">主要更新可能不方便。</span><span class="sxs-lookup"><span data-stu-id="8fb4b-119">Major updates can be inconvenient.</span></span> <span data-ttu-id="8fb4b-120">但是，`Az` 模块具有兼容性模式，可帮助你在逐步掌握新语法的同时使用现有脚本。</span><span class="sxs-lookup"><span data-stu-id="8fb4b-120">However, the `Az` module has a compatibility mode to help you use existing scripts while you work on updates to the new syntax.</span></span> <span data-ttu-id="8fb4b-121">使用 `Enable-AzureRmAlias` cmdlet 可启用 `AzureRM` 兼容性模式。</span><span class="sxs-lookup"><span data-stu-id="8fb4b-121">Use the `Enable-AzureRmAlias` cmdlet to enable the `AzureRM` compatibility mode.</span></span> <span data-ttu-id="8fb4b-122">此 cmdlet 将 `AzureRM` cmdlet 名称定义为新 `Az` cmdlet 名称的别名。</span><span class="sxs-lookup"><span data-stu-id="8fb4b-122">This cmdlet defines `AzureRM` cmdlet names as aliases for the new `Az` cmdlet names.</span></span>

<span data-ttu-id="8fb4b-123">新 cmdlet 名称已设计为易于学习。</span><span class="sxs-lookup"><span data-stu-id="8fb4b-123">The new cmdlet names have been designed to be easy to learn.</span></span> <span data-ttu-id="8fb4b-124">请在 cmdlet 名称中使用 `Az`，而不是使用 `AzureRm` 或 `Azure`。</span><span class="sxs-lookup"><span data-stu-id="8fb4b-124">Instead of using `AzureRm` or `Azure` in cmdlet names, use `Az`.</span></span> <span data-ttu-id="8fb4b-125">例如，旧命令 `New-AzureRmVm` 已变为 `New-AzVm`。</span><span class="sxs-lookup"><span data-stu-id="8fb4b-125">For example, the old command `New-AzureRmVm` has become `New-AzVm`.</span></span>

<span data-ttu-id="8fb4b-126">有关迁移过程的完整说明，请参阅[从 AzureRM 迁移到 Az](migrate-from-azurerm-to-az.md)。</span><span class="sxs-lookup"><span data-stu-id="8fb4b-126">For a full description of the migration process, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>

## <a name="the-future-of-support-for-azurerm"></a><span data-ttu-id="8fb4b-127">对 AzureRM 的支持的未来</span><span class="sxs-lookup"><span data-stu-id="8fb4b-127">The future of support for AzureRM</span></span>

<span data-ttu-id="8fb4b-128">`Az` 1.0 版在 2018 年 12 月发布时，现有 `AzureRM` 模块将不再接收新的 cmdlet 或功能。</span><span class="sxs-lookup"><span data-stu-id="8fb4b-128">The existing `AzureRM` module will no longer receive new cmdlets or features when `Az` version 1.0 is released in December 2018.</span></span> <span data-ttu-id="8fb4b-129">但是，`AzureRM` 仍会受到正式维护，并且会获得 bug 修复。</span><span class="sxs-lookup"><span data-stu-id="8fb4b-129">However, `AzureRM` is still officially maintained and will get bug fixes.</span></span> <span data-ttu-id="8fb4b-130">若要及时了解最新的 Azure 服务和功能，应切换到 `Az` 模块。</span><span class="sxs-lookup"><span data-stu-id="8fb4b-130">To keep up with the latest Azure services and features, you should switch to the `Az` module.</span></span>