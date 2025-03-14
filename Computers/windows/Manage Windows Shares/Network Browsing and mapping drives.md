On both workgroup and domain networks, shares are listed by the file server computer under the Network object in File Explorer. Each computer is identified by its hostname. You can browse shares by opening the computer icons. Any network-enabled devices such as wireless displays, printers, smartphones, and routers/modems are also listed here.

*Mapped Drives*

A mapped drive is a share that has been assigned to a drive letter on a client device. To map a share as a drive, right click it and select Map Network Drive. Select a drive letter and keep Reconnect At Sign in checked unless you want to map the drive temporarily. The drive will now show up under This PC. To remove a mapped drive, right-click it and select Disconnect.

*net use Commands*

There are several *net* and *net use* command utilities that you can use to view and configure resources on a Windows network. A few of the commands are provided here, but you can view the full list by entering *net /?*

```
net view - Displays servers on the local network

net view \\MYSERVER - lists the shares on the target server

net use M: \\MYSERVER\DATA /persistent:yes - mounts the data folder from target server with the flag to keep it persistent between reboots

net use M: /delete - removes the mounted drive from the local computer 

net use * /delete - removes all mounted drives
```