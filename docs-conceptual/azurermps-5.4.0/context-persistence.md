---
title: "在不同的 PowerShell 会话中保留用户登录"
description: "本文介绍 Azure PowerShell 中的新功能：在多个不同的 PowerShell 会话中重复使用凭据和其他用户信息。"
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/31/2017
ms.openlocfilehash: 8ef20796b64b16c78a653e293a57d5e752d89710
ms.sourcegitcommit: 5fe9a579d2e0d1cb5a05aadaeba5db784f1b18fa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/28/2018
---
# <a name="persisting-user-logins-across-powershell-sessions"></a><span data-ttu-id="4a7a6-103">在不同的 PowerShell 会话中保留用户登录</span><span class="sxs-lookup"><span data-stu-id="4a7a6-103">Persisting user logins across PowerShell sessions</span></span>

<span data-ttu-id="4a7a6-104">在 Azure PowerShell 的 2017 年 9 月版中，Azure 资源管理器 cmdlet 引入了一个新功能：**Azure 上下文自动保存**。</span><span class="sxs-lookup"><span data-stu-id="4a7a6-104">In the September 2017 release of Azure PowerShell, Azure Resource Manager cmdlets introduce a new feature, **Azure Context Autosave**.</span></span> <span data-ttu-id="4a7a6-105">此功能可实现多个新的用户方案，包括：</span><span class="sxs-lookup"><span data-stu-id="4a7a6-105">This feature enables several new user scenarios, including:</span></span>

- <span data-ttu-id="4a7a6-106">在新 PowerShell 会话中保留登录信息供重复使用。</span><span class="sxs-lookup"><span data-stu-id="4a7a6-106">Retention of login information for reuse in new PowerShell sessions.</span></span>
- <span data-ttu-id="4a7a6-107">方便使用后台任务来执行长时间运行的 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4a7a6-107">Easier use of background tasks for executing long-running cmdlets.</span></span>
- <span data-ttu-id="4a7a6-108">无需单独登录即可在帐户、订阅和环境之间切换。</span><span class="sxs-lookup"><span data-stu-id="4a7a6-108">Switch between accounts, subscriptions, and environments without a separate login.</span></span>
- <span data-ttu-id="4a7a6-109">通过相同的 PowerShell 会话同时使用不同的凭据和订阅执行任务。</span><span class="sxs-lookup"><span data-stu-id="4a7a6-109">Execution of tasks using different credentials and subscriptions, simultaneously, from the same PowerShell session.</span></span>

## <a name="azure-contexts-defined"></a><span data-ttu-id="4a7a6-110">定义的 Azure 上下文</span><span class="sxs-lookup"><span data-stu-id="4a7a6-110">Azure contexts defined</span></span>

<span data-ttu-id="4a7a6-111">Azure 上下文是一组定义 Azure PowerShell cmdlet 目标的信息。</span><span class="sxs-lookup"><span data-stu-id="4a7a6-111">An *Azure context* is a set of information that defines the target of Azure PowerShell cmdlets.</span></span> <span data-ttu-id="4a7a6-112">上下文由五个部分组成：</span><span class="sxs-lookup"><span data-stu-id="4a7a6-112">The context consists of five parts:</span></span>

- <span data-ttu-id="4a7a6-113">帐户 - 对 Azure 通信进行身份验证时所用的用户名或服务主体</span><span class="sxs-lookup"><span data-stu-id="4a7a6-113">An *Account* - the UserName or Service Principal used to authenticate communications with Azure</span></span>
- <span data-ttu-id="4a7a6-114">订阅 - 包含正在操作的资源的 Azure 订阅。</span><span class="sxs-lookup"><span data-stu-id="4a7a6-114">A *Subscription* - The Azure Subscription containing the Resources being acted upon.</span></span>
- <span data-ttu-id="4a7a6-115">租户 - 包含你的订阅的 Azure Active Directory 租户。</span><span class="sxs-lookup"><span data-stu-id="4a7a6-115">A *Tenant* - The Azure Active Directory tenant that contains your subscription.</span></span> <span data-ttu-id="4a7a6-116">租户对于 ServicePrincipal 身份验证而言更重要。</span><span class="sxs-lookup"><span data-stu-id="4a7a6-116">Tenants are more important to ServicePrincipal authentication.</span></span>
- <span data-ttu-id="4a7a6-117">环境 - 作为目标的特定 Azure 云，通常是 Azure 全球云。</span><span class="sxs-lookup"><span data-stu-id="4a7a6-117">An *Environment* - The particular Azure Cloud being targeted, usually the Azure global Cloud.</span></span>
  <span data-ttu-id="4a7a6-118">但是，使用环境设置也可以指定以国家、政府和本地 (Azure Stack) 云为目标。</span><span class="sxs-lookup"><span data-stu-id="4a7a6-118">However, the environment setting allows you to target National, Government, and on-premises (Azure Stack) clouds as well.</span></span>
- <span data-ttu-id="4a7a6-119">凭据 - Azure 用来验证你的身份并确保你有权访问 Azure 中的资源的信息</span><span class="sxs-lookup"><span data-stu-id="4a7a6-119">*Credentials* - The information used by Azure to verify your identity and ensure your authorization to access resources in Azure</span></span>

<span data-ttu-id="4a7a6-120">在以前的版本中，每次打开新的 PowerShell 会话时，都必须创建 Azure 上下文。</span><span class="sxs-lookup"><span data-stu-id="4a7a6-120">In previous releases, your Azure Context had to be created each time you opened a new PowerShell session.</span></span> <span data-ttu-id="4a7a6-121">从 Azure PowerShell v4.4.0 开始，可以启用自动保存，然后，每次打开新的 PowerShell 会话时，可以重复使用 Azure 上下文。</span><span class="sxs-lookup"><span data-stu-id="4a7a6-121">Beginning with Azure PowerShell v4.4.0, you can enable the automatic saving and reuse of Azure Contexts whenever you open a new PowerShell session.</span></span>

## <a name="automatically-saving-the-context-for-the-next-login"></a><span data-ttu-id="4a7a6-122">自动保存上下文供下次登录使用</span><span class="sxs-lookup"><span data-stu-id="4a7a6-122">Automatically saving the context for the next login</span></span>

<span data-ttu-id="4a7a6-123">默认情况下，每当关闭 PowerShell 会话时，Azure PowerShell 会丢弃上下文信息。</span><span class="sxs-lookup"><span data-stu-id="4a7a6-123">By default, Azure PowerShell discards your context information whenever you close the PowerShell session.</span></span>

<span data-ttu-id="4a7a6-124">若要让 Azure PowerShell 在关闭 PowerShell 会话后记住上下文，请使用 `Enable-AzureRmContextAutosave`。</span><span class="sxs-lookup"><span data-stu-id="4a7a6-124">To allow Azure PowerShell to remember your context after the PowerShell session is closed, use `Enable-AzureRmContextAutosave`.</span></span> <span data-ttu-id="4a7a6-125">上下文和凭据信息自动保存在用户目录中的特殊隐藏文件夹内 (`%AppData%\Roaming\Windows Azure PowerShell`)。</span><span class="sxs-lookup"><span data-stu-id="4a7a6-125">Context and credential information are automatically saved in a special hidden folder in your user directory (`%AppData%\Roaming\Windows Azure PowerShell`).</span></span>
<span data-ttu-id="4a7a6-126">以后，每个新的 PowerShell 会话都以最后一个会话中使用的上下文为目标。</span><span class="sxs-lookup"><span data-stu-id="4a7a6-126">Subsequently, each new PowerShell session targets the context used in your last session.</span></span>

<span data-ttu-id="4a7a6-127">若要将 PowerShell 设置为忘记上下文和凭据，请使用 `Disable-AzureRmContextAutoSave`。</span><span class="sxs-lookup"><span data-stu-id="4a7a6-127">To set PowerShell to forget your context and credentials, use `Disable-AzureRmContextAutoSave`.</span></span> <span data-ttu-id="4a7a6-128">每次打开 PowerShell 会话时，都需要登录到 Azure。</span><span class="sxs-lookup"><span data-stu-id="4a7a6-128">You will need to log in to Azure every time you open a PowerShell session.</span></span>

<span data-ttu-id="4a7a6-129">用于管理 Azure 上下文的 cmdlet 也允许进行精细控制。</span><span class="sxs-lookup"><span data-stu-id="4a7a6-129">The cmdlets that allow you to manage Azure contexts also allow you fine grained control.</span></span> <span data-ttu-id="4a7a6-130">是希望将更改只应用到当前 PowerShell 会话（`Process` 范围）还是每个 PowerShell 会话（`CurrentUser` 范围）。</span><span class="sxs-lookup"><span data-stu-id="4a7a6-130">If you want changes to apply only to the current PowerShell session (`Process` scope) or every PowerShell session (`CurrentUser` scope).</span></span> <span data-ttu-id="4a7a6-131">[使用上下文范围](#Using-Context-Scopes)中更详细地介绍了这些选项。</span><span class="sxs-lookup"><span data-stu-id="4a7a6-131">These options are discussed in mode detail in [Using Context Scopes](#Using-Context-Scopes).</span></span>

## <a name="running-azure-powershell-cmdlets-as-background-jobs"></a><span data-ttu-id="4a7a6-132">以后台作业的形式运行 Azure PowerShell cmdlet</span><span class="sxs-lookup"><span data-stu-id="4a7a6-132">Running Azure PowerShell cmdlets as background jobs</span></span>

<span data-ttu-id="4a7a6-133">**Azure 上下文自动保存**功能还允许与 PowerShell 后台作业共享上下文。</span><span class="sxs-lookup"><span data-stu-id="4a7a6-133">The **Azure Context Autosave** feature also allows you to share you context with PowerShell background jobs.</span></span> <span data-ttu-id="4a7a6-134">在 PowerShell 中，可以后台作业的形式启动和监视长时间执行的任务，而无需等待任务完成。</span><span class="sxs-lookup"><span data-stu-id="4a7a6-134">PowerShell allows you to start and monitor long-executing tasks as background jobs without having to wait for the tasks to complete.</span></span> <span data-ttu-id="4a7a6-135">可通过两种不同的方式与后台作业共享凭据：</span><span class="sxs-lookup"><span data-stu-id="4a7a6-135">You can share credentials with background jobs in two different ways:</span></span>

- <span data-ttu-id="4a7a6-136">将上下文作为参数传递</span><span class="sxs-lookup"><span data-stu-id="4a7a6-136">Passing the context as an argument</span></span>

  <span data-ttu-id="4a7a6-137">大多数 AzureRM cmdlet 允许将上下文作为参数传递给 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4a7a6-137">Most AzureRM cmdlets allow you to pass the context as a parameter to the cmdlet.</span></span> <span data-ttu-id="4a7a6-138">可按以下示例中所示，将上下文传递给后台作业：</span><span class="sxs-lookup"><span data-stu-id="4a7a6-138">You can pass a context to a background job as shown in the following example:</span></span>

  ```powershell
  PS C:\> $job = Start-Job { param ($ctx) New-AzureRmVm -AzureRmContext $ctx [... Additional parameters ...]} -ArgumentList (Get-AzureRmContext)
  ```

- <span data-ttu-id="4a7a6-139">在启用自动保存的情况下使用默认上下文</span><span class="sxs-lookup"><span data-stu-id="4a7a6-139">Using the default context with Autosave enabled</span></span>

  <span data-ttu-id="4a7a6-140">如果已启用**上下文自动保存**，后台作业会自动使用默认保存的上下文。</span><span class="sxs-lookup"><span data-stu-id="4a7a6-140">If you have enabled **Context Autosave**, background jobs automatically use the default saved context.</span></span>

  ```powershell
  PS C:\> $job = Start-Job { New-AzureRmVm [... Additional parameters ...]}
  ```

<span data-ttu-id="4a7a6-141">需要知道后台任务的结果时，可使用 `Get-Job` 检查作业状态，使用 `Wait-Job` 等待作业完成。</span><span class="sxs-lookup"><span data-stu-id="4a7a6-141">When you need to know the outcome of the background task, use `Get-Job` to check the job status and `Wait-Job` to wait for the Job to complete.</span></span> <span data-ttu-id="4a7a6-142">使用 `Receive-Job` 可捕获或显示后台作业的输出。</span><span class="sxs-lookup"><span data-stu-id="4a7a6-142">Use `Receive-Job` to capture or display the output of the background job.</span></span> <span data-ttu-id="4a7a6-143">有关详细信息，请参阅 [about_Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs)。</span><span class="sxs-lookup"><span data-stu-id="4a7a6-143">For more information, see [about_Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span></span>

## <a name="creating-selecting-renaming-and-removing-contexts"></a><span data-ttu-id="4a7a6-144">创建、选择、重命名和删除上下文</span><span class="sxs-lookup"><span data-stu-id="4a7a6-144">Creating, selecting, renaming, and removing contexts</span></span>

<span data-ttu-id="4a7a6-145">若要创建上下文，必须登录到 Azure。</span><span class="sxs-lookup"><span data-stu-id="4a7a6-145">To create a context, you must be logged in to Azure.</span></span> <span data-ttu-id="4a7a6-146">`Add-AzureRmAccount` cmdlet（或其别名 `Login-AzureRmAccount`）设置后续 Azure PowerShell cmdlet 使用的默认上下文，并用于访问登录凭据所允许的任何租户或订阅。</span><span class="sxs-lookup"><span data-stu-id="4a7a6-146">The `Add-AzureRmAccount` cmdlet (or its alias, `Login-AzureRmAccount`) sets the default context used by subsequent Azure PowerShell cmdlets, and allows you to access any tenants or subscriptions allowed by your login credentials.</span></span>

<span data-ttu-id="4a7a6-147">若要在登录后添加新的上下文，请使用 `Set-AzureRmContext`（或其别名 `Select-AzureRmSubscription`）。</span><span class="sxs-lookup"><span data-stu-id="4a7a6-147">To add a new context after login, use `Set-AzureRmContext` (or its alias, `Select-AzureRmSubscription`).</span></span>

```powershell
PS C:\> Set-AzureRMContext -Subscription "Contoso Subscription 1" -Name "Contoso1"
```

<span data-ttu-id="4a7a6-148">上面的示例使用当前凭据添加了以“Contoso Subscription 1”为目标的新上下文。</span><span class="sxs-lookup"><span data-stu-id="4a7a6-148">The previous example adds a new context targeting 'Contoso Subscription 1' using your current credentials.</span></span> <span data-ttu-id="4a7a6-149">新上下文名为“Contoso1”。</span><span class="sxs-lookup"><span data-stu-id="4a7a6-149">The new context is named 'Contoso1'.</span></span> <span data-ttu-id="4a7a6-150">如果未提供上下文的名称，将使用包含帐户 ID 和订阅 ID 的默认名称。</span><span class="sxs-lookup"><span data-stu-id="4a7a6-150">If you do not provide a name for the context, a default name, using the account ID and subscription ID is used.</span></span>

<span data-ttu-id="4a7a6-151">若要重命名现有上下文，请使用 `Rename-AzureRmContext` cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4a7a6-151">To rename an existing context, use the `Rename-AzureRmContext` cmdlet.</span></span> <span data-ttu-id="4a7a6-152">例如：</span><span class="sxs-lookup"><span data-stu-id="4a7a6-152">For example:</span></span>

```powershell
PS C:\> Rename-AzureRmContext '[user1@contoso.org; 123456-7890-1234-564321]` 'Contoso2'
```

<span data-ttu-id="4a7a6-153">此示例将自动命名为 `[user1@contoso.org; 123456-7890-1234-564321]` 的上下文重命名为简单名称“Contoso2”。</span><span class="sxs-lookup"><span data-stu-id="4a7a6-153">This example renames the context with automatic name `[user1@contoso.org; 123456-7890-1234-564321]` to the simple name 'Contoso2'.</span></span> <span data-ttu-id="4a7a6-154">可管理上下文的 cmdlet 还会使用 tab 自动补全，让我们快速选择上下文。</span><span class="sxs-lookup"><span data-stu-id="4a7a6-154">Cmdlets that manage contexts also use tab completion, allowing you to quickly select the context.</span></span>

<span data-ttu-id="4a7a6-155">最后，若要删除上下文，请使用 `Remove-AzureRmContext` cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4a7a6-155">Finally, to remove a context, use the `Remove-AzureRmContext` cmdlet.</span></span>  <span data-ttu-id="4a7a6-156">例如：</span><span class="sxs-lookup"><span data-stu-id="4a7a6-156">For example:</span></span>

```powershell
PS C:\> Remove-AzureRmContext Contoso2
```

<span data-ttu-id="4a7a6-157">忘记名为“Contoso2”的上下文。</span><span class="sxs-lookup"><span data-stu-id="4a7a6-157">Forgets the context that was named 'Contoso2'.</span></span> <span data-ttu-id="4a7a6-158">以后可以使用 `Set-AzureRmContext` 重新创建此上下文</span><span class="sxs-lookup"><span data-stu-id="4a7a6-158">You can recreate this context subsequently using `Set-AzureRmContext`</span></span>

## <a name="removing-credentials"></a><span data-ttu-id="4a7a6-159">删除凭据</span><span class="sxs-lookup"><span data-stu-id="4a7a6-159">Removing credentials</span></span>

<span data-ttu-id="4a7a6-160">可以使用 `Remove-AzureRmAccount`（也称为 `Logout-AzureRmAccount`）删除用户或服务主体的所有凭据和关联的上下文。</span><span class="sxs-lookup"><span data-stu-id="4a7a6-160">You can remove all credentials and associated contexts for a user or service principal using `Remove-AzureRmAccount` (also known as `Logout-AzureRmAccount`).</span></span> <span data-ttu-id="4a7a6-161">在不带参数执行时，`Remove-AzureRmAccount` cmdlet 会删除与当前上下文中的用户或服务主体关联的所有凭据和上下文。</span><span class="sxs-lookup"><span data-stu-id="4a7a6-161">When executed without parameters, the `Remove-AzureRmAccount` cmdlet removes all credentials and contexts associated with the User or Service Principal in the current context.</span></span> <span data-ttu-id="4a7a6-162">可以传入用户名、服务主体名称或上下文，来指定以特定的主体为目标。</span><span class="sxs-lookup"><span data-stu-id="4a7a6-162">You may pass in a Username, Service Principal Name, or context to target a particular principal.</span></span>

```powershell
Remove-AzureRmAccount user1@contoso.org
```

## <a name="using-context-scopes"></a><span data-ttu-id="4a7a6-163">使用上下文范围</span><span class="sxs-lookup"><span data-stu-id="4a7a6-163">Using context scopes</span></span>

<span data-ttu-id="4a7a6-164">有时，我们希望在不影响其他会话的情况下，选择、更改或删除某个 PowerShell 会话中的上下文。</span><span class="sxs-lookup"><span data-stu-id="4a7a6-164">Occasionally, you may want to select, change, or remove a context in a PowerShell session without impacting other sessions.</span></span> <span data-ttu-id="4a7a6-165">若要更改上下文 cmdlet 的默认行为，请使用 `Scope` 参数。</span><span class="sxs-lookup"><span data-stu-id="4a7a6-165">To change the default behavior of context cmdlets, use the `Scope` parameter.</span></span> <span data-ttu-id="4a7a6-166">`Process` 范围使默认行为仅适用于当前会话，以此重写默认行为。</span><span class="sxs-lookup"><span data-stu-id="4a7a6-166">The `Process` scope overrides the default behavior by making it apply only for the current session.</span></span> <span data-ttu-id="4a7a6-167">与之相反，`CurrentUser` 范围会更改所有会话而不仅是当前会话中的上下文。</span><span class="sxs-lookup"><span data-stu-id="4a7a6-167">Conversely `CurrentUser` scope changes the context in all sessions, instead of just the current session.</span></span>

<span data-ttu-id="4a7a6-168">例如，若要更改当前 PowerShell 会话中的默认上下文且不影响其他会话时段或下次打开会话时使用的上下文，请使用:</span><span class="sxs-lookup"><span data-stu-id="4a7a6-168">As an example, to change the default context in the current PowerShell session without impacting other windows, or the context used the next time a session is opened, use:</span></span>

```powershell
PS C:\> Select-AzureRmContext Contoso1 -Scope Process
```

## <a name="how-the-context-autosave-setting-is-remembered"></a><span data-ttu-id="4a7a6-169">如何记住上下文自动保存设置</span><span class="sxs-lookup"><span data-stu-id="4a7a6-169">How the context autosave setting is remembered</span></span>

<span data-ttu-id="4a7a6-170">上下文自动保存设置保存到 Azure PowerShell 用户目录 (`%AppData%\Roaming\Windows Azure PowerShell`)。</span><span class="sxs-lookup"><span data-stu-id="4a7a6-170">The context AutoSave setting is saved to the user Azure PowerShell directory (`%AppData%\Roaming\Windows Azure PowerShell`).</span></span> <span data-ttu-id="4a7a6-171">某些类型的计算机帐户可能无权访问此目录。</span><span class="sxs-lookup"><span data-stu-id="4a7a6-171">Some kinds of computer accounts may not have access to this directory.</span></span> <span data-ttu-id="4a7a6-172">对于这种情况，可以使用环境变量</span><span class="sxs-lookup"><span data-stu-id="4a7a6-172">For such scenarios, you can use the environment variable</span></span>

```powershell
$env:AzureRmContextAutoSave="true" | "false"
```

<span data-ttu-id="4a7a6-173">如果设置为“true”，则自动保存上下文。</span><span class="sxs-lookup"><span data-stu-id="4a7a6-173">If set to 'true', the context is automatically saved.</span></span> <span data-ttu-id="4a7a6-174">如果设置为“false”，则不保存上下文。</span><span class="sxs-lookup"><span data-stu-id="4a7a6-174">If set to 'false', the context is not saved.</span></span>

## <a name="changes-to-the-azurermprofile-module"></a><span data-ttu-id="4a7a6-175">对 AzureRM.Profile 模块的更改</span><span class="sxs-lookup"><span data-stu-id="4a7a6-175">Changes to the AzureRM.Profile module</span></span>

<span data-ttu-id="4a7a6-176">用于管理上下文的新 cmdlet</span><span class="sxs-lookup"><span data-stu-id="4a7a6-176">New cmdlets for managing context</span></span>

- <span data-ttu-id="4a7a6-177">[Enable-AzureRmContextAutosave][enable] - 用于在不同的 PowerShell 会话中保存上下文。</span><span class="sxs-lookup"><span data-stu-id="4a7a6-177">[Enable-AzureRmContextAutosave][enable] - Allow saving the context between powershell sessions.</span></span>
  <span data-ttu-id="4a7a6-178">所做的任何更改都会更改全局上下文。</span><span class="sxs-lookup"><span data-stu-id="4a7a6-178">Any changes alter the global context.</span></span>
- <span data-ttu-id="4a7a6-179">[Disable-AzureRmContextAutosave][disable] - 关闭上下文自动保存。</span><span class="sxs-lookup"><span data-stu-id="4a7a6-179">[Disable-AzureRmContextAutosave][disable] - Turn off autosaving the context.</span></span> <span data-ttu-id="4a7a6-180">每打开一个新的 PowerShell 会话都需要重新登录。</span><span class="sxs-lookup"><span data-stu-id="4a7a6-180">Each new PowerShell session is required to log in again.</span></span>
- <span data-ttu-id="4a7a6-181">[Select-AzureRmContext][select] - 选择某个上下文作为默认值。</span><span class="sxs-lookup"><span data-stu-id="4a7a6-181">[Select-AzureRmContext][select] - Select a context as the default.</span></span> <span data-ttu-id="4a7a6-182">所有后续 cmdlet 都使用此上下文中的凭据进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="4a7a6-182">All subsequent cmdlets use the credentials in this context for authentication.</span></span>
- <span data-ttu-id="4a7a6-183">[Remove-AzureRmAccount][remove-cred] - 删除与帐户关联的所有凭据和上下文。</span><span class="sxs-lookup"><span data-stu-id="4a7a6-183">[Remove-AzureRmAccount][remove-cred] - Remove all credentials and contexts associated with an account.</span></span>
- <span data-ttu-id="4a7a6-184">[Remove-AzureRmContext][remove-context] - 删除命名的上下文。</span><span class="sxs-lookup"><span data-stu-id="4a7a6-184">[Remove-AzureRmContext][remove-context] - Remove a named context.</span></span>
- <span data-ttu-id="4a7a6-185">[Rename-AzureRmContext][rename] - 重命名现有上下文。</span><span class="sxs-lookup"><span data-stu-id="4a7a6-185">[Rename-AzureRmContext][rename] - Rename an existing context.</span></span>

<span data-ttu-id="4a7a6-186">对现有配置文件 cmdlet 的更改</span><span class="sxs-lookup"><span data-stu-id="4a7a6-186">Changes to existing profile cmdlets</span></span>

- <span data-ttu-id="4a7a6-187">[Add-AzureRmAccount][login] - 用于设置进程或当前用户的登录范围。</span><span class="sxs-lookup"><span data-stu-id="4a7a6-187">[Add-AzureRmAccount][login] - Allow scoping of the login to the process or the current user.</span></span>
  <span data-ttu-id="4a7a6-188">用于在登录后命名默认上下文。</span><span class="sxs-lookup"><span data-stu-id="4a7a6-188">Allow naming the default context after login.</span></span>
- <span data-ttu-id="4a7a6-189">[Import-AzureRmContext][import] - 用于设置进程或当前用户的登录范围。</span><span class="sxs-lookup"><span data-stu-id="4a7a6-189">[Import-AzureRmContext][import] - Allow scoping of the login to the process or the current user.</span></span>
- <span data-ttu-id="4a7a6-190">[Set-AzureRmContext][set-context] - 用于选择现有的命名上下文，以及设置对进程或当前用户的更改范围。</span><span class="sxs-lookup"><span data-stu-id="4a7a6-190">[Set-AzureRmContext][set-context] - Allow selection of existing named contexts, and scope changes to the process or current user.</span></span>

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
