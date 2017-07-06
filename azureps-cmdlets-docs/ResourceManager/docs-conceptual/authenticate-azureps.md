---
title: "使用 Azure PowerShell 登录"
description: "使用 Azure PowerShell 登录"
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: f6d249ca5bb09c4fe8445ba5b339ffa6012815ed
ms.sourcegitcommit: 226527be7cb647acfe2ea9ab151185053ab3c6db
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/29/2017
---
# <a name="log-in-with-azure-powershell"></a>使用 Azure PowerShell 登录

Azure PowerShell 支持多种登录方法。 最简单的初始方法是通过命令行以交互方式登录。

## <a name="interactive-log-in"></a>交互式登录

1. 键入 `Login-AzureRmAccount`。 此时将出现一个对话框，要求输入 Azure 凭据。

2. 键入与你的帐户关联的电子邮件地址和密码。 Azure 将对凭据信息进行身份验证和保存，然后关闭该窗口。

## <a name="log-in-with-a-service-principal"></a>使用服务主体登录

使用服务主体能够创建可用于处理资源的非交互式帐户。 服务主体类似于可以使用 Azure Active Directory 向其应用规则的用户帐户。 通过授予服务主体所需的最低权限，可以确保自动化脚本更加安全。

1. 如果尚未创建服务主体，请[创建一个](create-azure-service-principal-azureps.md)。

2. 使用服务主体登录。

    ```powershell
    Login-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
    ```

    若要获取 TenantId，请以交互方式登录，然后从订阅中获取 TenantId。

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
    ```

## <a name="log-in-to-another-cloud"></a>登录到其他云

Azure 云服务提供遵循各政府的数据处理法规的不同环境。 如果 Azure 帐户在政府云中，登录时需指定环境。 例如，如果帐户在中国云中，请使用以下命令登录：

```powershell
Login-AzureRmAccount -EnvironmentName AzureChinaCloud
```

使用以下命令获取可用环境的列表：

```powershell
Get-AzureRmEnvironment | Select-Object Name
```

```
Name
----
AzureCloud
AzureChinaCloud
AzureUSGovernment
AzureGermanCloud
```

## <a name="learn-more-about-managing-azure-role-based-access"></a>详细了解如何管理 Azure 基于角色的访问

有关 Azure 中的身份验证和订阅管理的详细信息，请参阅[管理帐户、订阅和管理角色](/azure/active-directory/role-based-access-control-configure)。

用于角色管理的 Azure PowerShell cmdlet

* [Get-AzureRmRoleAssignment](/powershell/module/AzureRM.Resources/Get-AzureRmRoleAssignment)
* [Get-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/Get-AzureRmRoleDefinition)
* [New-AzureRmRoleAssignment](/powershell/module/AzureRM.Resources/New-AzureRmRoleAssignment)
* [New-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/New-AzureRmRoleDefinition)
* [Remove-AzureRmRoleAssignment](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleAssignment)
* [Remove-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleDefinition)
* [Set-AzureRmRoleDefinition](/powershell/moduel/AzureRM.Resources/Set-AzureRmRoleDefinition)
