---
title: "Announcing Gloworm"
date: 2020-07-10T00:00:00-00:00
---

Hi everyone, today I would like to announce Gloworm: an inexpensive and open source vision module. While there are many awesome open source vision _software_ projects for FRC (such as PhotonVision and OpenSight), the accompanying hardware solutions are often unreliable and hacky. Even if your team is capable of setting up open source software or writing your own vision code, you might shy away from that if you don't want to duct tape a Raspberry Pi to your shooter. Gloworm aims to bridge this software-hardware gap and fully democratize vision tracking in FRC by providing a cheap and open source COTS hardware solution.

"People who are really serious about software should make their own hardware." - Alan Kay

Features:

* Raspberry Pi Compute Module 3+ (BCM2837 64-bit SoC @ 1.2GHz, 1GB LPDDR2 SDRAM, 8GB eMMC Flash)
* OV5647 Wide Angle Camera Module (640x480 @ 90FPS video)
* Dimmable 400 lumen green LED array (with constant brightness down to 7v)
* 10/100 Ethernet
* 12V Passive PoE (with reverse polarity protection and brownout tolerance)
* USB C ports for flashing and peripherals (such as a USB camera)
* WPILIB FRCVision-based image to kickstart your custom vision code
* Compatible with PhotonVision, a Raspbian image for PhotonVision on Gloworm will be available soon
* Completely open source (CERN Open Hardware License v2 - Permissive Variant)

Here's where we're at:

* Functional hardware prototypes
* Currently working on the last (or second to last if we get some great community feedback) hardware revision
* Working WPILIB FRCVision fork
* Still working on a 3D printed case design
* Have received multiple turnkey PCB assembly quotes and have the funding to execute a medium run
* [Copperforge](https://copperforge.cc/) will be working with the project to make Gloworm available as a COTS item in their store

Based on the quotes we have received for PCBs, as well as our predicted cost for 3D printed cases and hardware, camera price quotes, and overhead costs, **our target price is $125**. We are hoping to make fully assembled COTS units available by September, and we want to make beta units available ASAP. **If you're interested in purchasing a beta Gloworm, please fill out the interest check form, available [here](https://forms.gle/szYH1TfvKDQHjBjV7).**

Photos (renders are of latest revision):

![Gloworm (rev 0.4.0) render)](/announcing-gloworm/rev0.4.0-render.JPEG)
![Gloworm (rev 0.4.0) ledboard render)](/announcing-gloworm/rev0.4.0-ledboard-render.png)
![Gloworm (rev 0.3.0) with LEDs ON](/announcing-gloworm/rev0.3.0-leds-on.JPEG)
![Gloworm (rev 0.3.0) with LEDs OFF)](/announcing-gloworm/rev0.3.0-leds-off.JPEG)

Website: [https://gloworm.vision/](https://gloworm.vision/)

Discord: [https://discord.gg/DncQRky](https://discord.gg/DncQRky)

Github: [https://github.com/gloworm-vision/gloworm](https://github.com/gloworm-vision/gloworm)

FRCVision fork: [https://github.com/gloworm-vision/gloworm-pi-gen](https://github.com/gloworm-vision/gloworm-pi-gen)

Documentation source: [https://github.com/gloworm-vision/gloworm-docs](https://github.com/gloworm-vision/gloworm-docs)

If you're interested in contributing to the project, we could really use some help with the following:

* 3D printed case design, hardware .STEP files are available here [here](https://gloworm.vision/docs/hardware/mcad/)
* Schematic and PCB design review
* Documentation feedback
* Designing a logo or other art (banners, etc)
* Software support (in addition to Photon and FRCVision)
* (whatever cool idea popped into your head while reading this goes here)