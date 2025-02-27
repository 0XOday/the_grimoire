Kerckoffs's Principles 
	1. The system must substantially, if not mathematically,undecipherable
	2. The system must not require secrecy; even if stolen by the enemy, the system should remain secure.
	3. the keys must be easy to communicate and remember without written notes, and they must be easy to change or modify to use with different participants.
	4. The system ought to be compatible with communication via telegraph.
	5. The system must be portable, and its use must not require more than one person.
	6. Finally, the system must be easy to use, requiring neither complex thinking nor the knowledge of a long series of rules. 

## One-Time pads
Vernam cipher, is an unbreakable cipher when used properly.
To use it crate two copies of the same pad of paper containing a completely random set of numbers, known as *shifts.* you give one copy to each party. 

## Symmetric and Asymmetric Cryptography

Symmetric Cryptography - Known as private key cryptography,*symmetric key cryptography* uses a single key to both encrypt the plaintext and decrypt the ciphertext. You must share the key between the sender and receiver. The fact that you must share a single key among all users of the system is one of the weaknesses of symmetric key Cryptography.

## Block Vs. Stream Ciphers 

- Block cipher takes a predetermind number of bits knows as a block and encrypts that block. Block typically have have 64 bits but can change based on what algorithm used.
- A stream cipher encrypts each bit in the plaintext message one bit at a time. you can make a block cipher act as a stream cipher by setting the block size to one bit.
- Block ciphers are often slower than stream ciphers than stream ciphers but offer more versatile  
- Block ciphers are more prone to errors. If a block get corrupted during the encryption processes you loose a chunk of data
- Stream cipher an error will only corrupt a single bit.
Block mode defines the specific processes and operations that the cipher uses.

Typically block ciphers work better with messages where sizes are fixed 
Stream ciphers work better when you don't know the size and transmit and receive over a network 

## Symmetric Key Algorithms 

*DES* is a blovk cipher that uses a 56-bit key 

## Asymmetric Cryptography 

Asymmetric Cryptography has a public key and a private key 

Elliptic curve Cryptography can use short keys while maintaining a higher Cryptography strength than many other types of algorithms. Its fast and efficient. Secure hash algorithm 2 (SHA-2) and Elliptic curve Digital Signature Algorithm (ECDSA) Uses ECC. 

Many protocols and applications are based on asymmetric cryptography. PGP SSL TLS and some VoIP


## Hash Functions 

Hash Functions represent a third type of modern cryptography which is called key less cryptography.
Hash functions or message digest convert plaintext into largely unique and fixed-length value 

It is theoretically possible to engineer a matching hash for two different sets of data called a collision. This only happens if you are using a broken hashing algo like MD5 and SHA-1 

We use sha-2 and sha-3 MD-2,MD4 and RACE

## Digital signatures 

Another way to use asymmetric algorithms and their associated public and private keys are digital signature.

A digital signature allows you to sign a message so that others can detect any change to the message after you've sent it. 

## Certificates 

in addition to hashes and digital signatures. You can use Certificates to sign your messages. Digital signatures link a public to an individual by validating that key belongs to the proper owner. 
you typically create a certificate by taking the public key and identifying information such as a name and address and having them signed by a trusted entity that handles digital certificates, called *certificate authority*

A certificate authority is the entity that issues certificates. It acts as a trusted third party to both sides of the transactions that involve certificates by singing the certificate to begin with and later verifying that it is still valid.

one known certificate authority is VeriSign


## Protecting data at rest in motion and in use.
These are the three main categories that 


Note from wife look at FIPS 

Terminal talk z 16 implementation 

Correct: ECC

It’s an example of public key cryptography based on elliptic curves over infinite fields.