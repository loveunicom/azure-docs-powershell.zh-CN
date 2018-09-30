---
title: 在 macOS 或 Linux 上安装 Azure PowerShell
description: 如何在 macOS 或 Linux 上安装 Azure PowerShell。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/24/2018
ms.openlocfilehash: 05e86d96b345455f3d3bb3fe6dedf933fff6187c
ms.sourcegitcommit: 19dffee617477001f98d43e39a50ce1fad087b74
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2018
ms.locfileid: "47179235"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a><span data-ttu-id="97d45-103">在 macOS 或 Linux 上安装 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="97d45-103">Install Azure PowerShell on macOS or Linux</span></span>

<span data-ttu-id="97d45-104">对于非 Windows 平台，可以在 PowerShell Core v6 中运行 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="97d45-104">For non-Windows platforms, it's possible to run Azure PowerShell in PowerShell Core v6.</span></span> <span data-ttu-id="97d45-105">此版 PowerShell 可以在支持 .NET Core 的任何平台上使用。</span><span class="sxs-lookup"><span data-stu-id="97d45-105">This version of PowerShell is built for use on any platform that supports .NET Core.</span></span> <span data-ttu-id="97d45-106">可以使用一个与这些平台兼容的 .NET Standard 版 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="97d45-106">To work with these platforms, there's a .NET Standard version of Azure PowerShell available.</span></span>

> [!NOTE]
> <span data-ttu-id="97d45-107">目前，PowerShell Core v6 和 Azure PowerShell for .NET Standard 都还是 Beta 版本。</span><span class="sxs-lookup"><span data-stu-id="97d45-107">At this time, both PowerShell Core v6 and Azure PowerShell for .NET Standard are still in beta.</span></span>
> <span data-ttu-id="97d45-108">对这些产品的支持也是有限的。</span><span class="sxs-lookup"><span data-stu-id="97d45-108">Support for these products is limited.</span></span> <span data-ttu-id="97d45-109">如果你有需要询问的问题或发现了 bug，请在 GitHub 上提出问题。</span><span class="sxs-lookup"><span data-stu-id="97d45-109">If you have problems or discover bugs, please file an issue on GitHub.</span></span>
>
> * [<span data-ttu-id="97d45-110">PowerShell Core v6 的问题</span><span class="sxs-lookup"><span data-stu-id="97d45-110">Issues for PowerShell Core v6</span></span>](https://github.com/PowerShell/PowerShell/issues)
> * [<span data-ttu-id="97d45-111">Azure PowerShell 的问题</span><span class="sxs-lookup"><span data-stu-id="97d45-111">Issues for Azure PowerShell</span></span>](https://github.com/azure/azure-docs-powershell/issues)

## <a name="install-powershell-core"></a><span data-ttu-id="97d45-112">安装 PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="97d45-112">Install PowerShell Core</span></span>

<span data-ttu-id="97d45-113">就 macOS 和大多数 Linux 发行版来说，PowerShell Core 的安装说明是不同的。</span><span class="sxs-lookup"><span data-stu-id="97d45-113">The installation instructions for PowerShell Core are different for macOS and most Linux distributions.</span></span>
<span data-ttu-id="97d45-114">可在以下文章中找到详细说明：</span><span class="sxs-lookup"><span data-stu-id="97d45-114">Detailed instructions can be found in the following articles:</span></span>

* [<span data-ttu-id="97d45-115">在 macOS 上安装 PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="97d45-115">Install PowerShell Core on macOS</span></span>](/powershell/scripting/setup/installing-powershell-core-on-macos)
* [<span data-ttu-id="97d45-116">在 Linux 上安装 PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="97d45-116">Install PowerShell Core on Linux</span></span>](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-standard"></a><span data-ttu-id="97d45-117">安装 Azure PowerShell for .NET Standard</span><span class="sxs-lookup"><span data-stu-id="97d45-117">Install Azure PowerShell for .NET Standard</span></span>

> [!IMPORTANT]
> <span data-ttu-id="97d45-118">在其他文章中详细介绍的 `AzureRM` 模块不兼容 PowerShell Core。</span><span class="sxs-lookup"><span data-stu-id="97d45-118">The `AzureRM` module detailed in other articles does not work with PowerShell Core.</span></span>
> <span data-ttu-id="97d45-119">必须安装 `Az` 模块才能获取 PowerShell Core 中的 Azure PowerShell 功能。</span><span class="sxs-lookup"><span data-stu-id="97d45-119">You must install the `Az` module to get Azure PowerShell functionality in PowerShell Core.</span></span>

<span data-ttu-id="97d45-120">PowerShell Core 附带已安装的 PowerShellGet 模块。</span><span class="sxs-lookup"><span data-stu-id="97d45-120">PowerShell Core comes with the PowerShellGet module already installed.</span></span> <span data-ttu-id="97d45-121">请使用以下命令启动 PowerShell：</span><span class="sxs-lookup"><span data-stu-id="97d45-121">Start PowerShell with the command:</span></span>

```bash
pwsh
```

<span data-ttu-id="97d45-122">若要安装 Azure PowerShell，请运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="97d45-122">To install Azure PowerShell, run the following command:</span></span>

```powershell
Install-Module Az
```

> [!NOTE]
> <span data-ttu-id="97d45-123">如果在尝试安装模块时遇到权限错误，则可能需要以超级用户模式运行 PowerShell 才能安装模块。</span><span class="sxs-lookup"><span data-stu-id="97d45-123">If you encounter a permissions error when attempting to install the module, you may need to run PowerShell in superuser mode to install modules.</span></span>
>
> ```bash
> sudo pwsh
> ```

<span data-ttu-id="97d45-124">默认情况下，PowerShell 库未配置为 PowerShellGet 的受信任存储库。</span><span class="sxs-lookup"><span data-stu-id="97d45-124">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="97d45-125">首次使用 PSGallery 时会看到以下提示：</span><span class="sxs-lookup"><span data-stu-id="97d45-125">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="97d45-126">请回答 `Yes` 或 `Yes to All` 继续安装。</span><span class="sxs-lookup"><span data-stu-id="97d45-126">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

## <a name="enable-aliases"></a><span data-ttu-id="97d45-127">启用别名</span><span class="sxs-lookup"><span data-stu-id="97d45-127">Enable aliases</span></span>

<span data-ttu-id="97d45-128">为了兼容现有的 `AzureRM` 模块，新的 `Az` 模块可以为 `AzureRM` cmdlet 创建后向兼容的别名。</span><span class="sxs-lookup"><span data-stu-id="97d45-128">For compatibility with the existing `AzureRM` module, the new `Az` module has the ability to create backwards compatible aliases for the `AzureRM` cmdlets.</span></span> <span data-ttu-id="97d45-129">第一次使用该模块之前，请使用以下命令设置这些别名：</span><span class="sxs-lookup"><span data-stu-id="97d45-129">Before using the module for the first time, set up these aliases with the following command:</span></span>

```powershell
# Import the module into the PowerShell session
Import-Module Az
# Enable AzureRM aliases for the user
Enable-AzureRmAlias -Scope CurrentUser
```

<span data-ttu-id="97d45-130">该命令只为当前用户设置别名。</span><span class="sxs-lookup"><span data-stu-id="97d45-130">This sets up aliases for the current user only.</span></span> <span data-ttu-id="97d45-131">请查看 cmdlet 帮助，了解可以为 `-Scope` 提供哪些其他的值来设置别名。</span><span class="sxs-lookup"><span data-stu-id="97d45-131">Check the cmdlet help for other values that can be provided to `-Scope` to set up the aliases.</span></span>

> [!NOTE]
> <span data-ttu-id="97d45-132">如果遇到有关路径位置的错误，请确保它存在于本地系统中。</span><span class="sxs-lookup"><span data-stu-id="97d45-132">If you encounter an error about a path location, make sure that it exists on your local system.</span></span> <span data-ttu-id="97d45-133">如果范围仅限 `CurrentUser`，则可通过在 `bash` 中运行以下命令来解决该错误：</span><span class="sxs-lookup"><span data-stu-id="97d45-133">For the `CurrentUser` scope, this error can be resolved by running the following command in `bash`:</span></span>
>
> ```bash
> mkdir -p $HOME/.config/powershell
> ```

## <a name="sign-in"></a><span data-ttu-id="97d45-134">登录</span><span class="sxs-lookup"><span data-stu-id="97d45-134">Sign in</span></span>

<span data-ttu-id="97d45-135">若要开始使用 Azure PowerShell，需使用 [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet 将 `Az` 加载到 PowerShell 会话中，然后使用 Azure 凭据登录。</span><span class="sxs-lookup"><span data-stu-id="97d45-135">To start working with Azure PowerShell, you need to load `Az` into your PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span> <span data-ttu-id="97d45-136">导入模块不需要提升的权限。</span><span class="sxs-lookup"><span data-stu-id="97d45-136">Importing a module does __not__ require elevated privileges.</span></span>

```powershell
# Import the module into the PowerShell session
Import-Module Az
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="97d45-137">需对每个启动的新 PowerShell 会话重复这些步骤。</span><span class="sxs-lookup"><span data-stu-id="97d45-137">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="97d45-138">自动导入 `Az` 模块要求设置 PowerShell 配置文件，详见[关于配置文件](/powershell/module/microsoft.powershell.core/about/about_profiles)。</span><span class="sxs-lookup"><span data-stu-id="97d45-138">Automatically importing the `Az` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="97d45-139">在 macOS 和 Linux 上，应通过 `$Profile` 环境变量来使用配置文件。</span><span class="sxs-lookup"><span data-stu-id="97d45-139">On macOS and Linux, you should work with your profile through the `$Profile` environment variable.</span></span> <span data-ttu-id="97d45-140">若要了解如何跨会话保持 Azure 登录状态，请参阅[跨 PowerShell 会话保持用户凭据](context-persistence.md)。</span><span class="sxs-lookup"><span data-stu-id="97d45-140">To learn how to persist your Azure sign-in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="97d45-141">后续步骤</span><span class="sxs-lookup"><span data-stu-id="97d45-141">Next Steps</span></span>

<span data-ttu-id="97d45-142">有关使用 Azure PowerShell 的详细信息，请参阅 [Azure PowerShell 入门](get-started-azureps.md)一文。</span><span class="sxs-lookup"><span data-stu-id="97d45-142">For more information about using Azure PowerShell, see the [Get started with Azure PowerShell](get-started-azureps.md) article.</span></span>
