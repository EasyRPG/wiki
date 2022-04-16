---
title: "Compiling Player for Nintendo Wii"
---
For compiling EasyRPG Player for your Wii you will need [devkitpro](http://sourceforge.net/projects/devkitpro/).

And you will need the following libraries:

-   SDL (\>=1.2.10).
-   SDL_mixer (\>=1.2.6) with support for WAV, MIDI, OGG and MP3.

Precompiled SDL-libs can be found on the website from [SDL Wii](https://code.google.com/p/sdl-wii/downloads/list).

-   libpng (\>=1.2.8).
-   zlib (\>=1.2.2).
-   freetype (\>=2.4.3).

They can be found in the [devkitpro portlibs](http://sourceforge.net/projects/devkitpro/files/portlibs/).

-   iconv
-   pixman
-   expat

Recent versions can be found here: <https://github.com/carstene1ns/portlibs-wii>

You need to build liblcf as portlib:

``` bash
cd liblcf
./configure --host=powerpc-eabi --prefix="$DEVKITPRO/portlibs/ppc" \
            --disable-shared --enable-static \
            CFLAGS="-g -O2 -Wall -DGEKKO -mcpu=750 -meabi -mhard-float"
make install
```

Once you have all dependencies above, change into the player/builds/wii folder and type 'make'. It will build a boot.dol that you can place on your sd card alongside meta.xml, icon.png and a game. That's all!

#### Notes about music playback (Ogg, Midi)

There can be some linker problems with SDL_mixer when ogg is enabled, either try to compile an ogg lib (and link against -lvorbisfile -lvorbis -lvorbisenc -logg) or recompile SDL_mixer without ogg support (remove -DOGG_MUSIC from the Makefile).

For midi you should also patch some lines in the sdl_mixer-timidity-folder (or you will have to put 20mb of "instruments" in the game root):

`common.c:116: (add the lines)`  
`add_to_pathlist("sd:/data/timidity");`  
`add_to_pathlist("usb:/data/timidity");`

`config.h:173: (change the lines)`  
`#define CONFIG_FILE "sd:/data/timidity/timidity.cfg`  
`#define CONFIG_FILE_ETC "usb:/data/timidity/timidity.cfg`
