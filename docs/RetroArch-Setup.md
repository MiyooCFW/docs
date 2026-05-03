## Hotkeys mapping (from custom MiyooCFW build)

Capitalized buttons description refers to Retropad input

- Menu Toggle: MENU  
- Menu Toggle Combo: START+SELECT  
- Quit Combo: START hold

All bellow bindings Enabled by: SELECT hold

Retropad | Hotkey CMD
:-----: | :-----:
B (Down) | LoadState
A (Right) | SaveState
Y (Left)| Rewind (*)
X (Top) | FastForward (Toggle)
L1 | Reset Content
L2 | Toggle FPS
R1 | Pause/Unpause
R2 | Game Focus (**)

\*) *You must first enable Rewind functionality manually in `Settings->Frame_Throttle->Rewind->Rewind_Support(ON)` or in Gmenu2X's extra RetroArch settings*  
\**) *`Game Focus` mode will disable all RA bindings and read direct keyboard inputs from connected controller (only applicable to "Keyboard" controller in cores that utilizes it e.g. emulating vintage computer like AMIGA)*

## Recommended settings  

*) Video  
- Output - `sdl`  
- Synchronization - VSync - OFF: (It is recommended to NOT use Vertical Sync because the frameskipping and rendering may be broken when in conjunction with it, regardless for some cores it may beneficial in reducing tearing effect)  
- Synchronization - G-Sync/FresSync - ON: (greatly reduces bad framerate pacing)

*) Audio  
- Output - alsa`: for Frameskip options to work (eg. PCSX, gpSP, MAME, snes9x cores), you must use default audio driver.

#### **QuickNES** core
Recommended:  
- Main Menu - Settings - Video - Scaling - Integer Scale - ON  
- Main Menu - Settings - Video - Image Interpolation - Nearest Neighbor  
- Main Menu - Settings - Video - Video Filter - Upscale_256X-320  
- Quick Menu - Options - Audio Mode - Linear  

Optional:  
- Show Vertical Overscan: ON (for correct pixels scaling)  
- Show Vertical Overscan:OFF (for accurate aspect ratio)  
NOTES: with ON most of games will look squashed and have black bar at the bottom, on the other hand OFF will blur some of pixelization

#### **gpSP** core
Recommended:  
- Main Menu - Settings - Video - Video Filter - Upscale_240x160-320x240.filt **(for bilinear effect)**  
- Main Menu - Settings - Video - Video Filter - Upscale_240x160-320x240-mix.filt **(for improved readability)**

## Recommended cores by systems

- **mGBA** for GB and GBC (not recommended to use for GBA games).
- **gpSP** for GBA (faster)
- **Gambatte** for GB and GBC (faster), offers more options for pallet change.
- **GenesisPlusGX** for SMS and GG (not recommended to use for MD games).
- **Picodrive** for MD/SMS/GG (faster)
- **Snes9x 2005** mostly for PAL SNES (not recommended)
- **Snes9x 2002** for SNES (faster)

## New cores
You can use the nightly version for new updates that are not yet in the stable branch or for new cores that are coming out and are not included in the stable version. The cores should be added in the /mnt/.retroarch/cores folder

You can download the latest builds via RetroArch's Online Updater or manually from "Cores" section on this website.

## More Info  
To save the configuration of a core  
- Main Menu - Configuration File - Save New Configuration

To save core's general settings to use with RetroArch app, while in-game:  
- Quick Menu -> Overrides -> Save Core Overrides-> .....

All core options from Quick Menu->Options will be saved automatically upon closing content. 

Scummvm can also be launched indicating a rom, if you want more information on how to do it you can read this page in Spanish
[http://apuntes.eduardofilo.es/2020-08-15-rg350_scummvm_launchers.html](http://apuntes.eduardofilo.es/2020-08-15-rg350_scummvm_launchers.html)

For more information on how to integrate RetroArch in GMenu2x you can see this page in Spanish
[http://apuntes.eduardofilo.es/2021-01-16-rg350_ra_installer.html](http://apuntes.eduardofilo.es/2021-01-16-rg350_ra_installer.html)