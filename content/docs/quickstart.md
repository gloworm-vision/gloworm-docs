---
title: Quick Start
weight: 1
---


# Quick Start

## Imaging

1. Download the latest Gloworm release of FRCVision [here](https://github.com/gloworm-vision/gloworm-pi-gen/releases)
2. Download [BalenaEtcher](https://www.balena.io/etcher/)
4. Plug a USB C cable into the outermost USB C port from your computer into the Gloworm
5. Run BalenaEtcher as an administrator
6. Select the FRCVision zip file you downloaded in the first step
7. Select the compute module (initialization may take a while)
8. Hit flash
9. After flashing is completed, disconnect your USB C cable. Never use the outermost USB C port during normal operation, it will force Gloworm into USB boot mode. Peripherals should be connected to the adjacent (innermost) USB C port.

![Balena Etcher](/balenaEtcher.png)

## Wiring

Gloworm is powered via 12V passive PoE. **Not** standard 48V PoE.

1. Wire a [passive PoE injector](https://www.revrobotics.com/rev-11-1210/) to your PDP
2. Run an Ethernet cable from the passive PoE injector output to Gloworm's Ethernet port

At this point you can also plug any USB peripherals (such as a USB camera) into the Gloworm USB A port.

## Testing

1. Make sure your USB C cable is disconnected from the Gloworm
3. Run an Ethernet cable from the passive PoE injector to a LAN or PC
4. Turn on your robot (or any other 12V/1A power supply you're using)
5. Open a web browser and connect to http://frcvision.local/

FRCVision documentation is available [here](https://docs.wpilib.org/en/stable/docs/software/vision-processing/raspberry-pi/the-raspberry-pi-frc-console.html).