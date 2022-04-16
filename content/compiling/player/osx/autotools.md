---
title: "Building Player on OS X with Autotools"
---
Build and install liblcf:

-   [../../liblcf/osx/autotools](..//../liblcf/osx/autotools)

Install requirements with Homebrew:

    brew install libpng libvorbis sdl2 sdl2_mixer pixman freetype

Download Player sources from git:

    git clone https://github.com/EasyRPG/Player

Enter to the Player folder:

    cd Player

Set up pkgconfig to see expat and icu4c configurations:

    export PKG_CONFIG_PATH="/usr/local/opt/icu4c/lib/pkgconfig:/usr/local/opt/expat/lib/pkgconfig:$PKG_CONFIG_PATH"

Generate configure script:

    autoreconf -i

Generate Makefile:

    ./configure

Build:

    make -j4

Install:

    sudo make install
