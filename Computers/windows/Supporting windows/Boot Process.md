When a computer starts, the firmware runs a power on self-test (POST) to verify that the system components are present and functioning correctly. it then identifies a boot devices and passes control to the operating systems' boot loader process.

With a Legacy BIOS, the firmware scans the disk identified as the boot device and reads the master boot record (MBR) in the first sector of the disk. The MBR identifies the boot sector for the partition marked as active. The boot sector loads the boot manager, which for Window is BOOTMGR.EXE. The boot manager reads information from the boot configuration data (BCD) file, which identifies operating systems installed on the computer. BOOTMGR and the BCD are normally installed to a hidden System Reserved partition.

Assuming there is only a single Windows installation, The boot manager loads the windows boot loader WINLOAD.EXE stored in the system root folder on the boot partition.

WINLOAD then continues the windows boot process by loading the windows kernel (NTOSKRNL.EXE), the hardware abstraction layer (HAL.DLL), and boot devices drivers. Control is then passed to the kernal, which initializes and starts loading the required processes. When complete, the WINLOGON process waits for the user to authenticate.

In UEFI boot mode, the initial part of the boot process is different. following POST, The firmware reads the GUID partition table (GPT) on the boot device.

The GPT identifies the EFI System Partition. The EFI system partition contains the EFI boot manager and BCD. Each Windows installation has a subfolder under `\EFI\Microsoft\` that contains a BCD and BOOTMGW.EFI

BOOTMGW.EFI reads the BCD to identify whether to show a boot menu and to find the location of the WINLOAD.EFI from this point, The windows boot loader continues the boot process by loading the kernel, as described previously 



