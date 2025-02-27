```
shutdown /s closes all open programs and services before powering off the computer/ The user should save changes in any open files first but will be prompted to saace any open files during shutdown. The shutdown /t nn command can be used to specify delay in seconds. the default is 30 seconds. If a shutdown is in progress, shutdown /a abourts it.  

Hibernate - shutdown /h 

Log off - shutdown /i

Restart - shutdown /r

```

## System file checker 

```
The windows Resource Protection mechanism prevents damage to or malicious use of system fifles and registry keys and files.

sfc - provides a manual interface for for verifying system files and resotring them from cache if they are found corrupt of damaged 


sfc /scannow 

sfc /scanonce - schedules a scan when the computer is next restarted 

sfc /scanboot - schedules a scan each time the pc boots
```

## Reporting Windows Version

The winver command reports version information. 

Windows 10 or Windows 11 is a “brand” version. Its main purpose is to identify the OS as a client version because Windows Server versions use the same codebase.
Version refers to a feature update via a year/month code representing the time of release, such as 1607 (July 2016) or 21H1 (first half of 2021).
OS Build is a two-part numeric value with the first part representing the brand plus feature update and the second rev part representing quality update status (patches). You can use the rev number to look up changes and known issues associated with the update in the Microsoft Knowledge Base


#windows #system-management