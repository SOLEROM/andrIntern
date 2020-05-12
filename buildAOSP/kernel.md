# kernel

* The root of the kernel source checkout contains build/build.sh. The Android tree contains only prebuilt kernel binaries. 


## dw

```
repo init -u https://android.googlesource.com/kernel/manifest 
repo init -b common-android-mainline
repo sync

```

## Customizing build

* BUILD_CONFIG 	

```
Build config file to initialize the build environment from. 
The location is to be defined relative to the Repo root directory. 
Defaults to build.config.
Mandatory for common kernels. 	

BUILD_CONFIG=common/build.config.cuttlefish.x86_64
```

* OUT_DIR

```
Base output directory for the kernel build.

OUT_DIR=/path/to/my/out
```

* DIST_DIR 	

```
Base output directory for the kernel distribution.

OUT_DIR=/path/to/my/dist
```
* CC
 
```
Override compiler to be used. 
Falls back to the default compiler defined by build.config. 

CC=clang
```

* SKIP_MRPROPER

```
Skip make mrproper

SKIP_MRPROPER=1
```

* SKIP_DEFCONFIG

```
Skip make defconfig 

SKIP_DEFCONFIG=1
```


## build

```
build/build.sh

Mandatory for common kernels:
=============================
export BUILD_CONFIG=common/build.config.allmodconfig.arm
./build/build.sh
```

## output

* The kernel binary, modules, and corresponding image are located in the out/BRANCH/dist director


## run (1):Embedding into the Android image

* optinonA: Copy Image.lz4-dtb to the respective kernel binary location within the AOSP tree and rebuild the boot image.

* optionB: define the TARGET_PREBUILT_KERNEL variable while using make bootimage
* this varible is set up via device/common/populate-new-device.sh
* example:

```
export TARGET_PREBUILT_KERNEL=DIST_DIR/Image.lz4-dtb
```

## run (2):Flashing and booting kernels with fastboot

* boot the kernel without flashing:
* the kernel isn't actually flashed, and won't persist across a reboot

```
adb reboot bootloader
fastboot boot Image.lz4-dtb
```



