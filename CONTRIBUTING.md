# Contributing

## Introduction
Welcome to this page, Minitena's contributors! I'm [protonesso](https://github.com/protonesso) the creator of Minitena. At this page, you can find information about Minitena contribution.

## Preparing


### Building tools for ```wok```
```wok``` is a framework that builds Minitena. It can build cross-toolchain, chroot system, tarball and *.iso image. ```wok``` uses ```pacman``` as package manager to manipulate chroot and toolchain packages on host system and native packages on the target system. First, we'll install host packages.

Debian or Ubuntu (and derivatives):
```
apt-get install build-essential gcc-multilib g++-multilib m4 wget gawk bc bison flex texinfo python3 python perl libtool autoconf automake autopoint gperf bsdtar libarchive-dev fakeroot xorriso curl syslinux-utils -y
```
Arch Linux (and derivatives):
```
pacman -S base-devel syslinux xorriso
```
Minitena:
```
pacman -S meta-base syslinux xorriso
```
Building pacman:
```
cd /tmp
wget https://sources.archlinux.org/other/pacman/pacman-5.1.1.tar.gz
tar -xvf pacman-5.1.1.tar.gz
cd pacman-5.1.1
sed -i -e '/x-cpio/s@)@|*application/x-empty*)@' scripts/makepkg.sh.in
sed -i -e 's/EUID == 0/EUID == -1/' scripts/makepkg.sh.in
autoreconf -vif
./configure \
--prefix=/dedicated/dir \
--with-scriptlet-shell=/usr/bin/bash \
--disable-doc \
--disable-nls \
DUFLAGS="-sk" \
SEDINPLACEFLAGS="-i"
make -j $(expr $(nproc) + 1)
make install -j $(expr $(nproc) + 1)
```
After building ```pacman``` you need to add path to /dedicated/dir/bin in your bashrc


### Building Minitena
The first step is building chroot system for Minitena. Minitena supports 4 CPU architectures:
```
x86_64  - 64-bit x86 (AMD64/EMT64)
i586    - 32-bit x86 (for Pentium-compatible and higher)
aarch64 - 64-bit ARM
arm     - 32-bit ARM (version 7)
```
Building chroot system:
```
sudo BARCH=[CPU architecture] MKJOBS=[number of CPU cores (if you don't want to specify that wok will use all of your CPU cores!)] ./wok bootstrap
```
**WARNING: If you want to build ARM system on x86 you should use enter-chroot-binfmt!**
Then we need to enter chroot:
```
sudo BARCH=[CPU architecture] ./wok enter-chroot
```
Let's build final system:
```
wok final-system
```
After that all you can build *.iso image (x86_64 and i586 only):
```
sudo BARCH=[CPU architecture] ./wok image
```
And *.tar.xz tarball (all architectures)
```
sudo BARCH=[CPU architecture] ./wok tarball
```


## Making packages
TODO
