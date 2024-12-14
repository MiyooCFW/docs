### Download files

NOTE: RetroArch is now included in 2.0.0 beta so you can skip the download/unzip steps (1 ad 2)!

1. Download the RetroArch.7z file from the Retroarch website https://www.retroarch.com/?page=platforms go down to the Miyoo section (Pocket Go, PowKiddy Q90 / V90, New BittBoy) to download the latest stable version
2. Unzip the retroarch folder from the Retroach.7z file on the main partition. With this you can now use the Retroarch from the emulators section.
The only thing missing is the icon and background of the theme being used.
3. Some kernels need bios, which go in the .retroarch/system folder.
You can use this repository https://github.com/Abdess/retroarch_system

### Configuration
The recommended configuration is:  
- Main Menu - Settings - User Interface - Show Advanced Settings: Enabled

**with ``alsa`` audio  output (by default):**  
- Main Menu - Settings - Audio - Resampler - Audio Resampler: nearest / Resampler Quality: Minimum / Output speed (Hz): 32000

**with ``sdl`` audio output:**  
- Main Menu - Settings - Audio - Resampler - Audio Resampler: sync / Resampler Quality: Minimum / Output speed (Hz): 22000

**for video output:**  
- Main Menu - Settings - Video - Video Threading: Off  
- Main Menu - Settings - Video - Synchronization - Vertical Synchronization: On / VSync Swap: 1 / Frame Delay: 0 / Sync to Exact ...: On (for Scummvm turn Off)  

For Frameskip options to work (eg. PCSX, gpSP, MAME, snes9x cores), you must use default ``alsa`` audio driver.

For **QuickNES** core add  
- Main Menu - Settings - Video - Scaling - Integer Scale: on  
- Main Menu - Settings - Video - Image Interpolation - Nearest Neighbor  
- Main Menu - Settings - Video - Video Filter - Upscale_256X-320  
- Quick Menu - Options - Audio Mode - Linear  

For fullscreen scaling in **QuikNES** core, set:  
- Main Menu - Setting - Video - Scaling -Integar Scale: OFF / Keep Aspect: OFF / Crop Overscan: OFF  
- Quick Menu - Options - Aspect Ratio: 4:3 / Show Horizontal Overscan: ON/ Show Vertical Overscan: ON  

Show Vertical Overscan: ON (for correct pixels scaling) ; OFF (for accurate aspect ratio) 
with this setting ON most of games will look squashed and have black bar at the bottom
on the other hand OFF will blurr some of pixelization

For **gpSP** core add  
- Main Menu - Settings - Video - Video Filter - Upscale_240x160-320x240.filt **(for bilinear effect)**  
- Main Menu - Settings - Video - Video Filter - Upscale_240x160-320x240-mix.filt **(for improved readability)**

To save the configuration of a core  
- Main Menu - Configuration File - Save New Configuration

To save core's general settings to use with RetroArch app, while in-game:  
- Quick Menu -> Overrides -> Save Core Overrides-> .....

All core options from Quick Menu->Options will be saved automatically upon closing content. 

### Recommended cores by systems

- **mGBA** core is not recommended to use for GBA games, but GB and GBC games run fine on that core. For GBA better use core gpsp.

Gambatte core is faster for GB and GBC titles and offers more options for pallete change.

- **GenesisPlusGX** core is not recommended to use for MD games, but SMS and GG games run fine on that core. For MegaDrive better use Picodrive core

Picodrive core is faster option for SMS games, especially if any of the video filters will be applied and if no emulated CPU overclocking is needed (for that use Genesis plus GX).

- **Snes9x 2005** core has better performance with pal roms

### New cores
You can use the nightly version for new updates that are not yet in the stable branch or for new cores that are coming out and are not included in the stable version. The cores are added in the .retroarch/cores folder

They are at this link:  
https://buildbot.libretro.com/nightly/dingux/miyoo-arm32/latest/

### Integrate with GMenu2X
ROMs can be run by launching Retroarch or by running from GMenu2X, selecting the ROM and launching the RetroArch core as if it were a native emulator.
 
To launch the Retroach cores from Gmenu2x you have to create a script and a link in gmenu2x to that script

The structure of the script is

```
retroarch_path -v -L core_path --config config_path [rom_to_load]
```


***

For example, for the Game Boy Advanced system, the **gba_ra.sh** script is created with the content

```
#!/bin/sh
/mnt/emus/retroarch/retroarch -v -L /mnt/.retroarch/cores/gpsp_libretro.so --config /mnt/.retroarch/config/gpsp_libretro.cfg "$1"
```

If you haven't created a configuration for core gpsp use global configuration, the script would be

```
#!/bin/sh
/mnt/emus/retroarch/retroarch -v -L /mnt/.retroarch/cores/gpsp_libretro.so --config /mnt/.retroarch/retroarch.cfg "$1"
```

To save the configuration of a core
* Main Menu - Configuration File - Save New Configuration


This script is saved in the emulators folder with the name gba_ra.sh, remember the path /mnt/emus/gba_ra.sh
You can use whatever name you want but with the .sh extension and save it in whatever folder you want on the main partition, but remember the name and the folder.

A new link is created in gmenu2x, in the main partition in the folder gmenu2x/sections/emulators/gba_ra with the content

```
title=GBA
description=gba Retroarch
exec=/mnt/emus/gba_ra.sh
clock=702
selectordir=/mnt/roms/GBA
selectorscreens=/mnt/roms/gba/.preview
```

For more information on gmenu2x bindings
[https://mtorromeo.github.io/gmenu2x/documentation/](https://mtorromeo.github.io/gmenu2x/documentation/)

For Windows system's users to properly write shell scripts for these devices, you need to have End Of Line conversion se to Unix (LF) in your editing program.

***

If you want to use a core that does not need to indicate a rom to initialize it, such as Scummvm, these would be the files to create.

```
#!/bin/sh
/mnt/emus/retroarch/retroarch -v -L /mnt/.retroarch/cores/scummvm_libretro.so --config /mnt/.retroarch/config/scummvm_libretro.cfg
title=Scummvm
description=Scummvm
exec=/mnt/emus/scummvm_retroarch.sh
clock=702
```


Scummvm can also be launched indicating a rom, if you want more information on how to do it you can read this page in Spanish
[http://apuntes.eduardofilo.es/2020-08-15-rg350_scummvm_launchers.html](http://apuntes.eduardofilo.es/2020-08-15-rg350_scummvm_launchers.html)


***

If you want to use a core that always uses the same rom to initialize it, such as **NXEngine** with **Cave Story**, these would be the files to create.

```
#!/bin/sh
/mnt/emus/retroarch/retroarch -v -L /mnt/.retroarch/cores/nxengine_libretro.so --config /mnt/.retroarch/retroarch.cfg /mnt/roms/cavestory/Doukutsu.exe
```

```
title=Cave Story
description=Cave Story
exec=/mnt/emus/cavestory_ra.sh
clock=702
```

For more information on how to integrate Retroarch in gmenu2x you can see this page in Spanish
[http://apuntes.eduardofilo.es/2021-01-16-rg350_ra_installer.html](http://apuntes.eduardofilo.es/2021-01-16-rg350_ra_installer.html)

***
If you also add a key combination to close Retroarch, you can use not having the Retroarch cores without handling its interface.

A key combination is assigned to close Retroarch on
* Main Menu - Setting - Input - Hotkeys - Quit Controller Combo

The only thing that you will not have the icon and the background (if the theme uses a background), you have to create the image of the icon and the background

For example, for the Game Boy Advanced system.
For the icon on the main partition in the folder gmenu2x/skins/{Theme_you_are_using}/icons/ create an image with the name gpsp_ra.png. The easiest is to duplicate the file gpsp_rumble.png and name it gba_ra.sh.

For the background, not all themes use backgrounds. In the main partition in the folder gmenu2x/skins/{Theme_you_are_using}/backdrops/ create an image with the name gpsp_ra.png. The easiest is to duplicate the file gpsp_rumble.png and name it gba_ra.sh.

### Launch Retroarch with the last game played

If you want to start from the last played game whenever you open RetroArch, these would be the files to create.

**retroarch_history.sh**
```
#!/bin/sh
function start_retroarch {
  cd /mnt/emus/retroarch
  if ! read -n 1 -t 1 -s; then
    local history_path='/mnt/.retroarch/content_history.lpl'
    if test -f "${history_path}"; then
      local rom_path="$(head -n20 "${history_path}" | grep -Eo -m1 '/mnt/roms/[^"]+')"
      local core_path="$(head -n20 "${history_path}" | grep -Eo -m1 '/mnt/.retroarch/cores/.+\.so')"
      if test -f "${core_path}" -a -f "${rom_path}"; then
        clear
        echo -e "\n\n\n\n\n\n\n\n\n\n\n\n\n\n              \e[1;33m[ LOADING ]\e[0m"
        ./retroarch --load-menu-on-error --libretro "${core_path}" "${rom_path}" > /dev/null 2>&1
        return
      fi
    fi
  fi
  ./retroarch --menu > /dev/null 2>&1
}
start_retroarch
```


A new link should be created in gmenu2x, in the main partition in the folder gmenu2x/sections/emulators/start_retroarch.sh with the content
```
title=RA History
description=Retroarch History
exec=/mnt/emus/retroarch_history.sh
clock=702
```

**The above script is already provided with MiyooCFW 2.0.0**

(function provided from https://github.com/jahed/powkiddy-v90)

