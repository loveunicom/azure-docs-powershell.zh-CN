---
title: "使用 Azure PowerShell 创建 Azure 服务主体"
description: "了解如何使用 Azure PowerShell 为应用或服务创建服务主体。"
keywords: Azure PowerShell, Azure Active Directory, Azure Active Directory, AD, RBAC
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: 6eda2d2a729331b212938aa2681d0188a25b734a
ms.sourcegitcommit: c42c7176276ec4e1cc3360a93e6b15d32083bf9f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/14/2017
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a><span data-ttu-id="fb4f3-104">使用 Azure PowerShell 创建 Azure 服务主体</span><span class="sxs-lookup"><span data-stu-id="fb4f3-104">Create an Azure service principal with Azure PowerShell</span></span>

<span data-ttu-id="fb4f3-105">如果打算使用 Azure PowerShell 来管理应用或服务，应使用 Azure Active Directory (AAD) 服务主体而不是自己的凭据运行 PowerShell。</span><span class="sxs-lookup"><span data-stu-id="fb4f3-105">If you plan to manage your app or service with Azure PowerShell, you should run it under an Azure Active Directory (AAD) service principal, rather than your own credentials.</span></span> <span data-ttu-id="fb4f3-106">本主题逐步讲解如何使用 Azure PowerShell 创建安全主体。</span><span class="sxs-lookup"><span data-stu-id="fb4f3-106">This topic steps you through creating a security principal with Azure PowerShell.</span></span>

> [!NOTE]
> <span data-ttu-id="fb4f3-107">也可以通过 Azure 门户创建服务主体。</span><span class="sxs-lookup"><span data-stu-id="fb4f3-107">You can also create a service principal through the Azure portal.</span></span> <span data-ttu-id="fb4f3-108">有关详细信息，请参阅[使用门户创建可访问资源的 Active Directory 应用程序和服务主体](/azure/azure-resource-manager/resource-group-create-service-principal-portal)。</span><span class="sxs-lookup"><span data-stu-id="fb4f3-108">Read [Use portal to create Active Directory application and service principal that can access resources](/azure/azure-resource-manager/resource-group-create-service-principal-portal) for more details.</span></span>

## <a name="what-is-a-service-principal"></a><span data-ttu-id="fb4f3-109">什么是“服务主体”？</span><span class="sxs-lookup"><span data-stu-id="fb4f3-109">What is a 'service principal'?</span></span>

<span data-ttu-id="fb4f3-110">Azure 服务主体是用户创建的应用、服务和自动化工具用来访问特定 Azure 资源的安全标识。</span><span class="sxs-lookup"><span data-stu-id="fb4f3-110">An Azure service principal is a security identity used by user-created apps, services, and automation tools to access specific Azure resources.</span></span> <span data-ttu-id="fb4f3-111">可将其视为具有特定角色，并且权限受到严格控制的“用户标识”（用户名和密码，或者证书）。</span><span class="sxs-lookup"><span data-stu-id="fb4f3-111">Think of it as a 'user identity' (username and password or certificate) with a specific role, and tightly controlled permissions.</span></span> <span data-ttu-id="fb4f3-112">与普通的用户标识不同，它只需能够完成特定的任务。</span><span class="sxs-lookup"><span data-stu-id="fb4f3-112">It only needs to be able to do specific things, unlike a general user identity.</span></span> <span data-ttu-id="fb4f3-113">如果只向它授予执行管理任务所需的最低权限级别，则可以提高安全性。</span><span class="sxs-lookup"><span data-stu-id="fb4f3-113">It improves security if you only grant it the minimum permissions level needed to perform its management tasks.</span></span>

## <a name="verify-your-own-permission-level"></a><span data-ttu-id="fb4f3-114">验证自己的权限级别</span><span class="sxs-lookup"><span data-stu-id="fb4f3-114">Verify your own permission level</span></span>

<span data-ttu-id="fb4f3-115">首先，在 Azure Active Directory 和 Azure 订阅中必须拥有足够的权限。</span><span class="sxs-lookup"><span data-stu-id="fb4f3-115">First, you must have sufficient permissions in both your Azure Active Directory and your Azure subscription.</span></span> <span data-ttu-id="fb4f3-116">具体而言，必须能够在 Active Directory 中创建应用并向服务主体分配角色。</span><span class="sxs-lookup"><span data-stu-id="fb4f3-116">Specifically, you must be able to create an app in the Active Directory, and assign a role to the service principal.</span></span>

<span data-ttu-id="fb4f3-117">检查帐户是否有足够权限的最简方法是使用门户。</span><span class="sxs-lookup"><span data-stu-id="fb4f3-117">The easiest way to check whether your account has adequate permissions is through the portal.</span></span> <span data-ttu-id="fb4f3-118">请参阅[在门户中检查所需的权限](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions)。</span><span class="sxs-lookup"><span data-stu-id="fb4f3-118">See [Check required permission in portal](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions).</span></span>

## <a name="create-a-service-principal-for-your-app"></a><span data-ttu-id="fb4f3-119">为应用创建服务主体</span><span class="sxs-lookup"><span data-stu-id="fb4f3-119">Create a service principal for your app</span></span>

<span data-ttu-id="fb4f3-120">登录到 Azure 帐户后，可创建服务主体。</span><span class="sxs-lookup"><span data-stu-id="fb4f3-120">Once you are signed into your Azure account, you can create the service principal.</span></span> <span data-ttu-id="fb4f3-121">必须使用以下方式之一来标识已部署的应用：</span><span class="sxs-lookup"><span data-stu-id="fb4f3-121">You must have one of the following ways to identify your deployed app:</span></span>

* <span data-ttu-id="fb4f3-122">已部署的应用的唯一名称（例如以下示例中的“MyDemoWebApp”），或</span><span class="sxs-lookup"><span data-stu-id="fb4f3-122">The unique name of your deployed app, such as "MyDemoWebApp" in the following examples, or</span></span>
* <span data-ttu-id="fb4f3-123">应用程序 ID，即与已部署的应用、服务或对象关联的唯一 GUID</span><span class="sxs-lookup"><span data-stu-id="fb4f3-123">the Application ID, the unique GUID associated with your deployed app, service, or object</span></span>

### <a name="get-information-about-your-application"></a><span data-ttu-id="fb4f3-124">获取有关应用程序的信息</span><span class="sxs-lookup"><span data-stu-id="fb4f3-124">Get information about your application</span></span>

<span data-ttu-id="fb4f3-125">可以使用 `Get-AzureRmADApplication` cmdlet 发现有关应用程序的信息。</span><span class="sxs-lookup"><span data-stu-id="fb4f3-125">The `Get-AzureRmADApplication` cmdlet can be used to discover information about your application.</span></span>

```powershell
Get-AzureRmADApplication -DisplayNameStartWith MyDemoWebApp
```

```
DisplayName             : MyDemoWebApp
ObjectId                : 775f64cd-0ec8-4b9b-b69a-8b8946022d9f
IdentifierUris          : {http://MyDemoWebApp}
HomePage                : http://www.contoso.com
Type                    : Application
ApplicationId           : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
AvailableToOtherTenants : False
AppPermissions          :
ReplyUrls               : {}
```

### <a name="create-a-service-principal-for-your-application"></a><span data-ttu-id="fb4f3-126">为应用程序创建服务主体</span><span class="sxs-lookup"><span data-stu-id="fb4f3-126">Create a service principal for your application</span></span>

<span data-ttu-id="fb4f3-127">可以使用 `New-AzureRmADServicePrincipal` cmdlet 创建服务主体。</span><span class="sxs-lookup"><span data-stu-id="fb4f3-127">The `New-AzureRmADServicePrincipal` cmdlet is used to create the service principal.</span></span>

```powershell
Add-Type -Assembly System.Web
$password = [System.Web.Security.Membership]::GeneratePassword(16,3)
New-AzureRmADServicePrincipal -ApplicationId 00c01aaa-1603-49fc-b6df-b78c4e5138b4 -Password $password
```

```
DisplayName                    Type                           ObjectId
-----------                    ----                           --------
MyDemoWebApp                   ServicePrincipal               698138e7-d7b6-4738-a866-b4e3081a69e4
```

### <a name="get-information-about-the-service-principal"></a><span data-ttu-id="fb4f3-128">获取有关服务主体的信息</span><span class="sxs-lookup"><span data-stu-id="fb4f3-128">Get information about the service principal</span></span>

```powershell
$svcprincipal = Get-AzureRmADServicePrincipal -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
$svcprincipal | Select-Object *
```

```
ServicePrincipalNames : {http://MyDemoWebApp, 00c01aaa-1603-49fc-b6df-b78c4e5138b4}
ApplicationId         : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
DisplayName           : MyDemoWebApp
Id                    : 698138e7-d7b6-4738-a866-b4e3081a69e4
Type                  : ServicePrincipal
```

### <a name="sign-in-using-the-service-principal"></a><span data-ttu-id="fb4f3-129">使用服务主体登录</span><span class="sxs-lookup"><span data-stu-id="fb4f3-129">Sign in using the service principal</span></span>

<span data-ttu-id="fb4f3-130">现在，可以使用提供的 *appId* 和*密码*，以应用的新服务主体身份登录。</span><span class="sxs-lookup"><span data-stu-id="fb4f3-130">You can now sign in as the new service principal for your app using the *appId* and *password* you provided.</span></span> <span data-ttu-id="fb4f3-131">需要提供帐户的租户 ID。</span><span class="sxs-lookup"><span data-stu-id="fb4f3-131">You need to supply the Tenant Id for your account.</span></span> <span data-ttu-id="fb4f3-132">使用个人凭据登录到 Azure 时，会显示租户 ID。</span><span class="sxs-lookup"><span data-stu-id="fb4f3-132">Your Tenant Id is displayed when you sign into Azure with your personal credentials.</span></span>

```powershell
$cred = Get-Credential -UserName $svcprincipal.ApplicationId -Message "Enter Password"
Login-AzureRmAccount -Credential $cred -ServicePrincipal -TenantId XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

<span data-ttu-id="fb4f3-133">请通过新的 PowerShell 会话运行此命令。</span><span class="sxs-lookup"><span data-stu-id="fb4f3-133">Run this command from a new PowerShell session.</span></span> <span data-ttu-id="fb4f3-134">成功登录后，会看到如下所示的输出：</span><span class="sxs-lookup"><span data-stu-id="fb4f3-134">After a successfully signing on you see output something like this:</span></span>

```
Environment           : AzureCloud
Account               : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
SubscriptionId        :
SubscriptionName      :
CurrentStorageAccount :
```

<span data-ttu-id="fb4f3-135">祝贺你！</span><span class="sxs-lookup"><span data-stu-id="fb4f3-135">Congratulations!</span></span> <span data-ttu-id="fb4f3-136">现在可以使用这些凭据来运行应用。</span><span class="sxs-lookup"><span data-stu-id="fb4f3-136">You can use these credentials to run your app.</span></span> <span data-ttu-id="fb4f3-137">接下来，需要调整服务主体的权限。</span><span class="sxs-lookup"><span data-stu-id="fb4f3-137">Next, you need to adjust the permissions of the service principal.</span></span>

## <a name="managing-roles"></a><span data-ttu-id="fb4f3-138">管理角色</span><span class="sxs-lookup"><span data-stu-id="fb4f3-138">Managing roles</span></span>

> [!NOTE]
> <span data-ttu-id="fb4f3-139">Azure 基于角色的访问控制 (RBAC) 是定义和管理用户及服务主体的角色时使用的模型。</span><span class="sxs-lookup"><span data-stu-id="fb4f3-139">Azure Role-Based Access Control (RBAC) is a model for defining and managing roles for user and service principals.</span></span> <span data-ttu-id="fb4f3-140">角色具有关联的权限集，这些权限确定主体可以读取、访问、写入或管理的资源。</span><span class="sxs-lookup"><span data-stu-id="fb4f3-140">Roles have sets of permissions associated with them, which determine the resources a principal can read, access, write, or manage.</span></span> <span data-ttu-id="fb4f3-141">有关 RBAC 和角色的详细信息，请参阅 [RBAC：内置角色](/azure/active-directory/role-based-access-built-in-roles)。</span><span class="sxs-lookup"><span data-stu-id="fb4f3-141">For more information on RBAC and roles, see [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles).</span></span>

<span data-ttu-id="fb4f3-142">Azure PowerShell 提供以下 cmdlet 用于管理角色分配：</span><span class="sxs-lookup"><span data-stu-id="fb4f3-142">Azure PowerShell provides the following cmdlets to manage role assignments:</span></span>

* [<span data-ttu-id="fb4f3-143">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="fb4f3-143">Get-AzureRmRoleAssignment</span></span>](/powershell/module/azurerm.resources/get-azurermroleassignment)
* [<span data-ttu-id="fb4f3-144">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="fb4f3-144">New-AzureRmRoleAssignment</span></span>](/powershell/module/azurerm.resources/new-azurermroleassignment)
* [<span data-ttu-id="fb4f3-145">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="fb4f3-145">Remove-AzureRmRoleAssignment</span></span>](/powershell/module/azurerm.resources/remove-azurermroleassignment)

<span data-ttu-id="fb4f3-146">服务主体的默认角色是“参与者”。</span><span class="sxs-lookup"><span data-stu-id="fb4f3-146">The default role for a service principal is **Contributor**.</span></span> <span data-ttu-id="fb4f3-147">由于该角色的权限比较广泛，根据应用与 Azure 服务之间的交互范围，该角色可能不是最合适的选择。</span><span class="sxs-lookup"><span data-stu-id="fb4f3-147">It may not be the best choice depending on the scope of your app's interactions with Azure services, given its broad permissions.</span></span>
<span data-ttu-id="fb4f3-148">“读取者”角色受到严格的限制，可能非常适合用于只读的应用。</span><span class="sxs-lookup"><span data-stu-id="fb4f3-148">The **Reader** role is more restrictive and can be a good choice for read-only apps.</span></span> <span data-ttu-id="fb4f3-149">可以查看有关角色特定的权限的详细信息，或者如何通过 Azure 门户创建自定义角色。</span><span class="sxs-lookup"><span data-stu-id="fb4f3-149">You can view details on role-specific permissions or create custom ones through the Azure portal.</span></span>

<span data-ttu-id="fb4f3-150">本示例将“读取者”角色添加到前面的示例，并删除“参与者”角色：</span><span class="sxs-lookup"><span data-stu-id="fb4f3-150">In this example, we add the **Reader** role to our prior example, and delete the **Contributor** one:</span></span>

```powershell
New-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Reader
```

```
RoleAssignmentId   : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG/providers/Microsoft.Authorization/roleAssignments/818892f2-d075-46a1-a3a2-3a4e1a12fcd5
Scope              : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG
DisplayName        : MyDemoWebApp
SignInName         :
RoleDefinitionName : Reader
RoleDefinitionId   : b24988ac-6180-42a0-ab88-20f7382dd24c
ObjectId           : 698138e7-d7b6-4738-a866-b4e3081a69e4
ObjectType         : ServicePrincipal
```

```powershell
Remove-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Contributor
```

<span data-ttu-id="fb4f3-151">查看当前分配的角色：</span><span class="sxs-lookup"><span data-stu-id="fb4f3-151">To view the current roles assigned:</span></span>

```powershell
Get-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
```

```
RoleAssignmentId   : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG/providers/Microsoft.Authorization/roleAssignments/0906bbd8-9982-4c03-8dae-aeaae8b13f9e
Scope              : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG
DisplayName        : MyDemoWebApp
SignInName         :
RoleDefinitionName : Reader
RoleDefinitionId   : acdd72a7-3385-48ef-bd42-f606fba81ae7
ObjectId           : 698138e7-d7b6-4738-a866-b4e3081a69e4
ObjectType         : ServicePrincipal
```

<span data-ttu-id="fb4f3-152">用于角色管理的其他 Azure PowerShell cmdlet：</span><span class="sxs-lookup"><span data-stu-id="fb4f3-152">Other Azure PowerShell cmdlets for role management:</span></span>

* [<span data-ttu-id="fb4f3-153">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="fb4f3-153">Get-AzureRmRoleDefinition</span></span>](/powershell/module/azurerm.resources/Get-AzureRmRoleDefinition)
* [<span data-ttu-id="fb4f3-154">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="fb4f3-154">New-AzureRmRoleDefinition</span></span>](/powershell/module/azurerm.resources/New-AzureRmRoleDefinition)
* [<span data-ttu-id="fb4f3-155">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="fb4f3-155">Remove-AzureRmRoleDefinition</span></span>](/powershell/module/azurerm.resources/Remove-AzureRmRoleDefinition)
* [<span data-ttu-id="fb4f3-156">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="fb4f3-156">Set-AzureRmRoleDefinition</span></span>](/powershell/module/azurerm.resources/Set-AzureRmRoleDefinition)

## <a name="change-the-credentials-of-the-security-principal"></a><span data-ttu-id="fb4f3-157">更改安全主体的凭据</span><span class="sxs-lookup"><span data-stu-id="fb4f3-157">Change the credentials of the security principal</span></span>

<span data-ttu-id="fb4f3-158">良好的安全做法是定期审查权限并更新密码。</span><span class="sxs-lookup"><span data-stu-id="fb4f3-158">It's a good security practice to review the permissions and update the password regularly.</span></span> <span data-ttu-id="fb4f3-159">此外，随着应用的变化，可能还需要管理和修改安全凭据。</span><span class="sxs-lookup"><span data-stu-id="fb4f3-159">You may also want to manage and modify the security credentials as your app changes.</span></span> <span data-ttu-id="fb4f3-160">例如，可以通过创建新密码并删除旧密码来更改服务主体的密码。</span><span class="sxs-lookup"><span data-stu-id="fb4f3-160">For example, we can change the password of the service principal by creating a new password and removing the old one.</span></span>

### <a name="add-a-new-password-for-the-service-principal"></a><span data-ttu-id="fb4f3-161">为服务主体添加新密码</span><span class="sxs-lookup"><span data-stu-id="fb4f3-161">Add a new password for the service principal</span></span>

```powershell
$password = [System.Web.Security.Membership]::GeneratePassword(16,3)
New-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp -Password $password
```

```
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
```

### <a name="get-a-list-of-credentials-for-the-service-principal"></a><span data-ttu-id="fb4f3-162">获取主体服务的凭据列表</span><span class="sxs-lookup"><span data-stu-id="fb4f3-162">Get a list of credentials for the service principal</span></span>

```powershell
Get-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
5/5/2016 4:55:27 PM 5/5/2017 4:55:27 PM ca9d4846-4972-4c70-b6f5-a4effa60b9bc Password
```

### <a name="remove-the-old-password-from-the-service-principal"></a><span data-ttu-id="fb4f3-163">删除服务主体的旧密码</span><span class="sxs-lookup"><span data-stu-id="fb4f3-163">Remove the old password from the service principal</span></span>

```powershell
Remove-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp -KeyId ca9d4846-4972-4c70-b6f5-a4effa60b9bc
```

```
Confirm
Are you sure you want to remove credential with keyId '6f801c3e-6fcd-42b9-be8e-320b17ba1d36' for
service principal objectId '698138e7-d7b6-4738-a866-b4e3081a69e4'.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

### <a name="verify-the-list-of-credentials-for-the-service-principal"></a><span data-ttu-id="fb4f3-164">验证主体服务的凭据列表</span><span class="sxs-lookup"><span data-stu-id="fb4f3-164">Verify the list of credentials for the service principal</span></span>

```powershell
Get-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
```
