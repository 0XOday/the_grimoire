```

```VBScript
Set oShell = CreateObject("WScript.Shell")
sDst = oShell.SpecialFolders("Desktop")
sTarget = "http://tickets.515support.com"
Set oFso = CreateObject("Scripting.FileSystemObject")
Set oUrl  = oFso.CreateTextFile(sDst & "\Tickets.url", True)
oUrl.WriteLine "[DEFAULT]"
oUrl.WriteLine "BASEURL=" & sTarget

oUrl.WriteLine "[InternetShortcut]"
oUrl.WriteLine "URL=" & sTarget

oUrl.WriteLine "IconFile=file://LOCALHOST/Windows/System32/SHELL32.dll"
oUrl.WriteLine "IconIndex=23"
oUrl.Close
```


```