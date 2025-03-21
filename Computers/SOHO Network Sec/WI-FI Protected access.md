wireless LANs require careful configuration to make the connection and transmissions over the link secure. The main problem with wireless is that because it is unguided, there is no way to prevent anything within range from listening to the signals. if the wireless traffic is unencrypted, this could allow the interception of data or the unauthorized use of the network.

*Temporal Key integrity protocol*

The first version of WI-FI Protected Access (WPA) was designed to fix critical vulnerabilities in the earlier wired equivalent privacy (WEP) standard. Like WEP version 1 of WPA uses the RC4 symmetric cipher to encrypt traffic but adds a mechanism called Temporal Key Protocol (TKIP) to try to mitigate the various attacks against WEP that had been developed.

*WPA2*
Neither WEP nor the original WPA version are considered secure enough for continued use. Even with TKIP,WPA is vulnerable to various types of replay attack that aim to recover the encryption key. WPA2 uses the Advanced Encryption Standard (AES) cipher deployed within the Counter Mode with Cipher Block Chaining Message Authentication Code Protocol (CCMP), AES replaces RC4 and CCMP replaces TKIP,CCMP provides authenticated encryption, which is designed to make replay attacks harder.

Note : Some access points allows WPA2 to be used in WPA2-TKIP or WPA2-TKIP+AES compatibility mode. This provides support for legacy clients at the expense of weakening the security. it is better to select WPA2-AES

*WPA3*
Weaknesses have also been found in WPA2, however, which has led to its intended replacement by WPA3. The main features of WPA3 are as follows:

* Simultaneous Authentication of Equals ( SAE ) - WPA2 personal authentication uses a 4-way handshake with a preshared key (PSK) to allow a station to associate with an access point, authenticate its credential, and exchange a key to use for data encryption. The WPA2=PSK mechanism is vulnerable to manipulations that allow a threat actor to recover the key. WPA3 replaces WPA2-PSK with the more secure WPA3-SAE mechanism.
* Updated cryptographic protocols - WPA3 replaces AES CCMP with the stronger AES Galois Counter Mode Protocol (GCMP) mode of operation
* Protected management frames - management frames are used for association and authentication and disassociation and deauthentication messages between stations and access points as devies join and leave the network. These frames can be spoofed and misused in various ways under WPA and WPA2. WPA3 mandates use of encryption for these frames to protect against key recovery attacks and Dos attacks that for stations to disconnect.
* WI-FI Enhanced Open - An open is one with no passphrase. Any station can join the network. in WPA2, This also means that all traffic is unencrypted. WPA3 encrypts this traffic. This means that any station can still join the network, but traffic is protected against sniffing.