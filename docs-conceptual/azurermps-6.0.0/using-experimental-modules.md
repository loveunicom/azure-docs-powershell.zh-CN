---
title: 使用 Azure PowerShell 试验性模块
description: 了解 Azure PowerShell 试验性模块的思路和用法。
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/05/2017
ms.openlocfilehash: c11e4503c07b0a0c4a71021bc511da723098188e
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/08/2018
---
# <a name="using-experimental-azure-powershell-modules"></a><span data-ttu-id="d5a32-103">使用 Azure PowerShell 试验性模块</span><span class="sxs-lookup"><span data-stu-id="d5a32-103">Using experimental Azure PowerShell modules</span></span>

<span data-ttu-id="d5a32-104">Azure PowerShell 团队正在以 Azure 中的开发人员工具（尤其是 CLI）为重点，试验 Azure PowerShell 体验的诸多改进方案。</span><span class="sxs-lookup"><span data-stu-id="d5a32-104">With the emphasis on developer tools (especially CLIs) in Azure, the Azure PowerShell team is experimenting with many improvements to the Azure PowerShell experience.</span></span>

## <a name="experimentation-methodology"></a><span data-ttu-id="d5a32-105">试验方法</span><span class="sxs-lookup"><span data-stu-id="d5a32-105">Experimentation methodology</span></span>

<span data-ttu-id="d5a32-106">为便于试验，我们会创建新的 Azure PowerShell 模块，用于以更易于使用的全新方式实现现有的 Azure SDK 功能。</span><span class="sxs-lookup"><span data-stu-id="d5a32-106">To facilitate experimentation, we are creating new Azure PowerShell modules that implement existing Azure SDK functionality in new, easier to use ways.</span></span> <span data-ttu-id="d5a32-107">在大多数情况下，这些 cmdlet 能够准确对应现有 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d5a32-107">In most cases, the cmdlets exactly mirror existing cmdlets.</span></span> <span data-ttu-id="d5a32-108">但是，试验性 cmdlet 提供速记表示法和更智能化的默认值，使 Azure 资源的创建和管理变得更轻松。</span><span class="sxs-lookup"><span data-stu-id="d5a32-108">However, the experimental cmdlets provide a shorthand notation and smarter default values that make it easier to create and manage Azure resources.</span></span>

<span data-ttu-id="d5a32-109">这些模块可与现有的 Azure PowerShell 模块一同安装。</span><span class="sxs-lookup"><span data-stu-id="d5a32-109">These modules can be installed side-by-side with existing Azure PowerShell modules.</span></span> <span data-ttu-id="d5a32-110">cmdlet 名称经过简化，因此变得更短，并可避免与现有的非试验性 cmdlet 名称相冲突。</span><span class="sxs-lookup"><span data-stu-id="d5a32-110">The cmdlet names have been shortened to provide shorter names and avoid name conflicts with existing, non-experimental cmdlets.</span></span>

<span data-ttu-id="d5a32-111">试验性模块使用以下命名约定：`AzureRM.*.Experiments`。</span><span class="sxs-lookup"><span data-stu-id="d5a32-111">The experimental modules use the following naming convention: `AzureRM.*.Experiments`.</span></span> <span data-ttu-id="d5a32-112">此命名约定类似于预览版模块的命名：`AzureRM.*.Preview`。</span><span class="sxs-lookup"><span data-stu-id="d5a32-112">This naming convention is similar to the naming of Preview modules: `AzureRM.*.Preview`.</span></span> <span data-ttu-id="d5a32-113">预览版模块不同于试验性模块。</span><span class="sxs-lookup"><span data-stu-id="d5a32-113">Preview modules differ from experimental modules.</span></span> <span data-ttu-id="d5a32-114">预览版模块实现仅以预览版产品的形式提供的新 Azure 服务功能。</span><span class="sxs-lookup"><span data-stu-id="d5a32-114">Preview modules implement new functionality of Azure services that is only available as a Preview offering.</span></span> <span data-ttu-id="d5a32-115">预览版模块可取代现有的 Azure PowerShell 模块，使用相同的 cmdlet 和参数名称。</span><span class="sxs-lookup"><span data-stu-id="d5a32-115">Preview modules replace existing Azure PowerShell modules and use the same cmdlet and parameter names.</span></span>

## <a name="how-to-install-an-experimental-module"></a><span data-ttu-id="d5a32-116">如何安装试验性模块</span><span class="sxs-lookup"><span data-stu-id="d5a32-116">How to install an experimental module</span></span>

<span data-ttu-id="d5a32-117">试验性模块像现有 Azure PowerShell 模块一样发布到 PowerShell 库。</span><span class="sxs-lookup"><span data-stu-id="d5a32-117">Experimental modules are published to the PowerShell Gallery just like the existing Azure PowerShell modules.</span></span> <span data-ttu-id="d5a32-118">若要查看实验性模块列表，请运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="d5a32-118">To see a list of experimental modules, run the following command:</span></span>

```powershell
Find-Module AzureRM.*.Experiments
```

```Output
Version Name                         Repository Description
------- ----                         ---------- -----------
1.0.25  AzureRM.Compute.Experiments  PSGallery  Azure Compute experiments for VM creation
1.0.0   AzureRM.Websites.Experiments PSGallery  Create and deploy web applications using Azure App Services.
```

<span data-ttu-id="d5a32-119">若要安装试验性模块，请在权限提升的 PowerShell 会话中使用以下命令：</span><span class="sxs-lookup"><span data-stu-id="d5a32-119">To install the experimental module, use the following commands from an elevated PowerShell session:</span></span>

```powershell
Install-Module AzureRM.Compute.Experiments
Install-Module AzureRM.Websites.Experiments
```

### <a name="documentation-and-support"></a><span data-ttu-id="d5a32-120">文档和支持</span><span class="sxs-lookup"><span data-stu-id="d5a32-120">Documentation and support</span></span>

<span data-ttu-id="d5a32-121">文档随附在安装包中，可使用 `Get-Help` cmdlet 进行访问。</span><span class="sxs-lookup"><span data-stu-id="d5a32-121">Documentation is included in the install package and is accessed using the `Get-Help` cmdlet.</span></span> <span data-ttu-id="d5a32-122">尚未发布试验性模块的官方文档。</span><span class="sxs-lookup"><span data-stu-id="d5a32-122">No official documentation is published for experimental modules.</span></span>

<span data-ttu-id="d5a32-123">我们建议测试这些模块。</span><span class="sxs-lookup"><span data-stu-id="d5a32-123">We encourage you to test these modules.</span></span> <span data-ttu-id="d5a32-124">各位的反馈可让我们改进可用性，并响应各位的需求。</span><span class="sxs-lookup"><span data-stu-id="d5a32-124">Your feedback allows us to improve usability and respond to your needs.</span></span> <span data-ttu-id="d5a32-125">但是，作为试验性产品，我们为这些模块提供的支持有限。</span><span class="sxs-lookup"><span data-stu-id="d5a32-125">However, being experimental, support for these modules is limited.</span></span> <span data-ttu-id="d5a32-126">可以通过在 GitHub 存储库中创建[问题](https://github.com/Azure/azure-powershell/issues)来报告问题。</span><span class="sxs-lookup"><span data-stu-id="d5a32-126">Questions or problem reports can be submitted by creating an [issue](https://github.com/Azure/azure-powershell/issues) in the GitHub repository.</span></span>

## <a name="experiments-and-areas-of-improvement"></a><span data-ttu-id="d5a32-127">试验和改进方面</span><span class="sxs-lookup"><span data-stu-id="d5a32-127">Experiments and areas of improvement</span></span>

<span data-ttu-id="d5a32-128">这些改进项目是根据与竞争产品的重要差异而选择的。</span><span class="sxs-lookup"><span data-stu-id="d5a32-128">These improvements were selected based on key differentiators in competing products.</span></span> <span data-ttu-id="d5a32-129">例如，Azure CLI 2.0 的思路是以“方案”而不是“API 外围应用”作为命令的基础。</span><span class="sxs-lookup"><span data-stu-id="d5a32-129">For example, Azure CLI 2.0 has made a point of basing commands on _scenarios_ rather than _API surface area_.</span></span>
<span data-ttu-id="d5a32-130">Azure CLI 2.0 使用大量的智能默认值，让最终用户更轻松地实现“入门”方案。</span><span class="sxs-lookup"><span data-stu-id="d5a32-130">Azure CLI 2.0 use a number of smart defaults that make "getting started" scenarios easier for end users.</span></span>

### <a name="core-improvements"></a><span data-ttu-id="d5a32-131">核心改进</span><span class="sxs-lookup"><span data-stu-id="d5a32-131">Core improvements</span></span>

<span data-ttu-id="d5a32-132">核心改进被视为“常识”，无需太多试验即可进一步实现这些更新。</span><span class="sxs-lookup"><span data-stu-id="d5a32-132">The core improvements are regarded as "common sense", and little experimentation is needed to move forward in implementing these updates.</span></span>

- <span data-ttu-id="d5a32-133">基于方案的 Cmdlet - \*所有 cmdlet 都应该围绕方案而不是 Azure REST 服务来设计。</span><span class="sxs-lookup"><span data-stu-id="d5a32-133">Scenario-based Cmdlets - \**All*- cmdlets should be designed around scenarios, not the Azure REST service.</span></span>

- <span data-ttu-id="d5a32-134">更短的名称 - 包含 cmdlet 的名称（例如 `New-AzureRmVM` => `New-AzVm`）和参数的名称（例如 `-ResourceGroupName` => `-Rg`）。</span><span class="sxs-lookup"><span data-stu-id="d5a32-134">Shorter Names - Includes the names of cmdlets (for example, `New-AzureRmVM` => `New-AzVm`) and the names of parameters (for example, `-ResourceGroupName` => `-Rg`).</span></span> <span data-ttu-id="d5a32-135">使用别名，以便与“旧”cmdlet 兼容。</span><span class="sxs-lookup"><span data-stu-id="d5a32-135">Use aliases for compatibility with "old" cmdlets.</span></span> <span data-ttu-id="d5a32-136">提供可向后兼容的参数集。</span><span class="sxs-lookup"><span data-stu-id="d5a32-136">Provide _backwards compatible_ parameter sets.</span></span>

- <span data-ttu-id="d5a32-137">智能默认值 - 创建智能默认值来填充“必需的”信息。</span><span class="sxs-lookup"><span data-stu-id="d5a32-137">Smart Defaults - Create smart defaults to fill in "required" information.</span></span> <span data-ttu-id="d5a32-138">例如：</span><span class="sxs-lookup"><span data-stu-id="d5a32-138">For example:</span></span>
  - <span data-ttu-id="d5a32-139">资源组</span><span class="sxs-lookup"><span data-stu-id="d5a32-139">Resource Group</span></span>
  - <span data-ttu-id="d5a32-140">Location</span><span class="sxs-lookup"><span data-stu-id="d5a32-140">Location</span></span>
  - <span data-ttu-id="d5a32-141">依赖资源</span><span class="sxs-lookup"><span data-stu-id="d5a32-141">Dependent resources</span></span>

### <a name="experimental-improvements"></a><span data-ttu-id="d5a32-142">试验改进</span><span class="sxs-lookup"><span data-stu-id="d5a32-142">Experimental improvements</span></span>

<span data-ttu-id="d5a32-143">试验改进提供团队想要通过试验进行验证的重大更改。</span><span class="sxs-lookup"><span data-stu-id="d5a32-143">The experimental improvements present a significant change that the team wants to validate via experimentation.</span></span>

- <span data-ttu-id="d5a32-144">简单类型 - 创建方案应该避开复杂的类型和配置对象。</span><span class="sxs-lookup"><span data-stu-id="d5a32-144">Simple types - Create scenarios should move away from complex types and config objects.</span></span> <span data-ttu-id="d5a32-145">将配置简化为一到两个参数。</span><span class="sxs-lookup"><span data-stu-id="d5a32-145">Simplify the configuration down to one or two parameters.</span></span>

- <span data-ttu-id="d5a32-146">“智能创建”- 实现“智能创建”的所有创建方案不包含必需的参数：Azure PowerShell 根据其“看法”选择所有必要的信息。</span><span class="sxs-lookup"><span data-stu-id="d5a32-146">"Smart Create" - All create scenarios implementing "Smart Create" would have _no_ required parameters: all necessary information would be chosen by Azure PowerShell in an opinionated fashion.</span></span>

- <span data-ttu-id="d5a32-147">灰色参数 - 在许多情况下，某些参数可以是“灰色”的，或不完全可选的。</span><span class="sxs-lookup"><span data-stu-id="d5a32-147">Gray Parameters - In many cases, some parameters could be "gray" or semi-optional.</span></span> <span data-ttu-id="d5a32-148">如果未指定参数，系统会要求用户确认是否要为其生成参数。</span><span class="sxs-lookup"><span data-stu-id="d5a32-148">If the parameter is not specified, the user is asked if they want the parameter generated for them.</span></span> <span data-ttu-id="d5a32-149">也可以让灰色参数在用户同意的情况下，根据上下文来推断值。</span><span class="sxs-lookup"><span data-stu-id="d5a32-149">It also makes sense for gray parameters to infer a value based on context with the user's consent.</span></span>
  <span data-ttu-id="d5a32-150">例如，合理的做法是让灰色参数推荐最近使用的值。</span><span class="sxs-lookup"><span data-stu-id="d5a32-150">For example, it may make sense to have the gray parameter suggest the most recently used value.</span></span>

- <span data-ttu-id="d5a32-151">`-Auto` 开关 - `-Auto` 开关提供一种“选择”方式让用户指定为所有项使用默认值，同时在主线路径中保留所需参数的完整性。</span><span class="sxs-lookup"><span data-stu-id="d5a32-151">`-Auto` Switch - The `-Auto` switch would provide an "opt-in" way for users to _default all the things_ while maintaining the integrity of required parameters in the mainline path.</span></span>

### <a name="feature-specific-switches"></a><span data-ttu-id="d5a32-152">功能特定的开关</span><span class="sxs-lookup"><span data-stu-id="d5a32-152">Feature-specific switches</span></span>

<span data-ttu-id="d5a32-153">例如，“创建 Web 应用”方案可以包含 `-Git` 或 `-AddRemote` 开关，以便将“azure”远程存储库添加到现有的 git 存储库。</span><span class="sxs-lookup"><span data-stu-id="d5a32-153">For example, the "Create web app" scenario might have a `-Git` or `-AddRemote` switch that would automatically add an "azure" remote to an existing git repository.</span></span>

- <span data-ttu-id="d5a32-154">可设置的默认值 - 用户应该能够将某些普遍的参数（例如 `-ResourceGroupName` 和 `-Location`）设置为默认值。</span><span class="sxs-lookup"><span data-stu-id="d5a32-154">Settable Defaults - Users should have the ability to default certain ubiquitous parameters like `-ResourceGroupName` and `-Location`.</span></span>

- <span data-ttu-id="d5a32-155">大小默认值 - 用户可能对资源“大小”感到混淆，因为许多资源提供程序使用不同的名称（例如，“Standard\_DS1\_v2”或“S1”）。</span><span class="sxs-lookup"><span data-stu-id="d5a32-155">Size Defaults - Resource "sizes" can be confusing to users since many Resource Providers use different names (for example, "Standard\_DS1\_v2" or "S1").</span></span> <span data-ttu-id="d5a32-156">但是，大多数用户更关心成本。</span><span class="sxs-lookup"><span data-stu-id="d5a32-156">However, most users care more about cost.</span></span> <span data-ttu-id="d5a32-157">因此，根据定价计划定义“通用”大小会很有作用。</span><span class="sxs-lookup"><span data-stu-id="d5a32-157">Therefore, it makes sense to define "universal" sizes based on a pricing schedule.</span></span> <span data-ttu-id="d5a32-158">用户可以选择特定的大小，或者让 Azure PowerShell 根据资源预算选择最佳选项。</span><span class="sxs-lookup"><span data-stu-id="d5a32-158">Users can choose a specific size or let Azure PowerShell choose the _best option_ based on the resource the budget.</span></span>

- <span data-ttu-id="d5a32-159">输出格式 - Azure PowerShell 目前返回 `PSObject`s，控制台输出信息很少。</span><span class="sxs-lookup"><span data-stu-id="d5a32-159">Output Format - Azure PowerShell currently returns `PSObject`s and there is little console output.</span></span> <span data-ttu-id="d5a32-160">Azure PowerShell 可能需要向用户显示一些有关所用“智能默认值”的信息。</span><span class="sxs-lookup"><span data-stu-id="d5a32-160">Azure PowerShell may need to display some information to the user regarding the "smart defaults" used.</span></span>
