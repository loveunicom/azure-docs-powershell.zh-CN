---
title: Azure Stack PowerShell 概述 | Microsoft Docs
description: 概述 Azure Stack PowerShell 并提供安装和配置说明。
author: bganapa
ms.author: bganapa
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 09/21/2018
ms.openlocfilehash: d514e43d82bcb51f65831dc506e58e8747db0381
ms.sourcegitcommit: 19dffee617477001f98d43e39a50ce1fad087b74
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2018
ms.locfileid: "47178453"
---
# <a name="azurerm-module-230"></a>AzureRM 模块 2.3.0

## <a name="requirements"></a>要求：
Azure Stack 最低支持版本为 1808。

注意：如果使用的是早期版本，请安装版本 1.2.11


## <a name="install"></a>安装
```powershell
# Remove previous versions of AzureStack modules
Uninstall-Module -Name AzureStack -Force 
Uninstall-Module -Name AzureRM -Force 
Uninstall-Module AzureRM.AzureStackAdmin -Force -ErrorAction Continue
Uninstall-Module AzureRM.AzureStackStorage -Force -ErrorAction Continue
Get-Module Azs.* -ListAvailable | Uninstall-Module -Force
Get-Module Azure.* -ListAvailable | Uninstall-Module -Force


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2018-03-01-hybrid -Force

```

##<a name="release-notes"></a>发行说明
* 发行版 2.3.0 附带一系列重大变更。 若要从 1.2.11 版升级，请使用我们在 https://aka.ms/azspowershellmigration 创建的迁移指南
* 此发行版对应于特定于 azurestack 的 API 配置文件 2018-03-01-hybrid
* 所有模块都会采用高于或等于 AzureRm.Profile 模块依赖项的版本。
* 每个模块支持的 API 版本都会更新。 
    * 计算 - 2017-03-30
    * 网络 - 2017-10-01
    * 存储 - 2016-01-01
    * 资源 - 2018-02-01
    * Keyvault - 2016-10-01
    * Dns - 2016-04-01
* https://github.com/Azure/azure-rest-api-specs/blob/master/profile/2018-03-01-hybrid.json 提供每个资源类型的完整 API 版本映射

## <a name="content"></a>内容：
### <a name="azure-bridge"></a>Azure Bridge
Azure Stack AzureBridge 管理员模块的预览版，用于联合 Azure 提供的映像。

### <a name="backup"></a>备份
备份管理员模块的预览版，允许管理员执行以下操作：
- 配置备份的存储位置
- 执行备份
- 列出和还原完成的备份

### <a name="commerce"></a>商务
Azure Stack 商务管理员模块的预览版，用于查看整个 Azure Stack 系统的聚合数据使用情况。

### <a name="compute"></a>计算
Azure Stack 计算管理员模块的预览版，其提供的功能用于管理计算配额、平台映像、托管磁盘和虚拟机扩展。

### <a name="fabric"></a>Fabric
Azure Stack Fabric 管理员模块的预览版，允许管理员查看和管理基础结构组件：
- 停止、启动和关闭缩放单元节点
- 针对 FRU 相关活动清空和恢复缩放单元节点
- 修复缩放单元节点
- 重启基础结构角色
- 停止、启动和关闭基础结构角色实例
- 创建新的 IP 池


### <a name="gallery"></a>库
Azure Stack 库管理员模块的预览版，其提供的功能用于管理 Azure Stack 市场中的库项。

### <a name="infrastructure-insights"></a>基础结构见解
基础结构见解管理员模块的预览版，允许管理员执行以下操作：
- 查看 Azure Stack 戳资源的运行状况
- 查看和管理警报

### <a name="keyvault"></a>KeyVault
Azure Stack KeyVault 管理员模块的预览版，允许管理员查看 KeyVault 配额。

### <a name="network"></a>网络
网络管理员模块的预览版，用于执行以下操作：
- 管理网络配额
- 查看分配的网络资源，例如公共 IP 地址、虚拟网络、负载均衡器
- 提供一个显示管理员概览的 cmdlet

### <a name="storage"></a>存储
Azure Stack 存储管理员模块的预览版。  此版本提供以下功能：
- 管理存储配额
- 回收删除的存储资源
- 还原删除的存储帐户
- 将容器从一个共享迁移到另一个共享
- 查看单个存储组件的信息
- 查看使用情况和性能信息

### <a name="subscription-admin"></a>订阅管理员
Azure Stack 订阅管理员模块的预览版。  此模块提供的功能允许管理员执行以下操作：
- 管理计划和套餐
- 查看使用情况和性能信息
- 管理 RBAC

### <a name="subscription"></a>订阅
Azure Stack 订阅模块的预览版。  此模块提供的功能允许用户执行以下操作：
- 创建、删除和更新订阅

### <a name="update"></a>更新
Azure Stack 更新管理员模块的预览版。  在此模块中，管理员可以执行以下操作：
- 列出和安装可用更新
- 恢复中断的更新
- 查看安装的更新
