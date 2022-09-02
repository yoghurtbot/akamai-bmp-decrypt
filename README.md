# Akamai BMP Decrypt

The format of an Akamai Mobile SDK (BMP) sensor string is (depending on version);
> 1,a,\<Encrypted AES Key\>,\<Encrypted HMAC SHA-256 Key\>$\<Sensor\>\$<Timestamps\>

The AES Key (used to encrypt the sensor) and HMAC key are encrypted using an RSA public key and the sensor is encrypted using AES-128-CBC.

It is not possible to decrypt the AES or HMAC key without the matching RSA private key. Therefore, to decrypt the sensor, you must know the matching unencrypted AES key used for encryption.

 1. The private key to decrypt the encrypted AES Key in the sensor string; or
 2. The unencrypted AES 

It's highly unlikely you have the Akamai private key, so you'd need the unencrypted key to use this example.

You can use this repository to test your encrypted sensors :)
