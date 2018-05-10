---
title: Azure Stack PowerShell 概述 | Microsoft Docs
description: Azure Stack PowerShell 安装和配置概述。
author: SnehaGunda
manager: Byronr
ms.product: azure-stack
ms.service: powershell
ms.devlang: powershell
ms.topic: reference
ms.author: sngun
ms.manager: byronr
ms.openlocfilehash: f895992b4200f260189b3dbc541452e73a377b00
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/08/2018
---
# <a name="azure-stack-powershell"></a>Azure Stack PowerShell

Azure Stack 需要以下两个 PowerShell 模块：  

1. 与 Azure Stack 兼容的 **AzureRM** 模块，可通过安装 **2017-03-09-profile** API 版本配置文件获取。 使用此配置文件安装的 cmdlet 只能由 Azure Stack 操作员和用户使用。

2. 最新版本为 **AzureStack** 模块的 **1.2.11** 安装。 使用此模块安装的 cmdlet 只能由 Azure Stack 操作员使用。 操作员可以使用此模块提供的 PowerShell cmdlet 执行多种操作，例如，管理产品、计划、服务、配额等等。 若要了解此模块提供的 PowerShell cmdlet，请参阅 [AzureStackAdmin](https://docs.microsoft.com/powershell/module/azurerm.azurestackadmin/?view=azurestackps-1.2.11#azurerm.azurestackadmin) 和 [AzureStackStorage](https://docs.microsoft.com/powershell/module/azurerm.azurestackstorage/?view=azurestackps-1.2.11#azurerm.azurestackstorage) 参考内容。

## <a name="next-steps"></a>后续步骤

* [安装适用于 Azure Stack 的 PowerShell](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install?view=azurestackps-1.2.9&toc=%2fpowershell%2fmodule%2ftoc.json%3fview%3dazurestackps-1.2.9&view=azurestackps-1.2.9)
* [配置适用于 Azure Stack 的 PowerShell](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-configure?view=azurestackps-1.2.9&toc=%2fpowershell%2fmodule%2ftoc.json%3fview%3dazurestackps-1.2.9&view=azurestackps-1.2.9)
