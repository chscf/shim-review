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
The company is called cpsd (https://www.cpsd.at/), located in Austria. We're working in the field of IT security, with our main focus on full disk encryption.

-------------------------------------------------------------------------------
What product or service is this for:
-------------------------------------------------------------------------------
The pre-boot authentication environment for our company's Full Disk Encryption CryptoPro Secure Disk (see https://www.cpsd.at/)

-------------------------------------------------------------------------------
What's the justification that this really does need to be signed for the whole world to be able to boot it:
-------------------------------------------------------------------------------
Because we want the whole world to use our product ;)

-------------------------------------------------------------------------------
Who is the primary contact for security updates, etc.
-------------------------------------------------------------------------------
- Name: Christian Schaubschläger
- Position: Senior Developer, R&D
- Email address: christian.schaubschlaeger@secofact.at
- PGP key, signed by the other security contacts, and preferably also with signatures that are reasonably well known in the linux community:

-------------------------------------------------------------------------------
Who is the secondary contact for security updates, etc.
-------------------------------------------------------------------------------
- Name: Robert Duda
- Position: CTO
- Email address: robert.duda@secofact.at
- PGP key, signed by the other security contacts, and preferably also with signatures that are reasonably well known in the linux community:

-------------------------------------------------------------------------------
What upstream shim tag is this starting from:
-------------------------------------------------------------------------------
https://github.com/rhboot/shim/releases/tag/15

-------------------------------------------------------------------------------
URL for a repo that contains the exact code which was built to get this binary:
-------------------------------------------------------------------------------
https://github.com/rhboot/shim/releases/tag/15

-------------------------------------------------------------------------------
What patches are being applied and why:
-------------------------------------------------------------------------------
https://github.com/chscf/shim-review/blob/master/shim-15-SCF.patch
This patch only changes some paths in Make.defaults; without that shim-15 doesn't compile on Ubuntu 18.04.

-------------------------------------------------------------------------------
What OS and toolchain must we use to reproduce this build?  Include where to find it, etc.  We're going to try to reproduce your build as close as possible to verify that it's really a build of the source tree you tell us it is, so these need to be fairly thorough. At the very least include the specific versions of gcc, binutils, and gnu-efi which were used, and where to find those binaries.
-------------------------------------------------------------------------------
Build environment is Ubuntu 18.04 x64 with all available security updates.
gcc 7.3.0
binutils 2.30
gnu-efi 3.0.8

-------------------------------------------------------------------------------
Which files in this repo are the logs for your build?   This should include logs for creating the buildroots, applying patches, doing the build, creating the archives, etc.
-------------------------------------------------------------------------------
https://github.com/chscf/shim-review/blob/master/shim-15-SCF-build.log

-------------------------------------------------------------------------------
Add any additional information you think we may need to validate this shim
-------------------------------------------------------------------------------
N/A
