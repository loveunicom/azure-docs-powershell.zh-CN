---
title: 使用 PowerShellGet 安装 Azure PowerShell
description: 如何使用 PowerShellGet 安装 Azure PowerShell
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/31/2018
ms.openlocfilehash: 9b7046157e32a5c8473210e9840f9ae1b2f45902
ms.sourcegitcommit: bcf80dfd7fbe17e82e7ad029802cfe8a2f02b15c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "35323095"
---
# <a name="install-azure-powershell-with-powershellget"></a><span data-ttu-id="b9f92-103">使用 PowerShellGet 安装 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="b9f92-103">Install Azure PowerShell with PowerShellGet</span></span>

<span data-ttu-id="b9f92-104">本文介绍了在 Windows 环境中使用 PowerShellGet 安装 Azure PowerShell 模块的步骤。</span><span class="sxs-lookup"><span data-stu-id="b9f92-104">This article explains the steps to install the Azure PowerShell modules in a Windows environment using PowerShellGet.</span></span>  <span data-ttu-id="b9f92-105">这是安装 Azure PowerShell 的首选方法，但是如果希望使用 Web 平台安装程序或 MSI 包进行安装，请参阅[其他安装方法](other-install.md)。</span><span class="sxs-lookup"><span data-stu-id="b9f92-105">This is the preferred way to install Azure PowerShell, but if you would rather install with the Web Platform Installer or MSI package, see [Other installation methods](other-install.md).</span></span>

<span data-ttu-id="b9f92-106">如果想要在 macOS 或 Linux 上使用 Azure PowerShell，请参阅以下文章：[在 macOS 和 Linux 上安装和配置 Azure PowerShell](install-azurermps-maclinux.md)。</span><span class="sxs-lookup"><span data-stu-id="b9f92-106">If you want to use Azure PowerShell on macOS or Linux, see the following article: [Install and configure Azure PowerShell on macOS and Linux](install-azurermps-maclinux.md).</span></span>

## <a name="system-requirements"></a><span data-ttu-id="b9f92-107">系统要求</span><span class="sxs-lookup"><span data-stu-id="b9f92-107">System requirements</span></span>

<span data-ttu-id="b9f92-108">Azure PowerShell 6.1.0 版要求使用 5.0 或更高版本的 PowerShell。</span><span class="sxs-lookup"><span data-stu-id="b9f92-108">Azure PowerShell version 6.1.0 requires version 5.0 (or higher) of PowerShell.</span></span> <span data-ttu-id="b9f92-109">有关升级到 PowerShell 5.0 的信息，请参阅[升级现有的 Windows PowerShell](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell)。</span><span class="sxs-lookup"><span data-stu-id="b9f92-109">For information on upgrading to PowerShell 5.0, see [Upgrading existing Windows PowerShell](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).</span></span>

<span data-ttu-id="b9f92-110">PowerShellGet 自动包括为 PowerShell 5.0 的一部分。</span><span class="sxs-lookup"><span data-stu-id="b9f92-110">PowerShellGet is automatically included as part of PowerShell 5.0.</span></span>

## <a name="install-or-update-the-azure-powershell-module"></a><span data-ttu-id="b9f92-111">安装或更新 Azure PowerShell 模块</span><span class="sxs-lookup"><span data-stu-id="b9f92-111">Install or update the Azure PowerShell module</span></span>

<span data-ttu-id="b9f92-112">从 PowerShell 库安装 Azure PowerShell 需要提升的特权。</span><span class="sxs-lookup"><span data-stu-id="b9f92-112">Installing Azure PowerShell from the PowerShell Gallery requires elevated privileges.</span></span> <span data-ttu-id="b9f92-113">从权限提升的 PowerShell 会话运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="b9f92-113">Run the following command from an elevated PowerShell session:</span></span>

```powershell
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

> [!IMPORTANT]
> <span data-ttu-id="b9f92-114">此命令将更新系统上任何现有的 Azure PowerShell 安装。</span><span class="sxs-lookup"><span data-stu-id="b9f92-114">This command will update any existing installation of Azure PowerShell on your system.</span></span> <span data-ttu-id="b9f92-115">如果需要安装多个版本，请参阅常见问题解答中的[是否可以安装 Azure PowerShell 的多个版本？](#multiple-versions)</span><span class="sxs-lookup"><span data-stu-id="b9f92-115">If you need to have more than one version installed, see the FAQ answer for [Can I install multiple versions of Azure PowerShell?](#multiple-versions)</span></span>

<span data-ttu-id="b9f92-116">默认情况下，PowerShell 库未配置为 PowerShellGet 的受信任存储库。</span><span class="sxs-lookup"><span data-stu-id="b9f92-116">By default, the PowerShell gallery is not configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="b9f92-117">首次使用 PSGallery 时会看到以下提示：</span><span class="sxs-lookup"><span data-stu-id="b9f92-117">The first time you use the PSGallery you see the following prompt:</span></span>

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="b9f92-118">回答“是”或“全部确认”，可继续进行安装。</span><span class="sxs-lookup"><span data-stu-id="b9f92-118">Answer 'Yes' or 'Yes to All' to continue with the installation.</span></span>

> [!NOTE]
> <span data-ttu-id="b9f92-119">如果使用的 NuGet 版本低于 2.8.5.201，系统会提示下载并安装最新版本的 NuGet。</span><span class="sxs-lookup"><span data-stu-id="b9f92-119">If you have a version older than 2.8.5.201 of NuGet, you are prompted to download and install the latest version of NuGet.</span></span>

<span data-ttu-id="b9f92-120">AzureRM 模块是 Azure 资源管理器 cmdlet 的汇总模块。</span><span class="sxs-lookup"><span data-stu-id="b9f92-120">The AzureRM module is a rollup module for the Azure Resource Manager cmdlets.</span></span> <span data-ttu-id="b9f92-121">安装 AzureRM 模块时，将从 PowerShell 库下载先前未安装的所有 Azure PowerShell 模块。</span><span class="sxs-lookup"><span data-stu-id="b9f92-121">When you install the AzureRM module, any Azure PowerShell module not previously installed is downloaded from the PowerShell Gallery.</span></span>

## <a name="load-the-azure-powershell-module"></a><span data-ttu-id="b9f92-122">加载 Azure PowerShell 模块</span><span class="sxs-lookup"><span data-stu-id="b9f92-122">Load the Azure PowerShell module</span></span>

<span data-ttu-id="b9f92-123">安装该模块后，需要将它加载到 PowerShell 会话中。</span><span class="sxs-lookup"><span data-stu-id="b9f92-123">Once the module is installed, you need to load the module into your PowerShell session.</span></span> <span data-ttu-id="b9f92-124">应该在正常（而非提升）的 PowerShell 会话中执行此操作。</span><span class="sxs-lookup"><span data-stu-id="b9f92-124">You should do this in a normal (non-elevated) PowerShell session.</span></span> <span data-ttu-id="b9f92-125">可以使用 `Import-Module` cmdlet 加载模块，如下所示：</span><span class="sxs-lookup"><span data-stu-id="b9f92-125">Modules are loaded using the `Import-Module` cmdlet, as follows:</span></span>

```powershell
Import-Module -Name AzureRM
```

## <a name="reporting-issues-and-feedback"></a><span data-ttu-id="b9f92-126">报告问题和反馈</span><span class="sxs-lookup"><span data-stu-id="b9f92-126">Reporting issues and feedback</span></span>

<span data-ttu-id="b9f92-127">如果遇到工具的任何 bug，请[在 GitHub 上提出问题](https://github.com/Azure/azure-powershell/issues)。</span><span class="sxs-lookup"><span data-stu-id="b9f92-127">If you encounter any bugs with the tool, please [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span> <span data-ttu-id="b9f92-128">若要从命令行提供反馈，请使用 `Send-Feedback` cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b9f92-128">To provide feedback from the command line, use the `Send-Feedback` cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="b9f92-129">后续步骤</span><span class="sxs-lookup"><span data-stu-id="b9f92-129">Next Steps</span></span>

<span data-ttu-id="b9f92-130">有关使用 Azure PowerShell 的详细信息，请参阅以下文章：</span><span class="sxs-lookup"><span data-stu-id="b9f92-130">For more information about using Azure PowerShell, see the following articles:</span></span>

* [<span data-ttu-id="b9f92-131">Azure PowerShell 入门</span><span class="sxs-lookup"><span data-stu-id="b9f92-131">Get started with Azure PowerShell</span></span>](get-started-azureps.md)

## <a name="frequently-asked-questions"></a><span data-ttu-id="b9f92-132">常见问题</span><span class="sxs-lookup"><span data-stu-id="b9f92-132">Frequently asked questions</span></span>

### <a id="helpmechoose"></a><span data-ttu-id="b9f92-133">如何检查 Azure PowerShell 的版本？</span><span class="sxs-lookup"><span data-stu-id="b9f92-133">How do I check the version of Azure PowerShell?</span></span>

<span data-ttu-id="b9f92-134">虽然建议尽早升级到最新版本，但仍然支持多个 Azure PowerShell 版本。</span><span class="sxs-lookup"><span data-stu-id="b9f92-134">Although we encourage you to upgrade to the latest version as early as possible, several versions of Azure PowerShell are supported.</span></span> <span data-ttu-id="b9f92-135">若要确定安装的 Azure PowerShell 版本，请从命令行运行 `Get-Module AzureRM`。</span><span class="sxs-lookup"><span data-stu-id="b9f92-135">To determine the version of Azure PowerShell you have installed, run `Get-Module AzureRM` from your command line.</span></span>

```powershell
Get-Module AzureRM -ListAvailable | Select-Object -Property Name,Version,Path
```

### <a name="can-i-use-azure-powershell-for-azure-classic-deployments"></a><span data-ttu-id="b9f92-136">是否可以使用 Azure PowerShell 进行 Azure 经典部署？</span><span class="sxs-lookup"><span data-stu-id="b9f92-136">Can I use Azure PowerShell for Azure Classic deployments?</span></span>

<span data-ttu-id="b9f92-137">如果部署使用了经典部署模型，则可以安装 Azure PowerShell 的服务管理版本。</span><span class="sxs-lookup"><span data-stu-id="b9f92-137">If you have deployments that use the classic deployment model you can install the Service Management version of Azure PowerShell.</span></span> <span data-ttu-id="b9f92-138">有关详细信息，请参阅[安装 Azure PowerShell 服务管理模块](/powershell/azure/servicemanagement/install-azure-ps)。</span><span class="sxs-lookup"><span data-stu-id="b9f92-138">For more information, see [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span> <span data-ttu-id="b9f92-139">Azure 和 AzureRM 模块共享通用的依赖项。</span><span class="sxs-lookup"><span data-stu-id="b9f92-139">The Azure and AzureRM modules share common dependencies.</span></span> <span data-ttu-id="b9f92-140">如果同时使用 Azure 和 AzureRM 模块，应该安装每个包的同一版本。</span><span class="sxs-lookup"><span data-stu-id="b9f92-140">If you use both the Azure and AzureRM modules, you should install the same version of each package.</span></span>

### <a name="a-namemultiple-versionscan-i-install-multiple-versions-of-azure-powershell"></a><span data-ttu-id="b9f92-141"><a name="multiple-versions"/>是否可以安装 Azure PowerShell 的多个版本？</span><span class="sxs-lookup"><span data-stu-id="b9f92-141"><a name="multiple-versions"/>Can I install multiple versions of Azure PowerShell?</span></span>

<span data-ttu-id="b9f92-142">PowerShellGet 是唯一支持多个版本的安装方法。</span><span class="sxs-lookup"><span data-stu-id="b9f92-142">PowerShellGet the only method of installation that supports multiple versions.</span></span> <span data-ttu-id="b9f92-143">若要安装多个版本，可以向 `Install-Module` cmdlet 中添加 `-RequiredVersion` 参数。</span><span class="sxs-lookup"><span data-stu-id="b9f92-143">To install multiple versions, you can add the `-RequiredVersion` parameter to the `Install-Module` cmdlet.</span></span> <span data-ttu-id="b9f92-144">例如，若要同时安装 6.1.0 和 1.2.9 这两个版本，请使用以下命令：</span><span class="sxs-lookup"><span data-stu-id="b9f92-144">For example, to install both versions 6.1.0 and 1.2.9:</span></span>

```powershell
Install-Module -Name AzureRM -RequiredVersion 6.1.0
Install-Module -Name AzureRM -RequiredVersion 1.2.9
```

<span data-ttu-id="b9f92-145">在一个 PowerShell 会话中只能加载一个模块版本。</span><span class="sxs-lookup"><span data-stu-id="b9f92-145">Only one version of the module can be loaded in a PowerShell session.</span></span> <span data-ttu-id="b9f92-146">必须打开一个新的 PowerShell 窗口，并使用 `Import-Module` 导入 Azure PowerShell 模块的特定版本。</span><span class="sxs-lookup"><span data-stu-id="b9f92-146">You must open a new PowerShell window and use `Import-Module` to import a specific version of the Azure PowerShell module.</span></span>

```powershell
Import-Module -Name AzureRM -RequiredVersion 1.2.9
```

> [!NOTE]
> <span data-ttu-id="b9f92-147">版本 2.1.0 和 1.2.6 是可以同时安装和使用的初始模块版本。</span><span class="sxs-lookup"><span data-stu-id="b9f92-147">Version 2.1.0 and version 1.2.6 are the first module versions designed to be installed and used side by side.</span></span> <span data-ttu-id="b9f92-148">加载 Azure PowerShell 早期版本时，会加载不兼容版本的 **AzureRM.Profile** 模块。</span><span class="sxs-lookup"><span data-stu-id="b9f92-148">When loading an earlier version of the Azure PowerShell, incompatible versions of the **AzureRM.Profile** module are loaded.</span></span> <span data-ttu-id="b9f92-149">这会导致在执行 cmdlet 时，cmdlet 会提示用户登录。</span><span class="sxs-lookup"><span data-stu-id="b9f92-149">This results in the cmdlets prompting you to log in whenever you execute a cmdlet.</span></span>
