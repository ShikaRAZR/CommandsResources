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

## Videos

>  Disable Windows 11 Telemetry, Internet Search, Data Collection, Cortana, etc.<br>
Tek Syndicate <br>
https://youtu.be/Zcr95HBFgWg?si=6laqK7JmrjiuZSDq 

> How to Fully Optimize Windows 11 For Gaming<br>
Lecctron<br>
https://youtu.be/Ntkc6PeImhU?si=XJu-_09i5WTuWDLD 


