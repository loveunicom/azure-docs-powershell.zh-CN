---
title: 安装和配置 Azure PowerShell | Microsoft Docs
description: 如何安装和配置首次使用的 Azure PowerShell。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/27/2018
ms.openlocfilehash: 8819a0ba2dfb6bc3f88e80581257180aa1558ba4
ms.sourcegitcommit: c98e3a21037ebd82936828bcb544eed902b24212
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/08/2018
ms.locfileid: "34853808"
---
# <a name="install-and-configure-azure-powershell"></a><span data-ttu-id="af106-103">安装和配置 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="af106-103">Install and configure Azure PowerShell</span></span>

<span data-ttu-id="af106-104">本文介绍了在 Windows 环境中安装 Azure PowerShell 模块的步骤。</span><span class="sxs-lookup"><span data-stu-id="af106-104">This article explains the steps to install the Azure PowerShell modules in a Windows environment.</span></span>
<span data-ttu-id="af106-105">如果想要在 macOS 或 Linux 上使用 Azure PowerShell，请参阅以下文章：[在 macOS 和 Linux 上安装和配置 Azure PowerShell](install-azurermps-maclinux.md)。</span><span class="sxs-lookup"><span data-stu-id="af106-105">If you want to use Azure PowerShell on macOS or Linux, see the following article: [Install and configure Azure PowerShell on macOS and Linux](install-azurermps-maclinux.md).</span></span>

<span data-ttu-id="af106-106">从 PowerShell 库安装 Azure PowerShell 是首选的安装方法。</span><span class="sxs-lookup"><span data-stu-id="af106-106">Installing Azure PowerShell from the PowerShell Gallery is the preferred method of installation.</span></span>

## <a name="step-1-install-powershellget"></a><span data-ttu-id="af106-107">步骤 1：安装 PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="af106-107">Step 1: Install PowerShellGet</span></span>

<span data-ttu-id="af106-108">安装 PowerShell 库中的项需要 PowerShellGet 模块。</span><span class="sxs-lookup"><span data-stu-id="af106-108">Installing items from the PowerShell Gallery requires the PowerShellGet module.</span></span> <span data-ttu-id="af106-109">请确保使用适当版本的 PowerShellGet 并满足其他系统要求。</span><span class="sxs-lookup"><span data-stu-id="af106-109">Make sure you have the appropriate version of PowerShellGet and other system requirements.</span></span> <span data-ttu-id="af106-110">运行以下命令，确定是否已在系统上安装 PowerShellGet。</span><span class="sxs-lookup"><span data-stu-id="af106-110">Run the following command to see if you have PowerShellGet installed on your system.</span></span>

```powershell
Get-Module -Name PowerShellGet -ListAvailable | Select-Object -Property Name,Version,Path
```

<span data-ttu-id="af106-111">应会看到类似于下面的信息：</span><span class="sxs-lookup"><span data-stu-id="af106-111">You should see something similar to the following output:</span></span>

```Output
Name          Version Path
----          ------- ----
Name          Version Path
----          ------- ----
PowerShellGet 1.6.0   C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.6.0\PowerShellGet.psd1
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

<span data-ttu-id="af106-112">需要 PowerShellGet 版本 1.1.2.0 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="af106-112">You need PowerShellGet version 1.1.2.0 or higher.</span></span> <span data-ttu-id="af106-113">若要更新 PowerShellGet，请使用以下命令：</span><span class="sxs-lookup"><span data-stu-id="af106-113">To update PowerShellGet, use the following command:</span></span>

```powershell
Install-Module PowerShellGet -Force
```

<span data-ttu-id="af106-114">如果没有安装 PowerShellGet，请参阅本文的[如何获取 PowerShellGet](#how-to-get-powershellget) 部分。</span><span class="sxs-lookup"><span data-stu-id="af106-114">If you do not have PowerShellGet installed, see the [How to get PowerShellGet](#how-to-get-powershellget) section of this article.</span></span>

> [!NOTE]
> <span data-ttu-id="af106-115">使用 PowerShellGet 需要一个允许运行脚本的执行策略。</span><span class="sxs-lookup"><span data-stu-id="af106-115">Using PowerShellGet requires an Execution Policy that allows you to run scripts.</span></span> <span data-ttu-id="af106-116">有关 PowerShell 执行策略的详细信息，请参阅[关于执行策略](/powershell/module/microsoft.powershell.core/about/about_execution_policies)。</span><span class="sxs-lookup"><span data-stu-id="af106-116">For more information about PowerShell's Execution Policy, see [About Execution Policies](/powershell/module/microsoft.powershell.core/about/about_execution_policies).</span></span>

## <a name="step-2-install-azure-powershell"></a><span data-ttu-id="af106-117">步骤 2：安装 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="af106-117">Step 2: Install Azure PowerShell</span></span>

<span data-ttu-id="af106-118">从 PowerShell 库安装 Azure PowerShell 需要提升的特权。</span><span class="sxs-lookup"><span data-stu-id="af106-118">Installing Azure PowerShell from the PowerShell Gallery requires elevated privileges.</span></span> <span data-ttu-id="af106-119">从权限提升的 PowerShell 会话运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="af106-119">Run the following command from an elevated PowerShell session:</span></span>

```powershell
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

<span data-ttu-id="af106-120">默认情况下，PowerShell 库未配置为 PowerShellGet 的受信任存储库。</span><span class="sxs-lookup"><span data-stu-id="af106-120">By default, the PowerShell gallery is not configured as a Trusted repository for PowerShellGet.</span></span> <span data-ttu-id="af106-121">首次使用 PSGallery 时会看到以下提示：</span><span class="sxs-lookup"><span data-stu-id="af106-121">The first time you use the PSGallery you see the following prompt:</span></span>

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"): Y
```

<span data-ttu-id="af106-122">回答“是”或“全部确认”，可继续进行安装。</span><span class="sxs-lookup"><span data-stu-id="af106-122">Answer 'Yes' or 'Yes to All' to continue with the installation.</span></span>

> [!NOTE]
> <span data-ttu-id="af106-123">如果使用的 NuGet 版本低于 2.8.5.201，系统会提示下载并安装最新版本的 NuGet。</span><span class="sxs-lookup"><span data-stu-id="af106-123">If you have a version older than 2.8.5.201 of NuGet, you are prompted to download and install the latest version of NuGet.</span></span>

<span data-ttu-id="af106-124">AzureRM 模块是 Azure 资源管理器 cmdlet 的汇总模块。</span><span class="sxs-lookup"><span data-stu-id="af106-124">The AzureRM module is a rollup module for the Azure Resource Manager cmdlets.</span></span> <span data-ttu-id="af106-125">安装 AzureRM 模块时，将从 PowerShell 库下载先前未安装的所有 Azure PowerShell 模块。</span><span class="sxs-lookup"><span data-stu-id="af106-125">When you install the AzureRM module, any Azure PowerShell module not previously installed is downloaded and from the PowerShell Gallery.</span></span>

<span data-ttu-id="af106-126">如果安装了早期版本的 Azure PowerShell，可能会出错。</span><span class="sxs-lookup"><span data-stu-id="af106-126">If you have a previous version of Azure PowerShell installed you may receive an error.</span></span> <span data-ttu-id="af106-127">若要解决此问题，请参阅本文中的[更新到新版 Azure PowerShell](#update-azps) 部分。</span><span class="sxs-lookup"><span data-stu-id="af106-127">To resolve this issue, see the [Updating to a new version of Azure PowerShell](#update-azps) section of this article.</span></span>

## <a name="step-3-load-the-azurerm-module"></a><span data-ttu-id="af106-128">步骤 3：加载 AzureRM 模块</span><span class="sxs-lookup"><span data-stu-id="af106-128">Step 3: Load the AzureRM module</span></span>
<span data-ttu-id="af106-129">安装该模块后，需要将它加载到 PowerShell 会话中。</span><span class="sxs-lookup"><span data-stu-id="af106-129">Once the module is installed, you need to load the module into your PowerShell session.</span></span> <span data-ttu-id="af106-130">应该在正常（而非提升）的 PowerShell 会话中执行此操作。</span><span class="sxs-lookup"><span data-stu-id="af106-130">You should do this in a normal (non-elevated) PowerShell session.</span></span> <span data-ttu-id="af106-131">可以使用 `Import-Module` cmdlet 加载模块，如下所示：</span><span class="sxs-lookup"><span data-stu-id="af106-131">Modules are loaded using the `Import-Module` cmdlet, as follows:</span></span>

```powershell
Import-Module -Name AzureRM
```

## <a name="next-steps"></a><span data-ttu-id="af106-132">后续步骤</span><span class="sxs-lookup"><span data-stu-id="af106-132">Next Steps</span></span>

<span data-ttu-id="af106-133">有关使用 Azure PowerShell 的详细信息，请参阅以下文章：</span><span class="sxs-lookup"><span data-stu-id="af106-133">For more information about using Azure PowerShell, see the following articles:</span></span>

* [<span data-ttu-id="af106-134">Azure PowerShell 入门</span><span class="sxs-lookup"><span data-stu-id="af106-134">Get started with Azure PowerShell</span></span>](get-started-azureps.md)

## <a name="reporting-issues-and-feedback"></a><span data-ttu-id="af106-135">报告问题和反馈</span><span class="sxs-lookup"><span data-stu-id="af106-135">Reporting issues and feedback</span></span>

<span data-ttu-id="af106-136">如果遇到该工具的任何 bug，请在 GitHub 存储库的[问题](https://github.com/Azure/azure-powershell/issues)部分中提出问题。</span><span class="sxs-lookup"><span data-stu-id="af106-136">If you encounter any bugs with the tool, file an issue in the [Issues](https://github.com/Azure/azure-powershell/issues) section of our GitHub repo.</span></span> <span data-ttu-id="af106-137">若要从命令行提供反馈，请使用 `Send-Feedback` cmdlet。</span><span class="sxs-lookup"><span data-stu-id="af106-137">To provide feedback from the command line, use the `Send-Feedback` cmdlet.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="af106-138">常见问题</span><span class="sxs-lookup"><span data-stu-id="af106-138">Frequently asked questions</span></span>

### <a name="how-to-get-powershellget"></a><span data-ttu-id="af106-139">如何获取 PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="af106-139">How to get PowerShellGet</span></span>

|<span data-ttu-id="af106-140">场景</span><span class="sxs-lookup"><span data-stu-id="af106-140">Scenario</span></span>|<span data-ttu-id="af106-141">安装说明</span><span class="sxs-lookup"><span data-stu-id="af106-141">Install instructions</span></span>|
|---|---|
|<span data-ttu-id="af106-142">Windows 10</span><span class="sxs-lookup"><span data-stu-id="af106-142">Windows 10</span></span><br/><span data-ttu-id="af106-143">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="af106-143">Windows Server 2016</span></span>|<span data-ttu-id="af106-144">内置在 OS 随附的 Windows Management Framework (WMF) 5.0 中</span><span class="sxs-lookup"><span data-stu-id="af106-144">Built into Windows Management Framework (WMF) 5.0 included in the OS</span></span>|
|<span data-ttu-id="af106-145">我想要升级到 PowerShell 5</span><span class="sxs-lookup"><span data-stu-id="af106-145">I want to upgrade to PowerShell 5</span></span>|<ol><li>[<span data-ttu-id="af106-146">安装最新版本的 WMF</span><span class="sxs-lookup"><span data-stu-id="af106-146">Install the latest version of WMF</span></span>](https://www.microsoft.com/en-us/download/details.aspx?id=54616)</li><li><span data-ttu-id="af106-147">运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="af106-147">Run the following command:</span></span><br/>```Install-Module PowerShellGet -Force```</li></ol>|
|<span data-ttu-id="af106-148">我正在运行某个包含 PowerShell 3 或 PowerShell 4 的 Windows 版本</span><span class="sxs-lookup"><span data-stu-id="af106-148">I am running on a version of Windows with PowerShell 3 or PowerShell 4</span></span>|<ol><span data-ttu-id="af106-149"><il>[获取 PackageManagement 模块](http://go.microsoft.com/fwlink/?LinkID=746217)</il></span><span class="sxs-lookup"><span data-stu-id="af106-149"><il>[Get the PackageManagement modules](http://go.microsoft.com/fwlink/?LinkID=746217)</il></span></span><li><span data-ttu-id="af106-150">运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="af106-150">Run the following command:</span></span><br/>```Install-Module PowerShellGet -Force```</li></ol>|

<a id="helpmechoose"></a>
### <a name="checking-the-version-of-azure-powershell"></a><span data-ttu-id="af106-151">检查 Azure PowerShell 的版本</span><span class="sxs-lookup"><span data-stu-id="af106-151">Checking the version of Azure PowerShell</span></span>

<span data-ttu-id="af106-152">虽然建议尽早升级到最新版本，但仍然支持多个 Azure PowerShell 版本。</span><span class="sxs-lookup"><span data-stu-id="af106-152">Although we encourage you to upgrade to the latest version as early as possible, several versions of Azure PowerShell are supported.</span></span> <span data-ttu-id="af106-153">若要确定安装的 Azure PowerShell 版本，请从命令行运行 `Get-Module AzureRM`。</span><span class="sxs-lookup"><span data-stu-id="af106-153">To determine the version of Azure PowerShell you have installed, run `Get-Module AzureRM` from your command line.</span></span>

```powershell
Get-Module AzureRM -ListAvailable | Select-Object -Property Name,Version,Path
```

### <a name="support-for-classic-deployment-methods"></a><span data-ttu-id="af106-154">支持经典部署方法</span><span class="sxs-lookup"><span data-stu-id="af106-154">Support for classic deployment methods</span></span>

<span data-ttu-id="af106-155">如果部署使用了经典部署模型，则可以安装 Azure PowerShell 的服务管理版本。</span><span class="sxs-lookup"><span data-stu-id="af106-155">If you have deployments that use the classic deployment model you can install the Service Management version of Azure PowerShell.</span></span> <span data-ttu-id="af106-156">有关详细信息，请参阅[安装 Azure PowerShell 服务管理模块](/powershell/azure/servicemanagement/install-azure-ps)。</span><span class="sxs-lookup"><span data-stu-id="af106-156">For more information, see [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span> <span data-ttu-id="af106-157">Azure 和 AzureRM 模块共享通用的依赖项。</span><span class="sxs-lookup"><span data-stu-id="af106-157">The Azure and AzureRM modules share common dependencies.</span></span> <span data-ttu-id="af106-158">如果同时使用 Azure 和 AzureRM 模块，应该安装每个包的同一版本。</span><span class="sxs-lookup"><span data-stu-id="af106-158">If you use both the Azure and AzureRM modules, you should install the same version of each package.</span></span>

### <a id="update-azps"></a><span data-ttu-id="af106-159">更新到新版 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="af106-159">Updating to a new version of Azure PowerShell</span></span>

<span data-ttu-id="af106-160">如果安装了包含 Service Management 模块的早期版本 Azure PowerShell，可能会出现以下错误：</span><span class="sxs-lookup"><span data-stu-id="af106-160">If you have a previous version of Azure PowerShell installed that includes the Service Management module, you may receive the following error:</span></span>

```Output
PackageManagement\Install-Package : A command with name 'Get-AzureStorageContainerAcl' is already
available on this system. This module 'Azure.Storage' may override the existing commands. If you
still want to install this module 'Azure.Storage', use -AllowClobber parameter.

At C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PSModule.psm1:1772 char:21
+ ...          $null = PackageManagement\Install-Package @PSBoundParameters
+                      ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : InvalidOperation: (Microsoft.Power....InstallPackage:InstallPackage) [Install-Package], Exception
    + FullyQualifiedErrorId : CommandAlreadyAvailable,Validate-ModuleCommandAlreadyAvailable,Microsoft.PowerShell.PackageManagement.Cmdlets.InstallPackage
```

<span data-ttu-id="af106-161">如错误消息所述，应该使用 -AllowClobber 参数安装模块。</span><span class="sxs-lookup"><span data-stu-id="af106-161">As the error message states, you need to use the -AllowClobber parameter to install the module.</span></span> <span data-ttu-id="af106-162">请使用以下命令：</span><span class="sxs-lookup"><span data-stu-id="af106-162">Use the following command:</span></span>

```powershell
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

<span data-ttu-id="af106-163">有关详细信息，请参阅 [Install-Module](https://msdn.microsoft.com/powershell/reference/5.1/PowerShellGet/install-module) 的帮助主题。</span><span class="sxs-lookup"><span data-stu-id="af106-163">For more information, see the help topic for [Install-Module](https://msdn.microsoft.com/powershell/reference/5.1/PowerShellGet/install-module).</span></span>

### <a name="installing-module-versions-side-by-side"></a><span data-ttu-id="af106-164">并行安装多个模块版本</span><span class="sxs-lookup"><span data-stu-id="af106-164">Installing module versions side by side</span></span>

<span data-ttu-id="af106-165">PowerShellGet 安装方法是唯一支持安装多个版本的方法。</span><span class="sxs-lookup"><span data-stu-id="af106-165">The PowerShellGet method of installation is the only method that supports the installation of multiple versions.</span></span> <span data-ttu-id="af106-166">例如，可能使用旧版 Azure PowerShell 编写了脚本，但没有时间或资源来更新这些脚本。</span><span class="sxs-lookup"><span data-stu-id="af106-166">For example, you may have scripts written using a previous version of Azure PowerShell that you don't have the time or resources to updated.</span></span> <span data-ttu-id="af106-167">以下命令演示如何安装 Azure PowerShell 的多个版本：</span><span class="sxs-lookup"><span data-stu-id="af106-167">The following commands illustrate how to install multiple versions of Azure PowerShell:</span></span>

```powershell
Install-Module -Name AzureRM -RequiredVersion 3.7.0
Install-Module -Name AzureRM -RequiredVersion 1.2.9
```

<span data-ttu-id="af106-168">在一个 PowerShell 会话中只能加载一个模块版本。</span><span class="sxs-lookup"><span data-stu-id="af106-168">Only one version of the module can be loaded in a PowerShell session.</span></span> <span data-ttu-id="af106-169">必须打开新的 PowerShell 窗口，并使用 `Import-Module` 导入特定版本的 AzureRM cmdlet：</span><span class="sxs-lookup"><span data-stu-id="af106-169">You must open a new PowerShell window and use `Import-Module` to import a specific version of the AzureRM cmdlets:</span></span>

```powershell
Import-Module -Name AzureRM -RequiredVersion 1.2.9
```

> [!NOTE]
> <span data-ttu-id="af106-170">版本 2.1.0 和 1.2.6 是可以同时安装和使用的初始模块版本。</span><span class="sxs-lookup"><span data-stu-id="af106-170">Version 2.1.0 and version 1.2.6 are the first module versions designed to be installed and used side by side.</span></span> <span data-ttu-id="af106-171">加载 Azure PowerShell 早期版本时，会加载不兼容版本的 **AzureRM.Profile** 模块。</span><span class="sxs-lookup"><span data-stu-id="af106-171">When loading an earlier version of the Azure PowerShell, incompatible versions of the **AzureRM.Profile** module are loaded.</span></span> <span data-ttu-id="af106-172">这会导致在执行 cmdlet 时，cmdlet 会提示用户登录。</span><span class="sxs-lookup"><span data-stu-id="af106-172">This results in the cmdlets prompting you to log in whenever you execute a cmdlet.</span></span>

### <a name="other-installation-methods"></a><span data-ttu-id="af106-173">其他安装方法</span><span class="sxs-lookup"><span data-stu-id="af106-173">Other installation methods</span></span>

<span data-ttu-id="af106-174">有关使用 Web 平台安装程序或 MSI 包进行安装的信息，请参阅[其他安装方法](other-install.md)</span><span class="sxs-lookup"><span data-stu-id="af106-174">For information about installing using the Web Platform Installer or the MSI Package, see [Other installation methods](other-install.md)</span></span>
