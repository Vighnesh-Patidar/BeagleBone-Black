# BeagleBone-Black
Completed build for Beagleboard Black using Yocto project and bitbake
To test :-
clone this repository in the directory where you have stored all the necessary layers.
```
git clone https://github.com/Vighnesh-Patidar/BeagleBone-Black/
```
dependent layers
poky:-
```
git clone git://git.yoctoproject.org/poky/
```
Possible problems:-
The layer for this build is cloned from dunfell branch of the Yocto project. It might cause a compatibility issue. If that happens checkout with dunfell branch and you will be fine.
```
git checkout dunfell
```
 The future builds in this repo will be using kirkstone as it is a newer branch with Long term support.
 This file contains the image obtained after parsing the layers with bitbake, you can just flash it on a partitioned SD card and it will be able to just bootup a beaglebone.
This repo also contains some embedded repos (sorry) so the clone of the outer repo will not be able to obtain it. The embedded repos belong to directory tmp/work-shared/beaglebone-yocto/kernel-source
so to add these repos too, either clone the whole list or .... idk or what.
navigate to the directory
```
git submodule add <url> tmp/work-shared/beaglebone-yocto/kernel-source
```
clone
```
git clone <URLs of listed files>

 tmp/work/all-poky-linux/update-rc.d/0.8-r0/git
 tmp/work/beaglebone_yocto-poky-linux-gnueabi/linux-yocto/5.4.58+gitAUTOINC+25f38de25d_706efec4c1-r0/kernel-meta
 tmp/work/beaglebone_yocto-poky-linux-gnueabi/u-boot/1_2020.01-r0/git
 tmp/work/cortexa8hf-neon-poky-linux-gnueabi/binutils/2.34-r0/git
 tmp/work/cortexa8hf-neon-poky-linux-gnueabi/btrfs-tools/5.4.1-r0/git
 tmp/work/cortexa8hf-neon-poky-linux-gnueabi/e2fsprogs/1.45.7-r0/git
 tmp/work/cortexa8hf-neon-poky-linux-gnueabi/expat/2.2.9-r0/git
 tmp/work/cortexa8hf-neon-poky-linux-gnueabi/glibc/2.31+gitAUTOINC+2d4f26e5cf-r0/git
 tmp/work/cortexa8hf-neon-poky-linux-gnueabi/gnome-desktop-testing/2018.1-r0/git
 tmp/work/cortexa8hf-neon-poky-linux-gnueabi/gnu-config/20200117+gitAUTOINC+5256817ace-r0/git
 tmp/work/cortexa8hf-neon-poky-linux-gnueabi/kmod/26-r0/git
 tmp/work/cortexa8hf-neon-poky-linux-gnueabi/libnsl2/1.2.0+gitAUTOINC+4a062cf418-r0/git
 tmp/work/cortexa8hf-neon-poky-linux-gnueabi/libxcrypt/4.4.15-r0/git
 tmp/work/cortexa8hf-neon-poky-linux-gnueabi/ncurses/6.2-r0/git
 tmp/work/cortexa8hf-neon-poky-linux-gnueabi/pkgconfig/0.29.2+gitAUTOINC+edf8e6f0ea-r0/git
 tmp/work/cortexa8hf-neon-poky-linux-gnueabi/procps/3.3.16-r0/git
 tmp/work/cortexa8hf-neon-poky-linux-gnueabi/ptest-runner/2.4.0+gitAUTOINC+834670317b-r0/git
 tmp/work/cortexa8hf-neon-poky-linux-gnueabi/shared-mime-info/1.15-r0/git
 tmp/work/x86_64-linux/binutils-cross-arm/2.34-r0/git
 tmp/work/x86_64-linux/binutils-native/2.34-r0/git
 tmp/work/x86_64-linux/bmap-tools-native/3.5+gitAUTOINC+db7087b883-r0/git
 tmp/work/x86_64-linux/btrfs-tools-native/5.4.1-r0/git
 tmp/work/x86_64-linux/createrepo-c-native/0.15.7-r0/git
 tmp/work/x86_64-linux/cross-localedef-native/2.31+gitAUTOINC+2d4f26e5cf_cd9f958c4c-r0/git
 tmp/work/x86_64-linux/dnf-native/4.2.2-r0/git
 tmp/work/x86_64-linux/dtc-native/1.6.0-r0/git
 tmp/work/x86_64-linux/e2fsprogs-native/1.45.7-r0/git
 tmp/work/x86_64-linux/expat-native/2.2.9-r0/git
 tmp/work/x86_64-linux/file-native/5.38-r0/git
 tmp/work/x86_64-linux/gnu-config-native/20200117+gitAUTOINC+5256817ace-r0/git
 tmp/work/x86_64-linux/kern-tools-native/0.2+gitAUTOINC+c66833e1ca-r12/git
 tmp/work/x86_64-linux/kmod-native/26-r0/git
 tmp/work/x86_64-linux/libcomps-native/0.1.15-r0/git
 tmp/work/x86_64-linux/libdnf-native/0.28.1-r0/git
 tmp/work/x86_64-linux/libmodulemd-v1-native/1.8.16-r0/git
 tmp/work/x86_64-linux/libnsl2-native/1.2.0+gitAUTOINC+4a062cf418-r0/git
 tmp/work/x86_64-linux/librepo-native/1.11.2-r0/git
 tmp/work/x86_64-linux/libsolv-native/0.7.10-r0/git
 tmp/work/x86_64-linux/lz4-native/1_1.9.2-r0/git
 tmp/work/x86_64-linux/mtd-utils-native/2.1.3-r0/git
 tmp/work/x86_64-linux/ncurses-native/6.2-r0/git
 tmp/work/x86_64-linux/ninja-native/1.10.0-r0/git
 tmp/work/x86_64-linux/pkgconfig-native/0.29.2+gitAUTOINC+edf8e6f0ea-r0/git
 tmp/work/x86_64-linux/prelink-native/1.0+gitAUTOINC+f9975537db-r0/git
 tmp/work/x86_64-linux/pseudo-native/1.9.0+gitAUTOINC+2b4b88eb51-r0/git
 tmp/work/x86_64-linux/rpm-native/1_4.14.2.1-r0/git
 tmp/work/x86_64-linux/shared-mime-info-native/1.15-r0/git
 tmp/work/x86_64-linux/squashfs-tools-native/4.4-r0/git
 tmp/work/x86_64-linux/update-rc.d-native/0.8-r0/git
```
