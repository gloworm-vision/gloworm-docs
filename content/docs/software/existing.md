---
title: Existing image
weight: 1
---

# Existing image

If you already have an image for a Raspberry Pi-based coprocessor (such as Raspbian), modifying it to work with the Gloworm is pretty straightforward.

## Compile Device Tree

We'll need to compile our custom device tree first.

### Linux

1. Download [gloworm-dt-blob.dts](https://github.com/gloworm-vision/gloworm-pi-gen/blob/frcvision/stage1/00-boot-files/files/gloworm-dt-blob.dts)
2. `sudo apt install device-tree-compiler`
3. `dtc -O dtb gloworm-dt-blob.dts -o dt-blob.bin -q`

## Flash the Gloworm

Before modifying the image, we need to flash it onto the Gloworm.

### Linux

1. `git clone --depth=1 https://github.com/raspberrypi/usbboot`
2. `cd usbboot`
3. `sudo apt install libusb-1.0-0-dev # install libusb-dev`
4. `make`
5. `sudo ./rpiboot`
6. Connect your computer to the outermost USB C port, wait for usbboot to finish.
7. `sudo fdisk -l`
8. Find the 8GB device. Make **sure** you're using the right device (for me this is `/dev/sda`)
9. `sudo dd if=your_existing_image.img of=<device from above> bs=4M status=progress`

## Modify the boot partition

### Linux

1. `sudo fdisk -l`
2. Find the boot partition of your 8GB device from before. This will be the smaller of the two (for me this is `/dev/sda1`)
3. `mkdir boot`
4. `sudo mount <device partition> boot`
5. `echo "\ndtoverlay=enc28j60" >> boot/config.txt`
6. `cp dt-blob.bin boot/ # copy your compiled device tree blob`

## Backup (optional)

You can backup your customized image now so you don't need to repeat those steps in the future.

### Linux

1. `sudo dd if=<device> of=gloworm_image.img bs=4M status=progress`