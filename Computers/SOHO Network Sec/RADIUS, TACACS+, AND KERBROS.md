Enterprise authentication uses an AAA server and network directory. These components can be implemented by several different protocols.

**RADIUS**
Remote Authentication Dial-in User Service is one way of implementing the AAA server when configured enterprise authentication. The wireless access point is configured as a client of the RADIUS server. Rather than storing and validating user credentials directly, it forwards this data between the RADIUS server and the supplicant without being able to read it. The wireless access point must be configured with the host name or IP address of the RADIUS server and a shared secret . The shared secret allows the RADIUS server and access point to trust one another

**TACACS+**
Terminal Access Controller Access Control System Plus is another way of implementing AAA. TACACS+ was developed by Cisco but is also supported on many third-party implementations. Where RADIUS is often used to authenticate connections by wireless and VPN users, TACACS+ is often used in authenticating administrative access to routers, switches and access points.

**Kerberos**
In theory, an access point could allow a user to authenticate directly to a directory server using the Kerberos protocol. On Windows networks, Kerberos allows a user account to authenticate to a domain controller over a trusted local cabled segment. Kerberos facilitates single sign-on. As well authenticating the user on the network, the Kerberos server issues authorization tickets that give the user account rights and permissions on compatible application servers.

in practice, there are no access points with direct support for Kerberos. Access points use RADIUS or TACACS+ and EAP to tunnel the creds and tokens that allow a domain user connecting via wireless client to authenticate to a DC and use SOO authorizations. 