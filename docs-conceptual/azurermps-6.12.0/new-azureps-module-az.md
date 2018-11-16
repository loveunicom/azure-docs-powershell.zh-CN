---
title: Azure Powershell Az 模块简介
description: 介绍新的 Azure PowerShell 模块 Az（AzureRM 模块的替代品）。
ms.date: 11/07/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: b0f31341d4344bdac5b4d657a1f66acfd9984dda
ms.sourcegitcommit: 4afdba3cd7e1d348876ce59f3503fdcd258f79ab
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/15/2018
ms.locfileid: "51574798"
---
# <a name="introducing-the-new-azure-powershell-az-module"></a>新 Azure Powershell Az 模块简介

从 2018 年 11 月起，Azure PowerShell `Az` 模块在完整公共预览版中提供。
Az 提供更短的命令，提高了稳定性，还支持 Windows、macOS 和 Linux。 Az 还提供与 AzureRM 的功能奇偶一致性以及轻松从 AzureRM 执行迁移的途径。

Az 使用 .NET Standard 库，这意味着它在 PowerShell 5.x 和 PowerShell 6.x 上运行。
由于 PowerShell 6.x 可以在 Linux、 macOS 和 Windows 上运行，因此这意味着 Az 对所有平台均可用。
使用 .NET Standard，我们可以在将对用户的影响降至最低的情况下统一 Azure PowerShell 的代码库。

Az 是新模块，因此版本已重置。 第一个稳定版本将是 1.0，但该模块与到 2018 年 11 月为止的 AzureRm 具有功能奇偶一致性。

## <a name="upgrade-to-az"></a>升级到 Az

我们建议用户升级到新的 `Az` 模块。 为此，请执行以下操作：

* [卸载 Azure PowerShell AzureRM 模块](/powershell/azure/uninstall-azurerm-ps)
* [安装 Azure PowerShell Az 模块](/powershell/azure/install-az-ps)
* 熟悉了新的命令集时，请使用 `Enable-AzureRMAlias` 为 AzureRM 启用兼容性模式。

## <a name="migrate-existing-scripts-to-az"></a>将现有脚本迁移到 Az

主要更新可能不方便。 但是，`Az` 模块具有兼容性模式，可帮助你在逐步掌握新语法的同时使用现有脚本。 使用 `Enable-AzureRmAlias` cmdlet 可启用 `AzureRM` 兼容性模式。 此 cmdlet 将 `AzureRM` cmdlet 名称定义为新 `Az` cmdlet 名称的别名。

新 cmdlet 名称已设计为易于学习。 请在 cmdlet 名称中使用 `Az`，而不是使用 `AzureRm` 或 `Azure`。 例如，旧命令 `New-AzureRmVm` 已变为 `New-AzVm`。

有关迁移过程的完整说明，请参阅[从 AzureRM 迁移到 Az](migrate-from-azurerm-to-az.md)。

## <a name="the-future-of-support-for-azurerm"></a>对 AzureRM 的支持的未来

`Az` 1.0 版在 2018 年 12 月发布时，现有 `AzureRM` 模块将不再接收新的 cmdlet 或功能。 但是，`AzureRM` 仍会受到正式维护，并且会获得 bug 修复。 若要及时了解最新的 Azure 服务和功能，应切换到 `Az` 模块。