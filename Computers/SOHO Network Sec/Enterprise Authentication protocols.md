The main problems with personal modes of authentication are that distribution of the passphrase cannot be secured properly and that the access point administrator may choose an unsecure passphrase. Personal authentication also fails to provide accounting because all users share the same credential.

As an alternative to personal authentication, WPA's 802.1x enterprise authentication method implements the Extensible Authentication Protocol (EAP). EAP allows the use of different mechanisms to authenticate against a network directory. 802.1x defines the use of EAP over Wireless (EAPoW) to allow an access point to forward authentication data without allowing any other type of network access. it is configured by selecting WPA2-Enterprise or WPA3-Enterprise as the security method on the access point.

Enterprise authentication uses the following general workflow:
1. When a wireless station (a supplicant) requests an association, the AP enables the channel for EAPoW traffic only
2. is passes the credentials submitted by the supplicant to an Authentication, Authorization, and Accounting (AAA) server on the wired network for validation. The AAA server determines weather to accept the credential.
3. When the use has been authenticated, the AAA server transmits a master key (MK) to the wireless PC or laptop. The wireless station and authentication server then derive the same pairwise master key from the mk 
4. The AA server transmits the PMK to the access point. The wireless station and access point use the PMK to derive session keys, using either the WPA 4-way handshake or WPA3 SAE methods. 
The enterprise authentication method means that the access point does not need to store any user accounts or credentails. They can be help in a more secure location on the AAA server. Another advantage of EAP is support for more advanced authentication methods than simple usernames and passwords. Strong EAP methods use a digital certificate on the server and/or client machines. These certificates allow the machines to establish a trust relationship and create a secure tunnel to transmit the user credential or to perform smart card authentication without a user password. This means the system is using strong multifactor authentication.

For example, EAP with Transport Layer Security (EAP-TLS) is one of the strongest types of multifactor authentication : 

1. Both the sever and the wireless supplicant are issued with an encryption key pair and digital certificate.
2. On the wireless device, the private key is stored securely in a trusted platform module (TMP) or USB key. The user must authenticate with the device using a PIN, password, or bio  gesture to allow use of the key. This is the fist factor.
3. When the device associates with the network and starts an EAP session, the server sends a digital signature handshake and its certificate.
4. the supplicant validates the signature and certificate and if trusted, sends its own handshake and certificate. This is the second factor.
5. The server checks the supplicants handshake and certificate and authenticates it if trusted
Note : Other methods of EAP use a certificate on the AAA server only. The AAA server uses the cert to create an encrypted tunnel for the supplicant to send a username/password securely 
