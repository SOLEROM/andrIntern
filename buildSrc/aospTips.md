# tips

## kernel name

* To locate the correct filename for your kernel, refer to device/VENDOR/NAME-kernel in the AOSP tree

```
cd $AOSP/device/VENDOR/NAME
git log --max-count=1
```

* Kernel version from system image

```
file kernel
grep -a 'Linux version' Image.lz4-dtb
```



