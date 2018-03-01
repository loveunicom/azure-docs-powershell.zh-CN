---
title: "使用 Azure PowerShell 管理 Azure 订阅 | Microsoft Docs"
description: "使用 Azure PowerShell 管理 Azure 订阅"
keywords: "Azure PowerShell, 订阅"
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/30/2017
ms.openlocfilehash: 68d03ec8d1a86fb3b270d02a4697bbf9af847f2d
ms.sourcegitcommit: 7e77fe7ecd2112d6b4515517509c5c723e750e27
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/19/2018
---
# <a name="manage-multiple-azure-subscriptions"></a><span data-ttu-id="92272-104">管理多个 Azure 订阅</span><span class="sxs-lookup"><span data-stu-id="92272-104">Manage multiple Azure subscriptions</span></span>

<span data-ttu-id="92272-105">如果是 Azure 的新手，也许只有一个订阅。</span><span class="sxs-lookup"><span data-stu-id="92272-105">If you are brand new to Azure, you probably only have a single subscription.</span></span> <span data-ttu-id="92272-106">但如果使用 Azure 有一段时间，可能已创建了多个 Azure 订阅。</span><span class="sxs-lookup"><span data-stu-id="92272-106">But if you have been using Azure for a while, you may have created multiple Azure subscriptions.</span></span> <span data-ttu-id="92272-107">可将 Azure PowerShell 配置为针对特定的订阅执行命令。</span><span class="sxs-lookup"><span data-stu-id="92272-107">You can configure Azure PowerShell to execute commands against a particular subscription.</span></span>

1. <span data-ttu-id="92272-108">获取帐户中所有订阅的列表。</span><span class="sxs-lookup"><span data-stu-id="92272-108">Get a list of all subscriptions in your account.</span></span>

    ```powershell
    Get-AzureRmSubscription
    ```

    ```
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

2. <span data-ttu-id="92272-109">设置默认值。</span><span class="sxs-lookup"><span data-stu-id="92272-109">Set the default.</span></span>

    ```powershell
    Select-AzureRmSubscription -SubscriptionName "My Demos"
    ```

3. <span data-ttu-id="92272-110">通过运行 `Get-AzureRmContext` cmdlet 验证更改。</span><span class="sxs-lookup"><span data-stu-id="92272-110">Verify the change by running the `Get-AzureRmContext` cmdlet.</span></span>

    ```powershell
    Get-AzureRmContext
    ```

    ```
    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My Demos
    CurrentStorageAccount :
    ```

<span data-ttu-id="92272-111">设置默认订阅后，所有后续 Azure PowerShell 命令将针对此订阅运行。</span><span class="sxs-lookup"><span data-stu-id="92272-111">Once you set your default subscription, all subsequent Azure PowerShell commands run against this subscription.</span></span>