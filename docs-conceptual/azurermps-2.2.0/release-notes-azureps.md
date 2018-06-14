---
title: Azure PowerShell 更改日志 | Microsoft Docs
description: 下面提供了对 Azure PowerShell 最新版本所做更改的历史记录。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: ca25f3c66f8e8f4c64fc04275da2bd28e32d2f6c
ms.sourcegitcommit: c98e3a21037ebd82936828bcb544eed902b24212
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/08/2018
ms.locfileid: "34854607"
---
# <a name="release-notes"></a><span data-ttu-id="b8c6e-103">发行说明</span><span class="sxs-lookup"><span data-stu-id="b8c6e-103">Release notes</span></span>

<span data-ttu-id="b8c6e-104">下面是此版本中对 Azure PowerShell 所做的更改列表。</span><span class="sxs-lookup"><span data-stu-id="b8c6e-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

## <a name="version-220"></a><span data-ttu-id="b8c6e-105">版本 2.2.0</span><span class="sxs-lookup"><span data-stu-id="b8c6e-105">Version 2.2.0</span></span>
* <span data-ttu-id="b8c6e-106">计算</span><span class="sxs-lookup"><span data-stu-id="b8c6e-106">Compute</span></span>
  - <span data-ttu-id="b8c6e-107">添加了从 AzureDiskEncryptionForLinux 扩展查询加密状态的支持</span><span class="sxs-lookup"><span data-stu-id="b8c6e-107">Add support for querying encryption status from the AzureDiskEncryptionForLinux extension</span></span>
* <span data-ttu-id="b8c6e-108">DataFactory</span><span class="sxs-lookup"><span data-stu-id="b8c6e-108">DataFactory</span></span>
  - <span data-ttu-id="b8c6e-109">添加了新 cmdlet 用于列出活动时间范围</span><span class="sxs-lookup"><span data-stu-id="b8c6e-109">Added new cmdlet for listing activity windows</span></span>
    + <span data-ttu-id="b8c6e-110">Get-AzureRmDataFactoryActivityWindow</span><span class="sxs-lookup"><span data-stu-id="b8c6e-110">Get-AzureRmDataFactoryActivityWindow</span></span>
* <span data-ttu-id="b8c6e-111">DataLake</span><span class="sxs-lookup"><span data-stu-id="b8c6e-111">DataLake</span></span>
  - <span data-ttu-id="b8c6e-112">已将参数 `Host` 更改为 `DatabaseHost`，并为 `Host` 添加了别名</span><span class="sxs-lookup"><span data-stu-id="b8c6e-112">Changed parameter `Host` to `DatabaseHost` and added alias to `Host`</span></span>
    + <span data-ttu-id="b8c6e-113">New-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="b8c6e-113">New-AzureRmDataLakeAnalyticsCatalogSecret</span></span>
    + <span data-ttu-id="b8c6e-114">Set-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="b8c6e-114">Set-AzureRmDataLakeAnalyticsCatalogSecret</span></span>
  - <span data-ttu-id="b8c6e-115">添加了删除 ACL 和默认 ACL 的支持</span><span class="sxs-lookup"><span data-stu-id="b8c6e-115">Add support for ACL and Default ACL removal</span></span>
  - <span data-ttu-id="b8c6e-116">添加了对获取和设置文件与文件夹的未命名权限的支持</span><span class="sxs-lookup"><span data-stu-id="b8c6e-116">Add support for getting and setting unnamed permissions on files and folders</span></span>
* <span data-ttu-id="b8c6e-117">KeyVault</span><span class="sxs-lookup"><span data-stu-id="b8c6e-117">KeyVault</span></span>
  - <span data-ttu-id="b8c6e-118">添加了对证书的支持</span><span class="sxs-lookup"><span data-stu-id="b8c6e-118">Add support for certificates</span></span>
    + <span data-ttu-id="b8c6e-119">Add-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="b8c6e-119">Add-AzureKeyVaultCertificate</span></span>
    + <span data-ttu-id="b8c6e-120">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="b8c6e-120">Add-AzureKeyVaultCertificateContact</span></span>
    + <span data-ttu-id="b8c6e-121">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="b8c6e-121">Get-AzureKeyVaultCertificate</span></span>
    + <span data-ttu-id="b8c6e-122">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="b8c6e-122">Get-AzureKeyVaultCertificateContact</span></span>
    + <span data-ttu-id="b8c6e-123">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="b8c6e-123">Get-AzureKeyVaultCertificateIssuer</span></span>
    + <span data-ttu-id="b8c6e-124">Get-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="b8c6e-124">Get-AzureKeyVaultCertificateOperation</span></span>
    + <span data-ttu-id="b8c6e-125">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="b8c6e-125">Get-AzureKeyVaultCertificatePolicy</span></span>
    + <span data-ttu-id="b8c6e-126">Import-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="b8c6e-126">Import-AzureKeyVaultCertificate</span></span>
    + <span data-ttu-id="b8c6e-127">New-AzureKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="b8c6e-127">New-AzureKeyVaultCertificateAdministratorDetails</span></span>
    + <span data-ttu-id="b8c6e-128">New-AzureKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="b8c6e-128">New-AzureKeyVaultCertificateOrganizationDetails</span></span>
    + <span data-ttu-id="b8c6e-129">New-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="b8c6e-129">New-AzureKeyVaultCertificatePolicy</span></span>
    + <span data-ttu-id="b8c6e-130">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="b8c6e-130">Remove-AzureKeyVaultCertificate</span></span>
    + <span data-ttu-id="b8c6e-131">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="b8c6e-131">Remove-AzureKeyVaultCertificateContact</span></span>
    + <span data-ttu-id="b8c6e-132">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="b8c6e-132">Remove-AzureKeyVaultCertificateIssuer</span></span>
    + <span data-ttu-id="b8c6e-133">Remove-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="b8c6e-133">Remove-AzureKeyVaultCertificateOperation</span></span>
    + <span data-ttu-id="b8c6e-134">Set-AzureKeyVaultCertificateAttribute</span><span class="sxs-lookup"><span data-stu-id="b8c6e-134">Set-AzureKeyVaultCertificateAttribute</span></span>
    + <span data-ttu-id="b8c6e-135">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="b8c6e-135">Set-AzureKeyVaultCertificateIssuer</span></span>
    + <span data-ttu-id="b8c6e-136">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="b8c6e-136">Set-AzureKeyVaultCertificatePolicy</span></span>
    + <span data-ttu-id="b8c6e-137">Stop-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="b8c6e-137">Stop-AzureKeyVaultCertificateOperation</span></span>
* <span data-ttu-id="b8c6e-138">网络</span><span class="sxs-lookup"><span data-stu-id="b8c6e-138">Network</span></span>

  - <span data-ttu-id="b8c6e-139">为网络接口添加了新的开关参数，用于启用/禁用加速网络：+New-AzureRmNetworkInterface -EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="b8c6e-139">New switch parameter added for network interface to enable/disable accelerated networking +New-AzureRmNetworkInterface -EnableAcceleratedNetworking</span></span>
  - <span data-ttu-id="b8c6e-140">使用 PowerShell cmdlet 启用主动-主动网关功能</span><span class="sxs-lookup"><span data-stu-id="b8c6e-140">Enable Active-Active gateway feature PowerShell cmdlets</span></span>
    + <span data-ttu-id="b8c6e-141">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="b8c6e-141">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
    + <span data-ttu-id="b8c6e-142">Remove-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="b8c6e-142">Remove-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="b8c6e-143">添加了新的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="b8c6e-143">Added new cmdlet</span></span>
    + <span data-ttu-id="b8c6e-144">Test-AzureRmPrivateIpAddressAvailability</span><span class="sxs-lookup"><span data-stu-id="b8c6e-144">Test-AzureRmPrivateIpAddressAvailability</span></span>
* <span data-ttu-id="b8c6e-145">资源</span><span class="sxs-lookup"><span data-stu-id="b8c6e-145">Resources</span></span>
  - <span data-ttu-id="b8c6e-146">支持提供程序和资源 cmdlet 中的区域</span><span class="sxs-lookup"><span data-stu-id="b8c6e-146">Support zones in provider and resource cmdlets</span></span>
    + <span data-ttu-id="b8c6e-147">Get-AzureRmProvider</span><span class="sxs-lookup"><span data-stu-id="b8c6e-147">Get-AzureRmProvider</span></span>
    + <span data-ttu-id="b8c6e-148">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="b8c6e-148">New-AzureRmResource</span></span>
    + <span data-ttu-id="b8c6e-149">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="b8c6e-149">Set-AzureRmResource</span></span>
* <span data-ttu-id="b8c6e-150">Sql</span><span class="sxs-lookup"><span data-stu-id="b8c6e-150">Sql</span></span>
  - <span data-ttu-id="b8c6e-151">为服务器级别的 Azure SQL 威胁检测策略管理添加了新的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="b8c6e-151">Added new cmdlets for Azure SQL threat detection policy management at server level</span></span>
    + <span data-ttu-id="b8c6e-152">Get-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b8c6e-152">Get-AzureRmSqlServerThreatDetectionPolicy</span></span>
    + <span data-ttu-id="b8c6e-153">Remove-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b8c6e-153">Remove-AzureRmSqlServerThreatDetectionPolicy</span></span>
    + <span data-ttu-id="b8c6e-154">Set-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b8c6e-154">Set-AzureRmSqlServerThreatDetectionPolicy</span></span>
  - <span data-ttu-id="b8c6e-155">添加了新的 cmdlet 用于支持启用/禁用 SQL Azure 数据仓库的 GeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="b8c6e-155">Added new cmdlets to support enabling/disabling GeoBackupPolicy for Sql Azure DataWarehouses</span></span>
    + <span data-ttu-id="b8c6e-156">Get-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="b8c6e-156">Get-AzureRmSqlDatabaseGeoBackupPolicy</span></span>
    + <span data-ttu-id="b8c6e-157">Set-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="b8c6e-157">Set-AzureRmSqlDatabaseGeoBackupPolicy</span></span>
  - <span data-ttu-id="b8c6e-158">为 Azure SQL 顾问和建议操作 API 添加了新的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="b8c6e-158">Added new cmdlets for Azure Sql Advisors and Recommended Actions APIs</span></span>
    + <span data-ttu-id="b8c6e-159">Get-AzureRmSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="b8c6e-159">Get-AzureRmSqlDatabaseAdvisor</span></span>
    + <span data-ttu-id="b8c6e-160">Get-AzureRmSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="b8c6e-160">Get-AzureRmSqlElasticPoolAdvisor</span></span>
    + <span data-ttu-id="b8c6e-161">Get-AzureRmSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="b8c6e-161">Get-AzureRmSqlServerAdvisor</span></span>
    + <span data-ttu-id="b8c6e-162">Get-AzureRmSqlDatabaseRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="b8c6e-162">Get-AzureRmSqlDatabaseRecommendedActions</span></span>
    + <span data-ttu-id="b8c6e-163">Get-AzureRmSqlElasticPoolRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="b8c6e-163">Get-AzureRmSqlElasticPoolRecommendedActions</span></span>
    + <span data-ttu-id="b8c6e-164">Get-AzureRmSqlServerRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="b8c6e-164">Get-AzureRmSqlServerRecommendedActions</span></span>
    + <span data-ttu-id="b8c6e-165">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="b8c6e-165">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span></span>
    + <span data-ttu-id="b8c6e-166">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="b8c6e-166">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span></span>
    + <span data-ttu-id="b8c6e-167">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="b8c6e-167">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span></span>
    + <span data-ttu-id="b8c6e-168">Set-AzureRmSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="b8c6e-168">Set-AzureRmSqlDatabaseRecommendedActionState</span></span>
    + <span data-ttu-id="b8c6e-169">Set-AzureRmSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="b8c6e-169">Set-AzureRmSqlElasticPoolRecommendedActionState</span></span>
    + <span data-ttu-id="b8c6e-170">Set-AzureRmSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="b8c6e-170">Set-AzureRmSqlServerRecommendedActionState</span></span>
