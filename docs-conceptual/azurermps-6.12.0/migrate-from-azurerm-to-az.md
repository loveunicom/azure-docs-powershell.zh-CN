---
title: 将 Azure PowerShell 脚本从 AzureRM 迁移到 Az
description: 了解有关将脚本从 AzureRM 模块迁移到新 Az 模块的步骤和工具。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/07/2018
ms.openlocfilehash: 0c73e7ac1d47a2a97b6136fa481d0adce8de33db
ms.sourcegitcommit: ac4b53bb42a25aae013a9d8cd9ae98ada9397274
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/08/2018
ms.locfileid: "51274886"
---
# <a name="migrate-from-azurerm-to-azure-powershell-az"></a>从 AzureRM 迁移到 Azure PowerShell Az

Az 模块与 AzureRM 具有功能奇偶一致性，但 Az 模块使用更短且更一致的 cmdlet 名称。
为 AzureRM cmdlet 编写的脚本不会自动与新模块配合工作。 为了简化转换，Az 提供了工具，以便你可以使用 AzureRM 运行现有的脚本。 不迁移到新的命令集十分省事，但本文将帮助你开始转换到新的模块。

## <a name="ensure-your-existing-scripts-work-with-the-latest-azurerm-release"></a>请确保现有的脚本与最新的 AzureRM 版本配合工作

这是最重要的步骤！ 运行现有的脚本，并确保它们与最新版本的 AzureRM (__6.12.0__) 配合工作。 如果脚本不起作用，请务必阅读 [AzureRM 迁移指南](migration-guide.6.0.0.md)。

## <a name="install-the-azure-powershell-az-module"></a>安装 Azure Powershell Az 模块

第一步是在平台上安装 Az 模块。 若要安装 Az，需要卸载 AzureRM。
以下步骤将介绍如何继续运行现有脚本并为旧 cmdlet 名称启用兼容性。

若要安装 Azure PowerShell Az 模块，请执行以下步骤：

* [卸载 AzureRM 模块](uninstall-azurerm-ps.md)。 请确保删除所有已安装的 AzureRM 版本，不只是最新版本。
* [安装 Az 模块](install-az-ps.md)

## <a name="a-namealiasesenable-azurerm-alias-mode"></a><a name="aliases"/>启用 AzureRM 别名模式

卸载了 AzureRM 并且脚本已与最新的 AzureRM 版本配合工作，现在可以为 Az 模块启用兼容性模式。 使用以下命令启用兼容性：

```powershell-interactive
Enable-AzureRmAlias -Scope CurrentUser
```

在安装了 `Az` 模块的情况下，通过别名可以使用旧 cmdlet 名称。 这些别名会写入到所选范围的用户配置文件。 如果不存在用户配置文件，则会创建一个。

> [!WARNING]
>
> 可以为此命令使用其他 `-Scope`，但不建议这样做！ 别名会写入到所选范围的用户配置文件，因此请保持将其启用到尽可能有限的范围。 在系统范围内启用别名也可能会导致已在其本地范围内安装 `AzureRM` 的其他用户出现问题。

启用别名模式后，请再次运行脚本以确认它们仍然正常运行。 

## <a name="change-module-imports-and-cmdlet-names"></a>更改模块导入和 cmdlet 名称

一般情况下，模块名称已更改，以便 `AzureRM` 和 `Azure` 变为 `Az`，对于 cmdlet 也是如此。
例如，`AzureRM.Compute` 模块已重命名为 `Az.Compute`。 `New-AzureRmVM` 已变为 `New-AzVM`，并且 `Get-AzureStorageBlob` 现在为 `Get-AzStorageBlob`。

执行任何重命名之前，应注意此命名更改有一些例外：

| AzureRM 模块 | Az 模块 |
|----------------|-----------|
| AzureRM.DataFactories | Az.DataFactory |
| AzureRM.DataFactoryV2 | Az.DataFactory |
| AzureRM.RecoveryServices.Backup | Az.RecoveryServices |
| AzureRM.RecoveryServices.SiteRecovery | Az.RecoveryServices |

## <a name="summary"></a>摘要

按照以下步骤操作，可以更新所有现有脚本以使用新模块。 如果对这些步骤有任何疑问或问题，使得迁移难于执行，请对本文发表评论，以便我们可以改进说明。