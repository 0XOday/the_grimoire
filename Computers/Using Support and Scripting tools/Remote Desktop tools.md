* Security considerations
	* Remote access permissions should be using least privilege principles 
	* Must be using encryption 
	* The server support the connection must be safely configured especially when the server has a port making a connection over the internet 
* Remote Desktop Protocol 
	* Windows uses RDP 
	* `mstsc.exe` to run RDP you can use FQDN and IP to connect 
	* To specify a domain account use the typical format `Domain\Username`
	* starting a rdp session will lock the user out (I observed different behavior with Anydesk not sure about TigerVNC)
	* In Mac, IOS, Android can be used to establish a remote desktop session 
	* Mac screen sharing is encrypted
	* windows home editions do not include RDP server 

RDP Server and Security settings 
* You can manage security settings via the settings page
* User settings will be here selecting which ones are allowed to connect remotely 
	* Users in the local admin group are allowed to connect by default 
	* You can select users from the local account database or from the domain if joined  
	* In Advanced Settings you can allow older RDP clients to connect while also requiring RDP clients to support Network Level Authentication (NLA)
		* NLA protects the server from DOS Attacks  
	* If the endpoint is compromised credentials are at risk.
	* RDP Restricted Admin Mode and Remote Credential Guard helps mitigate this risk. 
		* [docs.microsoft.com/en-us/windows/security/identity-protection/remote-credential-guard](http://docs.microsoft.com/en-us/windows/security/identity-protection/remote-credential-guard).



