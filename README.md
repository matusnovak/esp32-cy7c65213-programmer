# ESP32 USB-C programmer with CY7C65213

This is a simple USB-C programmer that uses the CY7C65213 UART bridge controller. This repository contains KiCad 6 project files with gerber files exported. This board is capable of DTR and RTS, therefore the program upload experience should be without any problem.

**NOTE!**

* Do not connect a capacitor on the BOOT pin (GPIO 0 pin) towards the ground. It will cause the ESP32 to jump to the programming mode on power up.
* Use 1uF capacitor between the ESP32 reset pin (also known as EN or PN pin) between its and the ground. You will also need 10K pull-up resistor between that same reset pin and the + 3.3V.
* The Rx, Tx, Boot, and En pins on this board are 3.3V tolerant only.

**Why CY7C65213?**

It works in Linux and Windows out of the box without the need to install any drivers. Compared to the CH340 UART controllers the drivers for CY7C65213 are stable and mature. I do not want to install some shady CH340 drivers that work half of the time.
