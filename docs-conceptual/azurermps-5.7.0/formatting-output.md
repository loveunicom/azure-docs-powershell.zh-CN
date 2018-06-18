---
title: 设置 Azure PowerShell cmdlet 的输出格式
description: 如何为 Azure PowerShell 设置 cmdlet 输出格式。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/07/2018
ms.openlocfilehash: 833c82903305f99be5ad43f707e22644bb568abe
ms.sourcegitcommit: bcf80dfd7fbe17e82e7ad029802cfe8a2f02b15c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "35323384"
---
# <a name="format-azurepowershell-cmdlet-output"></a>设置 AzurePowerShell cmdlet 的输出格式

默认情况下，每个 Azure PowerShell cmdlet 都有预定义的输出格式，使输出结果易于阅读。  PowerShell 还可让你使用以下 cmdlet 灵活调整输出，或者将 cmdlet 输出转换为不同的格式：

| 格式设置      | 转换       |
|-----------------|------------------|
| [Format-Custom](/powershell/module/microsoft.powershell.utility/format-custom) | [ConvertTo-Csv](/powershell/module/microsoft.powershell.utility/convertto-csv)  |
| [Format-List](/powershell/module/microsoft.powershell.utility/format-list)   | [ConvertTo-Html](/powershell/module/microsoft.powershell.utility/convertto-html) |
| [Format-Table](/powershell/module/microsoft.powershell.utility/format-table)  | [ConvertTo-Json](/powershell/module/microsoft.powershell.utility/convertto-json) |
| [Format-Wide](/powershell/module/microsoft.powershell.utility/format-wide)   | [ConvertTo-Xml](/powershell/module/microsoft.powershell.utility/convertto-xml)  |

## <a name="format-examples"></a>格式示例

此示例获取默认订阅中的 Azure VM 列表。  `Get-AzureRmVM` 命令默认将输出设置为表格式。

```azurepowershell-interactive
Get-AzureRmVM
```

```output
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

若要限制返回的列，可以使用 `Format-Table` cmdlet。 以下示例获取相同的虚拟机列表，但会将输出限制为只返回 VM 名称、资源组和 VM 位置。  `-Autosize` 参数根据数据大小调整列的大小。

```azurepowershell-interactive
Get-AzureRmVM | Format-Table Name,ResourceGroupName,Location -AutoSize
```

```output
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

还可以将输出格式设置为列表。 以下示例演示如何使用 `Format-List` cmdlet 以列表格式显示信息。

```azurepowershell-interactive
Get-AzureRmVM | Format-List Name,VmId,Location,ResourceGroupName
```

```output
Name              : MyUnbuntu1610
VmId              : 33422f9b-e339-4704-bad8-dbe094585496
Location          : westeurope
ResourceGroupName : MYWESTEURG

Name              : MyWin2016VM
VmId              : 4650c755-fc2b-4fc7-a5bc-298d5c00808f
Location          : westeurope
ResourceGroupName : MYWESTEURG
```

## <a name="convert-to-other-data-types"></a>转换为其他数据类型

PowerShell 还允许获取命令输出并将其转换为多种数据格式。 在以下示例中，`Select-Object` cmdlet 用来获取订阅中虚拟机的属性，然后将输出转换为 CSV 格式，以便将其导入数据库或电子表格中。

```azurepowershell-interactive
Get-AzureRmVM | Select-Object ResourceGroupName,Id,VmId,Name,Location,ProvisioningState | ConvertTo-Csv -NoTypeInformation
```

```output
"ResourceGroupName","Id","VmId","Name","Location","ProvisioningState"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyUnbuntu1610","33422f9b-e339-4704-bad8-dbe094585496","MyUnbuntu1610","westeurope","Succeeded"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyWin2016VM","4650c755-fc2b-4fc7-a5bc-298d5c00808f","MyWin2016VM","westeurope","Succeeded"
```

还可以将输出转换为 JSON 格式。  以下示例创建相同的 VM 列表，但会将输出格式更改为 JSON。

```azurepowershell-interactive
Get-AzureRmVM | Select-Object ResourceGroupName,Id,VmId,Name,Location,ProvisioningState | ConvertTo-Json
```

```output
[
    {
        "ResourceGroupName":  "MYWESTEURG",
        "Id":  "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTEURG/providers/Microsoft.Compute/virtualMachines/MyUnbuntu1610",
        "VmId":  "33422f9b-e339-4704-bad8-dbe094585496",
        "Name":  "MyUnbuntu1610",
        "Location":  "westeurope",
        "ProvisioningState":  "Succeeded"
    },
    {
        "ResourceGroupName":  "MYWESTEURG",
        "Id":  "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTEURG/providers/Microsoft.Compute/virtualMachines/MyWin2016VM",
        "VmId":  "4650c755-fc2b-4fc7-a5bc-298d5c00808f",
        "Name":  "MyWin2016VM",
        "Location":  "westeurope",
        "ProvisioningState":  "Succeeded"
    }
]
```
