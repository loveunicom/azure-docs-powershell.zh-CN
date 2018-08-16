---
title: 使用 Azure PowerShell 管理 Azure 订阅
description: 使用 Azure PowerShell 管理 Azure 订阅
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/30/2017
ms.openlocfilehash: e1606ddb02adf1de2cb5496917d61755ac3dad23
ms.sourcegitcommit: 7df99dc139e93a8a4e6d5b1a27968857588d75dd
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/16/2018
ms.locfileid: "40106327"
---
# <a name="manage-multiple-azure-subscriptions"></a><span data-ttu-id="f84db-103">管理多个 Azure 订阅</span><span class="sxs-lookup"><span data-stu-id="f84db-103">Manage multiple Azure subscriptions</span></span>

<span data-ttu-id="f84db-104">如果是 Azure 的新手，也许只有一个订阅。</span><span class="sxs-lookup"><span data-stu-id="f84db-104">If you are brand new to Azure, you probably only have a single subscription.</span></span> <span data-ttu-id="f84db-105">但如果使用 Azure 有一段时间，可能已创建了多个 Azure 订阅。</span><span class="sxs-lookup"><span data-stu-id="f84db-105">But if you have been using Azure for a while, you may have created multiple Azure subscriptions.</span></span> <span data-ttu-id="f84db-106">可将 Azure PowerShell 配置为针对特定的订阅执行命令。</span><span class="sxs-lookup"><span data-stu-id="f84db-106">You can configure Azure PowerShell to execute commands against a particular subscription.</span></span>

1. <span data-ttu-id="f84db-107">获取帐户中所有订阅的列表。</span><span class="sxs-lookup"><span data-stu-id="f84db-107">Get a list of all subscriptions in your account.</span></span>

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

2. <span data-ttu-id="f84db-108">设置默认值。</span><span class="sxs-lookup"><span data-stu-id="f84db-108">Set the default.</span></span>

    ```azurepowershell-interactive
    Select-AzureRmSubscription -Subscription "My Demos"
    ```

3. <span data-ttu-id="f84db-109">通过运行 `Get-AzureRmContext` cmdlet 验证更改。</span><span class="sxs-lookup"><span data-stu-id="f84db-109">Verify the change by running the `Get-AzureRmContext` cmdlet.</span></span>

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

<span data-ttu-id="f84db-110">设置默认订阅后，所有后续 Azure PowerShell 命令将针对此订阅运行。</span><span class="sxs-lookup"><span data-stu-id="f84db-110">Once you set your default subscription, all subsequent Azure PowerShell commands run against this subscription.</span></span>
