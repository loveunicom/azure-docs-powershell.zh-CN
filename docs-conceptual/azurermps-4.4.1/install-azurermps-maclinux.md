---
title: 在 macOS 和 Linux 上安装和配置 Azure PowerShell | Microsoft Docs
description: 如何在 macOS 和 Linux 上安装和配置首次使用的 Azure PowerShell。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/12/2018
ms.openlocfilehash: 336acecfdaee0eee0862805064ac5aab90a32982
ms.sourcegitcommit: c98e3a21037ebd82936828bcb544eed902b24212
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/08/2018
ms.locfileid: "34853536"
---
# <a name="install-and-configure-azure-powershell-on-macos-and-linux"></a>在 macOS 和 Linux 上安装和配置 Azure PowerShell

现在，非 Windows 平台上也可以安装 PowerShell Core v6 和 Azure PowerShell 了。
在 macOS 和 Linux 上安装 Azure PowerShell 的过程与在 Windows 上的安装过程相同，但是，必须首先安装 PowerShell Core v6。

> [!NOTE]

> 目前，PowerShell Core v6 和 Azure PowerShell for .NET Core 都还是 beta 版本。
> 对这些产品的支持也是有限的。 如果你发现问题或 bug，请在 GitHub 中提出问题。
>
> * [PowerShell Core v6 的问题](https://github.com/PowerShell/PowerShell/issues)
> * [Azure PowerShell 的问题](https://github.com/azure/azure-docs-powershell/issues)

## <a name="step-1-install-powershell-core-v6"></a>步骤 1：安装 PowerShell Core v6

PowerShell Core v6 的安装过程因目标操作系统而异。
虽然可在 Windows 上安装 PowerShell Core v6，但本文将重点介绍在 macOS 和 Linux 上进行安装。 如果想要在 Windows 上使用 Azure PowerShell，请参阅适用于 Windows 的[安装](./install-azurerm-ps.md)文章。

在 Linux 或 macOS 上安装 **PowerShell Core v6** 的过程因 Linux 分发版和 OS 版本而异。
可以在以下文章中找到详细说明：

- [在 macOS 和 Linux 上安装 PowerShell Core](/powershell/scripting/setup/installing-powershell-core-on-macos-and-linux)

## <a name="step-2-install-azure-powershell-for-net-core"></a>步骤 2：安装 Azure PowerShell for .NET Core

PowerShell Core v6 随已安装的 PowerShellGet 模块一起提供。 这使得安装发布到 PowerShell 库的任何模块非常容易。 若要安装 Azure PowerShell，请打开一个新的 PowerShell 会话并运行以下命令：

```powershell
Install-Module AzureRM.NetCore
```

## <a name="step-3-load-the-azurermnetcore-module"></a>步骤 3：加载 AzureRM.Netcore 模块

安装该模块后，需要将它加载到 PowerShell 会话中。 可以使用 `Import-Module` cmdlet 加载模块，如下所示：

```powershell
Import-Module AzureRM.Netcore
Import-Module AzureRM.Profile.Netcore
```

导入完成后，可以通过使用以下命令尝试登录到 Azure，测试新安装的模块：

```powershell
Login-AzureRMAccount
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
