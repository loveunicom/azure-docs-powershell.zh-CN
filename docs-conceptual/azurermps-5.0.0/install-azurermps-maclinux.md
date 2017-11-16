---
title: "在 macOS 和 Linux 上安装和配置 Azure PowerShell | Microsoft Docs"
description: "如何在 macOS 和 Linux 上安装和配置首次使用的 Azure PowerShell。"
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/06/2017
ms.openlocfilehash: 94b39c18acaca7a4b17b5207feed025442665acc
ms.sourcegitcommit: 358d260a867c6ee2e8700b91f776ba4f1b0e24a5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/11/2017
---
# <a name="install-and-configure-azure-powershell-on-macos-and-linux"></a><span data-ttu-id="b3e59-103">在 macOS 和 Linux 上安装和配置 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="b3e59-103">Install and configure Azure PowerShell on macOS and Linux</span></span>

<span data-ttu-id="b3e59-104">现在可在非 Windows 平台上安装 PowerShell 6（beta 版本）和 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="b3e59-104">It is now possible to install PowerShell 6 (beta) and Azure PowerShell on non-Windows platforms.</span></span>
<span data-ttu-id="b3e59-105">在 macOS 和 Linux 上安装 Azure PowerShell 的过程与在 Windows 上的安装过程相同，但是，必须首先安装 PowerShell 6（beta 版本）。</span><span class="sxs-lookup"><span data-stu-id="b3e59-105">The process of installing Azure PowerShell on macOS and Linux is not that different from Windows, however, you must first install PowerShell 6 (beta).</span></span>

> [!NOTE]

> <span data-ttu-id="b3e59-106">在此期间，PowerShell 6（beta 版本）和 Azure PowerShell for .NET Core 仍是 beta 版本。</span><span class="sxs-lookup"><span data-stu-id="b3e59-106">At this time, both PowerShell 6 (beta) and Azure PowerShell for .NET Core are still in beta.</span></span>
> <span data-ttu-id="b3e59-107">对这些产品的支持也是有限的。</span><span class="sxs-lookup"><span data-stu-id="b3e59-107">Support for these products is limited.</span></span> <span data-ttu-id="b3e59-108">如果你发现问题或 bug，请在 GitHub 中提出问题。</span><span class="sxs-lookup"><span data-stu-id="b3e59-108">If you have problems or discover bugs, please file Issues in GitHub.</span></span>
>
> * [<span data-ttu-id="b3e59-109">PowerShell 6（beta 版本）的问题</span><span class="sxs-lookup"><span data-stu-id="b3e59-109">Issues for PowerShell 6 (beta)</span></span>](https://github.com/PowerShell/PowerShell/issues)
> * [<span data-ttu-id="b3e59-110">Azure PowerShell 的问题</span><span class="sxs-lookup"><span data-stu-id="b3e59-110">Issues for Azure PowerShell</span></span>](https://github.com/azure/azure-docs-powershell/issues)

## <a name="step-1-install-powershell-6-beta"></a><span data-ttu-id="b3e59-111">步骤 1：安装 PowerShell 6（beta 版本）</span><span class="sxs-lookup"><span data-stu-id="b3e59-111">Step 1: Install PowerShell 6 (beta)</span></span>

<span data-ttu-id="b3e59-112">安装 PowerShell 6（beta 版本）的过程各不相同，具体取决于目标操作系统。</span><span class="sxs-lookup"><span data-stu-id="b3e59-112">The process of installing PowerShell 6 (beta) on varies depending on the target operating system.</span></span>
<span data-ttu-id="b3e59-113">虽然可在 Windows 上安装 PowerShell 6（beta 版本），但本文将重点介绍在 macOS 和 Linux 上进行安装。</span><span class="sxs-lookup"><span data-stu-id="b3e59-113">While it is possible to install PowerShell 6 (beta) on Windows, this article focuses on macOS and Linux.</span></span> <span data-ttu-id="b3e59-114">如果想要在 Windows 上使用 Azure PowerShell，请参阅适用于 Windows 的[安装](./install-azurerm-ps.md)文章。</span><span class="sxs-lookup"><span data-stu-id="b3e59-114">If you want to use Azure PowerShell on Windows, see the [install](./install-azurerm-ps.md) article for Windows.</span></span>

<span data-ttu-id="b3e59-115">若要在 Linux 或 macOS 上安装 PowerShell 6（beta 版本），需要：</span><span class="sxs-lookup"><span data-stu-id="b3e59-115">To install **PowerShell 6** (beta) on Linux or macOS, you need to:</span></span>

1. <span data-ttu-id="b3e59-116">从 [GitHub](https://github.com/powershell/powershell#get-powershell) 获取特定 OS 和版本的 PowerShell</span><span class="sxs-lookup"><span data-stu-id="b3e59-116">Get PowerShell for the specific OS and version, from [GitHub](https://github.com/powershell/powershell#get-powershell)</span></span>
2. <span data-ttu-id="b3e59-117">遵照安装说明操作</span><span class="sxs-lookup"><span data-stu-id="b3e59-117">Follow the installation instructions</span></span>
   - [<span data-ttu-id="b3e59-118">Linux</span><span class="sxs-lookup"><span data-stu-id="b3e59-118">Linux</span></span>](https://github.com/PowerShell/PowerShell/blob/master/docs/installation/linux.md)
   - [<span data-ttu-id="b3e59-119">macOS</span><span class="sxs-lookup"><span data-stu-id="b3e59-119">macOS</span></span>](https://github.com/PowerShell/PowerShell/blob/master/docs/installation/linux.md#macos-1012)

## <a name="step-2-install-azure-powershell-for-net-core"></a><span data-ttu-id="b3e59-120">步骤 2：安装 Azure PowerShell for .NET Core</span><span class="sxs-lookup"><span data-stu-id="b3e59-120">Step 2: Install Azure PowerShell for .NET Core</span></span>

<span data-ttu-id="b3e59-121">PowerShell 6（beta 版本）随已安装的 PowerShellGet 模块一起提供。</span><span class="sxs-lookup"><span data-stu-id="b3e59-121">PowerShell 6 (beta) comes with the PowerShellGet module already installed.</span></span> <span data-ttu-id="b3e59-122">这使得安装发布到 PowerShell 库的任何模块非常容易。</span><span class="sxs-lookup"><span data-stu-id="b3e59-122">This makes it easy to install any module that is published to the PowerShell Gallery.</span></span> <span data-ttu-id="b3e59-123">若要安装 Azure PowerShell，请打开一个新的 PowerShell 会话并运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="b3e59-123">To install Azure PowerShell, open a new PowerShell session and run the following command:</span></span>

```powershell
Install-Module AzureRM.NetCore
```

## <a name="step-3-load-the-azurermnetcore-module"></a><span data-ttu-id="b3e59-124">步骤 3：加载 AzureRM.Netcore 模块</span><span class="sxs-lookup"><span data-stu-id="b3e59-124">Step 3: Load the AzureRM.Netcore module</span></span>

<span data-ttu-id="b3e59-125">安装该模块后，需要将它加载到 PowerShell 会话中。</span><span class="sxs-lookup"><span data-stu-id="b3e59-125">Once the module is installed, you need to load the module into your PowerShell session.</span></span> <span data-ttu-id="b3e59-126">可以使用 `Import-Module` cmdlet 加载模块，如下所示：</span><span class="sxs-lookup"><span data-stu-id="b3e59-126">Modules are loaded using the `Import-Module` cmdlet, as follows:</span></span>

```powershell
Import-Module AzureRM.Netcore
```

<span data-ttu-id="b3e59-127">导入完成后，可以通过使用以下命令尝试登录到 Azure，测试新安装的模块：</span><span class="sxs-lookup"><span data-stu-id="b3e59-127">After the import completes, you can test your newly installed and module by attempting to sign into Azure using the following command:</span></span>

```powershell
Login-AzureRMAccount
```

<span data-ttu-id="b3e59-128">以上命令将提示你转到 `https://aka.ms/devicelogin` 并输入提供的代码。</span><span class="sxs-lookup"><span data-stu-id="b3e59-128">The above command should prompt you to go to `https://aka.ms/devicelogin` and enter the provided code.</span></span>

## <a name="available-cmdlets"></a><span data-ttu-id="b3e59-129">可用的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="b3e59-129">Available cmdlets</span></span>

<span data-ttu-id="b3e59-130">适用于 .NET 标准的 Azure PowerShell 模块仍处于开发之中。</span><span class="sxs-lookup"><span data-stu-id="b3e59-130">The Azure PowerShell modules for .NET Standard are still in development.</span></span> <span data-ttu-id="b3e59-131">这些模块不提供可用于模块 Windows 版本的完整 cmdlet 集。</span><span class="sxs-lookup"><span data-stu-id="b3e59-131">These modules do not provide the full set of cmdlets that are available for the Windows version of the modules.</span></span> <span data-ttu-id="b3e59-132">AzureRM.Netcore 模块中实现了以下功能：</span><span class="sxs-lookup"><span data-stu-id="b3e59-132">The following functions are implemented in AzureRM.Netcore modules:</span></span>

* <span data-ttu-id="b3e59-133">帐户管理</span><span class="sxs-lookup"><span data-stu-id="b3e59-133">Account management</span></span>
  - <span data-ttu-id="b3e59-134">通过 Microsoft Azure Active Directory 使用 Microsoft 帐户、组织帐户或服务主体登录</span><span class="sxs-lookup"><span data-stu-id="b3e59-134">Login with Microsoft account, Organizational account, or Service Principal through Microsoft Azure Active Directory</span></span>
  - <span data-ttu-id="b3e59-135">通过 Save-AzureRmContext 将凭据保存到磁盘，然后使用 Import-AzureRmContext 加载保存的凭据</span><span class="sxs-lookup"><span data-stu-id="b3e59-135">Save Credentials to disk with Save-AzureRmContext and load saved credentials using Import-AzureRmContext</span></span>
* <span data-ttu-id="b3e59-136">环境</span><span class="sxs-lookup"><span data-stu-id="b3e59-136">Environment</span></span>
  - <span data-ttu-id="b3e59-137">获取不同的现成 Microsoft Azure 环境</span><span class="sxs-lookup"><span data-stu-id="b3e59-137">Get the different out-of-box Microsoft Azure environments</span></span>
  - <span data-ttu-id="b3e59-138">添加/设置/删除自定义环境（如 Azure Stack 或 Windows Azure Pack 环境）</span><span class="sxs-lookup"><span data-stu-id="b3e59-138">Add/Set/Remove customized environments (like your Azure Stack or Windows Azure Pack environments)</span></span>
* <span data-ttu-id="b3e59-139">使用资源管理器和服务管理接口的 Azure 服务管理平面 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b3e59-139">Management plane cmdlets for Azure services using Resource Manager and Service Management interfaces.</span></span>
  - <span data-ttu-id="b3e59-140">虚拟机</span><span class="sxs-lookup"><span data-stu-id="b3e59-140">Virtual Machine</span></span>
  - <span data-ttu-id="b3e59-141">应用服务（网站）</span><span class="sxs-lookup"><span data-stu-id="b3e59-141">App Service (Websites)</span></span>
  - <span data-ttu-id="b3e59-142">SQL 数据库</span><span class="sxs-lookup"><span data-stu-id="b3e59-142">SQL Database</span></span>
  - <span data-ttu-id="b3e59-143">存储</span><span class="sxs-lookup"><span data-stu-id="b3e59-143">Storage</span></span>
  - <span data-ttu-id="b3e59-144">网络</span><span class="sxs-lookup"><span data-stu-id="b3e59-144">Network</span></span>

## <a name="next-steps"></a><span data-ttu-id="b3e59-145">后续步骤</span><span class="sxs-lookup"><span data-stu-id="b3e59-145">Next Steps</span></span>

<span data-ttu-id="b3e59-146">有关使用 Azure PowerShell 的详细信息，请参阅 [Azure PowerShell 入门](get-started-azureps.md)一文。</span><span class="sxs-lookup"><span data-stu-id="b3e59-146">For more information about using Azure PowerShell, see the [Get started with Azure PowerShell](get-started-azureps.md) article.</span></span>
