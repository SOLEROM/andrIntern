
# dw

repo init -u https://android.googlesource.com/platform/manifest -b XXXX
			XXXX
OPM7.181205.001 	android-8.1.0_r52 	Oreo 	Nexus 5X, Nexus 6P 	2018-12-05
repo sync

# build for the emulator

. build/envsetup.sh
lunch aosp_arm-eng
m

# out

```
out/
|-- Android.mk
|-- CaseCheck.txt
|-- CleanSpec.mk
|-- build-aosp_arm.ninja
|-- build.trace.gz
|-- build_date.txt
|-- build_number.txt
|-- casecheck.txt
|-- combined-aosp_arm.ninja
|-- env-aosp_arm.sh
|-- host
|-- microfactory_Linux
|-- ninja-aosp_arm.sh
|-- ninja_build
|-- soong
|-- soong.log
|-- soong_ui
`-- target


```


lunch sdk_phone_x86_64

m
============================================
PLATFORM_VERSION_CODENAME=REL
PLATFORM_VERSION=8.1.0
TARGET_PRODUCT=sdk_phone_x86_64
TARGET_BUILD_VARIANT=eng
TARGET_BUILD_TYPE=release
TARGET_ARCH=x86_64
TARGET_ARCH_VARIANT=x86_64
TARGET_2ND_ARCH=x86
TARGET_2ND_ARCH_VARIANT=x86_64
HOST_ARCH=x86_64
HOST_2ND_ARCH=x86
HOST_OS=linux
HOST_OS_EXTRA=Linux-5.0.0-23-generic-x86_64-with-Ubuntu-16.04-xenial
HOST_CROSS_OS=windows
HOST_CROSS_ARCH=x86
HOST_CROSS_2ND_ARCH=x86_64
HOST_BUILD_TYPE=release
BUILD_ID=OPM7.181205.001
OUT_DIR=out
============================================



