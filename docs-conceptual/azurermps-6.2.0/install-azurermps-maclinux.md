---
title: 在 macOS 或 Linux 上安装 Azure PowerShell
description: 如何在 macOS 或 Linux 上安装 Azure PowerShell。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/06/2018
ms.openlocfilehash: 17912c155255b6fdfd3cfb9242163b67d405dc03
ms.sourcegitcommit: bcf80dfd7fbe17e82e7ad029802cfe8a2f02b15c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "35323163"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a>在 macOS 或 Linux 上安装 Azure PowerShell

对于非 Windows 平台，可以在 PowerShell Core v6 的基础上运行 Azure PowerShell。 本产品不是基于 .NET Framework for Windows 构建的标准 Azure PowerShell，它是针对 .NET Core 构建的并且可以在支持 .Net Core 运行时的任何平台上运行。

> [!NOTE]
> 目前，PowerShell Core v6 和 Azure PowerShell for .NET Core 都还是 beta 版本。
> 对这些产品的支持也是有限的。 如果你有需要询问的问题或发现了 bug，请在 GitHub 上提出问题。
>
> * [PowerShell Core v6 的问题](https://github.com/PowerShell/PowerShell/issues)
> * [Azure PowerShell 的问题](https://github.com/azure/azure-docs-powershell/issues)

## <a name="install-powershell-core-v6"></a>安装 PowerShell Core v6

在 Linux 或 macOS 上安装 PowerShell Core v6 的过程因 Linux 分发版和 OS 版本而异。
可在以下文章中找到详细说明：

- [在 macOS 上安装 PowerShell Core](/powershell/scripting/setup/installing-powershell-core-on-macos)
- [在 Linux 上安装 PowerShell Core](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-core"></a>安装 Azure PowerShell for .NET Core

PowerShell Core v6 随已安装的 PowerShellGet 模块一起提供。 这使得安装发布到 PowerShell 库的任何模块非常容易。 若要安装 Azure PowerShell，请打开一个新的 PowerShell 会话并运行以下命令：

```powershell
Install-Module AzureRM.NetCore
```

## <a name="load-the-azurermnetcore-module"></a>加载 AzureRM.Netcore 模块

安装该模块后，需要将它加载到 PowerShell 会话中。 可以使用 `Import-Module` cmdlet 加载模块，如下所示：

```powershell
Import-Module AzureRM.Netcore
Import-Module AzureRM.Profile.Netcore
```

导入完成后，可以通过使用以下命令尝试登录到 Azure，测试新安装的模块：

```powershell
Connect-AzureRmAccount
```

以上命令将提示你转到 `https://aka.ms/devicelogin` 并输入提供的代码。

## <a name="available-cmdlets"></a>可用的 cmdlet

适用于 .NET 标准的 Azure PowerShell 模块仍处于开发之中。 这些模块不提供可用于模块 Windows 版本的完整 cmdlet 集。 AzureRM.Netcore 模块中实现了以下功能：

* 帐户管理
  - 通过 Microsoft Azure Active Directory 使用 Microsoft 帐户、组织帐户或服务主体登录
  - 通过 Save-AzureRmContext 将凭据保存到磁盘，然后使用 Import-AzureRmContext 加载保存的凭据
* 环境
  - 获取不同的现成 Microsoft Azure 环境
  - 添加/设置/删除自定义环境（如 Azure Stack 或 Windows Azure Pack 环境）
* 使用资源管理器和服务管理接口的 Azure 服务管理平面 cmdlet。
  - 虚拟机
  - 应用服务（网站）
  - SQL 数据库
  - 存储
  - 网络

## <a name="next-steps"></a>后续步骤

有关使用 Azure PowerShell 的详细信息，请参阅 [Azure PowerShell 入门](get-started-azureps.md)一文。
