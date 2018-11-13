---
title: 使用 Azure PowerShell 进行登录
description: 如何使用 Azure PowerShell 以用户、服务主体或 Azure 资源托管标识的形式登录。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/09/2018
ms.openlocfilehash: 6a42217c47c1e5101a708da87c15fc14004f2069
ms.sourcegitcommit: ac4b53bb42a25aae013a9d8cd9ae98ada9397274
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/08/2018
ms.locfileid: "51275412"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="01945-103">使用 Azure PowerShell 进行登录</span><span class="sxs-lookup"><span data-stu-id="01945-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="01945-104">Azure PowerShell 支持多种身份验证方法。</span><span class="sxs-lookup"><span data-stu-id="01945-104">Azure PowerShell supports several authentication methods.</span></span> <span data-ttu-id="01945-105">最简单的入门方法是通过命令行以交互方式登录。</span><span class="sxs-lookup"><span data-stu-id="01945-105">The simplest way to get started is to sign in interactively at the command line.</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="01945-106">以交互方式登录</span><span class="sxs-lookup"><span data-stu-id="01945-106">Sign in interactively</span></span>

<span data-ttu-id="01945-107">若要以交互方式登录，请使用 [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount) cmdlet。</span><span class="sxs-lookup"><span data-stu-id="01945-107">To sign in interactively, use the [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount) cmdlet.</span></span>

```azurepowershell-interactive
Connect-AzureRmAccount
```

<span data-ttu-id="01945-108">当运行时，此 cmdlet 将显示一个对话框，提示输入与你的 Azure 帐户关联的电子邮件地址和密码。</span><span class="sxs-lookup"><span data-stu-id="01945-108">When run, this cmdlet will bring up a dialog box prompting you for your email address and password associated with your Azure account.</span></span> <span data-ttu-id="01945-109">在当前 PowerShell 会话期间，此身份验证将持续进行。</span><span class="sxs-lookup"><span data-stu-id="01945-109">This authentication lasts for the current PowerShell session.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="01945-110">从 Azure PowerShell 6.3.0 开始，只要你保持登录到 Windows，凭据将在多个 PowerShell 会话之间共享。</span><span class="sxs-lookup"><span data-stu-id="01945-110">As of Azure PowerShell 6.3.0, your credentials are shared among multiple PowerShell sessions as long as you remain signed in to Windows.</span></span> <span data-ttu-id="01945-111">有关详细信息，请参阅[持久保留凭据](context-persistence.md)。</span><span class="sxs-lookup"><span data-stu-id="01945-111">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-with-a-service-principal"></a><span data-ttu-id="01945-112">使用服务主体进行登录</span><span class="sxs-lookup"><span data-stu-id="01945-112">Sign in with a service principal</span></span>

<span data-ttu-id="01945-113">服务主体属于非交互式 Azure 帐户。</span><span class="sxs-lookup"><span data-stu-id="01945-113">Service principals are non-interactive Azure accounts.</span></span> <span data-ttu-id="01945-114">与其他用户帐户一样，服务主体的权限通过 Azure Active Directory 进行管理。</span><span class="sxs-lookup"><span data-stu-id="01945-114">Like other user accounts, their permissions are managed with Azure Active Directory.</span></span> <span data-ttu-id="01945-115">只向服务主体授予它所需的权限可让自动化脚本保持安全。</span><span class="sxs-lookup"><span data-stu-id="01945-115">By granting a service principal only the permissions it needs, your automation scripts stay secure.</span></span>

<span data-ttu-id="01945-116">若要了解如何创建与 Azure PowerShell 配合使用的服务主体，请参阅[使用 Azure PowerShell 创建 Azure 服务主体](create-azure-service-principal-azureps.md)。</span><span class="sxs-lookup"><span data-stu-id="01945-116">To learn how to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="01945-117">若要使用服务主体进行登录，请将 `-ServicePrincipal` 参数与 `Connect-AzureRmAccount` cmdlet 一起使用。</span><span class="sxs-lookup"><span data-stu-id="01945-117">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzureRmAccount` cmdlet.</span></span> <span data-ttu-id="01945-118">此外，还需要服务主体的应用程序 ID、登录凭据以及与服务主体关联的租户 ID。</span><span class="sxs-lookup"><span data-stu-id="01945-118">You'll also need the service principal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="01945-119">若要获取用作相应对象的服务主体凭据，请使用 [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet。</span><span class="sxs-lookup"><span data-stu-id="01945-119">To get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="01945-120">此 cmdlet 将显示一个对话框，可以在其中输入服务主体用户 ID 和密码。</span><span class="sxs-lookup"><span data-stu-id="01945-120">This cmdlet will display a dialog box to enter the service principal user ID and password into.</span></span>

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-an-azure-managed-service-identity"></a><span data-ttu-id="01945-121">使用 Azure 托管服务标识登录</span><span class="sxs-lookup"><span data-stu-id="01945-121">Sign in using an Azure Managed Service Identity</span></span>

<span data-ttu-id="01945-122">Azure 资源的托管标识是 Azure Active Directory 的一项功能。</span><span class="sxs-lookup"><span data-stu-id="01945-122">Managed identities for Azure resources is a feature of Azure Active Directory.</span></span> <span data-ttu-id="01945-123">可以使用托管标识服务主体登录，并获取仅限应用的访问令牌来访问其他资源。</span><span class="sxs-lookup"><span data-stu-id="01945-123">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="01945-124">托管标识只能在 Azure 云中运行的虚拟机上使用。</span><span class="sxs-lookup"><span data-stu-id="01945-124">Managed identities are only available on virtual machines running in an Azure cloud.</span></span>

<span data-ttu-id="01945-125">有关 Azure 资源的托管标识的详细信息，请参阅[如何在 Azure VM 上使用 Azure 资源托管标识来获取访问令牌](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token)。</span><span class="sxs-lookup"><span data-stu-id="01945-125">For more information about managed identities for Azure resources, see [How to use managed identities for Azure resources on an Azure VM to acquire an access token](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span></span>

## <a name="sign-in-as-a-cloud-solution-provider-csp"></a><span data-ttu-id="01945-126">以云解决方案提供商 (CSP) 身份登录</span><span class="sxs-lookup"><span data-stu-id="01945-126">Sign in as a Cloud Solution Provider (CSP)</span></span>

<span data-ttu-id="01945-127">[云解决方案提供商 (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/) 登录需要使用 `-TenantId`。</span><span class="sxs-lookup"><span data-stu-id="01945-127">A [Cloud Solution Provider (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/) sign-in requires the use of `-TenantId`.</span></span> <span data-ttu-id="01945-128">通常情况下，此参数可以采用租户 ID 或域名的形式提供。</span><span class="sxs-lookup"><span data-stu-id="01945-128">Normally, this parameter can be provided as either a tenant ID or a domain name.</span></span> <span data-ttu-id="01945-129">但是，对于 CSP 登录，必须为其提供**租户 ID**。</span><span class="sxs-lookup"><span data-stu-id="01945-129">However, for CSP sign-in, it must be provided a **tenant ID**.</span></span>

```azurepowershell-interactive
Connect-AzureRmAccount -TenantId 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="01945-130">登录到其他云</span><span class="sxs-lookup"><span data-stu-id="01945-130">Sign in to another Cloud</span></span>

<span data-ttu-id="01945-131">Azure 云服务提供符合区域数据处理法规的环境。</span><span class="sxs-lookup"><span data-stu-id="01945-131">Azure cloud services offer environments compliant with regional data-handling regulations.</span></span>
<span data-ttu-id="01945-132">对于区域云中的帐户，请在登录时使用 `-Environment` 参数设置环境。</span><span class="sxs-lookup"><span data-stu-id="01945-132">For accounts in a regional cloud, set the environment when you sign in with the `-Environment` argument.</span></span>
<span data-ttu-id="01945-133">例如，如果你的帐户位于中国云中：</span><span class="sxs-lookup"><span data-stu-id="01945-133">For example, if your account is in the China cloud:</span></span>

```azurepowershell-interactive
Connect-AzureRmAccount -Environment AzureChinaCloud
```

<span data-ttu-id="01945-134">以下命令获取可用环境的列表：</span><span class="sxs-lookup"><span data-stu-id="01945-134">The following command gets a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzureRmEnvironment | Select-Object Name
```

## <a name="learn-more-about-managing-azure-role-based-access"></a><span data-ttu-id="01945-135">详细了解如何管理 Azure 基于角色的访问</span><span class="sxs-lookup"><span data-stu-id="01945-135">Learn more about managing Azure role-based access</span></span>

<span data-ttu-id="01945-136">有关 Azure 中的身份验证和订阅管理的详细信息，请参阅[管理帐户、订阅和管理角色](/azure/active-directory/role-based-access-control-configure)。</span><span class="sxs-lookup"><span data-stu-id="01945-136">For more information about authentication and subscription management in Azure, see [Manage Accounts, Subscriptions, and Administrative Roles](/azure/active-directory/role-based-access-control-configure).</span></span>

<span data-ttu-id="01945-137">用于角色管理的 Azure PowerShell cmdlet：</span><span class="sxs-lookup"><span data-stu-id="01945-137">Azure PowerShell cmdlets for role management:</span></span>

* [<span data-ttu-id="01945-138">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="01945-138">Get-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleAssignment)
* [<span data-ttu-id="01945-139">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="01945-139">Get-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleDefinition)
* [<span data-ttu-id="01945-140">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="01945-140">New-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleAssignment)
* [<span data-ttu-id="01945-141">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="01945-141">New-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleDefinition)
* [<span data-ttu-id="01945-142">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="01945-142">Remove-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleAssignment)
* [<span data-ttu-id="01945-143">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="01945-143">Remove-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleDefinition)
* [<span data-ttu-id="01945-144">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="01945-144">Set-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Set-AzureRmRoleDefinition)
