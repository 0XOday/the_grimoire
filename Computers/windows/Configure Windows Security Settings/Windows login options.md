Windows authentication involves a complex architecture of components ([docs.microsoft.com/en-us/windows-server/security/windows-authentication/credentials-processes-in-windows-authentication](https://docs.microsoft.com/en-us/windows-server/security/windows-authentication/credentials-processes-in-windows-authentication)), but the following three scenarios are typical:
* Windows local sign-in - The Local Security Authority (LSA) compares the submitted credential to the one stored in the Security Accounts Manage (SAM) database, which is part of the registry. This is also referred to as interactive logon.
* Windows network sign-in : The LSA can pass credentials for authentication to a network service. The preferred system for network authentication is based on a system called Kerberos 
* Remote sign-in -- if the user's device is not connected to the local network, authentication can take place over some type of VPN or web portal

Username and Password 
A username and password credential is configured by creating the user account and choosing a password. The user can change the password by pressing CTRL+ALT+DELETE or using account settings. An administrator can also reset the password using Local Users and Groups. 

Windows hello 
The windows hello subsystem allows the user to configure an alternative means of authenticating. Depending on hardware support, the follow options are available:
* Personal identification number - unlike a normal Microsoft account password, a Windows hello PIN is separately configured for each device. it uses the Trusted platform module (TPM) feature of the CPU or chipset and encryption to ensure that the PIN does not have to be stored on the device itself. This is designed to prevent the sort of sniffing and interception attackts that ordinary passwords are subjected to. Despite the name, a PIN can contain letters and symbols.
* also the typical authentication options such as pinchy print and security keys

Single Sign-On
Signle Sign-On means that a user authenticates once to a device or network to gain access to multiple applications or services. The Kerberos authentication and authorization model for Active Directory domain networks implements SSO. A user who has authenticated with Windows is also auth'd with the Windows domain's SQL Server and Exchange Server services. Another example is signing in to Windows with a Microsoft account and also being signed in to cloud applications such as OneDrive and Microsoft 365
The advantage of SSO is that each user does not have to manage multiple digital identities and passwords. The disadvantage is that compromising the account also effects other services. The use of passwords in SSO systems has proven extremely vulnerable to attacks.  

The windows hello for business mechanism seeks to mitigate these risks by transitioning to a passwordless SSO. This works as follows
1. The user devices is registered on the network. This uses public/private encryption keypair The private key is only stored within the TPM of the user device and never transmitted over the network or known by the user . The public key is registered on the server
2. When the user auths to the device via Windows Hello, the device communicates a secret encrypted by its private key to the network auth server.
3. The server uses the public key to decrypt the secret. This proves that the secret really did come from the device as it could only have been encrypted by the private key. Therefore, the network server can auth the user account and issue it with an authorization token to use network services and applications. 