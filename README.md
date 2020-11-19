# Razer Blade 17 Pro 2020 Hackintosh

Configuration for getting macOS Catalina to run on a Razer Blade 17 Pro 2020 using OpenCore 0.6.4-dev

## Introduction

If you would like to get started with creating a Hackintosh on your Razer Blade but have no experience, I would highly reccomend following Dortania's fantastic [Opencore Install guide][1] and then returning here for troubleshooting.

## Specs

| Key                    | Value                                                        |
| ---------------------- | ------------------------------------------------------------ |
| CPU                    | Intel Core i7 10875h                                         |
| GPU                    | Intel UHD Graphics 630                                       |
| Screen                 | 17" UHD 120hz Touch Display                                  |
| Camera                 | HD webcam (720p)                                             |
| RAM                    | 16 DDR4 2,933MHz (2x8GB)                                     |
| Internal SSD           | 512GB M.2 PCIe SSD                                           |
| Audio                  | Unknown                                                      |
| Wireless               | Intel Wireless-AX201                                         |

Quick Note: My serial number, MLB, and UUID have been removed from the config.plist. Please use CorpNewt's [GenSMBIOS][2] to create your own

## Pre-Install

Razer has locked the BIOS tight this time, so you'll need a hardware programmer to unlock DVMT Options this time around. Follow the instructions on https://git.io/JkuFs for how to mod your BIOS for this.
After modding the BIOS, change DVMT Pre Alloc to 64MB, DVMT Max Alloc to MAX. Also if you've selected "Dedicated GPU Only" Graphics mode, you'll need to put it back in "NVIDIA (R) Optimus" along with Disabling Secure boot.

## Post Install

After installation, you should install the HeliPort.app from OpenIntelWireless to be able to use wifi on your Razer Blade.

## What works

- iGPU
- Audio
- Sleep
- Battery
- Touchpad
- Touchscreen
- USB Ports
- CPU Freq
- Intel bluetooth / wifi (using HeliPort.app)

## Credits:

- [hackintosh.expert][3] - You should contact them to make you the Hackintosh config, highly recommended!
- Apple for their OS
- OpenCore Team
- CorpNewt

[1]:https://dortania.github.io/OpenCore-Install-Guide/
[2]:https://github.com/corpnewt/GenSMBIOS
[3]:https://hackintosh.expert/
