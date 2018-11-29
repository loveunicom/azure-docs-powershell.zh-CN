---
title: 使用 PowerShellGet 在 Windows 上安装 Azure PowerShell
description: 如何使用 PowerShellGet 安装 Azure PowerShell
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/16/2018
ms.openlocfilehash: 616a9e14c3944e3151676d89b8a22e35d8f9d406
ms.sourcegitcommit: 558436c824d9b59731aa9b963cdc8df4dea932e7
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/29/2018
ms.locfileid: "52586422"
---
# <a name="install-azure-powershell-on-windows-with-powershellget"></a>使用 PowerShellGet 在 Windows 上安装 Azure PowerShell

本文介绍了在 Windows 环境中使用 PowerShellGet 安装 Azure PowerShell 模块的步骤。 PowerShellGet 和模块管理是安装 Azure PowerShell 的首选方法，但是如果希望使用 Web 平台安装程序或 MSI 包进行安装，请参阅[其他安装方法](other-install.md)。

有关如何在其他平台上安装 Azure PowerShell 的说明，请参阅[在 macOS 和 Linux 上安装和配置 Azure PowerShell](install-azurermps-maclinux.md)。

此版 Azure PowerShell 不支持 Azure 经典部署模型。 若要获取经典部署的支持，请按[安装 Azure PowerShell 服务管理模块](/powershell/azure/servicemanagement/install-azure-ps)中的说明操作。

[!INCLUDE[az-replacing-azurerm](../includes/az-replacing-azurerm.md)]

## <a name="requirements"></a>要求

从 Azure PowerShell 版本 6.0 开始，Azure PowerShell 需要 PowerShell 版本 5.0。 若要查看在计算机上运行的 PowerShell 的版本，请运行以下命令：

```powershell-interactive
$PSVersionTable.PSVersion
```

如果版本已过时，请参阅[升级现有的 Windows PowerShell](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell)。

> [!IMPORTANT]
> 本文档中介绍的模块 AzureRM 使用 .NET Framework。 这使得它与使用 .NET Core 的 PowerShell 6.0 兼容。 如果使用的是 PowerShell 6.0，请遵循[适用于 macOS 和 Linux 的安装说明](install-azurermps-maclinux.md)。

## <a name="install-the-azure-powershell-module"></a>安装 Azure Powershell 模块

需要提升的权限才能通过 PowerShell 库安装模块。 若要安装 Azure PowerShell，请在已提升权限的会话中运行以下命令：

```powershell-interactive
Install-Module -Name AzureRM -AllowClobber
```

> [!NOTE]
> 如果使用的 NuGet 版本低于 2.8.5.201，系统会提示下载并安装最新版本的 NuGet。

默认情况下，PowerShell 库未配置为 PowerShellGet 的受信任存储库。 首次使用 PSGallery 时会看到以下提示：

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

请回答 `Yes` 或 `Yes to All` 继续安装。

`AzureRM` 模块是 Azure PowerShell cmdlet 的汇总模块。 安装它时，系统会下载所有可用的 Azure 资源管理器模块并使其 cmdlet 可供使用。

## <a name="sign-in"></a>登录

若要开始使用 Azure PowerShell，请通过 Azure 凭据登录。

```powershell-interactive
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

> [!NOTE]
>
> 如果已禁用模块自动加载，则需使用 `Import-Module AzureRM` 手动导入模块。 考虑到模块的构造方式，这可能需要几秒钟时间。


需对每个启动的新 PowerShell 会话重复这些步骤。 若要了解如何跨 PowerShell 会话保持 Azure 登录状态，请参阅[跨 PowerShell 会话保持用户凭据](context-persistence.md)。

## <a name="update-the-azure-powershell-module"></a>更新 Azure PowerShell 模块

可以通过运行 [Update-Module](/powershell/module/powershellget/update-module) 来更新 Azure PowerShell 安装。 此命令不卸载以前的版本。

```powershell-interactive
Update-Module -Name AzureRM
```

若要从系统中删除旧版 Azure PowerShell，请参阅[卸载 Azure PowerShell 模块](uninstall-azurerm-ps.md)。

## <a name="use-multiple-versions-of-azure-powershell"></a>使用多个版本的 Azure PowerShell

可以安装多个版本的 Azure PowerShell。 若要检查是否安装了多个版本的 Azure PowerShell，请使用以下命令：

```powershell-interactive
Get-Module -Name AzureRM -List | select Name,Version
```

若要删除 Azure PowerShell 的某个版本，请参阅[卸载 Azure PowerShell 模块](uninstall-azurerm-ps.md)。

如果使用本地 Azure Stack 资源、运行旧版 Windows，或使用 Azure 经典部署模型，则可能需要多个版本。 若要安装旧版本，请在安装时提供 `-RequiredVersion` 参数。

```powershell-interactive
# Install version 2.3.0 of Azure PowerShell
Install-Module -Name AzureRM -RequiredVersion 2.3.0
```

加载 Azure PowerShell 模块时，默认加载最新版本。 若要加载另一版本，请提供 `-RequiredVersion` 参数。

```powershell-interactive
# Load version 2.3.0 of Azure PowerShell
Import-Module -Name AzureRM -RequiredVersion 2.3.0
```

## <a name="provide-feedback"></a>提供反馈

如果在使用 Azure Powershell 时发现了 bug，请[在 GitHub 上提出问题](https://github.com/Azure/azure-powershell/issues)。
若要从命令行提供反馈，请使用 [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet。

## <a name="next-steps"></a>后续步骤

若要开始使用 Azure PowerShell，请参阅 [Azure PowerShell 入门](get-started-azureps.md)，详细了解此模块及其功能。
