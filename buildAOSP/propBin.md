# proprietary binaries

## DW

* AOSP can't be used from pure source code only and requires additional hardware-related proprietary libraries to run, such as for hardware graphics acceleration

* https://developers.google.com/android/drivers

## Extract proprietary binaries

Each set of binaries comes as a self-extracting script in a compressed archive. Uncompress each archive, run the included self-extracting script from the root of the source tree, then confirm you agree to the terms of the enclosed license agreement. The binaries and their matching makefiles will be installed in the vendor/ hierarchy of the source tree.

## INSTALL 

To ensure the newly installed binaries are properly taken into account after being extracted, delete the existing output of any previous build using:
```
make clobber
```

 unpack them, m installclean, and rebuild


