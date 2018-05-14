# <a name="breaking-changes-for-microsoft-azure-powershell-300"></a>Microsoft Azure PowerShell 3.0.0 的重大更改

本文档是面向 Microsoft Azure PowerShell cmdlet 的使用者的重大更改通知和迁移指南。  每部分都介绍了重大更改的影响和最简便的迁移路径。  有关深入的上下文，请参考与每个更改关联的拉取请求。

## <a name="table-of-contents"></a>目录
1. [Data Lake Store cmdlet 的重大更改](#breaking-changes-to-data-lake-store-cmdlets)
2. [ApiManagement cmdlet 的重大更改](#breaking-changes-to-apimanagement-cmdlets)
3. [网络 cmdlet 的重大更改](#breaking-changes-to-network-cmdlets)

## <a name="breaking-changes-to-data-lake-store-cmdlets"></a>Data Lake Store cmdlet 的重大更改

版本 [PR 2965](https://github.com/Azure/azure-powershell/pull/2965) 影响以下 cmdlet：

**Get-AzureRmDataLakeStoreItemAcl (Get-AdlStoreItemAcl)**
- 此 cmdlet 已删除并替换为 ``Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)``。
- 旧 cmdlet 返回一个表示访问控制列表 (ACL) 的复杂对象。 新 cmdlet 返回所选路径的 ACL 中的条目的简单列表。

```powershell
# Old
Get-AdlStoreItemAcl -Account myadlsaccount -Path /foo

# New
Get-AdlStoreItemAclEntry -Account myadlsaccount -Path /foo
```

**Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)**
- 此 cmdlet 替换了旧 cmdlet ``Get-AzureRmDataLakeStoreItemAcl (Get-AdlStoreItemAcl)``。
- 此新 cmdlet 返回所选路径的 ACL 中的条目的简单列表，类型为 ``DataLakeStoreItemAce[]``。
- 可以将此 cmdlet 的输出传递给以下 cmdlet 的 ``-Acl`` 参数：
   - ``Remove-AzureRmDataLakeStoreItemAcl``
   - ``Set-AzureRmDataLakeStoreItemAcl``
   - ``Set-AzureRmDataLakeStoreItemAclEntry``

```powershell
# Old
Get-AdlStoreItemAcl -Account myadlsaccount -Path /foo

# New
Get-AdlStoreItemAclEntry -Account myadlsaccount -Path /foo
```

**Remove-AzureRmDataLakeStoreItemAcl (Remove-AdlStoreItemAcl)**、**Set-AzureRmDataLakeStoreItemAcl (Set-AdlStoreItemAcl)**、**Set-AzureRmDataLakeStoreItemAclEntry (Set-AdlStoreItemAclEntry)**
- 对于 ``-Acl`` 参数，这些 cmdlet 现在接受 ``DataLakeStoreItemAce[]``。
- ``DataLakeStoreItemAce[]`` 是由 ``Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)`` 返回的。

```powershell
# Old
$acl = Get-AdlStoreItemAcl -Account myadlsaccount -Path /foo
Set-AdlStoreItemAcl -Account myadlsaccount -Path /foo -Acl $acl

# New
$aclEntries = Get-AdlStoreItemAclEntry -Account myadlsaccount -Path /foo
Set-AdlStoreItemAcl -Account myadlsaccount -Path /foo -Acl $aclEntries
```

## <a name="breaking-changes-to-apimanagement-cmdlets"></a>ApiManagement cmdlet 的重大更改

版本 [PR 2971](https://github.com/Azure/azure-powershell/pull/2971) 影响以下 cmdlet：

**New-AzureRmApiManagementVirtualNetwork**
- 用来引用虚拟网络的必需参数已从需要 SubnetName 和 VnetId 更改为需要格式为 ``/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ClassicNetwork/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}`` 的 SubnetResourceId

```powershell
# Old
$virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetName <String> -VnetId <Guid>

# New
$virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>

```

**即将弃用 Cmdlet Set-AzureRmApiManagementVirtualNetworks**
- 此 Cmdlet 即将弃用，因为有多种方式可用来将虚拟网络设置为与 ApiManagement 部署相关联。

```powershell
# Old
$networksList = @()
$networksList += New-AzureRmApiManagementVirtualNetwork -Location $vnetLocation -VnetId $vnetId -SubnetName $subnetName
Set-AzureRmApiManagementVirtualNetworks -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetworks $networksList

# New
$masterRegionVirtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>
Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $masterRegionVirtualNetwork
```

## <a name="breaking-changes-to-network-cmdlets"></a>网络 cmdlet 的重大更改

版本 [PR 2982](https://github.com/Azure/azure-powershell/pull/2982) 影响以下 cmdlet：

**New-AzureRmVirtualNetworkGateway**
- 有关具体更改的说明：删除了 ``:- Bool parameter:-ActiveActive`` 并添加了 ``SwitchParameter:-EnableActiveActiveFeature``，后者用于在新创建的虚拟网络网关上启用主动-主动功能。

```powershell
# Old 
# Sample of how the cmdlet was previously called
New-AzureRmVirtualNetworkGateway -ResourceGroupName $rgname -name $rname -Location $location -IpConfigurations $vnetIpConfig1,$vnetIpConfig2 -GatewayType Vpn -VpnType RouteBased -EnableBgp $false -GatewaySku HighPerformance -ActiveActive $true

# New
# Sample of how the cmdlet should now be called
New-AzureRmVirtualNetworkGateway -ResourceGroupName $rgname -name $rname -Location $location -IpConfigurations $vnetIpConfig1,$vnetIpConfig2 -GatewayType Vpn -VpnType RouteBased -EnableBgp $false -GatewaySku HighPerformance -EnableActiveActiveFeature
```

Set-AzureRmVirtualNetworkGateway
- 有关具体更改的说明：删除了 ``:- Bool parameter:-ActiveActive`` 并添加了 2 个参数 - ``SwitchParameters:-EnableActiveActiveFeature`` / ``DisableActiveActiveFeature``，添加的 2 个参数用于在虚拟网络网关上启用和禁用主动-主动功能。

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