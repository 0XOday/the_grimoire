* Promote a server to DC 

```
Install-ADDSDomainController `
-SkipPreChecks `
-NoGlobalCatalog:$false `
-CreateDnsDelegation:$false `
-CriticalReplicationOnly:$false `
-DatabasePath "C:\Windows\NTDS" `
-DomainName "TreyResearch.net" `
-InstallDns:$true `
-LogPath "C:\Windows\NTDS" `
xiiIntroduction
-NoRebootOnCompletion:$false `
-SiteName "Default-First-Site-Name" `
-SysvolPath "C:\Windows\SYSVOL" `
-Force:$true
```

