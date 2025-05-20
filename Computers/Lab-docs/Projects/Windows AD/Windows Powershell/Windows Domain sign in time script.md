[Removing unnecessary apps from windows 10 base image](https://learn.microsoft.com/en-us/windows-server/storage/folder-redirection/deploy-roaming-user-profiles)

- To remove apps, use the [Remove-AppxProvisionedPackage](https://learn.microsoft.com/en-us/powershell/module/dism/remove-appxprovisionedpackage) cmdlet in Windows PowerShell to uninstall the following applications. If your PCs are already deployed, you can script the removal of some apps by using [Remove-AppxPackage](https://learn.microsoft.com/en-us/powershell/module/appx/remove-appxpackage).
- Microsoft.windowscommunicationsapps_8wekyb3d8bbwe
    - Microsoft.BingWeather_8wekyb3d8bbwe
    - Microsoft.DesktopAppInstaller_8wekyb3d8bbwe
    - Microsoft.Getstarted_8wekyb3d8bbwe
    - Microsoft.Windows.Photos_8wekyb3d8bbwe
    - Microsoft.WindowsCamera_8wekyb3d8bbwe
    - Microsoft.WindowsFeedbackHub_8wekyb3d8bbwe
    - Microsoft.XboxApp_8wekyb3d8bbwe
    - Microsoft.XboxIdentityProvider_8wekyb3d8bbwe
    - Microsoft.ZuneMusic_8wekyb3d8bbwe

```
Get-AppxProvisionedPackage -Online| Where-Object DisplayName -like "*Microsoft.BingWeather*" | Remove-AppxProvisionedPackage -Online
```
* We can get a list of provisioned apps installed via the command `Get-AppxProvisionedPackege -online` then use `|` to redirect that output to `DisplayName -like "Microsoft.BingWeather (or whatever)` then pipe that to `Remove-AppxProvisionedPackage -Online` to remove what we want  
	* Side note Remove-ProvisionedPackage removes app for *future accounts* from the windows image 
	* Remove-appxPackage removes the apps from the current or specified user profile 