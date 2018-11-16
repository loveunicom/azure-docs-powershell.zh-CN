---
title: 设置 Azure PowerShell cmdlet 的输出格式
description: 如何为 Azure PowerShell 设置 cmdlet 输出格式。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/09/2018
ms.openlocfilehash: 390285bcf483e75b7a2b77d345ccb108669f66e5
ms.sourcegitcommit: 4afdba3cd7e1d348876ce59f3503fdcd258f79ab
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/15/2018
ms.locfileid: "51575512"
---
# <a name="format-azurepowershell-cmdlet-output"></a><span data-ttu-id="7f68d-103">设置 AzurePowerShell cmdlet 的输出格式</span><span class="sxs-lookup"><span data-stu-id="7f68d-103">Format AzurePowerShell cmdlet output</span></span>

<span data-ttu-id="7f68d-104">默认情况下，每个 Azure PowerShell cmdlet 都有预定义的输出格式，使输出结果易于阅读。</span><span class="sxs-lookup"><span data-stu-id="7f68d-104">By default each Azure PowerShell cmdlet has predefined formatting of output making it easy to read.</span></span>  <span data-ttu-id="7f68d-105">PowerShell 还可让你使用以下 cmdlet 灵活调整输出，或者将 cmdlet 输出转换为不同的格式：</span><span class="sxs-lookup"><span data-stu-id="7f68d-105">PowerShell also provides the flexibility to adjust the output or convert the cmdlet output to a different format with the following cmdlets:</span></span>

| <span data-ttu-id="7f68d-106">格式设置</span><span class="sxs-lookup"><span data-stu-id="7f68d-106">Formatting</span></span>      | <span data-ttu-id="7f68d-107">转换</span><span class="sxs-lookup"><span data-stu-id="7f68d-107">Conversion</span></span>       |
|-----------------|------------------|
| [<span data-ttu-id="7f68d-108">Format-Custom</span><span class="sxs-lookup"><span data-stu-id="7f68d-108">Format-Custom</span></span>](/powershell/module/microsoft.powershell.utility/format-custom) | [<span data-ttu-id="7f68d-109">ConvertTo-Csv</span><span class="sxs-lookup"><span data-stu-id="7f68d-109">ConvertTo-Csv</span></span>](/powershell/module/microsoft.powershell.utility/convertto-csv)  |
| [<span data-ttu-id="7f68d-110">Format-List</span><span class="sxs-lookup"><span data-stu-id="7f68d-110">Format-List</span></span>](/powershell/module/microsoft.powershell.utility/format-list)   | [<span data-ttu-id="7f68d-111">ConvertTo-Html</span><span class="sxs-lookup"><span data-stu-id="7f68d-111">ConvertTo-Html</span></span>](/powershell/module/microsoft.powershell.utility/convertto-html) |
| [<span data-ttu-id="7f68d-112">Format-Table</span><span class="sxs-lookup"><span data-stu-id="7f68d-112">Format-Table</span></span>](/powershell/module/microsoft.powershell.utility/format-table)  | [<span data-ttu-id="7f68d-113">ConvertTo-Json</span><span class="sxs-lookup"><span data-stu-id="7f68d-113">ConvertTo-Json</span></span>](/powershell/module/microsoft.powershell.utility/convertto-json) |
| [<span data-ttu-id="7f68d-114">Format-Wide</span><span class="sxs-lookup"><span data-stu-id="7f68d-114">Format-Wide</span></span>](/powershell/module/microsoft.powershell.utility/format-wide)   | [<span data-ttu-id="7f68d-115">ConvertTo-Xml</span><span class="sxs-lookup"><span data-stu-id="7f68d-115">ConvertTo-Xml</span></span>](/powershell/module/microsoft.powershell.utility/convertto-xml)  |

## <a name="format-examples"></a><span data-ttu-id="7f68d-116">格式示例</span><span class="sxs-lookup"><span data-stu-id="7f68d-116">Format examples</span></span>

<span data-ttu-id="7f68d-117">此示例获取默认订阅中的 Azure VM 列表。</span><span class="sxs-lookup"><span data-stu-id="7f68d-117">In this example, we get a list of Azure VMs in our default subscription.</span></span>  <span data-ttu-id="7f68d-118">`Get-AzureRmVM` 命令默认将输出设置为表格式。</span><span class="sxs-lookup"><span data-stu-id="7f68d-118">The `Get-AzureRmVM` command defaults output into a table format.</span></span>

```azurepowershell-interactive
Get-AzureRmVM
```

```output
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

<span data-ttu-id="7f68d-119">若要限制返回的列，可以使用 `Format-Table` cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7f68d-119">If you would like to limit the columns returned you can use the `Format-Table` cmdlet.</span></span> <span data-ttu-id="7f68d-120">以下示例获取相同的虚拟机列表，但会将输出限制为只返回 VM 名称、资源组和 VM 位置。</span><span class="sxs-lookup"><span data-stu-id="7f68d-120">In the following example, we get the same list of virtual machines but restrict the output to just the name of the VM, the resource group, and the location of the VM.</span></span>  <span data-ttu-id="7f68d-121">`-Autosize` 参数根据数据大小调整列的大小。</span><span class="sxs-lookup"><span data-stu-id="7f68d-121">The `-Autosize` parameter sizes the columns according to the size of the data.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Format-Table Name,ResourceGroupName,Location -AutoSize
```

```output
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

<span data-ttu-id="7f68d-122">还可以将输出格式设置为列表。</span><span class="sxs-lookup"><span data-stu-id="7f68d-122">Output can also be formatted into a list.</span></span> <span data-ttu-id="7f68d-123">以下示例演示如何使用 `Format-List` cmdlet 以列表格式显示信息。</span><span class="sxs-lookup"><span data-stu-id="7f68d-123">The following example shows this using the`Format-List` cmdlet.</span></span>

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

## <a name="convert-to-other-data-types"></a><span data-ttu-id="7f68d-124">转换为其他数据类型</span><span class="sxs-lookup"><span data-stu-id="7f68d-124">Convert to other data types</span></span>

<span data-ttu-id="7f68d-125">PowerShell 还允许获取命令输出并将其转换为多种数据格式。</span><span class="sxs-lookup"><span data-stu-id="7f68d-125">PowerShell also allows taking command output and converting it into multiple data formats.</span></span> <span data-ttu-id="7f68d-126">在以下示例中，`Select-Object` cmdlet 用来获取订阅中虚拟机的属性，然后将输出转换为 CSV 格式，以便将其导入数据库或电子表格中。</span><span class="sxs-lookup"><span data-stu-id="7f68d-126">In the following example, the `Select-Object` cmdlet is used to get attributes of the virtual machines in our subscription and convert the output to CSV format for easy import into a database or spreadsheet.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Select-Object ResourceGroupName,Id,VmId,Name,Location,ProvisioningState | ConvertTo-Csv -NoTypeInformation
```

```output
"ResourceGroupName","Id","VmId","Name","Location","ProvisioningState"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyUnbuntu1610","33422f9b-e339-4704-bad8-dbe094585496","MyUnbuntu1610","westeurope","Succeeded"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyWin2016VM","4650c755-fc2b-4fc7-a5bc-298d5c00808f","MyWin2016VM","westeurope","Succeeded"
```

<span data-ttu-id="7f68d-127">还可以将输出转换为 JSON 格式。</span><span class="sxs-lookup"><span data-stu-id="7f68d-127">Output can also be converted into the JSON format.</span></span>  <span data-ttu-id="7f68d-128">以下示例创建相同的 VM 列表，但会将输出格式更改为 JSON。</span><span class="sxs-lookup"><span data-stu-id="7f68d-128">The following example creates the same list of VMs but changes the output format to JSON.</span></span>

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
