---
title: 在 Docker 容器中运行 Azure PowerShell
description: 如何在 Docker 容器中运行 Azure PowerShell。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/20/2018
ms.openlocfilehash: 27ac176d8bd0b142b7740b2ba6793edb500a8af3
ms.sourcegitcommit: dca906e73e943aac207cee23b79915773419c673
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/30/2018
ms.locfileid: "43250088"
---
# <a name="run-azure-powershell-in-a-docker-container"></a><span data-ttu-id="c1f2b-103">在 Docker 容器中运行 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="c1f2b-103">Run Azure PowerShell in a Docker container</span></span>

<span data-ttu-id="c1f2b-104">为了方便用户在可移植环境中运行 Azure PowerShell，Microsoft 发布了预安装了 Azure PowerShell 的 Docker 映像。</span><span class="sxs-lookup"><span data-stu-id="c1f2b-104">To make running Azure PowerShell in portable environments easy, Microsoft publishes Docker images with Azure PowerShell pre-installed.</span></span> <span data-ttu-id="c1f2b-105">这些映像为 Linux 来宾提供 PowerShell Core，为 Windows 来宾提供 PowerShell Core 或 PowerShell 5。</span><span class="sxs-lookup"><span data-stu-id="c1f2b-105">These images offer a Linux guest running PowerShell Core, or a Windows guest with either PowerShell Core or PowerShell 5.</span></span>

| <span data-ttu-id="c1f2b-106">环境</span><span class="sxs-lookup"><span data-stu-id="c1f2b-106">Environment</span></span> | <span data-ttu-id="c1f2b-107">Docker 映像</span><span class="sxs-lookup"><span data-stu-id="c1f2b-107">Docker image</span></span> |
|-------------|--------------|
| <span data-ttu-id="c1f2b-108">Windows 上的 PowerShell</span><span class="sxs-lookup"><span data-stu-id="c1f2b-108">PowerShell on Windows</span></span> | [<span data-ttu-id="c1f2b-109">azuresdk/azure-powershell</span><span class="sxs-lookup"><span data-stu-id="c1f2b-109">azuresdk/azure-powershell</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell/) |
| <span data-ttu-id="c1f2b-110">Windows 上的 PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="c1f2b-110">PowerShell Core on Windows</span></span> | [<span data-ttu-id="c1f2b-111">azuresdk/azure-powershell-core:nanoserver</span><span class="sxs-lookup"><span data-stu-id="c1f2b-111">azuresdk/azure-powershell-core:nanoserver</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |
| <span data-ttu-id="c1f2b-112">Linux 上的 PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="c1f2b-112">PowerShell Core on Linux</span></span> | [<span data-ttu-id="c1f2b-113">azuresdk/azure-powershell-core:latest</span><span class="sxs-lookup"><span data-stu-id="c1f2b-113">azuresdk/azure-powershell-core:latest</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |

<span data-ttu-id="c1f2b-114">若要运行这些容器中的任何一个，请使用 `docker run -it $ImageName` 获取交互式终端。</span><span class="sxs-lookup"><span data-stu-id="c1f2b-114">To run any of these containers, you use `docker run -it $ImageName` to get an interactive terminal.</span></span> <span data-ttu-id="c1f2b-115">例如，若要在 Linux 容器上运行 PowerShell Core，请使用：</span><span class="sxs-lookup"><span data-stu-id="c1f2b-115">For example, to run the PowerShell Core on Linux container, use:</span></span>

```powershell
docker run -it azuresdk/azure-powershell-core:latest
```

> [!NOTE]
> <span data-ttu-id="c1f2b-116">若要在 Docker 中运行 Windows 容器，主机 OS 必须是 Windows 并且 Docker 必须设置为运行 Windows 容器。</span><span class="sxs-lookup"><span data-stu-id="c1f2b-116">To run a Windows container in Docker, your host OS must be Windows and Docker must be set to run Windows containers.</span></span> <span data-ttu-id="c1f2b-117">若要了解如何在 Docker 中在 Windows 与 Linux 环境之间进行切换，请参阅 Docker 文档[在 Windows 与 Linux 容器之间进行切换](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers)。</span><span class="sxs-lookup"><span data-stu-id="c1f2b-117">To learn about switching between Windows and Linux environments in Docker, see the Docker documentation [Switch between Windows and Linux containers](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers).</span></span>

## <a name="use-a-powershell-core-container"></a><span data-ttu-id="c1f2b-118">使用 PowerShell Core 容器</span><span class="sxs-lookup"><span data-stu-id="c1f2b-118">Use a PowerShell Core container</span></span>

<span data-ttu-id="c1f2b-119">PowerShell Core 容器已预装 PowerShell Core v6 和 `AzureRM.NetCore` 模块。</span><span class="sxs-lookup"><span data-stu-id="c1f2b-119">The PowerShell Core containers come with PowerShell Core v6 and the `AzureRM.NetCore` module pre-installed.</span></span> <span data-ttu-id="c1f2b-120">请运行 [Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet，然后使用 Azure 帐户登录：</span><span class="sxs-lookup"><span data-stu-id="c1f2b-120">Run the [Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet and then sign in with your Azure account:</span></span>

```powershell
Import-Module AzureRM.NetCore
Connect-AzureRmAccount
```

## <a name="use-the-windows-container-with-powershell"></a><span data-ttu-id="c1f2b-121">将 Windows 容器与 PowerShell 配合使用</span><span class="sxs-lookup"><span data-stu-id="c1f2b-121">Use the Windows container with PowerShell</span></span>

<span data-ttu-id="c1f2b-122">Windows 容器已预装 `AzureRM` 模块。</span><span class="sxs-lookup"><span data-stu-id="c1f2b-122">The Windows container has the `AzureRM` module pre-installed.</span></span> <span data-ttu-id="c1f2b-123">请运行 [Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet，然后使用 Azure 帐户登录：</span><span class="sxs-lookup"><span data-stu-id="c1f2b-123">Run the [Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet and then sign in with your Azure account:</span></span>

```powershell
Import-Module AzureRM
Connect-AzureRmAccount
```
