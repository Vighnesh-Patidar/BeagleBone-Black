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
