# Version 1.3.3

---

## How to build your own games
This is an small guide to start making games for Bittboy/PocketGo (not for beginners). Thanks to **crait** for this guide and **gameblabla** for his updates.

## SDL 1.2 keys (MiyooCFW 1.3.3)
Physical button bindings for Miyoo 1'st gen consoles (Bittboy's in round brackets)

Button | SDLKey 
:-----: | :-----: 
A (TA) | SDLK_LALT
B (A) | SDLK_LCTRL
X (TB) | SDLK_LSHIFT 
Y (B)| SDLK_SPACE
L1 | SDLK_TAB
R1 | SDLK_BACKSPACE 
L2 | SDLK_PAGEUP
R2 | SDLK_PAGEDOWN
RESET | SDLK_RCTRL
START | SDLK_RETURN
SELECT | SDLK_ESCAPE
UP/DOWN | SDLK_UP/DOWN
LEFT/RIGHT | SDLK_LEFT/RIGHT

To check correctness of this table use [I/O tester](https://github.com/Apaczer/iotester/releases/latest) on your handheld.

## Step 1

Since we're working with Linux-based devices, you're going to need to run a Linux distribution.
So, if you're on Windows, you'll need to install a Virtual Machine, Cygwin, WSL or something like that.

crait uses Virtualbox along with Xubuntu 18.04 but you can also use mostly any linux distribution as long as it's not too old and that GCC, make and bison are available on it. 

I'm using Void linux on my machine myself so most linux distributions should work.

## Step 2 

The BittBoy uses a custom firmware based around buildroot and Linux.
To compile programs for it, we'll need to get buildroot in order to cross-compile programs for the Bittboy/PocketGo.



For downloadable pre-built packages/binaries of the toolchain/SDK [see here](https://github.com/MiyooCFW/toolchain/releases).


If you wish to compile the toolchain/SDK from source, be sure you have the following dependencies:
`bison`, `make`, `gcc`.
You will also need at least 10GB of free space before you can proceed.
Run the following commands in the terminal :

```
sudo mkdir /opt/miyoo
cd /opt/miyoo
sudo git clone https://github.com/MiyooCFW/toolchain.git

cd toolchain
sudo make sdk
```

Warning : this can take a long time ! (a few hours depending on your machine)

## Step 3

Once compiling the toolchain is done, go to the "output" folder and then inside of that, go to the "host" folder.
Now grab the content of that folder inside and put it in /opt/miyoo/.

(Note that the contents of /opt are usually not writable by normal users, so you may need to become administrator/root.)

The easiest way of doing this step is via the terminal:

```
sudo mv /opt/miyoo/toolchain/output/host/* /opt/miyoo/
```

## Step 4

Create a folder for your project with your game's source code and create a "Makefile" for it.
Here's the one that crait used for the Midnight Wild game:

```
CHAINPREFIX= /opt/miyoo/
CROSS_COMPILE=$(CHAINPREFIX)/bin/arm-buildroot-linux-musleabi-

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


## Step 5

Build your software with "make" in the terminal and you should be good to go!

Do you want to find a good example of some source code for the BittBoy? Check out pingflood's IOTester: https://github.com/pingflood/iotester

If you want more support or questions join our **Discord** chat server [here](https://discord.gznetwork.com/)