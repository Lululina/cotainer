# cotainer
Learning Story

Docker Env install:
Windows Sever 2016 DataCenter(include GUI) Install
Enable Hardware virtualization at VMWave
Install Hyper-V

Powershell TLS1.0 isue
[System.Net.ServicePointManager]::SecurityProtocol = [System.Net.SecurityProtocolType]::Tls11 -bor [System.Net.SecurityProtocolType]::Tls12;
[System.Net.ServicePointManager]::SecurityProtocol = [System.Net.SecurityProtocolType]::Tls12;



_______________________________________________________________________________
ServerCore Enable clinet connect
ServerCore
Enable-PSRemoting -force
winrm quickconfig
#設定allow all *
Set-Item WSMan:\localhost\Client\TrustedHosts -Value "*" -Force

Client:
winrm quickconfig
Set-Item WSMan:\localhost\Client\TrustedHosts $Servername -Concatenate -Force
Get-Item WSMan:\localhost\Client\TrustedHosts #confirm Server alredy add

cmdkey /add:$Servername /user:administrator /pass:*******

Enter-PSSession -ComputerName "$Servername" 
______________________________________________________________________________












