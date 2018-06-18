---
title: Azure PowerShell 的其他安装方式
description: 如何使用 MSI 包或 Web 平台安装程序安装 Azure PowerShell。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/06/2018
ms.openlocfilehash: 0919583d9cb05a75fae3b812eed84109be8b28aa
ms.sourcegitcommit: bcf80dfd7fbe17e82e7ad029802cfe8a2f02b15c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "35323316"
---
# <a name="other-installation-methods"></a><span data-ttu-id="b1908-103">其他安装方法</span><span class="sxs-lookup"><span data-stu-id="b1908-103">Other installation methods</span></span>

<span data-ttu-id="b1908-104">本文介绍了如何使用 MSI 或 Web 平台安装程序 (WebPI) 安装 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="b1908-104">This article explains how to install Azure PowerShell using an MSI or Web Platform Installer (WebPI).</span></span> <span data-ttu-id="b1908-105">还可以从 Docker 容器内部运行 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="b1908-105">You can also run Azure PowerShell from inside of a Docker container.</span></span> <span data-ttu-id="b1908-106">只有当你的系统需要时才应使用这些安装方法。</span><span class="sxs-lookup"><span data-stu-id="b1908-106">Use these installation methods only if they're necessary for your system.</span></span> <span data-ttu-id="b1908-107">安装 Azure PowerShell 的常规方法是使用 PowerShellGet。</span><span class="sxs-lookup"><span data-stu-id="b1908-107">The canonical way to install Azure PowerShell is through PowerShellGet.</span></span> <span data-ttu-id="b1908-108">有关使用 PowerShellGet 安装 Azure PowerShell 的说明，请参阅[使用 PowerShellGet 安装 Azure PowerShell](install-azurerm-ps.md)。</span><span class="sxs-lookup"><span data-stu-id="b1908-108">For instructions on using PowerShellGet to install Azure PowerShell, see [Install Azure PowerShell with PowerShellGet](install-azurerm-ps.md).</span></span>

<span data-ttu-id="b1908-109">若要在 Linux 或 macOS 环境中进行安装，请参阅[在 macOS 或 Linux 上安装 Azure PowerShell](install-azurermps-maclinux.md)。</span><span class="sxs-lookup"><span data-stu-id="b1908-109">To install on Linux or macOS environments, see [Install Azure PowerShell on macOS or Linux](install-azurermps-maclinux.md).</span></span>

## <a name="install-or-update-on-windows-using-the-web-platform-installer"></a><span data-ttu-id="b1908-110">使用 Web 平台安装程序在 Windows 上进行安装或更新</span><span class="sxs-lookup"><span data-stu-id="b1908-110">Install or update on Windows using the Web Platform Installer</span></span>

<span data-ttu-id="b1908-111">从 WebPI 安装最新 Azure PowerShell 的过程与安装以往版本的过程相同。</span><span class="sxs-lookup"><span data-stu-id="b1908-111">Installing the latest Azure PowerShell from WebPI is the same as it was for previous versions.</span></span>
<span data-ttu-id="b1908-112">下载 [Azure PowerShell WebPI 包](http://aka.ms/webpi-azps)，并开始安装。</span><span class="sxs-lookup"><span data-stu-id="b1908-112">Download the [Azure PowerShell WebPI package](http://aka.ms/webpi-azps) and start the install.</span></span>

> [!NOTE]
> <span data-ttu-id="b1908-113">如果之前从 PowerShell 库安装了 Azure 模块，安装程序会自动删除这些模块。</span><span class="sxs-lookup"><span data-stu-id="b1908-113">If you have previously installed Azure modules from the PowerShell Gallery, the installer automatically removes them.</span></span> <span data-ttu-id="b1908-114">这可确保只安装一个 Azure PowerShell 版本，因此可以简化环境。</span><span class="sxs-lookup"><span data-stu-id="b1908-114">This simplifies your environment by ensuring that only one version of Azure PowerShell is installed.</span></span> <span data-ttu-id="b1908-115">但是，在某些情况下，可能需要同时安装多个版本。</span><span class="sxs-lookup"><span data-stu-id="b1908-115">However, there are scenarios where you may need multiple versions installed at the same time.</span></span>
>
> <span data-ttu-id="b1908-116">PowerShell 库模块在 `$env:ProgramFiles\WindowsPowerShell\Modules` 中安装模块。</span><span class="sxs-lookup"><span data-stu-id="b1908-116">PowerShell Gallery modules install modules in `$env:ProgramFiles\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="b1908-117">相比之下，WebPI 安装程序在 `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\` 中安装 Azure 模块。</span><span class="sxs-lookup"><span data-stu-id="b1908-117">In contrast, the WebPI installer installs the Azure modules in `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\`.</span></span>
>
> <span data-ttu-id="b1908-118">如果在安装期间出错，可以手动删除 `$env:ProgramFiles\WindowsPowerShell\Modules` 文件夹中的 `Azure*` 文件夹，并重试安装。</span><span class="sxs-lookup"><span data-stu-id="b1908-118">If an error occurs during install, you can manually remove the `Azure*` folders in your `$env:ProgramFiles\WindowsPowerShell\Modules` folder, and try the installation again.</span></span>

<span data-ttu-id="b1908-119">完成安装后，`$env:PSModulePath` 设置中应有包含 Azure PowerShell cmdlet 的目录。</span><span class="sxs-lookup"><span data-stu-id="b1908-119">Once the installation completes, your `$env:PSModulePath` setting should include the directories containing the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="b1908-120">可以使用以下命令验证是否正确安装了 Azure PowerShell：</span><span class="sxs-lookup"><span data-stu-id="b1908-120">The following command can be used to verify that the Azure PowerShell is installed properly:</span></span>

```powershell
# To make sure the Azure PowerShell module is available after you install
Get-Module -ListAvailable Azure* | Select-Object Name, Version, Path
```

> [!NOTE]
> <span data-ttu-id="b1908-121">从 WebPI 安装时，可能会发生一个已知问题。</span><span class="sxs-lookup"><span data-stu-id="b1908-121">There is a known issue that can occur when installing from WebPI.</span></span> <span data-ttu-id="b1908-122">如果计算机由于系统更新或其他安装而需要重新启动，有可能会导致更新 `$env:PSModulePath` 时无法包含 Azure PowerShell 的安装路径。</span><span class="sxs-lookup"><span data-stu-id="b1908-122">If your computer requires a restart due to system updates or other installations, it may cause updates to `$env:PSModulePath` to fail to include the path where Azure PowerShell is installed.</span></span>

<span data-ttu-id="b1908-123">安装后尝试加载或执行 cmdlet 时，可能会出现以下错误消息：</span><span class="sxs-lookup"><span data-stu-id="b1908-123">When attempting to load or execute cmdlets after installation, you can receive the following error message:</span></span>

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

<span data-ttu-id="b1908-124">重启计算机或使用完全限定的路径导入模块可更正此问题。</span><span class="sxs-lookup"><span data-stu-id="b1908-124">This error can be corrected by restarting the machine or importing the module using the fully qualified path.</span></span>

```powershell
Import-Module "$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\AzureRM.psd1"
```

## <a name="install-or-update-on-windows-using-the-msi-package"></a><span data-ttu-id="b1908-125">使用 MSI 包在 Windows 上进行安装或更新</span><span class="sxs-lookup"><span data-stu-id="b1908-125">Install or update on Windows using the MSI Package</span></span>

<span data-ttu-id="b1908-126">可以使用 [GitHub](https://aka.ms/azps-release) 中提供的 MSI 文件安装 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="b1908-126">Azure PowerShell can be installed using the MSI file available from [GitHub](https://aka.ms/azps-release).</span></span> <span data-ttu-id="b1908-127">如果已安装旧版 Azure 模块，安装程序会自动删除这些模块。</span><span class="sxs-lookup"><span data-stu-id="b1908-127">If you have installed previous versions of Azure modules, the installer automatically removes them.</span></span> <span data-ttu-id="b1908-128">MSI 包在 `$env:ProgramFiles\WindowsPowerShell\Modules` 中安装模块，但不会创建版本特定的文件夹。</span><span class="sxs-lookup"><span data-stu-id="b1908-128">The MSI package installs modules in `$env:ProgramFiles\WindowsPowerShell\Modules` but does not create version-specific folders.</span></span>

## <a name="run-in-a-docker-container"></a><span data-ttu-id="b1908-129">在 Docker 容器中运行</span><span class="sxs-lookup"><span data-stu-id="b1908-129">Run in a Docker container</span></span>

<span data-ttu-id="b1908-130">我们维护着随 Azure PowerShell 预先配置的一组 Docker 映像。</span><span class="sxs-lookup"><span data-stu-id="b1908-130">We maintain a set of Docker images preconfigured with Azure PowerShell.</span></span> <span data-ttu-id="b1908-131">提供了两种类型的容器：在 Windows 上运行传统 PowerShell 的容器，和在 Windows 或 Linux 上运行 PowerShell Core 的容器。</span><span class="sxs-lookup"><span data-stu-id="b1908-131">There are two types of containers available: Those running traditional PowerShell on Windows, and a container running PowerShell Core on either Windows or Linux.</span></span>

| <span data-ttu-id="b1908-132">环境</span><span class="sxs-lookup"><span data-stu-id="b1908-132">Environment</span></span> | <span data-ttu-id="b1908-133">Docker 映像</span><span class="sxs-lookup"><span data-stu-id="b1908-133">Docker image</span></span> |
|-------------|--------------|
| <span data-ttu-id="b1908-134">Windows 上的 PowerShell</span><span class="sxs-lookup"><span data-stu-id="b1908-134">PowerShell on Windows</span></span> | [<span data-ttu-id="b1908-135">azuresdk/azure-powershell</span><span class="sxs-lookup"><span data-stu-id="b1908-135">azuresdk/azure-powershell</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell/) |
| <span data-ttu-id="b1908-136">Windows 上的 PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="b1908-136">PowerShell Core on Windows</span></span> | [<span data-ttu-id="b1908-137">azuresdk/azure-powershell-core:nanoserver</span><span class="sxs-lookup"><span data-stu-id="b1908-137">azuresdk/azure-powershell-core:nanoserver</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |
| <span data-ttu-id="b1908-138">Linux 上的 PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="b1908-138">PowerShell Core on Linux</span></span> | [<span data-ttu-id="b1908-139">azuresdk/azure-powershell-core:latest</span><span class="sxs-lookup"><span data-stu-id="b1908-139">azuresdk/azure-powershell-core:latest</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |

<span data-ttu-id="b1908-140">若要运行这些容器中的任何一个，请使用 `docker run -it $ImageName` 获取交互式终端。</span><span class="sxs-lookup"><span data-stu-id="b1908-140">To run any of these containers, you use `docker run -it $ImageName` to get an interactive terminal.</span></span> <span data-ttu-id="b1908-141">例如，若要在 Linux 容器上运行 PowerShell Core，请使用：</span><span class="sxs-lookup"><span data-stu-id="b1908-141">For example, to run the PowerShell Core on Linux container, use:</span></span>

```powershell
docker run -it azuresdk/azure-powershell-core:latest
```

> [!NOTE]
> <span data-ttu-id="b1908-142">若要在 Docker 中运行 Windows 容器，主机 OS 必须是 Windows 并且 Docker 必须设置为运行 Windows 容器。</span><span class="sxs-lookup"><span data-stu-id="b1908-142">To run a Windows container in Docker, your host OS must be Windows and Docker must be set to run Windows containers.</span></span> <span data-ttu-id="b1908-143">若要了解如何在 Docker 中在 Windows 与 Linux 环境之间进行切换，请参阅 Docker 文档[在 Windows 与 Linux 容器之间进行切换](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers)。</span><span class="sxs-lookup"><span data-stu-id="b1908-143">To learn about switching between Windows and Linux environments in Docker, see the Docker documentation [Switch between Windows and Linux containers](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers).</span></span>