# RSA_Encryption
This program does simple RSA encryption

from Wiki:
-----------------------------------------
RSA is the algorithm used by modern computers to encrypt and decrypt messages. It is an asymmetric cryptographic algorithm. Asymmetric means that there are two different keys. This is also called public key cryptography, because one of them can be given to everyone. The other key must be kept private.

![alt tag](https://raw.githubusercontent.com/Denisolt/RSA_Encryption/master/img.png)

Important
-----------------------------------------
Compilation:  javac RSA.java
Execution:    java RSA n

Generate an N-bit public and private RSA key and use to encrypt
and decrypt a random message of size n/2.

% java RSA 50
public  = 65537

private = 553699199426609

modulus = 825641896390631

message   = 48194775244950

encrpyted = 321340212160104

decrypted = 48194775244950

Known bugs (not addressed for simplicity)
-----------------------------------------
It could be the case that the message >= modulus. To avoid, use
a do-while loop to generate key until modulus happen to be exactly N bits.

It's possible that gcd(phi, e) != 1 in which case
the key generation fails. This will only happen if phi is a
multiple of 65537. To avoid, use a do-while loop to generate
keys until the gcd is 1.
