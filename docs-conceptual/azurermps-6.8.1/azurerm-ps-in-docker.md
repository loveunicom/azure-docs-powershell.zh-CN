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
ms.sourcegitcommit: bc88e64c494337821274d6a66c1edad656c119c5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/20/2018
ms.locfileid: "46304006"
---
# <a name="run-azure-powershell-in-a-docker-container"></a><span data-ttu-id="3a866-103">在 Docker 容器中运行 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="3a866-103">Run Azure PowerShell in a Docker container</span></span>

<span data-ttu-id="3a866-104">Microsoft 发布了已预装 Azure PowerShell 的 Docker 映像。</span><span class="sxs-lookup"><span data-stu-id="3a866-104">Microsoft publishes Docker images with Azure PowerShell pre-installed.</span></span> <span data-ttu-id="3a866-105">使用这些映像可以体验 Azure PowerShell，或者在隔离的环境中运行它。</span><span class="sxs-lookup"><span data-stu-id="3a866-105">These images allow for experimenting with Azure PowerShell or running it in an isolated environment.</span></span> <span data-ttu-id="3a866-106">有些映像运行 PowerShell Core 和 PowerShell 5。</span><span class="sxs-lookup"><span data-stu-id="3a866-106">There are images running both PowerShell Core and PowerShell 5.</span></span> 

| <span data-ttu-id="3a866-107">环境</span><span class="sxs-lookup"><span data-stu-id="3a866-107">Environment</span></span> | <span data-ttu-id="3a866-108">Docker 映像</span><span class="sxs-lookup"><span data-stu-id="3a866-108">Docker image</span></span> |
|-------------|--------------|
| <span data-ttu-id="3a866-109">Windows 上的 PowerShell</span><span class="sxs-lookup"><span data-stu-id="3a866-109">PowerShell on Windows</span></span> | [<span data-ttu-id="3a866-110">azuresdk/azure-powershell</span><span class="sxs-lookup"><span data-stu-id="3a866-110">azuresdk/azure-powershell</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell/) |
| <span data-ttu-id="3a866-111">Windows 上的 PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="3a866-111">PowerShell Core on Windows</span></span> | [<span data-ttu-id="3a866-112">azuresdk/azure-powershell-core:nanoserver</span><span class="sxs-lookup"><span data-stu-id="3a866-112">azuresdk/azure-powershell-core:nanoserver</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |
| <span data-ttu-id="3a866-113">Linux 上的 PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="3a866-113">PowerShell Core on Linux</span></span> | [<span data-ttu-id="3a866-114">azuresdk/azure-powershell-core:latest</span><span class="sxs-lookup"><span data-stu-id="3a866-114">azuresdk/azure-powershell-core:latest</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |

<span data-ttu-id="3a866-115">若要运行这些容器中的任何一个，请使用 `docker run -it $ImageName` 获取交互式终端。</span><span class="sxs-lookup"><span data-stu-id="3a866-115">To run any of these containers, use `docker run -it $ImageName` to get an interactive terminal.</span></span> <span data-ttu-id="3a866-116">例如，若要运行包含 PowerShell Core 的 Linux 容器：</span><span class="sxs-lookup"><span data-stu-id="3a866-116">For example, to run a Linux container with PowerShell Core:</span></span>

```powershell
docker run -it azuresdk/azure-powershell-core:latest
```

> [!NOTE]
> <span data-ttu-id="3a866-117">若要在 Docker 中运行 Windows 容器，主机 OS 必须是 Windows 并且 Docker 必须设置为运行 Windows 容器。</span><span class="sxs-lookup"><span data-stu-id="3a866-117">To run a Windows container in Docker, your host OS must be Windows and Docker must be set to run Windows containers.</span></span> <span data-ttu-id="3a866-118">若要了解如何在 Docker 中在 Windows 与 Linux 环境之间进行切换，请参阅 Docker 文档[在 Windows 与 Linux 容器之间进行切换](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers)。</span><span class="sxs-lookup"><span data-stu-id="3a866-118">To learn about switching between Windows and Linux environments in Docker, see the Docker documentation [Switch between Windows and Linux containers](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers).</span></span>

## <a name="use-a-powershell-core-container"></a><span data-ttu-id="3a866-119">使用 PowerShell Core 容器</span><span class="sxs-lookup"><span data-stu-id="3a866-119">Use a PowerShell Core container</span></span>

<span data-ttu-id="3a866-120">PowerShell Core 容器已预装 PowerShell Core v6 和 `AzureRM.NetCore` 模块。</span><span class="sxs-lookup"><span data-stu-id="3a866-120">The PowerShell Core containers come with PowerShell Core v6 and the `AzureRM.NetCore` module pre-installed.</span></span> <span data-ttu-id="3a866-121">请运行 [Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet，然后使用 Azure 帐户登录：</span><span class="sxs-lookup"><span data-stu-id="3a866-121">Run the [Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet and then sign in with your Azure account:</span></span>

```powershell
Import-Module AzureRM.NetCore
Connect-AzureRmAccount
```

## <a name="use-the-windows-container-with-powershell"></a><span data-ttu-id="3a866-122">将 Windows 容器与 PowerShell 配合使用</span><span class="sxs-lookup"><span data-stu-id="3a866-122">Use the Windows container with PowerShell</span></span>

<span data-ttu-id="3a866-123">Windows 容器已预装 `AzureRM` 模块。</span><span class="sxs-lookup"><span data-stu-id="3a866-123">The Windows container has the `AzureRM` module pre-installed.</span></span> <span data-ttu-id="3a866-124">请运行 [Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet，然后使用 Azure 帐户登录：</span><span class="sxs-lookup"><span data-stu-id="3a866-124">Run the [Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet and then sign in with your Azure account:</span></span>

```powershell
Import-Module AzureRM
Connect-AzureRmAccount
```
