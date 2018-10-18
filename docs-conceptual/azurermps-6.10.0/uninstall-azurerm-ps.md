---
title: 卸载 Azure PowerShell
description: 如何完整地卸载 Azure PowerShell
ms.date: 09/11/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 385dd0281185cfb9e7bdd2c98e4c557659fff384
ms.sourcegitcommit: f6f5e256143aa6c097de3e57e930d8badea49f30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2018
ms.locfileid: "49398985"
---
# <a name="uninstall-the-azure-powershell-module"></a>卸载 Azure PowerShell 模块

本文介绍如何卸载旧版 Azure PowerShell 或将其从系统中完全删除。 如果你决定彻底卸载 Azure PowerShell，请通过 [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet 为我们提供一些反馈。
如果你在遇到 bug 后[提出 GitHub 问题](https://github.com/azure/azure-powershell/issues)，我们将十分感激。

## <a name="uninstall-msi"></a>卸载 MSI

若是使用 MSI 包安装的 Azure PowerShell，则必须通过 Windows 系统而不是 PowerShell 进行卸载。

| 平台 | 说明 |
|----------|--------------|
| Windows 10 | “开始”>“设置”>“应用” |
| Windows 7 </br>Windows 8 | “开始”>“控制面板”>“程序”>“卸载程序” |

转到此屏幕以后，会在程序列表中看到“Azure PowerShell”，可以从该处卸载。

## <a name="uninstall-from-powershell"></a>从 PowerShell 卸载

若是使用 PowerShellGet 安装的 Azure PowerShell，则可使用 [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet。 但是，`Uninstall-Module` 只卸载一个模块。 若要彻底删除 Azure PowerShell，必须单独卸载每个模块。 如果安装了多个版本的 Azure PowerShell，则卸载过程可能很复杂。

以下脚本查询 PowerShell 库以获取依赖性子模块的列表。 然后，此脚本会卸载每个子模块的正确版本。

```powershell
function Uninstall-AllModules {
  param(
    [Parameter(Mandatory=$true)]
    [string]$TargetModule,

    [Parameter(Mandatory=$true)]
    [string]$Version,

    [switch]$Force
  )

  $AllModules = @()

  'Creating list of dependencies...'
  $target = Find-Module $TargetModule -RequiredVersion $version
  $target.Dependencies | ForEach-Object {
    $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$_.requiredversion}
  }
  $AllModules += New-Object -TypeName psobject -Property @{name=$TargetModule; version=$Version}

  foreach ($module in $AllModules) {
    Write-Host ('Uninstalling {0} version {1}' -f $module.name,$module.version)
    try {
      Uninstall-Module -Name $module.name -RequiredVersion $module.version -Force:$Force -ErrorAction Stop
    } catch {
      Write-Host ("`t" + $_.Exception.Message)
    }
  }
}
```

若要使用此函数，请将代码复制并粘贴到 PowerShell 会话中。 以下示例演示了如何运行此函数来删除旧版 Azure PowerShell。

```powershell
Uninstall-AllModules -TargetModule AzureRM -Version 4.4.1 -Force
```

此脚本在运行时会显示每个要卸载的子模块的名称和版本。

```output
Creating list of dependencies...
Uninstalling AzureRM.Profile version 3.4.1
Uninstalling Azure.Storage version 3.4.1
Uninstalling AzureRM.AnalysisServices version 0.4.7
Uninstalling Azure.AnalysisServices version 0.4.7
...
```

请针对要卸载的每个 Azure PowerShell 版本运行此命令。
