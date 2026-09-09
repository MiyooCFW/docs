Final Burn Alpha is an arcade emulator supporting the following hardware platforms;

 - Capcom CPS-1
 - Capcom CPS-2
 - Cave
 - Neo Geo
 - Sega System 16 (and similar), System 18, X-Board, Y-Board
 - Toaplan
 - Taito Rainbow Islands/Operation Wolf/Rastan
 - Psikyo 68EC020 based hardware
 - misc stuff

## Important Notes
This emulator uses 0.2.96.86 FBA ROMset and it's based of fba-a320 src.

## Introduction to the *.fba files (cached ROMsets):
**_What is *.fba ROMset file?_**  
The latest builds of our FBA utilize loading mmap-backed *.fba cache for CPS, Cave, Neo Geo, and PGM platforms.

**_Why would you want to use FBA files instead of ZIP?_**  
They Allow for booting up faster ROMs comparingly to ZIP format.

**_How do I acquire *.fba ROMsets?_**  
You need to convert original zipped files to .fba using `fbacache.exe` build for Windows (on Linux via `wine`, since there is no src) via any platform with reasonable RAM available.

- Downlaod FBA Cache utility (by _HeadOverHeels_) to create cache files from roms:
    - from https://github.com/RetroPie/pifba repo: [FBACache_windows.zip](https://github.com/RetroPie/pifba/raw/refs/heads/master/FBACache_windows.zip)
    - from official link: https://pyra-handheld.com/boards/resources/fba-cache.1540/
    - from here: [FBA_Cache_win32.zip](assets/FBA_Cache_win32.zip)
- Dump .fba file under Windows (*):
    1. Unzip package somewhere
    2. Copy the ROM set to the 'roms' folder of FBACache
    3. If it's a NeoGeo or PGM game, copy also the BIOS set (neogeo.zip or pgm.zip)
    4. If it's a clone set, copy also the parent set
    5. Open the Command_Prompt/Powershell, and go to the FBACache directory
    6. Type and enter 'fbacache.exe -d [romname].zip' (no quotes, and [romname] is the ROM set's filename)
    7. Wait until the dumping process completes (make sure no missing files are indicated)
    8. Grab & use only the [romname].fba for launching faster your favourite game

_*) To run under Linux use `wine32` from pkg manager, on 64bit Debian you'll need to prompt `dpkg --add-architecture i386` to enable 32bit packages d/l._
