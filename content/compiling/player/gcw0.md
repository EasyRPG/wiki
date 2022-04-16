---
title: "Compiling Player for GCW Zero"
---
You need to setup the gcw0 buildroot first: Download a precompiled toolchain from <http://www.gcw-zero.com/develop>.

[You need to cross-compile pixman](/development/compiling/toolchains/gcw0#cross-compile-pixman).

Download Player and liblcf from GitHub:

``` bash
git clone --depth=1 https://github.com/EasyRPG/Player.git
cd Player/libs
git clone --depth=1 https://github.com/EasyRPG/liblcf.git
cd ..
```

Change into the `builds/opendingux` folder and start the build:

``` bash
cd builds/opendingux
make
```

If no error occured, there will be an EasyRPG executable in the `gcw-zero` subdirectory. To build an opk ready to deploy to the device:

``` bash
cd gcw-zero
./opk_build.sh
```
