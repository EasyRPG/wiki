---
title: "Logo"
---
# Logo

The Logo-Scene is the first scene executed on startup. It displays the shiny EasyRPG Logo :) and waits for three seconds. After the wait time it will push the [Title-Scene](/development/player/scenes/title) on the stack.

### Known Issues

The logo scene is usually not showing the fade out. That's because the Title-Scene parses the database which is a blocking operation. This causes a frameskip in the graphic system.

### Files

-   scene_logo.cpp
-   scene_logo.h
