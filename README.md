
# Open PS2 Loader (OPL)

Open PS2 Loader (OPL) is an open-source game and application loader for Sony PlayStation 2 consoles. It provides a unified interface for launching supported games and homebrew applications from multiple storage devices.

OPL is a homebrew application, not a replacement for the PlayStation 2 system firmware. It does not install a custom operating system or modify the console's firmware as a CFW would.

## Core Capabilities

- Load supported PlayStation 2 game images from USB storage.
- Load games from network shares using SMBv1.
- Access games stored on internal HDDs connected through the PS2 expansion-bay interface.
- Support MX4SIO SD-card storage adapters.
- Support compatible IEEE 1394 / i.LINK storage devices.
- Launch homebrew applications in ELF format.
- Configure virtual memory cards.
- Apply per-game configuration settings.
- Customize the interface with themes and language files.

## Storage Interfaces

OPL supports several storage interfaces:

| Interface | Description |
|---|---|
| USB | USB mass-storage devices |
| SMB | Network shares using SMBv1 |
| HDD | ATA/PATA/IDE or SATA storage through a compatible expansion-bay adapter |
| MX4SIO | SD-card storage connected through a memory-card-port adapter |
| i.LINK | Compatible IEEE 1394 / SBP-2 storage devices |

Feature availability depends on the OPL build, console hardware, storage adapter, and configuration.

## Supported File Formats

OPL supports multiple formats for games and applications, including:

- ISO disc images
- ZSO compressed disc images
- USB Extreme (`.ul`) format
- ELF homebrew applications
- HDLoader format for supported expansion-bay HDD configurations

For USB and MX4SIO devices, supported filesystem and partition-table combinations depend on the OPL build. The project documentation describes FAT32 and exFAT support, as well as MBR and GPT partition tables.

## Application Architecture

OPL is organized around several functional areas:

### Loader Core

Coordinates device discovery, game listing, configuration handling, and launch operations.

### Storage Backends

Provide access to supported storage sources, including USB mass storage, SMB network shares, internal HDDs, MX4SIO, and compatible i.LINK devices.

### Game Configuration

Stores per-title settings and related configuration data.

### Virtual Memory Cards

Provides virtual memory card support through image files stored on supported devices.

### Application Launcher

Allows users to organize and launch homebrew applications compiled in ELF format.

### User Interface

Provides the game browser, device selection, themes, language resources, and configuration menus.

## Directory Structure

OPL uses a directory layout for game images, applications, configuration files, artwork, themes, and other resources.

| Directory | Purpose |
|---|---|
| `CD` | CD-format game images |
| `DVD` | DVD-format game images |
| `VMC` | Virtual memory card images |
| `CFG` | Per-game configuration files |
| `ART` | Game artwork |
| `THM` | Interface themes |
| `LNG` | Language resources |
| `CHT` | Cheat configuration files |
| `APPS` | ELF homebrew applications |

The directory structure and supported storage modes may vary by device type.

## Additional Features

Depending on the build, OPL may include:

- GSM (GS Mode Selector) video output configuration
- In-game reset functionality
- Virtual memory card management
- PADEMU controller emulation
- In-game screenshot functionality in applicable builds
- Parental controls
- Per-game configuration profiles
- Multiple interface languages
- Custom themes

Some features are build-specific and should not be assumed to be present in every release.

## Build Variants

The project provides different build configurations. Examples documented by the project include:

| Build type | Description |
|---|---|
| Release | Standard release configuration with the project's integrated feature set |
| DTL_T10000 | Build intended for PlayStation 2 development tools |
| IGS | Build with in-game screenshot functionality |
| PADEMU | Build with controller emulation features |
| RTL | Build with right-to-left language support |

Check the release notes and included files before selecting a build.

## PlayStation 3 Compatibility

OPL can also be used on certain PlayStation 3 models with hardware-based PlayStation 2 backward compatibility.

The project's documentation identifies supported PS3 board revisions:
- COK-001
- COK-002
- COK-002W

Running OPL on a compatible PS3 requires an appropriate entry point for launching PS2 software. Support is limited to the documented backward-compatible hardware and supported operating configurations.

## Installation Overview

1. Obtain an OPL build from the official project repository or its linked release resources.
2. Prepare a supported storage device and filesystem.
3. Copy the OPL application to a location accessible to the console's homebrew launch environment.
4. Configure the required storage source.
5. Place supported game images and application files in the appropriate directories.
6. Launch OPL and configure the device settings.

The exact installation method depends on the console model, homebrew entry point, storage interface, and selected OPL build.

## Development

OPL is an open-source project developed for PlayStation 2 hardware.

The project repository contains the source code and development information. The project documentation identifies the PlayStation 2 SDK (PS2SDK) as a build requirement.

Development areas include:

- Storage interface support
- Game and application loading
- Device compatibility
- User interface development
- Configuration management
- Runtime features and integrations

## Project Information

| Property | Value |
|---|---|
| Project | Open PS2 Loader |
| Abbreviation | OPL |
| Platform | Sony PlayStation 2 |
| Additional platform support | Compatible PlayStation 3 models with PS2 backward compatibility |
| Project type | Open-source game and application loader |
| Primary language | C |
| License | Academic Free License 3.0 |
| Official repository | https://github.com/ps2homebrew/Open-PS2-Loader |

## Resources

- Source code: https://github.com/ps2homebrew/Open-PS2-Loader
- Releases: https://github.com/ps2homebrew/Open-PS2-Loader/releases
- Project website: https://www.ps2homebrew.org/Open-PS2-Loader/
- User guide: https://www.ps2homebrew.org/Open-PS2-Loader-User-Guide/

---

Open PS2 Loader is a modular homebrew loading environment for PlayStation 2, bringing together multiple storage backends, game image formats, application launching, and configurable runtime features.
