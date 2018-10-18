---
title: 使用 Azure PowerShell 管理 Azure 订阅
description: 使用 Azure PowerShell 管理 Azure 订阅
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: 3f1c1bab5f9903ee7df813bf1ef043c7107ebe79
ms.sourcegitcommit: f6f5e256143aa6c097de3e57e930d8badea49f30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2018
ms.locfileid: "49399121"
---
# <a name="manage-multiple-azure-subscriptions"></a>管理多个 Azure 订阅

如果你是 Azure 新手，也许只有一个订阅。 但如果使用 Azure 有一段时间，可能已创建了多个 Azure 订阅。 可将 Azure PowerShell 配置为针对特定的订阅执行命令。

1. 获取帐户中所有订阅的列表。

    ```azurepowershell-interactive
    Get-AzureRmSubscription
    ```

    ```output
    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My Production Subscription
    CurrentStorageAccount :

    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My DevTest Subscription
    CurrentStorageAccount :

    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My Demos
    CurrentStorageAccount :
    ```

2. 设置默认值。

    ```azurepowershell-interactive
    Select-AzureRmSubscription -Subscription "My Demos"
    ```

3. 通过运行 `Get-AzureRmContext` cmdlet 验证更改。

    ```azurepowershell-interactive
    Get-AzureRmContext
    ```

    ```output
    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My Demos
    CurrentStorageAccount :
    ```

设置默认订阅后，所有 Azure PowerShell 命令将针对此订阅运行。
