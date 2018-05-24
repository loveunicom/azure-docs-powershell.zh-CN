---
title: Azure PowerShell 的其他安装方式 | Microsoft Docs
description: 如何使用 MSI 包或 Web 平台安装程序安装 Azure PowerShell。
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/06/2017
ms.openlocfilehash: 8b7d9631581046800c772d7bc6f654bb6a9eb483
ms.sourcegitcommit: 5971c92cb023bdd1d71fa2ad0a3b378abfbd092a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/23/2018
---
# <a name="other-installation-methods"></a><span data-ttu-id="71757-103">其他安装方法</span><span class="sxs-lookup"><span data-stu-id="71757-103">Other installation methods</span></span>

<span data-ttu-id="71757-104">Azure PowerShell 提供多种安装方法。</span><span class="sxs-lookup"><span data-stu-id="71757-104">Azure PowerShell has multiple installation methods.</span></span> <span data-ttu-id="71757-105">首选的方法是结合使用 PowerShellGet 和 PowerShell 库。</span><span class="sxs-lookup"><span data-stu-id="71757-105">Using PowerShellGet with the PowerShell Gallery is the preferred method.</span></span> <span data-ttu-id="71757-106">可以使用 Web 平台安装程序 (WebPI) 或者 GitHub 中提供的 MSI 文件在 Windows 上安装 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="71757-106">Azure PowerShell can be installed on Windows using the Web Platform Installer (WebPI) or by using the MSI file available from GitHub.</span></span> <span data-ttu-id="71757-107">也可以在 Docker 容器中安装 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="71757-107">Azure PowerShell can also be installed in a Docker container.</span></span>

## <a name="install-on-windows-using-the-web-platform-installer"></a><span data-ttu-id="71757-108">使用 Web 平台安装程序在 Windows 上安装</span><span class="sxs-lookup"><span data-stu-id="71757-108">Install on Windows using the Web Platform Installer</span></span>

<span data-ttu-id="71757-109">从 WebPI 安装最新 Azure PowerShell 的过程与安装以往版本的过程相同。</span><span class="sxs-lookup"><span data-stu-id="71757-109">Installing the latest Azure PowerShell from WebPI is the same as it was for previous versions.</span></span>
<span data-ttu-id="71757-110">下载 [Azure PowerShell WebPI 包](http://aka.ms/webpi-azps)，并开始安装。</span><span class="sxs-lookup"><span data-stu-id="71757-110">Download the [Azure PowerShell WebPI package](http://aka.ms/webpi-azps) and start the install.</span></span>

> [!NOTE]
> <span data-ttu-id="71757-111">如果之前从 PowerShell 库安装了 Azure 模块，安装程序会自动删除这些模块。</span><span class="sxs-lookup"><span data-stu-id="71757-111">If you have previously installed Azure modules from the PowerShell Gallery, the installer automatically removes them.</span></span> <span data-ttu-id="71757-112">这可确保只安装一个 Azure PowerShell 版本，因此可以简化环境。</span><span class="sxs-lookup"><span data-stu-id="71757-112">This simplifies your environment by ensuring that only one version of Azure PowerShell is installed.</span></span> <span data-ttu-id="71757-113">但是，在某些情况下，可能需要同时安装多个版本。</span><span class="sxs-lookup"><span data-stu-id="71757-113">However, there are scenarios where you may need multiple versions installed at the same time.</span></span>
>
> <span data-ttu-id="71757-114">PowerShell 库模块在 `$env:ProgramFiles\WindowsPowerShell\Modules` 中安装模块。</span><span class="sxs-lookup"><span data-stu-id="71757-114">PowerShell Gallery modules install modules in `$env:ProgramFiles\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="71757-115">相比之下，WebPI 安装程序在 `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\` 中安装 Azure 模块。</span><span class="sxs-lookup"><span data-stu-id="71757-115">In contrast, the WebPI installer installs the Azure modules in `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\`.</span></span>
>
> <span data-ttu-id="71757-116">如果安装期间出错，可以手动删除 `$env:ProgramFiles\WindowsPowerShell\Modules` 文件夹中的 Azure\* 文件夹，并重试安装。</span><span class="sxs-lookup"><span data-stu-id="71757-116">If an error occurs during install, you can manually remove the Azure\* folders in your `$env:ProgramFiles\WindowsPowerShell\Modules` folder, and try the installation again.</span></span>

<span data-ttu-id="71757-117">完成安装后，`$env:PSModulePath` 设置中应有包含 Azure PowerShell cmdlet 的目录。</span><span class="sxs-lookup"><span data-stu-id="71757-117">Once the installation completes, your `$env:PSModulePath` setting should include the directories containing the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="71757-118">可以使用以下命令验证正确安装了 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="71757-118">The following command can be used to verify that the Azure PowerShell is installed properly.</span></span>

```powershell
# To make sure the Azure PowerShell module is available after you install
Get-Module -ListAvailable Azure* | Select-Object Name, Version, Path
```

> [!NOTE]
> <span data-ttu-id="71757-119">从 WebPI 安装时，可能会发生一个已知问题。</span><span class="sxs-lookup"><span data-stu-id="71757-119">There is a known issue that can occur when installing from WebPI.</span></span> <span data-ttu-id="71757-120">如果计算机由于系统更新或其他安装而需要重新启动，有可能会导致更新 `$env:PSModulePath` 时无法包含 Azure PowerShell 的安装路径。</span><span class="sxs-lookup"><span data-stu-id="71757-120">If your computer requires a restart due to system updates or other installations, it may cause updates to `$env:PSModulePath` to fail to include the path where Azure PowerShell is installed.</span></span>

<span data-ttu-id="71757-121">安装后尝试加载或执行 cmdlet 时，可能会出现以下错误消息：</span><span class="sxs-lookup"><span data-stu-id="71757-121">When attempting to load or execute cmdlets after installation, you can receive the following error message:</span></span>

```
PS C:\> Connect-AzureRmAccount
Connect-AzureRmAccount : The term 'Connect-AzureRmAccount' is not recognized as the name of a cmdlet,
function, script file, or operable program. Check the spelling of the name, or if a path was
included, verify that the path is correct and try again.
At line:1 char:1
+ Connect-AzureRmAccount
+ ~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : ObjectNotFound: (Connect-AzureRmAccount:String) [], CommandNotFoundException
    + FullyQualifiedErrorId : CommandNotFoundException
```

<span data-ttu-id="71757-122">重启计算机或使用完全限定的路径导入模块可更正此问题。</span><span class="sxs-lookup"><span data-stu-id="71757-122">This error can be corrected by restarting the machine or importing the module using the fully qualified path.</span></span> <span data-ttu-id="71757-123">例如：</span><span class="sxs-lookup"><span data-stu-id="71757-123">For example:</span></span>

```powershell
Import-Module "$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\AzureRM.psd1"
```

## <a name="install-on-windows-using-the-msi-package"></a><span data-ttu-id="71757-124">使用 MSI 包在 Windows 上安装</span><span class="sxs-lookup"><span data-stu-id="71757-124">Install on Windows using the MSI Package</span></span>

<span data-ttu-id="71757-125">可以使用 [GitHub](https://aka.ms/azps-release) 中提供的 MSI 文件安装 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="71757-125">Azure PowerShell can be installed using the MSI file available from [GitHub](https://aka.ms/azps-release).</span></span> <span data-ttu-id="71757-126">如果已安装旧版 Azure 模块，安装程序会自动删除这些模块。</span><span class="sxs-lookup"><span data-stu-id="71757-126">If you have installed previous versions of Azure modules, the installer automatically removes them.</span></span> <span data-ttu-id="71757-127">MSI 包在 `$env:ProgramFiles\WindowsPowerShell\Modules` 中安装模块，但不会创建版本特定的文件夹。</span><span class="sxs-lookup"><span data-stu-id="71757-127">The MSI package installs modules in `$env:ProgramFiles\WindowsPowerShell\Modules` but does not create version-specific folders.</span></span>

## <a name="install-in-a-docker-container"></a><span data-ttu-id="71757-128">在 Docker 容器中安装</span><span class="sxs-lookup"><span data-stu-id="71757-128">Install in a Docker container</span></span>

<span data-ttu-id="71757-129">我们维护预先配置了 Azure PowerShell 的 Docker 映像。</span><span class="sxs-lookup"><span data-stu-id="71757-129">We maintain a Docker image preconfigured with Azure PowerShell.</span></span>

<span data-ttu-id="71757-130">通过 `docker run` 运行容器。</span><span class="sxs-lookup"><span data-stu-id="71757-130">Run the container with `docker run`.</span></span>

```powershell
docker run azuresdk/azure-powershell
```

<span data-ttu-id="71757-131">此外，我们还维护作为 PowerShell Core 容器的 cmdlet 子集。</span><span class="sxs-lookup"><span data-stu-id="71757-131">In addition, we maintain a subset of cmdlets as a PowerShell Core container.</span></span>

<span data-ttu-id="71757-132">对于 Mac/Linux，请使用 `latest` 映像。</span><span class="sxs-lookup"><span data-stu-id="71757-132">For Mac/Linux, use the `latest` image.</span></span>

```bash
docker run azuresdk/azure-powershell-core:latest
```

<span data-ttu-id="71757-133">对于 Windows，请使用 `nanoserver` 映像。</span><span class="sxs-lookup"><span data-stu-id="71757-133">For Windows, use the `nanoserver` image.</span></span>

```powershell
docker run azuresdk/azure-powershell-core:nanoserver
```

<span data-ttu-id="71757-134">通过 [PowerShell 库](https://www.powershellgallery.com/)中的 `Install-Module` 将 Azure PowerShell 安装到映像上。</span><span class="sxs-lookup"><span data-stu-id="71757-134">Azure PowerShell is installed on the image via `Install-Module` from the [PowerShell Gallery](https://www.powershellgallery.com/).</span></span>
