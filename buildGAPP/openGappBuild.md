# openGapps

* https://www.makeuseof.com/tag/install-gapps-android/
* https://github.com/opengapps/opengapps 

## build ENV

```
# deps
=======
curl -s https://packagecloud.io/install/repositories/github/git-lfs/script.deb.sh | sudo bash
sudo apt-get install git-lfs
git lfs install


cd /usr/lib/python3/dist-packages
cp apt_pkg.cpython-35m-x86_64-linux-gnu.so apt_pkg.so

sudo apt-add-repository ppa:maarten-fonville/android-build-tools
sudo apt-get update 
sudo apt-get install android-build-tools-installer

apt-get install lzip

# repo
=======
git clone https://github.com/opengapps/opengapps.git
./download_sources.sh --shallow arm


# build
=======
make arm-27-pico
```

## example


```

```

```
open_gapps-arm-8.1-pico-20200413-UNOFFICIAL.zip 

├── app_densities.txt
├── app_sizes.txt
├── bkup_tail.sh
├── busybox-arm
├── Core
├── GApps
├── gapps-remove.txt
├── g.prop
├── installer.sh
├── LICENSE
├── META-INF
├── Optional
├── tar-arm
├── unzip-arm
└── zip-arm



[CONT]root@AndBuild:/gapp/opengapps/out/unzip$ ls Core/
carriersetup-all.tar.lz         extsharedgoogle-all.tar.lz        googlefeedback-all.tar.lz            setupwizarddefault-all.tar.lz
configupdater-all.tar.lz        gmscore-arm.tar.lz                googleonetimeinitializer-all.tar.lz  setupwizardtablet-all.tar.lz
defaultetc-common.tar.lz        gmssetup-all.tar.lz               googlepartnersetup-all.tar.lz        vending-arm.tar.lz
defaultframework-common.tar.lz  googlebackuptransport-all.tar.lz  googlepixelconfig-common.tar.lz
extservicesgoogle-all.tar.lz    googlecontactssync-all.tar.lz     gsfcore-all.tar.lz

```
