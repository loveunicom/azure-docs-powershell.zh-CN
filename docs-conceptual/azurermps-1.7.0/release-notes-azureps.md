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
ms.openlocfilehash: 9a40eae86b60afb5e04dd6a6074b60e82731578f
ms.sourcegitcommit: c98e3a21037ebd82936828bcb544eed902b24212
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/08/2018
ms.locfileid: "34854624"
---
# <a name="release-notes"></a>发行说明

下面是此版本中对 Azure PowerShell 所做的更改列表。

## <a name="version-170"></a>版本 1.7.0

* **所有 cmdlet 的 -Force、–Confirm 和 $ConfirmPreference 参数的行为更改。我们正在根据 PowerShell 准则更改此实现。对于大多数 cmdlet，这意味着删除 Force 参数，并且若要跳过 ShouldProcess 提示，用户需要在其 PowerShell 脚本中包含“-Confirm:$false”参数。** 此更改将解决以下问题：
  - 正确实现 -WhatIf 功能，允许用户确定 cmdlet 或脚本的影响，而无需进行任何实际更改
  - 使用会话范围的 $ConfirmPreference 控制提示，以便根据预期更改的影响（在 cmdlet 的 ConfirmImpact 设置中报告）提示用户
  - 使用 –Confirm 参数对确认提示进行 Cmdlet 特定的控制
  - 在各个 cmdlet 之间一致使用 ShouldContinue 和 –Force 参数，仅针对由于更改的特殊性质（例如，删除隐藏的文件）而需要用户提示的操作
  - 与其他 PowerShell cmdlet 保持一致，使其他 cmdlet 的 PowerShell 脚本知识可立即适用于 Azure PowerShell cmdlet。

**请注意，现在为了*在所有情况下跳过所有提示*，Azure PowerShell cmdlet 要求用户提供两个参数：**
```powershell
My-CmdletWithConfirmation –Confirm:$false -Force
```
* Azure 计算
  - Set-AzureRmVMADDomainExtension
  - Get-AzureRmVMADDomainExtension
  - Restart-AzureVM 的 -Redeploy 参数
  - Move-AzureService、Move-AzureStorageAccount 和 Move-AzureVirtualNetwork 的 -Validate 参数
  - 像以前一样，扩展 cmdlet 的名称和版本参数是可选的。
  - New-AzureVM 可从 VM 对象中获取许可证类型。
* Azure 存储
  - 将 Tags 参数更改为 Tag，并添加了参数别名 Tags
    + New-AzureRmStorageAccount
    + Set-AzureRmStorageAccount
* Azure 网络
  - 为虚拟网络对等互连添加了新的 cmdlet
* Azure Redis Cache
  - 为 Reset-AzureRmRedisCache 添加了新的 cmdlet
  - 为 Export-AzureRmRedisCache 添加了新的 cmdlet
  - 为 Import-AzureRmRedisCache 添加了新的 cmdlet
  - 修改了 cmdlet New-AzureRmRedisCache，在其中包含了 vNet 的参数更改
* Azure SQL 数据库备份/还原
  - LTR（长期保留）备份功能的 Cmdlet
  - Get-AzureRmSqlServerBackupLongTermRetentionVault
  - Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy
  - Set-AzureRmSqlServerBackupLongTermRetentionVault
  - Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy
  - Restore-AzureRmSqlDatabase 现在支持已删除的数据库的时间点还原
  - Restore-AzureRmSqlDatabase 现在支持从长期保留备份中还原
* Azure 逻辑应用
  - 添加了逻辑应用集成帐户 cmdlet。
  - Get-AzureRmIntegrationAccountAgreement
  - Get-AzureRmIntegrationAccountCallbackUrl
  - Get-AzureRmIntegrationAccountCertificate
  - Get-AzureRmIntegrationAccount
  - Get-AzureRmIntegrationAccountMap
  - Get-AzureRmIntegrationAccountPartner
  - Get-AzureRmIntegrationAccountSchema
  - New-AzureRmIntegrationAccountAgreement
  - New-AzureRmIntegrationAccountCertificate
  - New-AzureRmIntegrationAccount
  - New-AzureRmIntegrationAccountMap
  - New-AzureRmIntegrationAccountPartner
  - New-AzureRmIntegrationAccountSchema
  - Remove-AzureRmIntegrationAccountAgreement
  - Remove-AzureRmIntegrationAccountCertificate
  - Remove-AzureRmIntegrationAccount
  - Remove-AzureRmIntegrationAccountMap
  - Remove-AzureRmIntegrationAccountPartner
  - Remove-AzureRmIntegrationAccountSchema
  - Set-AzureRmIntegrationAccountAgreement
  - Set-AzureRmIntegrationAccountCertificate
  - Set-AzureRmIntegrationAccount
  - Set-AzureRmIntegrationAccountMap
  - Set-AzureRmIntegrationAccountPartner
  - Set-AzureRmIntegrationAccountSchema
* Azure Data Lake Store
  - 大幅提高了文件和文件夹上传与下载的性能。
  - 这包括对用于下载的参数名称的轻微更改，并包含用于上传的两个新参数：
    + NumThreads -> PerFileThreadCount，用于指示要在单个文件中使用的线程数
    + ConcurrentFileCount，用于指示上传/下载文件夹的过程中同时上传/下载的文件数。
  - 默认线程值现已设计为针对大多数文件大小全面改善吞吐量。 如果性能不符合要求，可以修改上述值来满足要求。
* Azure Data Lake Analytics
  - 在不结合任何参数调用的情况下，Get-AzureRMDataLakeAnalyticsDataSource 现在返回所有数据源。
  - 此更改还从 cmdlet 中删除了数据源类型参数。
  - 此更改导致针对列表操作返回包含以下属性的新对象：
    + Type：数据源的类型
    + Name：数据源的名称
    + IsDefault：如果这是帐户的默认数据源，则设置为 true
  - Get-AzureRMDataLakeAnalyticsJob 已修复。根据 submittedBefore 和 submittedAfter 筛选时，可以正常返回某些日期时间偏移值的列表。
* Web 应用
  - 为常规交换和包含预览的交换添加了 Swap-AzureRmWebAppSlot cmdlet
  - 扩展了 AzureRmWebAppSlot cmdlet 以支持自动交换
* Azure API 管理
  - 修复了 AzureChinaCloud 的 Azure API 管理部署 cmdlet。
  - 删除了 cmdlet Set-AzureRmApiManagementTenantGitAccess，因为 Git 访问默认已启用。
* Azure 恢复服务备份
  - 添加了对 Azure SQL 工作负荷的支持
  - 添加了对备份和还原已加密 Azure VM 的支持
  - Backup-AzureRmRecoveryServicesBackupItem - 为恢复点添加了可选的保留时间功能
  - 在 Get-AzureRmRecoveryServicesBackupContainer 和 Get-AzureRmRecoveryServicesBackupItem cmdlet 中进行了轻微的筛选器相关 bug 修复
* Azure 自动化
  - 添加了 Get-AzureRmAutomationHybridWorkerGroup
