# Razer Blade 17 Pro 2020 Hackintosh

A work in progress of getting macOS Catalina to run on a Razer Blade 17 Pro 2020 using OpenCore 0.6.1.

## Introduction
The EFI included in this repository is a work in progress. It's enough to be able to get you through install and give you a non-GPU acceleration machine to work with. The touchpad doesn't yet work so you'll need to plug a USB Mouse for installation.

If you would like to get started with creating a Hackintosh on your XPS 9500 but have no experience, I would highly reccomend following Dortania's fantastic [Opencore Install guide][1] and then returning here for troubleshooting.

## Specs

| Key                    | Value                                                        |
| ---------------------- | ------------------------------------------------------------ |
| CPU                    | Intel Core i7 10750H                                         |
| GPU                    | Intel UHD Graphics 630                                       |
| Screen                 | 17" UHD 120hz Touch Display                                  |
| Camera                 | HD webcam (720p)                                            |
| RAM                    | 16 DDR4 2,933MHz (2x8GB)                                     |
| Internal SSD           | 512GB M.2 PCIe SSD                                           |
| Audio                  | Unknown                                                      |
| Wireless               | Intel Wireless-AX201                                         |

Quick Note: My serial number, MLB, and UUID have been removed from the config.plist. Please use CorpNewt's [GenSMBIOS][2] to create your own

## What works

- It boots
- Keyboard
- USB Ports

## What Doesn't Work

- iGPU acceleration (remove `-igfxvesa` from the cofig if you wanna have a go at it)
- Trackpad and Touchscreen
- Audio & Brightness Control

## What I need help with

Any help with the iGPU acceleration would be much appreciated. From my fiddling so far, I think we need to patch the appropriate Framebuffer patches for connectors.
Also there's a black line at the bottom of the display, I have no idea what's causing it but maybe it'll be fixed when iGPU is fixed?

<img src="https://user-images.githubusercontent.com/4278113/93589138-d4115280-f9c5-11ea-872f-fd7c7027fb28.jpg" />

Please open up a pull request or issue if you have any fixes to contribute.

## Credits:

- Apple for their OS
- OpenCore Team
- CorpNewt
- @robotblox for his [XPS 15 9500 config][3]

[1]:https://dortania.github.io/OpenCore-Install-Guide/
[2]:https://github.com/corpnewt/GenSMBIOS
[3]:https://github.com/robotblox/XPS-15-9500-Catalina-10.15.6
