# <a name="breaking-changes-for-microsoft-azure-powershell-300"></a><span data-ttu-id="9bc4f-101">Microsoft Azure PowerShell 3.0.0 的重大更改</span><span class="sxs-lookup"><span data-stu-id="9bc4f-101">Breaking changes for Microsoft Azure PowerShell 3.0.0.</span></span>

<span data-ttu-id="9bc4f-102">本文档是面向 Microsoft Azure PowerShell cmdlet 的使用者的重大更改通知和迁移指南。</span><span class="sxs-lookup"><span data-stu-id="9bc4f-102">This document serves as both a breaking change notification and migration guide for consumers of the Microsoft Azure PowerShell cmdlets.</span></span>  <span data-ttu-id="9bc4f-103">每部分都介绍了重大更改的影响和最简便的迁移路径。</span><span class="sxs-lookup"><span data-stu-id="9bc4f-103">Each section describes both the impetus for the breaking change and the migration path of least resistance.</span></span>  <span data-ttu-id="9bc4f-104">有关深入的上下文，请参考与每个更改关联的拉取请求。</span><span class="sxs-lookup"><span data-stu-id="9bc4f-104">For in-depth context, please refer to the pull request associated with each change.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="9bc4f-105">目录</span><span class="sxs-lookup"><span data-stu-id="9bc4f-105">Table of Contents</span></span>
1. [<span data-ttu-id="9bc4f-106">Data Lake Store cmdlet 的重大更改</span><span class="sxs-lookup"><span data-stu-id="9bc4f-106">Breaking changes to Data Lake Store cmdlets</span></span>](#breaking-changes-to-data-lake-store-cmdlets)
2. [<span data-ttu-id="9bc4f-107">ApiManagement cmdlet 的重大更改</span><span class="sxs-lookup"><span data-stu-id="9bc4f-107">Breaking changes to ApiManagement cmdlets</span></span>](#breaking-changes-to-apimanagement-cmdlets)
3. [<span data-ttu-id="9bc4f-108">网络 cmdlet 的重大更改</span><span class="sxs-lookup"><span data-stu-id="9bc4f-108">Breaking changes to Network cmdlets</span></span>](#breaking-changes-to-network-cmdlets)

## <a name="breaking-changes-to-data-lake-store-cmdlets"></a><span data-ttu-id="9bc4f-109">Data Lake Store cmdlet 的重大更改</span><span class="sxs-lookup"><span data-stu-id="9bc4f-109">Breaking changes to Data Lake Store cmdlets</span></span>

<span data-ttu-id="9bc4f-110">版本 [PR 2965](https://github.com/Azure/azure-powershell/pull/2965) 影响以下 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="9bc4f-110">The following cmdlets were affected this release ([PR 2965](https://github.com/Azure/azure-powershell/pull/2965)):</span></span>

<span data-ttu-id="9bc4f-111">**Get-AzureRmDataLakeStoreItemAcl (Get-AdlStoreItemAcl)**</span><span class="sxs-lookup"><span data-stu-id="9bc4f-111">**Get-AzureRmDataLakeStoreItemAcl (Get-AdlStoreItemAcl)**</span></span>
- <span data-ttu-id="9bc4f-112">此 cmdlet 已删除并替换为 ``Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)``。</span><span class="sxs-lookup"><span data-stu-id="9bc4f-112">This cmdlet was removed and replaced with ``Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)``.</span></span>
- <span data-ttu-id="9bc4f-113">旧 cmdlet 返回一个表示访问控制列表 (ACL) 的复杂对象。</span><span class="sxs-lookup"><span data-stu-id="9bc4f-113">The old cmdlet returned a complex object representing the access control list (ACL).</span></span> <span data-ttu-id="9bc4f-114">新 cmdlet 返回所选路径的 ACL 中的条目的简单列表。</span><span class="sxs-lookup"><span data-stu-id="9bc4f-114">The new cmdlet returns a simple list of entries in the chosen path's ACL.</span></span>

```powershell
# Old
Get-AdlStoreItemAcl -Account myadlsaccount -Path /foo

# New
Get-AdlStoreItemAclEntry -Account myadlsaccount -Path /foo
```

<span data-ttu-id="9bc4f-115">**Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)**</span><span class="sxs-lookup"><span data-stu-id="9bc4f-115">**Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)**</span></span>
- <span data-ttu-id="9bc4f-116">此 cmdlet 替换了旧 cmdlet ``Get-AzureRmDataLakeStoreItemAcl (Get-AdlStoreItemAcl)``。</span><span class="sxs-lookup"><span data-stu-id="9bc4f-116">This cmdlet replaces the old cmdlet ``Get-AzureRmDataLakeStoreItemAcl (Get-AdlStoreItemAcl)``.</span></span>
- <span data-ttu-id="9bc4f-117">此新 cmdlet 返回所选路径的 ACL 中的条目的简单列表，类型为 ``DataLakeStoreItemAce[]``。</span><span class="sxs-lookup"><span data-stu-id="9bc4f-117">This new cmdlet returns a simple list of entries in the chosen path's ACL, with type ``DataLakeStoreItemAce[]``.</span></span>
- <span data-ttu-id="9bc4f-118">可以将此 cmdlet 的输出传递给以下 cmdlet 的 ``-Acl`` 参数：</span><span class="sxs-lookup"><span data-stu-id="9bc4f-118">The output of this cmdlet can be passed in to the ``-Acl`` parameter of the following cmdlets:</span></span>
   - ``Remove-AzureRmDataLakeStoreItemAcl``
   - ``Set-AzureRmDataLakeStoreItemAcl``
   - ``Set-AzureRmDataLakeStoreItemAclEntry``

```powershell
# Old
Get-AdlStoreItemAcl -Account myadlsaccount -Path /foo

# New
Get-AdlStoreItemAclEntry -Account myadlsaccount -Path /foo
```

<span data-ttu-id="9bc4f-119">**Remove-AzureRmDataLakeStoreItemAcl (Remove-AdlStoreItemAcl)**、**Set-AzureRmDataLakeStoreItemAcl (Set-AdlStoreItemAcl)**、**Set-AzureRmDataLakeStoreItemAclEntry (Set-AdlStoreItemAclEntry)**</span><span class="sxs-lookup"><span data-stu-id="9bc4f-119">**Remove-AzureRmDataLakeStoreItemAcl (Remove-AdlStoreItemAcl)**, **Set-AzureRmDataLakeStoreItemAcl (Set-AdlStoreItemAcl)**, **Set-AzureRmDataLakeStoreItemAclEntry (Set-AdlStoreItemAclEntry)**</span></span>
- <span data-ttu-id="9bc4f-120">对于 ``-Acl`` 参数，这些 cmdlet 现在接受 ``DataLakeStoreItemAce[]``。</span><span class="sxs-lookup"><span data-stu-id="9bc4f-120">These cmdlets now accept ``DataLakeStoreItemAce[]`` for the ``-Acl`` parameter.</span></span>
- <span data-ttu-id="9bc4f-121">``DataLakeStoreItemAce[]`` 是由 ``Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)`` 返回的。</span><span class="sxs-lookup"><span data-stu-id="9bc4f-121">``DataLakeStoreItemAce[]`` is returned by ``Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)``.</span></span>

```powershell
# Old
$acl = Get-AdlStoreItemAcl -Account myadlsaccount -Path /foo
Set-AdlStoreItemAcl -Account myadlsaccount -Path /foo -Acl $acl

# New
$aclEntries = Get-AdlStoreItemAclEntry -Account myadlsaccount -Path /foo
Set-AdlStoreItemAcl -Account myadlsaccount -Path /foo -Acl $aclEntries
```

## <a name="breaking-changes-to-apimanagement-cmdlets"></a><span data-ttu-id="9bc4f-122">ApiManagement cmdlet 的重大更改</span><span class="sxs-lookup"><span data-stu-id="9bc4f-122">Breaking changes to ApiManagement cmdlets</span></span>

<span data-ttu-id="9bc4f-123">版本 [PR 2971](https://github.com/Azure/azure-powershell/pull/2971) 影响以下 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="9bc4f-123">The following cmdlets were affected this release ([PR 2971](https://github.com/Azure/azure-powershell/pull/2971)):</span></span>

<span data-ttu-id="9bc4f-124">**New-AzureRmApiManagementVirtualNetwork**</span><span class="sxs-lookup"><span data-stu-id="9bc4f-124">**New-AzureRmApiManagementVirtualNetwork**</span></span>
- <span data-ttu-id="9bc4f-125">用来引用虚拟网络的必需参数已从需要 SubnetName 和 VnetId 更改为需要格式为 ``/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ClassicNetwork/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}`` 的 SubnetResourceId</span><span class="sxs-lookup"><span data-stu-id="9bc4f-125">The required parameters to reference a virtual network changed from requiring SubnetName and VnetId to SubnetResourceId in format ``/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ClassicNetwork/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}``</span></span>

```powershell
# Old
$virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetName <String> -VnetId <Guid>

# New
$virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>

```

<span data-ttu-id="9bc4f-126">**即将弃用 Cmdlet Set-AzureRmApiManagementVirtualNetworks**</span><span class="sxs-lookup"><span data-stu-id="9bc4f-126">**Deprecating Cmdlet Set-AzureRmApiManagementVirtualNetworks**</span></span>
- <span data-ttu-id="9bc4f-127">此 Cmdlet 即将弃用，因为有多种方式可用来将虚拟网络设置为与 ApiManagement 部署相关联。</span><span class="sxs-lookup"><span data-stu-id="9bc4f-127">The Cmdlet is getting deprecated as there was more than one way to Set Virtual Network associated to ApiManagement deployment.</span></span>

```powershell
# Old
$networksList = @()
$networksList += New-AzureRmApiManagementVirtualNetwork -Location $vnetLocation -VnetId $vnetId -SubnetName $subnetName
Set-AzureRmApiManagementVirtualNetworks -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetworks $networksList

# New
$masterRegionVirtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>
Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $masterRegionVirtualNetwork
```

## <a name="breaking-changes-to-network-cmdlets"></a><span data-ttu-id="9bc4f-128">网络 cmdlet 的重大更改</span><span class="sxs-lookup"><span data-stu-id="9bc4f-128">Breaking changes to Network cmdlets</span></span>

<span data-ttu-id="9bc4f-129">版本 [PR 2982](https://github.com/Azure/azure-powershell/pull/2982) 影响以下 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="9bc4f-129">The following cmdlets were affected this release ([PR 2982](https://github.com/Azure/azure-powershell/pull/2982)):</span></span>

<span data-ttu-id="9bc4f-130">**New-AzureRmVirtualNetworkGateway**</span><span class="sxs-lookup"><span data-stu-id="9bc4f-130">**New-AzureRmVirtualNetworkGateway**</span></span>
- <span data-ttu-id="9bc4f-131">有关具体更改的说明：删除了 ``:- Bool parameter:-ActiveActive`` 并添加了 ``SwitchParameter:-EnableActiveActiveFeature``，后者用于在新创建的虚拟网络网关上启用主动-主动功能。</span><span class="sxs-lookup"><span data-stu-id="9bc4f-131">Description of what has changed ``:- Bool parameter:-ActiveActive`` is removed and ``SwitchParameter:-EnableActiveActiveFeature`` is added for enabling Active-Active feature on newly creating virtual network gateway.</span></span>

```powershell
# Old 
# Sample of how the cmdlet was previously called
New-AzureRmVirtualNetworkGateway -ResourceGroupName $rgname -name $rname -Location $location -IpConfigurations $vnetIpConfig1,$vnetIpConfig2 -GatewayType Vpn -VpnType RouteBased -EnableBgp $false -GatewaySku HighPerformance -ActiveActive $true

# New
# Sample of how the cmdlet should now be called
New-AzureRmVirtualNetworkGateway -ResourceGroupName $rgname -name $rname -Location $location -IpConfigurations $vnetIpConfig1,$vnetIpConfig2 -GatewayType Vpn -VpnType RouteBased -EnableBgp $false -GatewaySku HighPerformance -EnableActiveActiveFeature
```

<span data-ttu-id="9bc4f-132">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9bc4f-132">Set-AzureRmVirtualNetworkGateway</span></span>
- <span data-ttu-id="9bc4f-133">有关具体更改的说明：删除了 ``:- Bool parameter:-ActiveActive`` 并添加了 2 个参数 - ``SwitchParameters:-EnableActiveActiveFeature`` / ``DisableActiveActiveFeature``，添加的 2 个参数用于在虚拟网络网关上启用和禁用主动-主动功能。</span><span class="sxs-lookup"><span data-stu-id="9bc4f-133">Description of what has changed ``:- Bool parameter:-ActiveActive`` is removed and 2 ``SwitchParameters:-EnableActiveActiveFeature`` / ``DisableActiveActiveFeature`` are added for enabling and disabling Active-Active feature on virtual network gateway.</span></span>

```powershell
# Old
# Sample of how the cmdlet was previously called
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $gw -ActiveActive $true
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $gw -ActiveActive $false  

# New
# Sample of how the cmdlet should now be called
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $gw -EnableActiveActiveFeature
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $gw -DisableActiveActiveFeature
```