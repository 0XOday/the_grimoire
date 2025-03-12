Windows can report several types of error state for a local network adapter. if the connection is reported as unplugged or disconnected, you need to check the cable or wireless network configuration. Two other states are reported if the link is available, but ip is not correctly configured:

* Limited connectivity - the adapter is set to obtain an address automatically, but no DHCP server can be contacted. The adapter will either use an address from the automatic up addressing (APIPA) 169.254.x.y range or will use an address specified as an alternate configuration in ipv4 properties.
* No internet access - this means that the IP config is valid for the local network but that Windows cannot identify a working internet connection. Windows tests internet access by attempting a connection to `www.msfincsl.com` and checking that DNS resolves the IP address correctly. This state could indicate a problem with the router, with DNS or with both.
Most IP troubleshooting activity will start with an investigation of the current settings. In Windows, IP configuration information is displayed though network and sharing settings or the adapters status dialog. You can also view this information at a command line using the `ipconfig command` tool.

*ipconfig* Command 
Used without switches, ipconfig displays the ip address, subnet mask, and default gateway (router) for all network adapters to which TCP/IP is bound. The /all switch displays detailed configuration, including DHCP and DNS servers, MAC address, and NetBIOS status. `ipconfig` can resolve the following questions:

* is the adapter configured with a status address? if so, are the parameters correct ?
* is the adapter configured by dhcp? is there a valid lease ?

Some commands to keep in mind. 
	ipconfig /release *adaptername*
	ipconfig /renew *adaptername*
	ipconfig /displaydns
	ipconfig /flushdns clears cached dns records

Hostname command 
The `hostname` command returns the name configured on the local machine. if the machine is configured as a server, client machines will need to use the hostname to access shared folders and printers
*Network Reset*
if there are persistent networking problems with either a client or a sever, one "stock" response is to try restarting the computer hardware. you can also try restarting just the application service.

Another option is to reset the network stack on the device. In Windows, this will clear any custom adapter configurations and network connections, including VPN connections. There will have to be reconfigured after the reset. The Network reset command is on the Settings > Network & internet > Status page.


	


