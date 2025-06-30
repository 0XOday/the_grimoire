User and Group Accounts

A **user account** is the principal means of controlling access to computer and network resources and assigning rights or privileges. In Windows, a user can be set up with a local account or a Microsoft account:

- A **local account** is defined on that computer only. For example, PC1\David is the username for an account configured on a host named PC1. A local user account is stored in a database known as the Security Account Manager (SAM), which is part of the HKEY_LOCAL_MACHINE registry. Each machine maintains its own SAM and set of SIDs for accounts. Consequently, a local account cannot be used to log on to a different computer or access a file over the network.
- A **Microsoft account** is managed via an online portal (account.microsoft.com) and identified by an email address. Configuring access to a device by a Microsoft account creates a profile associated with a local account. Profile settings can be synchronized between devices via the online portal.

The guided setup process requires a Microsoft account to be configured initially. However, the account type can be switched from Microsoft to local or local to Microsoft as preferred via the **Your info** page in the Settings app.

### Security Groups

A security **group** is a collection of user accounts. Security groups are used when assigning permissions and rights, as it is more efficient to assign permissions to a group than to assign them individually to each user. You can set up a number of custom groups with least privilege permissions for different roles and then make user accounts members of the appropriate group(s).

Built-in groups are given a standard set of rights that allow them to perform appropriate system tasks.

- A user account that is a member of the **Administrators** group can perform all management tasks and generally has very high access to all files and other objects in the system. The local or Microsoft user created during setup is automatically added to this group. Other accounts should not routinely be added to the Administrators group. It is more secure to restrict membership of the Administrators group as tightly as possible.

There is also a _user_ account named "Administrator," but it is disabled by default to improve security.

- A **standard account** is a member of the Users group. This group is generally only able to configure settings for its profile. However, it can also shut down the computer, run desktop applications, install and run store apps, and use printers. Additional accounts should be set up as standard users unless there is a compelling reason to add another administrative account.
- The **Guest** group is only present for legacy reasons. It has the same default permissions and rights as the User group.

The Guest _user_ account is disabled by default. Microsoft ended support for using the Guest account to login to Windows in a feature update. The Guest account is only used to implement file sharing without passwords.

- The **Power Users** group is present to support legacy applications. Historically, this group was intended to have intermediate permissions between administrators and users. However, this approach created vulnerabilities that allowed accounts to escalate to the administrators group. In Windows 10/11, this group has the same permissions as the standard Users group.

### Local Users and Groups

The **Local Users and Groups** management console provides an interface for managing both user and group accounts. Use the shortcut menus and object Properties dialogs to create, disable, and delete accounts, change account properties, reset user passwords, create custom groups, and modify group membership.

![](https://s3.amazonaws.com/wmx-api-production/courses/35011/images/4543-1640183213613-windows_10_group_account.png)

Configuring members of the Administrators built-in group. (Screenshot courtesy of Microsoft.)

### net user Commands

You can also manage accounts at the command line using **net user**. You need to execute these commands in an administrative command prompt.

- Add a new user account and force the user to choose a new password at first login:

net user dmartin Pa$$w0rd /add /fullname:"David Martin" /logonpasswordchg:yes

- Disable the dmartin account:

net user dmartin /active:no

- Show the properties of the dmartin account:

net user dmartin

- Add the dmartin account to the Administrators local group:

net localgroup Administrators dmartin /add