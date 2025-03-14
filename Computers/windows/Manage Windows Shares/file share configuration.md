Simple enabling file sharing does not make any resources available to do that, you need to configure a file.

in a workgroup, you can enable Public folder sharing to make a shared resource available quickly. The public folder is a directory that all users of the computer can read and write to. This can be shared over the network by selecting the option under `Advanced sharing settings > All networks > Turn on sharing so anyone with network access can read and write files in the Public folders`

To share a specific folder, right-click it and select `Give access to.` Select an account, and then set the Permission level to Read or Read/write as appropriate.

The Share tab in the folders properties dialog can be used to customize permissions, change share name, and limit the number of simultaneous connections. Windows Desktop versions are limited to 10 inbound connections. 

in addition to any local shares created by a user, Windows automatically creates hidden administrative shares. These include the root folder of any local drives `(C$) and the system folder (ADMIN$)`. Administrative shares can only be accessed by members of the local Administrators group

Note : In fact, if you add a $ sign at the end of a local share name, it will be hidden from general browsing too. It can still be accessed via the command-line or by mapping a drive to the share name.