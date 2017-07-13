---
title: "<span data-ttu-id=\"e5696-101\">安装和配置 Azure PowerShell 服务管理模块 | Microsoft Docs</span><span class=\"sxs-lookup\"><span data-stu-id=\"e5696-101\">Install and configure the Azure PowerShell Service Management module | Microsoft Docs</span></span>"
description: "<span data-ttu-id=\"e5696-102\">如何安装和配置首次使用的 Azure PowerShell。</span><span class=\"sxs-lookup\"><span data-stu-id=\"e5696-102\">How to install and configure Azure PowerShell for first time use.</span></span>"
services: azure
author: sdwheeler
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/06/2017
ms.openlocfilehash: c51c727c1cb022eca59f819c7f24d8e058c677da
ms.sourcegitcommit: 226527be7cb647acfe2ea9ab151185053ab3c6db
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/29/2017
---
# <span data-ttu-id="e5696-103">安装 Azure PowerShell 服务管理模块</span><span class="sxs-lookup"><span data-stu-id="e5696-103">Installing the Azure PowerShell Service Management module</span></span>
<a id="installing-the-azure-powershell-service-management-module" class="xliff"></a>

<span data-ttu-id="e5696-104">从 [PowerShell 库](https://www.powershellgallery.com/)安装 Azure PowerShell 是首选的安装方法。</span><span class="sxs-lookup"><span data-stu-id="e5696-104">Installing Azure PowerShell from the [PowerShell Gallery](https://www.powershellgallery.com/) is the preferred method of installation.</span></span>

## <span data-ttu-id="e5696-105">步骤 1：安装 PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="e5696-105">Step 1: Install PowerShellGet</span></span>
<a id="step-1-install-powershellget" class="xliff"></a>

<span data-ttu-id="e5696-106">安装 PowerShell 库中的项需要 PowerShellGet 模块。</span><span class="sxs-lookup"><span data-stu-id="e5696-106">Installing items from the PowerShell Gallery requires the PowerShellGet module.</span></span> <span data-ttu-id="e5696-107">请确保使用适当版本的 PowerShellGet 并满足其他系统要求。</span><span class="sxs-lookup"><span data-stu-id="e5696-107">Make sure you have the appropriate version of PowerShellGet and other system requirements.</span></span> <span data-ttu-id="e5696-108">运行以下命令，确定是否已在系统上安装 PowerShellGet。</span><span class="sxs-lookup"><span data-stu-id="e5696-108">Run the following command to see if you have PowerShellGet installed on your system.</span></span>

```powershell
Get-Module PowerShellGet -list | Select-Object Name,Version,Path
```

<span data-ttu-id="e5696-109">你应会看到类似于下面的信息：</span><span class="sxs-lookup"><span data-stu-id="e5696-109">You should see something similar to the following output:</span></span>

```
Name          Version Path
----          ------- ----
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

<span data-ttu-id="e5696-110">如果没有安装 PowerShellGet，请参阅[如何获取 PowerShellGet](install-azurerm-ps.md#how-to-get-powershellget)。</span><span class="sxs-lookup"><span data-stu-id="e5696-110">If you do not have PowerShellGet installed, see the [How to get PowerShellGet](install-azurerm-ps.md#how-to-get-powershellget).</span></span>

## <span data-ttu-id="e5696-111">步骤 2：安装 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="e5696-111">Step 2: Install Azure PowerShell</span></span>
<a id="step-2-install-azure-powershell" class="xliff"></a>

<span data-ttu-id="e5696-112">在以管理员身份运行的 Windows PowerShell 控制台中运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="e5696-112">Run the following command from the Windows PowerShell console running as Administrator:</span></span>

```powershell
Install-Module Azure
```

<span data-ttu-id="e5696-113">Azure 模块是 Azure Resource Manager cmdlet 的汇总模块。</span><span class="sxs-lookup"><span data-stu-id="e5696-113">The Azure module is a rollup module for the Azure Resource Manager cmdlets.</span></span> <span data-ttu-id="e5696-114">安装 AzureRM 模块时，将从 PowerShell 库下载并安装先前尚未安装的其他所有 Azure 模块。</span><span class="sxs-lookup"><span data-stu-id="e5696-114">When you install the AzureRM module, any other Azure modules that have not previously been installed will be downloaded and installed from the PowerShell Gallery.</span></span>

<span data-ttu-id="e5696-115">Azure 服务管理模块与 Azure PowerShell Resource Manager 模块共享依赖项。</span><span class="sxs-lookup"><span data-stu-id="e5696-115">The Azure Service Management module shares dependencies with the Azure PowerShell Resource Manager modules.</span></span> <span data-ttu-id="e5696-116">如果已安装 Azure PowerShell Resource Manager 模块，需在安装命令中添加 `-AllowClobber` 参数。</span><span class="sxs-lookup"><span data-stu-id="e5696-116">If you have installed the Azure PowerShell Resource Manager modules, you will need to add the `-AllowClobber` parameter to the install command.</span></span> <span data-ttu-id="e5696-117">这样，便可以更新现有的共享依赖项。</span><span class="sxs-lookup"><span data-stu-id="e5696-117">This allows this existing shared dependencies to be updated.</span></span> <span data-ttu-id="e5696-118">如果不提供此参数，模块安装将会失败。</span><span class="sxs-lookup"><span data-stu-id="e5696-118">Without this parameter, installation of the module fails.</span></span>

```powershell
Install-Module Azure -AllowClobber
```

<span data-ttu-id="e5696-119">安装此模块后，可运行以下命令导入此模块：</span><span class="sxs-lookup"><span data-stu-id="e5696-119">After you install this module, you can import the module by running the following command:</span></span>

```powershell
Import-Module Azure
```

## <span data-ttu-id="e5696-120">使用 cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5696-120">To use the cmdlets</span></span>
<a id="to-use-the-cmdlets" class="xliff"></a>

<span data-ttu-id="e5696-121">若要开始使用 Azure 服务管理 cmdlet，请先登录到 Azure 帐户。</span><span class="sxs-lookup"><span data-stu-id="e5696-121">To start working with the Azure Service Management cmdlets, first log on to your Azure account.</span></span> <span data-ttu-id="e5696-122">若要登录到帐户，请运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="e5696-122">To log on to your account, run the following command:</span></span>

```powershell
Add-AzureAccount
```

<span data-ttu-id="e5696-123">登录到 Azure 后，Azure PowerShell 将为给定的会话创建上下文。</span><span class="sxs-lookup"><span data-stu-id="e5696-123">After logging into Azure, Azure PowerShell creates a context for the given session.</span></span> <span data-ttu-id="e5696-124">该上下文包含用于该会话中的所有 cmdlet 的 Azure PowerShell 环境、帐户、租户和订阅。</span><span class="sxs-lookup"><span data-stu-id="e5696-124">That context contains the Azure PowerShell environment, account, tenant, and subscription that will be used for all cmdlets within that session.</span></span> <span data-ttu-id="e5696-125">现已准备就绪，可以使用下面的模块。</span><span class="sxs-lookup"><span data-stu-id="e5696-125">Now you are ready to use the modules below.</span></span>

## <span data-ttu-id="e5696-126">Azure 服务管理 cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5696-126">Azure Service Management cmdlets</span></span>
<a id="azure-service-management-cmdlets" class="xliff"></a>

<span data-ttu-id="e5696-127">Azure PowerShell 模块经常更新。</span><span class="sxs-lookup"><span data-stu-id="e5696-127">Azure PowerShell modules are updated frequently.</span></span> <span data-ttu-id="e5696-128">如果你发现 cmdlet 联机帮助包含模块中所不包含的 cmdlet 或参数，请下载并安装最新版本的模块。</span><span class="sxs-lookup"><span data-stu-id="e5696-128">If you notice that the online cmdlet help includes cmdlets or parameters that are not in your module, download and install the latest version of the module.</span></span> <span data-ttu-id="e5696-129">若要查找模块版本，请键入：`(Get-Module Azure).Version`。</span><span class="sxs-lookup"><span data-stu-id="e5696-129">To find the version of your module, type: `(Get-Module Azure).Version`.</span></span>

<span data-ttu-id="e5696-130">有关可帮助你自动完成 Azure 中某些常见任务的示例脚本，请参阅 [Windows Azure 脚本中心](http://www.windowsazure.com/documentation/scripts/)。</span><span class="sxs-lookup"><span data-stu-id="e5696-130">For sample scripts that can help you automate some of the common tasks in Azure, see the [Windows Azure Script Center](http://www.windowsazure.com/documentation/scripts/).</span></span>

<span data-ttu-id="e5696-131">有关安装、学习、使用和自定义 Windows PowerShell 的一般信息，请参阅[使用 Windows PowerShell 编写脚本](http://go.microsoft.com/fwlink/p/?linkid=320210)。</span><span class="sxs-lookup"><span data-stu-id="e5696-131">For general information about installing, learning, using, and customizing Windows PowerShell, see [Scripting with Windows PowerShell](http://go.microsoft.com/fwlink/p/?linkid=320210).</span></span>
