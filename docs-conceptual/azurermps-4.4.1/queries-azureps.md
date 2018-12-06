---
title: 查询 Azure 资源和设置结果的格式 | Microsoft Docs
description: 如何查询 Azure 中的资源以及设置结果的格式。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/30/2017
ms.openlocfilehash: 9a7627a25f9bbd196b1d615229e45a6e1ce7a7d9
ms.sourcegitcommit: 93f93b90ef88c2659be95f3acaba514fe9639169
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2018
ms.locfileid: "52828478"
---
# <a name="querying-for-azure-resources"></a>查询 Azure 资源

可以在 PowerShell 中使用内置的 cmdlet 完成查询。 在 PowerShell 中，cmdlet 名称采用 **_动词-名词_** 格式。 使用动词 **_Get_** 的 cmdlet 是查询 cmdlet。 cmdlet 名词是 cmdlet 动词处理的 Azure 资源的类型。

## <a name="selecting-simple-properties"></a>选择简单属性

Azure PowerShell 为每个 cmdlet 定义了默认格式。 每种资源类型的最常见属性自动以表或列表格式显示。 有关设置输出格式的详细信息，请参阅[设置查询结果的格式](formatting-output.md)。

使用 `Get-AzureRmVM` cmdlet 可以查询帐户中的 VM 列表。

```powershell-interactive
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

```powershell-interactive
Get-AzureRmVM | Select Name,ResourceGroupName,Location
```

```output
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

## <a name="selecting-complex-nested-properties"></a>选择复杂的嵌套属性

如果要选择的属性嵌套在 JSON 输出中的深层位置，则需要提供该嵌套属性的完整路径。 以下示例演示如何从 `Get-AzureRmVM` cmdlet 选择 VM 名称和 OS 类型。

```powershell-interactive
Get-AzureRmVM | Select Name,@{Name='OSType'; Expression={$_.StorageProfile.OSDisk.OSType}}
```

```output
Name           OSType
----           ------
MyUnbuntu1610   Linux
MyWin2016VM   Windows
```

## <a name="filter-result-using-the-where-object-cmdlet"></a>使用 Where-Object cmdlet 筛选结果

使用 `Where-Object` cmdlet 可以根据任何属性值筛选结果。 在以下示例中，筛选器仅选择名称中包含文本“RGD”的 VM。

```powershell-interactive
Get-AzureRmVM | Where ResourceGroupName -like RGD* | Select ResourceGroupName,Name
```

```output
ResourceGroupName  Name
-----------------  ----
RGDEMO001          KBDemo001VM
RGDEMO001          KBDemo020
```

在下一个示例中，结果将返回 vmSize 为“Standard_DS1_V2”的 VM。

```powershell-interactive
Get-AzureRmVM | Where vmSize -eq Standard_DS1_V2
```

```output
ResourceGroupName          Name     Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----     --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610   westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM   westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```
