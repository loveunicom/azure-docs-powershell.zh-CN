---
title: Azure PowerShell 的其他安装方式
description: 如何使用 MSI 在没有 PowerShellGet 的情况下安装 Azure PowerShell
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: 52bcbe3f91600c96546c7d8ff5648977a7917ff9
ms.sourcegitcommit: ff44dec6418a449757bded3c6ebe0a7d4c05ee6e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/01/2018
ms.locfileid: "50737860"
---
# <a name="install-azure-powershell-on-windows-with-msi"></a><span data-ttu-id="e4daa-103">使用 MSI 在 Windows 上安装 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="e4daa-103">Install Azure PowerShell on Windows with MSI</span></span>

<span data-ttu-id="e4daa-104">本文介绍如何使用 MSI 安装程序在 Windows 上安装 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="e4daa-104">This article explains how to install Azure PowerShell on Windows using an MSI installer.</span></span>  
<span data-ttu-id="e4daa-105">只有当你的系统需要时才应使用这些安装方法。</span><span class="sxs-lookup"><span data-stu-id="e4daa-105">Use these installation methods only if they're necessary for your system.</span></span> <span data-ttu-id="e4daa-106">若要在 Windows 上安装 Azure PowerShell，建议的方法是使用 PowerShellGet。</span><span class="sxs-lookup"><span data-stu-id="e4daa-106">The recommended way to install Azure PowerShell on Windows is with PowerShellGet.</span></span> <span data-ttu-id="e4daa-107">有关使用 PowerShellGet 安装 Azure PowerShell 的说明，请参阅[使用 PowerShellGet 安装 Azure PowerShell](install-azurerm-ps.md)。</span><span class="sxs-lookup"><span data-stu-id="e4daa-107">For instructions on using PowerShellGet to install Azure PowerShell, see [Install Azure PowerShell with PowerShellGet](install-azurerm-ps.md).</span></span>

> [!NOTE]
> <span data-ttu-id="e4daa-108">Web 平台安装程序安装方法不再适用于 Azure PowerShell 6.x 及更高版本。</span><span class="sxs-lookup"><span data-stu-id="e4daa-108">The Web Platform Installer method of installation is no longer available for versions of Azure PowerShell 6.x and higher.</span></span> <span data-ttu-id="e4daa-109">如果要求使用 Web 平台安装程序，请考虑改用 MSI，也可安装旧版 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="e4daa-109">If you require use of the Web Platform Installer please consider using the MSI instead, or you can install an earlier version of Azure PowerShell.</span></span>

<span data-ttu-id="e4daa-110">若要在 Linux 或 macOS 环境中进行安装，请参阅[在 macOS 或 Linux 上安装 Azure PowerShell](install-azurermps-maclinux.md)。</span><span class="sxs-lookup"><span data-stu-id="e4daa-110">To install on Linux or macOS environments, see [Install Azure PowerShell on macOS or Linux](install-azurermps-maclinux.md).</span></span>

## <a name="install-or-update-on-windows-using-the-msi-package"></a><span data-ttu-id="e4daa-111">使用 MSI 包在 Windows 上进行安装或更新</span><span class="sxs-lookup"><span data-stu-id="e4daa-111">Install or update on Windows using the MSI Package</span></span>

<span data-ttu-id="e4daa-112">可以使用 [GitHub](https://github.com/Azure/azure-powershell/releases/latest) 中提供的 MSI 文件安装 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="e4daa-112">Azure PowerShell can be installed using the MSI file available from [GitHub](https://github.com/Azure/azure-powershell/releases/latest).</span></span> <span data-ttu-id="e4daa-113">如果已将旧版 Azure 模块作为 MSI 安装，安装程序会自动删除这些模块。</span><span class="sxs-lookup"><span data-stu-id="e4daa-113">If you have installed previous versions of Azure modules as an MSI, the installer automatically removes them.</span></span> <span data-ttu-id="e4daa-114">MSI 包在 `${env:ProgramFiles}\WindowsPowerShell\Modules` 中安装模块。</span><span class="sxs-lookup"><span data-stu-id="e4daa-114">The MSI package installs modules in `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="e4daa-115">`AzureRM` 和 `Azure` 模块都安装。</span><span class="sxs-lookup"><span data-stu-id="e4daa-115">Both the `AzureRM` and `Azure` modules are installed.</span></span>

> [!NOTE]
> <span data-ttu-id="e4daa-116">如果使用的是 Azure 经典部署模型，则只使用 `Azure` 模块。</span><span class="sxs-lookup"><span data-stu-id="e4daa-116">Only use the `Azure` module if you are working with the Azure classic deployment model.</span></span>

<span data-ttu-id="e4daa-117">若要开始使用 Azure PowerShell，需使用 [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet 将 `AzureRM` 加载到当前的 PowerShell 会话中，然后使用 Azure 凭据登录。</span><span class="sxs-lookup"><span data-stu-id="e4daa-117">To start working with Azure PowerShell, you need to load `AzureRM` into your current PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span>

```powershell
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="e4daa-118">需对每个启动的新 PowerShell 会话重复这些步骤。</span><span class="sxs-lookup"><span data-stu-id="e4daa-118">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="e4daa-119">自动导入 `AzureRM` 模块要求设置 PowerShell 配置文件，详见[关于配置文件](/powershell/module/microsoft.powershell.core/about/about_profiles)。</span><span class="sxs-lookup"><span data-stu-id="e4daa-119">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="e4daa-120">若要了解如何跨会话保持 Azure 登录状态，请参阅[跨 PowerShell 会话保持用户凭据](context-persistence.md)。</span><span class="sxs-lookup"><span data-stu-id="e4daa-120">To learn how to persist your Azure sign-in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>
