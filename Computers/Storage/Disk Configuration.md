A mass storage device or fixed disk, such as hard drive (HDD) or solid-state drive (SSD), requires partitioning and formatting before it can be used. Partition and file system options can be chosen by responding to prompts in the setup program, configured in an answer file, or built into an image that is cloned to the target disk.

A partition is a logically separate storage area. You must create at least one partition on a fixed disk before performing a high-level format to create a file system.

information about partitions is stored on the disk itself in one of two types : Master boot record (MBR) or GUID {Globally unique identifier } partition table (GPT)

# MBR-Style Partitioning 
- The master boot record (MBR) partition style stores a partition table in the first 512-byte sector on the disk. With MBR-Style, A given physical disk can contain up to four primary partitions, any one of which can be marked as active, and therefore made bootable. This allows for four different drives on the same physical disk and for multiple operating systems ( A multiboot system) You might also use partitions to create discrete areas for user data file storage, storing log files, or hosting databases. Each drive can be formatted with a different file system.

* The start of each primary partition contains a boot sector, or partition boot record (PBR). When a partition is marked as active, Its boot sector is populated with a record that points to the OS boot loader. In Windows, this active partition is also referred to as the system partition or system reserved. the drive containing the windows  operating system files is referred to as the boot partition. This can be on a logical drive in an extended partition and does not have to be the same as the system drive.
* When the disk uses MBR partitioning, the system firmware must be set to use the legacy BIOS boot method. if the boot method is set to UEFI, the disk will not be recognized as a boot device.

**GPT-Style Partitioning**

* The globally unique identifier (GUID) partition table (GPT) style provides a more up-to-date scheme to address some of the limitations of MBR. One of the features of GPT is support for more than four primary partitons. Windows allows up to 128 partitions with GPT. GPT also supports larger partitions 2 TB + and a backup copy of the partition entries. A GPT-style disk includes a protective MBT for compatibility with systems that do not recognize GPT

When the disk uses GPT partitioning, the system firmware must be set to use the UEFI boot method. If the boot method is set to BIOS, the disk will not be recognized as a boot device. 

Note : The mbr2gpt utility can be used in a windows 10 1703 and later to convert a disk with an existing partition structure and data. there are also third-party utilities that will perform this type of conversion. as with any important system change, A backup should be made before attemting the conversion. Following the conversion, use the firmware setup program to switch to UEFI boot mode.

**Drive Format**

An OS must be installed to a partition formatted useing a compatible file system. For Windows, this means using NTFS, MacOS APFS and Linux can use ext3/ext4 or a variety of other file system types. During an attended installation, Partition and formatting choices are guided by the setup program. 








