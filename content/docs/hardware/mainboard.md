---
title: Mainboard
weight: 1
---

# Mainboard

## Functionality

* DDR2 SODIMM slot for CM3+
* Ethernet MagJack for passive PoE and 10/100 Ethernet
* Reverse polarity protection, bulk capacitance, 1.5A polyfuse, TVS protection on all ports
* TLV62130 5V voltage regulator
* AOZ1282CI 3.3V and 1.8V voltage regulators
* ENC28J60 SPI Ethernet controller
* USB C port for USB boot
* USB C port for USB peripherials (such as a USB camera)
* FSUSB42MUX chip and USB boot circuit
* 15-pin FFC connector for the camera
* 2x M2 mounting holes
* Molex PicoBlade 53047 2-pin 1.25mm fan connector (5v)

## Pin Configuration

| Function   | CM3+ Pin |
| ---------- | -------- |
| CAM0_SHDN  | GPIO3    |
| USR_LED_A  | GPIO4    |
| USR_LED_B  | GPIO5    |
| LED_PWM_R  | GPIO13   |
| LED_PWRM_L | GPIO18   |
| ETH_INT    | GPIO25   |
| CD0_SDA    | GPIO28   |
| CD0_SCL    | GPIO29   |
| CAM0_LED   | GPIO30   |
| ETH_RST    | GPIO31   |
| ETH_CLK    | GPIO44   |