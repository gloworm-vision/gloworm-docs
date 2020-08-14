---
weight: 10
---

# Hardware

## Custom PCBs

Gloworm's main custom components are the mainboard and ledboard. The ledboard hosts high power green LEDs and the two small status LEDs, and the mainboard supports the CM3+. They're connected via four 1x2 0.1" pin headers, which allows the mainboard to passthrough power to the ledboard and control the LEDs.

## System on Module

Gloworm uses a RPI CM3+ System on Module (SoM) as a vision coprocessor. It's plenty performant for most applications, and there's a plethora of documentation available on how to design hardware around it. We're also looking into the Rockchip PX30 SoM.

## Camera Module

The ledboard is slotted to fit a Raspberry Pi Wide Angle Camera Module from Seeedstudio (and other generic equivalents). The OV5647 sensor allows for 640x480 video at up to 90 FPS which is much faster than the Raspberry Pi Camera Module v2 while still being relatively cheap and easy to source. It talks to the mainboard via MIPI CSI-2 over a 15-pin flat flex cable. We designed the mainboard with a top-mount 15-pin FFC connector so you can use the cable that comes with your camera without bending it (rather than use a custom FFC).