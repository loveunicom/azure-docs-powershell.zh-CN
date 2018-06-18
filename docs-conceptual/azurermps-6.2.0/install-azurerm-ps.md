---
title: 使用 PowerShellGet 安装 Azure PowerShell
description: 如何使用 PowerShellGet 安装 Azure PowerShell
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/31/2018
ms.openlocfilehash: 9b7046157e32a5c8473210e9840f9ae1b2f45902
ms.sourcegitcommit: bcf80dfd7fbe17e82e7ad029802cfe8a2f02b15c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "35323095"
---
# <a name="install-azure-powershell-with-powershellget"></a>使用 PowerShellGet 安装 Azure PowerShell

本文介绍了在 Windows 环境中使用 PowerShellGet 安装 Azure PowerShell 模块的步骤。  这是安装 Azure PowerShell 的首选方法，但是如果希望使用 Web 平台安装程序或 MSI 包进行安装，请参阅[其他安装方法](other-install.md)。

如果想要在 macOS 或 Linux 上使用 Azure PowerShell，请参阅以下文章：[在 macOS 和 Linux 上安装和配置 Azure PowerShell](install-azurermps-maclinux.md)。

## <a name="system-requirements"></a>系统要求

Azure PowerShell 6.1.0 版要求使用 5.0 或更高版本的 PowerShell。 有关升级到 PowerShell 5.0 的信息，请参阅[升级现有的 Windows PowerShell](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell)。

PowerShellGet 自动包括为 PowerShell 5.0 的一部分。

## <a name="install-or-update-the-azure-powershell-module"></a>安装或更新 Azure PowerShell 模块

从 PowerShell 库安装 Azure PowerShell 需要提升的特权。 从权限提升的 PowerShell 会话运行以下命令：

```powershell
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

> [!IMPORTANT]
> 此命令将更新系统上任何现有的 Azure PowerShell 安装。 如果需要安装多个版本，请参阅常见问题解答中的[是否可以安装 Azure PowerShell 的多个版本？](#multiple-versions)

默认情况下，PowerShell 库未配置为 PowerShellGet 的受信任存储库。 首次使用 PSGallery 时会看到以下提示：

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

回答“是”或“全部确认”，可继续进行安装。

> [!NOTE]
> 如果使用的 NuGet 版本低于 2.8.5.201，系统会提示下载并安装最新版本的 NuGet。

AzureRM 模块是 Azure 资源管理器 cmdlet 的汇总模块。 安装 AzureRM 模块时，将从 PowerShell 库下载先前未安装的所有 Azure PowerShell 模块。

## <a name="load-the-azure-powershell-module"></a>加载 Azure PowerShell 模块

安装该模块后，需要将它加载到 PowerShell 会话中。 应该在正常（而非提升）的 PowerShell 会话中执行此操作。 可以使用 `Import-Module` cmdlet 加载模块，如下所示：

```powershell
Import-Module -Name AzureRM
```

## <a name="reporting-issues-and-feedback"></a>报告问题和反馈

如果遇到工具的任何 bug，请[在 GitHub 上提出问题](https://github.com/Azure/azure-powershell/issues)。 若要从命令行提供反馈，请使用 `Send-Feedback` cmdlet。

## <a name="next-steps"></a>后续步骤

有关使用 Azure PowerShell 的详细信息，请参阅以下文章：

* [Azure PowerShell 入门](get-started-azureps.md)

## <a name="frequently-asked-questions"></a>常见问题

### <a id="helpmechoose"></a>如何检查 Azure PowerShell 的版本？

虽然建议尽早升级到最新版本，但仍然支持多个 Azure PowerShell 版本。 若要确定安装的 Azure PowerShell 版本，请从命令行运行 `Get-Module AzureRM`。

```powershell
Get-Module AzureRM -ListAvailable | Select-Object -Property Name,Version,Path
```

### <a name="can-i-use-azure-powershell-for-azure-classic-deployments"></a>是否可以使用 Azure PowerShell 进行 Azure 经典部署？

如果部署使用了经典部署模型，则可以安装 Azure PowerShell 的服务管理版本。 有关详细信息，请参阅[安装 Azure PowerShell 服务管理模块](/powershell/azure/servicemanagement/install-azure-ps)。 Azure 和 AzureRM 模块共享通用的依赖项。 如果同时使用 Azure 和 AzureRM 模块，应该安装每个包的同一版本。

### <a name="a-namemultiple-versionscan-i-install-multiple-versions-of-azure-powershell"></a><a name="multiple-versions"/>是否可以安装 Azure PowerShell 的多个版本？

PowerShellGet 是唯一支持多个版本的安装方法。 若要安装多个版本，可以向 `Install-Module` cmdlet 中添加 `-RequiredVersion` 参数。 例如，若要同时安装 6.1.0 和 1.2.9 这两个版本，请使用以下命令：

```powershell
Install-Module -Name AzureRM -RequiredVersion 6.1.0
Install-Module -Name AzureRM -RequiredVersion 1.2.9
```

在一个 PowerShell 会话中只能加载一个模块版本。 必须打开一个新的 PowerShell 窗口，并使用 `Import-Module` 导入 Azure PowerShell 模块的特定版本。

```powershell
Import-Module -Name AzureRM -RequiredVersion 1.2.9
```

> [!NOTE]
> 版本 2.1.0 和 1.2.6 是可以同时安装和使用的初始模块版本。 加载 Azure PowerShell 早期版本时，会加载不兼容版本的 **AzureRM.Profile** 模块。 这会导致在执行 cmdlet 时，cmdlet 会提示用户登录。
