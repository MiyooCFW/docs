## Clone uBoot repo
```
git clone https://github.com/MiyooCFW/uboot.git
cd uboot
```
---
## Build uBoot locally

You need to have [SDK](Get-the-prebuilt-SDK-from-GH-actions.md) installed in `/opt/miyoo` directory

- set environment variables inline with SDK location:
```
export PATH=$PATH:/opt/miyoo/bin
export ARCH=arm
export CROSS_COMPILE=arm-linux-
```
- build uBoot

```
make miyoo_defconfig
make
```
---
## build uBoot using docker with MiyooCFW Toolchain:

```
cd uboot
docker run --volume ./:/src/ -it miyoocfw/toolchain-shared-uclibc:latest
cd /src
make miyoo_defconfig
make
```
---
## install uboot on SD card
```
dd if=./u-boot-sunxi-with-spl.bin of=/dev/mmcblk0 bs=1024 seek=8
```