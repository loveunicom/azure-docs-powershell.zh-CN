---
title: 查询 Azure 资源和设置结果的格式 | Microsoft Docs
description: 如何查询 Azure 中的资源以及设置结果的格式。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/30/2017
ms.openlocfilehash: 1584c8166078b7d7d24ce8748307fde0f565b662
ms.sourcegitcommit: c98e3a21037ebd82936828bcb544eed902b24212
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/08/2018
ms.locfileid: "34853468"
---
# <a name="querying-for-azure-resources"></a><span data-ttu-id="81f3c-103">查询 Azure 资源</span><span class="sxs-lookup"><span data-stu-id="81f3c-103">Querying for Azure resources</span></span>

<span data-ttu-id="81f3c-104">可以在 PowerShell 中使用内置的 cmdlet 完成查询。</span><span class="sxs-lookup"><span data-stu-id="81f3c-104">Querying in PowerShell can be completed by using built-in cmdlets.</span></span> <span data-ttu-id="81f3c-105">在 PowerShell 中，cmdlet 名称采用 **_动词-名词_** 格式。</span><span class="sxs-lookup"><span data-stu-id="81f3c-105">In PowerShell, cmdlet names take the form of **_Verb-Noun_**.</span></span> <span data-ttu-id="81f3c-106">使用动词 **_Get_** 的 cmdlet 是查询 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="81f3c-106">The cmdlets using the verb **_Get_** are the query cmdlets.</span></span> <span data-ttu-id="81f3c-107">cmdlet 名词是 cmdlet 动词处理的 Azure 资源的类型。</span><span class="sxs-lookup"><span data-stu-id="81f3c-107">The cmdlet nouns are the types of Azure resources that are acted upon by the cmdlet verbs.</span></span>


## <a name="selecting-simple-properties"></a><span data-ttu-id="81f3c-108">选择简单属性</span><span class="sxs-lookup"><span data-stu-id="81f3c-108">Selecting simple properties</span></span>

<span data-ttu-id="81f3c-109">Azure PowerShell 为每个 cmdlet 定义了默认格式。</span><span class="sxs-lookup"><span data-stu-id="81f3c-109">Azure PowerShell has default formatting defined for each cmdlet.</span></span> <span data-ttu-id="81f3c-110">每种资源类型的最常见属性自动以表或列表格式显示。</span><span class="sxs-lookup"><span data-stu-id="81f3c-110">The most common properties for each resource type are displayed in a table or list format automatically.</span></span> <span data-ttu-id="81f3c-111">有关设置输出格式的详细信息，请参阅[设置查询结果的格式](formatting-output.md)。</span><span class="sxs-lookup"><span data-stu-id="81f3c-111">For more information about formatting output, see [Formatting query results](formatting-output.md).</span></span>

<span data-ttu-id="81f3c-112">使用 `Get-AzureRmVM` cmdlet 可以查询帐户中的 VM 列表。</span><span class="sxs-lookup"><span data-stu-id="81f3c-112">Use the `Get-AzureRmVM` cmdlet to query for a list of VMs in your account.</span></span>

```powershell
Get-AzureRmVM
```

<span data-ttu-id="81f3c-113">默认输出自动设置为表格式。</span><span class="sxs-lookup"><span data-stu-id="81f3c-113">The default output is automatically formatted as a table.</span></span>

```
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

<span data-ttu-id="81f3c-114">可以使用 `Select-Object` cmdlet 选择所需的特定属性。</span><span class="sxs-lookup"><span data-stu-id="81f3c-114">The `Select-Object` cmdlet can be used to select the specific properties that are interesting to you.</span></span>

```powershell
Get-AzureRmVM | Select Name,ResourceGroupName,Location
```

```
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

## <a name="selecting-complex-nested-properties"></a><span data-ttu-id="81f3c-115">选择复杂的嵌套属性</span><span class="sxs-lookup"><span data-stu-id="81f3c-115">Selecting complex nested properties</span></span>

<span data-ttu-id="81f3c-116">如果要选择的属性嵌套在 JSON 输出中的深层位置，则需要提供该嵌套属性的完整路径。</span><span class="sxs-lookup"><span data-stu-id="81f3c-116">If the property you want to select is nested deep in the JSON output you need to supply the full path to that nested property.</span></span> <span data-ttu-id="81f3c-117">以下示例演示如何从 `Get-AzureRmVM` cmdlet 选择 VM 名称和 OS 类型。</span><span class="sxs-lookup"><span data-stu-id="81f3c-117">The following example shows how to select the VM Name and the OS type from the `Get-AzureRmVM` cmdlet.</span></span>

```powershell
Get-AzureRmVM | Select Name,@{Name='OSType'; Expression={$_.StorageProfile.OSDisk.OSType}}
```

```
Name           OSType
----           ------
MyUnbuntu1610   Linux
MyWin2016VM   Windows
```

## <a name="filter-result-using-the-where-object-cmdlet"></a><span data-ttu-id="81f3c-118">使用 Where-Object cmdlet 筛选结果</span><span class="sxs-lookup"><span data-stu-id="81f3c-118">Filter result using the Where-Object cmdlet</span></span>

<span data-ttu-id="81f3c-119">使用 `Where-Object` cmdlet 可以根据任何属性值筛选结果。</span><span class="sxs-lookup"><span data-stu-id="81f3c-119">The `Where-Object` cmdlet allows you to filter the result based on any property value.</span></span> <span data-ttu-id="81f3c-120">在以下示例中，筛选器仅选择名称中包含文本“RGD”的 VM。</span><span class="sxs-lookup"><span data-stu-id="81f3c-120">In the following example, the filter selects only VMs that have the text "RGD" in their name.</span></span>

```powershell
Get-AzureRmVM | Where ResourceGroupName -like RGD* | Select ResourceGroupName,Name
```

```
ResourceGroupName  Name
-----------------  ----
RGDEMO001          KBDemo001VM
RGDEMO001          KBDemo020
```

<span data-ttu-id="81f3c-121">在下一个示例中，结果将返回 vmSize 为“Standard_DS1_V2”的 VM。</span><span class="sxs-lookup"><span data-stu-id="81f3c-121">With the next example, the results will return the VMs that have the vmSize 'Standard_DS1_V2'.</span></span>

```powershell
Get-AzureRmVM | Where vmSize -eq Standard_DS1_V2
```

```
ResourceGroupName          Name     Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----     --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610   westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM   westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```
