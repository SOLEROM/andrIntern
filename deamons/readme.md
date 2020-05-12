

* The services are mostly strewn in /init.rc
* The "core" services start first, followed by the "main" ones.
* The rc defines a "late_start" class, for services which depend on the /data partition


## Core Services
* adbd
* [servicemanager](servicemanager.md)
* healthd
* lmkd
* logd
* vold

## Network Services
* netd
* mdnsd
* mtpd
* racoon
* rild

## Graphics and Media Services
* surfaceflinger
* bootanimation
* mediaserver
* drmserver


## Other Services
* installd
* debuggerd
* sdcard
* zygote
* [system_server](framework/systemServer.md) 
