The GnGeo is an AES/MVS Neo Geo emulator (without NG-CD support) based of MAME ROMsets.

## Important Notes:
Place **neogeo.zip** BIOS alongside your ROMset.

Romset/games need to be from MAME 0.138 or FBA 2012 ROMset.

## Introduction to the *.GNO files (cached ROMsets):

**_What is *.gno ROMset file?_**   
It is a combination of  decrypted ROMs' files and BIOSes (partly encrypted). In short they are fast cache files, compering to *.ZIP ROMsets.

**_Why would you want to use GNO files instead of ZIP?_**  
GNOs loading time is 5÷10 times faster in GnGeo emulator and thus it can easily handle larger ROMsets (thanks to lower RAM usage).
The emu is trying to fit the entire unzipped ROM in memory while executing the game (decrypting the encrypted data), which explain the long load times with ZIP files and why anything larger than ~40Mb is prone to crashes on low-mem devices (in that case use *.gno ROMs)

**_How do I acquire *.gno ROMsets?_**

You need to convert original ziped files to .gno using GnGeo build for windows/linux/osx system (any platform with more RAM available). Just add "--dump" to your executable parameters in CLI. 
Example: ``./gngeo -i /my_roms_folder --dump mslug3``  

- Compile GnGeo and create GNO files (*): 
    1. Download current src (*)

            git clone --single-branch --branch gngeo-upd https://github.com/Apaczer/gngeo

    2. Pass commands

            cd gngeo/
            ./bootstrap
            ./configure
            make -j$(nproc)

    3. Grab ``gngeo`` binary from ./src/ directory and move it to ./gngeo.dat
    4. Create "roms" folder in ./gngeo.dat/ and put ziped ROMsets there
    5. Open terminal and cd to ./gngeo.dat directory
    6. Launch gngeo (test if it works) and exit
       
            chmod +x ./gngeo  
            gngeo

    5. Create *.gno dump:  
        
            gngeo --dump [romset_name]

    6. Grab new ``romset_name.gno`` file from ./gngeo.dat/ dir
    7. BENEFIT faster loading times with new ROMset format on your low-mem device

- Use pre-build binaries for:
    - x86_64 Linux systems (**): [gngeo_Linux-x86_64.zip](assets/gngeo_Linux-x86_64.zip)
    - Windows 32-bit (***): [gngeo-win32_0.1.zip](https://github.com/Apaczer/gngeo/releases/download/gngeo-win32_0.1/gngeo-win32_0.1.zip)

_\*) You might need some additional libraries to compile properly gngeo._   
_\*\*) For running binary ``libsdl1.2-dev`` should suffice on Debian distros._  
_\*\*\*) Use `dump.bat` script and drag&drop zipped ROMs to create *.gno_  