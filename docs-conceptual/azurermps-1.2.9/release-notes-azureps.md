---
title: "Azure PowerShell 更改日志 | Microsoft Docs"
description: "下面提供了对 Azure PowerShell 最新版本所做更改的历史记录。"
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: 
ms.date: 05/18/2017
ms.openlocfilehash: 5fe7591855577e083aad5923aed37b18d0b2a40c
ms.sourcegitcommit: 226527be7cb647acfe2ea9ab151185053ab3c6db
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/29/2017
---
# <a name="release-notes"></a>发行说明

下面是此版本中对 Azure PowerShell 所做的更改列表。

## <a name="version-129"></a>版本 1.2.9

此版本的更改

* AzureRm.AzureStackAdmin 模块
    + 更改了 Add-AzureRmResourceProviderRegistration cmdlet，以便支持管理员 Azure Resource Manager 和租户 Azure Resource Manager 的拆分。 添加了新参数 -ResourceManagerType。
    + 从每个 cmdlet 中删除了参数 -AdminUri、-ApiVersion、-SubscriptionId 和 -Token。 我们一直在列显警告消息，指出这些参数即将弃用，并且现在已被删除。
* AzureStackStorage 模块
    + 添加了新的 cmdlet 用于支持容器迁移方案。
    + 删除了引用内部组件和基础功能的 cmdlet。
* AzureRM.BootStrapper
    + 创建了新的模块用于通过版本配置文件管理 Azure PowerShell cmdlet 的版本