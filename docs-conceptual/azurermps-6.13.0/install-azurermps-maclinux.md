---
title: 在 macOS 或 Linux 上安装 Azure PowerShell
description: 如何在 macOS 或 Linux 上安装 Azure PowerShell。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/05/2018
ms.openlocfilehash: f60ea1c608be4b1c8319d53303713ba039276abc
ms.sourcegitcommit: 93f93b90ef88c2659be95f3acaba514fe9639169
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2018
ms.locfileid: "52828053"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a>在 macOS 或 Linux 上安装 Azure PowerShell

对于非 Windows 平台，可以在 PowerShell Core v6 中运行 Azure PowerShell。 此版 PowerShell 可以在支持 .NET Core 的任何平台上使用。 可以使用一个与这些平台兼容的 .NET Standard 版 Azure PowerShell。

> [!NOTE]
> 目前，Azure PowerShell for .NET Standard 仍处于测试阶段。
> 如果你有需要询问的问题或发现了 bug，请在 GitHub 上提出问题。
>
> * [Azure PowerShell 的问题](https://github.com/azure/azure-docs-powershell/issues)

## <a name="install-powershell-core"></a>安装 PowerShell Core

就 macOS 和大多数 Linux 发行版来说，PowerShell Core 的安装说明是不同的。
可在以下文章中找到详细说明：

* [在 macOS 上安装 PowerShell Core](/powershell/scripting/setup/installing-powershell-core-on-macos)
* [在 Linux 上安装 PowerShell Core](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-standard"></a>安装 Azure PowerShell for .NET Standard

> [!IMPORTANT]
> 在其他文章中详细介绍的 `AzureRM` 模块不兼容 PowerShell Core。
> 必须安装 `Az` 模块才能获取 PowerShell Core 中的 Azure PowerShell 功能。

PowerShell Core 附带已安装的 PowerShellGet 模块。 请使用以下命令启动 PowerShell：

```bash
pwsh
```

若要安装 Azure PowerShell，请运行以下命令：

```powershell-interactive
Install-Module Az
```

> [!NOTE]
> 如果在尝试安装模块时遇到权限错误，则可能需要以超级用户模式运行 PowerShell 才能安装模块。
>
> ```bash
> sudo pwsh
> ```

默认情况下，PowerShell 库未配置为 PowerShellGet 的受信任存储库。 首次使用 PSGallery 时会看到以下提示：

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

请回答 `Yes` 或 `Yes to All` 继续安装。

## <a name="enable-aliases"></a>启用别名

为了兼容现有的 `AzureRM` 模块，新的 `Az` 模块可以为 `AzureRM` cmdlet 创建后向兼容的别名。 第一次使用该模块之前，请使用以下命令设置这些别名：

```powershell-interactive
# Import the module into the PowerShell session
Import-Module Az
# Enable AzureRM aliases for the user
Enable-AzureRmAlias -Scope CurrentUser
```

该命令只为当前用户设置别名。 请查看 cmdlet 帮助，了解可以为 `-Scope` 提供哪些其他的值来设置别名。

> [!NOTE]
> 如果遇到有关路径位置的错误，请确保它存在于本地系统中。 如果范围仅限 `CurrentUser`，则可通过在 `bash` 中运行以下命令来解决该错误：
>
> ```bash
> mkdir -p $HOME/.config/powershell
> ```

## <a name="sign-in"></a>登录

若要开始使用 Azure PowerShell，需使用 [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet 将 `Az` 加载到 PowerShell 会话中，然后使用 Azure 凭据登录。 导入模块不需要提升的权限。

```powershell-interactive
# Import the module into the PowerShell session
Import-Module Az
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

需对每个启动的新 PowerShell 会话重复这些步骤。 自动导入 `Az` 模块要求设置 PowerShell 配置文件，详见[关于配置文件](/powershell/module/microsoft.powershell.core/about/about_profiles)。
在 macOS 和 Linux 上，应通过 `$Profile` 环境变量来使用配置文件。 若要了解如何跨会话保持 Azure 登录状态，请参阅[跨 PowerShell 会话保持用户凭据](context-persistence.md)。

## <a name="next-steps"></a>后续步骤

有关使用 Azure PowerShell 的详细信息，请参阅 [Azure PowerShell 入门](get-started-azureps.md)一文。
