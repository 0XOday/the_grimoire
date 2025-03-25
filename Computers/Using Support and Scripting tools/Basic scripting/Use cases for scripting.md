* Python uses an API to call functions to the OS
	* API calls must be implemented as modules 
* Restarting Endpoints
	* Windows PowerShell `Restart-Computer -force` 
* Remapping Network Drives 
	* in a Windows batch file we can use the `net use` command for drive mapping 
	* We can also use `New-PSDrive` 
		* ``If (Test-Path L:) {Get-PSdrive L | Remove-PSDrive}New-PSDrive -Name "L" -Persist -PSProvider FileSystem -Root "\\MS10\LABFILES"
* Installing application scripts
	* In windows we can have a setup file execute in silent mode by using switch's 
		* ``C:\Rose\Downloads\setup.exe /S /desktopicon=yes
	*  To use a Windows installer we can add the `msiexec` command 
		* `msieexec C:\rose\Downlaods\install.msi /qn`
		* Start-Process cmdlet allows us to have more control of how the installation goes 
* Installing updates 
	* `wusa.exe` can be called from a batch file to preform update tasks 
	* We can do the same thing in PowerShell with `PSWindowsUpdate` module  
* information gathering 
	* ``Get-NetAdapter gets network adaptor information
	* ```Get-WinEvent returns log information
		* for both of these we can use `Where-Object` and `Select-Object` to apply filters 
		