---
title: Azure PowerShell 更改日志 | Microsoft Docs
description: 下面提供了对 Azure PowerShell 最新版本所做更改的历史记录。
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: b42ad6f22f47e10c9190cf5a919f781375ff26f2
ms.sourcegitcommit: 5971c92cb023bdd1d71fa2ad0a3b378abfbd092a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/23/2018
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