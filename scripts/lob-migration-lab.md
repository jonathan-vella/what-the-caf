# Line-of-business application migration

A series of scripts that can be of great help during this lab.

---

#### Re-arm SQL Server VM

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


