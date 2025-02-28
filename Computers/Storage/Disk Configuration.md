A mass storage device or fixed disk, such as hard drive (HDD) or solid-state drive (SSD), requires partitioning and formatting before it can be used. Partition and file system options can be chosen by responding to prompts in the setup program, configured in an answer file, or built into an image that is cloned to the target disk.

A partition is a logically separate storage area. You must create at least one partition on a fixed disk before performing a high-level format to create a file system.

information about partitions is stored on the disk itself in one of two types : Master boot record (MBR) or GUID {Globally unique identifier } partition table (GPT)

MBR-Style Partitioning : The master boot record (MBR) partition style stores a partition table in the first 512-byte sector on the disk. With MBR-Style, A given physical disk can contain up to four primary partitions, any one of which can be marked as active, and therefore made bootable. This allows for four different drives on the same physical disk and for multiple operating systems ( A multiboot system) You might also use partitions to create discrete areas for user data file storage, storing log files, or hosting databases. Each drive can be formatted with a different file system.

The start of each primary partition contains a boot sector, or partition boot record (PBR). When a partition is marked as active, Its boot sector is populated with a record that points to the OS boot loader. In Windows, this active partition is also referred to as t 