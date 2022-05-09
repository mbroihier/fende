# fende - file encryptor and decryptor

This repository contains a small python3 script that encrypts and decrypts files.  It is based on the work of Woody Pope (woody.pope@mailfence.com)  Woody's original work includes a GUI that I removed so that I could incorporate it into a mail client that could send and receive encrypted messages.  I have added two scripts. One encrypts and sends files as email, and one that receives and decrypts files.

RSA is used to encrypt/decrypt a password/phrase that is then used for the AES algorithm to encrypt/decrypt a file.  The password/phrase can be stored with the encrypted message or put into its own file so that delivery of the message and the password/phrase can be handled independently.

# Setup

I'm running this on a Raspberry PI under Raspbian (buster).  You don't have to have a Raspberry PI or Raspbian.  This should run fine on most Debian Linux systems.

You will need git, python3, and pip3

From a bash shell:

1) git clone https://github.com/mbroihier/fende
2) cd fende
3) sudo pip3 install pillow
4) typing
   - ./fende or ./fendeMessSend or ./fendeMessReceive will display usage messages

# Notes
Files to be encrypted are treated as binary.

Public and private keys are created with fende using the --generateKeys option.  These keys are needed for encrypting and decrypting the files.

To use the email features, the configure.py file must be filled out to specify the specific IMAPS and SMTPS servers you are going to use and to provide login credentials.  When sending mail, the public key of the receiver is necessary for encrypting the message.  This, of course, means that you must exchange public keys with anyone who will receive your email. 
