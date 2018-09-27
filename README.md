# Introduction
Minitena is a minimal and optimized general purpose Linux distribution that was made from scratch. It can run on x86_64 or aarch64 CPUs. Minitena aimed to be simple, flexible and easy for experienced Linux users. The code was written with KISS (Keep It Simple, Stupid) principle. That allows making the code readable and easy to maintain. The package manager of Minitena is `pacman` because it's simple.

# More information
## Made from scratch
Minitena is an independent Linux distribution. That allows making own package repository, optimize each package and get full control of dependency and package version control.

## Rolling release
Minitena doesn't use "fixed" as release system. Minitena is a rolling Linux distribution. That allows getting new packages and their version instead of awaiting a new release of the distribution.

## Hardened
Each package of Minitena was compiled with full RELRO support, Smash Stacking Protector (SSP). All libraries compiled with PIC (position-independent code) and executables with PIE (position-independent executable). That allows being protected from vulnerabilities.

## For experienced users
Minitena doesn't have any kind of installer. You need to write down commands manually. Also, it allows being flexible because it allows to build your own system and configure that for your needs.

## Support
We provide [wiki](https://github.com/minitena/wiki/wiki) also you will rather use [issues page](https://github.com/minitena/issues/issues) to ask the community of this project to get help.
