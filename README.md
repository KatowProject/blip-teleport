# GTA San Andreas Radar Blip Teleport

A lightweight CLEO script for **Grand Theft Auto: San Andreas 1.0 US** that allows CJ to teleport to the first valid coordinate-based radar blip by pressing **F6**.

The script reads the game's radar blip table directly from memory and only performs **read-only memory access** when searching for a destination.

## Features

- Teleport CJ to a coordinate-based radar blip with **F6**
- Automatically moves CJ's vehicle together with him when applicable
- Ignores:
  - Shop icons
  - Safehouse icons
  - Player-created waypoint
  - Vehicle blips
  - Pedestrian blips
  - Object/entity blips
- Uses the first matching radar blip found in the game's radar table
- Does nothing when no valid coordinate blip is available
- Includes coordinate validation to reject invalid or unreasonable values
- Supports installation through **Mod Loader**
- Designed for **GTA San Andreas 1.0 US**

## Requirements

- GTA San Andreas **1.0 US**
- [CLEO](https://cleo.li/)
- [Mod Loader](https://www.mixmods.com.br/2015/04/mod-loader/)
- [Sanny Builder 4](https://sannybuilder.com/) if compiling the source yourself

## Installation

### Using Mod Loader

Create a folder inside your GTA San Andreas installation:

```text
modloader/
└── RadarBlip Teleport/
    └── RadarBlip_Teleport.cs
```

### Build and Release

`RadarBlip_Teleport.txt` is the Sanny Builder source code and should remain in the repository. The `.cs` file is the compiled binary installed through Mod Loader, so it does not need to be stored in the repository.

The GitHub Actions workflow automatically compiles the source and adds `RadarBlip_Teleport.cs` to the GitHub Release whenever a release is published. Create a release with a version tag, such as `v1.0.0`.

To build manually with Sanny Builder 4:

```text
sanny.exe --mode sa_sbl --compile RadarBlip_Teleport.txt RadarBlip_Teleport.cs
```