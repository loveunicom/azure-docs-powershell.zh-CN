---
title: 使用 PowerShellGet 安装 Azure PowerShell
description: 如何使用 PowerShellGet 安装 Azure PowerShell
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/29/2018
ms.openlocfilehash: c4af07816aaa6713d67e3349a45880f8cc22c80a
ms.sourcegitcommit: ac4b53bb42a25aae013a9d8cd9ae98ada9397274
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/08/2018
ms.locfileid: "51276025"
---
# <a name="install-azure-powershell-with-powershellget"></a><span data-ttu-id="935ec-103">使用 PowerShellGet 安装 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="935ec-103">Install Azure PowerShell with PowerShellGet</span></span>

<span data-ttu-id="935ec-104">本文介绍如何使用 PowerShellGet 安装 Azure PowerShell 模块。</span><span class="sxs-lookup"><span data-stu-id="935ec-104">This article tells you how to install the Azure PowerShell modules using PowerShellGet.</span></span> <span data-ttu-id="935ec-105">对于 Az 预览版，任何其他安装方法均不受支持。</span><span class="sxs-lookup"><span data-stu-id="935ec-105">For the preview release of Az, no other install methods are supported.</span></span> 

## <a name="requirements"></a><span data-ttu-id="935ec-106">要求</span><span class="sxs-lookup"><span data-stu-id="935ec-106">Requirements</span></span>

<span data-ttu-id="935ec-107">Azure PowerShell 在 Windows 上可与 PowerShell 5.x 配合工作，在任何平台上都可与 PowerShell 6.x 配合工作。</span><span class="sxs-lookup"><span data-stu-id="935ec-107">Azure PowerShell works with either PowerShell 5.x on Windows, or PowerShell 6.x on any platform.</span></span> <span data-ttu-id="935ec-108">若要查看在计算机上运行的 PowerShell 的版本，请运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="935ec-108">To check the version of PowerShell running on your machine, run the following command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="935ec-109">如果你的版本已过时或需要安装 PowerShell，请参阅[安装各种版本的 PowerShell](https://docs.microsoft.com/en-us/powershell/scripting/setup/installing-powershell?view=powershell-6)。</span><span class="sxs-lookup"><span data-stu-id="935ec-109">If you have an outdated version or need to install PowerShell, see [Installing various versions of PowerShell](https://docs.microsoft.com/en-us/powershell/scripting/setup/installing-powershell?view=powershell-6).</span></span> <span data-ttu-id="935ec-110">从该页面中的链接可访问适用于你的平台的安装信息。</span><span class="sxs-lookup"><span data-stu-id="935ec-110">Install information for your platform is linked from that page.</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="935ec-111">安装 Azure Powershell 模块</span><span class="sxs-lookup"><span data-stu-id="935ec-111">Install the Azure PowerShell module</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="935ec-112">一个系统上不应同时安装有 `AzureRM` 和 `Az` 模块。</span><span class="sxs-lookup"><span data-stu-id="935ec-112">You shouldn't have both the `AzureRM` and `Az` modules installed on a system at the same time.</span></span> <span data-ttu-id="935ec-113">若要安装 `Az` 模块，必须卸载 `AzureRM`。</span><span class="sxs-lookup"><span data-stu-id="935ec-113">In order to install the `Az` module, `AzureRM` must be uninstalled.</span></span> <span data-ttu-id="935ec-114">有关如何执行该操作的说明，请参阅[卸载 Azure PowerShell 模块 (AzureRM)](uninstall-azurerm-ps.md)。</span><span class="sxs-lookup"><span data-stu-id="935ec-114">For instructions on how to do that, see [Uninstall the Azure PowerShell module (AzureRM)](uninstall-azurerm-ps.md).</span></span>

<span data-ttu-id="935ec-115">若要在全局范围安装模块，需要具有提升的权限来安装 PowerShell 库中的模块。</span><span class="sxs-lookup"><span data-stu-id="935ec-115">To install modules at a global scope, you need elevated privileges to install modules from the PowerShell Gallery.</span></span> <span data-ttu-id="935ec-116">若要安装 Azure PowerShell，请在提升的会话中（在 Windows 上“以管理员身份运行”，或在 macOS 或 Linux 上使用超级用户权限）运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="935ec-116">To install Azure PowerShell, run the following command in an elevated session ("Run as Administrator" on Windows, or with superuser privileges on macOS or Linux):</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber
```

<span data-ttu-id="935ec-117">如果没有管理员权限，则可以通过添加 `-Scope` 参数为当前用户进行安装。</span><span class="sxs-lookup"><span data-stu-id="935ec-117">If you don't have access to administrator privileges, you can install for the current user by adding the `-Scope` argument.</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

<span data-ttu-id="935ec-118">默认情况下，PowerShell 库未配置为 PowerShellGet 的受信任存储库。</span><span class="sxs-lookup"><span data-stu-id="935ec-118">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="935ec-119">首次使用 PSGallery 时会看到以下提示：</span><span class="sxs-lookup"><span data-stu-id="935ec-119">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="935ec-120">请回答 `Yes` 或 `Yes to All` 继续安装。</span><span class="sxs-lookup"><span data-stu-id="935ec-120">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="935ec-121">`Az` 模块是 Azure PowerShell cmdlet 的汇总模块。</span><span class="sxs-lookup"><span data-stu-id="935ec-121">The `Az` module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="935ec-122">安装它时，系统会下载所有可用的 Azure 资源管理器模块并使其 cmdlet 可供使用。</span><span class="sxs-lookup"><span data-stu-id="935ec-122">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="sign-in"></a><span data-ttu-id="935ec-123">登录</span><span class="sxs-lookup"><span data-stu-id="935ec-123">Sign in</span></span>

<span data-ttu-id="935ec-124">若要开始使用 Azure PowerShell，需使用 [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet 将 `Az` 加载到当前的 PowerShell 会话中，然后使用 Azure 凭据登录。</span><span class="sxs-lookup"><span data-stu-id="935ec-124">To start working with Azure PowerShell, you need to load `Az` into your current PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span>

```powershell-interactive
# Import the module into the PowerShell session
Import-Module Az
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

<span data-ttu-id="935ec-125">需对每个启动的新 PowerShell 会话重复这些步骤。</span><span class="sxs-lookup"><span data-stu-id="935ec-125">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="935ec-126">自动导入 `Az` 模块要求设置 PowerShell 配置文件，详见[关于配置文件](/powershell/module/microsoft.powershell.core/about/about_profiles)。</span><span class="sxs-lookup"><span data-stu-id="935ec-126">Automatically importing the `Az` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="935ec-127">若要了解如何跨会话保持 Azure 登录状态，请参阅[跨 PowerShell 会话保持用户凭据](context-persistence.md)。</span><span class="sxs-lookup"><span data-stu-id="935ec-127">To learn how to persist your Azure sign-in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="935ec-128">更新 Azure PowerShell 模块</span><span class="sxs-lookup"><span data-stu-id="935ec-128">Update the Azure PowerShell module</span></span>

<span data-ttu-id="935ec-129">可以通过运行 [Update-Module](/powershell/module/powershellget/update-module) 来更新 Azure PowerShell 安装。</span><span class="sxs-lookup"><span data-stu-id="935ec-129">You can update your Azure PowerShell installation by running [Update-Module](/powershell/module/powershellget/update-module).</span></span> <span data-ttu-id="935ec-130">此命令不卸载以前的版本。</span><span class="sxs-lookup"><span data-stu-id="935ec-130">This command does __not__ uninstall earlier versions.</span></span>

```powershell-interactive
Update-Module -Name Az
```

<span data-ttu-id="935ec-131">若要从系统中删除旧版 Azure PowerShell，请参阅[卸载 Azure PowerShell 模块](uninstall-azurerm-ps.md)。</span><span class="sxs-lookup"><span data-stu-id="935ec-131">If you want to remove older versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="935ec-132">使用多个版本的 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="935ec-132">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="935ec-133">可以安装多个版本的 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="935ec-133">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="935ec-134">若要检查是否安装了多个版本的 Azure PowerShell，请使用以下命令：</span><span class="sxs-lookup"><span data-stu-id="935ec-134">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-Module -Name Az -List | select Name,Version
```

<span data-ttu-id="935ec-135">若要删除 Azure PowerShell 的某个版本，请参阅[卸载 Azure PowerShell 模块](uninstall-azurerm-ps.md)。</span><span class="sxs-lookup"><span data-stu-id="935ec-135">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

<span data-ttu-id="935ec-136">可以通过将 `-RequiredVersion` 参数与 `Install-Module` 或 `Import-Module` 配合使用来加载特定版本的 `Az`：</span><span class="sxs-lookup"><span data-stu-id="935ec-136">You can load a specific version of the `Az` module by using the `-RequiredVersion` argument with `Install-Module` or `Import-Module`:</span></span>

```powershell-interactive
Install-Module -Name Az -RequiredVersion 0.4.0
Import-Module -Name Az -RequiredVersion 0.4.0
```

<span data-ttu-id="935ec-137">如果安装了该模块的多个版本，导入时默认情况下会加载最新版本。</span><span class="sxs-lookup"><span data-stu-id="935ec-137">If you have more than one version of the module installed, the latest version is loaded by default when importing.</span></span>

## <a name="provide-feedback"></a><span data-ttu-id="935ec-138">提供反馈</span><span class="sxs-lookup"><span data-stu-id="935ec-138">Provide feedback</span></span>

<span data-ttu-id="935ec-139">如果在使用 Azure Powershell 时发现了 bug，请[在 GitHub 上提出问题](https://github.com/Azure/azure-powershell/issues)。</span><span class="sxs-lookup"><span data-stu-id="935ec-139">If you find a bug when using Azure Powershell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="935ec-140">若要从命令行提供反馈，请使用 [Send-Feedback](/powershell/module/az.profile/send-feedback) cmdlet。</span><span class="sxs-lookup"><span data-stu-id="935ec-140">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.profile/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="935ec-141">后续步骤</span><span class="sxs-lookup"><span data-stu-id="935ec-141">Next Steps</span></span>

<span data-ttu-id="935ec-142">若要开始使用 Azure PowerShell，请参阅 [Azure PowerShell 入门](get-started-azureps.md)，详细了解此模块及其功能。</span><span class="sxs-lookup"><span data-stu-id="935ec-142">To get started using Azure PowerShell, see [Get Started with Azure PowerShell](get-started-azureps.md) to learn more about the module and its features.</span></span>