# lunch


* complete build for the emulator, with all debugging enabled:
```
lunch aosp_arm-eng
```

## lunch param style:

All build targets take the form BUILD-BUILDTYPE, where the BUILD is a codename referring to the particular feature combination. The BUILDTYPE is one of the following.

```
user 	Limited access; suited for production
userdebug 	Like user but with root access and debug capability; preferred for debugging
eng 	Development configuration with additional debugging tools
```

## Selecting a device build

```
Device 	Code name 	Build configuration
Pixel 3a XL 	bonito 	aosp_bonito-userdebug
Pixel 3a 	sargo 	aosp_sargo-userdebug
Pixel 3 XL 	crosshatch 	aosp_crosshatch-userdebug
Pixel 3 	blueline 	aosp_blueline-userdebug
Pixel 2 XL 	taimen 	aosp_taimen-userdebug
Pixel 2 	walleye 	aosp_walleye-userdebug
Pixel XL 	marlin 	aosp_marlin-userdebug
Pixel 	sailfish 	aosp_sailfish-userdebug
HiKey 	hikey 	hikey-userdebug
Nexus 6P 	angler 	aosp_angler-userdebug
Nexus 5X 	bullhead 	aosp_bullhead-userdebug
Nexus 6 	shamu 	aosp_shamu-userdebug
Nexus Player 	fugu 	aosp_fugu-userdebug
Nexus 9 	volantis (flounder) 	aosp_flounder-userdebug
Nexus 5 (GSM/LTE) 	hammerhead 	aosp_hammerhead-userdebug
Nexus 7 (Wi-Fi) 	razor (flo) 	aosp_flo-userdebug
Nexus 7 (Mobile) 	razorg (deb) 	aosp_deb-userdebug
Nexus 10 	mantaray (manta) 	full_manta-userdebug
Nexus 4 	occam (mako) 	full_mako-userdebug
Nexus 7 (Wi-Fi) 	nakasi (grouper) 	full_grouper-userdebug
Nexus 7 (Mobile) 	nakasig (tilapia) 	full_tilapia-userdebug
Galaxy Nexus (GSM/HSPA+) 	yakju (maguro) 	full_maguro-userdebug
Galaxy Nexus (Verizon) 	mysid (toro) 	aosp_toro-userdebug
Galaxy Nexus (Experimental) 	mysidspr (toroplus) 	aosp_toroplus-userdebug
Motorola Xoom (U.S. Wi-Fi) 	wingray 	full_wingray-userdebug
Nexus S 	soju (crespo) 	full_crespo-userdebug
Nexus S 4G 	sojus (crespo4g) 	full_crespo4g-userdebug

```
