---
title: 使用 Azure PowerShell 进行登录
description: 如何使用 Azure PowerShell 以用户、服务主体或 Azure 资源托管标识的形式登录。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/09/2018
ms.openlocfilehash: 2a118e1aa8b6755ef5769f44429427d22532780d
ms.sourcegitcommit: a749eb729f583c9d0dd86141bbd04984d77ae9ab
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/11/2018
ms.locfileid: "48882065"
---
# <a name="sign-in-with-azure-powershell"></a>使用 Azure PowerShell 进行登录

Azure PowerShell 支持多种身份验证方法。 最简单的入门方法是通过命令行以交互方式登录。

## <a name="sign-in-interactively"></a>以交互方式登录

若要以交互方式登录，请使用 [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount) cmdlet。

```azurepowershell
Connect-AzureRmAccount
```

当运行时，此 cmdlet 将显示一个对话框，提示输入与你的 Azure 帐户关联的电子邮件地址和密码。 在当前 PowerShell 会话期间，此身份验证将持续进行。

> [!IMPORTANT]
> 从 Azure PowerShell 6.3.0 开始，只要你保持登录到 Windows，凭据将在多个 PowerShell 会话之间共享。 有关详细信息，请参阅[持久保留凭据](context-persistence.md)。

## <a name="sign-in-with-a-service-principal"></a>使用服务主体进行登录

服务主体属于非交互式 Azure 帐户。 与其他用户帐户一样，服务主体的权限通过 Azure Active Directory 进行管理。 只向服务主体授予它所需的权限可让自动化脚本保持安全。

若要了解如何创建与 Azure PowerShell 配合使用的服务主体，请参阅[使用 Azure PowerShell 创建 Azure 服务主体](create-azure-service-principal-azureps.md)。

若要使用服务主体进行登录，请将 `-ServicePrincipal` 参数与 `Connect-AzureRmAccount` cmdlet 一起使用。 此外，还需要服务主体的应用程序 ID、登录凭据以及与服务主体关联的租户 ID。 若要获取用作相应对象的服务主体凭据，请使用 [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet。 此 cmdlet 将显示一个对话框，可以在其中输入服务主体用户 ID 和密码。

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-an-azure-managed-service-identity"></a>使用 Azure 托管服务标识登录

Azure 资源的托管标识是 Azure Active Directory 的一项功能。 可以使用托管标识服务主体登录，并获取仅限应用的访问令牌来访问其他资源。 托管标识只能在 Azure 云中运行的虚拟机上使用。

有关 Azure 资源的托管标识的详细信息，请参阅[如何在 Azure VM 上使用 Azure 资源托管标识来获取访问令牌](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token)。

## <a name="sign-in-to-another-cloud"></a>登录到其他云

Azure 云服务提供符合区域数据处理法规的环境。
对于区域云中的帐户，请在登录时使用 `-Environment` 参数设置环境。
例如，如果你的帐户位于中国云中：

```azurepowershell-interactive
Connect-AzureRmAccount -Environment AzureChinaCloud
```

以下命令获取可用环境的列表：

```azurepowershell-interactive
Get-AzureRmEnvironment | Select-Object Name
```

## <a name="learn-more-about-managing-azure-role-based-access"></a>详细了解如何管理 Azure 基于角色的访问

有关 Azure 中的身份验证和订阅管理的详细信息，请参阅[管理帐户、订阅和管理角色](/azure/active-directory/role-based-access-control-configure)。

用于角色管理的 Azure PowerShell cmdlet：

* [Get-AzureRmRoleAssignment](/powershell/module/AzureRM.Resources/Get-AzureRmRoleAssignment)
* [Get-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/Get-AzureRmRoleDefinition)
* [New-AzureRmRoleAssignment](/powershell/module/AzureRM.Resources/New-AzureRmRoleAssignment)
* [New-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/New-AzureRmRoleDefinition)
* [Remove-AzureRmRoleAssignment](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleAssignment)
* [Remove-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleDefinition)
* [Set-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/Set-AzureRmRoleDefinition)
