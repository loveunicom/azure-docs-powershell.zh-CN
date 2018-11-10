---
title: 使用 Azure PowerShell 创建 Azure 服务主体
description: 了解如何使用 Azure PowerShell 为应用或服务创建服务主体。
keywords: Azure PowerShell, Azure Active Directory, Azure Active Directory, AD, RBAC
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/09/2018
ms.openlocfilehash: 433a638187f024883c177457e420a759968fed9a
ms.sourcegitcommit: ac4b53bb42a25aae013a9d8cd9ae98ada9397274
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/08/2018
ms.locfileid: "51273831"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a>使用 Azure PowerShell 创建 Azure 服务主体

如果打算使用 Azure PowerShell 来管理应用或服务，应使用 Azure Active Directory (AAD) 服务主体而不是自己的凭据运行 PowerShell。 本文逐步讲解如何使用 Azure PowerShell 创建安全主体。

> [!NOTE]
> 也可以通过 Azure 门户创建服务主体。 有关详细信息，请参阅[使用门户创建可访问资源的 Active Directory 应用程序和服务主体](/azure/azure-resource-manager/resource-group-create-service-principal-portal)。

## <a name="what-is-a-service-principal"></a>什么是“服务主体”？

Azure 服务主体是用户创建的应用、服务和自动化工具用来访问特定 Azure 资源的安全标识。 可将其视为具有特定角色，并且权限受到严格控制的“用户标识”（用户名和密码，或者证书）。 与普通的用户标识不同，服务主体只需执行特定的操作。 如果只向它授予执行管理任务所需的最低权限级别，则可以提高安全性。

## <a name="verify-your-own-permission-level"></a>验证自己的权限级别

首先，在 Azure Active Directory 和 Azure 订阅中必须拥有足够的权限。 必须能够在 Active Directory 中创建应用并向服务主体分配角色。

检查帐户是否有适当权限的最简方法是使用门户。 请参阅[在门户中检查所需的权限](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions)。

## <a name="create-a-service-principal-for-your-app"></a>为应用创建服务主体

登录到 Azure 帐户后，可以创建服务主体。 必须使用以下方式之一来标识已部署的应用：

* 已部署的应用的唯一名称（例如以下示例中的“MyDemoWebApp”），或
* 应用程序 ID，即与已部署的应用、服务或对象关联的唯一 GUID

### <a name="get-information-about-your-application"></a>获取有关应用程序的信息

可以使用 `Get-AzureRmADApplication` cmdlet 获取有关应用程序的信息。

```azurepowershell-interactive
Get-AzureRmADApplication -DisplayNameStartWith MyDemoWebApp
```

```output
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

### <a name="create-a-service-principal-for-your-application"></a>为应用程序创建服务主体

可以使用 `New-AzureRmADServicePrincipal` cmdlet 创建服务主体。

```azurepowershell-interactive
Add-Type -Assembly System.Web
$password = [System.Web.Security.Membership]::GeneratePassword(16,3)
$securePassword = ConvertTo-SecureString -Force -AsPlainText -String $password
New-AzureRmADServicePrincipal -ApplicationId 00c01aaa-1603-49fc-b6df-b78c4e5138b4 -Password $securePassword
```

```output
DisplayName                    Type                           ObjectId
-----------                    ----                           --------
MyDemoWebApp                   ServicePrincipal               698138e7-d7b6-4738-a866-b4e3081a69e4
```

### <a name="get-information-about-the-service-principal"></a>获取有关服务主体的信息

```azurepowershell-interactive
$svcprincipal = Get-AzureRmADServicePrincipal -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
$svcprincipal | Select-Object *
```

```output
ServicePrincipalNames : {http://MyDemoWebApp, 00c01aaa-1603-49fc-b6df-b78c4e5138b4}
ApplicationId         : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
DisplayName           : MyDemoWebApp
Id                    : 698138e7-d7b6-4738-a866-b4e3081a69e4
Type                  : ServicePrincipal
```

### <a name="sign-in-using-the-service-principal"></a>使用服务主体登录

现在，可以使用提供的 *appId* 和*密码*，以应用的新服务主体身份登录。 还需要服务主体的租户 ID。 使用个人凭据登录到 Azure 时，会显示租户 ID。 若要使用服务主体登录，请使用以下命令：

```azurepowershell-interactive
$cred = Get-Credential -UserName $svcprincipal.ApplicationId -Message "Enter Password"
Connect-AzureRmAccount -Credential $cred -ServicePrincipal -TenantId XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

成功登录后，会看到如下所示的输出：

```output
Environment           : AzureCloud
Account               : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
SubscriptionId        :
SubscriptionName      :
CurrentStorageAccount :
```

祝贺你！ 现在可以使用这些凭据来运行应用。 接下来，需要调整服务主体的权限。

## <a name="managing-roles"></a>管理角色

> [!NOTE]
> Azure 基于角色的访问控制 (RBAC) 是定义和管理用户及服务主体的角色时使用的模型。 角色具有关联的权限集，这些权限确定主体可以读取、访问、写入或管理的资源。 有关 RBAC 和角色的详细信息，请参阅 [RBAC：内置角色](/azure/active-directory/role-based-access-built-in-roles)。

Azure PowerShell 提供以下 cmdlet 用于管理角色分配：

* [Get-AzureRmRoleAssignment](/powershell/module/azurerm.resources/get-azurermroleassignment)
* [New-AzureRmRoleAssignment](/powershell/module/azurerm.resources/new-azurermroleassignment)
* [Remove-AzureRmRoleAssignment](/powershell/module/azurerm.resources/remove-azurermroleassignment)

服务主体的默认角色是“参与者”。 由于该角色的权限比较广泛，根据应用与 Azure 服务之间的交互范围，该角色可能不是最合适的选择。
“读取者”角色受到严格的限制，可能非常适合用于只读的应用。 可以查看有关角色特定的权限的详细信息，或者如何通过 Azure 门户创建自定义角色。

本示例将“读取者”角色添加到前面的示例，并删除“参与者”角色：

```azurepowershell-interactive
New-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Reader
```

```output
RoleAssignmentId   : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG/providers/Microsoft.Authorization/roleAssignments/818892f2-d075-46a1-a3a2-3a4e1a12fcd5
Scope              : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG
DisplayName        : MyDemoWebApp
SignInName         :
RoleDefinitionName : Reader
RoleDefinitionId   : b24988ac-6180-42a0-ab88-20f7382dd24c
ObjectId           : 698138e7-d7b6-4738-a866-b4e3081a69e4
ObjectType         : ServicePrincipal
```

```azurepowershell-interactive
Remove-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Contributor
```

查看当前分配的角色：

```azurepowershell-interactive
Get-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
```

```output
RoleAssignmentId   : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG/providers/Microsoft.Authorization/roleAssignments/0906bbd8-9982-4c03-8dae-aeaae8b13f9e
Scope              : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG
DisplayName        : MyDemoWebApp
SignInName         :
RoleDefinitionName : Reader
RoleDefinitionId   : acdd72a7-3385-48ef-bd42-f606fba81ae7
ObjectId           : 698138e7-d7b6-4738-a866-b4e3081a69e4
ObjectType         : ServicePrincipal
```

用于角色管理的其他 Azure PowerShell cmdlet：

* [Get-AzureRmRoleDefinition](/powershell/module/azurerm.resources/Get-AzureRmRoleDefinition)
* [New-AzureRmRoleDefinition](/powershell/module/azurerm.resources/New-AzureRmRoleDefinition)
* [Remove-AzureRmRoleDefinition](/powershell/module/azurerm.resources/Remove-AzureRmRoleDefinition)
* [Set-AzureRmRoleDefinition](/powershell/module/azurerm.resources/Set-AzureRmRoleDefinition)

## <a name="change-the-credentials-of-the-security-principal"></a>更改安全主体的凭据

良好的安全做法是定期审查权限并更新密码。 此外，随着应用的变化，可能还需要管理和修改安全凭据。 例如，可以通过创建新密码并删除旧密码来更改服务主体的密码。

### <a name="add-a-new-password-for-the-service-principal"></a>为服务主体添加新密码

```azurepowershell-interactive
$password = [System.Web.Security.Membership]::GeneratePassword(16,3)
New-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp -Password $password
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
```

### <a name="get-a-list-of-credentials-for-the-service-principal"></a>获取主体服务的凭据列表

```azurepowershell-interactive
Get-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
5/5/2016 4:55:27 PM 5/5/2017 4:55:27 PM ca9d4846-4972-4c70-b6f5-a4effa60b9bc Password
```

### <a name="remove-the-old-password-from-the-service-principal"></a>删除服务主体的旧密码

```azurepowershell-interactive
Remove-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp -KeyId ca9d4846-4972-4c70-b6f5-a4effa60b9bc
```

```output
Confirm
Are you sure you want to remove credential with keyId '6f801c3e-6fcd-42b9-be8e-320b17ba1d36' for
service principal objectId '698138e7-d7b6-4738-a866-b4e3081a69e4'.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

### <a name="verify-the-list-of-credentials-for-the-service-principal"></a>验证主体服务的凭据列表

```azurepowershell-interactive
Get-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
```
