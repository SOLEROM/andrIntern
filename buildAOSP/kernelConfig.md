# kernelConfig

* maintaining a local modification or copy of the build config
* used for working on a feature, or if you need an option to be set for development purposes

* Set the variable POST_DEFCONFIG_CMDS to a statement that is evaluated right after the usual make defconfig step is done


* example to disabling link time optimization (LTO):

```
POST_DEFCONFIG_CMDS="check_defconfig && update_debug_config"
function update_debug_config() {
    ${KERNEL_DIR}/scripts/config --file ${OUT_DIR}/.config \
         -d LTO \
         -d LTO_CLANG \
         -d CFI \
         -d CFI_PERMISSIVE \
         -d CFI_CLANG
    (cd ${OUT_DIR} && \
     make O=${OUT_DIR} $archsubarch CC=${CC} CROSS_COMPILE=${CROSS_COMPILE} olddefconfig)
}
```
