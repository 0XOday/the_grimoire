A user account is the principal means of controlling access to computer and network resources and assigning rights or privileges. In windows, a user can be set up with a local account or Microsoft account:
* A local account is defined on that computer only.  For example `PC1\David` is that username for an account configured on a host named PC1. A local user account is stored in a database known as the *Security Account Manger* (SAM), which is part of the `HKEY_LOCAL_MACHINE` registry. Each machine maintains its own SAM and set of SIDs for accounts. Consequently, a local account cannot be used to log on to a different computer or access a file over the network.
* A *Microsoft account* is managed via an online portal (account.microsoft.com) and identified by an email address Configuring access to a device by a Microsoft account creates a profile associated with a local account. Profile settings can be synchronized between devies via the online portal.
The guided setup process requires a Microsoft account to be configured initially. However, the account type can be switched from Microsoft to local or local to Microsoft as preferred via the Your info page in the settings app.

Security Groups
A security group is a collection of user accounts. Security groups are used when assigning permissions and rights, as it is more efficient to assign permissions to a group than to assign them individually to each user. you can set up a number of custom groups with least privlege permissions for different roles and then make user accounts members of the appropriate group(s)

Build-in groups are given a slandered set of rights that allow them to perform appropriate system tasks.
* A user account that is a member of the Administrators group can perform all management tasks and generally has very high access to all files and other objects in the system. The local or Microsoft user created during setup is automatically added to this group. Other accounts should not routinely be added to the administrators group. it is more secure to restrict membership of the administrators group as tightly as possible.
* *Standard account* is a member of the User group. This group is generally only able to configure settings for its profile. However, it can also shut down the computer, run desktop applications, install and run store apps, and use printers. Additional accounts should be set up as standard users unless there is a compelling reason to add another admin account.
* *Guest* group is only present for legacy reasons. is has the same default permissions and rights as the User group
* *Power users* group is present to support legacy applications. Historically, this group was intended to have intermediate permissions between admin and users. However, this approach created vulns that allowed accounts to escalate to the admin group. in Windows 10/11, this group has the same permissions as the standard Users group.
*Local Users and Groups*
The Local Users and Groups management console provides an interface for managing both user and group accounts. Use the shortcut menus and object Properties dialogs to create, disable, and delete accounts, change account properties, reset user passwords, create groups and modify group membership. 

*Net user commands*
You can also manage accounts at the command line using *net user*. You need to execute these commands in administrative command prompt.
* Add a new user account and force the user to choose a new password at first login: `net user dildoswagins Pa$$w0rd /add /logonpasswordchg:yes`
* disable dildoswagins account : `net user dildoswagins /active:no 
* Show the properties of dildoswagins account `net user dildoswagins`
* Add dildoswagins account to the admin local group `net localgroup Administrators dildoswagins /add`
*


