---
title: 安装和配置 Azure PowerShell 服务管理模块 | Microsoft Docs
description: 如何安装和配置首次使用的 Azure PowerShell。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/06/2017
ms.openlocfilehash: 5f59e5e5fec4fb721ac7548c12c906c7c8d5733e
ms.sourcegitcommit: c98e3a21037ebd82936828bcb544eed902b24212
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/08/2018
ms.locfileid: "34854964"
---
# <a name="installing-the-azure-powershell-service-management-module"></a>安装 Azure PowerShell 服务管理模块

从 [PowerShell 库](https://www.powershellgallery.com/)安装 Azure PowerShell 是首选的安装方法。

## <a name="step-1-install-powershellget"></a>步骤 1：安装 PowerShellGet

安装 PowerShell 库中的项需要 PowerShellGet 模块。 请确保使用适当版本的 PowerShellGet 并满足其他系统要求。 运行以下命令，确定是否已在系统上安装 PowerShellGet。

```powershell
Get-Module PowerShellGet -list | Select-Object Name,Version,Path
```

应会看到类似于下面的信息：

```
Name          Version Path
----          ------- ----
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

如果没有安装 PowerShellGet，请参阅[如何获取 PowerShellGet](#how-to-get-powershellget)。

## <a name="step-2-install-azure-powershell"></a>步骤 2：安装 Azure PowerShell

在以管理员身份运行的 Windows PowerShell 控制台中运行以下命令：

```powershell
Install-Module Azure
```

Azure 模块是 Azure 资源管理器 cmdlet 的汇总模块。 安装 AzureRM 模块时，将从 PowerShell 库下载并安装先前尚未安装的其他所有 Azure 模块。

Azure 服务管理模块与 Azure PowerShell Resource Manager 模块共享依赖项。 如果已安装 Azure PowerShell Resource Manager 模块，需在安装命令中添加 `-AllowClobber` 参数。 这样，便可以更新现有的共享依赖项。 如果不提供此参数，模块安装会失败。

```powershell
Install-Module Azure -AllowClobber
```

安装此模块后，可运行以下命令导入此模块：

```powershell
Import-Module Azure
```

## <a name="to-use-the-cmdlets"></a>使用 cmdlet

若要开始使用 Azure 服务管理 cmdlet，请先登录到 Azure 帐户。 若要登录到帐户，请运行以下命令：

```powershell
Add-AzureAccount
```

登录到 Azure 后，Azure PowerShell 将为给定的会话创建上下文。 该上下文包含用于该会话中的所有 cmdlet 的 Azure PowerShell 环境、帐户、租户和订阅。 现已准备就绪，可以使用下面的模块。

## <a name="azure-service-management-cmdlets"></a>Azure 服务管理 cmdlet

Azure PowerShell 模块经常更新。 如果发现 cmdlet 联机帮助包含模块中所不包含的 cmdlet 或参数，请下载并安装最新版本的模块。 若要查找模块版本，请键入：`(Get-Module Azure).Version`。

有关可帮助自动完成 Azure 中某些常见任务的示例脚本，请参阅 [Windows Azure 脚本中心](http://www.windowsazure.com/documentation/scripts/)。

有关安装、学习、使用和自定义 Windows PowerShell 的一般信息，请参阅[使用 Windows PowerShell 编写脚本](http://go.microsoft.com/fwlink/p/?linkid=320210)。

### <a name="how-to-get-powershellget"></a>如何获取 PowerShellGet

|OS 版本。|安装说明|
|---|---|
|我使用的是 Windows 10 或 Windows Server 2016|内置在 OS 随附的 Windows Management Framework (WMF) 5.0 中|
|我想要升级到 PowerShell 5|[安装最新版本的 WMF](https://www.microsoft.com/en-us/download/details.aspx?id=54616)|
|我正在运行某个包含 PowerShell 3 或 PowerShell 4 的 Windows 版本|[获取 PackageManagement 模块](http://go.microsoft.com/fwlink/?LinkID=746217)|

<a id="helpmechoose"></a>
### <a name="checking-the-version-of-azure-powershell"></a>检查 Azure PowerShell 的版本

虽然我们建议尽早升级到最新版本，但仍然支持多个 Azure PowerShell 版本。 若要确定安装的 Azure PowerShell 版本，请从命令行运行 `Get-Module AzureRM`。

```powershell
Get-Module AzureRM -list | Select-Object Name,Version,Path
```
