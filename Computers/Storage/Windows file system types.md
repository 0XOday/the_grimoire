NTFS : New technology file system is a proprietary file system developed by microsoft for use with windows. It provides a 64-bit addressing scheme, allowing for very large volumes and file sizes.

The maximum in theory volume size is 16 exabytes, but in practice it is limited to between 137 GB and 256 TIB depending on the windows version. 

Key NTFS features are : 
	Journaling - when data is written to an NTFS volume, it is re-read, verified, and logged. in the event of a problem, the sector concerned is marked as bad and the data is relocated. journaling makes recovery after power outages and crashes faster and more reliable. 
	Snapshots - This allows the Volume Shadow copy service to make read-only copies of files at given points in time even if the files is locked by another process. This file version history allows users to revert changes more easily and also supports backup operations. 
	Security - Features such as file permissions and ownership, file access audit trails, quota management, and encrypting file system (EFS) allow administrators to ensure only authorized users can read/modify file data.
	 POSIX Compliance - To support UNIX/Linux compatiblity, Microsoft engineered NTFS to support case-sensitive nameing, hard links, other key features required by UNIX/Linux applications. 
	Indexing - The indexing Service creates a catalog of file and folder locations and properties speeding up searches.
	 Dynamic Disks - This disk management feature allows space on multiple physical disks to be combined into volumes 

windows can only be installed to an NTFS-formatted partition, NTFS is also usually the best choice for additional partitions and removable drives that will be used with windows. The only significant drawback of NTFS is that it is not fully supported by other operating systems. 


#windows #storage #file-systems 