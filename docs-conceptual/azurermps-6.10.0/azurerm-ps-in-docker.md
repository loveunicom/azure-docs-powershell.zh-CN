---
title: 在 Docker 容器中运行 Azure PowerShell
description: 如何在 Docker 容器中运行 Azure PowerShell。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/09/2018
ms.openlocfilehash: 0ed8f50abbcb2aa00192196f19004446dc696b5d
ms.sourcegitcommit: a749eb729f583c9d0dd86141bbd04984d77ae9ab
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/11/2018
ms.locfileid: "48882051"
---
# <a name="run-azure-powershell-in-a-docker-container"></a>在 Docker 容器中运行 Azure PowerShell

Microsoft 发布了已预装 Azure PowerShell 的 Docker 映像。 使用这些映像可以体验 Azure PowerShell，或者在隔离的环境中运行它。 有些映像运行 PowerShell Core 和 PowerShell 5。 

| 环境 | Docker 映像 |
|-------------|--------------|
| Windows 上的 PowerShell | [azuresdk/azure-powershell](https://hub.docker.com/r/azuresdk/azure-powershell/) |
| Windows 上的 PowerShell Core | [azuresdk/azure-powershell-core:nanoserver](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |
| Linux 上的 PowerShell Core | [azuresdk/azure-powershell-core:latest](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |

若要运行这些容器中的任何一个，请使用 `docker run -it $ImageName` 获取交互式终端。 例如，若要运行包含 PowerShell Core 的 Linux 容器：

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
