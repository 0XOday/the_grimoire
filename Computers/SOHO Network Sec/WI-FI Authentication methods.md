WI-FI authentication comes in three types : open , personal , adn enterprise. Within the personal authentication category, there are two methodsL WPA2 -pre-shared key (PSK) authentication and WPA3 simultaneous authentication of equals (SAE)

*WPA2 Pre-Shared Key Authentication*
in WPA, *pre-shared key* (PSK) authentication uses a passphrase to generate the key that is used to encrypt communications. it is also referred to as group authentication because a group of users shares the same passphrase. When the access point is set to WPA2-PSK mode, the administrator configures a passphrase consisting of 8 to 63 characters. This is converted to a type of hash value, referred to as the pairwise master key (PMK) The same secret must be configured on each station that joins the network. The PMK is used as part WPA2's 4-way handshake to derive various session keys.

All types of PSK authentication have been shown to be vulnerable to attacks that attempt to recover the passphrase. The passphrase must be at least 14 characters long to try to mitigate risks from cracking.

WPA3 Personal authentication
While WPA3 still uses passphrase-based group authentication of stations in personal mode, it changes the method by which the secret used to agree session keys is generated. In WPA3, the simultaneous authentication of equals (SAE) protocol replaces the PSK mechanism.