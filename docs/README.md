[![Pooyan Logo](pooyan-logo.png)](#)

---

[![Active Development](https://img.shields.io/badge/Maintenance%20Level-Actively%20Developed-brightgreen.svg)](#status-of-features)
[![Build](https://github.com/opengateware/arcade-pooyan/actions/workflows/build-pocket.yml/badge.svg)](https://github.com/opengateware/arcade-pooyan/actions/workflows/build-pocket.yml)
[![release](https://img.shields.io/github/release/opengateware/arcade-pooyan.svg)](https://github.com/opengateware/arcade-pooyan/releases)
[![license](https://img.shields.io/github/license/opengateware/arcade-pooyan.svg?label=License&color=yellow)](#legal-notices)
[![issues](https://img.shields.io/github/issues/opengateware/arcade-pooyan.svg?label=Issues&color=red)](https://github.com/opengateware/arcade-pooyan/issues)
[![stars](https://img.shields.io/github/stars/opengateware/arcade-pooyan.svg?label=Project%20Stars)](https://github.com/opengateware/arcade-pooyan/stargazers)
[![discord](https://img.shields.io/discord/676418475635507210.svg?logo=discord&logoColor=white&label=Discord&color=5865F2)](https://chat.raetro.org)
[![Twitter Follow](https://img.shields.io/twitter/follow/marcusjordan?style=social)](https://twitter.com/marcusjordan)

## Konami [Pooyan] Compatible Gateware IP Core

This Implementation of a compatible Pooyan arcade hardware in HDL is the work of [Dar](https://github.com/darfpga).

## Overview

Pooyan (プーヤン) is a fixed shooter arcade game released by Konami in Japan in 1982. It was manufactured in North America by Stern Electronics.

The player takes on the role of a bow-and-arrow welding pig who must protect her piglets from the pack of hungry wolves ballooning up or down the cliff face. The pig is suspended in a winch-controlled cage and must move vertically up and down, shooting the balloons and sending the wolves plummeting to the ground. Any wolves she misses will, having safely reached the ground, climb a ladder to try and bite her. Also, if any of the wolves reach the ground, more piglets will be captured by them. Mother Pig must try to kill as many wolves as possible without letting them reach the ground.

On the second level, the wolves use balloons to float upwards to the top of a high cliff. If enough of them reach the cliff, they will push a huge boulder down onto Mother Pig's cage. After this level has been completed, the piglets who have been captured are rescued and the game starts over with increased difficulty.

There is also a bonus round where Mother Pig will attempt to eliminate as many wolves on ascending balloons as possible by throwing as few slabs of meat as possible for a maximum bonus score.

## Technical specifications

- **Main CPU:**     Zilog Z80 @ 3.72 MHz
- **Sound CPU:**    Zilog Z80 @ 1.789772 MHz
- **Sound Chip:**   (2x) General Instrument AY8910 @ 1.789772 Mhz
- **Resolution:**   256×224, 256 colors
- **Display Box:**  256×256 @ 3.93216 MHz
- **Aspect Ratio:** 8:7
- **Orientation:**  Vertical (90º)

## Compatible Platforms

- Analogue Pocket

## Compatible Games

> **ROMs NOT INCLUDED:** By using this gateware you agree to provide your own roms.

| **Game**                   | Region | Status |
| :------------------------- | :----: | :----: |
| Pooyan                     |  JPN   |   ✅   |
| **Alternatives**           |        |        |
| Pooyan (Stern Electronics) |  USA   |   ✅   |
| Pootan (Bootleg)           |  JPN   |   ✅   |
| **Homebrews**              |        |        |
| Pooyan Tester              |        |   ✅   |

### ROM Instructions

1. Download and Install [ORCA](https://github.com/opengateware/tools-orca/releases/latest) (Open ROM Conversion Assistant)
2. Download the [ROM Recipes](https://github.com/opengateware/arcade-pooyan/releases/latest) and extract to your computer.
3. Copy the required MAME `.zip` file(s) into the `roms` folder.
4. Inside the `tools` folder execute the script related to your system.
   1. **Windows:** right click `make_roms.ps1` and select `Run with Powershell`.
   2. **Linux and MacOS:** run script `make_roms.sh`.
5. After the conversion is completed, copy the `Assets` folder to the Root of your SD Card.
6. **Optional:** an `.md5` file is included to verify if the hash of the ROMs are valid. (eg: `md5sum -c checklist.md5`)

> **Note:** Make sure your `.rom` files are in the `Assets/pooyan/common` directory.

## Status of Features

> **WARNING**: This repository is in active development. There are no guarantees about stability. Breaking changes might occur until a stable release is made and announced.

- [x] Dip Switches
- [x] Pause
- [ ] Hi-Score Save

## Credits and acknowledgment

- [Alan Steremberg](https://github.com/alanswx)
- [Alexey Melnikov](https://github.com/sorgelig)
- [Daniel Wallner](https://opencores.org/projects/t80)
- [Dar](https://github.com/darfpga)
- [MikeJ](https://github.com/Takasa)

## Powered by Open-Source Software

This project borrowed and use code from several other projects. A great thanks to their efforts!

| Modules                        | Copyright/Developer     |
| :----------------------------- | :---------------------- |
| [Data Loader]                  | 2022 (c) Adam Gastineau |
| [Pooyan RTL]                   | 2017 (c) Dar            |
| [T80]                          | 2001 (c) Daniel Wallner |
| YM2149                         | 2005 (c) MikeJ          |

## Legal Notices

Pooyan © 1982 Konami Industry Company, Limited.
All trademarks, logos, and copyrights are property of their respective owners.

The authors and contributors or any of its maintainers are in no way associated with or endorsed by Konami.

[Data Loader]: https://github.com/agg23/analogue-pocket-utils
[Pooyan RTL]: https://github.com/MiSTer-devel/Arcade-Pooyan_MiSTer/tree/master/rtl
[T80]: https://opencores.org/projects/t80

[Pooyan]: https://en.wikipedia.org/wiki/Pooyan
