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
## Contributors

- [SwedishGojira](http://github.com/swedishgojira)
- [Rob Loach](http://github.com/robloach)
- [Alcaro](https://github.com/Alcaro)
