---
title: Azure PowerShell 的其他安装方式 | Microsoft Docs
description: 如何使用 MSI 包或 Web 平台安装程序安装 Azure PowerShell。
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/06/2017
ms.openlocfilehash: cb4ced3b72b69546594d75e7eb7db822b549a664
ms.sourcegitcommit: 2eea03b7ac19ad6d7c8097743d33c7ddb9c4df77
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/06/2018
ms.locfileid: "34821439"
---
# <a name="other-installation-methods"></a>其他安装方法

Azure PowerShell 提供多种安装方法。 首选的方法是结合使用 PowerShellGet 和 PowerShell 库。 可以使用 Web 平台安装程序 (WebPI) 或者 GitHub 中提供的 MSI 文件在 Windows 上安装 Azure PowerShell。 也可以在 Docker 容器中安装 Azure PowerShell。

## <a name="install-on-windows-using-the-web-platform-installer"></a>使用 Web 平台安装程序在 Windows 上安装

从 WebPI 安装最新 Azure PowerShell 的过程与安装以往版本的过程相同。
下载 [Azure PowerShell WebPI 包](http://aka.ms/webpi-azps)，并开始安装。

> [!NOTE]
> 如果之前从 PowerShell 库安装了 Azure 模块，安装程序会自动删除这些模块。 这可确保只安装一个 Azure PowerShell 版本，因此可以简化环境。 但是，在某些情况下，可能需要同时安装多个版本。
>
> PowerShell 库模块在 `$env:ProgramFiles\WindowsPowerShell\Modules` 中安装模块。 相比之下，WebPI 安装程序在 `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\` 中安装 Azure 模块。
>
> 如果安装期间出错，可以手动删除 `$env:ProgramFiles\WindowsPowerShell\Modules` 文件夹中的 Azure* 文件夹，并重试安装。

完成安装后，`$env:PSModulePath` 设置中应有包含 Azure PowerShell cmdlet 的目录。 可以使用以下命令验证正确安装了 Azure PowerShell。

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

重启计算机或使用完全限定的路径导入模块可更正此问题。 例如：

```powershell
Import-Module "$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\AzureRM.psd1"
```

## <a name="install-on-windows-using-the-msi-package"></a>使用 MSI 包在 Windows 上安装

可以使用 [GitHub](https://aka.ms/azps-release) 中提供的 MSI 文件安装 Azure PowerShell。 如果已安装旧版 Azure 模块，安装程序会自动删除这些模块。 MSI 包在 `$env:ProgramFiles\WindowsPowerShell\Modules` 中安装模块，但不会创建版本特定的文件夹。

## <a name="install-in-a-docker-container"></a>在 Docker 容器中安装

我们维护预先配置了 Azure PowerShell 的 Docker 映像。

通过 `docker run` 运行容器。

```powershell
docker run azuresdk/azure-powershell
```

此外，我们还维护作为 PowerShell Core 容器的 cmdlet 子集。

对于 Mac/Linux，请使用 `latest` 映像。

```bash
docker run azuresdk/azure-powershell-core:latest
```

对于 Windows，请使用 `nanoserver` 映像。

```powershell
docker run azuresdk/azure-powershell-core:nanoserver
```

通过 [PowerShell 库](https://www.powershellgallery.com/)中的 `Install-Module` 将 Azure PowerShell 安装到映像上。
