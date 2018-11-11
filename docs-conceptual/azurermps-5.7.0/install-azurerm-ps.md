---
title: 使用 PowerShellGet 在 Windows 上安装 Azure PowerShell
description: 如何使用 PowerShellGet 安装 Azure PowerShell
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/15/2018
ms.openlocfilehash: a868a62bd7bb2f39775a3b7878e2c8484c50438d
ms.sourcegitcommit: ac4b53bb42a25aae013a9d8cd9ae98ada9397274
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/08/2018
ms.locfileid: "51274171"
---
# <a name="install-azure-powershell-on-windows-with-powershellget"></a><span data-ttu-id="28ce4-103">使用 PowerShellGet 在 Windows 上安装 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="28ce4-103">Install Azure PowerShell on Windows with PowerShellGet</span></span>

<span data-ttu-id="28ce4-104">本文介绍了在 Windows 环境中使用 PowerShellGet 安装 Azure PowerShell 模块的步骤。</span><span class="sxs-lookup"><span data-stu-id="28ce4-104">This article explains the steps to install the Azure PowerShell modules in a Windows environment using PowerShellGet.</span></span> <span data-ttu-id="28ce4-105">PowerShellGet 和模块管理是安装 Azure PowerShell 的首选方法，但是如果希望使用 Web 平台安装程序或 MSI 包进行安装，请参阅[其他安装方法](other-install.md)。</span><span class="sxs-lookup"><span data-stu-id="28ce4-105">PowerShellGet and module management is the preferred way to install Azure PowerShell but if you would rather install with the Web Platform Installer or MSI package, see [Other installation methods](other-install.md).</span></span>

<span data-ttu-id="28ce4-106">有关如何在其他平台上安装 Azure PowerShell 的说明，请参阅[在 macOS 和 Linux 上安装和配置 Azure PowerShell](install-azurermps-maclinux.md)。</span><span class="sxs-lookup"><span data-stu-id="28ce4-106">For instructions to install Azure PowerShell on other platforms, see [Install and configure Azure PowerShell on macOS and Linux](install-azurermps-maclinux.md).</span></span>

<span data-ttu-id="28ce4-107">此版 Azure PowerShell 不支持 Azure 经典部署模型。</span><span class="sxs-lookup"><span data-stu-id="28ce4-107">The Azure classic deployment model is not supported by this version of Azure PowerShell.</span></span> <span data-ttu-id="28ce4-108">若要获取经典部署的支持，请按[安装 Azure PowerShell 服务管理模块](/powershell/azure/servicemanagement/install-azure-ps)中的说明操作。</span><span class="sxs-lookup"><span data-stu-id="28ce4-108">For support for classic deployments, follow the instructions in [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span>

## <a name="requirements"></a><span data-ttu-id="28ce4-109">要求</span><span class="sxs-lookup"><span data-stu-id="28ce4-109">Requirements</span></span>

<span data-ttu-id="28ce4-110">若要安装 Azure PowerShell，则需 PowerShellGet 1.1.2.0 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="28ce4-110">To install Azure PowerShell, you need PowerShellGet version 1.1.2.0 or higher.</span></span> <span data-ttu-id="28ce4-111">若要查看它在系统上是否可用，请运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="28ce4-111">To check if it is available on your system, run the following command:</span></span>

```powershell-interactive
Get-Module -Name PowerShellGet -ListAvailable | Select-Object -Property Name,Version,Path
```

<span data-ttu-id="28ce4-112">应会看到类似于下面的信息：</span><span class="sxs-lookup"><span data-stu-id="28ce4-112">You should see something similar to the following output:</span></span>

```output
Name          Version Path
----          ------- ----
Name          Version Path
----          ------- ----
PowerShellGet 1.6.0   C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.6.0\PowerShellGet.psd1
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

<span data-ttu-id="28ce4-113">如需更新安装的 PowerShellGet，请运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="28ce4-113">If you need to update your installation of PowerShellGet, run the following command:</span></span>

```powershell-interactive
Install-Module PowerShellGet -Force
```

<span data-ttu-id="28ce4-114">如果尚未安装 PowerShellGet，请按下表中针对系统的说明操作。</span><span class="sxs-lookup"><span data-stu-id="28ce4-114">If you don't have PowerShellGet installed, follow the instructions in the table below for your system.</span></span>

|<span data-ttu-id="28ce4-115">场景</span><span class="sxs-lookup"><span data-stu-id="28ce4-115">Scenario</span></span>|<span data-ttu-id="28ce4-116">安装说明</span><span class="sxs-lookup"><span data-stu-id="28ce4-116">Install instructions</span></span>|
|---|---|
|<span data-ttu-id="28ce4-117">Windows 10</span><span class="sxs-lookup"><span data-stu-id="28ce4-117">Windows 10</span></span><br/><span data-ttu-id="28ce4-118">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="28ce4-118">Windows Server 2016</span></span>|<span data-ttu-id="28ce4-119">内置在 OS 随附的 Windows Management Framework (WMF) 5.0 中</span><span class="sxs-lookup"><span data-stu-id="28ce4-119">Built into Windows Management Framework (WMF) 5.0 included in the OS</span></span>|
|<span data-ttu-id="28ce4-120">升级到 PowerShell 5</span><span class="sxs-lookup"><span data-stu-id="28ce4-120">Upgrade to PowerShell 5</span></span>| <ol><li>[<span data-ttu-id="28ce4-121">安装最新版本的 WMF</span><span class="sxs-lookup"><span data-stu-id="28ce4-121">Install the latest version of WMF</span></span>](https://www.microsoft.com/en-us/download/details.aspx?id=54616)</li><li><span data-ttu-id="28ce4-122">运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="28ce4-122">Run the following command:</span></span><br/>```Install-Module PowerShellGet -Force```</li></ol>|
|<span data-ttu-id="28ce4-123">装有 PowerShell 3 或 PowerShell 4 的 Windows</span><span class="sxs-lookup"><span data-stu-id="28ce4-123">Windows with PowerShell 3 or PowerShell 4</span></span>|<ol><span data-ttu-id="28ce4-124"><il>[获取 PackageManagement 模块](http://go.microsoft.com/fwlink/?LinkID=746217)</il></span><span class="sxs-lookup"><span data-stu-id="28ce4-124"><il>[Get the PackageManagement modules](http://go.microsoft.com/fwlink/?LinkID=746217)</il></span></span><li><span data-ttu-id="28ce4-125">运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="28ce4-125">Run the following command:</span></span><br/>```Install-Module PowerShellGet -Force```</li></ol>|

> [!NOTE]
> <span data-ttu-id="28ce4-126">使用 PowerShellGet 需要一个允许运行脚本的执行策略。</span><span class="sxs-lookup"><span data-stu-id="28ce4-126">Using PowerShellGet requires an Execution Policy that allows you to run scripts.</span></span> <span data-ttu-id="28ce4-127">有关 PowerShell 执行策略的详细信息，请参阅[关于执行策略](/powershell/module/microsoft.powershell.core/about/about_execution_policies)。</span><span class="sxs-lookup"><span data-stu-id="28ce4-127">For more information about PowerShell's Execution Policy, see [About Execution Policies](/powershell/module/microsoft.powershell.core/about/about_execution_policies).</span></span>
>
> [!IMPORTANT]
> <span data-ttu-id="28ce4-128">本文档中介绍的模块 AzureRM 使用 .NET Framework。</span><span class="sxs-lookup"><span data-stu-id="28ce4-128">The module described in this document, AzureRM, uses .NET Framework.</span></span> <span data-ttu-id="28ce4-129">这使得它与使用 .NET Core 的 PowerShell 6.0 兼容。</span><span class="sxs-lookup"><span data-stu-id="28ce4-129">This makes it incompatible with PowerShell 6.0, which uses .NET Core.</span></span> <span data-ttu-id="28ce4-130">如果使用的是 PowerShell 6.0，请遵循[适用于 macOS 和 Linux 的安装说明](install-azurermps-maclinux.md)。</span><span class="sxs-lookup"><span data-stu-id="28ce4-130">If you are using PowerShell 6.0, follow the [installation instructions for macOS and Linux](install-azurermps-maclinux.md).</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="28ce4-131">安装 Azure Powershell 模块</span><span class="sxs-lookup"><span data-stu-id="28ce4-131">Install the Azure PowerShell module</span></span>

<span data-ttu-id="28ce4-132">需要提升的权限才能通过 PowerShell 库安装模块。</span><span class="sxs-lookup"><span data-stu-id="28ce4-132">You need elevated privileges to install modules from the PowerShell Gallery.</span></span> <span data-ttu-id="28ce4-133">若要安装 Azure PowerShell，请在已提升权限的会话中运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="28ce4-133">To install Azure PowerShell, run the following command in an elevated session:</span></span>

```powershell-interactive
Install-Module -Name AzureRM
```

> [!NOTE]
> <span data-ttu-id="28ce4-134">如果使用的 NuGet 版本低于 2.8.5.201，系统会提示下载并安装最新版本的 NuGet。</span><span class="sxs-lookup"><span data-stu-id="28ce4-134">If you have a version older than 2.8.5.201 of NuGet, you are prompted to download and install the latest version of NuGet.</span></span>

<span data-ttu-id="28ce4-135">默认情况下，PowerShell 库未配置为 PowerShellGet 的受信任存储库。</span><span class="sxs-lookup"><span data-stu-id="28ce4-135">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="28ce4-136">首次使用 PSGallery 时会看到以下提示：</span><span class="sxs-lookup"><span data-stu-id="28ce4-136">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="28ce4-137">请回答 `Yes` 或 `Yes to All` 继续安装。</span><span class="sxs-lookup"><span data-stu-id="28ce4-137">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="28ce4-138">`AzureRM` 模块是 Azure PowerShell cmdlet 的汇总模块。</span><span class="sxs-lookup"><span data-stu-id="28ce4-138">The `AzureRM` module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="28ce4-139">安装它时，系统会下载所有可用的 Azure 资源管理器模块并使其 cmdlet 可供使用。</span><span class="sxs-lookup"><span data-stu-id="28ce4-139">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="sign-in"></a><span data-ttu-id="28ce4-140">登录</span><span class="sxs-lookup"><span data-stu-id="28ce4-140">Sign in</span></span>

<span data-ttu-id="28ce4-141">若要开始使用 Azure PowerShell，需使用 [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet 将 `AzureRM` 加载到当前的 PowerShell 会话中，然后使用 Azure 凭据登录。</span><span class="sxs-lookup"><span data-stu-id="28ce4-141">To start working with Azure PowerShell, you need to load `AzureRM` into your current PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span>

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="28ce4-142">需对每个启动的新 PowerShell 会话重复这些步骤。</span><span class="sxs-lookup"><span data-stu-id="28ce4-142">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="28ce4-143">自动导入 `AzureRM` 模块要求设置 PowerShell 配置文件，详见[关于配置文件](/powershell/module/microsoft.powershell.core/about/about_profiles)。</span><span class="sxs-lookup"><span data-stu-id="28ce4-143">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="28ce4-144">若要了解如何跨会话保持 Azure 登录状态，请参阅[跨 PowerShell 会话保持用户凭据](context-persistence.md)。</span><span class="sxs-lookup"><span data-stu-id="28ce4-144">To learn how to persist your Azure sign in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="28ce4-145">更新 Azure PowerShell 模块</span><span class="sxs-lookup"><span data-stu-id="28ce4-145">Update the Azure PowerShell module</span></span>

<span data-ttu-id="28ce4-146">可以通过运行 [Update-Module](/powershell/module/powershellget/update-module) 来更新 Azure PowerShell 安装。</span><span class="sxs-lookup"><span data-stu-id="28ce4-146">You can update your Azure PowerShell installation by running [Update-Module](/powershell/module/powershellget/update-module).</span></span> <span data-ttu-id="28ce4-147">此命令不卸载以前的版本。</span><span class="sxs-lookup"><span data-stu-id="28ce4-147">This command does __not__ uninstall earlier versions.</span></span>

```powershell-interactive
Update-Module -Name AzureRM
```

<span data-ttu-id="28ce4-148">若要从系统中删除旧版 Azure PowerShell，请参阅[卸载 Azure PowerShell 模块](uninstall-azurerm-ps.md)。</span><span class="sxs-lookup"><span data-stu-id="28ce4-148">If you want to remove older versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="28ce4-149">使用多个版本的 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="28ce4-149">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="28ce4-150">可以安装多个版本的 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="28ce4-150">It's possible to install multiple versions of Azure PowerShell.</span></span> <span data-ttu-id="28ce4-151">如果使用本地 Azure Stack 资源、运行不能更新到 PowerShell 5.0 的旧版 Windows，或者使用 Azure 经典部署模型，则可能需要多个版本。</span><span class="sxs-lookup"><span data-stu-id="28ce4-151">You might need more than one version if you work with on-premises Azure Stack resources, run an older version of Windows that you can't update to PowerShell 5.0, or use the Azure classic deployment model.</span></span> <span data-ttu-id="28ce4-152">若要安装旧版本，请在安装时提供 `-RequiredVersion` 参数。</span><span class="sxs-lookup"><span data-stu-id="28ce4-152">To install an older version, provide the `-RequiredVersion` argument when installing.</span></span>

```powershell-interactive
# Install version 1.2.9 of Azure PowerShell
Install-Module -Name AzureRM -RequiredVersion 1.2.9
```

<span data-ttu-id="28ce4-153">加载 Azure PowerShell 模块时，默认加载最新版本。</span><span class="sxs-lookup"><span data-stu-id="28ce4-153">When loading the Azure PowerShell module the latest version is loaded by default.</span></span> <span data-ttu-id="28ce4-154">若要加载另一版本，请提供 `-RequiredVersion` 参数。</span><span class="sxs-lookup"><span data-stu-id="28ce4-154">To load a different version, provide the `-RequiredVersion` argument.</span></span>

```powershell-interactive
# Load version 1.2.9 of Azure PowerShell
Import-Module -Name AzureRM -RequiredVersion 1.2.9
```

## <a name="provide-feedback"></a><span data-ttu-id="28ce4-155">提供反馈</span><span class="sxs-lookup"><span data-stu-id="28ce4-155">Provide feedback</span></span>

<span data-ttu-id="28ce4-156">如果在使用 Azure Powershell 时发现 Bug，请[在 GitHub 上提出问题](https://github.com/Azure/azure-powershell/issues)。</span><span class="sxs-lookup"><span data-stu-id="28ce4-156">If you find a bug when using Azure Powershell, please [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="28ce4-157">若要从命令行提供反馈，请使用 [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet。</span><span class="sxs-lookup"><span data-stu-id="28ce4-157">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="28ce4-158">后续步骤</span><span class="sxs-lookup"><span data-stu-id="28ce4-158">Next Steps</span></span>

<span data-ttu-id="28ce4-159">若要开始使用 Azure PowerShell，请参阅 [Azure PowerShell 入门](get-started-azureps.md)，详细了解此模块及其功能。</span><span class="sxs-lookup"><span data-stu-id="28ce4-159">To get started using Azure PowerShell, see [Get Started with Azure PowerShell](get-started-azureps.md) to learn more about the module and its features.</span></span>