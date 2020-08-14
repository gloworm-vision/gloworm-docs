---
title: Gloworm
type: docs
---

# Gloworm

Gloworm is an inexpensive and open source vision module.

While there are many awesome open source vision _software_ projects for FRC (such as PhotonVision and OpenSight), the accompanying hardware solutions are often unreliable and hacky. Even if your team is capable of setting up open source software or writing your own vision code, you might shy away from that if you don't want to duct tape a Raspberry Pi to your shooter. Gloworm aims to bridge this software-hardware gap and fully democratize vision tracking in FRC by providing a cheap and open source COTS hardware solution.

## Features

* Raspberry Pi Compute Module 3+ (BCM2837 64-bit SoC @ 1.2GHz, 1GB LPDDR2 SDRAM, 8GB eMMC Flash)
* OV5647 Camera Module (640x480 @ 90FPS video, low distortion 62.7° lens)
* Dimmable 400 lumen green LED array (with constant brightness down to 7v)
* 10/100 Ethernet
* 12V Passive PoE (with reverse polarity protection and brownout tolerance)
* USB C ports for flashing and peripherals (such as a USB camera)
* PhotonVision image for getting started with vision tracking quickly
* WPILIB FRCVision-based image for custom vision code
* Completely open source (CERN Open Hardware License v2 - Permissive Variant)
* 20mm 5v cooling fan

![Assembled Gloworm](/gloworm.png)