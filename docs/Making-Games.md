## How to build your own games
This is an small guide to start making games for Miyoo (not for beginners). Thanks to **crait** for this guide and **gameblabla** for his updates.

## SDL 1.2 keys (MiyooCFW 2.0.0 & above)
Physical button bindings for Miyoo 1'st gen consoles (Bittboy's in round brackets)

Button | SDLKey 
:-----: | :-----: 
A (A) | SDLK_LALT
B (B) | SDLK_LCTRL
X (TA) | SDLK_LSHIFT 
Y (TB)| SDLK_SPACE
L1 | SDLK_TAB
R1 | SDLK_BACKSPACE 
L2 | SDLK_PAGEUP
R2 | SDLK_PAGEDOWN
L3 | SDLK_RALT
R3 | SDLK_RSHIFT
RESET | SDLK_RCTRL
START | SDLK_RETURN
SELECT | SDLK_ESCAPE
UP/DOWN | SDLK_UP/DOWN
LEFT/RIGHT | SDLK_LEFT/RIGHT

To check correctness of this table use [I/O tester](https://github.com/Apaczer/iotester/releases/latest) on your handheld.


## Step 1

Since we're working with Linux-based devices, you're going to need to run a Linux distribution.
So, if you're on Windows, you'll need to install a Virtual Machine, Cygwin, WSL or something like that.

Recommended Linux distribution is Ubuntu 22.04

## Step 2 
The Miyoo uses a custom firmware based around buildroot and Linux.
To compile programs for it, we'll need to get buildroot in order to cross-compile programs for the Miyoo.

For downloadable pre-built packages/binaries of the toolchain/SDK [see here](https://github.com/TriForceX/MiyooCFW/wiki/Get-the-prebuilt-SDK-from-GH-actions).

If you wish to compile the toolchain/SDK from source, [see here](https://github.com/TriForceX/MiyooCFW/wiki/Build-Image-and-SDK)

## Step 3
Create a folder for your project with your game's source code and create a "Makefile" for it.
Here's the one that crait used for the Midnight Wild game:

```
CHAINPREFIX= /opt/miyoo/
CROSS_COMPILE=$(CHAINPREFIX)/bin/arm-linux-

CC = $(CROSS_COMPILE)gcc
CXX = $(CROSS_COMPILE)g++
STRIP = $(CROSS_COMPILE)strip
SYSROOT     := $(shell $(CC) --print-sysroot)
SDL_CFLAGS  := $(shell $(SYSROOT)/usr/bin/sdl-config --cflags)
SDL_LIBS    := $(shell $(SYSROOT)/usr/bin/sdl-config --libs)

OUTPUTNAME = midnightwild/midnightwild.elf

DEFINES = -DHAVE_STDINT_H -DVERSION_BITTBOY
INCLUDES = -Iinclude $(SDL_CFLAGS)
OPT_FLAGS  = -Ofast -fdata-sections -fdata-sections -fno-common -fno-PIC -flto
EXTRA_LDFLAGS = -lasound -lmikmod -lmodplug -Wl,--as-needed -Wl,--gc-sections -flto -s

CFLAGS = $(DEFINES) $(INCLUDES) $(OPT_FLAGS) -std=gnu11 
CXXFLAGS = $(DEFINES) $(INCLUDES) $(OPT_FLAGS) -std=gnu++11 
LDFLAGS = -Wl,--start-group -lSDL -lSDL_image -lpng -ljpeg -lSDL_mixer -lfreetype -lSDL_ttf -logg -lvorbisidec -lmikmod -lmodplug -lm -pthread -lz -lstdc++ $(EXTRA_LDFLAGS) -Wl,--end-group

# Redream (main engine)
OBJS =  \
	src/main.o

.c.o:
	$(CC) $(CFLAGS) -c -o $@ $< 

.cpp.o:
	$(CXX) $(CXXFLAGS) -c -o $@ $< 

all: $(OBJS)
	$(CC) -o $(OUTPUTNAME) $(OBJS) $(CFLAGS) $(LDFLAGS)

clean:
	rm -f $(OBJS) $(OUTPUTNAME)
```

## Step 4

Build your software with "make" in the terminal and you should be good to go!

Do you want to find a good example of some source code for the BittBoy? Check out pingflood's IOTester: https://github.com/pingflood/iotester

If you want more support or questions join our **Discord** chat server [here](https://discord.gznetwork.com/)