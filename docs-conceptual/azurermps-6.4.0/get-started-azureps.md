---
title: Azure PowerShell 入门
description: ''
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: get-started-article
ms.date: 11/15/2017
ms.openlocfilehash: 102dfb7476a4964af541a29416b10bc880c53adb
ms.sourcegitcommit: de0e60800df1add9f3400166faacca202ef567d9
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/03/2018
ms.locfileid: "37406156"
---
# <a name="get-started-with-azure-powershell"></a><span data-ttu-id="04a03-102">Azure PowerShell 入门</span><span class="sxs-lookup"><span data-stu-id="04a03-102">Get started with Azure PowerShell</span></span>

<span data-ttu-id="04a03-103">Azure PowerShell 用于从命令行管理 Azure 资源，以及生成可以针对 Azure 资源管理器运行的自动化脚本。</span><span class="sxs-lookup"><span data-stu-id="04a03-103">Azure PowerShell is designed for managing and administering Azure resources from the command line, and for building automation scripts that work against the Azure Resource Manager.</span></span> <span data-ttu-id="04a03-104">可以通过 [Azure Cloud Shell](/azure/cloud-shell/overview) 在浏览器中使用它，也可以将它安装在本地计算机上。</span><span class="sxs-lookup"><span data-stu-id="04a03-104">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview) or you install it on your local machine.</span></span> <span data-ttu-id="04a03-105">本文将帮助你开始使用 Azure PowerShell，并讲解与其相关的核心概念。</span><span class="sxs-lookup"><span data-stu-id="04a03-105">This article helps get you started with Azure PowerShell and teaches the core concepts behind it.</span></span>

## <a name="install-azure-powershell"></a><span data-ttu-id="04a03-106">安装 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="04a03-106">Install Azure PowerShell</span></span>

<span data-ttu-id="04a03-107">首先，请确保已安装最新版本的 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="04a03-107">The first step is to make sure you have the latest version of the Azure PowerShell installed.</span></span> <span data-ttu-id="04a03-108">有关最新版本的信息，请参阅[发行说明](./release-notes-azureps.md)。</span><span class="sxs-lookup"><span data-stu-id="04a03-108">For information about the latest release, see the [release notes](./release-notes-azureps.md).</span></span>

1. <span data-ttu-id="04a03-109">[安装 Azure PowerShell](install-azurerm-ps.md)。</span><span class="sxs-lookup"><span data-stu-id="04a03-109">[Install Azure PowerShell](install-azurerm-ps.md).</span></span>

2. <span data-ttu-id="04a03-110">若要验证安装是否成功，请从命令行运行 `Get-Module AzureRM -ListAvailable`。</span><span class="sxs-lookup"><span data-stu-id="04a03-110">To verify the installation was successful, run `Get-Module AzureRM -ListAvailable` from your command line.</span></span>

## <a name="azure-cloud-shell"></a><span data-ttu-id="04a03-111">Azure Cloud Shell</span><span class="sxs-lookup"><span data-stu-id="04a03-111">Azure Cloud Shell</span></span> 

<span data-ttu-id="04a03-112">最简单的入门方法是[启动 Cloud Shell](/azure/cloud-shell/quickstart)。</span><span class="sxs-lookup"><span data-stu-id="04a03-112">The simplest way to get started is to [launch Cloud Shell](/azure/cloud-shell/quickstart).</span></span>

1. <span data-ttu-id="04a03-113">从 Azure 门户的顶部导航栏启动 Cloud Shell。</span><span class="sxs-lookup"><span data-stu-id="04a03-113">Launch Cloud Shell from the top navigation of the Azure portal.</span></span>

   ![Shell 图标](~/media/get-started-azureps/shell-icon.png)

2. <span data-ttu-id="04a03-115">选择要使用的订阅并创建存储帐户。</span><span class="sxs-lookup"><span data-stu-id="04a03-115">Choose the subscription you want to use and create a storage account.</span></span>

   ![创建存储帐户](~/media/get-started-azureps/storage-prompt.png)

<span data-ttu-id="04a03-117">创建存储后，Cloud Shell 会在浏览器中打开 PowerShell 会话。</span><span class="sxs-lookup"><span data-stu-id="04a03-117">Once your storage has been created, the Cloud Shell will open a PowerShell session in the browser.</span></span>

![适用于 PowerShell 的 Cloud Shell](~/media/get-started-azureps/cloud-powershell.png)

<span data-ttu-id="04a03-119">也可以安装 Azure PowerShell 并在 PowerShell 会话本地使用它。</span><span class="sxs-lookup"><span data-stu-id="04a03-119">You can also install Azure PowerShell and use it locally in a PowerShell session.</span></span>

## <a name="sign-in-to-azure"></a><span data-ttu-id="04a03-120">登录 Azure</span><span class="sxs-lookup"><span data-stu-id="04a03-120">Sign in to Azure</span></span>

<span data-ttu-id="04a03-121">以交互方式登录：</span><span class="sxs-lookup"><span data-stu-id="04a03-121">Sign on interactively:</span></span>

1. <span data-ttu-id="04a03-122">键入 `Connect-AzureRmAccount`。</span><span class="sxs-lookup"><span data-stu-id="04a03-122">Type `Connect-AzureRmAccount`.</span></span> <span data-ttu-id="04a03-123">此时会出现一个对话框，要求输入 Azure 凭据。</span><span class="sxs-lookup"><span data-stu-id="04a03-123">You will get dialog box asking for your Azure credentials.</span></span> <span data-ttu-id="04a03-124">使用 '-Environment' 选项可登录“Azure 中国”或“Azure 德国”。</span><span class="sxs-lookup"><span data-stu-id="04a03-124">Option '-Environment' can let you login in Azure China or Azure Germany.</span></span>

   <span data-ttu-id="04a03-125">例如 Connect-AzureRmAccount -Environment AzureChinaCloud</span><span class="sxs-lookup"><span data-stu-id="04a03-125">e.g. Connect-AzureRmAccount -Environment AzureChinaCloud</span></span>

2. <span data-ttu-id="04a03-126">键入与帐户关联的电子邮件地址和密码。</span><span class="sxs-lookup"><span data-stu-id="04a03-126">Type the email address and password associated with your account.</span></span> <span data-ttu-id="04a03-127">Azure 将对凭据信息进行身份验证和保存，然后关闭该窗口。</span><span class="sxs-lookup"><span data-stu-id="04a03-127">Azure authenticates and saves the credential information, and then closes the window.</span></span>

<span data-ttu-id="04a03-128">登录到 Azure 帐户后，可以使用 Azure PowerShell cmdlet 访问和管理订阅中的资源。</span><span class="sxs-lookup"><span data-stu-id="04a03-128">Once you have signed in to an Azure account, you can use the Azure PowerShell cmdlets to access and manage the resources in your subscription.</span></span>

## <a name="create-a-windows-virtual-machine-using-simple-defaults"></a><span data-ttu-id="04a03-129">使用简单的默认值创建 Windows 虚拟机</span><span class="sxs-lookup"><span data-stu-id="04a03-129">Create a Windows virtual machine using simple defaults</span></span>

<span data-ttu-id="04a03-130">`New-AzureRmVM` cmdlet 提供了一种简化的语法，使得创建新虚拟机更加轻松。</span><span class="sxs-lookup"><span data-stu-id="04a03-130">The `New-AzureRmVM` cmdlet provides a simplified syntax making it easy to create a new virtual machine.</span></span> <span data-ttu-id="04a03-131">必须提供的只有两个参数值：VM 的名称和该 VM 上本地管理员帐户的一组凭据。</span><span class="sxs-lookup"><span data-stu-id="04a03-131">There are only two parameter values you must provide: the name of the VM and a set of credentials for the local administrator account on the VM.</span></span>

<span data-ttu-id="04a03-132">首先，创建凭据对象。</span><span class="sxs-lookup"><span data-stu-id="04a03-132">First, create the credential object.</span></span>

```azurepowershell-interactive
$cred = Get-Credential -Message "Enter a username and password for the virtual machine."
```

```output
Windows PowerShell credential request.
Enter a username and password for the virtual machine.
User: localAdmin
Password for user localAdmin: *********
```
<span data-ttu-id="04a03-133">然后，创建 VM。</span><span class="sxs-lookup"><span data-stu-id="04a03-133">Next, create the VM.</span></span>

```azurepowershell-interactive
New-AzureRmVM -Name SampleVM -Credential $cred
```

```output
ResourceGroupName        : SampleVM
Id                       : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/SampleVM/providers/Microsoft.Compute/virtualMachines/SampleVM
VmId                     : 43f6275d-ce50-49c8-a831-5d5974006e63
Name                     : SampleVM
Type                     : Microsoft.Compute/virtualMachines
Location                 : eastus
Tags                     : {}
HardwareProfile          : {VmSize}
NetworkProfile           : {NetworkInterfaces}
OSProfile                : {ComputerName, AdminUsername, WindowsConfiguration, Secrets}
ProvisioningState        : Succeeded
StorageProfile           : {ImageReference, OsDisk, DataDisks}
FullyQualifiedDomainName : samplevm-2c0867.eastus.cloudapp.azure.com
```

<span data-ttu-id="04a03-134">这非常简单。</span><span class="sxs-lookup"><span data-stu-id="04a03-134">That was easy.</span></span> <span data-ttu-id="04a03-135">但你可能想知道还创建了其他哪些对象以及 VM 是如何配置的。</span><span class="sxs-lookup"><span data-stu-id="04a03-135">But, you may wonder what else is created and how is the VM configured.</span></span> <span data-ttu-id="04a03-136">让我们先看一下资源组。</span><span class="sxs-lookup"><span data-stu-id="04a03-136">First, let's look at our resource groups.</span></span>

```azurepowershell-interactive
Get-AzureRmResourceGroup | Select-Object ResourceGroupName,Location
```

```output
ResourceGroupName          Location
-----------------          --------
cloud-shell-storage-westus westus
SampleVM                   eastus
```

<span data-ttu-id="04a03-137">**cloud-shell-storage-westus** 资源组是在你首次使用 Cloud Shell 时创建的。</span><span class="sxs-lookup"><span data-stu-id="04a03-137">The **cloud-shell-storage-westus** resource group is created the first time you use the Cloud Shell.</span></span> <span data-ttu-id="04a03-138">**SampleVM** 资源组由 `New-AzureRmVM` cmdlet 创建。</span><span class="sxs-lookup"><span data-stu-id="04a03-138">The **SampleVM** resource group was created by the `New-AzureRmVM` cmdlet.</span></span>

<span data-ttu-id="04a03-139">现在，这一新资源组中还创建了其他哪些资源？</span><span class="sxs-lookup"><span data-stu-id="04a03-139">Now, what other resources were created in this new resource group?</span></span>

```azurepowershell-interactive
Get-AzureRmResource |
  Where ResourceGroupName -eq SampleVM |
    Select-Object ResourceGroupName,Location,ResourceType,Name
```

```output
ResourceGroupName          Location ResourceType                            Name
-----------------          -------- ------------                            ----
SAMPLEVM                   eastus   Microsoft.Compute/disks                 SampleVM_OsDisk_1_9b286c54b168457fa1f8c47...
SampleVM                   eastus   Microsoft.Compute/virtualMachines       SampleVM
SampleVM                   eastus   Microsoft.Network/networkInterfaces     SampleVM
SampleVM                   eastus   Microsoft.Network/networkSecurityGroups SampleVM
SampleVM                   eastus   Microsoft.Network/publicIPAddresses     SampleVM
SampleVM                   eastus   Microsoft.Network/virtualNetworks       SampleVM
```

<span data-ttu-id="04a03-140">让我们再了解一些有关该 VM 的详细信息。</span><span class="sxs-lookup"><span data-stu-id="04a03-140">Let's get some more details about the VM.</span></span> <span data-ttu-id="04a03-141">此示例演示如何检索有关用于创建 VM 的 OS 映像的信息。</span><span class="sxs-lookup"><span data-stu-id="04a03-141">This examples shows how to retrieve information about the OS Image used to create the VM.</span></span>

```azurepowershell-interactive
Get-AzureRmVM -Name SampleVM -ResourceGroupName SampleVM |
  Select-Object -ExpandProperty StorageProfile |
    Select-Object -ExpandProperty ImageReference
```

```output
Publisher : MicrosoftWindowsServer
Offer     : WindowsServer
Sku       : 2016-Datacenter
Version   : latest
Id        :
```

## <a name="create-a-fully-configured-linux-virtual-machine"></a><span data-ttu-id="04a03-142">创建完全配置的 Linux 虚拟机</span><span class="sxs-lookup"><span data-stu-id="04a03-142">Create a fully configured Linux Virtual Machine</span></span>

<span data-ttu-id="04a03-143">前面的示例使用了简化的语法和默认参数值来创建 Windows 虚拟机。</span><span class="sxs-lookup"><span data-stu-id="04a03-143">The previous example used the simplified syntax and default parameter values to create a Windows virtual machine.</span></span> <span data-ttu-id="04a03-144">在此示例中，我们为虚拟机的所有选项提供值。</span><span class="sxs-lookup"><span data-stu-id="04a03-144">In this example, we provide values for all options of the virtual machine.</span></span>

### <a name="create-a-resource-group"></a><span data-ttu-id="04a03-145">创建资源组</span><span class="sxs-lookup"><span data-stu-id="04a03-145">Create a resource group</span></span>

<span data-ttu-id="04a03-146">对于此示例，我们想要创建资源组。</span><span class="sxs-lookup"><span data-stu-id="04a03-146">For this example we want to create a Resource Group.</span></span> <span data-ttu-id="04a03-147">使用 Azure 中的资源组可以同时管理希望以逻辑方式分组的多个资源。</span><span class="sxs-lookup"><span data-stu-id="04a03-147">Resource Groups in Azure provide a way to manage multiple resources that you want to logically group together.</span></span> <span data-ttu-id="04a03-148">例如，可为应用程序或项目创建资源组，并在其中添加虚拟机、数据库和 CDN 服务。</span><span class="sxs-lookup"><span data-stu-id="04a03-148">For example, you might create a Resource Group for an application or project and add a virtual machine, a database and a CDN service within it.</span></span>

<span data-ttu-id="04a03-149">让我们在 Azure 的西欧区域创建一个名为“MyResourceGroup”的资源组。</span><span class="sxs-lookup"><span data-stu-id="04a03-149">Let's create a resource group named "MyResourceGroup" in the westeurope region of Azure.</span></span> <span data-ttu-id="04a03-150">为此，请键入以下命令：</span><span class="sxs-lookup"><span data-stu-id="04a03-150">To do so type the following command:</span></span>

```azurepowershell-interactive
New-AzureRmResourceGroup -Name 'myResourceGroup' -Location 'westeurope'
```

```output
ResourceGroupName : myResourceGroup
Location          : westeurope
ProvisioningState : Succeeded
Tags              :
ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myResourceGroup
```

<span data-ttu-id="04a03-151">这一新资源组将用于包含我们创建的新 VM 所需的所有资源。</span><span class="sxs-lookup"><span data-stu-id="04a03-151">This new resource group will be used to contain all of the resources needed for the new VM we create.</span></span> <span data-ttu-id="04a03-152">要创建新的 Linux VM，必须先创建其他所需的资源并将其分配到配置中。</span><span class="sxs-lookup"><span data-stu-id="04a03-152">To create a new Linux VM we must first create the other required resources and assign them to a configuration.</span></span> <span data-ttu-id="04a03-153">然后，可以使用该配置来创建 VM。</span><span class="sxs-lookup"><span data-stu-id="04a03-153">Then we can use that configuration to create the VM.</span></span> <span data-ttu-id="04a03-154">此外，用户配置文件的 .ssh 目录中需具备名为 `id_rsa.pub` 的 SSH 公钥。</span><span class="sxs-lookup"><span data-stu-id="04a03-154">Also, you will need to have an SSH public key named `id_rsa.pub` in the .ssh directory of your user profile.</span></span>

#### <a name="create-the-required-network-resources"></a><span data-ttu-id="04a03-155">创建所需的网络资源</span><span class="sxs-lookup"><span data-stu-id="04a03-155">Create the required network resources</span></span>

<span data-ttu-id="04a03-156">首先，需要创建一个子网配置，以便在创建虚拟网络过程中使用。</span><span class="sxs-lookup"><span data-stu-id="04a03-156">First we need to create a subnet configuration to be used with the virtual network creation process.</span></span> <span data-ttu-id="04a03-157">此外，还要创建一个公共 IP 地址，以便能够连接到此 VM。</span><span class="sxs-lookup"><span data-stu-id="04a03-157">We also create a public IP address so that we can connect to this VM.</span></span> <span data-ttu-id="04a03-158">我们将创建一个网络安全组来保护对公共地址的访问。</span><span class="sxs-lookup"><span data-stu-id="04a03-158">We create a network security group to secure access to the public address.</span></span> <span data-ttu-id="04a03-159">最后，使用上述所有资源创建虚拟 NIC。</span><span class="sxs-lookup"><span data-stu-id="04a03-159">Finally we create the virtual NIC using all of the previous resources.</span></span>

```azurepowershell-interactive
# Variables for common values
$resourceGroup = "myResourceGroup"
$location = "westeurope"
$vmName = "myLinuxVM"

# Definer user name and blank password
$securePassword = ConvertTo-SecureString 'azurepassword' -AsPlainText -Force
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

### <a name="create-the-vm-configuration"></a><span data-ttu-id="04a03-160">创建 VM 配置</span><span class="sxs-lookup"><span data-stu-id="04a03-160">Create the VM configuration</span></span>

<span data-ttu-id="04a03-161">有了所需资源以后，就可以创建 VM 配置对象了。</span><span class="sxs-lookup"><span data-stu-id="04a03-161">Now that we have the required resources we can create the VM configuration object.</span></span>

```azurepowershell-interactive
# Create a virtual machine configuration
$vmConfig = New-AzureRmVMConfig -VMName $vmName -VMSize Standard_D1 |
  Set-AzureRmVMOperatingSystem -Linux -ComputerName $vmName -Credential $cred -DisablePasswordAuthentication |
  Set-AzureRmVMSourceImage -PublisherName Canonical -Offer UbuntuServer -Skus 14.04.2-LTS -Version latest |
  Add-AzureRmVMNetworkInterface -Id $nic.Id

# Configure SSH Keys
$sshPublicKey = Get-Content -Raw "$env:USERPROFILE\.ssh\id_rsa.pub"
Add-AzureRmVMSshPublicKey -VM $vmConfig -KeyData $sshPublicKey -Path "/home/azureuser/.ssh/authorized_keys"
```

### <a name="create-the-virtual-machine"></a><span data-ttu-id="04a03-162">创建虚拟机</span><span class="sxs-lookup"><span data-stu-id="04a03-162">Create the virtual machine</span></span>

<span data-ttu-id="04a03-163">现在可以使用 VM 配置对象创建 VM。</span><span class="sxs-lookup"><span data-stu-id="04a03-163">Now we can create the VM using the VM configuration object.</span></span>

```azurepowershell-interactive
New-AzureRmVM -ResourceGroupName $resourceGroup -Location $location -VM $vmConfig
```

<span data-ttu-id="04a03-164">创建 VM 后，可以使用创建的 VM 的公共 IP 地址通过 SSH 登录到新的 Linux VM：</span><span class="sxs-lookup"><span data-stu-id="04a03-164">Now that the VM has been created, you can log on to your new Linux VM using SSH with the public IP address of the VM you created:</span></span>

```bash
ssh xx.xxx.xxx.xxx
```

```output
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

my-login@MyLinuxVM:../../..$
```

## <a name="creating-other-resources-in-azure"></a><span data-ttu-id="04a03-165">在 Azure 中创建其他资源</span><span class="sxs-lookup"><span data-stu-id="04a03-165">Creating other resources in Azure</span></span>

<span data-ttu-id="04a03-166">前面已经逐步讲解了如何创建资源组、Linux VM 和 Windows Server VM。</span><span class="sxs-lookup"><span data-stu-id="04a03-166">We've now walked through how to create a Resource Group, a Linux VM, and a Windows Server VM.</span></span> <span data-ttu-id="04a03-167">还可以创建许多其他类型的 Azure 资源。</span><span class="sxs-lookup"><span data-stu-id="04a03-167">You can create many other types of Azure resources as well.</span></span>

<span data-ttu-id="04a03-168">例如，若要创建稍后可与新建的 VM 相关联的 Azure 网络负载均衡器，可以使用以下 create 命令：</span><span class="sxs-lookup"><span data-stu-id="04a03-168">For example, to create an Azure Network Load Balancer that we could then associate with our newly created VMs, we can use the following create command:</span></span>

```azurepowershell-interactive
New-AzureRmLoadBalancer -Name MyLoadBalancer -ResourceGroupName myResourceGroup -Location westeurope
```

<span data-ttu-id="04a03-169">还可以使用以下命令为基础结构创建新的专用虚拟网络（在 Azure 中通常称为“VNet”）：</span><span class="sxs-lookup"><span data-stu-id="04a03-169">We could also create a new private Virtual Network (commonly referred to as a "VNet" within Azure) for our infrastructure using the following command:</span></span>

```azurepowershell-interactive
$subnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name mySubnet2 -AddressPrefix 10.0.0.0/16
$vnet = New-AzureRmVirtualNetwork -ResourceGroupName myResourceGroup -Location westeurope `
  -Name MYvNET3 -AddressPrefix 10.0.0.0/16 -Subnet $subnetConfig
```

<span data-ttu-id="04a03-170">Azure 和 Azure PowerShell 的强大之处在于，我们不仅可以使用它们来获取基于云的基础结构，而且还可以创建托管的平台服务。</span><span class="sxs-lookup"><span data-stu-id="04a03-170">What makes Azure and the Azure PowerShell powerful is that we can use it not just to get cloud-based infrastructure but also to create managed platform services.</span></span> <span data-ttu-id="04a03-171">此外，可将托管的平台服务与基础结构结合使用，构建更强大的解决方案。</span><span class="sxs-lookup"><span data-stu-id="04a03-171">The managed platform services can also be combined with infrastructure to build even more powerful solutions.</span></span>

<span data-ttu-id="04a03-172">例如，可以使用 Azure PowerShell 创建 Azure 应用服务。</span><span class="sxs-lookup"><span data-stu-id="04a03-172">For example, you can use the Azure PowerShell to create an Azure AppService.</span></span> <span data-ttu-id="04a03-173">Azure 应用服务是一个托管的平台服务，使用它能够十分方便地托管 Web 应用，而无需考虑基础结构。</span><span class="sxs-lookup"><span data-stu-id="04a03-173">Azure AppService is a managed platform service that provides a great way to host web apps without having to worry about infrastructure.</span></span> <span data-ttu-id="04a03-174">创建 Azure 应用服务后，可以使用以下命令中应用服务中创建两个新的 Azure Web 应用：</span><span class="sxs-lookup"><span data-stu-id="04a03-174">After creating the Azure AppService, you can create two new Azure Web Apps within the AppService using the following commands:</span></span>

```azurepowershell-interactive
# Create an Azure AppService that we can host any number of web apps within
New-AzureRmAppServicePlan -Name MyAppServicePlan -Tier Basic -NumberofWorkers 2 -WorkerSize Small -ResourceGroupName myResourceGroup -Location westeurope

# Create Two Web Apps within the AppService (note: name param must be a unique DNS entry)
New-AzureRmWebApp -Name MyWebApp43432 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
New-AzureRmWebApp -Name MyWebApp43433 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
```

## <a name="listing-deployed-resources"></a><span data-ttu-id="04a03-175">列出已部署的资源</span><span class="sxs-lookup"><span data-stu-id="04a03-175">Listing deployed resources</span></span>

<span data-ttu-id="04a03-176">可以使用 `Get-AzureRmResource` cmdlet 列出 Azure 中运行的资源。</span><span class="sxs-lookup"><span data-stu-id="04a03-176">You can use the `Get-AzureRmResource` cmdlet to list the resources running in Azure.</span></span> <span data-ttu-id="04a03-177">以下示例显示我们刚刚在新资源组中创建的资源。</span><span class="sxs-lookup"><span data-stu-id="04a03-177">The following example shows the resources we just created in the new resource group.</span></span>

```azurepowershell-interactive
Get-AzureRmResource |
  Where-Object ResourceGroupName -eq myResourceGroup |
    Select-Object Name,Location,ResourceType
```

```output
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

## <a name="deleting-resources"></a><span data-ttu-id="04a03-178">删除资源</span><span class="sxs-lookup"><span data-stu-id="04a03-178">Deleting resources</span></span>

<span data-ttu-id="04a03-179">若要清理 Azure 帐户，可以删除我们在本示例中创建的资源。</span><span class="sxs-lookup"><span data-stu-id="04a03-179">To clean up your Azure account, you want to remove the resources we created in this example.</span></span> <span data-ttu-id="04a03-180">可以使用 `Remove-AzureRm*` cmdlet 删除不再需要的资源。</span><span class="sxs-lookup"><span data-stu-id="04a03-180">You can use the `Remove-AzureRm*` cmdlets to delete the resources you no longer need.</span></span> <span data-ttu-id="04a03-181">若要删除我们创建的 Windows VM，请使用以下命令：</span><span class="sxs-lookup"><span data-stu-id="04a03-181">To remove the Windows VM we created, using the following command:</span></span>

```azurepowershell-interactive
Remove-AzureRmVM -Name myWindowsVM -ResourceGroupName myResourceGroup
```

<span data-ttu-id="04a03-182">系统会提示确认删除该资源。</span><span class="sxs-lookup"><span data-stu-id="04a03-182">You will be prompted to confirm that you want to remove the resource.</span></span>

```output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="04a03-183">还可以一次性删除多个资源。</span><span class="sxs-lookup"><span data-stu-id="04a03-183">You can also use the delete many resources at one time.</span></span> <span data-ttu-id="04a03-184">例如，以下命令将删除本入门教程中所有示例使用的“MyResourceGroup”资源组中的所有资源。</span><span class="sxs-lookup"><span data-stu-id="04a03-184">For example, the following command deletes all the resource group "MyResourceGroup" that we've used for all the samples in this Get Started tutorial.</span></span> <span data-ttu-id="04a03-185">这会删除该资源组及其包含的所有资源。</span><span class="sxs-lookup"><span data-stu-id="04a03-185">This removes the resource group and all of the resources in it.</span></span>

```azurepowershell-interactive
Remove-AzureRmResourceGroup -Name myResourceGroup
```

```output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="04a03-186">此过程需要几分钟才能完成。</span><span class="sxs-lookup"><span data-stu-id="04a03-186">This can take several minutes to complete.</span></span>

## <a name="get-samples"></a><span data-ttu-id="04a03-187">获取示例</span><span class="sxs-lookup"><span data-stu-id="04a03-187">Get samples</span></span>

<span data-ttu-id="04a03-188">若要详细了解 Azure PowerShell 的用法，请查看适用于 [Linux VM](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json)、[Windows VM](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json)、[Web 应用](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json)和 [SQL 数据库](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json)的最常用脚本。</span><span class="sxs-lookup"><span data-stu-id="04a03-188">To learn more about ways to use the Azure PowerShell, check out our most common scripts for [Linux VMs](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Windows VMs](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Web Apps](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), and [SQL Databases](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json).</span></span>

## <a name="next-steps"></a><span data-ttu-id="04a03-189">后续步骤</span><span class="sxs-lookup"><span data-stu-id="04a03-189">Next steps</span></span>

* [<span data-ttu-id="04a03-190">使用 Azure PowerShell 登录</span><span class="sxs-lookup"><span data-stu-id="04a03-190">Login with Azure PowerShell</span></span>](authenticate-azureps.md)
* [<span data-ttu-id="04a03-191">使用 Azure PowerShell 管理 Azure 订阅</span><span class="sxs-lookup"><span data-stu-id="04a03-191">Manage Azure subscriptions with Azure PowerShell</span></span>](manage-subscriptions-azureps.md)
* [<span data-ttu-id="04a03-192">使用 Azure PowerShell 在 Azure 中创建服务主体</span><span class="sxs-lookup"><span data-stu-id="04a03-192">Create service principals in Azure using Azure PowerShell</span></span>](create-azure-service-principal-azureps.md)
* <span data-ttu-id="04a03-193">阅读有关从较旧版本迁移的发行说明：[https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes](https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes)。</span><span class="sxs-lookup"><span data-stu-id="04a03-193">Read the Release notes about migrating from an older release: [https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes](https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes).</span></span>
* <span data-ttu-id="04a03-194">从社区获得帮助：</span><span class="sxs-lookup"><span data-stu-id="04a03-194">Get help from the community:</span></span>
  * [<span data-ttu-id="04a03-195">MSDN 上的 Azure 论坛</span><span class="sxs-lookup"><span data-stu-id="04a03-195">Azure forum on MSDN</span></span>](http://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [<span data-ttu-id="04a03-196">stackoverflow</span><span class="sxs-lookup"><span data-stu-id="04a03-196">stackoverflow</span></span>](http://go.microsoft.com/fwlink/?LinkId=320213)
