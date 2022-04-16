---
title: "Building the GCW Zero Toolchain"
---
For our [Jenkins build server](https://ci.easyrpg.org/) we needed a modified toolchain, that does not depend to be installed in `/opt`. The following instructions have been written along the way and should result in a working toolchain that is suitable to get a working EasyRPG Player build.

*Prerequisites*: I assume you do all the steps in a seperate build directory to not interfere with old toolchains and other stuff. Also you need some development tools installed on your machine, for example `gcc`, `make` and `subversion`. The buildroot will warn you, when you forgot to install something, though.

First, we need the buildroot from GitHub and change into the directory:

``` bash
git clone https://github.com/gcwnow/buildroot.git
cd buildroot
```

To use the default configuration:

``` bash
make gcw0_defconfig
```

**Optionally**, we can use a previously saved config file, just copy it to `.config`. We need to add newly available options then:

``` bash
make oldconfig
```

We configure the packages to be build and available options:

``` bash
make menuconfig
```

There are also the graphical frontends `xconfig`, using qt and `gconfig`, using gtk.

Most of the libraries and stuff under "Target Packages" are not needed, so we disable them to save some time while compiling. Needed libraries are `sdl`, `sdl_mixer` and `icu`.

Now the important step: change the toolchain directory from `/opt/gcw0-toolchain` to your desired directory under "Build Options" --\> "Host Dir". (`BR2_HOST_DIR="/home/jenkins/gcw0-toolchain"` in .config)

To speed up the build further, set the parallel make jobs to the cores of your cpu "Number of jobs to run simultaneously (0 for auto)". (`BR2_JLEVEL=2` in .config)

To speed up possibly rebuilds, enable `ccache` "Enable compiler cache". (`BR2_CCACHE=y` and `BR2_CCACHE_DIR="$(HOME)/.buildroot-ccache"` in .config)

When all things are set up, we can start the build and get something to drink in the meanwhile =)

``` bash
nice -n19 make
```

Afterwards, there should be a new, shiny toolchain in the directory you chose.

## Cross-compile pixman

Pixman is a needed library and not part of the toolchain.

Download [the latest release](http://cairographics.org/releases/) and extract it.

Then it is the normal auto-tools-based build steps:

``` bash
cd pixman-*/
./configure --host=mipsel-linux --prefix=/usr
make
make DESTDIR=/home/jenkins/gcw0-toolchain/usr/mipsel-gcw0-linux-uclibc/sysroot/ install
```

Be sure to install it in the sysroot directory to ensure it is found when compiling target packages.
