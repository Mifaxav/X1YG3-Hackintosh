# X1YG3-Hackintosh

**Status: Maintained**

Supported OS's: Sonoma

Highest supported OS: 14.2.1

Master doesnt have much, check the releases :D

Even if it shows a release released a while ago, please check the releases tab as i frequently upload pre releases which dont show up.

[![OpenCore](https://img.shields.io/badge/OpenCore-1.0.0-blue.svg)](https://github.com/acidanthera/OpenCorePkg)
[![macOS-stable](https://img.shields.io/badge/macOS-14.2.1-forest_green.svg)](https://www.apple.com/macos/sonoma)

**DISCLAIMER:**
Read the entire README and Dortania guides before you start. I am not responsible for any damage.
When you encounter bug or want to improve this repo, consider opening issue or pull request. 
If you find this bootloader configuration useful, consider giving it a star to make it more visible.

## Introduction

<details> 

<summary><strong>General knowledge & credits</strong></summary>

- To install macOS follow the guides provided by [Dortania](https://dortania.github.io/getting-started/)

- Useful tools by [CorpNewt](https://github.com/corpnewt) and [headkaze](https://github.com/headkaze/Hackintool)

[![UEFI](https://img.shields.io/badge/UEFI-N24ET61W-lightgrey)](https://pcsupport.lenovo.com/us/en/products/laptops-and-netbooks/thinkpad-t-series-laptops/thinkpad-t480-type-20l5-20l6/downloads/ds502355)
| Category  | Component                            | Note                                                                                                               |
| --------- | ------------------------------------ | ------------------------------------------------------------------------------------------------------------------ |
| CPU       | Intel(R) Core(TM) i7-8650U @ 1.90GHz |                                                                                                                    |
| GPU       | Intel UHD 620                        |                                                                                                                    |
| SSD       | Silicon Power P34A60 1TB NVMe        | Works perfectly with latest NVMeFix.kext                                                                           |
| Memory    | 16GB LPDDR3 2400Mhz(Soldered)        |                                                                                                                    |
| Battery   | Single battery                       | Shows up accurately under mac, lasts 4 - 5 hours                                                                   |
| Camera    | 720p Camera                          |                                                                                                                    |
| Wifi & BT | BCM93452Z                            | Broadcom is native.                                                                                                |                     
| Input     | PS2 Keyboard & Synaptics TrackPad    | [YogaSMC](https://github.com/zhen-zen/YogaSMC) for media keys like microphone switch, etc. PrtSc is mapped as F13. |


| Component      | Version        |
| -------------- | -------------- |
| OpenCore       | v0.1.0         |
| MacOS Sonoma   | 14.2.1 (23C71) |


| Kext                   | Comment        
|:---------------------- | ------------------------------      
| AppleALC               | Latest Speaker drivers
| BrightnessKeys         | Latest         
| HibernationFixup       | Latest                
| IntelMausi             | Latest Ethernet controller
| Lilu                   | Latest         
| NoTouchID              | Latest         
| NVMeFix                | Latest NVMe SSD fix
| RTCMemoryFixup         | Latest Real time clock fix
| VirtualSMC             | Latest         
| VoodooPS2Controller    | Latest         
| VoodooRMI              | Latest         
| VoodooI2C              | Latest Touchscreen drivers
| VooDooI2CHID           | Latest Intel satellite kext
| VoodooSMBus            | Latest         
| WhateverGreen          | Latest         
| YogaSMC                | Latest Lenovo SMC



What Works:

Touchscreen after wake (With thunderbolt enabled) ~ Fixed touchscreen issue with ACPI wake call
Airdrop, continuity camera, universal control, sidecar, handoff, all that. 
Touchscreen with pen input (No pressure though)
All special fn keys
USB 3.2 Type-C ports (upto 1000 MB/s speeds with my nvme external drive)

What doesnt work:

-Fingerprint sensor (Probably will never work)
-IR face unlock (Camera works but not the IR blasters)
-Touchscreen input wont switch orientation with mac (Minor bug, voodooI2C)
-ALS sensor (Need some help if someone knows how to enable)
