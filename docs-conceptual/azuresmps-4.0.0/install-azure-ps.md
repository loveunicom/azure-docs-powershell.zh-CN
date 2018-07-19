---
title: 安装和配置 Azure PowerShell 服务管理模块 | Microsoft Docs
description: 如何安装和配置首次使用的 Azure PowerShell。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/06/2017
ms.openlocfilehash: 21b61a2f91b4f6211fbeec8ba234782355b9a4b3
ms.sourcegitcommit: cb1fd248920d7efca67bd6c738a3b47206df7890
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/13/2018
ms.locfileid: "39024760"
---
# <a name="installing-the-azure-powershell-service-management-module"></a><span data-ttu-id="48def-103">安装 Azure PowerShell 服务管理模块</span><span class="sxs-lookup"><span data-stu-id="48def-103">Installing the Azure PowerShell Service Management module</span></span>

<span data-ttu-id="48def-104">从 [PowerShell 库](https://www.powershellgallery.com/)安装 Azure PowerShell 是首选的安装方法。</span><span class="sxs-lookup"><span data-stu-id="48def-104">Installing Azure PowerShell from the [PowerShell Gallery](https://www.powershellgallery.com/) is the preferred method of installation.</span></span>

## <a name="step-1-install-powershellget"></a><span data-ttu-id="48def-105">步骤 1：安装 PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="48def-105">Step 1: Install PowerShellGet</span></span>

<span data-ttu-id="48def-106">安装 PowerShell 库中的项需要 PowerShellGet 模块。</span><span class="sxs-lookup"><span data-stu-id="48def-106">Installing items from the PowerShell Gallery requires the PowerShellGet module.</span></span> <span data-ttu-id="48def-107">请确保使用适当版本的 PowerShellGet 并满足其他系统要求。</span><span class="sxs-lookup"><span data-stu-id="48def-107">Make sure you have the appropriate version of PowerShellGet and other system requirements.</span></span> <span data-ttu-id="48def-108">运行以下命令，确定是否已在系统上安装 PowerShellGet。</span><span class="sxs-lookup"><span data-stu-id="48def-108">Run the following command to see if you have PowerShellGet installed on your system.</span></span>

```powershell
Get-Module PowerShellGet -list | Select-Object Name,Version,Path
```

<span data-ttu-id="48def-109">应会看到类似于下面的信息：</span><span class="sxs-lookup"><span data-stu-id="48def-109">You should see something similar to the following output:</span></span>

```output
Name          Version Path
----          ------- ----
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

<span data-ttu-id="48def-110">如果没有安装 PowerShellGet，请参阅[如何获取 PowerShellGet](#how-to-get-powershellget)。</span><span class="sxs-lookup"><span data-stu-id="48def-110">If you do not have PowerShellGet installed, see the [How to get PowerShellGet](#how-to-get-powershellget).</span></span>

## <a name="step-2-install-azure-powershell"></a><span data-ttu-id="48def-111">步骤 2：安装 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="48def-111">Step 2: Install Azure PowerShell</span></span>

<span data-ttu-id="48def-112">在以管理员身份运行的 Windows PowerShell 控制台中运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="48def-112">Run the following command from the Windows PowerShell console running as Administrator:</span></span>

```powershell
Install-Module Azure
```

<span data-ttu-id="48def-113">Azure 模块是 Azure 资源管理器 cmdlet 的汇总模块。</span><span class="sxs-lookup"><span data-stu-id="48def-113">The Azure module is a rollup module for the Azure Resource Manager cmdlets.</span></span> <span data-ttu-id="48def-114">安装 AzureRM 模块时，将从 PowerShell 库下载并安装先前尚未安装的其他所有 Azure 模块。</span><span class="sxs-lookup"><span data-stu-id="48def-114">When you install the AzureRM module, any other Azure modules that have not previously been installed will be downloaded and installed from the PowerShell Gallery.</span></span>

<span data-ttu-id="48def-115">Azure 服务管理模块与 Azure PowerShell Resource Manager 模块共享依赖项。</span><span class="sxs-lookup"><span data-stu-id="48def-115">The Azure Service Management module shares dependencies with the Azure PowerShell Resource Manager modules.</span></span> <span data-ttu-id="48def-116">如果已安装 Azure PowerShell Resource Manager 模块，需在安装命令中添加 `-AllowClobber` 参数。</span><span class="sxs-lookup"><span data-stu-id="48def-116">If you have installed the Azure PowerShell Resource Manager modules, you will need to add the `-AllowClobber` parameter to the install command.</span></span> <span data-ttu-id="48def-117">这样，便可以更新现有的共享依赖项。</span><span class="sxs-lookup"><span data-stu-id="48def-117">This allows this existing shared dependencies to be updated.</span></span> <span data-ttu-id="48def-118">如果不提供此参数，模块安装会失败。</span><span class="sxs-lookup"><span data-stu-id="48def-118">Without this parameter, installation of the module fails.</span></span>

```powershell
Install-Module Azure -AllowClobber
```

<span data-ttu-id="48def-119">安装此模块后，可运行以下命令导入此模块：</span><span class="sxs-lookup"><span data-stu-id="48def-119">After you install this module, you can import the module by running the following command:</span></span>

```powershell
Import-Module Azure
```

## <a name="to-use-the-cmdlets"></a><span data-ttu-id="48def-120">使用 cmdlet</span><span class="sxs-lookup"><span data-stu-id="48def-120">To use the cmdlets</span></span>

<span data-ttu-id="48def-121">若要开始使用 Azure 服务管理 cmdlet，请先登录到 Azure 帐户。</span><span class="sxs-lookup"><span data-stu-id="48def-121">To start working with the Azure Service Management cmdlets, first log on to your Azure account.</span></span> <span data-ttu-id="48def-122">若要登录到帐户，请运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="48def-122">To log on to your account, run the following command:</span></span>

```powershell
Add-AzureAccount
```

<span data-ttu-id="48def-123">登录到 Azure 后，Azure PowerShell 将为给定的会话创建上下文。</span><span class="sxs-lookup"><span data-stu-id="48def-123">After logging into Azure, Azure PowerShell creates a context for the given session.</span></span> <span data-ttu-id="48def-124">该上下文包含用于该会话中的所有 cmdlet 的 Azure PowerShell 环境、帐户、租户和订阅。</span><span class="sxs-lookup"><span data-stu-id="48def-124">That context contains the Azure PowerShell environment, account, tenant, and subscription that will be used for all cmdlets within that session.</span></span> <span data-ttu-id="48def-125">现已准备就绪，可以使用下面的模块。</span><span class="sxs-lookup"><span data-stu-id="48def-125">Now you are ready to use the modules below.</span></span>

## <a name="azure-service-management-cmdlets"></a><span data-ttu-id="48def-126">Azure 服务管理 cmdlet</span><span class="sxs-lookup"><span data-stu-id="48def-126">Azure Service Management cmdlets</span></span>

<span data-ttu-id="48def-127">Azure PowerShell 模块经常更新。</span><span class="sxs-lookup"><span data-stu-id="48def-127">Azure PowerShell modules are updated frequently.</span></span> <span data-ttu-id="48def-128">如果发现 cmdlet 联机帮助包含模块中所不包含的 cmdlet 或参数，请下载并安装最新版本的模块。</span><span class="sxs-lookup"><span data-stu-id="48def-128">If you notice that the online cmdlet help includes cmdlets or parameters that are not in your module, download and install the latest version of the module.</span></span> <span data-ttu-id="48def-129">若要查找模块版本，请键入：`(Get-Module Azure).Version`。</span><span class="sxs-lookup"><span data-stu-id="48def-129">To find the version of your module, type: `(Get-Module Azure).Version`.</span></span>

<span data-ttu-id="48def-130">有关可帮助自动完成 Azure 中某些常见任务的示例脚本，请参阅 [Windows Azure 脚本中心](http://www.windowsazure.com/documentation/scripts/)。</span><span class="sxs-lookup"><span data-stu-id="48def-130">For sample scripts that can help you automate some of the common tasks in Azure, see the [Windows Azure Script Center](http://www.windowsazure.com/documentation/scripts/).</span></span>

<span data-ttu-id="48def-131">有关安装、学习、使用和自定义 Windows PowerShell 的一般信息，请参阅[使用 Windows PowerShell 编写脚本](http://go.microsoft.com/fwlink/p/?linkid=320210)。</span><span class="sxs-lookup"><span data-stu-id="48def-131">For general information about installing, learning, using, and customizing Windows PowerShell, see [Scripting with Windows PowerShell](http://go.microsoft.com/fwlink/p/?linkid=320210).</span></span>

### <a name="how-to-get-powershellget"></a><span data-ttu-id="48def-132">如何获取 PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="48def-132">How to get PowerShellGet</span></span>

|<span data-ttu-id="48def-133">OS 版本。</span><span class="sxs-lookup"><span data-stu-id="48def-133">OS Version</span></span>|<span data-ttu-id="48def-134">安装说明</span><span class="sxs-lookup"><span data-stu-id="48def-134">Install instructions</span></span>|
|---|---|
|<span data-ttu-id="48def-135">我使用的是 Windows 10 或 Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="48def-135">I have Windows 10 or Windows Server 2016</span></span>|<span data-ttu-id="48def-136">内置在 OS 随附的 Windows Management Framework (WMF) 5.0 中</span><span class="sxs-lookup"><span data-stu-id="48def-136">Built into Windows Management Framework (WMF) 5.0 included in the OS</span></span>|
|<span data-ttu-id="48def-137">我想要升级到 PowerShell 5</span><span class="sxs-lookup"><span data-stu-id="48def-137">I want to upgrade to PowerShell 5</span></span>|[<span data-ttu-id="48def-138">安装最新版本的 WMF</span><span class="sxs-lookup"><span data-stu-id="48def-138">Install the latest version of WMF</span></span>](https://www.microsoft.com/en-us/download/details.aspx?id=54616)|
|<span data-ttu-id="48def-139">我正在运行某个包含 PowerShell 3 或 PowerShell 4 的 Windows 版本</span><span class="sxs-lookup"><span data-stu-id="48def-139">I am running on a version of Windows with PowerShell 3 or PowerShell 4</span></span>|[<span data-ttu-id="48def-140">获取 PackageManagement 模块</span><span class="sxs-lookup"><span data-stu-id="48def-140">Get the PackageManagement modules</span></span>](http://go.microsoft.com/fwlink/?LinkID=746217)|

<div id="helpmechoose"/>
### <span data-ttu-id="48def-141">检查 Azure PowerShell 的版本</span><span class="sxs-lookup"><span data-stu-id="48def-141">Checking the version of Azure PowerShell</span></span>

<span data-ttu-id="48def-142">虽然我们建议尽早升级到最新版本，但仍然支持多个 Azure PowerShell 版本。</span><span class="sxs-lookup"><span data-stu-id="48def-142">Although we encourage you to upgrade to the latest version as early as possible, several versions of Azure PowerShell are support.</span></span> <span data-ttu-id="48def-143">若要确定安装的 Azure PowerShell 版本，请从命令行运行 `Get-Module AzureRM`。</span><span class="sxs-lookup"><span data-stu-id="48def-143">To determine the version of Azure PowerShell you have installed, run `Get-Module AzureRM` from your command line.</span></span>

```powershell
Get-Module AzureRM -list | Select-Object Name,Version,Path
```
