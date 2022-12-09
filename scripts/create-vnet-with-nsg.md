# Create an Azure Virtual Network with a Subnet including NSG

By default, the ALZ Accelerator assigns an Azure Policy which denies the creation of a subnet without a Network Security Group. This is a highly-recommended best practice which should consistently implemented and enforced.

However this introduces a minor challenge. At time of writing this document (December 2022), Azure Policy will not allow you to create a new Azure Virtual Network via the Azure Portal since there is no option to associate a Network Security Group to a subnet when creating a new Azure Virtual Network.

The solution to this minor challenge is a fairly easy one. Don't use the azure Portal, use code. Here's an example based on PowerShell.



```powershell
# Declare your variables
$location = "westeurope"
$rgname = "myrg"
$nsgname = "mynsg"
$vnetname  = "myvnet"
$subnetname = "mysubnet"
```



```powershell
# Create Azure Resource Group
New-AzResourceGroup -Name $rgname -Location $location
```

```powershell
# Create a Network Security Group
$nsg = New-AzNetworkSecurityGroup -ResourceGroupName $rgname -Location $location -Name $nsgname
```

```powershell
# Create Azure Virtual Network
$subnet = New-AzVirtualNetworkSubnetConfig -Name $subnetname -AddressPrefix "192.168.9.0/24" -NetworkSecurityGroup $nsg
$virtualNetwork = New-AzVirtualNetwork -Name $vnetname -ResourceGroupName $rgname -Location $location -AddressPrefix "192.168.8.0/22" -Subnet $subnet
```
