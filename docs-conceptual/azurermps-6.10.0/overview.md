---
title: Azure PowerShell 概述 | Microsoft Docs
description: 概述 Azure PowerShell 并提供安装和配置方法的链接。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.manager: carmonm
ms.date: 09/11/2018
ms.openlocfilehash: f03243f6f560407b63aff154494cf164d670d810
ms.sourcegitcommit: a749eb729f583c9d0dd86141bbd04984d77ae9ab
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/11/2018
ms.locfileid: "48882059"
---
# <a name="overview-of-azure-powershell"></a><span data-ttu-id="023ab-103">Azure PowerShell 概述</span><span class="sxs-lookup"><span data-stu-id="023ab-103">Overview of Azure PowerShell</span></span>

<span data-ttu-id="023ab-104">Azure PowerShell 提供一组可以使用 [Azure 资源管理器](/azure/azure-resource-manager/resource-group-overview)模型管理 Azure 资源的 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="023ab-104">Azure PowerShell provides a set of cmdlets that use the [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) model for managing your Azure resources.</span></span> <span data-ttu-id="023ab-105">可以在浏览器中结合 [Azure Cloud Shell](/azure/cloud-shell/overview) 使用这些 cmdlet，或者将它们安装在本地计算机上并在任何 PowerShell 会话中使用。</span><span class="sxs-lookup"><span data-stu-id="023ab-105">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or you can install it on your local machine and use it in any PowerShell session.</span></span>

<span data-ttu-id="023ab-106">使用 [Cloud Shell](/azure/cloud-shell/overview) 在浏览器中运行 Azure PowerShell，或者在自己的计算机上[安装](install-azurerm-ps.md)它。</span><span class="sxs-lookup"><span data-stu-id="023ab-106">Use the [Cloud Shell](/azure/cloud-shell/overview) to run the Azure PowerShell in your browser, or [install](install-azurerm-ps.md) it on own computer.</span></span> <span data-ttu-id="023ab-107">然后阅读[入门](get-started-azureps.md)一文开始使用。</span><span class="sxs-lookup"><span data-stu-id="023ab-107">Then read the [Get Started](get-started-azureps.md) article to begin using it.</span></span> <span data-ttu-id="023ab-108">有关最新版本的信息，请参阅[发行说明](release-notes-azureps.md)。</span><span class="sxs-lookup"><span data-stu-id="023ab-108">For information about the latest release, see the [release notes](release-notes-azureps.md).</span></span>

<span data-ttu-id="023ab-109">以下示例有助于了解如何使用 Azure PowerShell 执行常见方案：</span><span class="sxs-lookup"><span data-stu-id="023ab-109">The following samples can help you learn how to perform common scenarios with Azure PowerShell:</span></span>

* [<span data-ttu-id="023ab-110">Linux 虚拟机</span><span class="sxs-lookup"><span data-stu-id="023ab-110">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="023ab-111">Windows 虚拟机</span><span class="sxs-lookup"><span data-stu-id="023ab-111">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="023ab-112">Web 应用</span><span class="sxs-lookup"><span data-stu-id="023ab-112">Web Apps</span></span>](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="023ab-113">SQL 数据库</span><span class="sxs-lookup"><span data-stu-id="023ab-113">SQL Databases</span></span>](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

> [!NOTE]
> <span data-ttu-id="023ab-114">如果部署使用无法转换的经典部署模型，则可安装 Azure PowerShell 的服务管理版本。</span><span class="sxs-lookup"><span data-stu-id="023ab-114">If you have deployments that use the classic deployment model that cannot be converted, you can install the Service Management version of Azure PowerShell.</span></span> <span data-ttu-id="023ab-115">有关详细信息，请参阅[安装 Azure PowerShell 服务管理模块](/powershell/azure/servicemanagement/install-azure-ps)。</span><span class="sxs-lookup"><span data-stu-id="023ab-115">For more information, see [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span>

## <a name="learn-powershell-basics"></a><span data-ttu-id="023ab-116">了解 PowerShell 基础知识</span><span class="sxs-lookup"><span data-stu-id="023ab-116">Learn PowerShell basics</span></span>

<span data-ttu-id="023ab-117">如果你不熟悉 PowerShell，可以参阅 PowerShell 简介。</span><span class="sxs-lookup"><span data-stu-id="023ab-117">If you're unfamiliar with PowerShell, an introduction to PowerShell may be helpful.</span></span>

* [<span data-ttu-id="023ab-118">安装 PowerShell</span><span class="sxs-lookup"><span data-stu-id="023ab-118">Installing PowerShell</span></span>](/powershell/scripting/setup/installing-windows-powershell)
* [<span data-ttu-id="023ab-119">通过 PowerShell 编写脚本</span><span class="sxs-lookup"><span data-stu-id="023ab-119">Scripting with PowerShell</span></span>](/powershell/scripting/powershell-scripting)

<span data-ttu-id="023ab-120">也可以观看此视频：[PowerShell 基础知识：（第 1 部分）PowerShell 入门](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1)。</span><span class="sxs-lookup"><span data-stu-id="023ab-120">You can also watch this video: [PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).</span></span>

<span data-ttu-id="023ab-121">或者，参加 Microsoft Virtual Academy 的 [PowerShell 快速入门](https://mva.microsoft.com/liveevents/powershell-jumpstart)培训。</span><span class="sxs-lookup"><span data-stu-id="023ab-121">Or attend the Microsoft Virtual Academy's [Getting Started with PowerShell Jumpstart](https://mva.microsoft.com/liveevents/powershell-jumpstart).</span></span>

## <a name="build-your-skills-with-microsoft-learn"></a><span data-ttu-id="023ab-122">利用 Microsoft Learn 掌握技能</span><span class="sxs-lookup"><span data-stu-id="023ab-122">Build your skills with Microsoft Learn</span></span>

- [<span data-ttu-id="023ab-123">将脚本与 PowerShell 配合使用，自动完成 Azure 任务</span><span class="sxs-lookup"><span data-stu-id="023ab-123">Automate Azure tasks using scripts with PowerShell</span></span>](/learn/modules/automate-azure-tasks-with-powershell/)
- [<span data-ttu-id="023ab-124">更多交互式学习...</span><span class="sxs-lookup"><span data-stu-id="023ab-124">More interactive learning...</span></span>](/learn/browse/?term=powershell)

## <a name="other-azure-powershell-modules"></a><span data-ttu-id="023ab-125">其他 Azure PowerShell 模块</span><span class="sxs-lookup"><span data-stu-id="023ab-125">Other Azure PowerShell modules</span></span>

* [<span data-ttu-id="023ab-126">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="023ab-126">Azure Active Directory</span></span>](/powershell/azure/active-directory/)
* [<span data-ttu-id="023ab-127">Azure 信息保护</span><span class="sxs-lookup"><span data-stu-id="023ab-127">Azure Information Protection</span></span>](/powershell/azure/aip/)
* [<span data-ttu-id="023ab-128">Azure Service Fabric</span><span class="sxs-lookup"><span data-stu-id="023ab-128">Azure Service Fabric</span></span>](/powershell/azure/service-fabric/)
* [<span data-ttu-id="023ab-129">Azure ElasticDB</span><span class="sxs-lookup"><span data-stu-id="023ab-129">Azure ElasticDB</span></span>](/powershell/azure/elasticdbjobs/)