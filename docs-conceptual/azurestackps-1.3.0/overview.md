---
title: Azure Stack 管理员 PowerShell 概述 | Microsoft Docs
description: 概述 Azure Stack 管理员 PowerShell 并提供安装和配置说明。
author: bganapa
ms.author: bganapa
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 09/21/2018
ms.openlocfilehash: fb892daeafb1365ea62324392ac806cf9f3d39cf
ms.sourcegitcommit: 558436c824d9b59731aa9b963cdc8df4dea932e7
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/29/2018
ms.locfileid: "52586660"
---
# <a name="azure-stack-module-130"></a>Azure Stack 模块 1.3.0

## <a name="requirements"></a>要求：
Azure Stack 最低支持版本为 1804。

注意：如果使用的是早期版本，请安装版本 1.2.11

## <a name="known-issues"></a>已知问题：

- 关闭警报需要 Azure Stack 版本 1803
- 某些存储 cmdlet 需要 Azure Stack 版本 1804
- New-AzsOffer 不允许创建状态为“公共”的产品/服务。 随后需调用 Set-AzsOffer cmdlet 来更改状态。
- 在不重新部署的情况下，不能删除 IP 池

## <a name="breaking-changes"></a>重大更改
从 1.2.11 迁移时，所有重大更改记录在此处： https://aka.ms/azspowershellmigration

## <a name="install"></a>安装
```
# Remove previous Versions
Uninstall-Module AzureRM.AzureStackAdmin -Force
Uninstall-Module AzureRM.AzureStackStorage -Force
Uninstall-Module -Name AzureStack -Force 


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2017-03-09-profile -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.3.0
```
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
Azure Stack 计算管理员模块的预览版，其提供的功能用于管理计算配额、平台映像和虚拟机扩展。

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
