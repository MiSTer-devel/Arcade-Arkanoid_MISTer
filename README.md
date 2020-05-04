# Arkanoid for [MISTer](https://github.com/MiSTer-devel/Main_MiSTer/wiki)
An FPGA implementation of Arkanoid by Ace, ElectronAsh, enforcer831 and Kitrinx

## Features
- Modelling done at the chip level to match PCB behavior and logic as closely as possible
- Mouse and keyboard controls
- T80s CPU by Daniel Wallner with fixes by MikeJ, Sorgelig, and others
- YM2149 core with volume table mixing by MikeJ for accurate mixing down to the PCB's audio distortion

## Installation
Place `*.rbf` and `a.arkanoid.rom` in the root of your SD card.

## Controls
### Keyboard
| Key | Function |
| --- | --- |
| 1 | 1-Player Start |
| 2 | 2-Player Start |
| 5, 6 | Coin |
| 9 | Service Credit |

### Mouse
| Mouse action | Function |
| --- | --- |
| Left button | Fire |
| Left/Right | Movement |

## Known Issues
1) The game contains an MC68705 MCU which is currently not implemented
2) The required ROMs have a few bugs that the included IPS patch aims to correct, however, the difficulty settings have no effect, so the game is always on Hard difficulty
3) Analog output is limited to native resolution and timings (240p at 59.18Hz)
4) Resolution is incorrectly reported as 9x225 or 10x225

## Building the ROM
### ****ATTENTION****
ROMs are not included. In order to use this arcade, you need to provide the
correct ROMs.

To simplify the process .mra files are provided in the releases folder, that
specifies the required ROMs with checksums. The ROMs .zip filename refers to the
corresponding file of the M.A.M.E. project.

Please refer to https://github.com/MiSTer-devel/Main_MiSTer/wiki/Arcade-Roms for
information on how to setup and use the environment.

Quickreference for folders and file placement:

/_Arcade/<game name>.mra
/_Arcade/cores/<game rbf>.rbf
/_Arcade/mame/<mame rom>.zip
/_Arcade/hbmame/<hbmame rom>.zip
