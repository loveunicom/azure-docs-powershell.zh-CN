---
title: 在 macOS 或 Linux 上安装 Azure PowerShell
description: 如何在 macOS 或 Linux 上安装 Azure PowerShell。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/06/2018
ms.openlocfilehash: 6e7d447ea9672c174e3f1d103bc56c11a7f37192
ms.sourcegitcommit: f648ac92fafb16cc0e9ca6bc85d00fa327baf396
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/28/2018
ms.locfileid: "43019001"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a><span data-ttu-id="c0001-103">在 macOS 或 Linux 上安装 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="c0001-103">Install Azure PowerShell on macOS or Linux</span></span>

<span data-ttu-id="c0001-104">对于非 Windows 平台，可以在 PowerShell Core v6 中运行 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="c0001-104">For non-Windows platforms, it's possible to run Azure PowerShell in PowerShell Core v6.</span></span> <span data-ttu-id="c0001-105">此版 PowerShell 可以在支持 .NET Core 的任何平台上使用。</span><span class="sxs-lookup"><span data-stu-id="c0001-105">This version of PowerShell is built for use on any platform that supports .NET Core.</span></span> <span data-ttu-id="c0001-106">可以使用一个特殊的与这些平台兼容的 .NET Core 版 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="c0001-106">To work with these platforms, there's a special .NET Core version of Azure PowerShell available.</span></span>

> [!NOTE]
> <span data-ttu-id="c0001-107">目前，PowerShell Core v6 和 Azure PowerShell for .NET Core 都还是 beta 版本。</span><span class="sxs-lookup"><span data-stu-id="c0001-107">At this time, both PowerShell Core v6 and Azure PowerShell for .NET Core are still in beta.</span></span>
> <span data-ttu-id="c0001-108">对这些产品的支持也是有限的。</span><span class="sxs-lookup"><span data-stu-id="c0001-108">Support for these products is limited.</span></span> <span data-ttu-id="c0001-109">如果你有需要询问的问题或发现了 bug，请在 GitHub 上提出问题。</span><span class="sxs-lookup"><span data-stu-id="c0001-109">If you have problems or discover bugs, please file an issue on GitHub.</span></span>
>
> * [<span data-ttu-id="c0001-110">PowerShell Core v6 的问题</span><span class="sxs-lookup"><span data-stu-id="c0001-110">Issues for PowerShell Core v6</span></span>](https://github.com/PowerShell/PowerShell/issues)
> * [<span data-ttu-id="c0001-111">Azure PowerShell 的问题</span><span class="sxs-lookup"><span data-stu-id="c0001-111">Issues for Azure PowerShell</span></span>](https://github.com/azure/azure-docs-powershell/issues)

## <a name="install-powershell-core"></a><span data-ttu-id="c0001-112">安装 PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="c0001-112">Install PowerShell Core</span></span>

<span data-ttu-id="c0001-113">就 macOS 和大多数 Linux 发行版来说，PowerShell Core 的安装说明是不同的。</span><span class="sxs-lookup"><span data-stu-id="c0001-113">The installation instructions for PowerShell Core are different for macOS and most Linux distributions.</span></span>
<span data-ttu-id="c0001-114">可在以下文章中找到详细说明：</span><span class="sxs-lookup"><span data-stu-id="c0001-114">Detailed instructions can be found in the following articles:</span></span>

* [<span data-ttu-id="c0001-115">在 macOS 上安装 PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="c0001-115">Install PowerShell Core on macOS</span></span>](/powershell/scripting/setup/installing-powershell-core-on-macos)
* [<span data-ttu-id="c0001-116">在 Linux 上安装 PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="c0001-116">Install PowerShell Core on Linux</span></span>](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-core"></a><span data-ttu-id="c0001-117">安装 Azure PowerShell for .NET Core</span><span class="sxs-lookup"><span data-stu-id="c0001-117">Install Azure PowerShell for .NET Core</span></span>

<span data-ttu-id="c0001-118">PowerShell Core 附带已安装的 PowerShellGet 模块。</span><span class="sxs-lookup"><span data-stu-id="c0001-118">PowerShell Core comes with the PowerShellGet module already installed.</span></span> <span data-ttu-id="c0001-119">在 PowerShell 中安装模块需要提升的特权，因此需以超级用户身份启动会话。</span><span class="sxs-lookup"><span data-stu-id="c0001-119">Installation of modules in PowerShell requires elevated privileges, so you'll need to start your session as superuser:</span></span>

```bash
sudo pwsh
```

<span data-ttu-id="c0001-120">若要安装 Azure PowerShell，请运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="c0001-120">To install Azure PowerShell, run the following command:</span></span>

```powershell
Install-Module AzureRM.NetCore
```

> [!IMPORTANT]
> <span data-ttu-id="c0001-121">在其他文章中详细介绍的 `AzureRM` 模块不是针对 .NET Core 生成的，因此不兼容 PowerShell Core。</span><span class="sxs-lookup"><span data-stu-id="c0001-121">The `AzureRM` module detailed in other articles is not built for .NET Core and will not work with PowerShell Core.</span></span> <span data-ttu-id="c0001-122">`AzureRM` 和 `AzureRM.NetCore` 使用同一 cmdlet 名称，因此唯一区别是汇总模块的名称，以及它们所基于的 .NET 版本。</span><span class="sxs-lookup"><span data-stu-id="c0001-122">Both `AzureRM` and `AzureRM.NetCore` use the same cmdlet names, so the only difference is the name of the rollup module and which .NET version they are built against.</span></span>

<span data-ttu-id="c0001-123">默认情况下，PowerShell 库未配置为 PowerShellGet 的受信任存储库。</span><span class="sxs-lookup"><span data-stu-id="c0001-123">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="c0001-124">首次使用 PSGallery 时会看到以下提示：</span><span class="sxs-lookup"><span data-stu-id="c0001-124">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="c0001-125">请回答 `Yes` 或 `Yes to All` 继续安装。</span><span class="sxs-lookup"><span data-stu-id="c0001-125">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

## <a name="sign-in"></a><span data-ttu-id="c0001-126">登录</span><span class="sxs-lookup"><span data-stu-id="c0001-126">Sign in</span></span>

<span data-ttu-id="c0001-127">若要开始使用 Azure PowerShell，需使用 [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet 将 `AzureRM.Netcore` 加载到 PowerShell 会话中，然后使用 Azure 凭据登录。</span><span class="sxs-lookup"><span data-stu-id="c0001-127">To start working with Azure PowerShell, you need to load `AzureRM.Netcore` into your PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span> <span data-ttu-id="c0001-128">导入模块不需要提升的权限。</span><span class="sxs-lookup"><span data-stu-id="c0001-128">Importing a module does __not__ require elevated privileges.</span></span>

```powershell
# Import the module into the PowerShell session
Import-Module AzureRM.Netcore
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="c0001-129">需对每个启动的新 PowerShell 会话重复这些步骤。</span><span class="sxs-lookup"><span data-stu-id="c0001-129">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="c0001-130">自动导入 `AzureRM` 模块要求设置 PowerShell 配置文件，详见[关于配置文件](/powershell/module/microsoft.powershell.core/about/about_profiles)。</span><span class="sxs-lookup"><span data-stu-id="c0001-130">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="c0001-131">在 macOS 和 Linux 上，应通过 `$Profile` 环境变量来使用配置文件。</span><span class="sxs-lookup"><span data-stu-id="c0001-131">On macOS and Linux, you should work with your profile through the `$Profile` environment variable.</span></span> <span data-ttu-id="c0001-132">若要了解如何跨会话保持 Azure 登录状态，请参阅[跨 PowerShell 会话保持用户凭据](context-persistence.md)。</span><span class="sxs-lookup"><span data-stu-id="c0001-132">To learn how to persist your Azure sign in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="available-cmdlets"></a><span data-ttu-id="c0001-133">可用的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="c0001-133">Available cmdlets</span></span>

<span data-ttu-id="c0001-134">适用于 .NET Core 的 Azure PowerShell 模块仍处于开发之中。</span><span class="sxs-lookup"><span data-stu-id="c0001-134">The Azure PowerShell modules for .NET Core are still in development.</span></span> <span data-ttu-id="c0001-135">这些模块不提供可用于模块 Windows 版本的完整 cmdlet 集。</span><span class="sxs-lookup"><span data-stu-id="c0001-135">These modules do not provide the full set of cmdlets that are available for the Windows version of the modules.</span></span> <span data-ttu-id="c0001-136">AzureRM.Netcore 模块中实现了以下功能：</span><span class="sxs-lookup"><span data-stu-id="c0001-136">The following functions are implemented in AzureRM.Netcore modules:</span></span>

* <span data-ttu-id="c0001-137">帐户管理</span><span class="sxs-lookup"><span data-stu-id="c0001-137">Account management</span></span>
  * <span data-ttu-id="c0001-138">通过 Microsoft Azure Active Directory 使用 Microsoft 帐户、组织帐户或服务主体登录</span><span class="sxs-lookup"><span data-stu-id="c0001-138">Sign in with Microsoft account, Organizational account, or Service Principal through Microsoft Azure Active Directory</span></span>
  * <span data-ttu-id="c0001-139">通过 Save-AzureRmContext 将凭据保存到磁盘，然后使用 Import-AzureRmContext 加载保存的凭据</span><span class="sxs-lookup"><span data-stu-id="c0001-139">Save Credentials to disk with Save-AzureRmContext and load saved credentials using Import-AzureRmContext</span></span>
* <span data-ttu-id="c0001-140">环境</span><span class="sxs-lookup"><span data-stu-id="c0001-140">Environment</span></span>
  * <span data-ttu-id="c0001-141">获取不同的现成 Microsoft Azure 环境</span><span class="sxs-lookup"><span data-stu-id="c0001-141">Get the different out-of-box Microsoft Azure environments</span></span>
  * <span data-ttu-id="c0001-142">添加/设置/删除自定义环境（如 Azure Stack 或 Windows Azure Pack 环境）</span><span class="sxs-lookup"><span data-stu-id="c0001-142">Add/Set/Remove customized environments (like your Azure Stack or Windows Azure Pack environments)</span></span>
* <span data-ttu-id="c0001-143">使用资源管理器和服务管理接口的 Azure 服务管理平面 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c0001-143">Management plane cmdlets for Azure services using Resource Manager and Service Management interfaces.</span></span>
  * <span data-ttu-id="c0001-144">虚拟机</span><span class="sxs-lookup"><span data-stu-id="c0001-144">Virtual Machine</span></span>
  * <span data-ttu-id="c0001-145">应用服务（网站）</span><span class="sxs-lookup"><span data-stu-id="c0001-145">App Service (Websites)</span></span>
  * <span data-ttu-id="c0001-146">SQL 数据库</span><span class="sxs-lookup"><span data-stu-id="c0001-146">SQL Database</span></span>
  * <span data-ttu-id="c0001-147">存储</span><span class="sxs-lookup"><span data-stu-id="c0001-147">Storage</span></span>
  * <span data-ttu-id="c0001-148">网络</span><span class="sxs-lookup"><span data-stu-id="c0001-148">Network</span></span>

## <a name="next-steps"></a><span data-ttu-id="c0001-149">后续步骤</span><span class="sxs-lookup"><span data-stu-id="c0001-149">Next Steps</span></span>

<span data-ttu-id="c0001-150">有关使用 Azure PowerShell 的详细信息，请参阅 [Azure PowerShell 入门](get-started-azureps.md)一文。</span><span class="sxs-lookup"><span data-stu-id="c0001-150">For more information about using Azure PowerShell, see the [Get started with Azure PowerShell](get-started-azureps.md) article.</span></span>
