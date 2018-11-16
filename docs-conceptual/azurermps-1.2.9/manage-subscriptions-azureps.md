---
title: 使用 Azure PowerShell 管理 Azure 订阅 | Microsoft Docs
description: 使用 Azure PowerShell 管理 Azure 订阅
keywords: Azure PowerShell, 订阅
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/30/2017
ms.openlocfilehash: 8869b700e513d6fc07e69de1dbfe852bd2a52df1
ms.sourcegitcommit: 4afdba3cd7e1d348876ce59f3503fdcd258f79ab
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/15/2018
ms.locfileid: "51576260"
---
# <a name="manage-multiple-azure-subscriptions"></a><span data-ttu-id="4e39b-104">管理多个 Azure 订阅</span><span class="sxs-lookup"><span data-stu-id="4e39b-104">Manage multiple Azure subscriptions</span></span>

<span data-ttu-id="4e39b-105">如果是 Azure 的新手，也许只有一个订阅。</span><span class="sxs-lookup"><span data-stu-id="4e39b-105">If you are brand new to Azure, you probably only have a single subscription.</span></span> <span data-ttu-id="4e39b-106">但如果使用 Azure 有一段时间，可能已创建了多个 Azure 订阅。</span><span class="sxs-lookup"><span data-stu-id="4e39b-106">But if you have been using Azure for a while, you may have created multiple Azure subscriptions.</span></span> <span data-ttu-id="4e39b-107">可将 Azure PowerShell 配置为针对特定的订阅执行命令。</span><span class="sxs-lookup"><span data-stu-id="4e39b-107">You can configure Azure PowerShell to execute commands against a particular subscription.</span></span>

1. <span data-ttu-id="4e39b-108">获取帐户中所有订阅的列表。</span><span class="sxs-lookup"><span data-stu-id="4e39b-108">Get a list of all subscriptions in your account.</span></span>

    ```powershell-interactive
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

2. <span data-ttu-id="4e39b-109">设置默认值。</span><span class="sxs-lookup"><span data-stu-id="4e39b-109">Set the default.</span></span>

    ```powershell-interactive
    Select-AzureRmSubscription -SubscriptionName "My Demos"
    ```

3. <span data-ttu-id="4e39b-110">通过运行 `Get-AzureRmContext` cmdlet 验证更改。</span><span class="sxs-lookup"><span data-stu-id="4e39b-110">Verify the change by running the `Get-AzureRmContext` cmdlet.</span></span>

    ```powershell-interactive
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

<span data-ttu-id="4e39b-111">设置默认订阅后，所有后续 Azure PowerShell 命令将针对此订阅运行。</span><span class="sxs-lookup"><span data-stu-id="4e39b-111">Once you set your default subscription, all subsequent Azure PowerShell commands run against this subscription.</span></span>
