---
title: "Compiling Player for PlayStation Portable"
---
## Toolchain Requirement

For compiling EasyRPG Player for your PSP (PlayStation Portable) you will need the PSP SDK compiled with:

-   GCC 4.3.2 or later
-   Newlib 1.18 or later with support for libiconv.

## Library Requirement

You will need the following libraries:

-   SDL (\>=1.2.10).
-   SDL_image (\>=1.2.4) with support for BMP, PNG and JPG.
-   SDL_mixer (\>=1.2.6) with support for WAV, MIDI, OGG and MP3.
-   SDL_gfx (\>=2.0.13).
-   SDL_ttf (\>=2.0.7).
-   Independent JPEG (\>=6b 27-Mar-1998).
-   libpng (\>=1.2.8).
-   zlib (\>=1.2.2).
-   freetype (\>=2.4.3).
-   libvorbis (\>=1.3.2).
-   libmad (\>=0.15.1).
-   libmikmod (\>=3.1.11).

## Building

Once you have all dependencies above, just type '\$ make' in the builds/psp/ directory and it will build the EBOOT.PBP. That's all!

## Pixman support

1.  Get pixman-0.20.2 and extract it.
2.  Get config.sub from whatever PSP port that uses "configure" and copy it.
3.  Run " LDFLAGS="-L\$(psp-config --pspsdk-path)/lib" LIBS="-lc -lpspuser" ./configure --host psp --prefix=\$(psp-config --psp-prefix) && make && sudo make install"
