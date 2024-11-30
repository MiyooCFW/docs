## Important note

**You can find an alternative setup for DOSBox on Miyoo and see some further information on setting up MS-DOS software in [this thread](https://github.com/TriForceX/MiyooCFW/discussions/268).**

- DOSBox boots to the menu system 'LaunchBox for MS-DOS SE 2.0'
- To play the included game (Shareware Commander Keen Episode 1 "Marooned on Mars") Press 'start'

**Controls:**
- The keys to launch, quit and play are mapped
- Bittboy buttons map as:
```
PocketGo:       Bittboy:            Key:
Up              Up                  Up
Down            Down                Down
Left            Left                Left
Right           Right               Right
A               TA                  LALT
B               A                   LCTRL
X               TB                  LSHIFT
Y               B                   Space
Start           Start               RETURN
Select          Select              ESCAPE
Reset           R                   RCTRL
```
- When another key needs to be pressed (eg to quit the game) the On Screen Keyboard (OSK) must be used
- Opening (or closing) the OSK:
  - Bittboy: Press Start+B at the same time
  - PocketGo: L trigger
- To hold 2 or more keys you just need to press B once on the desired key, that will hold the key (a green border will appear), then you press the other key with A. To remove the old just press B again.

**Exiting from DOSbox:**
1. First Quit Commander Keen:
  - Press select. Use the OSK when prompted to press a key to quit
2. Then Exit the LaunchBox menu:
  - Press 'TA' ('A' on pocket-go) to select the 'File' menu, press start to accept. Use the dpad to choose 'Exit', press start to accept
 
**Adding new DOS games:**
- DOSBOX uses '\roms\PC\DOS' as 'C:\'
- DOSBOX configuration file location: '\emus\dosbox\dosbox.conf'
- Place the new game folder within '\roms\PC\DOS'
- Edit '\roms\PC\DOS\LAUNCHBX\LAUNCHBX.TXT' to add the new game to the LaunchBox menu
  - See example file 'LAUNCHBX - Example.TXT' in the same location