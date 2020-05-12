# flash HW

## (1) connect


## (2) Unlocking the bootloader

* devices released since 2014 (starting with Nexus 6 and Nexus 9) have factory-reset protection and require a multi-step process to unlock the bootloader.

```
(1) on the device:

    In Settings, tap About phone, then tap Build number seven (7) times.
    When you see the message You are a developer, tap the back button.
    Tap Developer options and enable OEM unlocking and USB debugging

```

```
(2)

fastboot flashing unlock
```

## (3) fastboot

* cold boot of a device, use the following key combinations

```
Nexus 6P        angler  Press and hold Volume Down, then press and hold Power.
```

or

* adb reboot bootloader


## (4) Flash

```
fastboot flashall -w
	// -w option wipes the /data partition on the device
```


