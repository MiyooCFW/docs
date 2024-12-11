
## Download the prebuilt toolchain from GH action artifacts

### Precondition
You have to be logged on GitHub

1. Go to https://github.com/MiyooCFW/buildroot/actions and select the latest action
2. From the artifacts section download SDKs

![image](imgs/gh-actions.png)

3. Once you have downloaded it, extract it
```
gzip -d arm-miyoo-linux-uclibcgnueabi_sdk-buildroot.tar.gz
tar xvf arm-miyoo-linux-uclibcgnueabi_sdk-buildroot.tar
mv arm-miyoo-linux-uclibcgnueabi_sdk-buildroot miyoo
sudo cp -a miyoo /opt/
/opt/miyoo/relocate-sdk.sh
```

Your SDK is ready to use
