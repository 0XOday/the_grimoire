When folders are secured using NTFS and/or share permissions, the matter of inheritance needs to be considered.

The first consideration is that NTFS permissions assigned to a folder are automatically inherited by the files and subfolders created under the folder. This default inheritance behavior can be disabled via Security > Advanced > Permission tab, however

Note : Directly assigned permissions (Explicit permissions) always override inherited permissions, including "Deny" inherited permissions. For example , if a parent folder specifies deny write permissions but an account is granted allow write permissions directly on a child file object, the effective permission will be to allow write access on the file object.

The second consideration is the combination of share and NTFS permissions. The permissions design needs to account for the following factors : 

* Share permissions only protect the resource when it is accessed across the network; NTFS permissions apply locally and across the network.
* Share permissions are set at the root of the share and all files and subdirectories inherit the same permissions.
* NTFS permissions inheritance is configurable and therefore is used in combination with the share permissions to provide greater flexibility; for example, to place more restrictive permissions at lower levels in the directory structure.
* if both share and NTFS permissions are applied to the same resource, the most restrictive applies when the file or folder is accessed over the network. For example, if the group "Everyone" has *read* permissions to a share and the "Users" group is given *Modify* permission though NTFS permissions, the effective permissions for a member of the "Users" group will be *read*
Note : Disk partitions using the FAT32 file system can only be protected using share permissions 

As the interaction between these permissions is quite complex, most of the time, the shared folder permission is set to FULL CONTROL for either the everyone or authenticated Users default groups The effective permissions are managed using NTFS security. 