---
title: Azure PowerShell 的其他安装方式
description: 如何在不使用 PowerShellGet 的情况下安装 Azure PowerShell
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/20/2018
ms.openlocfilehash: f9293d2715b36161c3e6d0d9469b6f18ab35d6c8
ms.sourcegitcommit: 06f9206e025afa7207d4657c8f57c94ddb74817a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/07/2018
ms.locfileid: "51212176"
---
# <a name="install-azure-powershell-on-windows-with-msi-or-web-platform-installer"></a><span data-ttu-id="7d181-103">使用 MSI 或 Web 平台安装程序在 Windows 上安装 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="7d181-103">Install Azure PowerShell on Windows with MSI or Web Platform Installer</span></span>

<span data-ttu-id="7d181-104">本文介绍如何使用 MSI 或 Web 平台安装程序 (WebPI) 在 Windows 上安装 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="7d181-104">This article explains how to install Azure PowerShell on Windows using an MSI or Web Platform Installer (WebPI).</span></span>  
<span data-ttu-id="7d181-105">只有当你的系统需要时才应使用这些安装方法。</span><span class="sxs-lookup"><span data-stu-id="7d181-105">Use these installation methods only if they're necessary for your system.</span></span> <span data-ttu-id="7d181-106">若要在 Windows 上安装 Azure PowerShell，建议的方法是使用 PowerShellGet。</span><span class="sxs-lookup"><span data-stu-id="7d181-106">The recommended way to install Azure PowerShell on Windows is with PowerShellGet.</span></span> <span data-ttu-id="7d181-107">有关使用 PowerShellGet 安装 Azure PowerShell 的说明，请参阅[使用 PowerShellGet 安装 Azure PowerShell](install-azurerm-ps.md)。</span><span class="sxs-lookup"><span data-stu-id="7d181-107">For instructions on using PowerShellGet to install Azure PowerShell, see [Install Azure PowerShell with PowerShellGet](install-azurerm-ps.md).</span></span>

<span data-ttu-id="7d181-108">若要在 Linux 或 macOS 环境中进行安装，请参阅[在 macOS 或 Linux 上安装 Azure PowerShell](install-azurermps-maclinux.md)。</span><span class="sxs-lookup"><span data-stu-id="7d181-108">To install on Linux or macOS environments, see [Install Azure PowerShell on macOS or Linux](install-azurermps-maclinux.md).</span></span>

## <a name="install-or-update-on-windows-using-the-msi-package"></a><span data-ttu-id="7d181-109">使用 MSI 包在 Windows 上进行安装或更新</span><span class="sxs-lookup"><span data-stu-id="7d181-109">Install or update on Windows using the MSI Package</span></span>

<span data-ttu-id="7d181-110">可以使用 [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v5.7.0-April2018) 中提供的 MSI 文件安装 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="7d181-110">Azure PowerShell can be installed using the MSI file available from [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v5.7.0-April2018).</span></span> <span data-ttu-id="7d181-111">如果已将旧版 Azure 模块作为 MSI 安装，安装程序会自动删除这些模块。</span><span class="sxs-lookup"><span data-stu-id="7d181-111">If you have installed previous versions of Azure modules as an MSI, the installer automatically removes them.</span></span> <span data-ttu-id="7d181-112">MSI 包在 `${env:ProgramFiles}\WindowsPowerShell\Modules` 中安装模块。</span><span class="sxs-lookup"><span data-stu-id="7d181-112">The MSI package installs modules in `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="7d181-113">`AzureRM` 和 `Azure` 模块都安装。</span><span class="sxs-lookup"><span data-stu-id="7d181-113">Both the `AzureRM` and `Azure` modules are installed.</span></span>

> [!NOTE]
> <span data-ttu-id="7d181-114">如果使用的是 Azure 经典部署模型，则只使用 `Azure` 模块。</span><span class="sxs-lookup"><span data-stu-id="7d181-114">Only use the `Azure` module if you are working with the Azure classic deployment model.</span></span>

<span data-ttu-id="7d181-115">若要开始使用 Azure PowerShell，需使用 [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet 将 `AzureRM` 加载到当前的 PowerShell 会话中，然后使用 Azure 凭据登录。</span><span class="sxs-lookup"><span data-stu-id="7d181-115">To start working with Azure PowerShell, you need to load `AzureRM` into your current PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span>

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="7d181-116">需对每个启动的新 PowerShell 会话重复这些步骤。</span><span class="sxs-lookup"><span data-stu-id="7d181-116">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="7d181-117">自动导入 `AzureRM` 模块要求设置 PowerShell 配置文件，详见[关于配置文件](/powershell/module/microsoft.powershell.core/about/about_profiles)。</span><span class="sxs-lookup"><span data-stu-id="7d181-117">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="7d181-118">若要了解如何跨会话保持 Azure 登录状态，请参阅[跨 PowerShell 会话保持用户凭据](context-persistence.md)。</span><span class="sxs-lookup"><span data-stu-id="7d181-118">To learn how to persist your Azure sign in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="install-or-update-on-windows-using-the-web-platform-installer"></a><span data-ttu-id="7d181-119">使用 Web 平台安装程序在 Windows 上进行安装或更新</span><span class="sxs-lookup"><span data-stu-id="7d181-119">Install or update on Windows using the Web Platform Installer</span></span>

<span data-ttu-id="7d181-120">下载 [Azure PowerShell WebPI 包](http://aka.ms/webpi-azps)，并开始安装。</span><span class="sxs-lookup"><span data-stu-id="7d181-120">Download the [Azure PowerShell WebPI package](http://aka.ms/webpi-azps) and start the install.</span></span> <span data-ttu-id="7d181-121">如果已通过 MSI 或 WebPI 安装旧版 Azure 模块，安装程序会自动删除这些模块。</span><span class="sxs-lookup"><span data-stu-id="7d181-121">If you have installed previous versions of Azure modules from an MSI or with WebPI, the installer automatically removes them.</span></span> <span data-ttu-id="7d181-122">模块安装到 `${env:ProgramFiles}\WindowsPowerShell\Modules` 中。</span><span class="sxs-lookup"><span data-stu-id="7d181-122">Modules are installed into `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="7d181-123">`AzureRM` 和 `Azure` 模块都安装。</span><span class="sxs-lookup"><span data-stu-id="7d181-123">Both the `AzureRM` and `Azure` modules are installed.</span></span>

> [!NOTE]
> <span data-ttu-id="7d181-124">如果使用的是 Azure 经典部署模型，则只使用 `Azure` 模块。</span><span class="sxs-lookup"><span data-stu-id="7d181-124">Only use the `Azure` module if you are working with the Azure classic deployment model.</span></span>

<span data-ttu-id="7d181-125">若要开始使用 Azure PowerShell，需使用 [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet 将 `AzureRM` 加载到当前的 PowerShell 会话中，然后使用 Azure 凭据登录。</span><span class="sxs-lookup"><span data-stu-id="7d181-125">To start working with Azure PowerShell, you need to load `AzureRM` into your current PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span>

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="7d181-126">需对每个启动的新 PowerShell 会话重复这些步骤。</span><span class="sxs-lookup"><span data-stu-id="7d181-126">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="7d181-127">自动导入 `AzureRM` 模块要求设置 PowerShell 配置文件，详见[关于配置文件](/powershell/module/microsoft.powershell.core/about/about_profiles)。</span><span class="sxs-lookup"><span data-stu-id="7d181-127">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="7d181-128">若要了解如何跨会话保持 Azure 登录状态，请参阅[跨 PowerShell 会话保持用户凭据](context-persistence.md)。</span><span class="sxs-lookup"><span data-stu-id="7d181-128">To learn how to persist your Azure sign in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>
