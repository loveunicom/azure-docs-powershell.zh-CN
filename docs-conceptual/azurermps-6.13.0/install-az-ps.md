---
title: 使用 PowerShellGet 安装 Azure PowerShell 的“Az”
description: 如何使用 PowerShellGet 在 Windows、macOS 和 Linux 上安装 Azure PowerShell。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/16/2018
ms.openlocfilehash: 32e96c6459c9db0c4b9eda0cc170c85ba99a22ca
ms.sourcegitcommit: 80a3da199954d0ab78765715fb49793e89a30f12
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/22/2018
ms.locfileid: "52259454"
---
# <a name="install-the-azure-powershell-az-module"></a><span data-ttu-id="383b9-103">安装 Azure PowerShell 的“Az”模块</span><span class="sxs-lookup"><span data-stu-id="383b9-103">Install the Azure PowerShell 'Az' module</span></span>

<span data-ttu-id="383b9-104">本文介绍如何使用 PowerShellGet 安装 Azure PowerShell 模块。</span><span class="sxs-lookup"><span data-stu-id="383b9-104">This article tells you how to install the Azure PowerShell modules using PowerShellGet.</span></span> <span data-ttu-id="383b9-105">这些说明适用于 Windows、macOS 和 Linux 平台。</span><span class="sxs-lookup"><span data-stu-id="383b9-105">These instructions work on Windows, macOS, and Linux platforms.</span></span> <span data-ttu-id="383b9-106">对于 Az 预览版，任何其他安装方法均不受支持。</span><span class="sxs-lookup"><span data-stu-id="383b9-106">For the preview release of Az, no other install methods are supported.</span></span> 

## <a name="requirements"></a><span data-ttu-id="383b9-107">要求</span><span class="sxs-lookup"><span data-stu-id="383b9-107">Requirements</span></span>

<span data-ttu-id="383b9-108">Azure PowerShell 在 Windows 上可与 PowerShell 5.x 配合工作，在任何平台上都可与 PowerShell 6.x 配合工作。</span><span class="sxs-lookup"><span data-stu-id="383b9-108">Azure PowerShell works with either PowerShell 5.x on Windows, or PowerShell 6.x on any platform.</span></span> <span data-ttu-id="383b9-109">若要查看在计算机上运行的 PowerShell 的版本，请运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="383b9-109">To check the version of PowerShell running on your machine, run the following command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="383b9-110">如果你的版本已过时或需要安装 PowerShell，请参阅[安装各种版本的 PowerShell](https://docs.microsoft.com/en-us/powershell/scripting/setup/installing-powershell?view=powershell-6)。</span><span class="sxs-lookup"><span data-stu-id="383b9-110">If you have an outdated version or need to install PowerShell, see [Installing various versions of PowerShell](https://docs.microsoft.com/en-us/powershell/scripting/setup/installing-powershell?view=powershell-6).</span></span> <span data-ttu-id="383b9-111">从该页面中的链接可访问适用于你的平台的安装信息。</span><span class="sxs-lookup"><span data-stu-id="383b9-111">Install information for your platform is linked from that page.</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="383b9-112">安装 Azure Powershell 模块</span><span class="sxs-lookup"><span data-stu-id="383b9-112">Install the Azure PowerShell module</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="383b9-113">一个系统上不应同时安装有 `AzureRM` 和 `Az` 模块。</span><span class="sxs-lookup"><span data-stu-id="383b9-113">You shouldn't have both the `AzureRM` and `Az` modules installed on a system at the same time.</span></span> <span data-ttu-id="383b9-114">若要安装 `Az` 模块，必须卸载 `AzureRM`。</span><span class="sxs-lookup"><span data-stu-id="383b9-114">In order to install the `Az` module, `AzureRM` must be uninstalled.</span></span> <span data-ttu-id="383b9-115">有关如何执行该操作的说明，请参阅[卸载 Azure PowerShell 模块 (AzureRM)](uninstall-azurerm-ps.md)。</span><span class="sxs-lookup"><span data-stu-id="383b9-115">For instructions on how to do that, see [Uninstall the Azure PowerShell module (AzureRM)](uninstall-azurerm-ps.md).</span></span>

<span data-ttu-id="383b9-116">若要在全局范围安装模块，需要具有提升的权限来安装 PowerShell 库中的模块。</span><span class="sxs-lookup"><span data-stu-id="383b9-116">To install modules at a global scope, you need elevated privileges to install modules from the PowerShell Gallery.</span></span> <span data-ttu-id="383b9-117">若要安装 Azure PowerShell，请在提升的会话中（在 Windows 上“以管理员身份运行”，或在 macOS 或 Linux 上使用超级用户权限）运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="383b9-117">To install Azure PowerShell, run the following command in an elevated session ("Run as Administrator" on Windows, or with superuser privileges on macOS or Linux):</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber
```

<span data-ttu-id="383b9-118">如果没有管理员权限，则可以通过添加 `-Scope` 参数为当前用户进行安装。</span><span class="sxs-lookup"><span data-stu-id="383b9-118">If you don't have access to administrator privileges, you can install for the current user by adding the `-Scope` argument.</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

<span data-ttu-id="383b9-119">默认情况下，PowerShell 库未配置为 PowerShellGet 的受信任存储库。</span><span class="sxs-lookup"><span data-stu-id="383b9-119">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="383b9-120">首次使用 PSGallery 时会看到以下提示：</span><span class="sxs-lookup"><span data-stu-id="383b9-120">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="383b9-121">请回答 `Yes` 或 `Yes to All` 继续安装。</span><span class="sxs-lookup"><span data-stu-id="383b9-121">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="383b9-122">`Az` 模块是 Azure PowerShell cmdlet 的汇总模块。</span><span class="sxs-lookup"><span data-stu-id="383b9-122">The `Az` module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="383b9-123">安装它时，系统会下载所有可用的 Azure 资源管理器模块并使其 cmdlet 可供使用。</span><span class="sxs-lookup"><span data-stu-id="383b9-123">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="sign-in"></a><span data-ttu-id="383b9-124">登录</span><span class="sxs-lookup"><span data-stu-id="383b9-124">Sign in</span></span>

<span data-ttu-id="383b9-125">若要开始使用 Azure PowerShell，请通过 Azure 凭据登录。</span><span class="sxs-lookup"><span data-stu-id="383b9-125">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
>
> <span data-ttu-id="383b9-126">如果已禁用模块自动加载，则需使用 `Import-Module Az` 手动导入模块。</span><span class="sxs-lookup"><span data-stu-id="383b9-126">If you've disabled module autoloading, you need to manually import the module with `Import-Module Az`.</span></span> <span data-ttu-id="383b9-127">考虑到模块的构造方式，这可能需要几秒钟时间。</span><span class="sxs-lookup"><span data-stu-id="383b9-127">Because of the way the module is structured, this can take a few seconds.</span></span>

<span data-ttu-id="383b9-128">需对每个启动的新 PowerShell 会话重复这些步骤。</span><span class="sxs-lookup"><span data-stu-id="383b9-128">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="383b9-129">若要了解如何跨 PowerShell 会话保持 Azure 登录状态，请参阅[跨 PowerShell 会话保持用户凭据](context-persistence.md)。</span><span class="sxs-lookup"><span data-stu-id="383b9-129">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="383b9-130">更新 Azure PowerShell 模块</span><span class="sxs-lookup"><span data-stu-id="383b9-130">Update the Azure PowerShell module</span></span>

<span data-ttu-id="383b9-131">可以通过运行 [Update-Module](/powershell/module/powershellget/update-module) 来更新 Azure PowerShell 安装。</span><span class="sxs-lookup"><span data-stu-id="383b9-131">You can update your Azure PowerShell installation by running [Update-Module](/powershell/module/powershellget/update-module).</span></span> <span data-ttu-id="383b9-132">此命令不卸载以前的版本。</span><span class="sxs-lookup"><span data-stu-id="383b9-132">This command does __not__ uninstall earlier versions.</span></span>

```powershell-interactive
Update-Module -Name Az
```

<span data-ttu-id="383b9-133">若要从系统中删除旧版 Azure PowerShell，请参阅[卸载 Azure PowerShell 模块](uninstall-azurerm-ps.md)。</span><span class="sxs-lookup"><span data-stu-id="383b9-133">If you want to remove older versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="383b9-134">使用多个版本的 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="383b9-134">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="383b9-135">可以安装多个版本的 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="383b9-135">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="383b9-136">若要检查是否安装了多个版本的 Azure PowerShell，请使用以下命令：</span><span class="sxs-lookup"><span data-stu-id="383b9-136">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-Module -Name Az -List | select Name,Version
```

<span data-ttu-id="383b9-137">若要删除 Azure PowerShell 的某个版本，请参阅[卸载 Azure PowerShell 模块](uninstall-azurerm-ps.md)。</span><span class="sxs-lookup"><span data-stu-id="383b9-137">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

<span data-ttu-id="383b9-138">可以通过将 `-RequiredVersion` 参数与 `Install-Module` 和 `Import-Module` 配合使用来加载特定版本的 `Az` 模块：</span><span class="sxs-lookup"><span data-stu-id="383b9-138">You can load a specific version of the `Az` module by using the `-RequiredVersion` argument with `Install-Module` and `Import-Module`:</span></span>

```powershell-interactive
Install-Module -Name Az -RequiredVersion 0.4.0
Import-Module -Name Az -RequiredVersion 0.4.0
```

<span data-ttu-id="383b9-139">如果安装了该模块的多个版本，默认情况下会加载最新版本。</span><span class="sxs-lookup"><span data-stu-id="383b9-139">If you have more than one version of the module installed, the latest version is loaded by default.</span></span>

## <a name="provide-feedback"></a><span data-ttu-id="383b9-140">提供反馈</span><span class="sxs-lookup"><span data-stu-id="383b9-140">Provide feedback</span></span>

<span data-ttu-id="383b9-141">如果在使用 Azure Powershell 时发现了 bug，请[在 GitHub 上提出问题](https://github.com/Azure/azure-powershell/issues)。</span><span class="sxs-lookup"><span data-stu-id="383b9-141">If you find a bug when using Azure Powershell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="383b9-142">若要从命令行提供反馈，请使用 [Send-Feedback](/powershell/module/az.profile/send-feedback) cmdlet。</span><span class="sxs-lookup"><span data-stu-id="383b9-142">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.profile/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="383b9-143">后续步骤</span><span class="sxs-lookup"><span data-stu-id="383b9-143">Next Steps</span></span>

<span data-ttu-id="383b9-144">若要开始使用 Azure PowerShell，请参阅 [Azure PowerShell 入门](get-started-azureps.md)，详细了解此模块及其功能。</span><span class="sxs-lookup"><span data-stu-id="383b9-144">To get started using Azure PowerShell, see [Get Started with Azure PowerShell](get-started-azureps.md) to learn more about the module and its features.</span></span>
