---
title: 在 macOS 或 Linux 上安装 Azure PowerShell
description: 如何在 macOS 或 Linux 上安装 Azure PowerShell。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: f014d62e898da195a38052db6b7e37a2cd96dfdd
ms.sourcegitcommit: 3a02e0c85c83de873981dd392500bc82c1cf9286
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2018
ms.locfileid: "46560110"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a>在 macOS 或 Linux 上安装 Azure PowerShell

对于非 Windows 平台，可以在 PowerShell Core v6 中运行 Azure PowerShell。 此版 PowerShell 可以在支持 .NET Core 的任何平台上使用。 可以使用一个与这些平台兼容的 .NET Standard 版 Azure PowerShell。

> [!NOTE]
> 目前，PowerShell Core v6 和 Azure PowerShell for .NET Core 都还是 beta 版本。
> 对这些产品的支持也是有限的。 如果你有需要询问的问题或发现了 bug，请在 GitHub 上提出问题。
>
> * [PowerShell Core v6 的问题](https://github.com/PowerShell/PowerShell/issues)
> * [Azure PowerShell 的问题](https://github.com/azure/azure-docs-powershell/issues)

## <a name="install-powershell-core"></a>安装 PowerShell Core

就 macOS 和大多数 Linux 发行版来说，PowerShell Core 的安装说明是不同的。
可在以下文章中找到详细说明：

* [在 macOS 上安装 PowerShell Core](/powershell/scripting/setup/installing-powershell-core-on-macos)
* [在 Linux 上安装 PowerShell Core](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-core"></a>安装 Azure PowerShell for .NET Core

PowerShell Core 附带已安装的 PowerShellGet 模块。 在 PowerShell 中安装模块需要提升的特权，因此需以超级用户身份启动会话。

```bash
sudo pwsh
```

若要安装 Azure PowerShell，请运行以下命令：

```powershell
Install-Module Az
```

> [!IMPORTANT]
> 在其他文章中详细介绍的 `AzureRM` 模块不是针对 .NET Core 生成的，因此不兼容 PowerShell Core。 `Az` 模块包含所有 `AzureRM` cmdlet 的命令别名，因此 `AzureRM` 的所有文档均适用。

默认情况下，PowerShell 库未配置为 PowerShellGet 的受信任存储库。 首次使用 PSGallery 时会看到以下提示：

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

请回答 `Yes` 或 `Yes to All` 继续安装。

## <a name="sign-in"></a>登录

若要开始使用 Azure PowerShell，需使用 [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet 将 `Az` 加载到 PowerShell 会话中，然后使用 Azure 凭据登录。 导入模块不需要提升的权限。

```powershell
# Import the module into the PowerShell session
Import-Module Az
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

需对每个启动的新 PowerShell 会话重复这些步骤。 自动导入 `Az` 模块要求设置 PowerShell 配置文件，详见[关于配置文件](/powershell/module/microsoft.powershell.core/about/about_profiles)。
在 macOS 和 Linux 上，应通过 `$Profile` 环境变量来使用配置文件。 若要了解如何跨会话保持 Azure 登录状态，请参阅[跨 PowerShell 会话保持用户凭据](context-persistence.md)。

## <a name="next-steps"></a>后续步骤

有关使用 Azure PowerShell 的详细信息，请参阅 [Azure PowerShell 入门](get-started-azureps.md)一文。
