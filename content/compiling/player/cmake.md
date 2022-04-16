---
title: "Building Player with CMake"
---
## Requirements

-   cmake-2.8 or greater
-   SDL2
-   SDL2_mixer
-   Freetype
-   Pixman
-   libpng
-   zlib
-   boost (**only for 0.4.1**, later versions don't require boost)
-   OpenAL
-   FluidSynth
-   Ruby
-   Doxygen (optional)
-   [liblcf](..//liblcf/cmake)

## Build

-   Run "cmake \${PATH TO player} && make".
-   If you want to build it with debug mode pass "-D CMAKE_BUILD_TYPE=Debug" to cmake.
