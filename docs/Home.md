<div align="center">

![miyoo-cfw](https://github.com/TriForceX/MiyooCFW/assets/16083854/51119d94-24a5-47b7-8bbd-f93b997c36c1)

> The definitive custom firmware for **BittBoy**, **PocketGo**, **PowKiddy V90-Q90-Q20** _(and 3rd party consoles)_ allows you unlock the potential of the hardware and use software from a wide variety of consoles and computers thanks to the availability of numerous emulators and native ports of several games!

---

![miyoo-consoles](https://user-images.githubusercontent.com/16083854/221029395-26b04557-dccf-40bd-a059-b9928553ee4f.png)

</div>

## Compatible Consoles
- BittBoy v1, v2, v2.5, v3, v3.5
- Pocket Go
- PowKiddy Q90
- PowKiddy V90
- PowKiddy Q20 Mini
- Sup M3 v1, v2 <sup>(See notes)</sup>
- XYC Q8
- RS-77 <sup>(Not confirmed)</sup>
- Powkiddy X7 <sup>(Not confirmed)</sup>

**Notes:**  Only devices with Allwinner ``F1C100S`` or ``F1C500S`` SOC are supported and even these can come with not fully compatible components (e.g. unfamiliar LCD display). There were reports of console revisions with "updated" SOC - ``F1E200`` or ``V100``.

The **Not confirmed** consoles are not supported yet, these consoles are under revision and may not be on the final compatibility list.

---

# General Information

### SD Card
Is <b>highly</b> recommended to <b><u>NOT</u></b> use the SD card included in the package with the console or unbranded ones, it can be corrupted easily without reason due its bad quality. We recommend to use the common brands, 2GB minimum and class 10 for faster install process.

---


### Shutting down the console
- Version 2.0.0 uses the BTRFS file system to prevent data corruption during an unsafe shutdown. This system automatically writes data every 5 seconds, so if you save a game and immediately turn off the console, the save may be lost. Therefore, it is safe to wait at least 5 seconds before shutting down the system or to perform a proper shutdown procedure.
- To safely shut down the console from GMenu2X:
  - Exit from the emulator or game you are playing to return to the main menu (gmenu)
  - Press the R/Reset(HOME) button to open the Power Menu
  - Press A to shut down
  - Alternatively, you can go to the settings section and use the "Shutdown" icon or use the *Quick Shutdown Hotkey*
  - When the screen turns black, flick the power switch

---
 
### Screen timeout/sleep mode (GMenu2X)
This only applies while in the menu:
- Holding the Start button button will put the device into sleep/suspend mode
  - Press R/Reset(HOME) or Start again to wake it up
- The default screen timeout is 30 seconds, after this the screen will go black (the device will go to sleep)
- Power timeout is disabled by default

---
### Screen tearing fix

The screen tearing fix is disabled by default for compatibility reasons. You can enable the screen tearing fix feature in GMenu2X in two ways:
- Globally:
  - Go to GMenu2X settings and set the TEfix method to 1, 2, or 3
- Per app:
  - For a specific app, press "Select," choose "Edit," and set the TEfix method to 1, 2, or 3

TEfix=0 - off  
TEfix=1 - for newer LCD panels  
TEfix=2 - for older LCD panels (use when overclocking CPU)  
TEfix=3 - for older LCD panels (use when underclocking CPU)  

> **_NOTE:_**  Choose the best TEfix method for your particular handheld's LCD panel. Some methods may not work correctly for you. Additionally, there may be a small FPS drop when TEfix is enabled

---
### IPK Support

Miyoo supports installing IPK packages for apps, emulators, and games. To install an IPK, simply copy the IPK file (e.g., [drpocketsnes.ipk](https://github.com/Apaczer/DrPocketSNES/releases/download/7.2.3/drpocketsnes.ipk)) to the main partition. Then, run the GMenu2X explorer, select the IPK file, and install it.

---

### Autostart

To enable the Autostart feature, go to GMenu2X settings and set Autostart to `ON`. Next, choose the app you want to autostart. When you quit the app, the handheld will shut down. After rebooting, the selected app will autostart. 
> **_NOTE:_**  To disable Autostart, quickly press the `Y` button when the GMenu2X hint box appears on the screen.

---

### TV-out mode

To enable TV-out, run "TVout ON/OFF" from the Apps section. The handheld will reboot and start working in TV-out mode

> **_NOTE:_**  To quickly exit TV-out mode, hold the select button after fully booting into GMenu2x

---

## Supported USB modes

### USB HID
Turn your handheld into USB gamepad for PC/Android

    - Connect handheld to PC via USB
    - Run this USB HID app
    - Now you should be able to control PC/phone via handheld buttons
    - Press RESET button to leave USB HID mode
### USB Host
Allows to connect external device (keyboard, mouse, gamepad) to the handheld

    - You need the USB OTG "Y" cable (male type C, see pic) to supply power from the charger to the external device since handheld doesn't provide it, as well for the USB bus to be active.

![type_c_cable](https://github.com/user-attachments/assets/4f90b0bd-3e1b-44ef-87d7-9719cdd5df8b)

    - Connect the external device to the handheld with external power

> **_NOTE:_**  Host mode also allows connection to the network using Android USB tethering

    - Connect Android phone and enable USB tethering
    - Start DHCP client app
    - Check the assigned IP in the show IP addr app


### USB MTP 
Allows to transfer files between a handheld and a PC using a USB connection

### USB Network 
Enable network on the handheld

    - IP address of handheld: 192.168.137.1
    - After enabling this mode you can start FTP server app or SSH server app or play multiplayer (netplay) in Retroarch
### USB Serial console 
Allows connection to a handheld terminal using a serial port (COM port)

---

### Alternative to access the "main" BTRFS partition on Windows (SD card)
[BTRFS driver for windows](https://github.com/maharmstone/btrfs)

---
### Additional settings

On the `main` partition, there is a file `options.cfg` that can be used to configure the following additional settings:


* `MODULES_CUSTOM=0` - set 1 if you want to load custom modules defined in file `modules.custom.sh` on `boot` partition
* `FAT_CHECK=1`  - set 0 to disable fsck `boot` partition
* `BOOT_LOGO=1` - set 0 to disable boot logo
* `FLIP=0` - Set to 1 to rotate the screen by 180 degrees
* `INVERT=0` - Set to 1 to invert colors on the screen
* `TVMODE=0` - Set to 1 to use PAL mode for TV output, otherwise use NTSC 
* `HOTKEY_CUSTOM=1` - Set 1 to enable custom hotkey bindings [see here](https://github.com/MiyooCFW/daemon?tab=readme-ov-file#config)


