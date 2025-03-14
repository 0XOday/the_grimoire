To troubleshoot boot issues, you need to use options and recovery tools to access an environment in which to run tests and attempt fixes.

**Advanced Boot Options**
The Advanced Boot Options menu allows the selection of different startup modes for troubleshooting. Startup options are displayed automatically if the system cannot start the OS. You can also invoke the menu manually with BIOS boot, startup options are accessed by pressing F8 before the OS loads. With UEFI, You need to reboot to show boot options. Hold the SHIFT key when selecting the Restart option from the Power menue on the lock screen -- note that you don't have to sign in to view the power menu.

Within startup options, from the first Choose an option screen, Select Troubleshoot. From the next screen select Advanced options. Select Startup Settings, and then on the next screen select Restart.

Press F4 to select Safe Mode, or choose another option as necessary. Safe Mode loads only basic drives and services required to start the system. This is a useful troubleshooting mode as it isolates reliability or performance problems to add-in drivers or application services and rules without having to fully reinstall Windows. It may also be a means of running analysis and recovery tools, such as chkdsk, System Restorer antivirus utilizes.

**WinRE and Startup Repair**

If you cannot boot the computer or access startup options from the local installation, you can try booting from the product media, a repair disk, or a recovery partition. You may have to access BIOS or UEFI setup to configure the recovery media as the priority boot device.
if you don't have the product media, you can make a system repair disk from Windows using the *Create a recovery drive* setting. you need to have done this before the computer starts failing to boot or create one using a working Windows installation. 

Once in the recovery environment, select the *Trouble shoot* menu and then *Advanced options*. if the boot files are damaged, you can use the *startup repair* option to try to fix them. You can also launch *system Restore* or restore from an image backup, perform a refresh, or reset reinstallation of Windows from here. The last two options are to run a memory diagnostic and to drop into the *Windows Recovery Environment (WinRE)* command prompt, Where you could run commands such as `diskpart, sfc, chkdsk bootrec bcedit, regedit` to try to repair the installation manually 


