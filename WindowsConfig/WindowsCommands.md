# Windows Setup

## Commands

>[ChrisTitusTech-winutil](https://github.com/ChrisTitusTech/winutil)

> Go to Command Prompt as Admin and paste - restores old context menu for windows 11
```
reg.exe add "HKCU\Software\Classes\CLSID\{86ca1aa0-34aa-4e8b-a509-50c905bae2a2}\InprocServer32" /f /ve
```

> Undo context menu
```
reg.exe delete "HKCU\Software\Classes\CLSID\{86ca1aa0-34aa-4e8b-a509-50c905bae2a2}" /f
```

<br>

### Check Microsoft Recall is Running (Inside Winutil)
> Check Recall
```
Dism /Online /Get-Featureinfo /Featurename:Recall
```
> Disable RECALL: 
```
Dism /Online /Disable-Feature /Featurename:Recall
```
> Enable RECALL:
```
Dism /Online /Disable-Feature /Featurename:Recall
```

<br>

### Provisioned Apps (Autoreinstalled apps)
> Cuurent Provisioned Apps
```
Get-AppxProvisionedPackage -Online | Format-Table DisplayName, PackageName
```
> Uninstall Provisioned App, (if Online:True, RestartNeeded:False it wont reinstall)
```
Remove-AppxProvisionedPackage -Online -PackageName {paste full package name here}
```
> Check Deprovisioned Apps
```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Appx\AppxAllUserStore\Deprovisioned\
```


<br>


### Mouse Sensitivity
Why Gamers are Switching to High DPI
https://www.youtube.com/watch?v=imYBTj2RXFs
https://www.reddit.com/r/Winsides/comments/1fu7ly4/is_it_possible_increase_mouse_speed_beyond/

```
HKEY_CURRENT_USER\Control Panel\Mouse
```
> Mouse sensitivity key and set its value to 5


<br>


### Change DNS

Displays all domain names currently stored in your DNS cache
/flushdns removes cache, and will have to ask DNS server again
```
ipconfig /displaydns
ipconfig /displaydns | Select-String "Record Name"
ipconfig /flushdns
```

> https://mullvad.net/en/help/dns-over-https-and-dns-over-tls
Settings > Network & internet > Wi-Fi/Ethernet > (Hardware Properties, if on wifi) > DNS Server Assignment > Manual

IPv4
- Preferred DNS
    - IP Address ```194.242.2.4```
    - DNS over HTTPS On(manual template) ```https://base.dns.mullvad.net/dns-query```
- Alternative DNS
    - IP Address ```194.242.2.2```
    - DNS over HTTPS On(manual template) ```https://dns.mullvad.net/dns-query```

IPv6
- Preferred DNS
    - IP Address ```2a07:e340::4```
    - DNS over HTTPS On(manual template) ```https://base.dns.mullvad.net/dns-query```
- Alternative DNS
    - IP Address ```2a07:e340::2```
    - DNS over HTTPS On(manual template) ```https://dns.mullvad.net/dns-query```

<br>

### Videos

>  Disable Windows 11 Telemetry, Internet Search, Data Collection, Cortana, etc.<br>
Tek Syndicate <br>
https://youtu.be/Zcr95HBFgWg?si=6laqK7JmrjiuZSDq 

> How to Fully Optimize Windows 11 For Gaming<br>
Lecctron<br>
https://youtu.be/Ntkc6PeImhU?si=XJu-_09i5WTuWDLD 


