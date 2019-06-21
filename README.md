This repo is for review of requests for signing shim.  To create a request for review:

- clone this repo
- edit the template below
- add the shim.efi to be signed
- add build logs
- commit all of that
- tag it with a tag of the form "myorg-shim-arch-YYYYMMDD"
- push that to github
- file an issue at https://github.com/rhboot/shim-review/issues with a link to your branch

Note that we really only have experience with using grub2 on Linux, so asking
us to endorse anything else for signing is going to require some convincing on
your part.

Here's the template:

-------------------------------------------------------------------------------
What organization or people are asking to have this signed:
-------------------------------------------------------------------------------
DLS Technology Corporation

-------------------------------------------------------------------------------
What product or service is this for:
-------------------------------------------------------------------------------
vKey: https://vkey.ca/


-------------------------------------------------------------------------------
What's the justification that this really does need to be signed for the whole world to be able to boot it:
-------------------------------------------------------------------------------
vKey is a bootable remote and local access security solution. vKey can be deployed in minutes and is easy to use. It was designed to transform any computer or IT device (tablet, phone, surface, etc.) into a clean, highly secure, self-contained work environment – virtually impossible to compromise. Ideal for any remote or local end-user work environment.

One of our primary goals is to achieve cross-compatibility for all devices, regardless of their configurations. As a result, we need to have the flexibility to control the boot process.

-------------------------------------------------------------------------------
Who is the primary contact for security updates, etc.
-------------------------------------------------------------------------------
- Name: Jordan Kurosky
- Position: Technology Manager
- Email address: jkurosky@dlstech.com
- PGP:  

-------------------------------------------------------------------------------
Who is the secondary contact for security updates, etc.
-------------------------------------------------------------------------------
- Name: Sibyl Weng
- Position: Operations Manager
- Email address: sweng@dlstech.com
- PGP:

-------------------------------------------------------------------------------
What upstream shim tag is this starting from:
-------------------------------------------------------------------------------
[ADD TAG]

-------------------------------------------------------------------------------
URL for a repo that contains the exact code which was built to get this binary:
-------------------------------------------------------------------------------
https://github.com/rhboot/shim/tree/a4a1fbe728c9545fc5647129df0cf1593b953bec

-------------------------------------------------------------------------------
What patches are being applied and why:
-------------------------------------------------------------------------------
There are no patches being applied.

-------------------------------------------------------------------------------
What OS and toolchain must we use to reproduce this build?  Include where to find it, etc.  We're going to try to reproduce your build as close as possible to verify that it's really a build of the source tree you tell us it is, so these need to be fairly thorough. At the very least include the specific versions of gcc, binutils, and gnu-efi which were used, and where to find those binaries.
-------------------------------------------------------------------------------
The SHIM was built using CentOS-3.10.0-957.21.2.el7.x86_64.
http://isoredirect.centos.org/centos/7/isos/x86_64/CentOS-7-x86_64-Minimal-1810.iso

gcc: 4.8.5 20150623 (Red Hat 4.8.5-36) (GCC)
http://mirror.centos.org/centos/7/os/x86_64/Packages/gcc-4.8.5-36.el7.x86_64.rpm

binutils: 2.27-34.base.el7
http://mirror.centos.org/centos/7/os/x86_64/Packages/binutils-2.27-34.base.el7.x86_64.rpm

gnu-efi.x86_64: 3.0.8-2.el7
http://mirror.centos.org/centos/7/os/x86_64/Packages/gnu-efi-3.0.8-2.el7.x86_64.rpm

gnu-efi-devel.x86_64: 3.0.8-2.el7
http://mirror.centos.org/centos/7/os/x86_64/Packages/gnu-efi-devel-3.0.8-2.el7.x86_64.rpm

-------------------------------------------------------------------------------
Which files in this repo are the logs for your build?   This should include logs for creating the buildroots, applying patches, doing the build, creating the archives, etc.
-------------------------------------------------------------------------------
We have not modified any of the files from the SHIM repository.
[Link build.log here]

-------------------------------------------------------------------------------
Add any additional information you think we may need to validate this shim
-------------------------------------------------------------------------------
We have not modified any of the files from the SHIM repository.