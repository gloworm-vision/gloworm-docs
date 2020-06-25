---
weight: 10
---

# Software

The Gloworm is basically a Raspberry Pi with some blinky lights, and as such, it's pretty easy to run existing Raspberry Pi images like WPILIB's FRCVision or Raspbian with PhotonVision on it. All we need to do is modify the image to enable the enc28j60 overlay and setup the pins as outlined in [Mainboard]({{< relref "/docs/hardware/mainboard" >}}). Then we can use a GPIO library like pigpio that supports hardware PWM for controlling the LED cluster brightness and the status LEDs.