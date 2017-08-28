---
title: "Azure PowerShell 的其他安装方式 | Microsoft Docs"
description: "如何使用 MSI 包或 Web 平台安装程序安装 Azure PowerShell。"
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: 9cee582f74b7f3260c6ae167a8ac358d360ad8ab
ms.sourcegitcommit: 45587b5091293288e16cfae8ac412e0d42f8f450
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/15/2017
---
# <a name="other-installation-methods"></a><span data-ttu-id="09c33-103">其他安装方法</span><span class="sxs-lookup"><span data-stu-id="09c33-103">Other installation methods</span></span>

<span data-ttu-id="09c33-104">Azure PowerShell 提供多种安装方法。</span><span class="sxs-lookup"><span data-stu-id="09c33-104">Azure PowerShell has multiple installation methods.</span></span> <span data-ttu-id="09c33-105">首选的方法是结合使用 PowerShellGet 和 PowerShell 库。</span><span class="sxs-lookup"><span data-stu-id="09c33-105">Using PowerShellGet with the PowerShell Gallery is the preferred method.</span></span> <span data-ttu-id="09c33-106">可以使用 Web 平台安装程序 (WebPI) 或者 [GitHub](https://github.com/Azure/azure-powershell/releases/latest) 中提供的 MSI 文件安装 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="09c33-106">Azure PowerShell can be installed using the Web Platform Installer (WebPI) or by using the MSI file available from [GitHub](https://github.com/Azure/azure-powershell/releases/latest).</span></span>

## <a name="docker"></a><span data-ttu-id="09c33-107">Docker</span><span class="sxs-lookup"><span data-stu-id="09c33-107">Docker</span></span>

<span data-ttu-id="09c33-108">我们维护预先配置了 Azure PowerShell 的 Docker 映像。</span><span class="sxs-lookup"><span data-stu-id="09c33-108">We maintain a Docker image preconfigured with Azure PowerShell.</span></span>

<span data-ttu-id="09c33-109">通过 `docker run` 运行容器。</span><span class="sxs-lookup"><span data-stu-id="09c33-109">Run the container with `docker run`.</span></span>

```powershell
docker run azuresdk/azure-powershell
```

<span data-ttu-id="09c33-110">此外，我们还维护作为 PowerShell Core 容器的 cmdlet 子集。</span><span class="sxs-lookup"><span data-stu-id="09c33-110">In addition, we maintain a subset of cmdlets as a PowerShell Core container.</span></span>

<span data-ttu-id="09c33-111">对于 Mac/Linux，请使用 `latest` 映像。</span><span class="sxs-lookup"><span data-stu-id="09c33-111">For Mac/Linux, use the `latest` image.</span></span>

```bash
docker run azuresdk/azure-powershell-core:latest
```

<span data-ttu-id="09c33-112">对于 Windows，请使用 `nanoserver` 映像。</span><span class="sxs-lookup"><span data-stu-id="09c33-112">For Windows, use the `nanoserver` image.</span></span>

```powershell
docker run azuresdk/azure-powershell-core:nanoserver
```

<span data-ttu-id="09c33-113">通过 [PowerShell 库](https://www.powershellgallery.com/)中的 `Install-Module` 将 Azure PowerShell 安装到映像上。</span><span class="sxs-lookup"><span data-stu-id="09c33-113">Azure PowerShell is installed on the image via `Install-Module` from the [PowerShell Gallery](https://www.powershellgallery.com/).</span></span>

## <a name="install-using-the-web-platform-installer"></a><span data-ttu-id="09c33-114">使用 Web 平台安装程序安装</span><span class="sxs-lookup"><span data-stu-id="09c33-114">Install using the Web Platform Installer</span></span>

<span data-ttu-id="09c33-115">从 WebPI 安装最新 Azure PowerShell 的过程与安装以往版本的过程相同。</span><span class="sxs-lookup"><span data-stu-id="09c33-115">Installing the latest Azure PowerShell from WebPI is the same as it was for previous versions.</span></span>
<span data-ttu-id="09c33-116">下载 [Azure PowerShell WebPI 包](http://aka.ms/webpi-azps)，并开始安装。</span><span class="sxs-lookup"><span data-stu-id="09c33-116">Download the [Azure PowerShell WebPI package](http://aka.ms/webpi-azps) and start the install.</span></span>

> [!NOTE]
> <span data-ttu-id="09c33-117">如果之前从 PowerShell 库安装了 Azure 模块，安装程序会自动删除这些模块。</span><span class="sxs-lookup"><span data-stu-id="09c33-117">If you have previously installed Azure modules from the PowerShell Gallery, the installer automatically removes them.</span></span> <span data-ttu-id="09c33-118">这可确保只安装一个 Azure PowerShell 版本，因此可以简化环境。</span><span class="sxs-lookup"><span data-stu-id="09c33-118">This simplifies your environment by ensuring that only one version of Azure PowerShell is installed.</span></span> <span data-ttu-id="09c33-119">但是，在某些情况下，可能需要同时安装多个版本。</span><span class="sxs-lookup"><span data-stu-id="09c33-119">However, there are scenarios where you may need multiple versions installed at the same time.</span></span>
>
> <span data-ttu-id="09c33-120">PowerShell 库模块在 `$env:ProgramFiles\WindowsPowerShell\Modules` 中安装模块。</span><span class="sxs-lookup"><span data-stu-id="09c33-120">PowerShell Gallery modules install modules in `$env:ProgramFiles\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="09c33-121">相比之下，WebPI 安装程序在 `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\` 中安装 Azure 模块。</span><span class="sxs-lookup"><span data-stu-id="09c33-121">In contrast, the WebPI installer installs the Azure modules in `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\`.</span></span>
>
> <span data-ttu-id="09c33-122">如果安装期间出错，可以手动删除 `$env:ProgramFiles\WindowsPowerShell\Modules` 文件夹中的 Azure* 文件夹，并重试安装。</span><span class="sxs-lookup"><span data-stu-id="09c33-122">If an error occurs during install, you can manually remove the Azure* folders in your `$env:ProgramFiles\WindowsPowerShell\Modules` folder, and try the installation again.</span></span>

<span data-ttu-id="09c33-123">完成安装后，`$env:PSModulePath` 设置中应有包含 Azure PowerShell cmdlet 的目录。</span><span class="sxs-lookup"><span data-stu-id="09c33-123">Once the installation completes, your `$env:PSModulePath` setting should include the directories containing the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="09c33-124">可以使用以下命令验证正确安装了 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="09c33-124">The following command can be used to verify that the Azure PowerShell is installed properly.</span></span>

```powershell
# To make sure the Azure PowerShell module is available after you install
Get-Module -ListAvailable Azure* | Select-Object Name, Version, Path
```

> [!NOTE]
> <span data-ttu-id="09c33-125">从 WebPI 安装时，可能会发生一个已知问题。</span><span class="sxs-lookup"><span data-stu-id="09c33-125">There is a known issue that can occur when installing from WebPI.</span></span> <span data-ttu-id="09c33-126">如果计算机由于系统更新或其他安装而需要重新启动，有可能会导致更新 `$env:PSModulePath` 时无法包含 Azure PowerShell 的安装路径。</span><span class="sxs-lookup"><span data-stu-id="09c33-126">If your computer requires a restart due to system updates or other installations, it may cause updates to `$env:PSModulePath` to fail to include the path where Azure PowerShell is installed.</span></span>

<span data-ttu-id="09c33-127">安装后尝试加载或执行 cmdlet 时，可能会出现以下错误消息：</span><span class="sxs-lookup"><span data-stu-id="09c33-127">When attempting to load or execute cmdlets after installation, you can receive the following error message:</span></span>

```
PS C:\> Login-AzureRmAccount
Login-AzureRmAccount : The term 'Login-AzureRmAccount' is not recognized as the name of a cmdlet,
function, script file, or operable program. Check the spelling of the name, or if a path was
included, verify that the path is correct and try again.
At line:1 char:1
+ Login-AzureRmAccount
+ ~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : ObjectNotFound: (Login-AzureRmAccount:String) [], CommandNotFoundException
    + FullyQualifiedErrorId : CommandNotFoundException
```

<span data-ttu-id="09c33-128">重启计算机或使用完全限定的路径导入模块可更正此问题。</span><span class="sxs-lookup"><span data-stu-id="09c33-128">This error can be corrected by restarting the machine or importing the module using the fully qualified path.</span></span> <span data-ttu-id="09c33-129">例如：</span><span class="sxs-lookup"><span data-stu-id="09c33-129">For example:</span></span>

```powershell
Import-Module "$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\AzureRM.psd1"
```

## <a name="install-using-the-msi-package"></a><span data-ttu-id="09c33-130">使用 MSI 包安装</span><span class="sxs-lookup"><span data-stu-id="09c33-130">Install using the MSI Package</span></span>

<span data-ttu-id="09c33-131">可以使用 [GitHub](https://github.com/Azure/azure-powershell/releases/latest) 中提供的 MSI 文件安装 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="09c33-131">Azure PowerShell can be installed using the MSI file available from [GitHub](https://github.com/Azure/azure-powershell/releases/latest).</span></span> <span data-ttu-id="09c33-132">如果已安装旧版 Azure 模块，安装程序会自动删除这些模块。</span><span class="sxs-lookup"><span data-stu-id="09c33-132">If you have installed previous versions of Azure modules, the installer automatically removes them.</span></span> <span data-ttu-id="09c33-133">MSI 包在 `$env:ProgramFiles\WindowsPowerShell\Modules` 中安装模块，但不会创建版本特定的文件夹。</span><span class="sxs-lookup"><span data-stu-id="09c33-133">The MSI package installs modules in `$env:ProgramFiles\WindowsPowerShell\Modules` but does not create version-specific folders.</span></span>
