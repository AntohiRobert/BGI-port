# Statically linked sdl2 library plus sdl_bgi
Two examples of hello world-ish windows, sdl2 statically linked.  
One example of bgi program(with Graphics.h)  
Uses latest stable release on unofficial github mirror for sdl2.  
Tested on: 
 * Windows 10, CLion 2020.2.4
 * MacOS Big Sur, CLion 2020.2.4
 * ArchLinux, CLion 2020.2.4
 
Submodule sdl-bgi mirror isn't used at all, just copied sources to src, left sdl-bgi for documentation.  
To update sdl-bgi:
* Download new sdl-bgi release either from a Github Mirror or http://libxbgi.sourceforge.net/
* Replace sdl-bgi folder with the new one(or don't,it isn't used)
* Copy graphics.h, SDL_bgi.h and SDL_bgi.c to src
* Remove "SDL2/" from include in the above mentioned files, leave just header files