# Cryptography



## DES

The usable class is DES to be used. There is no padding, so the text needs to be of multiple of 8 bit and secret key is of 8 bit. If the secret key is more than 8 bit then it will be trimmed. <br>
In order to use padding, use it as:

```
from cryptDES import des

key = "password"
text= raw_input("Enter the plain text: ")
d = des()
ciphered = d.encrypt(key,text,padding=True) #Or just True in third arg
plain = d.decrypt(key,ciphered,padding=True)
print "Cipher Text: %r" % ciphered
print "Decrypted Text: ", plain

```