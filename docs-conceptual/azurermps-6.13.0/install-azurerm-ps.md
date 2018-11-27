---
title: 使用 PowerShellGet 在 Windows 上安装 Azure PowerShell
description: 如何使用 PowerShellGet 安装 Azure PowerShell
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/16/2018
ms.openlocfilehash: 0830f3e00f85d3b69eff9a999bdb6c3e952cf360
ms.sourcegitcommit: 80a3da199954d0ab78765715fb49793e89a30f12
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/22/2018
ms.locfileid: "52259389"
---
# <a name="install-azure-powershell-on-windows-with-powershellget"></a><span data-ttu-id="e5f8f-103">使用 PowerShellGet 在 Windows 上安装 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="e5f8f-103">Install Azure PowerShell on Windows with PowerShellGet</span></span>

<span data-ttu-id="e5f8f-104">本文介绍了在 Windows 环境中使用 PowerShellGet 安装 Azure PowerShell 模块的步骤。</span><span class="sxs-lookup"><span data-stu-id="e5f8f-104">This article explains the steps to install the Azure PowerShell modules in a Windows environment using PowerShellGet.</span></span> <span data-ttu-id="e5f8f-105">PowerShellGet 和模块管理是安装 Azure PowerShell 的首选方法，但是如果希望使用 Web 平台安装程序或 MSI 包进行安装，请参阅[其他安装方法](other-install.md)。</span><span class="sxs-lookup"><span data-stu-id="e5f8f-105">PowerShellGet and module management is the preferred way to install Azure PowerShell but if you would rather install with the Web Platform Installer or MSI package, see [Other installation methods](other-install.md).</span></span>

<span data-ttu-id="e5f8f-106">有关如何在其他平台上安装 Azure PowerShell 的说明，请参阅[在 macOS 和 Linux 上安装和配置 Azure PowerShell](install-azurermps-maclinux.md)。</span><span class="sxs-lookup"><span data-stu-id="e5f8f-106">For instructions to install Azure PowerShell on other platforms, see [Install and configure Azure PowerShell on macOS and Linux](install-azurermps-maclinux.md).</span></span>

<span data-ttu-id="e5f8f-107">此版 Azure PowerShell 不支持 Azure 经典部署模型。</span><span class="sxs-lookup"><span data-stu-id="e5f8f-107">The Azure classic deployment model is not supported by this version of Azure PowerShell.</span></span> <span data-ttu-id="e5f8f-108">若要获取经典部署的支持，请按[安装 Azure PowerShell 服务管理模块](/powershell/azure/servicemanagement/install-azure-ps)中的说明操作。</span><span class="sxs-lookup"><span data-stu-id="e5f8f-108">For support for classic deployments, follow the instructions in [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span>

[!INCLUDE[az-replacing-azurerm](../includes/az-replacing-azurerm.md)]

## <a name="requirements"></a><span data-ttu-id="e5f8f-109">要求</span><span class="sxs-lookup"><span data-stu-id="e5f8f-109">Requirements</span></span>

<span data-ttu-id="e5f8f-110">从 Azure PowerShell 版本 6.0 开始，Azure PowerShell 需要 PowerShell 版本 5.0。</span><span class="sxs-lookup"><span data-stu-id="e5f8f-110">Starting with Azure PowerShell version 6.0, Azure PowerShell requires PowerShell version 5.0.</span></span> <span data-ttu-id="e5f8f-111">若要查看在计算机上运行的 PowerShell 的版本，请运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="e5f8f-111">To check the version of PowerShell running on your machine, run the following command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="e5f8f-112">如果版本已过时，请参阅[升级现有的 Windows PowerShell](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell)。</span><span class="sxs-lookup"><span data-stu-id="e5f8f-112">If you have an outdated version, see [Upgrading existing Windows PowerShell](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e5f8f-113">本文档中介绍的模块 AzureRM 使用 .NET Framework。</span><span class="sxs-lookup"><span data-stu-id="e5f8f-113">The module described in this document, AzureRM, uses .NET Framework.</span></span> <span data-ttu-id="e5f8f-114">这使得它与使用 .NET Core 的 PowerShell 6.0 兼容。</span><span class="sxs-lookup"><span data-stu-id="e5f8f-114">This makes it incompatible with PowerShell 6.0, which uses .NET Core.</span></span> <span data-ttu-id="e5f8f-115">如果使用的是 PowerShell 6.0，请遵循[适用于 macOS 和 Linux 的安装说明](install-azurermps-maclinux.md)。</span><span class="sxs-lookup"><span data-stu-id="e5f8f-115">If you are using PowerShell 6.0, follow the [installation instructions for macOS and Linux](install-azurermps-maclinux.md).</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="e5f8f-116">安装 Azure Powershell 模块</span><span class="sxs-lookup"><span data-stu-id="e5f8f-116">Install the Azure PowerShell module</span></span>

<span data-ttu-id="e5f8f-117">需要提升的权限才能通过 PowerShell 库安装模块。</span><span class="sxs-lookup"><span data-stu-id="e5f8f-117">You need elevated privileges to install modules from the PowerShell Gallery.</span></span> <span data-ttu-id="e5f8f-118">若要安装 Azure PowerShell，请在已提升权限的会话中运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="e5f8f-118">To install Azure PowerShell, run the following command in an elevated session:</span></span>

```powershell-interactive
Install-Module -Name AzureRM -AllowClobber
```

> [!NOTE]
> <span data-ttu-id="e5f8f-119">如果使用的 NuGet 版本低于 2.8.5.201，系统会提示下载并安装最新版本的 NuGet。</span><span class="sxs-lookup"><span data-stu-id="e5f8f-119">If you have a version older than 2.8.5.201 of NuGet, you are prompted to download and install the latest version of NuGet.</span></span>

<span data-ttu-id="e5f8f-120">默认情况下，PowerShell 库未配置为 PowerShellGet 的受信任存储库。</span><span class="sxs-lookup"><span data-stu-id="e5f8f-120">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="e5f8f-121">首次使用 PSGallery 时会看到以下提示：</span><span class="sxs-lookup"><span data-stu-id="e5f8f-121">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="e5f8f-122">请回答 `Yes` 或 `Yes to All` 继续安装。</span><span class="sxs-lookup"><span data-stu-id="e5f8f-122">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="e5f8f-123">`AzureRM` 模块是 Azure PowerShell cmdlet 的汇总模块。</span><span class="sxs-lookup"><span data-stu-id="e5f8f-123">The `AzureRM` module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="e5f8f-124">安装它时，系统会下载所有可用的 Azure 资源管理器模块并使其 cmdlet 可供使用。</span><span class="sxs-lookup"><span data-stu-id="e5f8f-124">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="sign-in"></a><span data-ttu-id="e5f8f-125">登录</span><span class="sxs-lookup"><span data-stu-id="e5f8f-125">Sign in</span></span>

<span data-ttu-id="e5f8f-126">若要开始使用 Azure PowerShell，请通过 Azure 凭据登录。</span><span class="sxs-lookup"><span data-stu-id="e5f8f-126">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

> [!NOTE]
>
> <span data-ttu-id="e5f8f-127">如果已禁用模块自动加载，则需使用 `Import-Module AzureRM` 手动导入模块。</span><span class="sxs-lookup"><span data-stu-id="e5f8f-127">If you've disabled module autoloading, you need to manually import the module with `Import-Module AzureRM`.</span></span> <span data-ttu-id="e5f8f-128">考虑到模块的构造方式，这可能需要几秒钟时间。</span><span class="sxs-lookup"><span data-stu-id="e5f8f-128">Because of the way the module is structured, this can take a few seconds.</span></span>


<span data-ttu-id="e5f8f-129">需对每个启动的新 PowerShell 会话重复这些步骤。</span><span class="sxs-lookup"><span data-stu-id="e5f8f-129">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="e5f8f-130">若要了解如何跨 PowerShell 会话保持 Azure 登录状态，请参阅[跨 PowerShell 会话保持用户凭据](context-persistence.md)。</span><span class="sxs-lookup"><span data-stu-id="e5f8f-130">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="e5f8f-131">更新 Azure PowerShell 模块</span><span class="sxs-lookup"><span data-stu-id="e5f8f-131">Update the Azure PowerShell module</span></span>

<span data-ttu-id="e5f8f-132">可以通过运行 [Update-Module](/powershell/module/powershellget/update-module) 来更新 Azure PowerShell 安装。</span><span class="sxs-lookup"><span data-stu-id="e5f8f-132">You can update your Azure PowerShell installation by running [Update-Module](/powershell/module/powershellget/update-module).</span></span> <span data-ttu-id="e5f8f-133">此命令不卸载以前的版本。</span><span class="sxs-lookup"><span data-stu-id="e5f8f-133">This command does __not__ uninstall earlier versions.</span></span>

```powershell-interactive
Update-Module -Name AzureRM
```

<span data-ttu-id="e5f8f-134">若要从系统中删除旧版 Azure PowerShell，请参阅[卸载 Azure PowerShell 模块](uninstall-azurerm-ps.md)。</span><span class="sxs-lookup"><span data-stu-id="e5f8f-134">If you want to remove older versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="e5f8f-135">使用多个版本的 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="e5f8f-135">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="e5f8f-136">可以安装多个版本的 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="e5f8f-136">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="e5f8f-137">若要检查是否安装了多个版本的 Azure PowerShell，请使用以下命令：</span><span class="sxs-lookup"><span data-stu-id="e5f8f-137">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-Module -Name AzureRM -List | select Name,Version
```

<span data-ttu-id="e5f8f-138">若要删除 Azure PowerShell 的某个版本，请参阅[卸载 Azure PowerShell 模块](uninstall-azurerm-ps.md)。</span><span class="sxs-lookup"><span data-stu-id="e5f8f-138">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

<span data-ttu-id="e5f8f-139">如果使用本地 Azure Stack 资源、运行旧版 Windows，或使用 Azure 经典部署模型，则可能需要多个版本。</span><span class="sxs-lookup"><span data-stu-id="e5f8f-139">You might need more than one version if you work with on-premises Azure Stack resources, run an older version of Windows, or use the Azure classic deployment model.</span></span> <span data-ttu-id="e5f8f-140">若要安装旧版本，请在安装时提供 `-RequiredVersion` 参数。</span><span class="sxs-lookup"><span data-stu-id="e5f8f-140">To install an older version, provide the `-RequiredVersion` argument when installing.</span></span>

```powershell-interactive
# Install version 1.2.9 of Azure PowerShell
Install-Module -Name AzureRM -RequiredVersion 1.2.9
```

<span data-ttu-id="e5f8f-141">加载 Azure PowerShell 模块时，默认加载最新版本。</span><span class="sxs-lookup"><span data-stu-id="e5f8f-141">When loading the Azure PowerShell module the latest version is loaded by default.</span></span> <span data-ttu-id="e5f8f-142">若要加载另一版本，请提供 `-RequiredVersion` 参数。</span><span class="sxs-lookup"><span data-stu-id="e5f8f-142">To load a different version, provide the `-RequiredVersion` argument.</span></span>

```powershell-interactive
# Load version 1.2.9 of Azure PowerShell
Import-Module -Name AzureRM -RequiredVersion 1.2.9
```

## <a name="provide-feedback"></a><span data-ttu-id="e5f8f-143">提供反馈</span><span class="sxs-lookup"><span data-stu-id="e5f8f-143">Provide feedback</span></span>

<span data-ttu-id="e5f8f-144">如果在使用 Azure Powershell 时发现了 bug，请[在 GitHub 上提出问题](https://github.com/Azure/azure-powershell/issues)。</span><span class="sxs-lookup"><span data-stu-id="e5f8f-144">If you find a bug when using Azure Powershell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="e5f8f-145">若要从命令行提供反馈，请使用 [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e5f8f-145">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="e5f8f-146">后续步骤</span><span class="sxs-lookup"><span data-stu-id="e5f8f-146">Next Steps</span></span>

<span data-ttu-id="e5f8f-147">若要开始使用 Azure PowerShell，请参阅 [Azure PowerShell 入门](get-started-azureps.md)，详细了解此模块及其功能。</span><span class="sxs-lookup"><span data-stu-id="e5f8f-147">To get started using Azure PowerShell, see [Get Started with Azure PowerShell](get-started-azureps.md) to learn more about the module and its features.</span></span>
