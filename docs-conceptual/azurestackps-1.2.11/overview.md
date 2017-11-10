---
title: "Azure Stack PowerShell 概述 | Microsoft Docs"
description: "Azure Stack PowerShell 安装和配置概述。"
author: SnehaGunda
manager: Byronr
ms.product: azure-stack
ms.service: powershell
ms.devlang: powershell
ms.topic: reference
ms.author: sngun
ms.manager: byronr
ms.openlocfilehash: 49980b361c580a1a00f07c2002241e71f2c0b654
ms.sourcegitcommit: df44d5d9874b55455ec745f1846e06a4b3266d13
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/06/2017
---
# <a name="azure-stack-powershell"></a><span data-ttu-id="76c09-103">Azure Stack PowerShell</span><span class="sxs-lookup"><span data-stu-id="76c09-103">Azure Stack PowerShell</span></span>

<span data-ttu-id="76c09-104">Azure Stack 需要以下两个 PowerShell 模块：</span><span class="sxs-lookup"><span data-stu-id="76c09-104">Azure Stack requires the following two PowerShell modules:</span></span>  

1. <span data-ttu-id="76c09-105">与 Azure Stack 兼容的 **AzureRM** 模块，可通过安装 **2017-03-09-profile** API 版本配置文件获取。</span><span class="sxs-lookup"><span data-stu-id="76c09-105">The Azure Stack compatible **AzureRM** module which is available by installing the **2017-03-09-profile** API Version Profile.</span></span> <span data-ttu-id="76c09-106">使用此配置文件安装的 cmdlet 只能由 Azure Stack 操作员和用户使用。</span><span class="sxs-lookup"><span data-stu-id="76c09-106">The cmdlets installed by using this profile can be used by Azure Stack operators and users.</span></span>

2. <span data-ttu-id="76c09-107">最新版本为 **AzureStack** 模块的 **1.2.11** 安装。</span><span class="sxs-lookup"><span data-stu-id="76c09-107">The most current version is the **1.2.11** install of the **AzureStack** module.</span></span> <span data-ttu-id="76c09-108">使用此模块安装的 cmdlet 只能由 Azure Stack 操作员使用。</span><span class="sxs-lookup"><span data-stu-id="76c09-108">The cmdlets installed by using this module can be used by Azure Stack operators only.</span></span> <span data-ttu-id="76c09-109">操作员可以使用此模块提供的 PowerShell cmdlet 执行多种操作，例如，管理产品、计划、服务、配额等等。</span><span class="sxs-lookup"><span data-stu-id="76c09-109">Operators can perform operations such as manage offers, plans, services, quotas, etc. by using the PowerShell cmdlets provided by this module.</span></span> <span data-ttu-id="76c09-110">若要了解此模块提供的 PowerShell cmdlet，请参阅 [AzureStackAdmin](https://docs.microsoft.com/en-us/powershell/module/azurerm.azurestackadmin/?view=azurestackps-1.2.11#azurerm.azurestackadmin) 和 [AzureStackStorage](https://docs.microsoft.com/en-us/powershell/module/azurerm.azurestackstorage/?view=azurestackps-1.2.11#azurerm.azurestackstorage) 参考内容。</span><span class="sxs-lookup"><span data-stu-id="76c09-110">To learn about the PowerShell cmdlets available in this module, see the [AzureStackAdmin](https://docs.microsoft.com/en-us/powershell/module/azurerm.azurestackadmin/?view=azurestackps-1.2.11#azurerm.azurestackadmin) and [AzureStackStorage](https://docs.microsoft.com/en-us/powershell/module/azurerm.azurestackstorage/?view=azurestackps-1.2.11#azurerm.azurestackstorage) Reference content.</span></span>

## <a name="next-steps"></a><span data-ttu-id="76c09-111">后续步骤</span><span class="sxs-lookup"><span data-stu-id="76c09-111">Next Steps</span></span>

* [<span data-ttu-id="76c09-112">安装适用于 Azure Stack 的 PowerShell</span><span class="sxs-lookup"><span data-stu-id="76c09-112">Install PowerShell for Azure Stack</span></span>](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-install?view=azurestackps-1.2.9&toc=%2fpowershell%2fmodule%2ftoc.json%3fview%3dazurestackps-1.2.9&view=azurestackps-1.2.9)
* [<span data-ttu-id="76c09-113">配置适用于 Azure Stack 的 PowerShell</span><span class="sxs-lookup"><span data-stu-id="76c09-113">Configure PowerShell for use with Azure Stack</span></span>](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-configure?view=azurestackps-1.2.9&toc=%2fpowershell%2fmodule%2ftoc.json%3fview%3dazurestackps-1.2.9&view=azurestackps-1.2.9)
