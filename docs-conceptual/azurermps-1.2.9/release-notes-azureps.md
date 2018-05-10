---
title: Azure PowerShell 更改日志 | Microsoft Docs
description: 下面提供了对 Azure PowerShell 最新版本所做更改的历史记录。
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: 5fe7591855577e083aad5923aed37b18d0b2a40c
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/08/2018
---
# <a name="release-notes"></a><span data-ttu-id="580e3-103">发行说明</span><span class="sxs-lookup"><span data-stu-id="580e3-103">Release notes</span></span>

<span data-ttu-id="580e3-104">下面是此版本中对 Azure PowerShell 所做的更改列表。</span><span class="sxs-lookup"><span data-stu-id="580e3-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

## <a name="version-129"></a><span data-ttu-id="580e3-105">版本 1.2.9</span><span class="sxs-lookup"><span data-stu-id="580e3-105">Version 1.2.9</span></span>

<span data-ttu-id="580e3-106">此版本的更改</span><span class="sxs-lookup"><span data-stu-id="580e3-106">Changes This Release</span></span>

* <span data-ttu-id="580e3-107">AzureRm.AzureStackAdmin 模块</span><span class="sxs-lookup"><span data-stu-id="580e3-107">AzureRm.AzureStackAdmin Module</span></span>
    + <span data-ttu-id="580e3-108">更改了 Add-AzureRmResourceProviderRegistration cmdlet，以便支持管理员 Azure Resource Manager 和租户 Azure Resource Manager 的拆分。</span><span class="sxs-lookup"><span data-stu-id="580e3-108">Changes in the Add-AzureRmResourceProviderRegistration cmdlet for the support of Admin Azure resource manager and tenant azure resource manager split.</span></span> <span data-ttu-id="580e3-109">添加了新参数 -ResourceManagerType。</span><span class="sxs-lookup"><span data-stu-id="580e3-109">A new parameter -ResourceManagerType has been added.</span></span>
    + <span data-ttu-id="580e3-110">从每个 cmdlet 中删除了参数 -AdminUri、-ApiVersion、-SubscriptionId 和 -Token。</span><span class="sxs-lookup"><span data-stu-id="580e3-110">Removal of the parameters -AdminUri, -ApiVersion, -SubscriptionId and -Token from each cmdlets.</span></span> <span data-ttu-id="580e3-111">我们一直在列显警告消息，指出这些参数即将弃用，并且现在已被删除。</span><span class="sxs-lookup"><span data-stu-id="580e3-111">We have been printing warnings that these parameters will be deprecated and now they got removed.</span></span>
* <span data-ttu-id="580e3-112">AzureStackStorage 模块</span><span class="sxs-lookup"><span data-stu-id="580e3-112">AzureStackStorage module</span></span>
    + <span data-ttu-id="580e3-113">添加了新的 cmdlet 用于支持容器迁移方案。</span><span class="sxs-lookup"><span data-stu-id="580e3-113">Added new cmdlets to support container migration scenarios.</span></span>
    + <span data-ttu-id="580e3-114">删除了引用内部组件和基础功能的 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="580e3-114">Removed cmdlets referring to internal components and underlying features.</span></span>
* <span data-ttu-id="580e3-115">AzureRM.BootStrapper</span><span class="sxs-lookup"><span data-stu-id="580e3-115">AzureRM.BootStrapper</span></span>
    + <span data-ttu-id="580e3-116">创建了新的模块用于通过版本配置文件管理 Azure PowerShell cmdlet 的版本</span><span class="sxs-lookup"><span data-stu-id="580e3-116">Created new module to manage versions of Azure PowerShell cmdlets through the use of version profiles</span></span>