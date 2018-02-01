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
ms.date: 01/12/2018
ms.openlocfilehash: 64a86dfd4af7f3f0a91501e9a096ff190f7100cb
ms.sourcegitcommit: 72f56597f0329d35779a3ea4ccea6293f0fd2502
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/01/2018
---
# <a name="install-and-configure-azure-powershell-on-macos-and-linux"></a><span data-ttu-id="58732-103">在 macOS 和 Linux 上安装和配置 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="58732-103">Install and configure Azure PowerShell on macOS and Linux</span></span>

<span data-ttu-id="58732-104">现在，非 Windows 平台上也可以安装 PowerShell Core v6 和 Azure PowerShell 了。</span><span class="sxs-lookup"><span data-stu-id="58732-104">It is now possible to install PowerShell Core v6 and Azure PowerShell on non-Windows platforms.</span></span>
<span data-ttu-id="58732-105">在 macOS 和 Linux 上安装 Azure PowerShell 的过程与在 Windows 上的安装过程相同，但是，必须首先安装 PowerShell Core v6。</span><span class="sxs-lookup"><span data-stu-id="58732-105">The process of installing Azure PowerShell on macOS and Linux is not that different from Windows, however, you must first install PowerShell Core v6.</span></span>

> [!NOTE]

> <span data-ttu-id="58732-106">目前，PowerShell Core v6 和 Azure PowerShell for .NET Core 都还是 beta 版本。</span><span class="sxs-lookup"><span data-stu-id="58732-106">At this time, both PowerShell Core v6 and Azure PowerShell for .NET Core are still in beta.</span></span>
> <span data-ttu-id="58732-107">对这些产品的支持也是有限的。</span><span class="sxs-lookup"><span data-stu-id="58732-107">Support for these products is limited.</span></span> <span data-ttu-id="58732-108">如果你发现问题或 bug，请在 GitHub 中提出问题。</span><span class="sxs-lookup"><span data-stu-id="58732-108">If you have problems or discover bugs, please file Issues in GitHub.</span></span>
>
> * [<span data-ttu-id="58732-109">PowerShell Core v6 的问题</span><span class="sxs-lookup"><span data-stu-id="58732-109">Issues for PowerShell Core v6</span></span>](https://github.com/PowerShell/PowerShell/issues)
> * [<span data-ttu-id="58732-110">Azure PowerShell 的问题</span><span class="sxs-lookup"><span data-stu-id="58732-110">Issues for Azure PowerShell</span></span>](https://github.com/azure/azure-docs-powershell/issues)

## <a name="step-1-install-powershell-core-v6"></a><span data-ttu-id="58732-111">步骤 1：安装 PowerShell Core v6</span><span class="sxs-lookup"><span data-stu-id="58732-111">Step 1: Install PowerShell Core v6</span></span>

<span data-ttu-id="58732-112">PowerShell Core v6 的安装过程因目标操作系统而异。</span><span class="sxs-lookup"><span data-stu-id="58732-112">The process of installing PowerShell Core v6 on varies depending on the target operating system.</span></span>
<span data-ttu-id="58732-113">虽然可在 Windows 上安装 PowerShell Core v6，但本文将重点介绍在 macOS 和 Linux 上进行安装。</span><span class="sxs-lookup"><span data-stu-id="58732-113">While it is possible to install PowerShell Core v6 on Windows, this article focuses on macOS and Linux.</span></span> <span data-ttu-id="58732-114">如果想要在 Windows 上使用 Azure PowerShell，请参阅适用于 Windows 的[安装](./install-azurerm-ps.md)文章。</span><span class="sxs-lookup"><span data-stu-id="58732-114">If you want to use Azure PowerShell on Windows, see the [install](./install-azurerm-ps.md) article for Windows.</span></span>

<span data-ttu-id="58732-115">在 Linux 或 macOS 上安装 **PowerShell Core v6** 的过程因 Linux 分发版和 OS 版本而异。</span><span class="sxs-lookup"><span data-stu-id="58732-115">Installing **PowerShell Core v6** on Linux or macOS varies depending on the Linux distribution and OS version.</span></span>
<span data-ttu-id="58732-116">可以在以下文章中找到详细说明：</span><span class="sxs-lookup"><span data-stu-id="58732-116">Detailed instructions can be found in the following article:</span></span>

- [<span data-ttu-id="58732-117">在 macOS 和 Linux 上安装 PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="58732-117">Installing PowerShell Core on macOS and Linux</span></span>](/powershell/scripting/setup/installing-powershell-core-on-macos-and-linux)

## <a name="step-2-install-azure-powershell-for-net-core"></a><span data-ttu-id="58732-118">步骤 2：安装 Azure PowerShell for .NET Core</span><span class="sxs-lookup"><span data-stu-id="58732-118">Step 2: Install Azure PowerShell for .NET Core</span></span>

<span data-ttu-id="58732-119">PowerShell Core v6 随已安装的 PowerShellGet 模块一起提供。</span><span class="sxs-lookup"><span data-stu-id="58732-119">PowerShell Core v6 comes with the PowerShellGet module already installed.</span></span> <span data-ttu-id="58732-120">这使得安装发布到 PowerShell 库的任何模块非常容易。</span><span class="sxs-lookup"><span data-stu-id="58732-120">This makes it easy to install any module that is published to the PowerShell Gallery.</span></span> <span data-ttu-id="58732-121">若要安装 Azure PowerShell，请打开一个新的 PowerShell 会话并运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="58732-121">To install Azure PowerShell, open a new PowerShell session and run the following command:</span></span>

```powershell
Install-Module AzureRM.NetCore
```

## <a name="step-3-load-the-azurermnetcore-module"></a><span data-ttu-id="58732-122">步骤 3：加载 AzureRM.Netcore 模块</span><span class="sxs-lookup"><span data-stu-id="58732-122">Step 3: Load the AzureRM.Netcore module</span></span>

<span data-ttu-id="58732-123">安装该模块后，需要将它加载到 PowerShell 会话中。</span><span class="sxs-lookup"><span data-stu-id="58732-123">Once the module is installed, you need to load the module into your PowerShell session.</span></span> <span data-ttu-id="58732-124">可以使用 `Import-Module` cmdlet 加载模块，如下所示：</span><span class="sxs-lookup"><span data-stu-id="58732-124">Modules are loaded using the `Import-Module` cmdlet, as follows:</span></span>

```powershell
Import-Module AzureRM.Netcore
Import-Module AzureRM.Profile.Netcore
```

<span data-ttu-id="58732-125">导入完成后，可以通过使用以下命令尝试登录到 Azure，测试新安装的模块：</span><span class="sxs-lookup"><span data-stu-id="58732-125">After the import completes, you can test your newly installed and module by attempting to sign into Azure using the following command:</span></span>

```powershell
Login-AzureRMAccount
```

<span data-ttu-id="58732-126">以上命令将提示你转到 `https://aka.ms/devicelogin` 并输入提供的代码。</span><span class="sxs-lookup"><span data-stu-id="58732-126">The above command should prompt you to go to `https://aka.ms/devicelogin` and enter the provided code.</span></span>

## <a name="available-cmdlets"></a><span data-ttu-id="58732-127">可用的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="58732-127">Available cmdlets</span></span>

<span data-ttu-id="58732-128">适用于 .NET 标准的 Azure PowerShell 模块仍处于开发之中。</span><span class="sxs-lookup"><span data-stu-id="58732-128">The Azure PowerShell modules for .NET Standard are still in development.</span></span> <span data-ttu-id="58732-129">这些模块不提供可用于模块 Windows 版本的完整 cmdlet 集。</span><span class="sxs-lookup"><span data-stu-id="58732-129">These modules do not provide the full set of cmdlets that are available for the Windows version of the modules.</span></span> <span data-ttu-id="58732-130">AzureRM.Netcore 模块中实现了以下功能：</span><span class="sxs-lookup"><span data-stu-id="58732-130">The following functions are implemented in AzureRM.Netcore modules:</span></span>

* <span data-ttu-id="58732-131">帐户管理</span><span class="sxs-lookup"><span data-stu-id="58732-131">Account management</span></span>
  - <span data-ttu-id="58732-132">通过 Microsoft Azure Active Directory 使用 Microsoft 帐户、组织帐户或服务主体登录</span><span class="sxs-lookup"><span data-stu-id="58732-132">Login with Microsoft account, Organizational account, or Service Principal through Microsoft Azure Active Directory</span></span>
  - <span data-ttu-id="58732-133">通过 Save-AzureRmContext 将凭据保存到磁盘，然后使用 Import-AzureRmContext 加载保存的凭据</span><span class="sxs-lookup"><span data-stu-id="58732-133">Save Credentials to disk with Save-AzureRmContext and load saved credentials using Import-AzureRmContext</span></span>
* <span data-ttu-id="58732-134">环境</span><span class="sxs-lookup"><span data-stu-id="58732-134">Environment</span></span>
  - <span data-ttu-id="58732-135">获取不同的现成 Microsoft Azure 环境</span><span class="sxs-lookup"><span data-stu-id="58732-135">Get the different out-of-box Microsoft Azure environments</span></span>
  - <span data-ttu-id="58732-136">添加/设置/删除自定义环境（如 Azure Stack 或 Windows Azure Pack 环境）</span><span class="sxs-lookup"><span data-stu-id="58732-136">Add/Set/Remove customized environments (like your Azure Stack or Windows Azure Pack environments)</span></span>
* <span data-ttu-id="58732-137">使用资源管理器和服务管理接口的 Azure 服务管理平面 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="58732-137">Management plane cmdlets for Azure services using Resource Manager and Service Management interfaces.</span></span>
  - <span data-ttu-id="58732-138">虚拟机</span><span class="sxs-lookup"><span data-stu-id="58732-138">Virtual Machine</span></span>
  - <span data-ttu-id="58732-139">应用服务（网站）</span><span class="sxs-lookup"><span data-stu-id="58732-139">App Service (Websites)</span></span>
  - <span data-ttu-id="58732-140">SQL 数据库</span><span class="sxs-lookup"><span data-stu-id="58732-140">SQL Database</span></span>
  - <span data-ttu-id="58732-141">存储</span><span class="sxs-lookup"><span data-stu-id="58732-141">Storage</span></span>
  - <span data-ttu-id="58732-142">网络</span><span class="sxs-lookup"><span data-stu-id="58732-142">Network</span></span>

## <a name="next-steps"></a><span data-ttu-id="58732-143">后续步骤</span><span class="sxs-lookup"><span data-stu-id="58732-143">Next Steps</span></span>

<span data-ttu-id="58732-144">有关使用 Azure PowerShell 的详细信息，请参阅 [Azure PowerShell 入门](get-started-azureps.md)一文。</span><span class="sxs-lookup"><span data-stu-id="58732-144">For more information about using Azure PowerShell, see the [Get started with Azure PowerShell](get-started-azureps.md) article.</span></span>
