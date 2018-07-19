---
title: 在 Docker 容器中运行 Azure PowerShell
description: 如何在 Docker 容器中运行 Azure PowerShell。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/20/2018
ms.openlocfilehash: 656c58fbb7cafb539736a0083d6aed1f46b7b98d
ms.sourcegitcommit: cb1fd248920d7efca67bd6c738a3b47206df7890
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/13/2018
ms.locfileid: "39024930"
---
# <a name="run-azure-powershell-in-a-docker-container"></a>在 Docker 容器中运行 Azure PowerShell

有一组通过 Azure PowerShell 预先配置的 Docker 映像。 提供了两种类型的容器：在 Windows 上运行传统 PowerShell 的容器，以及在 Windows 或 Linux 上运行 PowerShell Core 的容器。

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

## <a name="use-a-powershell-core-container"></a>使用 PowerShell Core 容器

PowerShell Core 容器已预装 PowerShell Core v6 和 `AzureRM.NetCore` 模块。 请运行 [Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet，然后使用 Azure 帐户登录：

```powershell
Import-Module AzureRM.NetCore
Connect-AzureRmAccount
```

## <a name="use-the-windows-container-with-powershell"></a>将 Windows 容器与 PowerShell 配合使用

Windows 容器已预装 `AzureRM` 模块。 请运行 [Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet，然后使用 Azure 帐户登录：

```powershell
Import-Module AzureRM
Connect-AzureRmAccount
```