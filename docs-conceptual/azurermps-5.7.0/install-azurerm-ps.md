---
title: 使用 PowerShellGet 在 Windows 上安装 Azure PowerShell
description: 如何使用 PowerShellGet 安装 Azure PowerShell
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/15/2018
ms.openlocfilehash: 5f7f65aa25d86feb77a85fc28d122118216542cc
ms.sourcegitcommit: 558436c824d9b59731aa9b963cdc8df4dea932e7
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/29/2018
ms.locfileid: "52588037"
---
# <a name="install-azure-powershell-on-windows-with-powershellget"></a>使用 PowerShellGet 在 Windows 上安装 Azure PowerShell

本文介绍了在 Windows 环境中使用 PowerShellGet 安装 Azure PowerShell 模块的步骤。 PowerShellGet 和模块管理是安装 Azure PowerShell 的首选方法，但是如果希望使用 Web 平台安装程序或 MSI 包进行安装，请参阅[其他安装方法](other-install.md)。

有关如何在其他平台上安装 Azure PowerShell 的说明，请参阅[在 macOS 和 Linux 上安装和配置 Azure PowerShell](install-azurermps-maclinux.md)。

此版 Azure PowerShell 不支持 Azure 经典部署模型。 若要获取经典部署的支持，请按[安装 Azure PowerShell 服务管理模块](/powershell/azure/servicemanagement/install-azure-ps)中的说明操作。

## <a name="requirements"></a>要求

若要安装 Azure PowerShell，则需 PowerShellGet 1.1.2.0 或更高版本。 若要查看它在系统上是否可用，请运行以下命令：

```powershell-interactive
Get-Module -Name PowerShellGet -ListAvailable | Select-Object -Property Name,Version,Path
```

应会看到类似于下面的信息：

```output
Name          Version Path
----          ------- ----
Name          Version Path
----          ------- ----
PowerShellGet 1.6.0   C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.6.0\PowerShellGet.psd1
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

如需更新安装的 PowerShellGet，请运行以下命令：

```powershell-interactive
Install-Module PowerShellGet -Force
```

如果尚未安装 PowerShellGet，请按下表中针对系统的说明操作。

|场景|安装说明|
|---|---|
|Windows 10<br/>Windows Server 2016|内置在 OS 随附的 Windows Management Framework (WMF) 5.0 中|
|升级到 PowerShell 5| <ol><li>[安装最新版本的 WMF](https://www.microsoft.com/en-us/download/details.aspx?id=54616)</li><li>运行以下命令：<br/>```Install-Module PowerShellGet -Force```</li></ol>|
|装有 PowerShell 3 或 PowerShell 4 的 Windows|<ol><il>[获取 PackageManagement 模块](http://go.microsoft.com/fwlink/?LinkID=746217)</il><li>运行以下命令：<br/>```Install-Module PowerShellGet -Force```</li></ol>|

> [!NOTE]
> 使用 PowerShellGet 需要一个允许运行脚本的执行策略。 有关 PowerShell 执行策略的详细信息，请参阅[关于执行策略](/powershell/module/microsoft.powershell.core/about/about_execution_policies)。
>
> [!IMPORTANT]
> 本文档中介绍的模块 AzureRM 使用 .NET Framework。 这使得它与使用 .NET Core 的 PowerShell 6.0 兼容。 如果使用的是 PowerShell 6.0，请遵循[适用于 macOS 和 Linux 的安装说明](install-azurermps-maclinux.md)。

## <a name="install-the-azure-powershell-module"></a>安装 Azure Powershell 模块

需要提升的权限才能通过 PowerShell 库安装模块。 若要安装 Azure PowerShell，请在已提升权限的会话中运行以下命令：

```powershell-interactive
Install-Module -Name AzureRM
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

若要开始使用 Azure PowerShell，需使用 [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet 将 `AzureRM` 加载到当前的 PowerShell 会话中，然后使用 Azure 凭据登录。

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

需对每个启动的新 PowerShell 会话重复这些步骤。 自动导入 `AzureRM` 模块要求设置 PowerShell 配置文件，详见[关于配置文件](/powershell/module/microsoft.powershell.core/about/about_profiles)。
若要了解如何跨会话保持 Azure 登录状态，请参阅[跨 PowerShell 会话保持用户凭据](context-persistence.md)。

## <a name="update-the-azure-powershell-module"></a>更新 Azure PowerShell 模块

可以通过运行 [Update-Module](/powershell/module/powershellget/update-module) 来更新 Azure PowerShell 安装。 此命令不卸载以前的版本。

```powershell-interactive
Update-Module -Name AzureRM
```

若要从系统中删除旧版 Azure PowerShell，请参阅[卸载 Azure PowerShell 模块](uninstall-azurerm-ps.md)。

## <a name="use-multiple-versions-of-azure-powershell"></a>使用多个版本的 Azure PowerShell

可以安装多个版本的 Azure PowerShell。 如果使用本地 Azure Stack 资源、运行不能更新到 PowerShell 5.0 的旧版 Windows，或者使用 Azure 经典部署模型，则可能需要多个版本。 若要安装旧版本，请在安装时提供 `-RequiredVersion` 参数。

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

如果在使用 Azure Powershell 时发现 Bug，请[在 GitHub 上提出问题](https://github.com/Azure/azure-powershell/issues)。
若要从命令行提供反馈，请使用 [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet。

## <a name="next-steps"></a>后续步骤

若要开始使用 Azure PowerShell，请参阅 [Azure PowerShell 入门](get-started-azureps.md)，详细了解此模块及其功能。
