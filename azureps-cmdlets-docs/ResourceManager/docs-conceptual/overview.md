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
ms.date: 05/15/2017
ms.openlocfilehash: f26b204604018449584c1fd2ff199728487b1515
ms.sourcegitcommit: 226527be7cb647acfe2ea9ab151185053ab3c6db
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/29/2017
---
# <span data-ttu-id="9f04f-103">Azure PowerShell 概述</span><span class="sxs-lookup"><span data-stu-id="9f04f-103">Overview of Azure PowerShell</span></span>
<a id="overview-of-azure-powershell" class="xliff"></a>

<span data-ttu-id="9f04f-104">Azure PowerShell 提供一组可以使用 [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) 模型管理 Azure 资源的 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9f04f-104">Azure PowerShell provides a set of cmdlets that use the [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) model for managing your Azure resources.</span></span>

<span data-ttu-id="9f04f-105">请参阅[安装](install-azurerm-ps.md)一文，了解如何在系统上启动和运行 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="9f04f-105">Review the [Install](install-azurerm-ps.md) article to get Azure PowerShell up and running on your system.</span></span> <span data-ttu-id="9f04f-106">然后阅读[入门](get-started-azureps.md)一文开始 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="9f04f-106">Then read the [Get Started](get-started-azureps.md) article to begin using it.</span></span> <span data-ttu-id="9f04f-107">有关最新版本的信息，请参阅[发行说明](release-notes-azureps.md)。</span><span class="sxs-lookup"><span data-stu-id="9f04f-107">For information about the latest release, see the [release notes](release-notes-azureps.md).</span></span>

<span data-ttu-id="9f04f-108">以下示例可帮助你了解如何使用 Azure PowerShell 执行常见方案：</span><span class="sxs-lookup"><span data-stu-id="9f04f-108">The following samples can help you learn how to perform common scenarios with Azure PowerShell:</span></span>

* [<span data-ttu-id="9f04f-109">Linux 虚拟机</span><span class="sxs-lookup"><span data-stu-id="9f04f-109">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="9f04f-110">Windows 虚拟机</span><span class="sxs-lookup"><span data-stu-id="9f04f-110">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="9f04f-111">Web 应用</span><span class="sxs-lookup"><span data-stu-id="9f04f-111">Web Apps</span></span>](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="9f04f-112">SQL 数据库</span><span class="sxs-lookup"><span data-stu-id="9f04f-112">SQL Databases</span></span>](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

> [!NOTE]
> <span data-ttu-id="9f04f-113">如果部署使用无法转换的经典部署模型，则可安装 Azure PowerShell 的服务管理版本。</span><span class="sxs-lookup"><span data-stu-id="9f04f-113">If you have deployments that use the classic deployment model that cannot be converted, you can install the Service Management version of Azure PowerShell.</span></span> <span data-ttu-id="9f04f-114">有关详细信息，请参阅</span><span class="sxs-lookup"><span data-stu-id="9f04f-114">For more information, see</span></span>

<span data-ttu-id="9f04f-115">[安装 Azure PowerShell 服务管理模块](/powershell/azure/servicemanagement/install-azure-ps)。</span><span class="sxs-lookup"><span data-stu-id="9f04f-115">[Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span>


### <span data-ttu-id="9f04f-116">需要有关 PowerShell 的帮助？</span><span class="sxs-lookup"><span data-stu-id="9f04f-116">Need help with PowerShell?</span></span>
<a id="need-help-with-powershell" class="xliff"></a>

<span data-ttu-id="9f04f-117">如果不熟悉 PowerShell，可能会发现 PowerShell 简介文章很有帮助。</span><span class="sxs-lookup"><span data-stu-id="9f04f-117">If you are unfamiliar with PowerShell, you may find an introduction to PowerShell helpful.</span></span> <span data-ttu-id="9f04f-118">若要开始使用 PowerShell，请参阅[使用 PowerShell 编写脚本](https://technet.microsoft.com/library/bb978526.aspx)。</span><span class="sxs-lookup"><span data-stu-id="9f04f-118">To get started with PowerShell, see [Scripting with PowerShell](https://technet.microsoft.com/library/bb978526.aspx).</span></span>

<span data-ttu-id="9f04f-119">也可以观看此视频：[PowerShell 基础知识：（第 1 部分）PowerShell 入门](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1)。</span><span class="sxs-lookup"><span data-stu-id="9f04f-119">You can also watch this video: [PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).</span></span>

## <span data-ttu-id="9f04f-120">其他 Azure PowerShell 模块</span><span class="sxs-lookup"><span data-stu-id="9f04f-120">Other Azure PowerShell modules</span></span>
<a id="other-azure-powershell-modules" class="xliff"></a>

* [<span data-ttu-id="9f04f-121">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="9f04f-121">Azure Active Directory</span></span>](/powershell/azure/active-directory/)
* [<span data-ttu-id="9f04f-122">Azure 信息保护</span><span class="sxs-lookup"><span data-stu-id="9f04f-122">Azure Information Protection</span></span>](/powershell/azure/aip/)
* [<span data-ttu-id="9f04f-123">Azure Service Fabric</span><span class="sxs-lookup"><span data-stu-id="9f04f-123">Azure Service Fabric</span></span>](/powershell/azure/oservice-fabric/)
* [<span data-ttu-id="9f04f-124">Azure ElasticDB</span><span class="sxs-lookup"><span data-stu-id="9f04f-124">Azure ElasticDB</span></span>](/powershell/azure/elasticdbjobs/)
