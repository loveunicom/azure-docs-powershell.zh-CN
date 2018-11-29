---
title: Azure PowerShell 的其他安装方式
description: 如何使用 MSI 在没有 PowerShellGet 的情况下安装 Azure PowerShell
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/16/2018
ms.openlocfilehash: b442da364a01cd6022c14cbb32a9b633676ca8c7
ms.sourcegitcommit: 558436c824d9b59731aa9b963cdc8df4dea932e7
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/29/2018
ms.locfileid: "52586966"
---
# <a name="install-azure-powershell-on-windows-with-msi"></a><span data-ttu-id="99cfe-103">使用 MSI 在 Windows 上安装 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="99cfe-103">Install Azure PowerShell on Windows with MSI</span></span>

<span data-ttu-id="99cfe-104">本文介绍如何使用 MSI 安装程序在 Windows 上安装 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="99cfe-104">This article explains how to install Azure PowerShell on Windows using an MSI installer.</span></span>  
<span data-ttu-id="99cfe-105">只有当你的系统需要时才应使用这些安装方法。</span><span class="sxs-lookup"><span data-stu-id="99cfe-105">Use these installation methods only if they're necessary for your system.</span></span> <span data-ttu-id="99cfe-106">若要在 Windows 上安装 Azure PowerShell，建议的方法是使用 PowerShellGet。</span><span class="sxs-lookup"><span data-stu-id="99cfe-106">The recommended way to install Azure PowerShell on Windows is with PowerShellGet.</span></span> <span data-ttu-id="99cfe-107">有关使用 PowerShellGet 安装 Azure PowerShell 的说明，请参阅[使用 PowerShellGet 安装 Azure PowerShell](install-azurerm-ps.md)。</span><span class="sxs-lookup"><span data-stu-id="99cfe-107">For instructions on using PowerShellGet to install Azure PowerShell, see [Install Azure PowerShell with PowerShellGet](install-azurerm-ps.md).</span></span>

> [!NOTE]
> <span data-ttu-id="99cfe-108">Web 平台安装程序安装方法不再适用于 Azure PowerShell 6.x 及更高版本。</span><span class="sxs-lookup"><span data-stu-id="99cfe-108">The Web Platform Installer method of installation is no longer available for versions of Azure PowerShell 6.x and higher.</span></span> <span data-ttu-id="99cfe-109">如果要求使用 Web 平台安装程序，请考虑改用 MSI，也可安装旧版 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="99cfe-109">If you require use of the Web Platform Installer please consider using the MSI instead, or you can install an earlier version of Azure PowerShell.</span></span>

<span data-ttu-id="99cfe-110">若要在 Linux 或 macOS 环境中进行安装，请参阅[在 macOS 或 Linux 上安装 Azure PowerShell](install-azurermps-maclinux.md)。</span><span class="sxs-lookup"><span data-stu-id="99cfe-110">To install on Linux or macOS environments, see [Install Azure PowerShell on macOS or Linux](install-azurermps-maclinux.md).</span></span>

## <a name="install-or-update-on-windows-using-the-msi-package"></a><span data-ttu-id="99cfe-111">使用 MSI 包在 Windows 上进行安装或更新</span><span class="sxs-lookup"><span data-stu-id="99cfe-111">Install or update on Windows using the MSI Package</span></span>

<span data-ttu-id="99cfe-112">可以使用 [GitHub](https://github.com/Azure/azure-powershell/releases/latest) 中提供的 MSI 文件安装 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="99cfe-112">Azure PowerShell can be installed using the MSI file available from [GitHub](https://github.com/Azure/azure-powershell/releases/latest).</span></span> <span data-ttu-id="99cfe-113">如果已将旧版 Azure 模块作为 MSI 安装，安装程序会自动删除这些模块。</span><span class="sxs-lookup"><span data-stu-id="99cfe-113">If you have installed previous versions of Azure modules as an MSI, the installer automatically removes them.</span></span> <span data-ttu-id="99cfe-114">MSI 包在 `${env:ProgramFiles}\WindowsPowerShell\Modules` 中安装模块。</span><span class="sxs-lookup"><span data-stu-id="99cfe-114">The MSI package installs modules in `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="99cfe-115">`AzureRM` 和 `Azure` 模块都安装。</span><span class="sxs-lookup"><span data-stu-id="99cfe-115">Both the `AzureRM` and `Azure` modules are installed.</span></span>

> [!NOTE]
> <span data-ttu-id="99cfe-116">如果使用的是 Azure 经典部署模型，则只使用 `Azure` 模块。</span><span class="sxs-lookup"><span data-stu-id="99cfe-116">Only use the `Azure` module if you are working with the Azure classic deployment model.</span></span>

<span data-ttu-id="99cfe-117">若要开始使用 Azure PowerShell，请通过 Azure 凭据登录。</span><span class="sxs-lookup"><span data-stu-id="99cfe-117">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

> [!NOTE]
>
> <span data-ttu-id="99cfe-118">如果已禁用模块自动加载，则需使用 `Import-Module AzureRM` 手动导入模块。</span><span class="sxs-lookup"><span data-stu-id="99cfe-118">If you've disabled module autoloading, you need to manually import the module with `Import-Module AzureRM`.</span></span> <span data-ttu-id="99cfe-119">考虑到模块的构造方式，这可能需要几秒钟时间。</span><span class="sxs-lookup"><span data-stu-id="99cfe-119">Because of the way the module is structured, this can take a few seconds.</span></span>

<span data-ttu-id="99cfe-120">需对每个启动的新 PowerShell 会话重复此步骤。</span><span class="sxs-lookup"><span data-stu-id="99cfe-120">You'll need to repeat this step for every new PowerShell session you start.</span></span> <span data-ttu-id="99cfe-121">若要了解如何跨 PowerShell 会话保持 Azure 登录状态，请参阅[跨 PowerShell 会话保持用户凭据](context-persistence.md)。</span><span class="sxs-lookup"><span data-stu-id="99cfe-121">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>
