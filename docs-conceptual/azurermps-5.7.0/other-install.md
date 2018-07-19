---
title: Azure PowerShell 的其他安装方式
description: 如何在不使用 PowerShellGet 的情况下安装 Azure PowerShell
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/20/2018
ms.openlocfilehash: 7c6446a66cd3ab9fe8f5d8adf13fed36ee093340
ms.sourcegitcommit: cb1fd248920d7efca67bd6c738a3b47206df7890
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/13/2018
ms.locfileid: "39025304"
---
# <a name="install-azure-powershell-on-windows-with-msi-or-web-platform-installer"></a><span data-ttu-id="7a763-103">使用 MSI 或 Web 平台安装程序在 Windows 上安装 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="7a763-103">Install Azure PowerShell on Windows with MSI or Web Platform Installer</span></span>

<span data-ttu-id="7a763-104">本文介绍如何使用 MSI 或 Web 平台安装程序 (WebPI) 在 Windows 上安装 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="7a763-104">This article explains how to install Azure PowerShell on Windows using an MSI or Web Platform Installer (WebPI).</span></span>  
<span data-ttu-id="7a763-105">只有当你的系统需要时才应使用这些安装方法。</span><span class="sxs-lookup"><span data-stu-id="7a763-105">Use these installation methods only if they're necessary for your system.</span></span> <span data-ttu-id="7a763-106">若要在 Windows 上安装 Azure PowerShell，建议的方法是使用 PowerShellGet。</span><span class="sxs-lookup"><span data-stu-id="7a763-106">The recommended way to install Azure PowerShell on Windows is with PowerShellGet.</span></span> <span data-ttu-id="7a763-107">有关使用 PowerShellGet 安装 Azure PowerShell 的说明，请参阅[使用 PowerShellGet 安装 Azure PowerShell](install-azurerm-ps.md)。</span><span class="sxs-lookup"><span data-stu-id="7a763-107">For instructions on using PowerShellGet to install Azure PowerShell, see [Install Azure PowerShell with PowerShellGet](install-azurerm-ps.md).</span></span>

<span data-ttu-id="7a763-108">若要在 Docker 容器中运行 Azure PowerShell，请参阅[在 Docker 中运行 Azure PowerShell](azurerm-ps-in-docker.md)。</span><span class="sxs-lookup"><span data-stu-id="7a763-108">To run Azure PowerShell in a Docker container, see [Run Azure PowerShell in Docker](azurerm-ps-in-docker.md).</span></span>

<span data-ttu-id="7a763-109">若要在 Linux 或 macOS 环境中进行安装，请参阅[在 macOS 或 Linux 上安装 Azure PowerShell](install-azurermps-maclinux.md)。</span><span class="sxs-lookup"><span data-stu-id="7a763-109">To install on Linux or macOS environments, see [Install Azure PowerShell on macOS or Linux](install-azurermps-maclinux.md).</span></span>

## <a name="install-or-update-on-windows-using-the-msi-package"></a><span data-ttu-id="7a763-110">使用 MSI 包在 Windows 上进行安装或更新</span><span class="sxs-lookup"><span data-stu-id="7a763-110">Install or update on Windows using the MSI Package</span></span>

<span data-ttu-id="7a763-111">可以使用 [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v5.7.0-April2018) 中提供的 MSI 文件安装 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="7a763-111">Azure PowerShell can be installed using the MSI file available from [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v5.7.0-April2018).</span></span> <span data-ttu-id="7a763-112">如果已将旧版 Azure 模块作为 MSI 安装，安装程序会自动删除这些模块。</span><span class="sxs-lookup"><span data-stu-id="7a763-112">If you have installed previous versions of Azure modules as an MSI, the installer automatically removes them.</span></span> <span data-ttu-id="7a763-113">MSI 包在 `${env:ProgramFiles}\WindowsPowerShell\Modules` 中安装模块。</span><span class="sxs-lookup"><span data-stu-id="7a763-113">The MSI package installs modules in `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="7a763-114">`AzureRM` 和 `Azure` 模块都安装。</span><span class="sxs-lookup"><span data-stu-id="7a763-114">Both the `AzureRM` and `Azure` modules are installed.</span></span>

> [!NOTE]
> <span data-ttu-id="7a763-115">如果使用的是 Azure 经典部署模型，则只使用 `Azure` 模块。</span><span class="sxs-lookup"><span data-stu-id="7a763-115">Only use the `Azure` module if you are working with the Azure classic deployment model.</span></span>

<span data-ttu-id="7a763-116">若要开始使用 Azure PowerShell，需使用 [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet 将 `AzureRM` 加载到当前的 PowerShell 会话中，然后使用 Azure 凭据登录。</span><span class="sxs-lookup"><span data-stu-id="7a763-116">To start working with Azure PowerShell, you need to load `AzureRM` into your current PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span>

```powershell
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="7a763-117">需对每个启动的新 PowerShell 会话重复这些步骤。</span><span class="sxs-lookup"><span data-stu-id="7a763-117">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="7a763-118">自动导入 `AzureRM` 模块要求设置 PowerShell 配置文件，详见[关于配置文件](/powershell/module/microsoft.powershell.core/about/about_profiles)。</span><span class="sxs-lookup"><span data-stu-id="7a763-118">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="7a763-119">若要了解如何跨会话保持 Azure 登录状态，请参阅[跨 PowerShell 会话保持用户凭据](context-persistence.md)。</span><span class="sxs-lookup"><span data-stu-id="7a763-119">To learn how to persist your Azure sign in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="install-or-update-on-windows-using-the-web-platform-installer"></a><span data-ttu-id="7a763-120">使用 Web 平台安装程序在 Windows 上进行安装或更新</span><span class="sxs-lookup"><span data-stu-id="7a763-120">Install or update on Windows using the Web Platform Installer</span></span>

<span data-ttu-id="7a763-121">下载 [Azure PowerShell WebPI 包](http://aka.ms/webpi-azps)，并开始安装。</span><span class="sxs-lookup"><span data-stu-id="7a763-121">Download the [Azure PowerShell WebPI package](http://aka.ms/webpi-azps) and start the install.</span></span> <span data-ttu-id="7a763-122">如果已通过 MSI 或 WebPI 安装旧版 Azure 模块，安装程序会自动删除这些模块。</span><span class="sxs-lookup"><span data-stu-id="7a763-122">If you have installed previous versions of Azure modules from an MSI or with WebPI, the installer automatically removes them.</span></span> <span data-ttu-id="7a763-123">模块安装到 `${env:ProgramFiles}\WindowsPowerShell\Modules` 中。</span><span class="sxs-lookup"><span data-stu-id="7a763-123">Modules are installed into `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="7a763-124">`AzureRM` 和 `Azure` 模块都安装。</span><span class="sxs-lookup"><span data-stu-id="7a763-124">Both the `AzureRM` and `Azure` modules are installed.</span></span>

> [!NOTE]
> <span data-ttu-id="7a763-125">如果使用的是 Azure 经典部署模型，则只使用 `Azure` 模块。</span><span class="sxs-lookup"><span data-stu-id="7a763-125">Only use the `Azure` module if you are working with the Azure classic deployment model.</span></span>

<span data-ttu-id="7a763-126">若要开始使用 Azure PowerShell，需使用 [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet 将 `AzureRM` 加载到当前的 PowerShell 会话中，然后使用 Azure 凭据登录。</span><span class="sxs-lookup"><span data-stu-id="7a763-126">To start working with Azure PowerShell, you need to load `AzureRM` into your current PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span>

```powershell
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="7a763-127">需对每个启动的新 PowerShell 会话重复这些步骤。</span><span class="sxs-lookup"><span data-stu-id="7a763-127">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="7a763-128">自动导入 `AzureRM` 模块要求设置 PowerShell 配置文件，详见[关于配置文件](/powershell/module/microsoft.powershell.core/about/about_profiles)。</span><span class="sxs-lookup"><span data-stu-id="7a763-128">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="7a763-129">若要了解如何跨会话保持 Azure 登录状态，请参阅[跨 PowerShell 会话保持用户凭据](context-persistence.md)。</span><span class="sxs-lookup"><span data-stu-id="7a763-129">To learn how to persist your Azure sign in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>