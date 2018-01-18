---
title: "设置查询结果的格式 | Microsoft Docs"
description: "如何查询 Azure 中的资源以及设置结果的格式。"
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/30/2017
ms.openlocfilehash: 916cf8590de89762bade4f01ce5a502383d51796
ms.sourcegitcommit: d320fd5a2f468445c9e5aaa8d28dc363ece12ffc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/16/2018
---
# <a name="formatting-query-results"></a><span data-ttu-id="c3269-103">设置查询结果的格式</span><span class="sxs-lookup"><span data-stu-id="c3269-103">Formatting query results</span></span>

<span data-ttu-id="c3269-104">默认情况下，每个 PowerShell cmdlet 都有预定义的输出格式，使输出结果易于阅读。</span><span class="sxs-lookup"><span data-stu-id="c3269-104">By default each PowerShell cmdlet has predefined formatting of output making it easy to read.</span></span>  <span data-ttu-id="c3269-105">PowerShell 还可让你使用以下 cmdlet 灵活调整输出，或者将 cmdlet 输出转换为不同的格式：</span><span class="sxs-lookup"><span data-stu-id="c3269-105">PowerShell also provides the flexibility to adjust the output or convert the cmdlet output to a different format with the following cmdlets:</span></span>

| <span data-ttu-id="c3269-106">格式设置</span><span class="sxs-lookup"><span data-stu-id="c3269-106">Formatting</span></span>      | <span data-ttu-id="c3269-107">转换</span><span class="sxs-lookup"><span data-stu-id="c3269-107">Conversion</span></span>       |
|-----------------|------------------|
| `Format-Custom` | `ConvertTo-Csv`  |
| `Format-List`   | `ConvertTo-Html` |
| `Format-Table`  | `ConvertTo-Json` |
| `Format-Wide`   | `ConvertTo-Xml`  |

## <a name="formatting-examples"></a><span data-ttu-id="c3269-108">格式设置示例</span><span class="sxs-lookup"><span data-stu-id="c3269-108">Formatting examples</span></span>

<span data-ttu-id="c3269-109">此示例获取默认订阅中的 Azure VM 列表。</span><span class="sxs-lookup"><span data-stu-id="c3269-109">In this example we get a list of Azure VMs in our default subscription.</span></span>  <span data-ttu-id="c3269-110">Get-AzureRmVM 命令将输出默认设置为表格式。</span><span class="sxs-lookup"><span data-stu-id="c3269-110">The Get-AzureRmVM command defaults output into a table format.</span></span>

```powershell
Get-AzureRmVM
```

```
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

<span data-ttu-id="c3269-111">若要限制返回的列，可以使用 `Format-Table` cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c3269-111">If you would like to limit the columns returned you can use the `Format-Table` cmdlet.</span></span> <span data-ttu-id="c3269-112">以下示例获取相同的虚拟机列表，但会将输出限制为只返回 VM 名称、资源组和 VM 位置。</span><span class="sxs-lookup"><span data-stu-id="c3269-112">In the following example we get the same list of virtual machines but restrict the output to just the name of the VM, the resource group, and the location of the VM.</span></span>  <span data-ttu-id="c3269-113">`-Autosize` 参数根据数据大小调整列的大小。</span><span class="sxs-lookup"><span data-stu-id="c3269-113">The `-Autosize` parameter sizes the columns according to the size of the data.</span></span>

```powershell
Get-AzureRmVM | Format-Table Name,ResourceGroupName,Location -AutoSize
```

```
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

<span data-ttu-id="c3269-114">如果需要，可使用列表格式查看信息。</span><span class="sxs-lookup"><span data-stu-id="c3269-114">If you would prefer you can view information in a list format.</span></span> <span data-ttu-id="c3269-115">以下示例演示如何使用 `Format-List` cmdlet 以列表格式显示信息。</span><span class="sxs-lookup"><span data-stu-id="c3269-115">The following example shows this using the`Format-List` cmdlet.</span></span>

```powershell
Get-AzureRmVM | Format-List Name,VmId,Location,ResourceGroupName
```

```
Name              : MyUnbuntu1610
VmId              : 33422f9b-e339-4704-bad8-dbe094585496
Location          : westeurope
ResourceGroupName : MYWESTEURG

Name              : MyWin2016VM
VmId              : 4650c755-fc2b-4fc7-a5bc-298d5c00808f
Location          : westeurope
ResourceGroupName : MYWESTEURG
```

## <a name="converting-to-other-data-types"></a><span data-ttu-id="c3269-116">转换为其他数据类型</span><span class="sxs-lookup"><span data-stu-id="c3269-116">Converting to other data types</span></span>

<span data-ttu-id="c3269-117">PowerShell 还提供多种输出格式，可以根据需要使用不同的格式。</span><span class="sxs-lookup"><span data-stu-id="c3269-117">PowerShell also offers multiple output format you can use to meet your needs.</span></span>  <span data-ttu-id="c3269-118">以下示例使用 `Select-Object` cmdlet 获取订阅中虚拟机的属性，然后将输出转换为 CSV 格式，以方便导入数据库或电子表格。</span><span class="sxs-lookup"><span data-stu-id="c3269-118">In the following example we use the `Select-Object` cmdlet to get attributes of the virtual machines in our subscription and and convert the output to CSV format for easy import into a database or spreadsheet.</span></span>

```powershell
Get-AzureRmVM | Select-Object ResourceGroupName,Id,VmId,Name,Location,ProvisioningState | ConvertTo-Csv -NoTypeInformation
```

```
"ResourceGroupName","Id","VmId","Name","Location","ProvisioningState"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyUnbuntu1610","33422f9b-e339-4704-bad8-dbe094585496","MyUnbuntu1610","westeurope","Succeeded"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyWin2016VM","4650c755-fc2b-4fc7-a5bc-298d5c00808f","MyWin2016VM","westeurope","Succeeded"
```

<span data-ttu-id="c3269-119">还可以将输出转换为 JSON 格式。</span><span class="sxs-lookup"><span data-stu-id="c3269-119">You can also convert the output into JSON format.</span></span>  <span data-ttu-id="c3269-120">以下示例创建相同的 VM 列表，但会将输出格式更改为 JSON。</span><span class="sxs-lookup"><span data-stu-id="c3269-120">The following example creates the same list of VMs but changes the output format to JSON.</span></span>

```powershell
Get-AzureRmVM | Select-Object ResourceGroupName,Id,VmId,Name,Location,ProvisioningState | ConvertTo-Json
```

```
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
