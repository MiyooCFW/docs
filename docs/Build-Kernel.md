## Clone kernel repo
```
git clone https://github.com/MiyooCFW/kernel
cd kernel
```

---
## Build kernel locally:

You need to have [SDK](Get-the-prebuilt-SDK-from-GH-actions.md) installed in `/opt/miyoo` directory

- set environment variables inline with SDK location:
```
export PATH=$PATH:/opt/miyoo/bin
export ARCH=arm
export CROSS_COMPILE=arm-linux-
```
- build kernel

```
make miyoo_defconfig
make
make dir-pkg
```

---
## Build kernel using docker with MiyooCFW Toolchain:
```
docker run --volume ./:/src/ -it miyoocfw/toolchain-shared-uclibc:latest
cd /src
make miyoo_defconfig
make
make dir-pkg
```
---
### Install kernel on SD card

- copy `arch/arm/boot/zImage` to `boot` partition on the SD card

### Install modules on SD card

- copy `tar-install/lib` directory to `rootfs` partition on the SD card