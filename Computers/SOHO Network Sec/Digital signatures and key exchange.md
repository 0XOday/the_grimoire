Cryptographic hashes and encryption ciphers have different roles in achieving the information security goals of confidentiality, integrity , and availability. Often two or more of these three different types are used together in the same product or technology.

The main drawback of asymmetric encryption is that a message cannot be larger than the key size. To encrypt a large file, it would have to be split into thousands of smaller pieces. Consequently, asymmetric encryption is used with hashes and symmetric encryption keys to implement various kinds of security products and protocols. 

### Digital Signatures

A digital signature proves that a message or digital certificate has not been altered or spoofed. The sender computes a cryptographic hash of a message, encrypts the hash with his or her private key, and attaches the output to the message as a digital signature. When the recipient receives the message, she or he can decrypt the signature using the public key to obtain the sender’s hash. The recipient then computes her or his own hash of the message and compares the two values to confirm they match.

### Key Exchange

Key exchange allows two hosts to know the same symmetric encryption key without any other host finding out what it is. A symmetric cipher is much faster than an asymmetric one, so it is often used to protect the actual data exchange in a session. Asymmetric encryption only operates efficiently on data that is smaller than the key size. This makes it well-suited to encrypt and exchange symmetric cipher keys.

The sender uses the recipient’s public key to encrypt a secret key. The recipient uses the private key to retrieve the secret key and then uses the secret key to decrypt whatever data message was transmitted by the sender. In this context, the symmetric cipher secret key is also referred to as a session key. If it is changed often, it is also referred to as an ephemeral key.

