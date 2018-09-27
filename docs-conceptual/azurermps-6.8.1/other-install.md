---
title: Azure PowerShell 的其他安装方式
description: 如何使用 MSI 在没有 PowerShellGet 的情况下安装 Azure PowerShell
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: 6bf66e312557f047a9393e26b9de736c1c55c261
ms.sourcegitcommit: 3a02e0c85c83de873981dd392500bc82c1cf9286
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2018
ms.locfileid: "46560195"
---
# <a name="install-azure-powershell-on-windows-with-msi"></a>使用 MSI 在 Windows 上安装 Azure PowerShell

本文介绍如何使用 MSI 安装程序在 Windows 上安装 Azure PowerShell。  
只有当你的系统需要时才应使用这些安装方法。 若要在 Windows 上安装 Azure PowerShell，建议的方法是使用 PowerShellGet。 有关使用 PowerShellGet 安装 Azure PowerShell 的说明，请参阅[使用 PowerShellGet 安装 Azure PowerShell](install-azurerm-ps.md)。

> [!NOTE]
> Web 平台安装程序安装方法不再适用于 Azure PowerShell 6.x 及更高版本。 如果要求使用 Web 平台安装程序，请考虑改用 MSI，也可安装旧版 Azure PowerShell。

若要在 Docker 容器中运行 Azure PowerShell，请参阅[在 Docker 中运行 Azure PowerShell](azurerm-ps-in-docker.md)。

若要在 Linux 或 macOS 环境中进行安装，请参阅[在 macOS 或 Linux 上安装 Azure PowerShell](install-azurermps-maclinux.md)。

## <a name="install-or-update-on-windows-using-the-msi-package"></a>使用 MSI 包在 Windows 上进行安装或更新

可以使用 [GitHub](https://github.com/Azure/azure-powershell/releases/latest) 中提供的 MSI 文件安装 Azure PowerShell。 如果已将旧版 Azure 模块作为 MSI 安装，安装程序会自动删除这些模块。 MSI 包在 `${env:ProgramFiles}\WindowsPowerShell\Modules` 中安装模块。 `AzureRM` 和 `Azure` 模块都安装。

> [!NOTE]
> 如果使用的是 Azure 经典部署模型，则只使用 `Azure` 模块。

若要开始使用 Azure PowerShell，需使用 [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet 将 `AzureRM` 加载到当前的 PowerShell 会话中，然后使用 Azure 凭据登录。

```powershell
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

需对每个启动的新 PowerShell 会话重复这些步骤。 自动导入 `AzureRM` 模块要求设置 PowerShell 配置文件，详见[关于配置文件](/powershell/module/microsoft.powershell.core/about/about_profiles)。
若要了解如何跨会话保持 Azure 登录状态，请参阅[跨 PowerShell 会话保持用户凭据](context-persistence.md)。