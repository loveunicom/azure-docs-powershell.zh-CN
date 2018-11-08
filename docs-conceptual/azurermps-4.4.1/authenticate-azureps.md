---
title: 使用 Azure PowerShell 进行登录
description: 如何使用 Azure PowerShell 以用户、服务主体或 Azure 资源托管标识的形式登录。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: d3e467714b1a9e4840f2a34b57eabfa5a2c6eaec
ms.sourcegitcommit: 06f9206e025afa7207d4657c8f57c94ddb74817a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/07/2018
ms.locfileid: "51212040"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="c3340-103">使用 Azure PowerShell 进行登录</span><span class="sxs-lookup"><span data-stu-id="c3340-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="c3340-104">Azure PowerShell 支持多种身份验证方法。</span><span class="sxs-lookup"><span data-stu-id="c3340-104">Azure PowerShell supports multiple authentication methods.</span></span> <span data-ttu-id="c3340-105">最简单的入门方法是通过命令行以交互方式登录。</span><span class="sxs-lookup"><span data-stu-id="c3340-105">The simplest way to get started is to sign in interactively at the command line.</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="c3340-106">以交互方式登录</span><span class="sxs-lookup"><span data-stu-id="c3340-106">Sign in interactively</span></span>

<span data-ttu-id="c3340-107">若要以交互方式登录，请使用 [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount) cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c3340-107">To sign in interactively, use the [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount) cmdlet.</span></span>

```azurepowershell-interactive
Connect-AzureRmAccount
```

<span data-ttu-id="c3340-108">当运行时，此 cmdlet 将显示一个对话框，提示输入与你的 Azure 帐户关联的电子邮件地址和密码。</span><span class="sxs-lookup"><span data-stu-id="c3340-108">When run, this cmdlet will bring up a dialog box prompting you for your email address and password associated with your Azure account.</span></span> <span data-ttu-id="c3340-109">进行身份验证时，将为当前 PowerShell 会话保存该信息，对话框将关闭并且你可以访问所有 Azure PowerShell cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c3340-109">When you authenticate, that information is saved for the current PowerShell session, the dialog is closed, and you have access to all of the Azure PowerShell cmdlets.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c3340-110">从 Azure PowerShell 6.3.0 开始，只要你保持登录到 Windows，凭据将在多个 PowerShell 会话之间共享。</span><span class="sxs-lookup"><span data-stu-id="c3340-110">As of Azure PowerShell 6.3.0, your credentials are shared among multiple PowerShell sessions as long as you remain signed in to Windows.</span></span> <span data-ttu-id="c3340-111">有关详细信息，请参阅[持久保留凭据](context-persistence.md)。</span><span class="sxs-lookup"><span data-stu-id="c3340-111">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-with-a-service-principal"></a><span data-ttu-id="c3340-112">使用服务主体进行登录</span><span class="sxs-lookup"><span data-stu-id="c3340-112">Sign in with a service principal</span></span>

<span data-ttu-id="c3340-113">使用服务主体能够创建可用于处理资源的非交互式帐户。</span><span class="sxs-lookup"><span data-stu-id="c3340-113">Service principals provide a way for you to create non-interactive accounts that you can use to manipulate resources.</span></span> <span data-ttu-id="c3340-114">服务主体类似于可以使用 Azure Active Directory 向其应用规则的用户帐户。</span><span class="sxs-lookup"><span data-stu-id="c3340-114">Service principals are like user accounts to which you can apply rules using Azure Active Directory.</span></span> <span data-ttu-id="c3340-115">通过授予服务主体所需的最低权限，可以确保自动化脚本更加安全。</span><span class="sxs-lookup"><span data-stu-id="c3340-115">By granting the minimum permissions needed to a service principal, you can ensure your automation scripts are even more secure.</span></span>

<span data-ttu-id="c3340-116">如果需要创建要通过 Azure PowerShell 使用的服务主体，请参阅[使用 Azure PowerShell 创建 Azure 服务主体](create-azure-service-principal-azureps.md)。</span><span class="sxs-lookup"><span data-stu-id="c3340-116">If you need to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="c3340-117">若要使用服务主体进行登录，请将 `-ServicePrincipal` 参数与 `Connect-AzureRmAccount` cmdlet 一起使用。</span><span class="sxs-lookup"><span data-stu-id="c3340-117">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzureRmAccount` cmdlet.</span></span> <span data-ttu-id="c3340-118">你还将需要服务主体的应用程序 ID、登录凭据以及与服务主体关联的租户 ID。</span><span class="sxs-lookup"><span data-stu-id="c3340-118">You will also need the service princpal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="c3340-119">若要将服务主体的凭据获取为合适的对象，请使用 [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c3340-119">In order to get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="c3340-120">此 cmdlet 将显示一个对话框，可以在其中输入服务主体用户 ID 和密码。</span><span class="sxs-lookup"><span data-stu-id="c3340-120">This cmdlet will display a dialog box to enter the service principal user ID and password into.</span></span>

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-managed-identities-for-azure-resources"></a><span data-ttu-id="c3340-121">使用 Azure 资源的托管标识登录</span><span class="sxs-lookup"><span data-stu-id="c3340-121">Sign in using managed identities for Azure resources</span></span>

<span data-ttu-id="c3340-122">Azure 资源的托管标识是 Azure Active Directory 的一项功能。</span><span class="sxs-lookup"><span data-stu-id="c3340-122">Managed identities for Azure resources is a feature of Azure Active Directory.</span></span> <span data-ttu-id="c3340-123">可以使用托管标识服务主体登录，并获取仅限应用的访问令牌来访问其他资源。</span><span class="sxs-lookup"><span data-stu-id="c3340-123">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="c3340-124">托管标识只能在 Azure 云中运行的虚拟机上使用。</span><span class="sxs-lookup"><span data-stu-id="c3340-124">Managed identities are only available on virtual machines running in an Azure cloud.</span></span>

<span data-ttu-id="c3340-125">有关 Azure 资源的托管标识的详细信息，请参阅[如何在 Azure VM 上使用 Azure 资源托管标识来获取访问令牌](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token)。</span><span class="sxs-lookup"><span data-stu-id="c3340-125">For more information about managed identities for Azure resources, see [How to use managed identities for Azure resources on an Azure VM to acquire an access token](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span></span>

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="c3340-126">登录到其他云</span><span class="sxs-lookup"><span data-stu-id="c3340-126">Sign in to another Cloud</span></span>

<span data-ttu-id="c3340-127">Azure 云服务提供了遵循各个区域的数据处理法规的不同环境。</span><span class="sxs-lookup"><span data-stu-id="c3340-127">Azure cloud services provide different environments that adhere to the data-handling regulations of various regions.</span></span> <span data-ttu-id="c3340-128">如果你的 Azure 帐户在与这些区域之一关联的云中，则在登录时需要指定环境。</span><span class="sxs-lookup"><span data-stu-id="c3340-128">If your Azure account is in a cloud associated with one of these regions, you need to specify the environment when you sign in.</span></span> <span data-ttu-id="c3340-129">例如，如果帐户在中国云中，请使用以下命令登录：</span><span class="sxs-lookup"><span data-stu-id="c3340-129">For example, if you account is in the China cloud you sign on using the following command:</span></span>

```azurepowershell-interactive
Login-AzureRmAccount -EnvironmentName AzureChinaCloud
```

<span data-ttu-id="c3340-130">使用以下命令获取可用环境的列表：</span><span class="sxs-lookup"><span data-stu-id="c3340-130">Use the following command to get a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzureRmEnvironment | Select-Object Name
```

## <a name="learn-more-about-managing-azure-role-based-access"></a><span data-ttu-id="c3340-131">详细了解如何管理 Azure 基于角色的访问</span><span class="sxs-lookup"><span data-stu-id="c3340-131">Learn more about managing Azure role-based access</span></span>

<span data-ttu-id="c3340-132">有关 Azure 中的身份验证和订阅管理的详细信息，请参阅[管理帐户、订阅和管理角色](/azure/active-directory/role-based-access-control-configure)。</span><span class="sxs-lookup"><span data-stu-id="c3340-132">For more information about authentication and subscription management in Azure, see [Manage Accounts, Subscriptions, and Administrative Roles](/azure/active-directory/role-based-access-control-configure).</span></span>

<span data-ttu-id="c3340-133">用于角色管理的 Azure PowerShell cmdlet：</span><span class="sxs-lookup"><span data-stu-id="c3340-133">Azure PowerShell cmdlets for role management:</span></span>

* [<span data-ttu-id="c3340-134">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="c3340-134">Get-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleAssignment)
* [<span data-ttu-id="c3340-135">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="c3340-135">Get-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleDefinition)
* [<span data-ttu-id="c3340-136">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="c3340-136">New-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleAssignment)
* [<span data-ttu-id="c3340-137">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="c3340-137">New-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleDefinition)
* [<span data-ttu-id="c3340-138">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="c3340-138">Remove-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleAssignment)
* [<span data-ttu-id="c3340-139">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="c3340-139">Remove-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleDefinition)
* [<span data-ttu-id="c3340-140">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="c3340-140">Set-AzureRmRoleDefinition</span></span>](/powershell/moduel/AzureRM.Resources/Set-AzureRmRoleDefinition)
