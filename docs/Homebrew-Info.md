# This guide may be outdated!
Since [Version 2.0.0 Beta](https://github.com/TriForceX/MiyooCFW/releases/tag/2.0.0-beta) was pre-released the following guide will change or be updated and the current one may be only for the old version 1.3.3. Be careful!

---

List of ports installed with CFW and its links. (Thanks to **dElAvA**)

Name | Status
:------------: | :------------:
[Hydra Castle Labyrinth](https://github.com/szymor/hydracastlelabyrinth) | Runs
[Homing Fever](https://github.com/szymor/HomingFever/) | Runs
[calculator](https://github.com/szymor/bittboy-calc) | Runs
[asciiportal](https://github.com/cymonsgames/ASCIIpOrtal) | Not Loading
[cannonball](https://github.com/djyt/cannonball) | Works with OutRun Revision B ROMs
[cavestory](https://github.com/libretro/nxengine-libretro)| Runs
[chocolate-doom](https://www.chocolate-doom.org/wiki/index.php/Chocolate_Doom) | Works with doom1.wad
[cdogs](https://cxong.github.io/cdogs-sdl/) | Long delay to load, runs slow
digger| Runs
[hheriticsdl](http://hhexen.sourceforge.net/hheretic.html) | Works with heritic1.wad
[hhexen-sdl](http://hhexen.sourceforge.net/hhexen.html)| Works with hexen.wad
[liero](https://www.liero.be/) | Runs
[mrdrillux](https://github.com/mthuurne/mrdrillux)| Runs
[OpeenBoR](https://github.com/DCurrent/openbor)| Runs\Needs Game Mods
[Opentyrian](https://bitbucket.org/opentyrian/opentyrian/wiki/Home) | Runs
[pang](https://en.wikipedia.org/wiki/Pang_(video_game))| Runs
Quake | Runs
Quake2 | Runs
rott | Needs Data Files
kof | Runs
sdlpal | Runs
sdlpal2 | 
sod| Needs Data Files

# Ports and Homebrews

### Calculator (By vamastah)
- A simple calculator made for Bittboy handheld. It supports elementary arithmetic operations.
- You can download [here](https://github.com/szymor/bittboy-calc/releases)
- Just place the file in a folder named 'calc' in the 'apps' folder on your SD card

### CANNONBALL (Outrun Arcade):
- Place Outrun datafiles in '\.cannonball\roms'
- See '.cannonball\roms\Place outrun ROM files here.txt' for information on required files
- 'R' Button ('Reset' on pocket-go) changes gear

### DOOM:
- Shareware WAD file is included
- To play other WADs, copy them to '\roms\PC\DOOM'

### HERETIC:
- Shareware datafile is included
- To play the full version, copy the retail HERTIC.WAD to 'games\hheretic\'

### HEXEN:
- Shareware datafile is included
- To play the full version, copy the retail HEXEN.WAD to 'games\hhexen\'

### SOD:
- Shareware datafiles are included
- To play the retail/full version of Spear of Destiny:
  - Copy the retail SOD datafiles (all .SOD files other than config.SOD) to 'games\sod\'
  - In the same folder:
    - Delete (or rename) the file 'sod'
    - Rename the file 'sod-Retail' to 'sod'
 
The SOD icon on the games tab of your bittboy will now load the full game instead of the shareware version.

### STRIFE:
- Only the full version datafile (STRIFE1.WAD) is supported
- To play strife:
  - Copy the 'STRIFE1.WAD' datafile from a full copy of the game to 'games\ccdoom'

### Wolf3D:
- Shareware datafiles are included
- To play the retail/full version of Wolfenstein 3D:
  - Copy the retail Wolf3D datafiles (all .WL6 files other than config.WL6) to 'games\wolf3d\'
  - In the same folder:
    - Delete (or rename) the file 'wolf3d'
    - Rename the file 'wolf3d-Retail' to 'wolf3d'
 
The Wolf3D icon on the games tab of your bittboy will now load the full game instead of the shareware version.

### MPLAYER

How to add videos to your Miyoo device. 

Standard video files generally wont work on the Miyoo, the video player is kinda trash and wont be able to downscale or work with formats that its not familiar with. 

1. download the free open source video encoder Handbrake https://handbrake.fr/
2. Import your video and set the file format to .mkv, resolution to 320x240 (v90's native screen size). 
3. select MPEG-2 as your video codec, set constant quality of 3, frame rate same as source and select constant frame rate. 
4. for audio, set the bitrate to 64kpbs, set to mono (or stero if you plan to exclusively use headphones). 
5. throw the video in your SD card and navigate to it when using the mplayer app. 

you will get slight black bars on the top and bottom of the screen due to the square screen of the device.

**IMPORTANT:** The video player will always remember the last place you left it if you swap to another app AND if you finish playing the video. it saves this state as a .resume file. Once the video has finished playing IT WILL NOT PLAY FROM THE BEGINNING AGAIN. you will either need to rewind the video using the L1/L2 buttons OR delete the .resume file via the file manager app 
