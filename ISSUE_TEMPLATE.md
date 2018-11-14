Make sure you have provided the following information:

 - [ ] link to your code branch cloned from rhboot/shim-review in the form user/repo@tag
 - [X] completed README.md file with the necessary information
 - [X] shim.efi to be signed
 - [X] public portion of your certificate embedded in shim (the file passed to VENDOR_CERT_FILE)
 - [X] any extra patches to shim via your own git tree or as files
 - [ ] any extra patches to grub via your own git tree or as files
 - [X] build logs


###### What organization or people are asking to have this signed:
The company is called cpsd (https://www.cpsd.at/)

###### What product or service is this for:
The pre-boot authentication environment for our company's Full Disk Encryption CryptoPro Secure Disk (see https://www.cpsd.at/)

###### What is the origin and full version number of your shim?
shim-15

###### What's the justification that this really does need to be signed for the whole world to be able to boot it:
Because we want the whole world to use our product ;)

###### How do you manage and protect the keys used in your SHIM?
The private key is on a FIPS 140-2 token.

###### Do you use EV certificates as embedded certificates in the SHIM?
Yes

###### What is the origin and full version number of your bootloader (GRUB or other)?
see below

###### If your SHIM launches any other components, please provide further details on what is launched
shim loads a self-developed boot component which does all further authorization/os loading stuff.

###### How do the launched components prevent execution of unauthenticated code?
All boot components must be signed

###### Does your SHIM load any loaders that support loading unsigned kernels (e.g. GRUB)?
No

###### What kernel are you using? Which patches does it includes to enforce Secure Boot?
N/A

###### What changes were made since your SHIM was last signed?
upgraded from shim-0.8 to shim-15

###### What is the hash of your final SHIM binary?
44ed00a46d11e631f334f8cfc3747b02b53e0e48b89e9641a0e4a1775f3121e1  shim-15-SCF-unsigned.efi
