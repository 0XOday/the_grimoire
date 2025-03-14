netstat command can be used to investigate open ports and connections on the local host. in a troubleshooting context, you can use this tool to verify whether other clients are connecting to them.

When used without switches, `netstat` lists active and listening TCP ports. An active port is connected to a foreign address, while a listening port is wating for a connection. the following represent some of the main switches that can be used: 
* -a includes UDP ports in the listening state
* -b shows the process that has opened the port. Alternatively, use the -o switch to list the process ID rather than the process name. these can only be used from an administrative command-prompt. 
* -n displays ports and addresses in numerical format. skipping name resolution speeds up each query.
* -e and -s can be used to report Ethernet and protocol statistics respectively 