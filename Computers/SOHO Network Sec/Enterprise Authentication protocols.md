The main problems with personal modes of authentication are that distribution of the passphrase cannot be secured properly and that the access point administrator may choose an unsecure passphrase. Personal authentication also fails to provide accounting because all users share the same credential.

As an alternative to personal authentication, WPA's 802.1x enterprise authentication method implements the Extensible Authentication Protocol (EAP). EAP allows the use of different mechanisms to authenticate against a network directory. 802.1x defines the use of EAP over Wireless (EAPoW) to allow an access point to forward authentication data without allowing any other type of network access. it is configured by selecting WPA2-Enterprise or WPA3-Enterprise as the security method on the access point.

Enterprise authentication uses the following general workflow:
1. When a wireless station (a supplicant) requests an association, the AP enables the channel for EAPoW traffic only
2. is passes the credentials submitted by the supplicant to an Authentication, Authorization, and Accounting (AAA) server on the wired network for validation. The AAA server determines weather to accept the credential.
3. When the use has been authenticated, the AAA server transmits a master key (MK) to the wireless PC or laptop. The wireless station and authentication server then derive the same pairwise master key from the mk 
4. The AA server transmits the PMK to the access point. The wireless station and access point use the PMK to derive session keys, using either the WPA 4-way handshake or WPA3 SAE methods. 
The enterprise authentication method means that the access point does not need to store any user accounts or credentails. They can be help in a more secure location on the AAA server. Another 
