---
title: "Azure PowerShell 概述 | Microsoft Docs"
description: "概述 Azure PowerShell 并提供安装和配置方法的链接。"
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.manager: carmonm
ms.date: 08/31/2017
ms.openlocfilehash: cd6b57ff6234895ec4f7a4200f9df0852b2280c2
ms.sourcegitcommit: b256bf48e15ee98865de0fae50e7b81878b03a54
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/03/2017
---
# <a name="overview-of-azure-powershell"></a><span data-ttu-id="fe4de-103">Azure PowerShell 概述</span><span class="sxs-lookup"><span data-stu-id="fe4de-103">Overview of Azure PowerShell</span></span>

<span data-ttu-id="fe4de-104">Azure PowerShell 提供一组可以使用 [Azure 资源管理器](/azure/azure-resource-manager/resource-group-overview)模型管理 Azure 资源的 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fe4de-104">Azure PowerShell provides a set of cmdlets that use the [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) model for managing your Azure resources.</span></span> <span data-ttu-id="fe4de-105">可以在浏览器中结合 [Azure Cloud Shell](/azure/cloud-shell/overview) 使用这些 cmdlet，或者将它们安装在本地计算机上并在任何 PowerShell 会话中使用。</span><span class="sxs-lookup"><span data-stu-id="fe4de-105">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or you can install it on your local machine and use it in any PowerShell session.</span></span>

<span data-ttu-id="fe4de-106">使用 [Cloud Shell](/azure/cloud-shell/overview) 在浏览器中运行 Azure PowerShell，或者在自己的计算机上[安装](install-azurerm-ps.md)它。</span><span class="sxs-lookup"><span data-stu-id="fe4de-106">Use the [Cloud Shell](/azure/cloud-shell/overview) to run the Azure PowerShell in your browser, or [install](install-azurerm-ps.md) it on own computer.</span></span> <span data-ttu-id="fe4de-107">然后阅读[入门](get-started-azureps.md)一文开始使用。</span><span class="sxs-lookup"><span data-stu-id="fe4de-107">Then read the [Get Started](get-started-azureps.md) article to begin using it.</span></span> <span data-ttu-id="fe4de-108">有关最新版本的信息，请参阅[发行说明](release-notes-azureps.md)。</span><span class="sxs-lookup"><span data-stu-id="fe4de-108">For information about the latest release, see the [release notes](release-notes-azureps.md).</span></span>

<span data-ttu-id="fe4de-109">以下示例有助于了解如何使用 Azure PowerShell 执行常见方案：</span><span class="sxs-lookup"><span data-stu-id="fe4de-109">The following samples can help you learn how to perform common scenarios with Azure PowerShell:</span></span>

* [<span data-ttu-id="fe4de-110">Linux 虚拟机</span><span class="sxs-lookup"><span data-stu-id="fe4de-110">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="fe4de-111">Windows 虚拟机</span><span class="sxs-lookup"><span data-stu-id="fe4de-111">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="fe4de-112">Web 应用</span><span class="sxs-lookup"><span data-stu-id="fe4de-112">Web Apps</span></span>](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="fe4de-113">SQL 数据库</span><span class="sxs-lookup"><span data-stu-id="fe4de-113">SQL Databases</span></span>](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

> [!NOTE]
> <span data-ttu-id="fe4de-114">如果部署使用无法转换的经典部署模型，则可安装 Azure PowerShell 的服务管理版本。</span><span class="sxs-lookup"><span data-stu-id="fe4de-114">If you have deployments that use the classic deployment model that cannot be converted, you can install the Service Management version of Azure PowerShell.</span></span> <span data-ttu-id="fe4de-115">有关详细信息，请参阅[安装 Azure PowerShell 服务管理模块](/powershell/azure/servicemanagement/install-azure-ps)。</span><span class="sxs-lookup"><span data-stu-id="fe4de-115">For more information, see [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span>


### <a name="need-help-with-powershell"></a><span data-ttu-id="fe4de-116">需要有关 PowerShell 的帮助？</span><span class="sxs-lookup"><span data-stu-id="fe4de-116">Need help with PowerShell?</span></span>

<span data-ttu-id="fe4de-117">如果不熟悉 PowerShell，可能会发现 PowerShell 简介文章很有帮助。</span><span class="sxs-lookup"><span data-stu-id="fe4de-117">If you are unfamiliar with PowerShell, you may find an introduction to PowerShell helpful.</span></span>

* [<span data-ttu-id="fe4de-118">安装 PowerShell</span><span class="sxs-lookup"><span data-stu-id="fe4de-118">Installing PowerShell</span></span>](/powershell/scripting/installing-windows-powershell)
* [<span data-ttu-id="fe4de-119">通过 PowerShell 编写脚本</span><span class="sxs-lookup"><span data-stu-id="fe4de-119">Scripting with PowerShell</span></span>](/powershell/scripting/scripting-with-windows-powershell)

<span data-ttu-id="fe4de-120">也可以观看此视频：[PowerShell 基础知识：（第 1 部分）PowerShell 入门](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1)。</span><span class="sxs-lookup"><span data-stu-id="fe4de-120">You can also watch this video: [PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).</span></span>

<span data-ttu-id="fe4de-121">或者，参加 Microsoft Virtual Academy 的 [PowerShell 快速入门](https://mva.microsoft.com/liveevents/powershell-jumpstart)培训。</span><span class="sxs-lookup"><span data-stu-id="fe4de-121">Or attend the Microsoft Virtual Academy's [Getting Started with PowerShell Jumpstart](https://mva.microsoft.com/liveevents/powershell-jumpstart).</span></span>

## <a name="other-azure-powershell-modules"></a><span data-ttu-id="fe4de-122">其他 Azure PowerShell 模块</span><span class="sxs-lookup"><span data-stu-id="fe4de-122">Other Azure PowerShell modules</span></span>

* [<span data-ttu-id="fe4de-123">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="fe4de-123">Azure Active Directory</span></span>](/powershell/azure/active-directory/)
* [<span data-ttu-id="fe4de-124">Azure 信息保护</span><span class="sxs-lookup"><span data-stu-id="fe4de-124">Azure Information Protection</span></span>](/powershell/azure/aip/)
* [<span data-ttu-id="fe4de-125">Azure Service Fabric</span><span class="sxs-lookup"><span data-stu-id="fe4de-125">Azure Service Fabric</span></span>](/powershell/azure/service-fabric/)
* [<span data-ttu-id="fe4de-126">Azure ElasticDB</span><span class="sxs-lookup"><span data-stu-id="fe4de-126">Azure ElasticDB</span></span>](/powershell/azure/elasticdbjobs/)
