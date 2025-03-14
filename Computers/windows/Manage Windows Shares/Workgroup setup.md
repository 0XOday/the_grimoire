As well as user management, the network model determines how shared resources are administrated. A workgroup is a peer-to-peer network model in which computers can share resources but management of each resource is performed on the individual computers. A domain is based on a client/server model that groups computers together for security and to centralize administration.  Some computers are designated as servers that host resources, while others are designated as clients that access resources. Administration of the servers and clients is centralized.

*Joining a Workgroup*
Windows setup automatically configures membership of the default workgroup, named *WORKGROUP*. Each computer is identified in the network browser by a hostname. The hostname can be changed using the *system properties* dialog or `sysdm.cpl`

*Network Discovery and file sharing*
Within a workgroup, the network type must normally be set to Private to make the computer discoverable and allow sharing. if the network type is Public, a notification will display in File Explorer when the Network object is selected. You can use this notification to make the network private. You can also change the network type via Network & internet settings. Sharing options are configured via the Advanced sharing settings applet in control Pane. To share files on the network, Turn on network discovery and Turn on file and printer sharing must both be selected.

Under All networks, you can select Turn off password-protected sharing to allow anyone to access file shares configured on the local computer without entering any creds. This works by enabling the Guest user account for network access only. 

Note : For password-protected sharing. Network users must have an account configured on the local machine. This is one of the drawbacks of workgroups compared to domains. Either you configure accounts for all users on all machines and manage passwords on each machine manually, use a single shared account for network access which still needs to be configured on all machines or disable security entirely.

Note : Windows also supports nearby sharing. This refers to sharing data between a PC and smartphone or another device over bluetooth in a personal area network (PAN) this is a simple way to exchange files between devices. 


