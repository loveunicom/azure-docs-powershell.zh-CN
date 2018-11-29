---
title: 使用 Azure PowerShell 进行登录
description: 如何使用 Azure PowerShell 以用户、服务主体或 Azure 资源托管标识的形式登录。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: 9a93145f2abeea466a739775ca8ae7e337e78166
ms.sourcegitcommit: 558436c824d9b59731aa9b963cdc8df4dea932e7
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/29/2018
ms.locfileid: "52587612"
---
# <a name="sign-in-with-azure-powershell"></a>使用 Azure PowerShell 进行登录

Azure PowerShell 支持多种身份验证方法。 最简单的入门方法是通过命令行以交互方式登录。

## <a name="sign-in-interactively"></a>以交互方式登录

若要以交互方式登录，请使用 [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount) cmdlet。

```azurepowershell-interactive
Connect-AzureRmAccount
```

当运行时，此 cmdlet 将显示一个对话框，提示输入与你的 Azure 帐户关联的电子邮件地址和密码。 进行身份验证时，将为当前 PowerShell 会话保存该信息，对话框将关闭并且你可以访问所有 Azure PowerShell cmdlet。

> [!IMPORTANT]
> 此登录仅适用于当前 PowerShell 会话。 若要在多个会话之间持久保留身份验证，请参阅有关[持久性凭据](context-persistence.md)的文章。

## <a name="sign-in-with-a-service-principal"></a>使用服务主体进行登录

使用服务主体能够创建可用于处理资源的非交互式帐户。 服务主体类似于可以使用 Azure Active Directory 向其应用规则的用户帐户。 通过授予服务主体所需的最低权限，可以确保自动化脚本更加安全。

如果需要创建要通过 Azure PowerShell 使用的服务主体，请参阅[使用 Azure PowerShell 创建 Azure 服务主体](create-azure-service-principal-azureps.md)。

若要使用服务主体进行登录，请将 `-ServicePrincipal` 参数与 `Connect-AzureRmAccount` cmdlet 一起使用。 你还将需要服务主体的应用程序 ID、登录凭据以及与服务主体关联的租户 ID。 若要将服务主体的凭据获取为合适的对象，请使用 [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet。 此 cmdlet 将显示一个对话框，可以在其中输入服务主体用户 ID 和密码。

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-managed-identities-for-azure-resources"></a>使用 Azure 资源的托管标识登录

Azure 资源的托管标识是 Azure Active Directory 的一项功能。 可以使用托管标识服务主体登录，并获取仅限应用的访问令牌来访问其他资源。 托管标识只能在 Azure 云中运行的虚拟机上使用。

有关 Azure 资源的托管标识的详细信息，请参阅[如何在 Azure VM 上使用 Azure 资源托管标识来获取访问令牌](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token)。

## <a name="sign-in-to-another-cloud"></a>登录到其他云

Azure 云服务提供了遵循各个区域的数据处理法规的不同环境。 如果你的 Azure 帐户在与这些区域之一关联的云中，则在登录时需要指定环境。 例如，如果帐户在中国云中，请使用以下命令登录：

```azurepowershell-interactive
Connect-AzureRmAccount -Environment AzureChinaCloud
```

使用以下命令获取可用环境的列表：

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
* [Set-AzureRmRoleDefinition](/powershell/moduel/AzureRM.Resources/Set-AzureRmRoleDefinition)
