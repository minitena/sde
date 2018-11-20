# Introduction
Minitena is a minimal and optimized general purpose [Linux](https://www.kernel.org/) distribution that was made from scratch. It can run on x86_64, i586, ARM64, ARMv7, ARMv6, ARMv5TE, PowerPC, PowerPC64 (big and little endian), SPARC (64-bit), s390x and RISC V (64-bit) CPUs. Minitena aimed to be simple, flexible and easy for experienced Linux users. The code was written with KISS (Keep It Simple, Stupid) principle. That allows making the code readable and easy to maintain. The package manager of Minitena is `pacman` because it's simple. Minitena uses own framework to build itself which called ```wok```. [Access to Minitena's package collection](https://github.com/minitena/source/tree/master/packages). Please, help us to add this distribution to Distrowatch! [Recommend us on Distrowatch](https://distrowatch.com/dwres.php?waitingdistro=492&resource=links#new).

# Getting release
Actually, we don't make "releases" for now but you can download snapshots of this distribution. Image files with distribution placed [here](https://drive.google.com/drive/folders/17zdceh-52TVSXpH87ZZvUNV-u-mSq34a?usp=sharing).

# More information
## Made from scratch
Minitena is an independent Linux distribution. That allows making own package repository, optimize each package and get full control of dependency and package version control.

## Rolling release
Minitena doesn't use "fixed" as release system. Minitena is a rolling Linux distribution. That allows getting new packages and their version instead of awaiting a new release of the distribution.

## Hardened
Each package of Minitena was compiled with full RELRO support, Smash Stacking Protector (SSP). All libraries compiled with PIC (position-independent code) and executables with PIE (position-independent executable). That allows being protected from vulnerabilities.

## LibreSSL
Due to [heartbleed bug](https://en.wikipedia.org/wiki/Heartbleed) Minitena already comes with [LibreSSL](https://www.libressl.org/) instead of [OpenSSL](https://www.openssl.org/) because it's more secure and small.

## For experienced users
Minitena doesn't have any kind of installer. You need to write down commands manually. Also, it allows being flexible because it allows to build your own system and configure that for your needs.

## Support
We provide [wiki](https://github.com/minitena/source/wiki) also you will rather use [issues page](https://github.com/minitena/source/issues) to ask the community of this project to get help.

## IRC channel
To communicate with each other person who uses Minitena, we made IRC channel. Because this is easy way to discuss this project. IRC: #minitena on ```freenode.net```.

## Development
Minitena uses `git` as control version system. Main repository with source code hosts at GitHub. To enter to the repository with source code just [click here](https://github.com/minitena/source).
