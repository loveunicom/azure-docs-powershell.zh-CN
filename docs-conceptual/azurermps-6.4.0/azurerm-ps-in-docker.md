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
# <a name="run-azure-powershell-in-a-docker-container"></a><span data-ttu-id="c1c7b-103">在 Docker 容器中运行 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="c1c7b-103">Run Azure PowerShell in a Docker container</span></span>

<span data-ttu-id="c1c7b-104">有一组通过 Azure PowerShell 预先配置的 Docker 映像。</span><span class="sxs-lookup"><span data-stu-id="c1c7b-104">There are a set of Docker images preconfigured with Azure PowerShell.</span></span> <span data-ttu-id="c1c7b-105">提供了两种类型的容器：在 Windows 上运行传统 PowerShell 的容器，以及在 Windows 或 Linux 上运行 PowerShell Core 的容器。</span><span class="sxs-lookup"><span data-stu-id="c1c7b-105">Two types of containers are available: Those running traditional PowerShell on Windows, and a container running PowerShell Core on either Windows or Linux.</span></span>

| <span data-ttu-id="c1c7b-106">环境</span><span class="sxs-lookup"><span data-stu-id="c1c7b-106">Environment</span></span> | <span data-ttu-id="c1c7b-107">Docker 映像</span><span class="sxs-lookup"><span data-stu-id="c1c7b-107">Docker image</span></span> |
|-------------|--------------|
| <span data-ttu-id="c1c7b-108">Windows 上的 PowerShell</span><span class="sxs-lookup"><span data-stu-id="c1c7b-108">PowerShell on Windows</span></span> | [<span data-ttu-id="c1c7b-109">azuresdk/azure-powershell</span><span class="sxs-lookup"><span data-stu-id="c1c7b-109">azuresdk/azure-powershell</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell/) |
| <span data-ttu-id="c1c7b-110">Windows 上的 PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="c1c7b-110">PowerShell Core on Windows</span></span> | [<span data-ttu-id="c1c7b-111">azuresdk/azure-powershell-core:nanoserver</span><span class="sxs-lookup"><span data-stu-id="c1c7b-111">azuresdk/azure-powershell-core:nanoserver</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |
| <span data-ttu-id="c1c7b-112">Linux 上的 PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="c1c7b-112">PowerShell Core on Linux</span></span> | [<span data-ttu-id="c1c7b-113">azuresdk/azure-powershell-core:latest</span><span class="sxs-lookup"><span data-stu-id="c1c7b-113">azuresdk/azure-powershell-core:latest</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |

<span data-ttu-id="c1c7b-114">若要运行这些容器中的任何一个，请使用 `docker run -it $ImageName` 获取交互式终端。</span><span class="sxs-lookup"><span data-stu-id="c1c7b-114">To run any of these containers, you use `docker run -it $ImageName` to get an interactive terminal.</span></span> <span data-ttu-id="c1c7b-115">例如，若要在 Linux 容器上运行 PowerShell Core，请使用：</span><span class="sxs-lookup"><span data-stu-id="c1c7b-115">For example, to run the PowerShell Core on Linux container, use:</span></span>

```powershell
docker run -it azuresdk/azure-powershell-core:latest
```

> [!NOTE]
> <span data-ttu-id="c1c7b-116">若要在 Docker 中运行 Windows 容器，主机 OS 必须是 Windows 并且 Docker 必须设置为运行 Windows 容器。</span><span class="sxs-lookup"><span data-stu-id="c1c7b-116">To run a Windows container in Docker, your host OS must be Windows and Docker must be set to run Windows containers.</span></span> <span data-ttu-id="c1c7b-117">若要了解如何在 Docker 中在 Windows 与 Linux 环境之间进行切换，请参阅 Docker 文档[在 Windows 与 Linux 容器之间进行切换](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers)。</span><span class="sxs-lookup"><span data-stu-id="c1c7b-117">To learn about switching between Windows and Linux environments in Docker, see the Docker documentation [Switch between Windows and Linux containers](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers).</span></span>

## <a name="use-a-powershell-core-container"></a><span data-ttu-id="c1c7b-118">使用 PowerShell Core 容器</span><span class="sxs-lookup"><span data-stu-id="c1c7b-118">Use a PowerShell Core container</span></span>

<span data-ttu-id="c1c7b-119">PowerShell Core 容器已预装 PowerShell Core v6 和 `AzureRM.NetCore` 模块。</span><span class="sxs-lookup"><span data-stu-id="c1c7b-119">The PowerShell Core containers come with PowerShell Core v6 and the `AzureRM.NetCore` module pre-installed.</span></span> <span data-ttu-id="c1c7b-120">请运行 [Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet，然后使用 Azure 帐户登录：</span><span class="sxs-lookup"><span data-stu-id="c1c7b-120">Run the [Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet and then sign in with your Azure account:</span></span>

```powershell
Import-Module AzureRM.NetCore
Connect-AzureRmAccount
```

## <a name="use-the-windows-container-with-powershell"></a><span data-ttu-id="c1c7b-121">将 Windows 容器与 PowerShell 配合使用</span><span class="sxs-lookup"><span data-stu-id="c1c7b-121">Use the Windows container with PowerShell</span></span>

<span data-ttu-id="c1c7b-122">Windows 容器已预装 `AzureRM` 模块。</span><span class="sxs-lookup"><span data-stu-id="c1c7b-122">The Windows container has the `AzureRM` module pre-installed.</span></span> <span data-ttu-id="c1c7b-123">请运行 [Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet，然后使用 Azure 帐户登录：</span><span class="sxs-lookup"><span data-stu-id="c1c7b-123">Run the [Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet and then sign in with your Azure account:</span></span>

```powershell
Import-Module AzureRM
Connect-AzureRmAccount
```