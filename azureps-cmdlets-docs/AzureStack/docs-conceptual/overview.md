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
# <a name="azure-stack-powershell"></a>Azure Stack PowerShell 

Azure Stack 需要以下两个 PowerShell 模块：  

1. 与 Azure Stack 兼容的 **AzureRM** 模块，可通过安装 **2017-03-09-profile** API 版本配置文件获取。 使用此配置文件安装的 cmdlet 可由 Azure Stack 云管理员和租户使用。 若要了解此配置文件中提供的 PowerShell cmdlet，请参阅 [AzureRM 版本 1.2.9](https://docs.microsoft.com/en-us/powershell/azure/overview?view=azurermps-1.2.9) 模块的 PowerShell 参考内容。  

2. **AzureStack** 模块版本 **1.2.9**。 使用此模块安装的 cmdlet 只能由 Azure Stack 云管理员使用。 管理员可以使用此模块提供的 PowerShell cmdlet 执行多种操作，例如，管理产品、计划、服务、配额等等。 若要了解此模块提供的 PowerShell cmdlet，请参阅 [AzureStackAdmin](https://docs.microsoft.com/en-us/powershell/module/azurerm.azurestackadmin/?view=azurestackps-1.2.9#azurerm.azurestackadmin) 和 [AzureStackStorage](https://docs.microsoft.com/en-us/powershell/module/azurerm.azurestackstorage/?view=azurestackps-1.2.9#azurerm.azurestackstorage) 参考内容。

## <a name="next-steps"></a>后续步骤

* [安装适用于 Azure Stack 的 PowerShell](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-install?view=azurestackps-1.2.9&toc=%2fpowershell%2fmodule%2ftoc.json%3fview%3dazurestackps-1.2.9&view=azurestackps-1.2.9)
* [配置适用于 Azure Stack 的 PowerShell](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-configure?view=azurestackps-1.2.9&toc=%2fpowershell%2fmodule%2ftoc.json%3fview%3dazurestackps-1.2.9&view=azurestackps-1.2.9)


