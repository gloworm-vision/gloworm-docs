---
title: Quick Start
weight: 1
---

# Quick Start

You have three main options for vision software on Gloworm:

* Run the PhotonVision beta (recommended)
* Run WPILIB's FRCVision image and write your own custom vision code
* Run your own custom Raspbian image (see [here]({{< relref "/docs/software/existing" >}}))

## Imaging

1. Download the latest Gloworm release of [PhotonVision](https://github.com/gloworm-vision/pi-gen/releases) or [FRCVision](https://github.com/gloworm-vision/gloworm-pi-gen/releases)
2. Download [BalenaEtcher](https://www.balena.io/etcher/) (**note**: you may need to run the [usbboot](https://github.com/raspberrypi/usbboot/blob/master/win32/rpiboot_setup.exe) installer if BalenaEtcher isn't recognizing anything)
3. Plug a USB C cable from your computer into the USB C port on Gloworm labeled with a download icon
4. Run BalenaEtcher as an administrator
5. Select the zip file you downloaded in the first step
6. Select the compute module. If it doesn't show up after 30s try using another USB port, initialization may take a while. If prompted, install the recommended missing drivers.
7. Hit flash
8. Wait for flashing to complete, then disconnect your USB C cable

Never use the download port during normal operation, it will force Gloworm into USB boot mode. Peripherals should be connected to the port labeled with a camera icon. First boot will be slower than the rest.

![Balena Etcher](/balenaEtcher.png)

## Mounting and Wiring

**Gloworm is powered via 12V passive PoE. **Not** standard 48V PoE.**

To use Gloworm on a robot, all you'll need is a [passive PoE injector](https://www.revrobotics.com/rev-11-1210/) and an Ethernet cable.

If you want to run Gloworm off wall-power, a [passive PoE injector with a DC barrel jack](https://www.amazon.com/dp/B00NRHNPUA) and a [12V/2A power supply](https://www.amazon.com/dp/B01GD4ZQRS) will be convenient.

1. Mount Gloworm using the provided 10-32 1-3/4" bolts and Nylon-insert nuts. **Take care not to overtighten the bolts.**
2. Wire a [passive PoE injector](https://www.revrobotics.com/rev-11-1210/) to your PDP. **Not the VRM.**
3. Run an Ethernet cable from the passive PoE injector output to Gloworm's Ethernet port
4. Plug any peripherals you have into the USB C port labeled with a camera icon

## Finding Gloworm

1. Make sure nothing is connected to the USB C port labeled with a download icon
2. Turn on your robot (or any other power supply you're using)
3. Open a web browser and connect to `http://gloworm.local:5800/` (PhotonVision) or `http://frcvision.local/` (FRCVision)

If those URLs don't resolve on your system, mDNS may not be setup properly. In that case, you'll want to use a tool such as [Angry IP Scanner](https://angryip.org/download) to find Gloworm on your network. After you find Gloworm, make sure to setup a static IP (which you can do in PhotonVision).

![Angry IP Scanner](/angryip.jpg)

## Usage

At this point, you'll want to follow along with the [PhotonVision](https://docs.photonvision.org/en/latest/) or [FRCVision](https://docs.wpilib.org/en/stable/docs/software/vision-processing/raspberry-pi/the-raspberry-pi-frc-console.html) documentation.