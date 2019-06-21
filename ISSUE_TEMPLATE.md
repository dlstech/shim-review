Make sure you have provided the following information:

 - [x] link to your code branch cloned from rhboot/shim-review in the form user/repo@tag
 - [x] completed README.md file with the necessary information
 - [x] shim.efi to be signed
 - [x] public portion of your certificate embedded in shim (the file passed to VENDOR_CERT_FILE)
 - [x] any extra patches to shim via your own git tree or as files
 - [x] any extra patches to grub via your own git tree or as files
 - [x] build logs


###### What organization or people are asking to have this signed:
`DLS Technology Corporation`

###### What product or service is this for:
`vKey`
https://vkey.ca/

###### What is the origin and full version number of your shim?
`We are using shim-15 commit a4a1fbe728c9545fc5647129df0cf1593b953bec.`

###### What's the justification that this really does need to be signed for the whole world to be able to boot it:
`vKey is a bootable remote and local access security solution. vKey can be deployed in minutes and is easy to use. It was designed to transform any computer or IT device (tablet, phone, surface, etc.) into a clean, highly secure, self-contained work environment – virtually impossible to compromise. Ideal for any remote or local end-user work environment.`

`One of our primary goals is to achieve cross-compatibility for all devices, regardless of their configurations. As a result, we need to have the flexibility to control the boot process.`

###### How do you manage and protect the keys used in your SHIM?
`The private key resides on a DigiCert certified eToken, which remains locked away.`

###### Do you use EV certificates as embedded certificates in the SHIM?
`Yes we use a DigiCert EV Code Signing Certificate emdedded in our SHIM.`

###### What is the origin and full version number of your bootloader (GRUB or other)?
`grub2-2.02-0.2.10.el7`

###### If your SHIM launches any other components, please provide further details on what is launched
`Our SHIM does not launch any other components.`

###### How do the launched components prevent execution of unauthenticated code?
`GRUB only launches kernels signed with our eToken. It does not launch any other code.`

###### Does your SHIM load any loaders that support loading unsigned kernels (e.g. GRUB)?
`Our SHIM loads GRUB.`

###### What kernel are you using? Which patches does it includes to enforce Secure Boot?
`We are using kernel 5.1.12-1.el7.x86_64 from ELRepo for CentOS 7.`

`Although no additional patches are implemented; vKey is a secure, encrypted operating system that prevents users from modifying any part of the system.`

###### What changes were made since your SHIM was last signed?
`This is our first submission.`

###### What is the hash of your final SHIM binary?
SHA256:
`41e33840ad3d48f3a90b2db24f8d6e0f4d469fcf4ce6b957b81c542e2e8b66f0  shimx64.efi`
