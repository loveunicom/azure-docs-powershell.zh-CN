---
title: 在不同的 PowerShell 会话中保留用户凭据
description: 了解如何在多个不同的 PowerShell 会话中重复使用 Azure 凭据和其他信息。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/31/2017
ms.openlocfilehash: 85de158cd2a4c3a38f653a530db8e6fae50cb37f
ms.sourcegitcommit: 80a3da199954d0ab78765715fb49793e89a30f12
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/22/2018
ms.locfileid: "52258513"
---
# <a name="persisting-user-credentials-across-powershell-sessions"></a><span data-ttu-id="2f497-103">在不同的 PowerShell 会话中保留用户凭据</span><span class="sxs-lookup"><span data-stu-id="2f497-103">Persisting user credentials across PowerShell sessions</span></span>

<span data-ttu-id="2f497-104">Azure PowerShell 提供了一项称为 **Azure 上下文自动保存**的功能，它提供了以下功能：</span><span class="sxs-lookup"><span data-stu-id="2f497-104">Azure PowerShell offers a feature called **Azure Context Autosave**, which gives the following features:</span></span>

- <span data-ttu-id="2f497-105">在新 PowerShell 会话中保留登录信息供重复使用。</span><span class="sxs-lookup"><span data-stu-id="2f497-105">Retention of sign in information for reuse in new PowerShell sessions.</span></span>
- <span data-ttu-id="2f497-106">方便使用后台任务来执行长时间运行的 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2f497-106">Easier use of background tasks for executing long-running cmdlets.</span></span>
- <span data-ttu-id="2f497-107">无需分别登录便可在不同的帐户、订阅和环境之间切换。</span><span class="sxs-lookup"><span data-stu-id="2f497-107">Switch between accounts, subscriptions, and environments without a separate sign in.</span></span>
- <span data-ttu-id="2f497-108">通过相同的 PowerShell 会话同时使用不同的凭据和订阅执行任务。</span><span class="sxs-lookup"><span data-stu-id="2f497-108">Execution of tasks using different credentials and subscriptions, simultaneously, from the same PowerShell session.</span></span>

## <a name="azure-contexts-defined"></a><span data-ttu-id="2f497-109">定义的 Azure 上下文</span><span class="sxs-lookup"><span data-stu-id="2f497-109">Azure contexts defined</span></span>

<span data-ttu-id="2f497-110">Azure 上下文是一组定义 Azure PowerShell cmdlet 目标的信息。</span><span class="sxs-lookup"><span data-stu-id="2f497-110">An *Azure context* is a set of information that defines the target of Azure PowerShell cmdlets.</span></span> <span data-ttu-id="2f497-111">上下文由五个部分组成：</span><span class="sxs-lookup"><span data-stu-id="2f497-111">The context consists of five parts:</span></span>

- <span data-ttu-id="2f497-112">帐户 - 对 Azure 通信进行身份验证时所用的用户名或服务主体</span><span class="sxs-lookup"><span data-stu-id="2f497-112">An *Account* - the UserName or Service Principal used to authenticate communications with Azure</span></span>
- <span data-ttu-id="2f497-113">订阅 - 包含正在操作的资源的 Azure 订阅。</span><span class="sxs-lookup"><span data-stu-id="2f497-113">A *Subscription* - The Azure Subscription containing the Resources being acted upon.</span></span>
- <span data-ttu-id="2f497-114">租户 - 包含你的订阅的 Azure Active Directory 租户。</span><span class="sxs-lookup"><span data-stu-id="2f497-114">A *Tenant* - The Azure Active Directory tenant that contains your subscription.</span></span> <span data-ttu-id="2f497-115">租户对于 ServicePrincipal 身份验证而言更重要。</span><span class="sxs-lookup"><span data-stu-id="2f497-115">Tenants are more important to ServicePrincipal authentication.</span></span>
- <span data-ttu-id="2f497-116">环境 - 作为目标的特定 Azure 云，通常是 Azure 全球云。</span><span class="sxs-lookup"><span data-stu-id="2f497-116">An *Environment* - The particular Azure Cloud being targeted, usually the Azure global Cloud.</span></span>
  <span data-ttu-id="2f497-117">但是，使用环境设置也可以指定以国家、政府和本地 (Azure Stack) 云为目标。</span><span class="sxs-lookup"><span data-stu-id="2f497-117">However, the environment setting allows you to target National, Government, and on-premises (Azure Stack) clouds as well.</span></span>
- <span data-ttu-id="2f497-118">凭据 - Azure 用来验证你的身份并确保你有权访问 Azure 中的资源的信息</span><span class="sxs-lookup"><span data-stu-id="2f497-118">*Credentials* - The information used by Azure to verify your identity and ensure your authorization to access resources in Azure</span></span>

<span data-ttu-id="2f497-119">在以前的版本中，每次打开新的 PowerShell 会话时，都必须创建 Azure 上下文。</span><span class="sxs-lookup"><span data-stu-id="2f497-119">In previous releases, your Azure Context had to be created each time you opened a new PowerShell session.</span></span> <span data-ttu-id="2f497-120">从 Azure PowerShell v4.4.0 开始，可以启用自动保存，然后，每次打开新的 PowerShell 会话时，可以重复使用 Azure 上下文。</span><span class="sxs-lookup"><span data-stu-id="2f497-120">Beginning with Azure PowerShell v4.4.0, you can enable the automatic saving and reuse of Azure Contexts whenever you open a new PowerShell session.</span></span>

## <a name="automatically-saving-the-context-for-the-next-sign-in"></a><span data-ttu-id="2f497-121">自动保存上下文供下次登录使用</span><span class="sxs-lookup"><span data-stu-id="2f497-121">Automatically saving the context for the next sign in</span></span>

<span data-ttu-id="2f497-122">默认情况下，每当关闭 PowerShell 会话时，Azure PowerShell 会丢弃上下文信息。</span><span class="sxs-lookup"><span data-stu-id="2f497-122">By default, Azure PowerShell discards your context information whenever you close the PowerShell session.</span></span>

<span data-ttu-id="2f497-123">若要让 Azure PowerShell 在关闭 PowerShell 会话后记住上下文，请使用 `Enable-AzureRmContextAutosave`。</span><span class="sxs-lookup"><span data-stu-id="2f497-123">To allow Azure PowerShell to remember your context after the PowerShell session is closed, use `Enable-AzureRmContextAutosave`.</span></span> <span data-ttu-id="2f497-124">上下文和凭据信息自动保存在用户目录中的特殊隐藏文件夹内 (`%AppData%\Roaming\Windows Azure PowerShell`)。</span><span class="sxs-lookup"><span data-stu-id="2f497-124">Context and credential information are automatically saved in a special hidden folder in your user directory (`%AppData%\Roaming\Windows Azure PowerShell`).</span></span>
<span data-ttu-id="2f497-125">以后，每个新的 PowerShell 会话都以最后一个会话中使用的上下文为目标。</span><span class="sxs-lookup"><span data-stu-id="2f497-125">Subsequently, each new PowerShell session targets the context used in your last session.</span></span>

<span data-ttu-id="2f497-126">若要将 PowerShell 设置为忘记上下文和凭据，请使用 `Disable-AzureRmContextAutoSave`。</span><span class="sxs-lookup"><span data-stu-id="2f497-126">To set PowerShell to forget your context and credentials, use `Disable-AzureRmContextAutoSave`.</span></span> <span data-ttu-id="2f497-127">每次打开 PowerShell 会话时，都需要登录到 Azure。</span><span class="sxs-lookup"><span data-stu-id="2f497-127">You will need to sign in to Azure every time you open a PowerShell session.</span></span>

<span data-ttu-id="2f497-128">用于管理 Azure 上下文的 cmdlet 也允许进行精细控制。</span><span class="sxs-lookup"><span data-stu-id="2f497-128">The cmdlets that allow you to manage Azure contexts also allow you fine grained control.</span></span> <span data-ttu-id="2f497-129">是希望将更改只应用到当前 PowerShell 会话（`Process` 范围）还是每个 PowerShell 会话（`CurrentUser` 范围）。</span><span class="sxs-lookup"><span data-stu-id="2f497-129">If you want changes to apply only to the current PowerShell session (`Process` scope) or every PowerShell session (`CurrentUser` scope).</span></span> <span data-ttu-id="2f497-130">[使用上下文范围](#Using-Context-Scopes)中更详细地介绍了这些选项。</span><span class="sxs-lookup"><span data-stu-id="2f497-130">These options are discussed in mode detail in [Using Context Scopes](#Using-Context-Scopes).</span></span>

## <a name="running-azure-powershell-cmdlets-as-background-jobs"></a><span data-ttu-id="2f497-131">以后台作业的形式运行 Azure PowerShell cmdlet</span><span class="sxs-lookup"><span data-stu-id="2f497-131">Running Azure PowerShell cmdlets as background jobs</span></span>

<span data-ttu-id="2f497-132">**Azure 上下文自动保存**功能还允许与 PowerShell 后台作业共享上下文。</span><span class="sxs-lookup"><span data-stu-id="2f497-132">The **Azure Context Autosave** feature also allows you to share you context with PowerShell background jobs.</span></span> <span data-ttu-id="2f497-133">在 PowerShell 中，可以后台作业的形式启动和监视长时间执行的任务，而无需等待任务完成。</span><span class="sxs-lookup"><span data-stu-id="2f497-133">PowerShell allows you to start and monitor long-executing tasks as background jobs without having to wait for the tasks to complete.</span></span> <span data-ttu-id="2f497-134">可通过两种不同的方式与后台作业共享凭据：</span><span class="sxs-lookup"><span data-stu-id="2f497-134">You can share credentials with background jobs in two different ways:</span></span>

- <span data-ttu-id="2f497-135">将上下文作为参数传递</span><span class="sxs-lookup"><span data-stu-id="2f497-135">Passing the context as an argument</span></span>

  <span data-ttu-id="2f497-136">大多数 AzureRM cmdlet 允许将上下文作为参数传递给 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2f497-136">Most AzureRM cmdlets allow you to pass the context as a parameter to the cmdlet.</span></span> <span data-ttu-id="2f497-137">可按以下示例中所示，将上下文传递给后台作业：</span><span class="sxs-lookup"><span data-stu-id="2f497-137">You can pass a context to a background job as shown in the following example:</span></span>

  ```powershell-interactive
  PS C:\> $job = Start-Job { param ($ctx) New-AzureRmVm -AzureRmContext $ctx [... Additional parameters ...]} -ArgumentList (Get-AzureRmContext)
  ```

- <span data-ttu-id="2f497-138">在启用自动保存的情况下使用默认上下文</span><span class="sxs-lookup"><span data-stu-id="2f497-138">Using the default context with Autosave enabled</span></span>

  <span data-ttu-id="2f497-139">如果已启用**上下文自动保存**，后台作业会自动使用默认保存的上下文。</span><span class="sxs-lookup"><span data-stu-id="2f497-139">If you have enabled **Context Autosave**, background jobs automatically use the default saved context.</span></span>

  ```powershell-interactive
  PS C:\> $job = Start-Job { New-AzureRmVm [... Additional parameters ...]}
  ```

<span data-ttu-id="2f497-140">需要知道后台任务的结果时，可使用 `Get-Job` 检查作业状态，使用 `Wait-Job` 等待作业完成。</span><span class="sxs-lookup"><span data-stu-id="2f497-140">When you need to know the outcome of the background task, use `Get-Job` to check the job status and `Wait-Job` to wait for the Job to complete.</span></span> <span data-ttu-id="2f497-141">使用 `Receive-Job` 可捕获或显示后台作业的输出。</span><span class="sxs-lookup"><span data-stu-id="2f497-141">Use `Receive-Job` to capture or display the output of the background job.</span></span> <span data-ttu-id="2f497-142">有关详细信息，请参阅 [about_Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs)。</span><span class="sxs-lookup"><span data-stu-id="2f497-142">For more information, see [about_Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span></span>

## <a name="creating-selecting-renaming-and-removing-contexts"></a><span data-ttu-id="2f497-143">创建、选择、重命名和删除上下文</span><span class="sxs-lookup"><span data-stu-id="2f497-143">Creating, selecting, renaming, and removing contexts</span></span>

<span data-ttu-id="2f497-144">若要创建上下文，必须登录到 Azure。</span><span class="sxs-lookup"><span data-stu-id="2f497-144">To create a context, you must be signed in to Azure.</span></span> <span data-ttu-id="2f497-145">`Add-AzureRmAccount` cmdlet（或其别名 `Login-AzureRmAccount`）设置后续 Azure PowerShell cmdlet 使用的默认上下文，并用于访问凭据所允许的任何租户或订阅。</span><span class="sxs-lookup"><span data-stu-id="2f497-145">The `Add-AzureRmAccount` cmdlet (or its alias, `Login-AzureRmAccount`) sets the default context used by subsequent Azure PowerShell cmdlets, and allows you to access any tenants or subscriptions allowed by your credentials.</span></span>

<span data-ttu-id="2f497-146">若要在登录后添加新的上下文，请使用 `Set-AzureRmContext`（或其别名 `Select-AzureRmSubscription`）。</span><span class="sxs-lookup"><span data-stu-id="2f497-146">To add a new context after sign in, use `Set-AzureRmContext` (or its alias, `Select-AzureRmSubscription`).</span></span>

```azurepowershell-interactive
PS C:\> Set-AzureRMContext -Subscription "Contoso Subscription 1" -Name "Contoso1"
```

<span data-ttu-id="2f497-147">上面的示例使用当前凭据添加了以“Contoso Subscription 1”为目标的新上下文。</span><span class="sxs-lookup"><span data-stu-id="2f497-147">The previous example adds a new context targeting 'Contoso Subscription 1' using your current credentials.</span></span> <span data-ttu-id="2f497-148">新上下文名为“Contoso1”。</span><span class="sxs-lookup"><span data-stu-id="2f497-148">The new context is named 'Contoso1'.</span></span> <span data-ttu-id="2f497-149">如果未提供上下文的名称，将使用包含帐户 ID 和订阅 ID 的默认名称。</span><span class="sxs-lookup"><span data-stu-id="2f497-149">If you do not provide a name for the context, a default name, using the account ID and subscription ID is used.</span></span>

<span data-ttu-id="2f497-150">若要重命名现有上下文，请使用 `Rename-AzureRmContext` cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2f497-150">To rename an existing context, use the `Rename-AzureRmContext` cmdlet.</span></span> <span data-ttu-id="2f497-151">例如：</span><span class="sxs-lookup"><span data-stu-id="2f497-151">For example:</span></span>

```azurepowershell-interactive
PS C:\> Rename-AzureRmContext '[user1@contoso.org; 123456-7890-1234-564321]` 'Contoso2'
```

<span data-ttu-id="2f497-152">此示例将自动命名为 `[user1@contoso.org; 123456-7890-1234-564321]` 的上下文重命名为简单名称“Contoso2”。</span><span class="sxs-lookup"><span data-stu-id="2f497-152">This example renames the context with automatic name `[user1@contoso.org; 123456-7890-1234-564321]` to the simple name 'Contoso2'.</span></span> <span data-ttu-id="2f497-153">可管理上下文的 cmdlet 还会使用 tab 自动补全，让我们快速选择上下文。</span><span class="sxs-lookup"><span data-stu-id="2f497-153">Cmdlets that manage contexts also use tab completion, allowing you to quickly select the context.</span></span>

<span data-ttu-id="2f497-154">最后，若要删除上下文，请使用 `Remove-AzureRmContext` cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2f497-154">Finally, to remove a context, use the `Remove-AzureRmContext` cmdlet.</span></span>  <span data-ttu-id="2f497-155">例如：</span><span class="sxs-lookup"><span data-stu-id="2f497-155">For example:</span></span>

```azurepowershell-interactive
PS C:\> Remove-AzureRmContext Contoso2
```

<span data-ttu-id="2f497-156">忘记名为“Contoso2”的上下文。</span><span class="sxs-lookup"><span data-stu-id="2f497-156">Forgets the context that was named 'Contoso2'.</span></span> <span data-ttu-id="2f497-157">以后可以使用 `Set-AzureRmContext` 重新创建此上下文</span><span class="sxs-lookup"><span data-stu-id="2f497-157">You can recreate this context subsequently using `Set-AzureRmContext`</span></span>

## <a name="removing-credentials"></a><span data-ttu-id="2f497-158">删除凭据</span><span class="sxs-lookup"><span data-stu-id="2f497-158">Removing credentials</span></span>

<span data-ttu-id="2f497-159">可以使用 `Remove-AzureRmAccount`（也称为 `Logout-AzureRmAccount`）删除用户或服务主体的所有凭据和关联的上下文。</span><span class="sxs-lookup"><span data-stu-id="2f497-159">You can remove all credentials and associated contexts for a user or service principal using `Remove-AzureRmAccount` (also known as `Logout-AzureRmAccount`).</span></span> <span data-ttu-id="2f497-160">在不带参数执行时，`Remove-AzureRmAccount` cmdlet 会删除与当前上下文中的用户或服务主体关联的所有凭据和上下文。</span><span class="sxs-lookup"><span data-stu-id="2f497-160">When executed without parameters, the `Remove-AzureRmAccount` cmdlet removes all credentials and contexts associated with the User or Service Principal in the current context.</span></span> <span data-ttu-id="2f497-161">可以传入用户名、服务主体名称或上下文，来指定以特定的主体为目标。</span><span class="sxs-lookup"><span data-stu-id="2f497-161">You may pass in a Username, Service Principal Name, or context to target a particular principal.</span></span>

```azurepowershell-interactive
Remove-AzureRmAccount user1@contoso.org
```

## <a name="using-context-scopes"></a><span data-ttu-id="2f497-162">使用上下文范围</span><span class="sxs-lookup"><span data-stu-id="2f497-162">Using context scopes</span></span>

<span data-ttu-id="2f497-163">有时，我们希望在不影响其他会话的情况下，选择、更改或删除某个 PowerShell 会话中的上下文。</span><span class="sxs-lookup"><span data-stu-id="2f497-163">Occasionally, you may want to select, change, or remove a context in a PowerShell session without impacting other sessions.</span></span> <span data-ttu-id="2f497-164">若要更改上下文 cmdlet 的默认行为，请使用 `Scope` 参数。</span><span class="sxs-lookup"><span data-stu-id="2f497-164">To change the default behavior of context cmdlets, use the `Scope` parameter.</span></span> <span data-ttu-id="2f497-165">`Process` 范围使默认行为仅适用于当前会话，以此重写默认行为。</span><span class="sxs-lookup"><span data-stu-id="2f497-165">The `Process` scope overrides the default behavior by making it apply only for the current session.</span></span> <span data-ttu-id="2f497-166">与之相反，`CurrentUser` 范围会更改所有会话而不仅是当前会话中的上下文。</span><span class="sxs-lookup"><span data-stu-id="2f497-166">Conversely `CurrentUser` scope changes the context in all sessions, instead of just the current session.</span></span>

<span data-ttu-id="2f497-167">例如，若要更改当前 PowerShell 会话中的默认上下文且不影响其他会话时段或下次打开会话时使用的上下文，请使用:</span><span class="sxs-lookup"><span data-stu-id="2f497-167">As an example, to change the default context in the current PowerShell session without impacting other windows, or the context used the next time a session is opened, use:</span></span>

```azurepowershell-interactive
PS C:\> Select-AzureRmContext Contoso1 -Scope Process
```

## <a name="how-the-context-autosave-setting-is-remembered"></a><span data-ttu-id="2f497-168">如何记住上下文自动保存设置</span><span class="sxs-lookup"><span data-stu-id="2f497-168">How the context autosave setting is remembered</span></span>

<span data-ttu-id="2f497-169">上下文自动保存设置保存到 Azure PowerShell 用户目录 (`%AppData%\Roaming\Windows Azure PowerShell`)。</span><span class="sxs-lookup"><span data-stu-id="2f497-169">The context AutoSave setting is saved to the user Azure PowerShell directory (`%AppData%\Roaming\Windows Azure PowerShell`).</span></span> <span data-ttu-id="2f497-170">某些类型的计算机帐户可能无权访问此目录。</span><span class="sxs-lookup"><span data-stu-id="2f497-170">Some kinds of computer accounts may not have access to this directory.</span></span> <span data-ttu-id="2f497-171">对于这种情况，可以使用环境变量</span><span class="sxs-lookup"><span data-stu-id="2f497-171">For such scenarios, you can use the environment variable</span></span>

```azurepowershell-interactive
$env:AzureRmContextAutoSave="true" | "false"
```

<span data-ttu-id="2f497-172">如果设置为“true”，则自动保存上下文。</span><span class="sxs-lookup"><span data-stu-id="2f497-172">If set to 'true', the context is automatically saved.</span></span> <span data-ttu-id="2f497-173">如果设置为“false”，则不保存上下文。</span><span class="sxs-lookup"><span data-stu-id="2f497-173">If set to 'false', the context is not saved.</span></span>

## <a name="changes-to-the-azurermprofile-module"></a><span data-ttu-id="2f497-174">对 AzureRM.Profile 模块的更改</span><span class="sxs-lookup"><span data-stu-id="2f497-174">Changes to the AzureRM.Profile module</span></span>

<span data-ttu-id="2f497-175">用于管理上下文的新 cmdlet</span><span class="sxs-lookup"><span data-stu-id="2f497-175">New cmdlets for managing context</span></span>

- <span data-ttu-id="2f497-176">[Enable-AzureRmContextAutosave][enable] - 用于在不同的 PowerShell 会话中保存上下文。</span><span class="sxs-lookup"><span data-stu-id="2f497-176">[Enable-AzureRmContextAutosave][enable] - Allow saving the context between powershell sessions.</span></span>
  <span data-ttu-id="2f497-177">所做的任何更改都会更改全局上下文。</span><span class="sxs-lookup"><span data-stu-id="2f497-177">Any changes alter the global context.</span></span>
- <span data-ttu-id="2f497-178">[Disable-AzureRmContextAutosave][disable] - 关闭上下文自动保存。</span><span class="sxs-lookup"><span data-stu-id="2f497-178">[Disable-AzureRmContextAutosave][disable] - Turn off autosaving the context.</span></span> <span data-ttu-id="2f497-179">每打开一个新的 PowerShell 会话都需要重新登录。</span><span class="sxs-lookup"><span data-stu-id="2f497-179">Each new PowerShell session is required to sign in again.</span></span>
- <span data-ttu-id="2f497-180">[Select-AzureRmContext][select] - 选择某个上下文作为默认值。</span><span class="sxs-lookup"><span data-stu-id="2f497-180">[Select-AzureRmContext][select] - Select a context as the default.</span></span> <span data-ttu-id="2f497-181">所有后续 cmdlet 都使用此上下文中的凭据进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="2f497-181">All subsequent cmdlets use the credentials in this context for authentication.</span></span>
- <span data-ttu-id="2f497-182">[Remove-AzureRmAccount][remove-cred] - 删除与帐户关联的所有凭据和上下文。</span><span class="sxs-lookup"><span data-stu-id="2f497-182">[Remove-AzureRmAccount][remove-cred] - Remove all credentials and contexts associated with an account.</span></span>
- <span data-ttu-id="2f497-183">[Remove-AzureRmContext][remove-context] - 删除命名的上下文。</span><span class="sxs-lookup"><span data-stu-id="2f497-183">[Remove-AzureRmContext][remove-context] - Remove a named context.</span></span>
- <span data-ttu-id="2f497-184">[Rename-AzureRmContext][rename] - 重命名现有上下文。</span><span class="sxs-lookup"><span data-stu-id="2f497-184">[Rename-AzureRmContext][rename] - Rename an existing context.</span></span>

<span data-ttu-id="2f497-185">对现有配置文件 cmdlet 的更改</span><span class="sxs-lookup"><span data-stu-id="2f497-185">Changes to existing profile cmdlets</span></span>

- <span data-ttu-id="2f497-186">[Add-AzureRmAccount][login] - 用于设置进程或当前用户的登录范围。</span><span class="sxs-lookup"><span data-stu-id="2f497-186">[Add-AzureRmAccount][login] - Allow scoping of the sign in to the process or the current user.</span></span>
  <span data-ttu-id="2f497-187">用于在身份验证后命名默认上下文。</span><span class="sxs-lookup"><span data-stu-id="2f497-187">Allow naming the default context after authentication.</span></span>
- <span data-ttu-id="2f497-188">[Import-AzureRmContext][import] - 用于设置进程或当前用户的登录范围。</span><span class="sxs-lookup"><span data-stu-id="2f497-188">[Import-AzureRmContext][import] - Allow scoping of the sign in to the process or the current user.</span></span>
- <span data-ttu-id="2f497-189">[Set-AzureRmContext][set-context] - 用于选择现有的命名上下文，以及设置对进程或当前用户的更改范围。</span><span class="sxs-lookup"><span data-stu-id="2f497-189">[Set-AzureRmContext][set-context] - Allow selection of existing named contexts, and scope changes to the process or current user.</span></span>

<!-- Hyperlinks -->
[enable]: /powershell/module/azurerm.profile/Enable-AzureRmContextAutosave
[disable]: /powershell/module/azurerm.profile/Disable-AzureRmContextAutosave
[select]: /powershell/module/azurerm.profile/Select-AzureRmContext
[remove-cred]: /powershell/module/azurerm.profile/Remove-AzureRmAccount
[remove-context]: /powershell/module/azurerm.profile/Remove-AzureRmContext
[rename]: /powershell/module/azurerm.profile/Rename-AzureRmContext

<!-- Updated cmdlets -->
[login]: /powershell/module/azurerm.profile/Add-AzureRmAccount
[import]: /powershell/module/azurerm.profile/Import-AzureRmAccount
[set-context]: /powershell/module/azurerm.profile/Import-AzureRmContext
