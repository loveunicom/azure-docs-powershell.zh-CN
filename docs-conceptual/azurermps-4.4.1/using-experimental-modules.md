---
title: 使用 Azure PowerShell 试验性模块
description: 了解 Azure PowerShell 试验性模块的思路和用法。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/05/2017
ms.openlocfilehash: 09858da9981c1136e2a39a079962c5b8fc39bde9
ms.sourcegitcommit: 06f9206e025afa7207d4657c8f57c94ddb74817a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/07/2018
ms.locfileid: "51211904"
---
# <a name="using-experimental-azure-powershell-modules"></a>使用 Azure PowerShell 试验性模块

Azure PowerShell 团队正在以 Azure 中的开发人员工具（尤其是 CLI）为重点，试验 Azure PowerShell 体验的诸多改进方案。

## <a name="experimentation-methodology"></a>试验方法

为便于试验，我们会创建新的 Azure PowerShell 模块，用于以更易于使用的全新方式实现现有的 Azure SDK 功能。 在大多数情况下，这些 cmdlet 能够准确对应现有 cmdlet。 但是，试验性 cmdlet 提供速记表示法和更智能化的默认值，使 Azure 资源的创建和管理变得更轻松。

这些模块可与现有的 Azure PowerShell 模块一同安装。 cmdlet 名称经过简化，因此变得更短，并可避免与现有的非试验性 cmdlet 名称相冲突。

试验性模块使用以下命名约定：`AzureRM.*.Experiments`。 此命名约定类似于预览版模块的命名：`AzureRM.*.Preview`。 预览版模块不同于试验性模块。 预览版模块实现仅以预览版产品的形式提供的新 Azure 服务功能。 预览版模块可取代现有的 Azure PowerShell 模块，使用相同的 cmdlet 和参数名称。

## <a name="how-to-install-an-experimental-module"></a>如何安装试验性模块

试验性模块像现有 Azure PowerShell 模块一样发布到 PowerShell 库。 若要查看实验性模块列表，请运行以下命令：

```powershell-interactive
Find-Module AzureRM.*.Experiments
```

```Output
Version Name                         Repository Description
------- ----                         ---------- -----------
1.0.25  AzureRM.Compute.Experiments  PSGallery  Azure Compute experiments for VM creation
1.0.0   AzureRM.Websites.Experiments PSGallery  Create and deploy web applications using Azure App Services.
```

若要安装试验性模块，请在权限提升的 PowerShell 会话中使用以下命令：

```powershell-interactive
Install-Module AzureRM.Compute.Experiments
Install-Module AzureRM.Websites.Experiments
```

### <a name="documentation-and-support"></a>文档和支持

文档随附在安装包中，可使用 `Get-Help` cmdlet 进行访问。 尚未发布试验性模块的官方文档。

我们建议测试这些模块。 各位的反馈可让我们改进可用性，并响应各位的需求。 但是，作为试验性产品，我们为这些模块提供的支持有限。 可以通过在 GitHub 存储库中创建[问题](https://github.com/Azure/azure-powershell/issues)来报告问题。

## <a name="experiments-and-areas-of-improvement"></a>试验和改进方面

这些改进项目是根据与竞争产品的重要差异而选择的。 例如，Azure CLI 2.0 的思路是以“方案”而不是“API 外围应用”作为命令的基础。
Azure CLI 2.0 使用大量的智能默认值，让最终用户更轻松地实现“入门”方案。

### <a name="core-improvements"></a>核心改进

核心改进被视为“常识”，无需太多试验即可进一步实现这些更新。

- 基于方案的 Cmdlet - *所有 cmdlet 都应该围绕方案而不是 Azure REST 服务来设计。

- 更短的名称 - 包含 cmdlet 的名称（例如 `New-AzureRmVM` => `New-AzVm`）和参数的名称（例如 `-ResourceGroupName` => `-Rg`）。 使用别名，以便与“旧”cmdlet 兼容。 提供可向后兼容的参数集。

- 智能默认值 - 创建智能默认值来填充“必需的”信息。 例如：
  - 资源组
  - 位置
  - 依赖资源

### <a name="experimental-improvements"></a>试验改进

试验改进提供团队想要通过试验进行验证的重大更改。

- 简单类型 - 创建方案应该避开复杂的类型和配置对象。 将配置简化为一到两个参数。

- “智能创建”- 实现“智能创建”的所有创建方案不包含必需的参数：Azure PowerShell 根据其“看法”选择所有必要的信息。

- 灰色参数 - 在许多情况下，某些参数可以是“灰色”的，或不完全可选的。 如果未指定参数，系统会要求用户确认是否要为其生成参数。 也可以让灰色参数在用户同意的情况下，根据上下文来推断值。
  例如，合理的做法是让灰色参数推荐最近使用的值。

- `-Auto` 开关 - `-Auto` 开关提供一种“选择”方式让用户指定为所有项使用默认值，同时在主线路径中保留所需参数的完整性。

### <a name="feature-specific-switches"></a>功能特定的开关

例如，“创建 Web 应用”方案可以包含 `-Git` 或 `-AddRemote` 开关，以便将“azure”远程存储库添加到现有的 git 存储库。

- 可设置的默认值 - 用户应该能够将某些普遍的参数（例如 `-ResourceGroupName` 和 `-Location`）设置为默认值。

- 大小默认值 - 用户可能对资源“大小”感到混淆，因为许多资源提供程序使用不同的名称（例如，“Standard\_DS1\_v2”或“S1”）。 但是，大多数用户更关心成本。 因此，根据定价计划定义“通用”大小会很有作用。 用户可以选择特定的大小，或者让 Azure PowerShell 根据资源预算选择最佳选项。

- 输出格式 - Azure PowerShell 目前返回 `PSObject`s，控制台输出信息很少。 Azure PowerShell 可能需要向用户显示一些有关所用“智能默认值”的信息。
