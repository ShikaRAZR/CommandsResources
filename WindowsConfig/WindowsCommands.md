# Windows Setup

## Commands
- Go to Command Prompt as Admin and paste - restores old context menu for windows 11
```
reg.exe add "HKCU\Software\Classes\CLSID\{86ca1aa0-34aa-4e8b-a509-50c905bae2a2}\InprocServer32" /f /ve
```

- Undo context menu
```
reg.exe delete "HKCU\Software\Classes\CLSID\{86ca1aa0-34aa-4e8b-a509-50c905bae2a2}" /f
```

- Check Microsoft Recall is Running (Inside Winutil)
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

## Videos

>  Disable Windows 11 Telemetry, Internet Search, Data Collection, Cortana, etc.<br>
Tek Syndicate <br>
https://youtu.be/Zcr95HBFgWg?si=6laqK7JmrjiuZSDq 

> How to Fully Optimize Windows 11 For Gaming<br>
Lecctron<br>
https://youtu.be/Ntkc6PeImhU?si=XJu-_09i5WTuWDLD 


