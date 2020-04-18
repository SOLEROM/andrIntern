

```
Trying to apply a .zip from stock recovery and when I select
"Apply update from SD card"

I get

"Couldn't mount /sdcard
Installation aborted

```

You can't flash a .zip from stock recovery. You can only adb sideload an OTA. If you want to flash a .zip, you'll have to use TWRP. 

you can boot TWRP from fastboot without installing it to flash your .zip


# get twrp

* https://www.xda-developers.com/how-to-install-twrp/
* https://twrp.me/huawei/huaweinexus6p.html

## boot

adb reboot bootloader
fastboot boot twrp-3.3.1-0-angler.img



## install twrp

adb reboot bootloader
fastboot flash recovery twrp-3.3.1-0-angler.img 
fastboot reboot

