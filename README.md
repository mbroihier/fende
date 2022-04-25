# fende - file encryptor and decryptor

This repository contains a small python3 script that encrypts and decrypts files.  It is based on the work of Woody Pope (woody.pope@mailfence.com)  Woody's original work includes a GUI that I removed so that I could incorporate it into a mail client that could send and receive encrypted messages.

RSA is used to encrypt/decrypt a password/phrase that is then used for the AES algorithm to encrypt/decrypt a file.  The password/phrase can be stored with the encrypted message or put into its own file so that delivery of the message and the password/phrase can be handled independently.
# Setup

I'm running this on a Raspberry PI under Raspbian (buster).  You don't have to have a Raspberry PI or Raspbian.  This should run fine on most Debian Linux systems.

You will need git, python3, and pip3

From a bash shell:

1) git clone https://github.com/mbroihier/fende
2) cd fende
3) sudo pip3 install pillow
4) typing
   - ./fende
   - will display usage
