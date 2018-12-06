---
title: 使用 PowerShellGet 安装 Azure PowerShell 的“Az”
description: 如何使用 PowerShellGet 在 Windows、macOS 和 Linux 上安装 Azure PowerShell。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/26/2018
ms.openlocfilehash: 3d52b18750341f220dc8e10d6bf89796457c5a10
ms.sourcegitcommit: 93f93b90ef88c2659be95f3acaba514fe9639169
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2018
ms.locfileid: "52826776"
---
# <a name="install-the-azure-powershell-az-module"></a>安装 Azure PowerShell 的“Az”模块

本文介绍如何使用 PowerShellGet 安装 Azure PowerShell 模块。 这些说明适用于 Windows、macOS 和 Linux 平台。 对于 Az 预览版，任何其他安装方法均不受支持。 

## <a name="requirements"></a>要求

Azure PowerShell 在 Windows 上可与 PowerShell 5.x 配合工作，在任何平台上都可与 PowerShell 6.x 配合工作。 若要查看在计算机上运行的 PowerShell 的版本，请运行以下命令：

```powershell-interactive
$PSVersionTable.PSVersion
```

如果你的版本已过时或需要安装 PowerShell，请参阅[安装各种版本的 PowerShell](https://docs.microsoft.com/en-us/powershell/scripting/setup/installing-powershell?view=powershell-6)。 从该页面中的链接可访问适用于你的平台的安装信息。

## <a name="install-the-azure-powershell-module"></a>安装 Azure Powershell 模块

> [!IMPORTANT]
>
> 可以同时安装 `AzureRM` 和 `Az` 模块。 如果同时安装这两个模块，__则不要启用别名__。
> 启用别名会导致在 `AzureRM` cmdlet 与 `Az` 命令别名之间出现冲突，并且可能会导致意外行为。
> 建议在安装 `Az` 模块之前卸载 `AzureRM`。 随时都可以卸载 `AzureRM` 或启用别名。 有关卸载说明，请参阅[卸载 Azure PowerShell 模块 (AzureRM)](uninstall-azurerm-ps.md)。 

若要在全局范围安装模块，需要具有提升的权限来安装 PowerShell 库中的模块。 若要安装 Azure PowerShell，请在提升的会话中（在 Windows 上“以管理员身份运行”，或在 macOS 或 Linux 上使用超级用户权限）运行以下命令：

```powershell-interactive
Install-Module -Name Az -AllowClobber
```

如果没有管理员权限，则可以通过添加 `-Scope` 参数为当前用户进行安装。

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

默认情况下，PowerShell 库未配置为 PowerShellGet 的受信任存储库。 首次使用 PSGallery 时会看到以下提示：

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

请回答 `Yes` 或 `Yes to All` 继续安装。

`Az` 模块是 Azure PowerShell cmdlet 的汇总模块。 安装它时，系统会下载所有可用的 Azure 资源管理器模块并使其 cmdlet 可供使用。

## <a name="sign-in"></a>登录

若要开始使用 Azure PowerShell，请通过 Azure 凭据登录。

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
>
> 如果已禁用模块自动加载，则需使用 `Import-Module Az` 手动导入模块。 考虑到模块的构造方式，这可能需要几秒钟时间。

需对每个启动的新 PowerShell 会话重复这些步骤。 若要了解如何跨 PowerShell 会话保持 Azure 登录状态，请参阅[跨 PowerShell 会话保持用户凭据](context-persistence.md)。

## <a name="update-the-azure-powershell-module"></a>更新 Azure PowerShell 模块

可以通过运行 [Update-Module](/powershell/module/powershellget/update-module) 来更新 Azure PowerShell 安装。 此命令不卸载以前的版本。

```powershell-interactive
Update-Module -Name Az
```

若要从系统中删除旧版 Azure PowerShell，请参阅[卸载 Azure PowerShell 模块](uninstall-azurerm-ps.md)。

## <a name="use-multiple-versions-of-azure-powershell"></a>使用多个版本的 Azure PowerShell

可以安装多个版本的 Azure PowerShell。 若要检查是否安装了多个版本的 Azure PowerShell，请使用以下命令：

```powershell-interactive
Get-Module -Name Az -List | select Name,Version
```

若要删除 Azure PowerShell 的某个版本，请参阅[卸载 Azure PowerShell 模块](uninstall-azurerm-ps.md)。

可以通过将 `-RequiredVersion` 参数与 `Install-Module` 和 `Import-Module` 配合使用来加载特定版本的 `Az` 模块：

```powershell-interactive
Install-Module -Name Az -RequiredVersion 0.4.0
Import-Module -Name Az -RequiredVersion 0.4.0
```

如果安装了该模块的多个版本，默认情况下会加载最新版本。

## <a name="provide-feedback"></a>提供反馈

如果在使用 Azure Powershell 时发现了 bug，请[在 GitHub 上提出问题](https://github.com/Azure/azure-powershell/issues)。
若要从命令行提供反馈，请使用 [Send-Feedback](/powershell/module/az.profile/send-feedback) cmdlet。

## <a name="next-steps"></a>后续步骤

若要开始使用 Azure PowerShell，请参阅 [Azure PowerShell 入门](get-started-azureps.md)，详细了解此模块及其功能。
