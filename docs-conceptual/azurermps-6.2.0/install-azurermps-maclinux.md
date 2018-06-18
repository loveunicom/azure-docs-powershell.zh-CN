---
title: 在 macOS 或 Linux 上安装 Azure PowerShell
description: 如何在 macOS 或 Linux 上安装 Azure PowerShell。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/06/2018
ms.openlocfilehash: 17912c155255b6fdfd3cfb9242163b67d405dc03
ms.sourcegitcommit: bcf80dfd7fbe17e82e7ad029802cfe8a2f02b15c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "35323163"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a><span data-ttu-id="bf413-103">在 macOS 或 Linux 上安装 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="bf413-103">Install Azure PowerShell on macOS or Linux</span></span>

<span data-ttu-id="bf413-104">对于非 Windows 平台，可以在 PowerShell Core v6 的基础上运行 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="bf413-104">For non-Windows platforms, it's possible to run Azure PowerShell on top of PowerShell Core v6.</span></span> <span data-ttu-id="bf413-105">本产品不是基于 .NET Framework for Windows 构建的标准 Azure PowerShell，它是针对 .NET Core 构建的并且可以在支持 .Net Core 运行时的任何平台上运行。</span><span class="sxs-lookup"><span data-stu-id="bf413-105">Rather than the standard Azure PowerShell built on .NET Framework for Windows, this product is built for .NET Core and can run on any platform which supports the .Net Core runtime.</span></span>

> [!NOTE]
> <span data-ttu-id="bf413-106">目前，PowerShell Core v6 和 Azure PowerShell for .NET Core 都还是 beta 版本。</span><span class="sxs-lookup"><span data-stu-id="bf413-106">At this time, both PowerShell Core v6 and Azure PowerShell for .NET Core are still in beta.</span></span>
> <span data-ttu-id="bf413-107">对这些产品的支持也是有限的。</span><span class="sxs-lookup"><span data-stu-id="bf413-107">Support for these products is limited.</span></span> <span data-ttu-id="bf413-108">如果你有需要询问的问题或发现了 bug，请在 GitHub 上提出问题。</span><span class="sxs-lookup"><span data-stu-id="bf413-108">If you have problems or discover bugs, please file an issue on GitHub.</span></span>
>
> * [<span data-ttu-id="bf413-109">PowerShell Core v6 的问题</span><span class="sxs-lookup"><span data-stu-id="bf413-109">Issues for PowerShell Core v6</span></span>](https://github.com/PowerShell/PowerShell/issues)
> * [<span data-ttu-id="bf413-110">Azure PowerShell 的问题</span><span class="sxs-lookup"><span data-stu-id="bf413-110">Issues for Azure PowerShell</span></span>](https://github.com/azure/azure-docs-powershell/issues)

## <a name="install-powershell-core-v6"></a><span data-ttu-id="bf413-111">安装 PowerShell Core v6</span><span class="sxs-lookup"><span data-stu-id="bf413-111">Install PowerShell Core v6</span></span>

<span data-ttu-id="bf413-112">在 Linux 或 macOS 上安装 PowerShell Core v6 的过程因 Linux 分发版和 OS 版本而异。</span><span class="sxs-lookup"><span data-stu-id="bf413-112">Installing PowerShell Core v6 on Linux or macOS varies depending on the Linux distribution and OS version.</span></span>
<span data-ttu-id="bf413-113">可在以下文章中找到详细说明：</span><span class="sxs-lookup"><span data-stu-id="bf413-113">Detailed instructions can be found in the following articles:</span></span>

- [<span data-ttu-id="bf413-114">在 macOS 上安装 PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="bf413-114">Install PowerShell Core on macOS</span></span>](/powershell/scripting/setup/installing-powershell-core-on-macos)
- [<span data-ttu-id="bf413-115">在 Linux 上安装 PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="bf413-115">Install PowerShell Core on Linux</span></span>](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-core"></a><span data-ttu-id="bf413-116">安装 Azure PowerShell for .NET Core</span><span class="sxs-lookup"><span data-stu-id="bf413-116">Install Azure PowerShell for .NET Core</span></span>

<span data-ttu-id="bf413-117">PowerShell Core v6 随已安装的 PowerShellGet 模块一起提供。</span><span class="sxs-lookup"><span data-stu-id="bf413-117">PowerShell Core v6 comes with the PowerShellGet module already installed.</span></span> <span data-ttu-id="bf413-118">这使得安装发布到 PowerShell 库的任何模块非常容易。</span><span class="sxs-lookup"><span data-stu-id="bf413-118">This makes it easy to install any module that is published to the PowerShell Gallery.</span></span> <span data-ttu-id="bf413-119">若要安装 Azure PowerShell，请打开一个新的 PowerShell 会话并运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="bf413-119">To install Azure PowerShell, open a new PowerShell session and run the following command:</span></span>

```powershell
Install-Module AzureRM.NetCore
```

## <a name="load-the-azurermnetcore-module"></a><span data-ttu-id="bf413-120">加载 AzureRM.Netcore 模块</span><span class="sxs-lookup"><span data-stu-id="bf413-120">Load the AzureRM.Netcore module</span></span>

<span data-ttu-id="bf413-121">安装该模块后，需要将它加载到 PowerShell 会话中。</span><span class="sxs-lookup"><span data-stu-id="bf413-121">Once the module is installed, you need to load the module into your PowerShell session.</span></span> <span data-ttu-id="bf413-122">可以使用 `Import-Module` cmdlet 加载模块，如下所示：</span><span class="sxs-lookup"><span data-stu-id="bf413-122">Modules are loaded using the `Import-Module` cmdlet, as follows:</span></span>

```powershell
Import-Module AzureRM.Netcore
Import-Module AzureRM.Profile.Netcore
```

<span data-ttu-id="bf413-123">导入完成后，可以通过使用以下命令尝试登录到 Azure，测试新安装的模块：</span><span class="sxs-lookup"><span data-stu-id="bf413-123">After the import completes, you can test your newly installed and module by attempting to sign into Azure using the following command:</span></span>

```powershell
Connect-AzureRmAccount
```

<span data-ttu-id="bf413-124">以上命令将提示你转到 `https://aka.ms/devicelogin` 并输入提供的代码。</span><span class="sxs-lookup"><span data-stu-id="bf413-124">The above command should prompt you to go to `https://aka.ms/devicelogin` and enter the provided code.</span></span>

## <a name="available-cmdlets"></a><span data-ttu-id="bf413-125">可用的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="bf413-125">Available cmdlets</span></span>

<span data-ttu-id="bf413-126">适用于 .NET 标准的 Azure PowerShell 模块仍处于开发之中。</span><span class="sxs-lookup"><span data-stu-id="bf413-126">The Azure PowerShell modules for .NET Standard are still in development.</span></span> <span data-ttu-id="bf413-127">这些模块不提供可用于模块 Windows 版本的完整 cmdlet 集。</span><span class="sxs-lookup"><span data-stu-id="bf413-127">These modules do not provide the full set of cmdlets that are available for the Windows version of the modules.</span></span> <span data-ttu-id="bf413-128">AzureRM.Netcore 模块中实现了以下功能：</span><span class="sxs-lookup"><span data-stu-id="bf413-128">The following functions are implemented in AzureRM.Netcore modules:</span></span>

* <span data-ttu-id="bf413-129">帐户管理</span><span class="sxs-lookup"><span data-stu-id="bf413-129">Account management</span></span>
  - <span data-ttu-id="bf413-130">通过 Microsoft Azure Active Directory 使用 Microsoft 帐户、组织帐户或服务主体登录</span><span class="sxs-lookup"><span data-stu-id="bf413-130">Login with Microsoft account, Organizational account, or Service Principal through Microsoft Azure Active Directory</span></span>
  - <span data-ttu-id="bf413-131">通过 Save-AzureRmContext 将凭据保存到磁盘，然后使用 Import-AzureRmContext 加载保存的凭据</span><span class="sxs-lookup"><span data-stu-id="bf413-131">Save Credentials to disk with Save-AzureRmContext and load saved credentials using Import-AzureRmContext</span></span>
* <span data-ttu-id="bf413-132">环境</span><span class="sxs-lookup"><span data-stu-id="bf413-132">Environment</span></span>
  - <span data-ttu-id="bf413-133">获取不同的现成 Microsoft Azure 环境</span><span class="sxs-lookup"><span data-stu-id="bf413-133">Get the different out-of-box Microsoft Azure environments</span></span>
  - <span data-ttu-id="bf413-134">添加/设置/删除自定义环境（如 Azure Stack 或 Windows Azure Pack 环境）</span><span class="sxs-lookup"><span data-stu-id="bf413-134">Add/Set/Remove customized environments (like your Azure Stack or Windows Azure Pack environments)</span></span>
* <span data-ttu-id="bf413-135">使用资源管理器和服务管理接口的 Azure 服务管理平面 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bf413-135">Management plane cmdlets for Azure services using Resource Manager and Service Management interfaces.</span></span>
  - <span data-ttu-id="bf413-136">虚拟机</span><span class="sxs-lookup"><span data-stu-id="bf413-136">Virtual Machine</span></span>
  - <span data-ttu-id="bf413-137">应用服务（网站）</span><span class="sxs-lookup"><span data-stu-id="bf413-137">App Service (Websites)</span></span>
  - <span data-ttu-id="bf413-138">SQL 数据库</span><span class="sxs-lookup"><span data-stu-id="bf413-138">SQL Database</span></span>
  - <span data-ttu-id="bf413-139">存储</span><span class="sxs-lookup"><span data-stu-id="bf413-139">Storage</span></span>
  - <span data-ttu-id="bf413-140">网络</span><span class="sxs-lookup"><span data-stu-id="bf413-140">Network</span></span>

## <a name="next-steps"></a><span data-ttu-id="bf413-141">后续步骤</span><span class="sxs-lookup"><span data-stu-id="bf413-141">Next Steps</span></span>

<span data-ttu-id="bf413-142">有关使用 Azure PowerShell 的详细信息，请参阅 [Azure PowerShell 入门](get-started-azureps.md)一文。</span><span class="sxs-lookup"><span data-stu-id="bf413-142">For more information about using Azure PowerShell, see the [Get started with Azure PowerShell](get-started-azureps.md) article.</span></span>
