## Recommended settings  

For Frameskip options to work (eg. PCSX, gpSP, MAME, snes9x cores), you must use default ``alsa`` audio driver.

#### **QuickNES** core
Recommended:  
- Main Menu - Settings - Video - Scaling - Integer Scale: on  
- Main Menu - Settings - Video - Image Interpolation - Nearest Neighbor  
- Main Menu - Settings - Video - Video Filter - Upscale_256X-320  
- Quick Menu - Options - Audio Mode - Linear  

Optional:  
- Show Vertical Overscan: ON (for correct pixels scaling)  
- Show Vertical Overscan:OFF (for accurate aspect ratio)  
NOTES: with ON most of games will look squashed and have black bar at the bottom, on the other hand OFF will blurr some of pixelization

#### **gpSP** core
Recommended:  
- Main Menu - Settings - Video - Video Filter - Upscale_240x160-320x240.filt **(for bilinear effect)**  
- Main Menu - Settings - Video - Video Filter - Upscale_240x160-320x240-mix.filt **(for improved readability)**

## Recommended cores by systems

- **mGBA** for GB and GBC (not recommended to use for GBA games).
- **gpSP** for GBA (faster)
- **Gambatte** for GB and GBC (faster), offers more options for pallete change.
- **GenesisPlusGX** for SMS and GG (not recommended to use for MD games).
- **Picodrive** for MD/SMS/GG (faster)
- **Snes9x 2005** mostly for PAL SNES (not recommended)
- **Snes9x 2002** fos SNES (faster)

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

For more information on how to integrate Retroarch in gmenu2x you can see this page in Spanish
[http://apuntes.eduardofilo.es/2021-01-16-rg350_ra_installer.html](http://apuntes.eduardofilo.es/2021-01-16-rg350_ra_installer.html)