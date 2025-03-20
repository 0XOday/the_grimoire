Append cat data to the destination file 
```

cat >> file

```


Metacharacters and Escaping 
When writing expressions, you need to understand how to escape metacharacters. A metacharacter is on that is interpreted by the shell in a special way. When you write an expression, you might want the asterisk to match any number of any characters.

This can be accomplished using the * metacharacter. If you want to find text that contains an asterisk character, you must escape it. Similarly, an expression that contains spaces must be escaped 

Three ways to escape strings: 

* \ escapes the next character only. For example, \ * treats * as a literal character; \\ treats \ as a literal character.
* Single quotes ('  ') preforms strong escaping, Everything within single quotes is treated as a literal character. For example, '$(pwd) * example one' results in the expression: &(pwd) * example one
* Double quotes(" ") performs weak escaping. This escapes metacharacters but expands variables and allows a feature called command substitution. For example, "$(pwd) * example one" expands to use the output of the pwd command:  /home/david * example one

df and du commands
The df and du commands check free space and report usage by the device, directory, or file specified as the argument 

* df (disk free) enables you to view the device's free space,file system, total size, space used,percentage value of space used and mount point
* `du` ("Disk usage") displays how a device is used, including the size directory trees and files within it.

User management Commands 

The commands `useradd,usermod and userdel` can be used to add, modify and delete user information. The command passwd can be used to change the password

Group management commands
Each user account can be assigned to a group as a means of allocating permissions over files. The `groupadd , groupmod and groupdel` can be used to manage group memberships

A user can belong to many groups but can only have one effctive group ID at any one time. The effective group ID is listed for the user account in etc passwd and can be changed using the `newgrp` command 


SAMBA 
Linux has a server message block (SMB) compatible file sharing protocol called Samba. Samba enables the integration of Linux and windows systems. When added to a linux workstation, that workstation can use the Windows file and print sharing protocol to access shared resources on a Windows host. When the samba service is added to a Linux server, the uses the SMB protocol to share directories to Windows clients 
