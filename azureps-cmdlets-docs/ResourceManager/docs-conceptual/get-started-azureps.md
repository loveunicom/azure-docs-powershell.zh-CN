---
title: "Azure PowerShell 入门 | Microsoft Docs"
description: 
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: get-started-article
ms.date: 03/30/2017
ms.openlocfilehash: f1c13317f0b42b547166a8130dd8c29bed5759c9
ms.sourcegitcommit: db5c50de90764a9bdc7c1f1dbca3aed5bfeb05fa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/22/2017
---
# <a name="getting-started-with-azure-powershell"></a><span data-ttu-id="f7a9d-102">Azure PowerShell 入门</span><span class="sxs-lookup"><span data-stu-id="f7a9d-102">Getting started with Azure PowerShell</span></span>

<span data-ttu-id="f7a9d-103">Azure PowerShell 用于从命令行管理 Azure 资源，以及生成可以针对 Azure Resource Manager 运行的自动化脚本。</span><span class="sxs-lookup"><span data-stu-id="f7a9d-103">Azure PowerShell is designed for managing and administering Azure resources from the command line, and for building automation scripts that work against the Azure Resource Manager.</span></span> <span data-ttu-id="f7a9d-104">本文将帮助你开始使用 Azure PowerShell，并讲解其重要概念。</span><span class="sxs-lookup"><span data-stu-id="f7a9d-104">This article helps get you started using it, and teaches you the core concepts behind it.</span></span>

## <a name="install-azure-powershell"></a><span data-ttu-id="f7a9d-105">安装 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="f7a9d-105">Install Azure PowerShell</span></span>

<span data-ttu-id="f7a9d-106">首先，请确保已安装最新版本的 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="f7a9d-106">The first step is to make sure you have the latest version of the Azure PowerShell installed.</span></span> <span data-ttu-id="f7a9d-107">有关最新版本的信息，请参阅[发行说明](./release-notes-azureps.md)。</span><span class="sxs-lookup"><span data-stu-id="f7a9d-107">For information about the latest release, see the [release notes](./release-notes-azureps.md).</span></span>

1. <span data-ttu-id="f7a9d-108">[安装 Azure PowerShell](install-azurerm-ps.md)。</span><span class="sxs-lookup"><span data-stu-id="f7a9d-108">[Install Azure PowerShell](install-azurerm-ps.md).</span></span>
2. <span data-ttu-id="f7a9d-109">若要验证安装是否成功，请从命令行运行 `Get-Module AzureRM`。</span><span class="sxs-lookup"><span data-stu-id="f7a9d-109">To verify the installation was successful, run `Get-Module AzureRM` from your command line.</span></span>

## <a name="log-in-to-azure"></a><span data-ttu-id="f7a9d-110">登录 Azure</span><span class="sxs-lookup"><span data-stu-id="f7a9d-110">Log in to Azure</span></span>

<span data-ttu-id="f7a9d-111">以交互方式登录：</span><span class="sxs-lookup"><span data-stu-id="f7a9d-111">Sign on interactively:</span></span>

1. <span data-ttu-id="f7a9d-112">键入 `Login-AzureRmAccount`。</span><span class="sxs-lookup"><span data-stu-id="f7a9d-112">Type `Login-AzureRmAccount`.</span></span> <span data-ttu-id="f7a9d-113">此时会出现一个对话框，要求输入 Azure 凭据。</span><span class="sxs-lookup"><span data-stu-id="f7a9d-113">You will get dialog box asking for your Azure credentials.</span></span> <span data-ttu-id="f7a9d-114">通过 '-EnvironmentName' 选项可登录 Azure China 或 Azure Germany。</span><span class="sxs-lookup"><span data-stu-id="f7a9d-114">Option '-EnvironmentName' can let you login in Azure China or Azure Germany.</span></span>

   <span data-ttu-id="f7a9d-115">例如 Login-AzureRmAccount -EnvironmentName AzureChinaCloud</span><span class="sxs-lookup"><span data-stu-id="f7a9d-115">e.g. Login-AzureRmAccount -EnvironmentName AzureChinaCloud</span></span>

2. <span data-ttu-id="f7a9d-116">键入与帐户关联的电子邮件地址和密码。</span><span class="sxs-lookup"><span data-stu-id="f7a9d-116">Type the email address and password associated with your account.</span></span> <span data-ttu-id="f7a9d-117">Azure 将对凭据信息进行身份验证和保存，然后关闭该窗口。</span><span class="sxs-lookup"><span data-stu-id="f7a9d-117">Azure authenticates and saves the credential information, and then closes the window.</span></span>

<span data-ttu-id="f7a9d-118">登录到 Azure 帐户后，可以使用 Azure PowerShell cmdlet 访问和管理器订阅中的资源。</span><span class="sxs-lookup"><span data-stu-id="f7a9d-118">Once you have signed in to an Azure account, you can use the Azure PowerShell cmdlets to access and manager the resources in your subscription.</span></span>

## <a name="create-a-resource-group"></a><span data-ttu-id="f7a9d-119">创建资源组</span><span class="sxs-lookup"><span data-stu-id="f7a9d-119">Create a resource group</span></span>

<span data-ttu-id="f7a9d-120">完成所有设置后，让我们使用 Azure PowerShell 在 Azure 中创建资源。</span><span class="sxs-lookup"><span data-stu-id="f7a9d-120">Now that we've got everything set up, let's use Azure PowerShell to create resources within Azure.</span></span>

<span data-ttu-id="f7a9d-121">首先，请创建一个资源组。</span><span class="sxs-lookup"><span data-stu-id="f7a9d-121">First, create a Resource Group.</span></span> <span data-ttu-id="f7a9d-122">使用 Azure 中的资源组可以同时管理希望以逻辑方式分组的多个资源。</span><span class="sxs-lookup"><span data-stu-id="f7a9d-122">Resource Groups in Azure provide a way to manage multiple resources that you want to logically group together.</span></span> <span data-ttu-id="f7a9d-123">例如，可为应用程序或项目创建资源组，并在其中添加虚拟机、数据库和 CDN 服务。</span><span class="sxs-lookup"><span data-stu-id="f7a9d-123">For example, you might create a Resource Group for an application or project and add a virtual machine, a database and a CDN service within it.</span></span>

<span data-ttu-id="f7a9d-124">让我们在 Azure 的西欧区域创建一个名为“MyResourceGroup”的资源组。</span><span class="sxs-lookup"><span data-stu-id="f7a9d-124">Let's create a resource group named "MyResourceGroup" in the westeurope region of Azure.</span></span> <span data-ttu-id="f7a9d-125">为此，请键入以下命令：</span><span class="sxs-lookup"><span data-stu-id="f7a9d-125">To do so type the following command:</span></span>

```powershell
New-AzureRmResourceGroup -Name 'myResourceGroup' -Location 'westeurope'
```

```
ResourceGroupName : myResourceGroup
Location          : westeurope
ProvisioningState : Succeeded
Tags              :
ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myResourceGroup
```

## <a name="create-a-windows-virtual-machine"></a><span data-ttu-id="f7a9d-126">创建 Windows 虚拟机</span><span class="sxs-lookup"><span data-stu-id="f7a9d-126">Create a Windows Virtual Machine</span></span>

<span data-ttu-id="f7a9d-127">创建资源组后，让我们在其中创建 Windows VM。</span><span class="sxs-lookup"><span data-stu-id="f7a9d-127">Now that we have our resource group, let's create a Windows VM within it.</span></span> <span data-ttu-id="f7a9d-128">要创建新的 VM，必须先创建其他所需的资源并将其分配到配置中。</span><span class="sxs-lookup"><span data-stu-id="f7a9d-128">To create a new VM we must first create the other required resources and assign them to a configuration.</span></span> <span data-ttu-id="f7a9d-129">然后，可以使用该配置来创建 VM。</span><span class="sxs-lookup"><span data-stu-id="f7a9d-129">Then we can use that configuration to create the VM.</span></span>

### <a name="create-the-required-network-resources"></a><span data-ttu-id="f7a9d-130">创建所需的网络资源</span><span class="sxs-lookup"><span data-stu-id="f7a9d-130">Create the required network resources</span></span>

<span data-ttu-id="f7a9d-131">首先，需要创建一个子网配置，以便在创建虚拟网络过程中使用。</span><span class="sxs-lookup"><span data-stu-id="f7a9d-131">First we need to create a subnet configuration to be used with the virtual network creation process.</span></span> <span data-ttu-id="f7a9d-132">此外，还要创建一个公共 IP 地址，以便能够连接到此 VM。</span><span class="sxs-lookup"><span data-stu-id="f7a9d-132">We also create a public IP address so that we can connect to this VM.</span></span> <span data-ttu-id="f7a9d-133">我们将创建一个网络安全组来保护对公共地址的访问。</span><span class="sxs-lookup"><span data-stu-id="f7a9d-133">We create a network security group to secure access to the public address.</span></span> <span data-ttu-id="f7a9d-134">最后，使用上述所有资源创建虚拟 NIC。</span><span class="sxs-lookup"><span data-stu-id="f7a9d-134">Finally we create the virtual NIC using all of the previous resources.</span></span>

```powershell
# Variables for common values
$resourceGroup = "myResourceGroup"
$location = "westeurope"
$vmName = "myWindowsVM"

# Create a subnet configuration
$subnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name mySubnet1 -AddressPrefix 192.168.1.0/24

# Create a virtual network
$vnet = New-AzureRmVirtualNetwork -ResourceGroupName $resourceGroup -Location $location `
  -Name MYvNET1 -AddressPrefix 192.168.0.0/16 -Subnet $subnetConfig

# Create a public IP address and specify a DNS name
$publicIp = New-AzureRmPublicIpAddress -ResourceGroupName $resourceGroup -Location $location `
  -Name "mypublicdns$(Get-Random)" -AllocationMethod Static -IdleTimeoutInMinutes 4
$publicIp | Select-Object Name,IpAddress

# Create an inbound network security group rule for port 3389
$nsgRuleRDP = New-AzureRmNetworkSecurityRuleConfig -Name myNetworkSecurityGroupRuleRDP  -Protocol Tcp `
  -Direction Inbound -Priority 1000 -SourceAddressPrefix * -SourcePortRange * -DestinationAddressPrefix * `
  -DestinationPortRange 3389 -Access Allow

# Create a network security group
$nsg = New-AzureRmNetworkSecurityGroup -ResourceGroupName $resourceGroup -Location $location `
  -Name myNetworkSecurityGroup1 -SecurityRules $nsgRuleRDP

# Create a virtual network card and associate with public IP address and NSG
$nic = New-AzureRmNetworkInterface -Name myNic1 -ResourceGroupName $resourceGroup -Location $location `
  -SubnetId $vnet.Subnets[0].Id -PublicIpAddressId $publicIp.Id -NetworkSecurityGroupId $nsg.Id
```

### <a name="create-the-virtual-machine"></a><span data-ttu-id="f7a9d-135">创建虚拟机</span><span class="sxs-lookup"><span data-stu-id="f7a9d-135">Create the virtual machine</span></span>

<span data-ttu-id="f7a9d-136">首先，需要提供 OS 的一组凭据。</span><span class="sxs-lookup"><span data-stu-id="f7a9d-136">First we need a set of credentials for the OS.</span></span>

```powershell
# Create user object
$cred = Get-Credential -Message "Enter a username and password for the virtual machine."
```

<span data-ttu-id="f7a9d-137">准备好所需的资源后，便可以创建 VM。</span><span class="sxs-lookup"><span data-stu-id="f7a9d-137">Now that we have the required resources we can create the VM.</span></span> <span data-ttu-id="f7a9d-138">在此步骤中，我们将创建一个 VM 配置对象，然后使用该配置来创建 VM。</span><span class="sxs-lookup"><span data-stu-id="f7a9d-138">For this step, we create a VM configuration object, then we use the configuration to create the VM.</span></span>

```powershell
# Create a virtual machine configuration
$vmConfig = New-AzureRmVMConfig -VMName $vmName -VMSize Standard_D1 |
  Set-AzureRmVMOperatingSystem -Windows -ComputerName $vmName -Credential $cred |
  Set-AzureRmVMSourceImage -PublisherName MicrosoftWindowsServer -Offer WindowsServer -Skus 2016-Datacenter -Version latest |
  Add-AzureRmVMNetworkInterface -Id $nic.Id

# Create a virtual machine
New-AzureRmVM -ResourceGroupName $resourceGroup -Location $location -VM $vmConfig
```

<span data-ttu-id="f7a9d-139">完全创建并已准备好使用 VM 后，`New-AzureRmVM` 命令将输出结果。</span><span class="sxs-lookup"><span data-stu-id="f7a9d-139">The `New-AzureRmVM` command outputs results once the VM has been fully created and is ready to be used.</span></span>

```
RequestId IsSuccessStatusCode StatusCode ReasonPhrase
--------- ------------------- ---------- ------------
                         True         OK OK
```

<span data-ttu-id="f7a9d-140">现在，请使用远程桌面和 VM 的公共 IP 地址登录到新建的 Windows Server VM。</span><span class="sxs-lookup"><span data-stu-id="f7a9d-140">Now log on to your newly created Windows Server VM using Remote Desktop and the public IP address of the VM.</span></span> <span data-ttu-id="f7a9d-141">以下命令显示上述脚本中创建的公共 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="f7a9d-141">The following command displays the public IP address created in the previous script.</span></span>

```powershell
$publicIp | Select-Object Name,IpAddress
```

```
Name                  IpAddress
----                  ---------
mypublicdns1400512543 xx.xx.xx.xx
```

<span data-ttu-id="f7a9d-142">如果使用的是基于 Windows 的系统，可以在命令行中使用 mstsc 命令来执行此操作：</span><span class="sxs-lookup"><span data-stu-id="f7a9d-142">If you are on a Windows-based system, you can do this from the command line using the mstsc command:</span></span>

```
mstsc /v:xx.xxx.xx.xxx
```

<span data-ttu-id="f7a9d-143">提供创建 VM 时所用的同一用户名/密码组合进行登录。</span><span class="sxs-lookup"><span data-stu-id="f7a9d-143">Supply the same username/password combination you used when creating the VM to log in.</span></span>


## <a name="create-a-linux-virtual-machine"></a><span data-ttu-id="f7a9d-144">创建 Linux 虚拟机</span><span class="sxs-lookup"><span data-stu-id="f7a9d-144">Create a Linux Virtual Machine</span></span>

<span data-ttu-id="f7a9d-145">要创建新的 Linux VM，必须先创建其他所需的资源并将其分配到配置中。</span><span class="sxs-lookup"><span data-stu-id="f7a9d-145">To create a new Linux VM we must first create the other required resources and assign them to a configuration.</span></span> <span data-ttu-id="f7a9d-146">然后，可以使用该配置来创建 VM。</span><span class="sxs-lookup"><span data-stu-id="f7a9d-146">Then we can use that configuration to create the VM.</span></span> <span data-ttu-id="f7a9d-147">此步骤假设已创建前面所示的资源组。</span><span class="sxs-lookup"><span data-stu-id="f7a9d-147">This assumes that you have already created the resource group as previously shown.</span></span> <span data-ttu-id="f7a9d-148">此外，用户配置文件的 .ssh 目录中需具备名为 `id_rsa.pub` 的 SSH 公钥。</span><span class="sxs-lookup"><span data-stu-id="f7a9d-148">Also, you will need to have an SSH public key named `id_rsa.pub` in the .ssh directory of your user profile.</span></span>

### <a name="create-the-required-network-resources"></a><span data-ttu-id="f7a9d-149">创建所需的网络资源</span><span class="sxs-lookup"><span data-stu-id="f7a9d-149">Create the required network resources</span></span>

<span data-ttu-id="f7a9d-150">首先，需要创建一个子网配置，以便在创建虚拟网络过程中使用。</span><span class="sxs-lookup"><span data-stu-id="f7a9d-150">First we need to create a subnet configuration to be used with the virtual network creation process.</span></span> <span data-ttu-id="f7a9d-151">此外，还要创建一个公共 IP 地址，以便能够连接到此 VM。</span><span class="sxs-lookup"><span data-stu-id="f7a9d-151">We also create a public IP address so that we can connect to this VM.</span></span> <span data-ttu-id="f7a9d-152">我们将创建一个网络安全组来保护对公共地址的访问。</span><span class="sxs-lookup"><span data-stu-id="f7a9d-152">We create a network security group to secure access to the public address.</span></span> <span data-ttu-id="f7a9d-153">最后，使用上述所有资源创建虚拟 NIC。</span><span class="sxs-lookup"><span data-stu-id="f7a9d-153">Finally we create the virtual NIC using all of the previous resources.</span></span>

```powershell
# Variables for common values
$resourceGroup = "myResourceGroup"
$location = "westeurope"
$vmName = "myLinuxVM"

# Definer user name and blank password
$securePassword = ConvertTo-SecureString ' ' -AsPlainText -Force
$cred = New-Object System.Management.Automation.PSCredential ("azureuser", $securePassword)

# Create a subnet configuration
$subnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name mySubnet2 -AddressPrefix 192.168.2.0/24

# Create a virtual network
$vnet = New-AzureRmVirtualNetwork -ResourceGroupName $resourceGroup -Location $location `
  -Name MYvNET2 -AddressPrefix 192.168.0.0/16 -Subnet $subnetConfig

# Create a public IP address and specify a DNS name
$publicIp = New-AzureRmPublicIpAddress -ResourceGroupName $resourceGroup -Location $location `
  -Name "mypublicdns$(Get-Random)" -AllocationMethod Static -IdleTimeoutInMinutes 4
$publicIp | Select-Object Name,IpAddress

# Create an inbound network security group rule for port 22
$nsgRuleSSH = New-AzureRmNetworkSecurityRuleConfig -Name myNetworkSecurityGroupRuleSSH  -Protocol Tcp `
  -Direction Inbound -Priority 1000 -SourceAddressPrefix * -SourcePortRange * -DestinationAddressPrefix * `
  -DestinationPortRange 22 -Access Allow

# Create a network security group
$nsg = New-AzureRmNetworkSecurityGroup -ResourceGroupName $resourceGroup -Location $location `
  -Name myNetworkSecurityGroup2 -SecurityRules $nsgRuleSSH

# Create a virtual network card and associate with public IP address and NSG
$nic = New-AzureRmNetworkInterface -Name myNic2 -ResourceGroupName $resourceGroup -Location $location `
  -SubnetId $vnet.Subnets[0].Id -PublicIpAddressId $publicIp.Id -NetworkSecurityGroupId $nsg.Id
```

### <a name="create-the-virtual-machine"></a><span data-ttu-id="f7a9d-154">创建虚拟机</span><span class="sxs-lookup"><span data-stu-id="f7a9d-154">Create the virtual machine</span></span>

<span data-ttu-id="f7a9d-155">准备好所需的资源后，便可以创建 VM。</span><span class="sxs-lookup"><span data-stu-id="f7a9d-155">Now that we have the required resources we can create the VM.</span></span> <span data-ttu-id="f7a9d-156">在此步骤中，我们将创建一个 VM 配置对象，然后使用该配置来创建 VM。</span><span class="sxs-lookup"><span data-stu-id="f7a9d-156">For this step, we create a VM configuration object, then we use the configuration to create the VM.</span></span>

```powershell
# Create a virtual machine configuration
$vmConfig = New-AzureRmVMConfig -VMName $vmName -VMSize Standard_D1 |
  Set-AzureRmVMOperatingSystem -Linux -ComputerName $vmName -Credential $cred -DisablePasswordAuthentication |
  Set-AzureRmVMSourceImage -PublisherName Canonical -Offer UbuntuServer -Skus 14.04.2-LTS -Version latest |
  Add-AzureRmVMNetworkInterface -Id $nic.Id

# Configure SSH Keys
$sshPublicKey = Get-Content "$env:USERPROFILE\.ssh\id_rsa.pub"
Add-AzureRmVMSshPublicKey -VM $vmConfig -KeyData $sshPublicKey -Path "/home/azureuser/.ssh/authorized_keys"

# Create a virtual machine
New-AzureRmVM -ResourceGroupName $resourceGroup -Location $location -VM $vmConfig
```

<span data-ttu-id="f7a9d-157">创建 VM 后，可以使用创建的 VM 的公共 IP 地址通过 SSH 登录到新的 Linux VM：</span><span class="sxs-lookup"><span data-stu-id="f7a9d-157">Now that the VM has been created, you can log on to your new Linux VM using SSH with the public IP address of the VM you created:</span></span>

```bash
ssh xx.xxx.xxx.xxx
```

```
Welcome to Ubuntu 14.04.4 LTS (GNU/Linux 3.19.0-65-generic x86_64)

 * Documentation:  https://help.ubuntu.com/

  System information as of Sun Feb 19 00:32:28 UTC 2017

  System load: 0.31              Memory usage: 3%   Processes:       89
  Usage of /:  39.6% of 1.94GB   Swap usage:   0%   Users logged in: 0

  Graph this data and manage this system at:
    https://landscape.canonical.com/

  Get cloud support with Ubuntu Advantage Cloud Guest:
    http://www.ubuntu.com/business/services/cloud

0 packages can be updated.
0 updates are security updates.



The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

my-login@MyLinuxVM:~$
```

## <a name="creating-other-resources-in-azure"></a><span data-ttu-id="f7a9d-158">在 Azure 中创建其他资源</span><span class="sxs-lookup"><span data-stu-id="f7a9d-158">Creating other resources in Azure</span></span>

<span data-ttu-id="f7a9d-159">前面已经逐步讲解了如何创建资源组、Linux VM 和 Windows Server VM。</span><span class="sxs-lookup"><span data-stu-id="f7a9d-159">We've now walked through how to create a Resource Group, a Linux VM, and a Windows Server VM.</span></span> <span data-ttu-id="f7a9d-160">还可以创建许多其他类型的 Azure 资源。</span><span class="sxs-lookup"><span data-stu-id="f7a9d-160">You can create many other types of Azure resources as well.</span></span>

<span data-ttu-id="f7a9d-161">例如，若要创建稍后可与新建的 VM 相关联的 Azure 网络负载均衡器，可以使用以下 create 命令：</span><span class="sxs-lookup"><span data-stu-id="f7a9d-161">For example, to create an Azure Network Load Balancer that we could then associate with our newly created VMs, we can use the following create command:</span></span>

```powershell
New-AzureRmLoadBalancer -Name MyLoadBalancer -ResourceGroupName myResourceGroup -Location westeurope
```

<span data-ttu-id="f7a9d-162">还可以使用以下命令为基础结构创建新的专用虚拟网络（在 Azure 中通常称为“VNet”）：</span><span class="sxs-lookup"><span data-stu-id="f7a9d-162">We could also create a new private Virtual Network (commonly referred to as a "VNet" within Azure) for our infrastructure using the following command:</span></span>

```powershell
$subnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name mySubnet2 -AddressPrefix 10.0.0.0/16
$vnet = New-AzureRmVirtualNetwork -ResourceGroupName myResourceGroup -Location westeurope `
  -Name MYvNET3 -AddressPrefix 10.0.0.0/16 -Subnet $subnetConfig
```

<span data-ttu-id="f7a9d-163">Azure 和 Azure PowerShell 的强大之处在于，我们不仅可以使用它们来获取基于云的基础结构，而且还可以创建托管的平台服务。</span><span class="sxs-lookup"><span data-stu-id="f7a9d-163">What makes Azure and the Azure PowerShell powerful is that we can use it not just to get cloud-based infrastructure but also to create managed platform services.</span></span> <span data-ttu-id="f7a9d-164">此外，可将托管的平台服务与基础结构结合使用，构建更强大的解决方案。</span><span class="sxs-lookup"><span data-stu-id="f7a9d-164">The managed platform services can also be combined with infrastructure to build even more powerful solutions.</span></span>

<span data-ttu-id="f7a9d-165">例如，可以使用 Azure PowerShell 创建 Azure 应用服务。</span><span class="sxs-lookup"><span data-stu-id="f7a9d-165">For example, you can use the Azure PowerShell to create an Azure AppService.</span></span> <span data-ttu-id="f7a9d-166">Azure 应用服务是一个托管的平台服务，使用它能够十分方便地托管 Web 应用，而无需考虑基础结构。</span><span class="sxs-lookup"><span data-stu-id="f7a9d-166">Azure AppService is a managed platform service that provides a great way to host web apps without having to worry about infrastructure.</span></span> <span data-ttu-id="f7a9d-167">创建 Azure 应用服务后，可以使用以下命令中应用服务中创建两个新的 Azure Web 应用：</span><span class="sxs-lookup"><span data-stu-id="f7a9d-167">After creating the Azure AppService, you can create two new Azure Web Apps within the AppService using the following commands:</span></span>

```powershell
# Create an Azure AppService that we can host any number of web apps within
New-AzureRmAppServicePlan -Name MyAppServicePlan -Tier Basic -NumberofWorkers 2 -WorkerSize Small -ResourceGroupName myResourceGroup -Location westeurope

# Create Two Web Apps within the AppService (note: name param must be a unique DNS entry)
New-AzureRmWebApp -Name MyWebApp43432 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
New-AzureRmWebApp -Name MyWebApp43433 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
```

## <a name="listing-deployed-resources"></a><span data-ttu-id="f7a9d-168">列出已部署的资源</span><span class="sxs-lookup"><span data-stu-id="f7a9d-168">Listing deployed resources</span></span>

<span data-ttu-id="f7a9d-169">可以使用 `Get-AzureRmResource` cmdlet 列出 Azure 中运行的资源。</span><span class="sxs-lookup"><span data-stu-id="f7a9d-169">You can use the `Get-AzureRmResource` cmdlet to list the resources running in Azure.</span></span> <span data-ttu-id="f7a9d-170">以下示例显示我们刚刚在新资源组中创建的资源。</span><span class="sxs-lookup"><span data-stu-id="f7a9d-170">The following example shows the resources we just created in the new resource group.</span></span>

```powershell
Get-AzureRmResource |
  Where-Object ResourceGroupName -eq myResourceGroup |
    Select-Object Name,Location,ResourceType
```

```
Name                                                  Location   ResourceType
----                                                  --------   ------------
myLinuxVM_OsDisk_1_36ca038791f642ba91270879088c249a   westeurope Microsoft.Compute/disks
myWindowsVM_OsDisk_1_f627e6e2bb454c72897d72e9632adf9a westeurope Microsoft.Compute/disks
myLinuxVM                                             westeurope Microsoft.Compute/virtualMachines
myWindowsVM                                           westeurope Microsoft.Compute/virtualMachines
myWindowsVM/BGInfo                                    westeurope Microsoft.Compute/virtualMachines/extensions
myNic1                                                westeurope Microsoft.Network/networkInterfaces
myNic2                                                westeurope Microsoft.Network/networkInterfaces
myNetworkSecurityGroup1                               westeurope Microsoft.Network/networkSecurityGroups
myNetworkSecurityGroup2                               westeurope Microsoft.Network/networkSecurityGroups
mypublicdns245369171                                  westeurope Microsoft.Network/publicIPAddresses
mypublicdns779537141                                  westeurope Microsoft.Network/publicIPAddresses
MYvNET1                                               westeurope Microsoft.Network/virtualNetworks
MYvNET2                                               westeurope Microsoft.Network/virtualNetworks
micromyresomywi032907510                              westeurope Microsoft.Storage/storageAccounts
```

## <a name="deleting-resources"></a><span data-ttu-id="f7a9d-171">删除资源</span><span class="sxs-lookup"><span data-stu-id="f7a9d-171">Deleting resources</span></span>

<span data-ttu-id="f7a9d-172">若要清理 Azure 帐户，可以删除我们在本示例中创建的资源。</span><span class="sxs-lookup"><span data-stu-id="f7a9d-172">To clean up your Azure account, you want to remove the resources we created in this example.</span></span> <span data-ttu-id="f7a9d-173">可以使用 `Remove-AzureRm*` cmdlet 删除不再需要的资源。</span><span class="sxs-lookup"><span data-stu-id="f7a9d-173">You can use the `Remove-AzureRm*` cmdlets to delete the resources you no longer need.</span></span> <span data-ttu-id="f7a9d-174">若要删除我们创建的 Windows VM，请使用以下命令：</span><span class="sxs-lookup"><span data-stu-id="f7a9d-174">To remove the Windows VM we created, using the following command:</span></span>

```powershell
Remove-AzureRmVM -Name myWindowsVM -ResourceGroupName myResourceGroup
```

<span data-ttu-id="f7a9d-175">系统会提示确认删除该资源。</span><span class="sxs-lookup"><span data-stu-id="f7a9d-175">You will be prompted to confirm that you want to remove the resource.</span></span>

```
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="f7a9d-176">还可以一次性删除多个资源。</span><span class="sxs-lookup"><span data-stu-id="f7a9d-176">You can also use the delete many resources at one time.</span></span> <span data-ttu-id="f7a9d-177">例如，以下命令将删除本入门教程中所有示例使用的“MyResourceGroup”资源组中的所有资源。</span><span class="sxs-lookup"><span data-stu-id="f7a9d-177">For example, the following command deletes all the resource group "MyResourceGroup" that we've used for all the samples in this Get Started tutorial.</span></span> <span data-ttu-id="f7a9d-178">这会删除该资源组及其包含的所有资源。</span><span class="sxs-lookup"><span data-stu-id="f7a9d-178">This removes the resource group and all of the resources in it.</span></span>

```powershell
Remove-AzureRmResourceGroup -Name myResourceGroup
```

```
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="f7a9d-179">此过程需要几分钟才能完成。</span><span class="sxs-lookup"><span data-stu-id="f7a9d-179">This can take several minutes to complete.</span></span>

## <a name="get-samples"></a><span data-ttu-id="f7a9d-180">获取示例</span><span class="sxs-lookup"><span data-stu-id="f7a9d-180">Get samples</span></span>

<span data-ttu-id="f7a9d-181">若要详细了解 Azure PowerShell 的用法，请查看适用于 [Linux VM](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json)、[Windows VM](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json)、[Web 应用](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json)和 [SQL 数据库](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json)的最常用脚本。</span><span class="sxs-lookup"><span data-stu-id="f7a9d-181">To learn more about ways to use the Azure PowerShell, check out our most common scripts for [Linux VMs](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Windows VMs](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Web Apps](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), and [SQL Databases](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json).</span></span>

## <a name="next-steps"></a><span data-ttu-id="f7a9d-182">后续步骤</span><span class="sxs-lookup"><span data-stu-id="f7a9d-182">Next steps</span></span>

* [<span data-ttu-id="f7a9d-183">使用 Azure PowerShell 登录</span><span class="sxs-lookup"><span data-stu-id="f7a9d-183">Login with Azure PowerShell</span></span>](authenticate-azureps.md)
* [<span data-ttu-id="f7a9d-184">使用 Azure PowerShell 管理 Azure 订阅</span><span class="sxs-lookup"><span data-stu-id="f7a9d-184">Manage Azure subscriptions with Azure PowerShell</span></span>](manage-subscriptions-azureps.md)
* [<span data-ttu-id="f7a9d-185">使用 Azure PowerShell 在 Azure 中创建服务主体</span><span class="sxs-lookup"><span data-stu-id="f7a9d-185">Create service principals in Azure using Azure PowerShell</span></span>](create-azure-service-principal-azureps.md)
* <span data-ttu-id="f7a9d-186">在发行说明中阅读有关从旧版迁移的信息：[https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes](https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes)。</span><span class="sxs-lookup"><span data-stu-id="f7a9d-186">Read the Release notes about migrating from an older release: [https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes](https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes).</span></span>
* <span data-ttu-id="f7a9d-187">从社区获得帮助：</span><span class="sxs-lookup"><span data-stu-id="f7a9d-187">Get help from the community:</span></span>
  + [<span data-ttu-id="f7a9d-188">MSDN 上的 Azure 论坛</span><span class="sxs-lookup"><span data-stu-id="f7a9d-188">Azure forum on MSDN</span></span>](http://go.microsoft.com/fwlink/p/?LinkId=320212)
  + [<span data-ttu-id="f7a9d-189">stackoverflow</span><span class="sxs-lookup"><span data-stu-id="f7a9d-189">stackoverflow</span></span>](http://go.microsoft.com/fwlink/?LinkId=320213)
