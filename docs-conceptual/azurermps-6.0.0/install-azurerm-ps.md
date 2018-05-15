---
title: 安装和配置 Azure PowerShell | Microsoft Docs
description: 如何安装和配置首次使用的 Azure PowerShell。
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/27/2018
ms.openlocfilehash: c6b8e2e8aa4afb9e58a2d357c4e51e19410a8188
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/08/2018
---
# <a name="install-and-configure-azure-powershell"></a>安装和配置 Azure PowerShell

本文介绍了在 Windows 环境中安装 Azure PowerShell 模块的步骤。
如果想要在 macOS 或 Linux 上使用 Azure PowerShell，请参阅以下文章：[在 macOS 和 Linux 上安装和配置 Azure PowerShell](install-azurermps-maclinux.md)。

## <a name="system-requirements"></a>系统要求

Azure PowerShell 6.0.0 版要求使用 5.0 或更高版本的 PowerShell。 旧版 Azure PowerShell 要求使用至少 3.0 版的 PowerShell 来运行 cmdlet。若要了解如何升级到 PowerShell 5.0，请查看[此表](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell)。

## <a name="step-1-install-powershellget"></a>步骤 1：安装 PowerShellGet

从 PowerShell 库安装 Azure PowerShell 是首选的安装方法。

安装 PowerShell 库中的项需要 PowerShellGet 模块。 请确保使用适当版本的 PowerShellGet 并满足其他系统要求。 运行以下命令，确定是否已在系统上安装 PowerShellGet。

```powershell
Get-Module -Name PowerShellGet -ListAvailable | Select-Object -Property Name,Version,Path
```

应会看到类似于下面的信息：

```Output
Name          Version Path
----          ------- ----
Name          Version Path
----          ------- ----
PowerShellGet 1.6.0   C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.6.0\PowerShellGet.psd1
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

需要 PowerShellGet 版本 1.1.2.0 或更高版本。 若要更新 PowerShellGet，请使用以下命令：

```powershell
Install-Module PowerShellGet -Force
```

如果没有安装 PowerShellGet，请参阅本文的[如何获取 PowerShellGet](#how-to-get-powershellget) 部分。

> [!NOTE]
> 使用 PowerShellGet 需要一个允许运行脚本的执行策略。 有关 PowerShell 执行策略的详细信息，请参阅[关于执行策略](/powershell/module/microsoft.powershell.core/about/about_execution_policies)。

## <a name="step-2-install-azure-powershell"></a>步骤 2：安装 Azure PowerShell

从 PowerShell 库安装 Azure PowerShell 需要提升的特权。 从权限提升的 PowerShell 会话运行以下命令：

```powershell
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

默认情况下，PowerShell 库未配置为 PowerShellGet 的受信任存储库。 首次使用 PSGallery 时会看到以下提示：

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"): Y
```

回答“是”或“全部确认”，可继续进行安装。

> [!NOTE]
> 如果使用的 NuGet 版本低于 2.8.5.201，系统会提示下载并安装最新版本的 NuGet。

AzureRM 模块是 Azure 资源管理器 cmdlet 的汇总模块。 安装 AzureRM 模块时，将从 PowerShell 库下载先前未安装的所有 Azure PowerShell 模块。

如果安装了早期版本的 Azure PowerShell，可能会出错。 若要解决此问题，请参阅本文中的[更新到新版 Azure PowerShell](#update-azps) 部分。

## <a name="step-3-load-the-azurerm-module"></a>步骤 3：加载 AzureRM 模块
安装该模块后，需要将它加载到 PowerShell 会话中。 应该在正常（而非提升）的 PowerShell 会话中执行此操作。 可以使用 `Import-Module` cmdlet 加载模块，如下所示：

```powershell
Import-Module -Name AzureRM
```

## <a name="next-steps"></a>后续步骤

有关使用 Azure PowerShell 的详细信息，请参阅以下文章：

* [Azure PowerShell 入门](get-started-azureps.md)

## <a name="reporting-issues-and-feedback"></a>报告问题和反馈

如果遇到该工具的任何 bug，请在 GitHub 存储库的[问题](https://github.com/Azure/azure-powershell/issues)部分中提出问题。 若要从命令行提供反馈，请使用 `Send-Feedback` cmdlet。

## <a name="frequently-asked-questions"></a>常见问题

### <a name="how-to-get-powershellget"></a>如何获取 PowerShellGet

|场景|安装说明|
|---|---|
|Windows 10<br/>Windows Server 2016|内置在 OS 随附的 Windows Management Framework (WMF) 5.0 中|
|我想要升级到 PowerShell 5|<ol><li>[安装最新版本的 WMF](https://www.microsoft.com/en-us/download/details.aspx?id=54616)</li><li>运行以下命令：<br/>```Install-Module PowerShellGet -Force```</li></ol>|
|我正在运行某个包含 PowerShell 3 或 PowerShell 4 的 Windows 版本|<ol><il>[获取 PackageManagement 模块](http://go.microsoft.com/fwlink/?LinkID=746217)</il><li>运行以下命令：<br/>```Install-Module PowerShellGet -Force```</li></ol>|

<a id="helpmechoose"></a>
### <a name="checking-the-version-of-azure-powershell"></a>检查 Azure PowerShell 的版本

虽然建议尽早升级到最新版本，但仍然支持多个 Azure PowerShell 版本。 若要确定安装的 Azure PowerShell 版本，请从命令行运行 `Get-Module AzureRM`。

```powershell
Get-Module AzureRM -ListAvailable | Select-Object -Property Name,Version,Path
```

### <a name="support-for-classic-deployment-methods"></a>支持经典部署方法

如果部署使用了经典部署模型，则可以安装 Azure PowerShell 的服务管理版本。 有关详细信息，请参阅[安装 Azure PowerShell 服务管理模块](/powershell/azure/servicemanagement/install-azure-ps)。 Azure 和 AzureRM 模块共享通用的依赖项。 如果同时使用 Azure 和 AzureRM 模块，应该安装每个包的同一版本。

### <a id="update-azps"></a>更新到新版 Azure PowerShell

如果安装了包含 Service Management 模块的早期版本 Azure PowerShell，可能会出现以下错误：

```Output
PackageManagement\Install-Package : A command with name 'Get-AzureStorageContainerAcl' is already
available on this system. This module 'Azure.Storage' may override the existing commands. If you
still want to install this module 'Azure.Storage', use -AllowClobber parameter.

At C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PSModule.psm1:1772 char:21
+ ...          $null = PackageManagement\Install-Package @PSBoundParameters
+                      ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : InvalidOperation: (Microsoft.Power....InstallPackage:InstallPackage) [Install-Package], Exception
    + FullyQualifiedErrorId : CommandAlreadyAvailable,Validate-ModuleCommandAlreadyAvailable,Microsoft.PowerShell.PackageManagement.Cmdlets.InstallPackage
```

如错误消息所述，应该使用 -AllowClobber 参数安装模块。 请使用以下命令：

```powershell
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

有关详细信息，请参阅 [Install-Module](https://msdn.microsoft.com/powershell/reference/5.1/PowerShellGet/install-module) 的帮助主题。

### <a name="installing-module-versions-side-by-side"></a>并行安装多个模块版本

PowerShellGet 安装方法是唯一支持安装多个版本的方法。 例如，可能使用旧版 Azure PowerShell 编写了脚本，但没有时间或资源来更新这些脚本。 以下命令演示如何安装 Azure PowerShell 的多个版本：

```powershell
Install-Module -Name AzureRM -RequiredVersion 3.7.0
Install-Module -Name AzureRM -RequiredVersion 1.2.9
```

在一个 PowerShell 会话中只能加载一个模块版本。 必须打开新的 PowerShell 窗口，并使用 `Import-Module` 导入特定版本的 AzureRM cmdlet：

```powershell
Import-Module -Name AzureRM -RequiredVersion 1.2.9
```

> [!NOTE]
> 版本 2.1.0 和 1.2.6 是可以同时安装和使用的初始模块版本。 加载 Azure PowerShell 早期版本时，会加载不兼容版本的 **AzureRM.Profile** 模块。 这会导致在执行 cmdlet 时，cmdlet 会提示用户登录。

### <a name="other-installation-methods"></a>其他安装方法

有关使用 Web 平台安装程序或 MSI 包进行安装的信息，请参阅[其他安装方法](other-install.md)
