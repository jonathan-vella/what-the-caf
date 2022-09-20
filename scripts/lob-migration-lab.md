# Line-of-business application migration

A series of scripts that can be of great help during this lab.

---

## Connect to SmartHotelHost VM using Azure Bastion with Native Client support

You can connect to your SmartHotelHost using Azure Bastion with Native Client support by performing the following:

- Peer the "SmartHotelVNet" and the "smarthotelhostvnet" virtual networks. Guidance is available [here](https://learn.microsoft.com/en-us/azure/virtual-network/virtual-network-manage-peering).

- Upgrade the "SmartHotelBastion" Azure Bastion SKU to Standard. Guidance is available [here](https://learn.microsoft.com/en-us/azure/bastion/upgrade-sku).

- Enable Azure Bastion Native Client support. Guidance is available [here](https://learn.microsoft.com/en-us/azure/bastion/connect-native-client-windows#to-modify-an-existing-bastion-deployment).

- You can use the PowerShell commands below to connect to your SmartHotelHost VM using Azure Bastion with Native Client:

```powershell
# Connect to Bastion using Native Client
# https://docs.microsoft.com/en-us/azure/bastion/connect-native-client-windows#connect

# Variables
$Subscription="your azure subscription name"
$BastionName="SmartHotelBastion"
$BastionResourceGroup="SmartHotelRG"
$VmID="your VM ID"

# Login to Azure
az login
az account set --subscription $Subscription

# Connect via RDP to Windows VM
az network bastion rdp --name $BastionName --resource-group $BastionResourceGroup --target-resource-id $VmID

```

---

## Re-arm SQL Server VM

Run the following PowerShell command on the host VM (SmartHotelHost) either via Invoke-AzVMRunCommand, the Run Command in the Portal GUI, or RDP'ing to the host and running it there:

```powershell
$VMName = "smarthotelSQL1"
$vm = Get-VM -Name $VMName 
do {
  if ($vm.state -eq "Off") { $vm | Start-VM }
  sleep -Seconds 5
  $ip = $vm.NetworkAdapters[0].IPAddresses[0]
} until ($ip)
Write-Output "Re-arm (extend eval license) for VM $VMName at $ip"
set-item wsman:\localhost\Client\TrustedHosts -value $ip -Force

# Replace string (item in quotes "") on next line with actual password before running
$secPassword = ConvertTo-SecureString "enter your lab password here" -AsPlainText -Force

$cred = New-Object System.Management.Automation.PSCredential ("Administrator", $secPassword)
Invoke-Command -ComputerName $ip -ScriptBlock { 
    slmgr.vbs /rearm
    net accounts /maxpwage:unlimited
    Restart-Computer -Force 
} -Credential $cred
```

> Note: Replace "enter your lab password here" with the password provided in the hands-on lab guide.

---
