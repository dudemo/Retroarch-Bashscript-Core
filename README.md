# Retroarch-Bashscript-Core
Based on [libretro-dolphin-launcher](https://github.com/RobLoach/libretro-dolphin-launcher).

Launch Bash-scripts directly from [RetroArch](http://www.libretro.com/) to launch your Linux games. Usable on the Arcade Legends Ultimate if used properly.


## Installation

1. Compile the core
  ``` bash
  git clone https://github.com/dudemo/Retroarch-Bashscript-Core.git
  cd libretro-bash-launcher
  make
  ```

2. Compile a bash script to launch whatever you would like to launch on the Legends Ultimate.
  ``` bash
  This can literally be whatever you want, but you must compile the required libraries
  and binaries and link them inside the script you intend to build into the UCE.
  ```

## Usage

  ``` bash
- Open AddOn Tool. 
- Create a game title (AddOn_XXXXX)
- Create or find boxart and select it
- Create or find bezel art and select it
- Select the built core
- When you select your game ROM, in the lower right hand corner, select the filetype drop-down and select 
   "Any file type". Now select your script.
- Build the UCE
- Put the resulting UCE on a USB drive and run AddOn X Tool on the drive
- Open the UCE in CoinOPS X
  ```
  
## Structure

  ``` bash
+----------+ 
|   PKG    | <-- name the root directory whatever you want, in the example above,
+---+------+      it would be "AddOn_OverlayFS"
    |
    |   +---------+ 
    +-- |   emu   |  <-- subdirectory for emulators' *.so and config files
    |   +---------+      (So far I have encountered no reason for anything but the .so file here)
    |
    |   +---------+ 
    +-- |   roms  |  <-- subdirectory for the game files 
    |   +---------+      this example uses the "overlayfs.sh" script
    |                    
    |   +---------+ 
    +-- | boxart  |  <-- subdirectory for boxart, "boxart.png" is the default name.
    |   +---------+
    |
    |   +---------+ 
    +-- |  save   |  <-- subdirectory for gamesave files
    |   +---------+	 go ahead and leave this empty for now as well
    |   
    +--  title       <-- symbolic link to "boxart/boxart.png"
    |   
    +--  cartridge.xml  <-- info header for menu display. *in XML format
    |   
    +--  exec.sh        <-- the script file to run emulator and game files.
                            the example contains:
                            /emulator/retroplayer ./emu/genesis_plus_gx_libretro.so "./roms/overlayfs.sh"

NOTE: You can add folders to this structure as necessary. 
  ```

## Example UCE exec.sh script

``` bash
#!/bin/sh

set -x
/emulator/retroplayer ./emu/bash_launcher_libretro.so "./roms/overlayfs.sh"
  ```

## Contributors

- [SwedishGojira](http://github.com/swedishgojira)
- [Rob Loach](http://github.com/robloach)
- [Alcaro](https://github.com/Alcaro)
