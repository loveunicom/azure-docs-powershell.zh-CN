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
ms.sourcegitcommit: ac4b53bb42a25aae013a9d8cd9ae98ada9397274
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/08/2018
ms.locfileid: "51275582"
---
# <a name="install-azure-powershell-on-windows-with-msi-or-web-platform-installer"></a>使用 MSI 或 Web 平台安装程序在 Windows 上安装 Azure PowerShell

本文介绍如何使用 MSI 或 Web 平台安装程序 (WebPI) 在 Windows 上安装 Azure PowerShell。  
只有当你的系统需要时才应使用这些安装方法。 若要在 Windows 上安装 Azure PowerShell，建议的方法是使用 PowerShellGet。 有关使用 PowerShellGet 安装 Azure PowerShell 的说明，请参阅[使用 PowerShellGet 安装 Azure PowerShell](install-azurerm-ps.md)。

若要在 Linux 或 macOS 环境中进行安装，请参阅[在 macOS 或 Linux 上安装 Azure PowerShell](install-azurermps-maclinux.md)。

## <a name="install-or-update-on-windows-using-the-msi-package"></a>使用 MSI 包在 Windows 上进行安装或更新

可以使用 [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v5.7.0-April2018) 中提供的 MSI 文件安装 Azure PowerShell。 如果已将旧版 Azure 模块作为 MSI 安装，安装程序会自动删除这些模块。 MSI 包在 `${env:ProgramFiles}\WindowsPowerShell\Modules` 中安装模块。 `AzureRM` 和 `Azure` 模块都安装。

> [!NOTE]
> 如果使用的是 Azure 经典部署模型，则只使用 `Azure` 模块。

若要开始使用 Azure PowerShell，需使用 [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet 将 `AzureRM` 加载到当前的 PowerShell 会话中，然后使用 Azure 凭据登录。

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

需对每个启动的新 PowerShell 会话重复这些步骤。 自动导入 `AzureRM` 模块要求设置 PowerShell 配置文件，详见[关于配置文件](/powershell/module/microsoft.powershell.core/about/about_profiles)。
若要了解如何跨会话保持 Azure 登录状态，请参阅[跨 PowerShell 会话保持用户凭据](context-persistence.md)。

## <a name="install-or-update-on-windows-using-the-web-platform-installer"></a>使用 Web 平台安装程序在 Windows 上进行安装或更新

下载 [Azure PowerShell WebPI 包](http://aka.ms/webpi-azps)，并开始安装。 如果已通过 MSI 或 WebPI 安装旧版 Azure 模块，安装程序会自动删除这些模块。 模块安装到 `${env:ProgramFiles}\WindowsPowerShell\Modules` 中。 `AzureRM` 和 `Azure` 模块都安装。

> [!NOTE]
> 如果使用的是 Azure 经典部署模型，则只使用 `Azure` 模块。

若要开始使用 Azure PowerShell，需使用 [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet 将 `AzureRM` 加载到当前的 PowerShell 会话中，然后使用 Azure 凭据登录。

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

需对每个启动的新 PowerShell 会话重复这些步骤。 自动导入 `AzureRM` 模块要求设置 PowerShell 配置文件，详见[关于配置文件](/powershell/module/microsoft.powershell.core/about/about_profiles)。
若要了解如何跨会话保持 Azure 登录状态，请参阅[跨 PowerShell 会话保持用户凭据](context-persistence.md)。
