When sharing a folder, the basic Give access to interface conceals some of the complexity of the Windows NTFS versus share permissions system: 

* Share-level permissions only apply when a folder is accessed over a network connection. They offer no protection against a user who is logged on locally to the computer hosting the shared resource.
* NTFS permissions are applied for both network and local access and can be applied to folders and to individual files. NTFS permissions can be assigned directly to user accounts, but it is better practice to assign permissions to security groups and make users members of appropriate groups.

NTFS permissions can be configured for a file or folder using the Security tab in its properties dialog.

The Security tab shows the ACL applied to the file or folder. Each access control entry (ACE) assigns a set of permissions
to a principal. A principal can either be a user account or a security group. The simple permissions are as follows:

* Read/list/execute permissions allows principals to open and browse files and folders and to run executable files.
* Write allows the principal to create files and subfolders and to append data to files.
* Modify allows the principal write permission plus the ability to change existing file data and delete files and folder.
* Full control allows all the other permissions plus the ability to change permissions and change the owner of the file or folder.