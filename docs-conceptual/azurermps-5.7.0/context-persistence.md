---
title: 在不同的 PowerShell 会话中保留用户凭据
description: 了解如何在多个不同的 PowerShell 会话中重复使用 Azure 凭据和其他信息。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/31/2017
ms.openlocfilehash: 164444b7bacbef202513bfafe2f75bdcd6d027c4
ms.sourcegitcommit: 93f93b90ef88c2659be95f3acaba514fe9639169
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2018
ms.locfileid: "52826929"
---
# <a name="persisting-user-credentials-across-powershell-sessions"></a>在不同的 PowerShell 会话中保留用户凭据

Azure PowerShell 提供了一项称为 **Azure 上下文自动保存**的功能，它提供了以下功能：

- 在新 PowerShell 会话中保留登录信息供重复使用。
- 方便使用后台任务来执行长时间运行的 cmdlet。
- 无需分别登录便可在不同的帐户、订阅和环境之间切换。
- 通过相同的 PowerShell 会话同时使用不同的凭据和订阅执行任务。

## <a name="azure-contexts-defined"></a>定义的 Azure 上下文

Azure 上下文是一组定义 Azure PowerShell cmdlet 目标的信息。 上下文由五个部分组成：

- 帐户 - 对 Azure 通信进行身份验证时所用的用户名或服务主体
- 订阅 - 包含正在操作的资源的 Azure 订阅。
- 租户 - 包含你的订阅的 Azure Active Directory 租户。 租户对于 ServicePrincipal 身份验证而言更重要。
- 环境 - 作为目标的特定 Azure 云，通常是 Azure 全球云。
  但是，使用环境设置也可以指定以国家、政府和本地 (Azure Stack) 云为目标。
- 凭据 - Azure 用来验证你的身份并确保你有权访问 Azure 中的资源的信息

在以前的版本中，每次打开新的 PowerShell 会话时，都必须创建 Azure 上下文。 从 Azure PowerShell v4.4.0 开始，可以启用自动保存，然后，每次打开新的 PowerShell 会话时，可以重复使用 Azure 上下文。

## <a name="automatically-saving-the-context-for-the-next-sign-in"></a>自动保存上下文供下次登录使用

默认情况下，每当关闭 PowerShell 会话时，Azure PowerShell 会丢弃上下文信息。

若要让 Azure PowerShell 在关闭 PowerShell 会话后记住上下文，请使用 `Enable-AzureRmContextAutosave`。 上下文和凭据信息自动保存在用户目录中的特殊隐藏文件夹内 (`%AppData%\Roaming\Windows Azure PowerShell`)。
以后，每个新的 PowerShell 会话都以最后一个会话中使用的上下文为目标。

若要将 PowerShell 设置为忘记上下文和凭据，请使用 `Disable-AzureRmContextAutoSave`。 每次打开 PowerShell 会话时，都需要登录到 Azure。

用于管理 Azure 上下文的 cmdlet 也允许进行精细控制。 是希望将更改只应用到当前 PowerShell 会话（`Process` 范围）还是每个 PowerShell 会话（`CurrentUser` 范围）。 [使用上下文范围](#Using-Context-Scopes)中更详细地介绍了这些选项。

## <a name="running-azure-powershell-cmdlets-as-background-jobs"></a>以后台作业的形式运行 Azure PowerShell cmdlet

**Azure 上下文自动保存**功能还允许与 PowerShell 后台作业共享上下文。 在 PowerShell 中，可以后台作业的形式启动和监视长时间执行的任务，而无需等待任务完成。 可通过两种不同的方式与后台作业共享凭据：

- 将上下文作为参数传递

  大多数 AzureRM cmdlet 允许将上下文作为参数传递给 cmdlet。 可按以下示例中所示，将上下文传递给后台作业：

  ```powershell-interactive
  PS C:\> $job = Start-Job { param ($ctx) New-AzureRmVm -AzureRmContext $ctx [... Additional parameters ...]} -ArgumentList (Get-AzureRmContext)
  ```

- 在启用自动保存的情况下使用默认上下文

  如果已启用**上下文自动保存**，后台作业会自动使用默认保存的上下文。

  ```powershell-interactive
  PS C:\> $job = Start-Job { New-AzureRmVm [... Additional parameters ...]}
  ```

需要知道后台任务的结果时，可使用 `Get-Job` 检查作业状态，使用 `Wait-Job` 等待作业完成。 使用 `Receive-Job` 可捕获或显示后台作业的输出。 有关详细信息，请参阅 [about_Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs)。

## <a name="creating-selecting-renaming-and-removing-contexts"></a>创建、选择、重命名和删除上下文

若要创建上下文，必须登录到 Azure。 `Connect-AzureRmAccount` cmdlet（或其别名 `Login-AzureRmAccount`）设置后续 Azure PowerShell cmdlet 使用的默认上下文，并用于访问凭据所允许的任何租户或订阅。

若要在登录后添加新的上下文，请使用 `Set-AzureRmContext`（或其别名 `Select-AzureRmSubscription`）。

```azurepowershell-interactive
PS C:\> Set-AzureRMContext -Subscription "Contoso Subscription 1" -Name "Contoso1"
```

上面的示例使用当前凭据添加了以“Contoso Subscription 1”为目标的新上下文。 新上下文名为“Contoso1”。 如果未提供上下文的名称，将使用包含帐户 ID 和订阅 ID 的默认名称。

若要重命名现有上下文，请使用 `Rename-AzureRmContext` cmdlet。 例如：

```azurepowershell-interactive
PS C:\> Rename-AzureRmContext '[user1@contoso.org; 123456-7890-1234-564321]` 'Contoso2'
```

此示例将自动命名为 `[user1@contoso.org; 123456-7890-1234-564321]` 的上下文重命名为简单名称“Contoso2”。 可管理上下文的 cmdlet 还会使用 tab 自动补全，让我们快速选择上下文。

最后，若要删除上下文，请使用 `Remove-AzureRmContext` cmdlet。  例如：

```azurepowershell-interactive
PS C:\> Remove-AzureRmContext Contoso2
```

忘记名为“Contoso2”的上下文。 以后可以使用 `Set-AzureRmContext` 重新创建此上下文

## <a name="removing-credentials"></a>删除凭据

可以使用 `Disconnect-AzureRmAccount`（也称为 `Logout-AzureRmAccount`）删除用户或服务主体的所有凭据和关联的上下文。 在不带参数执行时，`Disconnect-AzureRmAccount` cmdlet 会删除与当前上下文中的用户或服务主体关联的所有凭据和上下文。 可以传入用户名、服务主体名称或上下文，来指定以特定的主体为目标。

```azurepowershell-interactive
Disconnect-AzureRmAccount user1@contoso.org
```

## <a name="using-context-scopes"></a>使用上下文范围

有时，我们希望在不影响其他会话的情况下，选择、更改或删除某个 PowerShell 会话中的上下文。 若要更改上下文 cmdlet 的默认行为，请使用 `Scope` 参数。 `Process` 范围使默认行为仅适用于当前会话，以此重写默认行为。 与之相反，`CurrentUser` 范围会更改所有会话而不仅是当前会话中的上下文。

例如，若要更改当前 PowerShell 会话中的默认上下文且不影响其他会话时段或下次打开会话时使用的上下文，请使用:

```azurepowershell-interactive
PS C:\> Select-AzureRmContext Contoso1 -Scope Process
```

## <a name="how-the-context-autosave-setting-is-remembered"></a>如何记住上下文自动保存设置

上下文自动保存设置保存到 Azure PowerShell 用户目录 (`%AppData%\Roaming\Windows Azure PowerShell`)。 某些类型的计算机帐户可能无权访问此目录。 对于这种情况，可以使用环境变量

```azurepowershell-interactive
$env:AzureRmContextAutoSave="true" | "false"
```

如果设置为“true”，则自动保存上下文。 如果设置为“false”，则不保存上下文。

## <a name="changes-to-the-azurermprofile-module"></a>对 AzureRM.Profile 模块的更改

用于管理上下文的新 cmdlet

- [Enable-AzureRmContextAutosave][enable] - 用于在不同的 PowerShell 会话中保存上下文。
  所做的任何更改都会更改全局上下文。
- [Disable-AzureRmContextAutosave][disable] - 关闭上下文自动保存。 每打开一个新的 PowerShell 会话都需要重新登录。
- [Select-AzureRmContext][select] - 选择某个上下文作为默认值。 所有后续 cmdlet 都使用此上下文中的凭据进行身份验证。
- [Disconnect-AzureRmAccount][remove-cred] - 删除与帐户关联的所有凭据和上下文。
- [Remove-AzureRmContext][remove-context] - 删除命名的上下文。
- [Rename-AzureRmContext][rename] - 重命名现有上下文。

对现有配置文件 cmdlet 的更改

- [Add-AzureRmAccount][login] - 用于设置进程或当前用户的登录范围。
  用于在身份验证后命名默认上下文。
- [Import-AzureRmContext][import] - 用于设置进程或当前用户的登录范围。
- [Set-AzureRmContext][set-context] - 用于选择现有的命名上下文，以及设置对进程或当前用户的更改范围。

<!-- Hyperlinks -->
[enable]: /powershell/module/azurerm.profile/Enable-AzureRmContextAutosave
[disable]: /powershell/module/azurerm.profile/Disable-AzureRmContextAutosave
[select]: /powershell/module/azurerm.profile/Select-AzureRmContext
[remove-cred]: /powershell/module/azurerm.profile/Disconnect-AzureRmAccount
[remove-context]: /powershell/module/azurerm.profile/Remove-AzureRmContext
[rename]: /powershell/module/azurerm.profile/Rename-AzureRmContext

<!-- Updated cmdlets -->
[login]: /powershell/module/azurerm.profile/Connect-AzureRmAccount
[import]: /powershell/module/azurerm.profile/Import-AzureRmAccount
[set-context]: /powershell/module/azurerm.profile/Import-AzureRmContext
