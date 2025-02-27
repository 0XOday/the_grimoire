
Page 5 of 11 : Disk Maintenance Tools

Disk Maintenance Tools

Of all the computer's subsystems, disk drives and the file system probably require the most attention to keep in optimum working order. File storage is subject to three main problems:

    Fragmentation—On a hard disk, ideally each file would be saved in contiguous clusters on the disk. In practice, over time as files grow, they become fragmented across non-contiguous clusters, reducing read performance.
    Capacity—Typically, much more file creation occurs on a computer than file deletion. This means that capacity can reduce over time. If the boot volume has less than 20% free space, performance can be impaired. When space drops below 200 MB, a Low Disk Space warning is generated.
    Damage—Hard disk operations are physically intensive, and the platters of the disk are easy to damage, especially if there is a power cut. If the disk does not recognize that a sector is damaged, files can become corrupted. SSDs can suffer from degradation of the memory circuitry, resulting in bad blocks, and can be damaged by impacts, overheating, and electrical issues.

These problems can be addressed by the systematic use of disk maintenance tools. These tools should be run regularly—at least every month and before installing software applications.
Disk Defragmenter

The Defragment and Optimize Drives tool (dfrgui.exe) runs various operations to speed up the performance of HDDs and SSDs:

    On an HDD, defragmenting rewrites file data so that it occupies contiguous clusters, reducing the amount of time the controller has to seek over the disk to read a file.
    On an SSD, data is stored in units called blocks that are not directly managed by the OS. The drive controller determines how blocks are used according to wear-leveling routines to minimize degradation of the solid-state cells. The main purpose of the optimizer tool is to instruct the controller to run a TRIM operation. Essentially, TRIM is a process by which the controller identifies data that the OS has marked as deletable and can then tag corresponding blocks as writable. The optimizer does perform a type of defragmentation operation on an SSD if it holds the OS and the system protection feature Volume Shadow Copy service is enabled.

Optimize Drives (Defragmenter) in Windows 10. (Screenshot courtesy of Microsoft.)

Windows automatically schedules the disk optimizer to run using Task Scheduler. You should check for any issues, such as it not running successfully.
Disk Clean-up

The Disk Clean-up (cleanmgr.exe) tool tracks files that can be safely erased to reclaim disk space. These files include ones deleted but still available in the Recycle Bin and various temporary files and caches. The tool can be run in administrator mode using the Clean up system files option to reclaim data from caches such as Windows Update and Defender.

#windows #storage 