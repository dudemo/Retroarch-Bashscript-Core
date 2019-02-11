# libretro-bash-launcher
Based on [libretro-dolphin-launcher](https://github.com/RobLoach/libretro-dolphin-launcher).

Launch Bash-scripts directly from [RetroArch](http://www.libretro.com/) to launch your Linux games.

![Bash Launcher Screenshot](screenshot.jpg)

## Installation

1. Compile the core
  ``` bash
  git clone https://github.com/SwedishGojira/libretro-bash-launcher.git
  cd libretro-bash-launcher
  make
  ```

2. Copy the core file to the RetroArch cores directory (Path may differ depending on distribution. Check your system for correct path.)
  ``` bash
  cp bash_launcher_libretro.so /usr/lib/libretro/
  ```

## Usage

1. Scan Bash-scripts in RetroArch

2. Launch the script directly from the RetroArch menu

3. Alternatively, you can run games through the command line
  ``` bash
  retroarch -L bash_launcher_libretro.so script.sh
  ```

## Contributors

- [SwedishGojira](http://github.com/swedishgojira)
- [Rob Loach](http://github.com/robloach)
- [Alcaro](https://github.com/Alcaro)
