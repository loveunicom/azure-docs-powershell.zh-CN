---
title: Azure PowerShell cmdlet 的查询输出
description: 如何查询 Azure 中的资源以及设置结果的格式。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: da8c8f37d8c60e9555b4627a7b5c3d1d6e7888fa
ms.sourcegitcommit: 3a02e0c85c83de873981dd392500bc82c1cf9286
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2018
ms.locfileid: "46560365"
---
# <a name="query-output-of-azure-powershell-cmdlets"></a><span data-ttu-id="1b2fe-103">Azure PowerShell cmdlet 的查询输出</span><span class="sxs-lookup"><span data-stu-id="1b2fe-103">Query output of Azure PowerShell cmdlets</span></span>

<span data-ttu-id="1b2fe-104">可以在 PowerShell 中使用内置的 cmdlet 完成查询。</span><span class="sxs-lookup"><span data-stu-id="1b2fe-104">Querying in PowerShell can be completed by using built-in cmdlets.</span></span> <span data-ttu-id="1b2fe-105">在 PowerShell 中，cmdlet 名称采用 **_动词-名词_** 格式。</span><span class="sxs-lookup"><span data-stu-id="1b2fe-105">In PowerShell, cmdlet names take the form of **_Verb-Noun_**.</span></span> <span data-ttu-id="1b2fe-106">使用动词 **_Get_** 的 cmdlet 是查询 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1b2fe-106">The cmdlets using the verb **_Get_** are the query cmdlets.</span></span> <span data-ttu-id="1b2fe-107">cmdlet 名词是 cmdlet 动词处理的 Azure 资源的类型。</span><span class="sxs-lookup"><span data-stu-id="1b2fe-107">The cmdlet nouns are the types of Azure resources that are acted upon by the cmdlet verbs.</span></span>

## <a name="select-simple-properties"></a><span data-ttu-id="1b2fe-108">选择简单属性</span><span class="sxs-lookup"><span data-stu-id="1b2fe-108">Select simple properties</span></span>

<span data-ttu-id="1b2fe-109">Azure PowerShell 为每个 cmdlet 定义了默认格式。</span><span class="sxs-lookup"><span data-stu-id="1b2fe-109">Azure PowerShell has default formatting defined for each cmdlet.</span></span> <span data-ttu-id="1b2fe-110">每种资源类型的最常见属性自动以表或列表格式显示。</span><span class="sxs-lookup"><span data-stu-id="1b2fe-110">The most common properties for each resource type are displayed in a table or list format automatically.</span></span> <span data-ttu-id="1b2fe-111">有关设置输出格式的详细信息，请参阅[设置查询结果的格式](formatting-output.md)。</span><span class="sxs-lookup"><span data-stu-id="1b2fe-111">For more information about formatting output, see [Formatting query results](formatting-output.md).</span></span>

<span data-ttu-id="1b2fe-112">使用 `Get-AzureRmVM` cmdlet 可以查询帐户中的 VM 列表。</span><span class="sxs-lookup"><span data-stu-id="1b2fe-112">Use the `Get-AzureRmVM` cmdlet to query for a list of VMs in your account.</span></span>

```azurepowershell-interactive
Get-AzureRmVM
```

<span data-ttu-id="1b2fe-113">默认输出自动设置为表格式。</span><span class="sxs-lookup"><span data-stu-id="1b2fe-113">The default output is automatically formatted as a table.</span></span>

```output
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

<span data-ttu-id="1b2fe-114">可以使用 `Select-Object` cmdlet 选择所需的特定属性。</span><span class="sxs-lookup"><span data-stu-id="1b2fe-114">The `Select-Object` cmdlet can be used to select the specific properties that are interesting to you.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Select Name,ResourceGroupName,Location
```

```output
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

## <a name="select-complex-nested-properties"></a><span data-ttu-id="1b2fe-115">选择复杂的嵌套属性</span><span class="sxs-lookup"><span data-stu-id="1b2fe-115">Select complex nested properties</span></span>

<span data-ttu-id="1b2fe-116">如果所需的属性嵌套在 JSON 输出中，则需要提供该属性的完整路径。</span><span class="sxs-lookup"><span data-stu-id="1b2fe-116">If the property you want is nested in the JSON output, you need to supply the full path to the property.</span></span> <span data-ttu-id="1b2fe-117">以下示例演示如何从 `Get-AzureRmVM` cmdlet 选择 VM 名称和 OS 类型。</span><span class="sxs-lookup"><span data-stu-id="1b2fe-117">The following example shows how to select the VM Name and the OS type from the `Get-AzureRmVM` cmdlet.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Select Name,@{Name='OSType'; Expression={$_.StorageProfile.OSDisk.OSType}}
```

```output
Name           OSType
----           ------
MyUnbuntu1610   Linux
MyWin2016VM   Windows
```

## <a name="filter-results-with-the-where-object-cmdlet"></a><span data-ttu-id="1b2fe-118">使用 Where-Object cmdlet 筛选结果</span><span class="sxs-lookup"><span data-stu-id="1b2fe-118">Filter results with the Where-Object cmdlet</span></span>

<span data-ttu-id="1b2fe-119">使用 `Where-Object` cmdlet 可以根据任何属性值筛选结果。</span><span class="sxs-lookup"><span data-stu-id="1b2fe-119">The `Where-Object` cmdlet allows you to filter the result based on any property value.</span></span> <span data-ttu-id="1b2fe-120">在以下示例中，筛选器仅选择名称中包含文本“RGD”的 VM。</span><span class="sxs-lookup"><span data-stu-id="1b2fe-120">In the following example, the filter selects only VMs that have the text "RGD" in their name.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Where ResourceGroupName -like RGD* | Select ResourceGroupName,Name
```

```output
ResourceGroupName  Name
-----------------  ----
RGDEMO001          KBDemo001VM
RGDEMO001          KBDemo020
```

<span data-ttu-id="1b2fe-121">在下一个示例中，结果将返回 vmSize 为“Standard_DS1_V2”的 VM。</span><span class="sxs-lookup"><span data-stu-id="1b2fe-121">With the next example, the results will return the VMs that have the vmSize 'Standard_DS1_V2'.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Where vmSize -eq Standard_DS1_V2
```

```output
ResourceGroupName          Name     Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----     --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610   westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM   westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```