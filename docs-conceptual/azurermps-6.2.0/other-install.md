---
title: Azure PowerShell 的其他安装方式
description: 如何使用 MSI 包或 Web 平台安装程序安装 Azure PowerShell。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/06/2018
ms.openlocfilehash: 0919583d9cb05a75fae3b812eed84109be8b28aa
ms.sourcegitcommit: bcf80dfd7fbe17e82e7ad029802cfe8a2f02b15c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "35323316"
---
# <a name="other-installation-methods"></a>其他安装方法

本文介绍了如何使用 MSI 或 Web 平台安装程序 (WebPI) 安装 Azure PowerShell。 还可以从 Docker 容器内部运行 Azure PowerShell。 只有当你的系统需要时才应使用这些安装方法。 安装 Azure PowerShell 的常规方法是使用 PowerShellGet。 有关使用 PowerShellGet 安装 Azure PowerShell 的说明，请参阅[使用 PowerShellGet 安装 Azure PowerShell](install-azurerm-ps.md)。

若要在 Linux 或 macOS 环境中进行安装，请参阅[在 macOS 或 Linux 上安装 Azure PowerShell](install-azurermps-maclinux.md)。

## <a name="install-or-update-on-windows-using-the-web-platform-installer"></a>使用 Web 平台安装程序在 Windows 上进行安装或更新

从 WebPI 安装最新 Azure PowerShell 的过程与安装以往版本的过程相同。
下载 [Azure PowerShell WebPI 包](http://aka.ms/webpi-azps)，并开始安装。

> [!NOTE]
> 如果之前从 PowerShell 库安装了 Azure 模块，安装程序会自动删除这些模块。 这可确保只安装一个 Azure PowerShell 版本，因此可以简化环境。 但是，在某些情况下，可能需要同时安装多个版本。
>
> PowerShell 库模块在 `$env:ProgramFiles\WindowsPowerShell\Modules` 中安装模块。 相比之下，WebPI 安装程序在 `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\` 中安装 Azure 模块。
>
> 如果在安装期间出错，可以手动删除 `$env:ProgramFiles\WindowsPowerShell\Modules` 文件夹中的 `Azure*` 文件夹，并重试安装。

完成安装后，`$env:PSModulePath` 设置中应有包含 Azure PowerShell cmdlet 的目录。 可以使用以下命令验证是否正确安装了 Azure PowerShell：

```powershell
# To make sure the Azure PowerShell module is available after you install
Get-Module -ListAvailable Azure* | Select-Object Name, Version, Path
```

> [!NOTE]
> 从 WebPI 安装时，可能会发生一个已知问题。 如果计算机由于系统更新或其他安装而需要重新启动，有可能会导致更新 `$env:PSModulePath` 时无法包含 Azure PowerShell 的安装路径。

安装后尝试加载或执行 cmdlet 时，可能会出现以下错误消息：

```
PS C:\> Connect-AzureRmAccount
Connect-AzureRmAccount : The term 'Connect-AzureRmAccount' is not recognized as the name of a cmdlet,
function, script file, or operable program. Check the spelling of the name, or if a path was
included, verify that the path is correct and try again.
At line:1 char:1
+ Connect-AzureRmAccount
+ ~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : ObjectNotFound: (Connect-AzureRmAccount:String) [], CommandNotFoundException
    + FullyQualifiedErrorId : CommandNotFoundException
```

重启计算机或使用完全限定的路径导入模块可更正此问题。

```powershell
Import-Module "$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\AzureRM.psd1"
```

## <a name="install-or-update-on-windows-using-the-msi-package"></a>使用 MSI 包在 Windows 上进行安装或更新

可以使用 [GitHub](https://aka.ms/azps-release) 中提供的 MSI 文件安装 Azure PowerShell。 如果已安装旧版 Azure 模块，安装程序会自动删除这些模块。 MSI 包在 `$env:ProgramFiles\WindowsPowerShell\Modules` 中安装模块，但不会创建版本特定的文件夹。

## <a name="run-in-a-docker-container"></a>在 Docker 容器中运行

我们维护着随 Azure PowerShell 预先配置的一组 Docker 映像。 提供了两种类型的容器：在 Windows 上运行传统 PowerShell 的容器，和在 Windows 或 Linux 上运行 PowerShell Core 的容器。

| 环境 | Docker 映像 |
|-------------|--------------|
| Windows 上的 PowerShell | [azuresdk/azure-powershell](https://hub.docker.com/r/azuresdk/azure-powershell/) |
| Windows 上的 PowerShell Core | [azuresdk/azure-powershell-core:nanoserver](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |
| Linux 上的 PowerShell Core | [azuresdk/azure-powershell-core:latest](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |

若要运行这些容器中的任何一个，请使用 `docker run -it $ImageName` 获取交互式终端。 例如，若要在 Linux 容器上运行 PowerShell Core，请使用：

```powershell
docker run -it azuresdk/azure-powershell-core:latest
```

> [!NOTE]
> 若要在 Docker 中运行 Windows 容器，主机 OS 必须是 Windows 并且 Docker 必须设置为运行 Windows 容器。 若要了解如何在 Docker 中在 Windows 与 Linux 环境之间进行切换，请参阅 Docker 文档[在 Windows 与 Linux 容器之间进行切换](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers)。