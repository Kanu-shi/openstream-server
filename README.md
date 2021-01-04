# Open-Stream 

Open source low latency stream solution. 
Open Stream is a fork open Sunshine Server. Creating open source solution for Gaming and Desktop Management.

-----
# JoeJonnyBoy75 Fork 

This fork is focused on bringing more configuration options to the user interface, including
fixes for the existing AMF options.

### Project structure

- root folder: contains the GUI application. 
- `openstreamhost` folder: contains the streaming **host** application. Includes `git` submodules. 

### Building

#### Windows build requirements
- Windows 10 64 bits.
- [`Msys2`](https://www.msys2.org/) development platform.
- `Qt SDK` for `Msys2` [Qt packages](https://wiki.qt.io/MSYS2#Obtain_Pre-Built_Qt_.26_QtCreator_binary_files_and_Use_instantly_without_Building.2FCompiling)

#### Steps followed by developer

- Install [`Msys2`](https://www.msys2.org/) development platform. 
- Install required modules via the following command in MinGW64
``` 
 pacman -S mingw-w64-x86_64-openssl mingw-w64-x86_64-cmake mingw-w64-x86_64-toolchain mingw-w64-x86_64-ffmpeg mingw-w64-x86_64-boost
``` 
- Install Static QT via the following command in MinGW64
``` 
 pacman -S mingw-w64-i686-qt5-static mingw-w64-x86_64-qt5-static
```     
#### Build the project using QtCreator: 
- Open the project using the `CMake` support and selecting the `CMakeList` file in root folder.
- Select building kit `MinGW-w64 64bit (MSYS2)`
- Build the application to produce the executable files. These executable files will be required for packaging a new release installer. Go to `installer` folder to find the installer building instructions.
