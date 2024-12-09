---

# version 1.3.3 - deprecated

## OpenDingux for Miyoo/Bittboy/PocketGo Handheld

- This guide was made by **Steward** and describes how to build all of source codes that include uboot, kernel and emulators
  
## Prepare environment
- Debian 9 (x64)
  
## Configure toolchain
- Extract toolchain.7z into /opt/miyoo
  - Download form [here](https://drive.google.com/file/d/1Zp6elbB3r4Hq7G7FKXNtBZMTz0H93RiY/view?usp=sharing)
  - NOTE: Is recommended to build your own toolchain due it has received many updates, see [here](https://github.com/TriForceX/MiyooCFW/wiki/Making-Games#step-2)
- Export command
  - export PATH=$PATH:/opt/miyoo/bin
  
## Build UBoot
- Boot from SPI Flash
  - make ARCH=arm CROSS_COMPILE=arm-linux-gnueabi- licheepi_nano_spiflash_defconfig && make ARCH=arm
- Boot from SDCard
  - make ARCH=arm CROSS_COMPILE=arm-linux-gnueabi- miyoo_defconfig && make ARCH=arm
  
## Build Kernel (4bit sdcard - Hardware rev2 and later)
- vim arch/arm/boot/dts/suniv-f1c500s-miyoo.dts +55
  - bus-width = <4>;
- make ARCH=arm CROSS_COMPILE=arm-linux-gnueabi- miyoo_defconfig && make ARCH=arm zImage
  
## Build Kernel (1bit sdcard - Hardware rev1)
- vim arch/arm/boot/dts/suniv-f1c500s-miyoo.dts +55
  - bus-width = <1>;
- make ARCH=arm CROSS_COMPILE=arm-linux-gnueabi- miyoo_defconfig && make ARCH=arm zImage
  
## Build Boot.scr
- Create a file named boot.cmd and copy this:
  ```
  setenv bootargs console=tty0 console=ttyS1,115200 panic=5 rootwait root=/dev/mmcblk0p2 rw
  load mmc 0:1 0x80C00000 suniv-f1c500s-miyoo.dtb
  load mmc 0:1 0x80008000 zImage
  bootz 0x80008000 - 0x80C00000
  ```
- Build the file with:
  - mkimage -C none -A arm -T script -d boot.cmd boot.scr
  
## Prepare SDCard (>= 4GB)
- Partition 1: 256MB FAT32 (boot.scr, dtb and zImage)
- Partition 2: 256MB EXT4 (rootfs)
- Partition 3: 256MB SWAP
- Partition 4: FAT32 (GMenu2X, config files and emulators)
  
## Flash UBoot:
- Boot from SPI Flash (Hardware rev1 and rev2)
  - Short SPI Pin1 and Pin2
  - Connect USB to PC
  - Found device: 
    - usb 4-1.2.4.4: New USB device found, idVendor=1f3a, idProduct=efe8
  - Release SPI Pin1 and Pin2
  - Flash command: 
    - $ sudo sunxi-fel -p spiflash-write 0 u-boot-sunxi-with-spl.bin
- Boot from SDCard
  - $ sudo dd if=u-boot-sunxi-with-spl.bin of=/dev/sdX bs=1024 seek=8
  
## Flash Kernel
- Copy boot.scr into Partition 1
- Copy zImage into Partition 1
- Copy suniv-f1c500s-miyoo.dtb into Partition 1
- Copy r61520fb.ko into kernel folder in Partition 2
- Copy daemon into kernel folder in Partition 2
  
## Build Rootfs
- You can use an already configured buildroot from https://github.com/MiyooCFW/buildroot
  - See here: https://github.com/TriForceX/MiyooCFW/wiki/Making-Games#step-2
- Or download buildroot-2018.02.9 from https://buildroot.org
- Use config_buildroot-2018.02.9 and then make it
- Toolchain location: /opt/miyoo
- Rootfs location: output/images/rootfs.tar
  
## Flash Rootfs
- Extract rootfs.tar into Partition 2
  
## Author website
- You may find other resources and stuff for this (and the other guides) in https://github.com/steward-fu/miyoo/releases
- More reviews and details in https://steward-fu.github.io/website/handheld.htm