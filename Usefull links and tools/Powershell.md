#####  get local user SID

Get-LocalUser -Name BTLO |select SID


###### zone identifier

```ps
C:\Progs\Forensics> Get-Content -Path C:\Progs\Forensics\autopsy-4.17.0-64bit.msi -Stream zone.identifier
```

https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.management/get-content?view=powershell-7.2