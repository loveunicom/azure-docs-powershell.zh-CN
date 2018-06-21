# <a name="table-of-contents"></a><span data-ttu-id="23ac3-101">目录</span><span class="sxs-lookup"><span data-stu-id="23ac3-101">Table of Contents</span></span>
1. [<span data-ttu-id="23ac3-102">Force 参数的删除</span><span class="sxs-lookup"><span data-stu-id="23ac3-102">Removal of Force parameters</span></span>](#removal-of-force-parameters)
2. [<span data-ttu-id="23ac3-103">Tag 参数的更改</span><span class="sxs-lookup"><span data-stu-id="23ac3-103">Change of Tag parameters</span></span>](#change-of-tag-parameters)
3. [<span data-ttu-id="23ac3-104">存储 cmdlet 的重大更改</span><span class="sxs-lookup"><span data-stu-id="23ac3-104">Breaking changes to Storage cmdlets</span></span>](#breaking-changes-to-storage-cmdlets)
4. [<span data-ttu-id="23ac3-105">AD cmdlet 的重大更改</span><span class="sxs-lookup"><span data-stu-id="23ac3-105">Breaking changes to AD cmdlets</span></span>](#breaking-changes-to-ad-cmdlets)

## <a name="removal-of-force-parameters"></a><span data-ttu-id="23ac3-106">Force 参数的删除</span><span class="sxs-lookup"><span data-stu-id="23ac3-106">Removal of Force parameters</span></span>

<span data-ttu-id="23ac3-107">在此版本中，我们从 cmdlet 中删除了所有已过时的 `Force` 参数，并且在将来的版本中将删除与此参数相关的相应警告。</span><span class="sxs-lookup"><span data-stu-id="23ac3-107">This release, we removed all Obsolete `Force` parameters from cmdlets and the corresponding warnings that the parameter would be removed in a future release.</span></span>

<span data-ttu-id="23ac3-108">此更改影响以下 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="23ac3-108">The following cmdlets are affected by this change:</span></span>

<span data-ttu-id="23ac3-109">**ApiManagement**</span><span class="sxs-lookup"><span data-stu-id="23ac3-109">**ApiManagement**</span></span>
- <span data-ttu-id="23ac3-110">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="23ac3-110">Remove-AzureRmApiManagement</span></span>
- <span data-ttu-id="23ac3-111">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="23ac3-111">Remove-AzureRmApiManagementApi</span></span>
- <span data-ttu-id="23ac3-112">Remove-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="23ac3-112">Remove-AzureRmApiManagementGroup</span></span>
- <span data-ttu-id="23ac3-113">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="23ac3-113">Remove-AzureRmApiManagementLogger</span></span>
- <span data-ttu-id="23ac3-114">Remove-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="23ac3-114">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>
- <span data-ttu-id="23ac3-115">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="23ac3-115">Remove-AzureRmApiManagementOperation</span></span>
- <span data-ttu-id="23ac3-116">Remove-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="23ac3-116">Remove-AzureRmApiManagementPolicy</span></span>
- <span data-ttu-id="23ac3-117">Remove-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="23ac3-117">Remove-AzureRmApiManagementProduct</span></span>
- <span data-ttu-id="23ac3-118">Remove-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="23ac3-118">Remove-AzureRmApiManagementProperty</span></span>
- <span data-ttu-id="23ac3-119">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="23ac3-119">Remove-AzureRmApiManagementSubscription</span></span>
- <span data-ttu-id="23ac3-120">Remove-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="23ac3-120">Remove-AzureRmApiManagementUser</span></span>

<span data-ttu-id="23ac3-121">**自动化**</span><span class="sxs-lookup"><span data-stu-id="23ac3-121">**Automation**</span></span>
- <span data-ttu-id="23ac3-122">Remove-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="23ac3-122">Remove-AzureRmAutomationCertificate</span></span>
- <span data-ttu-id="23ac3-123">Remove-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="23ac3-123">Remove-AzureRmAutomationCredential</span></span>
- <span data-ttu-id="23ac3-124">Remove-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="23ac3-124">Remove-AzureRmAutomationVariable</span></span>
- <span data-ttu-id="23ac3-125">Remove-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="23ac3-125">Remove-AzureRmAutomationWebhook</span></span>

<span data-ttu-id="23ac3-126">**批处理**</span><span class="sxs-lookup"><span data-stu-id="23ac3-126">**Batch**</span></span>
- <span data-ttu-id="23ac3-127">Remove-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="23ac3-127">Remove-AzureBatchCertificate</span></span>
- <span data-ttu-id="23ac3-128">Remove-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="23ac3-128">Remove-AzureBatchComputeNode</span></span>
- <span data-ttu-id="23ac3-129">Remove-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="23ac3-129">Remove-AzureBatchComputeNodeUser</span></span>

<span data-ttu-id="23ac3-130">**DataFactories**</span><span class="sxs-lookup"><span data-stu-id="23ac3-130">**DataFactories**</span></span>
- <span data-ttu-id="23ac3-131">Resume-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="23ac3-131">Resume-AzureRmDataFactoryPipeline</span></span>
- <span data-ttu-id="23ac3-132">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="23ac3-132">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>
- <span data-ttu-id="23ac3-133">Suspend-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="23ac3-133">Suspend-AzureRmDataFactoryPipeline</span></span>

<span data-ttu-id="23ac3-134">**DataLakeStore**</span><span class="sxs-lookup"><span data-stu-id="23ac3-134">**DataLakeStore**</span></span>
- <span data-ttu-id="23ac3-135">Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="23ac3-135">Remove-AzureRmDataLakeStoreItemAclEntry</span></span>
- <span data-ttu-id="23ac3-136">Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="23ac3-136">Set-AzureRmDataLakeStoreItemAcl</span></span>
- <span data-ttu-id="23ac3-137">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="23ac3-137">Set-AzureRmDataLakeStoreItemAclEntry</span></span>
- <span data-ttu-id="23ac3-138">Set-AzureRmDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="23ac3-138">Set-AzureRmDataLakeStoreItemOwner</span></span>

<span data-ttu-id="23ac3-139">**OperationalInsights**</span><span class="sxs-lookup"><span data-stu-id="23ac3-139">**OperationalInsights**</span></span>
- <span data-ttu-id="23ac3-140">Remove-AzureRmOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="23ac3-140">Remove-AzureRmOperationalInsightsSavedSearch</span></span>

<span data-ttu-id="23ac3-141">**配置文件**</span><span class="sxs-lookup"><span data-stu-id="23ac3-141">**Profile**</span></span>
- <span data-ttu-id="23ac3-142">Remove-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="23ac3-142">Remove-AzureRmEnvironment</span></span>

<span data-ttu-id="23ac3-143">**RedisCache**</span><span class="sxs-lookup"><span data-stu-id="23ac3-143">**RedisCache**</span></span>
- <span data-ttu-id="23ac3-144">Remove-AzureRmRedisCacheDiagnostics</span><span class="sxs-lookup"><span data-stu-id="23ac3-144">Remove-AzureRmRedisCacheDiagnostics</span></span>

<span data-ttu-id="23ac3-145">**资源**</span><span class="sxs-lookup"><span data-stu-id="23ac3-145">**Resources**</span></span>
- <span data-ttu-id="23ac3-146">Register-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="23ac3-146">Register-AzureRmProviderFeature</span></span>
- <span data-ttu-id="23ac3-147">Register-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="23ac3-147">Register-AzureRmResourceProvider</span></span>
- <span data-ttu-id="23ac3-148">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="23ac3-148">Remove-AzureRmADServicePrincipal</span></span>
- <span data-ttu-id="23ac3-149">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="23ac3-149">Remove-AzureRmPolicyAssignment</span></span>
- <span data-ttu-id="23ac3-150">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="23ac3-150">Remove-AzureRmResourceGroupDeployment</span></span>
- <span data-ttu-id="23ac3-151">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="23ac3-151">Remove-AzureRmRoleAssignment</span></span>
- <span data-ttu-id="23ac3-152">Stop-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="23ac3-152">Stop-AzureRmResourceGroupDeployment</span></span>
- <span data-ttu-id="23ac3-153">Unregister-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="23ac3-153">Unregister-AzureRmResourceProvider</span></span>

<span data-ttu-id="23ac3-154">**存储**</span><span class="sxs-lookup"><span data-stu-id="23ac3-154">**Storage**</span></span>
- <span data-ttu-id="23ac3-155">Remove-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="23ac3-155">Remove-AzureStorageContainerStoredAccessPolicy</span></span>
- <span data-ttu-id="23ac3-156">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="23ac3-156">Remove-AzureStorageQueueStoredAccessPolicy</span></span>
- <span data-ttu-id="23ac3-157">Remove-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="23ac3-157">Remove-AzureStorageShareStoredAccessPolicy</span></span>
- <span data-ttu-id="23ac3-158">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="23ac3-158">Remove-AzureStorageTableStoredAccessPolicy</span></span>

<span data-ttu-id="23ac3-159">**StreamAnalytics**</span><span class="sxs-lookup"><span data-stu-id="23ac3-159">**StreamAnalytics**</span></span>
- <span data-ttu-id="23ac3-160">Remove-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="23ac3-160">Remove-AzureRmStreamAnalyticsFunction</span></span>
- <span data-ttu-id="23ac3-161">Remove-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="23ac3-161">Remove-AzureRmStreamAnalyticsInput</span></span>
- <span data-ttu-id="23ac3-162">Remove-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="23ac3-162">Remove-AzureRmStreamAnalyticsJob</span></span>
- <span data-ttu-id="23ac3-163">Remove-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="23ac3-163">Remove-AzureRmStreamAnalyticsOutput</span></span>

<span data-ttu-id="23ac3-164">**标记**</span><span class="sxs-lookup"><span data-stu-id="23ac3-164">**Tag**</span></span>
- <span data-ttu-id="23ac3-165">Remove-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="23ac3-165">Remove-AzureRmTag</span></span>

<br>

<span data-ttu-id="23ac3-166">如果具有使用以上任一 cmdlet 的脚本，则只需删除 `Force` 参数便可适应此重大更改。</span><span class="sxs-lookup"><span data-stu-id="23ac3-166">If you have a script that uses any of the above cmdlets, the breaking change can be fixed by simply removing the `Force` parameter.</span></span>

```powershell
# Old
New-AzureRmResourceGroup -Name $resourceGroupName -Location $location -Force

# New
New-AzureRmResourceGroup -Name $resourceGroupName -Location $location
```

<br>

## <a name="change-of-tag-parameters"></a><span data-ttu-id="23ac3-167">Tag 参数的更改</span><span class="sxs-lookup"><span data-stu-id="23ac3-167">Change of Tag parameters</span></span>

<span data-ttu-id="23ac3-168">在此版本中，`Tags` 参数名称已更改为 `Tag`，并且类型已从 `Hashtable[]` 更改为 `Hashtable`，更改了键-值对的格式。</span><span class="sxs-lookup"><span data-stu-id="23ac3-168">This release, the `Tags` parameter name was changed to `Tag`, and the type was changed from `Hashtable[]` to `Hashtable`, changing the format of the key-value pairings.</span></span>

<span data-ttu-id="23ac3-169">以前，`Hashtable[]` 中的每个条目表示单个键-值对：</span><span class="sxs-lookup"><span data-stu-id="23ac3-169">Previously, each entry in the `Hashtable[]` represented a single key-value pairing:</span></span>

```powershell
$tags = @{ Name = "test1"; Value = "testval1" }, @{ Name = "test2", Value = "testval2" }
$tags[0].Name  # Key for the first entry, "test1"
$tags[0].Value # Value for the first entry, "testval1"
$tags[1].Name  # Key for the second entry, "test2"
$tags[1].Value # Value for the second entry, "testval2"
```

<span data-ttu-id="23ac3-170">现在，`Name` 和 `Value` 不再是必需的，允许通过在 `Hashtable` 中分配 `Key = "Value"` 来创建键-值对：</span><span class="sxs-lookup"><span data-stu-id="23ac3-170">Now, `Name` and `Value` are no longer necessary, allowing for key-value pairings to be created by assigning `Key = "Value"` in the `Hashtable`:</span></span>

```powershell
$tag = @{ test1 = "testval1"; test2 = "testval2" }
$tag["test1"] # Gets the value associated with the key "test1"
$tag["test2"] # Gets the value associated with the key "test2"
```

<span data-ttu-id="23ac3-171">此更改影响以下 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="23ac3-171">The following cmdlets are affected by this change:</span></span>

<span data-ttu-id="23ac3-172">**批处理**</span><span class="sxs-lookup"><span data-stu-id="23ac3-172">**Batch**</span></span>
- <span data-ttu-id="23ac3-173">Get-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="23ac3-173">Get-AzureRmBatchAccount</span></span>
- <span data-ttu-id="23ac3-174">New-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="23ac3-174">New-AzureRmBatchAccount</span></span>
- <span data-ttu-id="23ac3-175">Set-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="23ac3-175">Set-AzureRmBatchAccount</span></span>

<span data-ttu-id="23ac3-176">**计算**</span><span class="sxs-lookup"><span data-stu-id="23ac3-176">**Compute**</span></span>
- <span data-ttu-id="23ac3-177">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="23ac3-177">New-AzureRmVM</span></span>
- <span data-ttu-id="23ac3-178">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="23ac3-178">Update-AzureRmVM</span></span>

<span data-ttu-id="23ac3-179">**DataLakeAnalytics**</span><span class="sxs-lookup"><span data-stu-id="23ac3-179">**DataLakeAnalytics**</span></span>
- <span data-ttu-id="23ac3-180">New-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="23ac3-180">New-AzureRmDataLakeAnalyticsAccount</span></span>
- <span data-ttu-id="23ac3-181">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="23ac3-181">Set-AzureRmDataLakeAnalyticsAccount</span></span>

<span data-ttu-id="23ac3-182">**DataLakeStore**</span><span class="sxs-lookup"><span data-stu-id="23ac3-182">**DataLakeStore**</span></span>
- <span data-ttu-id="23ac3-183">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="23ac3-183">New-AzureRmDataLakeStoreAccount</span></span>
- <span data-ttu-id="23ac3-184">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="23ac3-184">Set-AzureRmDataLakeStoreAccount</span></span>

<span data-ttu-id="23ac3-185">**Dns**</span><span class="sxs-lookup"><span data-stu-id="23ac3-185">**Dns**</span></span>
- <span data-ttu-id="23ac3-186">New-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="23ac3-186">New-AzureRmDnsZone</span></span>
- <span data-ttu-id="23ac3-187">Set-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="23ac3-187">Set-AzureRmDnsZone</span></span>

<span data-ttu-id="23ac3-188">**KeyVault**</span><span class="sxs-lookup"><span data-stu-id="23ac3-188">**KeyVault**</span></span>
- <span data-ttu-id="23ac3-189">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="23ac3-189">Get-AzureRmKeyVault</span></span>
- <span data-ttu-id="23ac3-190">New-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="23ac3-190">New-AzureRmKeyVault</span></span>

<span data-ttu-id="23ac3-191">**网络**</span><span class="sxs-lookup"><span data-stu-id="23ac3-191">**Network**</span></span>
- <span data-ttu-id="23ac3-192">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="23ac3-192">New-AzureRmApplicationGateway</span></span>
- <span data-ttu-id="23ac3-193">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="23ac3-193">New-AzureRmExpressRouteCircuit</span></span>
- <span data-ttu-id="23ac3-194">New-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="23ac3-194">New-AzureRmLoadBalancer</span></span>
- <span data-ttu-id="23ac3-195">New-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="23ac3-195">New-AzureRmLocalNetworkGateway</span></span>
- <span data-ttu-id="23ac3-196">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="23ac3-196">New-AzureRmNetworkInterface</span></span>
- <span data-ttu-id="23ac3-197">New-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="23ac3-197">New-AzureRmNetworkSecurityGroup</span></span>
- <span data-ttu-id="23ac3-198">New-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="23ac3-198">New-AzureRmPublicIpAddress</span></span>
- <span data-ttu-id="23ac3-199">New-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="23ac3-199">New-AzureRmRouteTable</span></span>
- <span data-ttu-id="23ac3-200">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="23ac3-200">New-AzureRmVirtualNetwork</span></span>
- <span data-ttu-id="23ac3-201">New-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="23ac3-201">New-AzureRmVirtualNetworkGateway</span></span>
- <span data-ttu-id="23ac3-202">New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="23ac3-202">New-AzureRmVirtualNetworkGatewayConnection</span></span>
- <span data-ttu-id="23ac3-203">New-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="23ac3-203">New-AzureRmVirtualNetworkPeering</span></span>

<span data-ttu-id="23ac3-204">**资源**</span><span class="sxs-lookup"><span data-stu-id="23ac3-204">**Resources**</span></span>
- <span data-ttu-id="23ac3-205">Find-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="23ac3-205">Find-AzureRmResource</span></span>
- <span data-ttu-id="23ac3-206">Find-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="23ac3-206">Find-AzureRmResourceGroup</span></span>
- <span data-ttu-id="23ac3-207">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="23ac3-207">New-AzureRmResource</span></span>
- <span data-ttu-id="23ac3-208">New-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="23ac3-208">New-AzureRmResourceGroup</span></span>
- <span data-ttu-id="23ac3-209">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="23ac3-209">Set-AzureRmResource</span></span>
- <span data-ttu-id="23ac3-210">Set-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="23ac3-210">Set-AzureRmResourceGroup</span></span>

<span data-ttu-id="23ac3-211">**SQL**</span><span class="sxs-lookup"><span data-stu-id="23ac3-211">**SQL**</span></span>
- <span data-ttu-id="23ac3-212">New-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="23ac3-212">New-AzureRmSqlDatabase</span></span>
- <span data-ttu-id="23ac3-213">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="23ac3-213">New-AzureRmSqlDatabaseCopy</span></span>
- <span data-ttu-id="23ac3-214">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="23ac3-214">New-AzureRmSqlDatabaseSecondary</span></span>
- <span data-ttu-id="23ac3-215">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="23ac3-215">New-AzureRmSqlElasticPool</span></span>
- <span data-ttu-id="23ac3-216">New-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="23ac3-216">New-AzureRmSqlServer</span></span>
- <span data-ttu-id="23ac3-217">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="23ac3-217">Set-AzureRmSqlDatabase</span></span>
- <span data-ttu-id="23ac3-218">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="23ac3-218">Set-AzureRmSqlElasticPool</span></span>
- <span data-ttu-id="23ac3-219">Set-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="23ac3-219">Set-AzureRmSqlServer</span></span>

<span data-ttu-id="23ac3-220">**存储**</span><span class="sxs-lookup"><span data-stu-id="23ac3-220">**Storage**</span></span>
- <span data-ttu-id="23ac3-221">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="23ac3-221">New-AzureRmStorageAccount</span></span>
- <span data-ttu-id="23ac3-222">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="23ac3-222">Set-AzureRmStorageAccount</span></span>

<span data-ttu-id="23ac3-223">**TrafficManager**</span><span class="sxs-lookup"><span data-stu-id="23ac3-223">**TrafficManager**</span></span>
- <span data-ttu-id="23ac3-224">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="23ac3-224">New-AzureRmTrafficManagerProfile</span></span>

<br>

<span data-ttu-id="23ac3-225">如果具有使用以上任一 cmdlet 的脚本，则可以通过将 `Tags` 参数更改为 `Tag` 以及将 `Tag` 更改为新格式来适应此重大更改。</span><span class="sxs-lookup"><span data-stu-id="23ac3-225">If you have a script that uses any of the above cmdlets, the breaking change can be fixed by changing the `Tags` parameter to `Tag`, as well as changing the `Tag` to the new format.</span></span>

```powershell
# Old
New-AzureRmResourceGroup -Name $resourceGroupName -Location -location -Tags @{ Name = "testtag"; Value = "testval" }

# New
New-AzureRmResourceGroup -Name $resourceGroupName -Location -location -Tag @{ testtag = "testval" }
```

<br>

## <a name="breaking-changes-to-storage-cmdlets"></a><span data-ttu-id="23ac3-226">存储 cmdlet 的重大更改</span><span class="sxs-lookup"><span data-stu-id="23ac3-226">Breaking changes to Storage cmdlets</span></span>

<span data-ttu-id="23ac3-227">此版本影响以下 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="23ac3-227">The following cmdlets were affected this release:</span></span>

<span data-ttu-id="23ac3-228">**Get-AzureRmStorageAccountKey**</span><span class="sxs-lookup"><span data-stu-id="23ac3-228">**Get-AzureRmStorageAccountKey**</span></span>
- <span data-ttu-id="23ac3-229">此 cmdlet 现在返回一个键列表，而非包含每个键的属性的对象</span><span class="sxs-lookup"><span data-stu-id="23ac3-229">The cmdlet now returns a list of keys, rather than an object with properties for each key</span></span>

```powershell
# Old
$key = (Get-AzureRmStorageAccountKey -ResourceGroupName $resourceGroupName -Name $accountName).Key1

# New
$key = (Get-AzureRmStorageAccountKey -ResourceGroupName $resourceGroupName -Name $accountName)[0].Value
```

<span data-ttu-id="23ac3-230">**New-AzureRmStorageAccountKey**</span><span class="sxs-lookup"><span data-stu-id="23ac3-230">**New-AzureRmStorageAccountKey**</span></span>
- <span data-ttu-id="23ac3-231">此 cmdlet 的输出中的 `StorageAccountRegenerateKeyResponse` 字段已重命名为 `StorageAccountListKeysResults`，它现在是一个键列表而非包含每个键的属性的对象</span><span class="sxs-lookup"><span data-stu-id="23ac3-231">`StorageAccountRegenerateKeyResponse` field in output of this cmdlet is renamed to `StorageAccountListKeysResults`, which is now a list of keys rather than an object with properties for each key</span></span>

```powershell
# Old
$key = (New-AzureRmStorageAccountKey -ResourceGroupName $resourceGroupName -Name $accountName).StorageAccountKeys.Key1

# New
$key = (New-AzureRmStorageAccountKey -ResourceGroupName $resourceGroupName -Name $accountName).Keys[0].Value
```

<span data-ttu-id="23ac3-232">**New/Get/Set-AzureRmStorageAccount**</span><span class="sxs-lookup"><span data-stu-id="23ac3-232">**New/Get/Set-AzureRmStorageAccount**</span></span>
- <span data-ttu-id="23ac3-233">此 cmdlet 的输出中的 `AccountType` 字段已重名为 `Sku.Name`</span><span class="sxs-lookup"><span data-stu-id="23ac3-233">`AccountType` field in output of this cmdlet is renamed to `Sku.Name`</span></span>
- <span data-ttu-id="23ac3-234">PrimaryEndpoints/Secondary 终结点 blob/table/queue/file 的输出类型已从 `Uri` 更改为 `String`</span><span class="sxs-lookup"><span data-stu-id="23ac3-234">Output type for PrimaryEndpoints/Secondary endpoints blob/table/queue/file changed from `Uri` to `String`</span></span>

```powershell
# Old
$accountType = (Get-AzureRmStorageAccount -ResourceGroupName $resourceGroupName -Name $accountName).AccountType

# New
$accountType = (Get-AzureRmStorageAccount -ResourceGroupName $resourceGroupName -Name $accountName).Sku.Name
```

```powershell
# Old 
$blobEndpoint = (Get-AzureRmStorageAccount -ResourceGroupName $resourceGroupName -Name $accountName).PrimaryEndpoints.Blob.ToString()
$blobEndpoint = (Get-AzureRmStorageAccount -ResourceGroupName $resourceGroupName -Name $accountName).PrimaryEndpoints.Blob.AbsolutePath

# New
$blobEndpoint = (Get-AzureRmStorageAccount -ResourceGroupName $resourceGroupName -Name $accountName).PrimaryEndpoints.Blob.ToString()
$blobEndpoint = (Get-AzureRmStorageAccount -ResourceGroupName $resourceGroupName -Name $accountName).PrimaryEndpoints.Blob
```

<br>

## <a name="breaking-changes-to-ad-cmdlets"></a><span data-ttu-id="23ac3-235">AD cmdlet 的重大更改</span><span class="sxs-lookup"><span data-stu-id="23ac3-235">Breaking changes to AD cmdlets</span></span>

<span data-ttu-id="23ac3-236">此版本影响以下 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="23ac3-236">The following cmdlets were affected this release:</span></span>

<span data-ttu-id="23ac3-237">**Get-AzureRMADServicePrincipal**</span><span class="sxs-lookup"><span data-stu-id="23ac3-237">**Get-AzureRMADServicePrincipal**</span></span>
- <span data-ttu-id="23ac3-238">此 cmdlet 的输出中的 `ServicePrincipalName` 字段已重名为 `ServicePrincipalNames`，并且现在是一个集合。</span><span class="sxs-lookup"><span data-stu-id="23ac3-238">`ServicePrincipalName` field in output of this cmdlet is renamed to `ServicePrincipalNames` and is now a collection.</span></span> <span data-ttu-id="23ac3-239">它现在还将 `ApplicationId` 显示为 SPN 和 identifierUri 之一。</span><span class="sxs-lookup"><span data-stu-id="23ac3-239">It now displays `ApplicationId` also as one of the SPN, along with the identifierUri.</span></span>

```powershell
# Old
$servicePrincipals = Get-AzureRmADServicePrincipal -SearchString $displayName
$spn = $servicePrincipals[0].ServicePrincipalName

# New
$servicePrincipals = Get-AzureRmADServicePrincipal -SearchString $displayName
$spn = $servicePrincipals[0].ServicePrincipalNames[0]
```

<span data-ttu-id="23ac3-240">**Get-AzureRmADApplication**</span><span class="sxs-lookup"><span data-stu-id="23ac3-240">**Get-AzureRmADApplication**</span></span>
- <span data-ttu-id="23ac3-241">参数 `ApplicationObjectId` 已重命名为 `ObjectId`。</span><span class="sxs-lookup"><span data-stu-id="23ac3-241">Parameter `ApplicationObjectId` is renamed to `ObjectId`.</span></span>
- <span data-ttu-id="23ac3-242">在此 cmdlet 的输出中，`ApplicationObjectId` 已重名为 `ObjectId`。</span><span class="sxs-lookup"><span data-stu-id="23ac3-242">In output of this cmdlet, `ApplicationObjectId` is renamed to `ObjectId`.</span></span>

```powershell
# Old
$app = Get-AzureRmADApplication -ApplicationObjectId $applicationObjectId
$objectId = $app.ApplicationObjectId

# New
$app = Get-AzureRmADApplication -ObjectId $objectId
$objectId = $app.ObjectId
```

<span data-ttu-id="23ac3-243">**Remove-AzureRmADApplication**</span><span class="sxs-lookup"><span data-stu-id="23ac3-243">**Remove-AzureRmADApplication**</span></span>
- <span data-ttu-id="23ac3-244">参数 `ApplicationObjectId` 已重命名为 `ObjectId`。</span><span class="sxs-lookup"><span data-stu-id="23ac3-244">Parameter `ApplicationObjectId` is renamed to `ObjectId`.</span></span>

```powershell
# Old
$app = Remove-AzureRmADApplication -ApplicationObjectId $applicationObjectId -Force

# New
$app = Remove-AzureRmADApplication -ObjectId $objectId -Force
```

<span data-ttu-id="23ac3-245">**New-AzureRmADApplication**</span><span class="sxs-lookup"><span data-stu-id="23ac3-245">**New-AzureRmADApplication**</span></span>
- <span data-ttu-id="23ac3-246">在此 cmdlet 的输出中，`ApplicationObjectId` 已重名为 `ObjectId`。</span><span class="sxs-lookup"><span data-stu-id="23ac3-246">In output of this cmdlet, `ApplicationObjectId` is renamed to `ObjectId`.</span></span>
- <span data-ttu-id="23ac3-247">`KeyValue`、`KeyUsage`、`KeyType` 参数已删除。</span><span class="sxs-lookup"><span data-stu-id="23ac3-247">`KeyValue`, `KeyUsage`, `KeyType` parameters are removed.</span></span>

```powershell
# Old
$app = New-AzureRmADApplication -DisplayName $displayName -HomePage $homePage -IdentifierUris $identifierUris -KeyValue $kv -KeyType $kt -KeyUsage $ku
$id = $app.ApplicationObjectId

# New
$app = New-AzureRmADApplication -DisplayName $displayName -HomePage $homePage -IdentifierUris $identifierUris
$id = $app.ObjectId
New-AzureRmADAppCredential -ObjectId $id -Password $kv
```

<span data-ttu-id="23ac3-248">**Get-AzureRmADGroup**</span><span class="sxs-lookup"><span data-stu-id="23ac3-248">**Get-AzureRmADGroup**</span></span>
- <span data-ttu-id="23ac3-249">`Mail` 字段已从输出中删除。</span><span class="sxs-lookup"><span data-stu-id="23ac3-249">`Mail` field is removed from the output.</span></span>

<span data-ttu-id="23ac3-250">**Get-AzureRmADUser**</span><span class="sxs-lookup"><span data-stu-id="23ac3-250">**Get-AzureRmADUser**</span></span>
- <span data-ttu-id="23ac3-251">`Mail` 字段已从输出中删除。</span><span class="sxs-lookup"><span data-stu-id="23ac3-251">`Mail` field is removed from the output.</span></span>

<span data-ttu-id="23ac3-252">**New-AzureRmADServicePrincipal**</span><span class="sxs-lookup"><span data-stu-id="23ac3-252">**New-AzureRmADServicePrincipal**</span></span>
- <span data-ttu-id="23ac3-253">删除了 `DisableAccount` 参数。</span><span class="sxs-lookup"><span data-stu-id="23ac3-253">Removed `DisableAccount` parameter.</span></span>

```powershell
# Old
$servicePrincipal = New-AzureRmADServicePrincipal -DisplayName $displayName -Password $password -DisableAccount true

# New
$servicePrincipal = New-AzureRmADServicePrincipal -DisplayName $displayName -Password $password
Remove-AzureRmADServicePrincipal -ObjectId $servicePrincipal.ObjectId
```