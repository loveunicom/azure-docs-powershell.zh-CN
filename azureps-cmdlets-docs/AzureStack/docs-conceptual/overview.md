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
ms.openlocfilehash: 2a03697e0f3e80d63c48f2dc5615f6c99b9ef716
ms.sourcegitcommit: 226527be7cb647acfe2ea9ab151185053ab3c6db
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/29/2017
---
# <a name="azure-stack-powershell"></a><span data-ttu-id="62b01-103">Azure Stack PowerShell</span><span class="sxs-lookup"><span data-stu-id="62b01-103">Azure Stack PowerShell</span></span> 

<span data-ttu-id="62b01-104">Azure Stack 需要以下两个 PowerShell 模块：</span><span class="sxs-lookup"><span data-stu-id="62b01-104">Azure Stack requires the following two PowerShell modules:</span></span>  

1. <span data-ttu-id="62b01-105">与 Azure Stack 兼容的 **AzureRM** 模块，可通过安装 **2017-03-09-profile** API 版本配置文件获取。</span><span class="sxs-lookup"><span data-stu-id="62b01-105">The Azure Stack compatible **AzureRM** module which is available by installing the **2017-03-09-profile** API Version Profile.</span></span> <span data-ttu-id="62b01-106">使用此配置文件安装的 cmdlet 可由 Azure Stack 云管理员和租户使用。</span><span class="sxs-lookup"><span data-stu-id="62b01-106">The cmdlets installed by using this profile can be used by the Azure Stack cloud administrators and the tenants.</span></span> <span data-ttu-id="62b01-107">若要了解此配置文件中提供的 PowerShell cmdlet，请参阅 [AzureRM 版本 1.2.9](https://docs.microsoft.com/en-us/powershell/azure/overview?view=azurermps-1.2.9) 模块的 PowerShell 参考内容。</span><span class="sxs-lookup"><span data-stu-id="62b01-107">To learn about the PowerShell cmdlets that are available in this profile, see the PowerShell reference content for the [1.2.9 version of AzureRM](https://docs.microsoft.com/en-us/powershell/azure/overview?view=azurermps-1.2.9) module.</span></span>  

2. <span data-ttu-id="62b01-108">**AzureStack** 模块版本 **1.2.9**。</span><span class="sxs-lookup"><span data-stu-id="62b01-108">The **1.2.9** version of the **AzureStack** module.</span></span> <span data-ttu-id="62b01-109">使用此模块安装的 cmdlet 只能由 Azure Stack 云管理员使用。</span><span class="sxs-lookup"><span data-stu-id="62b01-109">The cmdlets installed by using this module can be used by Azure Stack cloud administrators only.</span></span> <span data-ttu-id="62b01-110">管理员可以使用此模块提供的 PowerShell cmdlet 执行多种操作，例如，管理产品、计划、服务、配额等等。</span><span class="sxs-lookup"><span data-stu-id="62b01-110">Administrator can perform operations such as manage offers, plans, services, quotas, etc. by using the PowerShell cmdlets provided by this module.</span></span> <span data-ttu-id="62b01-111">若要了解此模块提供的 PowerShell cmdlet，请参阅 [AzureStackAdmin](https://docs.microsoft.com/en-us/powershell/module/azurerm.azurestackadmin/?view=azurestackps-1.2.9#azurerm.azurestackadmin) 和 [AzureStackStorage](https://docs.microsoft.com/en-us/powershell/module/azurerm.azurestackstorage/?view=azurestackps-1.2.9#azurerm.azurestackstorage) 参考内容。</span><span class="sxs-lookup"><span data-stu-id="62b01-111">To learn about the PowerShell cmdlets available in this module, see the [AzureStackAdmin](https://docs.microsoft.com/en-us/powershell/module/azurerm.azurestackadmin/?view=azurestackps-1.2.9#azurerm.azurestackadmin) and [AzureStackStorage](https://docs.microsoft.com/en-us/powershell/module/azurerm.azurestackstorage/?view=azurestackps-1.2.9#azurerm.azurestackstorage) Reference content.</span></span>

## <a name="next-steps"></a><span data-ttu-id="62b01-112">后续步骤</span><span class="sxs-lookup"><span data-stu-id="62b01-112">Next Steps</span></span>

* [<span data-ttu-id="62b01-113">安装适用于 Azure Stack 的 PowerShell</span><span class="sxs-lookup"><span data-stu-id="62b01-113">Install PowerShell for Azure Stack</span></span>](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-install?view=azurestackps-1.2.9&toc=%2fpowershell%2fmodule%2ftoc.json%3fview%3dazurestackps-1.2.9&view=azurestackps-1.2.9)
* [<span data-ttu-id="62b01-114">配置适用于 Azure Stack 的 PowerShell</span><span class="sxs-lookup"><span data-stu-id="62b01-114">Configure PowerShell for use with Azure Stack</span></span>](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-configure?view=azurestackps-1.2.9&toc=%2fpowershell%2fmodule%2ftoc.json%3fview%3dazurestackps-1.2.9&view=azurestackps-1.2.9)


