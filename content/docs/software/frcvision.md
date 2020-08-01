---
title: FRC Vision
weight: 1
---

# FRC Vision

WPILIB's FRC Vision is a great starting point for writing your own custom vision software. You can modify their images as outlined [here]({{< relref "/docs/software/existing" >}}), or download a [pre-built release](https://github.com/gloworm-vision/gloworm-pi-gen/releases) from our fork of their fork of pi-gen called [gloworm-pi-gen](https://github.com/gloworm-vision/gloworm-pi-gen).

## Flashing the image

## Linux, Windows, OSX

Cross platform instructions are [on the home page]({{< relref "/" >}}).

### Linux

1. `git clone --depth=1 https://github.com/raspberrypi/usbboot`
2. `cd usbboot`
3. `sudo apt install libusb-1.0-0-dev # install libusb-dev`
4. `make`
5. `sudo ./rpiboot`
6. Connect your computer to the USB C port labeled with a download icon, wait for usbboot to finish.
7. `sudo fdisk -l`
8. Find the 8GB device. Make **sure** you're using the right device (for me this is `/dev/sda`)
9. Download the latest release from gloworm-pi-gen
10. `unzip archive_name.zip`
11. `sudo dd if=image_name.img of=<device from above> bs=4M status=progress`