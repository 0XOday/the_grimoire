A blue screen of death displays a Windows Stop error. Which causes Windows to halt. Stop errors can occur when windows loads or while it is running. Most BSODs especially those that occur during startup, are caused by faulty hardware or hardware drivers. use the following procedures to try to troubleshoot the issue : 

* Use System Restore of (if you can boot safe Mode) driver tollback, or update rollback to restore the system to a working state
* Remove a recently added hardware device, or uninstall a recently installed program.
* check seating of hardware components can cables
* Run hardware diagnostics, chkdsk and scan for malware
* check fans and chassis vents for dust and clean if necessary
Make a note of the stop error code (which will be in the form : Stop 0x0) and search the Microsoft knowledge Base (support.microsoft.com/search) for known fixes and troubleshooting tips. The carious newsgroups accessible from this site offer another valuable source of assistance.

*System instability and Frequent Shutdowns*

A system that exhibits instabllity will freeze, shutdown, reboot or power off without any sort of error message. This type of error suggests an overheating problem, a power problem, a CPU/shipset/RAM issue or corrupt kernel files.

Windows includes a Windows Memory Diagnostics tool to test memory for errors. You can either run the tool from Administrative Tools or boot the recovery environment. The computer will restart and run the test. Press F1 if you want to test options.

if errors are found, first check that all the memory modules are correctly seated. remove all the memory modules but one and retest. you should be able to identify the faulty board by process of elimination. if a known-good memory module is reported faulty, the problem is likely to lie in the motherboard

if you suspect file corruption, run `chdsk` to verify the boot volumes file system and `sfc /verifyonly` to only scan windows system files if a tool reports errors, run it in repair mode `chkdsk /f or sfc /scannow` to attempt to fix the issue.

*usb issues*
if there are issues with USB devices not working after a connection, not working after the computer resumes from sleep/hibernation. or generating warning messages, make sure the controllers are using the lasted drivers 

A USB controller resource warning indicates that too many devices are connected to a single controller. this typically occurs if you use an unpowered USB hub to expand the number of ports available and connect more than five devices to a single controller. if updateing the chipset drivers doesn't resolve the issue, try the following.

1. connect the hub to a USB 2 port rather than USB 3 port. While USB 3 is higher bandwidth, in some chipset implementations each controller supports fewer device connections. use the hub to connect low-bandwidth input/output devices over USB 2 and reserve use of USB 3 ports for external disks and network adaptors.
2. Reduce the number of devices to see if that solves the issue. if it doesn't test to see if one device is the source of the errors.


























