---
title: Azure PowerShell cmdlet 的查询输出
description: 如何查询 Azure 中的资源以及设置结果的格式。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/08/2018
ms.openlocfilehash: daa39ada5b4e969264b6e8596dc7b090bb196fd5
ms.sourcegitcommit: 971f19181b2cd68b7845bbebdb22858c06541c8c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/06/2018
ms.locfileid: "43383730"
---
# <a name="query-output-of-azure-powershell-cmdlets"></a>Azure PowerShell cmdlet 的查询输出

可以在 PowerShell 中使用内置的 cmdlet 完成查询。 在 PowerShell 中，cmdlet 名称采用 **_动词-名词_** 格式。 使用动词 **_Get_** 的 cmdlet 是查询 cmdlet。 cmdlet 名词是 cmdlet 动词处理的 Azure 资源的类型。

## <a name="select-simple-properties"></a>选择简单属性

Azure PowerShell 为每个 cmdlet 定义了默认格式。 每种资源类型的最常见属性自动以表或列表格式显示。 有关设置输出格式的详细信息，请参阅[设置查询结果的格式](formatting-output.md)。

使用 `Get-AzureRmVM` cmdlet 可以查询帐户中的 VM 列表。

```azurepowershell-interactive
Get-AzureRmVM
```

默认输出自动设置为表格式。

```output
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

可以使用 `Select-Object` cmdlet 选择所需的特定属性。

```azurepowershell-interactive
Get-AzureRmVM | Select Name,ResourceGroupName,Location
```

```output
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

## <a name="select-complex-nested-properties"></a>选择复杂的嵌套属性

如果要选择的属性嵌套在 JSON 输出中的深层位置，则需要提供该嵌套属性的完整路径。 以下示例演示如何从 `Get-AzureRmVM` cmdlet 选择 VM 名称和 OS 类型。

```azurepowershell-interactive
Get-AzureRmVM | Select Name,@{Name='OSType'; Expression={$_.StorageProfile.OSDisk.OSType}}
```

```output
Name           OSType
----           ------
MyUnbuntu1610   Linux
MyWin2016VM   Windows
```

## <a name="filter-results-with-the-where-object-cmdlet"></a>使用 Where-Object cmdlet 筛选结果

使用 `Where-Object` cmdlet 可以根据任何属性值筛选结果。 在以下示例中，筛选器仅选择名称中包含文本“RGD”的 VM。

```azurepowershell-interactive
Get-AzureRmVM | Where ResourceGroupName -like RGD* | Select ResourceGroupName,Name
```

```output
ResourceGroupName  Name
-----------------  ----
RGDEMO001          KBDemo001VM
RGDEMO001          KBDemo020
```

在下一个示例中，结果将返回 vmSize 为“Standard_DS1_V2”的 VM。

```azurepowershell-interactive
Get-AzureRmVM | Where vmSize -eq Standard_DS1_V2
```

```output
ResourceGroupName          Name     Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----     --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610   westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM   westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```