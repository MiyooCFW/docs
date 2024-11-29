### Precondition for Ubuntu 22.04
```
sudo apt install -y wget unzip build-essential git bc swig libncurses-dev libpython3-dev libssl-dev cpio rsync subversion python3 mercurial imagemagick btrfs-progs
```
---
### Clone buildroot repo
```
git clone https://github.com/MiyooCFW/buildroot.git
cd buildroot
```


---
### You can build four types of source
1. Shared uClibc Image and SDK
2. Shared musl Image and SDK
3. Static uClibc SDK only
4. Static musl SDK only
> **_NOTE:_**  You can build only one type of source, after each build you need to clean workspace by using `make clean`

> **_NOTE:_**  Difference between static and shared: [Static library](https://en.wikipedia.org/wiki/Static_library) [Shared_library](https://en.wikipedia.org/wiki/Shared_library)

> **_NOTE:_**  You will also need at least 10GB of free space before you can proceed

> **_NOTE:_**  This can take a long time!

---
### Build uClibc image and SDK shared 
```
make miyoo_uclibc_defconfig
make sdk
```

### Build musl image and SDK shared 

```
make miyoo_musl_defconfig
make sdk
```

### Build uClibc SDK static 

```
make miyoo_static_uclibc_defconfig
make sdk
```

### Build musl SDK static 

```
make miyoo_static_musl_defconfig
make sdk
```
> **_NOTE:_**  If you have a multicore CPU, you can increase build speed with: make -j ${YOUR_CPU_COUNT}


---
### Install image

Img  will be in the `output` directory e.g.
```
miyoo-cfw-2.0.0-67298a0_uclibc-BETAv2.img
```

---
### Install SDK

SDK will be in the `output` directory
```
arm-miyoo-linux-uclibcgnueabi_sdk-buildroot.tar.gz
```

Unpack `arm-miyoo-linux-uclibcgnueabi_sdk-buildroot.tar.gz` to `/opt/miyoo`, additionally you can run `relocate-sdk.sh` in custom SDK path
```
gzip -d arm-miyoo-linux-uclibcgnueabi_sdk-buildroot.tar.gz
tar xvf arm-miyoo-linux-uclibcgnueabi_sdk-buildroot.tar
mv arm-miyoo-linux-uclibcgnueabi_sdk-buildroot miyoo
sudo cp -a miyoo /opt/
/opt/miyoo/relocate-sdk.sh
```

Your SDK is ready to use
