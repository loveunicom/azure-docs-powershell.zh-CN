---
title: "Azure PowerShell 更改日志 | Microsoft Docs"
description: "下面提供了对 Azure PowerShell 最新版本所做更改的历史记录。"
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: 
ms.date: 05/18/2017
ms.openlocfilehash: 143d92384fd270711378f6741ba59e88c12833d1
ms.sourcegitcommit: 226527be7cb647acfe2ea9ab151185053ab3c6db
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/29/2017
---
# <span data-ttu-id="17318-103">发行说明</span><span class="sxs-lookup"><span data-stu-id="17318-103">Release notes</span></span>
<a id="release-notes" class="xliff"></a>

<span data-ttu-id="17318-104">下面是此版本中对 Azure PowerShell 所做的更改列表。</span><span class="sxs-lookup"><span data-stu-id="17318-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

## <span data-ttu-id="17318-105">版本 2.2.0</span><span class="sxs-lookup"><span data-stu-id="17318-105">Version 2.2.0</span></span>
<a id="version-220" class="xliff"></a>
* <span data-ttu-id="17318-106">计算</span><span class="sxs-lookup"><span data-stu-id="17318-106">Compute</span></span>
  - <span data-ttu-id="17318-107">添加了从 AzureDiskEncryptionForLinux 扩展查询加密状态的支持</span><span class="sxs-lookup"><span data-stu-id="17318-107">Add support for querying encryption status from the AzureDiskEncryptionForLinux extension</span></span>
* <span data-ttu-id="17318-108">DataFactory</span><span class="sxs-lookup"><span data-stu-id="17318-108">DataFactory</span></span>
  - <span data-ttu-id="17318-109">添加了新 cmdlet 用于列出活动时间范围</span><span class="sxs-lookup"><span data-stu-id="17318-109">Added new cmdlet for listing activity windows</span></span>
    + <span data-ttu-id="17318-110">Get-AzureRmDataFactoryActivityWindow</span><span class="sxs-lookup"><span data-stu-id="17318-110">Get-AzureRmDataFactoryActivityWindow</span></span>
* <span data-ttu-id="17318-111">DataLake</span><span class="sxs-lookup"><span data-stu-id="17318-111">DataLake</span></span>
  - <span data-ttu-id="17318-112">已将参数 `Host` 更改为 `DatabaseHost`，并为 `Host` 添加了别名</span><span class="sxs-lookup"><span data-stu-id="17318-112">Changed parameter `Host` to `DatabaseHost` and added alias to `Host`</span></span>
    + <span data-ttu-id="17318-113">New-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="17318-113">New-AzureRmDataLakeAnalyticsCatalogSecret</span></span>
    + <span data-ttu-id="17318-114">Set-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="17318-114">Set-AzureRmDataLakeAnalyticsCatalogSecret</span></span>
  - <span data-ttu-id="17318-115">添加了删除 ACL 和默认 ACL 的支持</span><span class="sxs-lookup"><span data-stu-id="17318-115">Add support for ACL and Default ACL removal</span></span>
  - <span data-ttu-id="17318-116">添加了对获取和设置文件与文件夹的未命名权限的支持</span><span class="sxs-lookup"><span data-stu-id="17318-116">Add support for getting and setting unnamed permissions on files and folders</span></span>
* <span data-ttu-id="17318-117">KeyVault</span><span class="sxs-lookup"><span data-stu-id="17318-117">KeyVault</span></span>
  - <span data-ttu-id="17318-118">添加了对证书的支持</span><span class="sxs-lookup"><span data-stu-id="17318-118">Add support for certificates</span></span>
    + <span data-ttu-id="17318-119">Add-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="17318-119">Add-AzureKeyVaultCertificate</span></span>
    + <span data-ttu-id="17318-120">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="17318-120">Add-AzureKeyVaultCertificateContact</span></span>
    + <span data-ttu-id="17318-121">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="17318-121">Get-AzureKeyVaultCertificate</span></span>
    + <span data-ttu-id="17318-122">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="17318-122">Get-AzureKeyVaultCertificateContact</span></span>
    + <span data-ttu-id="17318-123">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="17318-123">Get-AzureKeyVaultCertificateIssuer</span></span>
    + <span data-ttu-id="17318-124">Get-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="17318-124">Get-AzureKeyVaultCertificateOperation</span></span>
    + <span data-ttu-id="17318-125">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="17318-125">Get-AzureKeyVaultCertificatePolicy</span></span>
    + <span data-ttu-id="17318-126">Import-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="17318-126">Import-AzureKeyVaultCertificate</span></span>
    + <span data-ttu-id="17318-127">New-AzureKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="17318-127">New-AzureKeyVaultCertificateAdministratorDetails</span></span>
    + <span data-ttu-id="17318-128">New-AzureKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="17318-128">New-AzureKeyVaultCertificateOrganizationDetails</span></span>
    + <span data-ttu-id="17318-129">New-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="17318-129">New-AzureKeyVaultCertificatePolicy</span></span>
    + <span data-ttu-id="17318-130">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="17318-130">Remove-AzureKeyVaultCertificate</span></span>
    + <span data-ttu-id="17318-131">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="17318-131">Remove-AzureKeyVaultCertificateContact</span></span>
    + <span data-ttu-id="17318-132">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="17318-132">Remove-AzureKeyVaultCertificateIssuer</span></span>
    + <span data-ttu-id="17318-133">Remove-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="17318-133">Remove-AzureKeyVaultCertificateOperation</span></span>
    + <span data-ttu-id="17318-134">Set-AzureKeyVaultCertificateAttribute</span><span class="sxs-lookup"><span data-stu-id="17318-134">Set-AzureKeyVaultCertificateAttribute</span></span>
    + <span data-ttu-id="17318-135">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="17318-135">Set-AzureKeyVaultCertificateIssuer</span></span>
    + <span data-ttu-id="17318-136">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="17318-136">Set-AzureKeyVaultCertificatePolicy</span></span>
    + <span data-ttu-id="17318-137">Stop-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="17318-137">Stop-AzureKeyVaultCertificateOperation</span></span>
* <span data-ttu-id="17318-138">网络</span><span class="sxs-lookup"><span data-stu-id="17318-138">Network</span></span>

  - <span data-ttu-id="17318-139">为网络接口添加了新的开关参数，用于启用/禁用加速网络：+New-AzureRmNetworkInterface -EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="17318-139">New switch parameter added for network interface to enable/disable accelerated networking +New-AzureRmNetworkInterface -EnableAcceleratedNetworking</span></span>
  - <span data-ttu-id="17318-140">使用 PowerShell cmdlet 启用主动-主动网关功能</span><span class="sxs-lookup"><span data-stu-id="17318-140">Enable Active-Active gateway feature PowerShell cmdlets</span></span>
    + <span data-ttu-id="17318-141">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="17318-141">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
    + <span data-ttu-id="17318-142">Remove-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="17318-142">Remove-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="17318-143">添加了新的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="17318-143">Added new cmdlet</span></span>
    + <span data-ttu-id="17318-144">Test-AzureRmPrivateIpAddressAvailability</span><span class="sxs-lookup"><span data-stu-id="17318-144">Test-AzureRmPrivateIpAddressAvailability</span></span>
* <span data-ttu-id="17318-145">资源</span><span class="sxs-lookup"><span data-stu-id="17318-145">Resources</span></span>
  - <span data-ttu-id="17318-146">支持提供程序和资源 cmdlet 中的区域</span><span class="sxs-lookup"><span data-stu-id="17318-146">Support zones in provider and resource cmdlets</span></span>
    + <span data-ttu-id="17318-147">Get-AzureRmProvider</span><span class="sxs-lookup"><span data-stu-id="17318-147">Get-AzureRmProvider</span></span>
    + <span data-ttu-id="17318-148">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="17318-148">New-AzureRmResource</span></span>
    + <span data-ttu-id="17318-149">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="17318-149">Set-AzureRmResource</span></span>
* <span data-ttu-id="17318-150">Sql</span><span class="sxs-lookup"><span data-stu-id="17318-150">Sql</span></span>
  - <span data-ttu-id="17318-151">为服务器级别的 Azure SQL 威胁检测策略管理添加了新的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="17318-151">Added new cmdlets for Azure SQL threat detection policy management at server level</span></span>
    + <span data-ttu-id="17318-152">Get-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="17318-152">Get-AzureRmSqlServerThreatDetectionPolicy</span></span>
    + <span data-ttu-id="17318-153">Remove-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="17318-153">Remove-AzureRmSqlServerThreatDetectionPolicy</span></span>
    + <span data-ttu-id="17318-154">Set-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="17318-154">Set-AzureRmSqlServerThreatDetectionPolicy</span></span>
  - <span data-ttu-id="17318-155">添加了新的 cmdlet 用于支持启用/禁用 SQL Azure 数据仓库的 GeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="17318-155">Added new cmdlets to support enabling/disabling GeoBackupPolicy for Sql Azure DataWarehouses</span></span>
    + <span data-ttu-id="17318-156">Get-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="17318-156">Get-AzureRmSqlDatabaseGeoBackupPolicy</span></span>
    + <span data-ttu-id="17318-157">Set-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="17318-157">Set-AzureRmSqlDatabaseGeoBackupPolicy</span></span>
  - <span data-ttu-id="17318-158">为 Azure SQL 顾问和建议操作 API 添加了新的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="17318-158">Added new cmdlets for Azure Sql Advisors and Recommended Actions APIs</span></span>
    + <span data-ttu-id="17318-159">Get-AzureRmSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="17318-159">Get-AzureRmSqlDatabaseAdvisor</span></span>
    + <span data-ttu-id="17318-160">Get-AzureRmSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="17318-160">Get-AzureRmSqlElasticPoolAdvisor</span></span>
    + <span data-ttu-id="17318-161">Get-AzureRmSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="17318-161">Get-AzureRmSqlServerAdvisor</span></span>
    + <span data-ttu-id="17318-162">Get-AzureRmSqlDatabaseRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="17318-162">Get-AzureRmSqlDatabaseRecommendedActions</span></span>
    + <span data-ttu-id="17318-163">Get-AzureRmSqlElasticPoolRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="17318-163">Get-AzureRmSqlElasticPoolRecommendedActions</span></span>
    + <span data-ttu-id="17318-164">Get-AzureRmSqlServerRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="17318-164">Get-AzureRmSqlServerRecommendedActions</span></span>
    + <span data-ttu-id="17318-165">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="17318-165">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span></span>
    + <span data-ttu-id="17318-166">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="17318-166">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span></span>
    + <span data-ttu-id="17318-167">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="17318-167">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span></span>
    + <span data-ttu-id="17318-168">Set-AzureRmSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="17318-168">Set-AzureRmSqlDatabaseRecommendedActionState</span></span>
    + <span data-ttu-id="17318-169">Set-AzureRmSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="17318-169">Set-AzureRmSqlElasticPoolRecommendedActionState</span></span>
    + <span data-ttu-id="17318-170">Set-AzureRmSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="17318-170">Set-AzureRmSqlServerRecommendedActionState</span></span>
