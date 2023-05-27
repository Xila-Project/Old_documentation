# 🪛 Reference kit

Here you can find information about the Xila's reference kit.

## 👓 Overview

The purpose of the hardware reference kit is to provide a reference for the hardware that can be used with Xila. It is composed of:

- A case.
- A WT32-SC01 Plus development board.
- A daughter printed circuit board.
- A battery.
- A speaker.

The overall cost of the kit is around 70€ (delivery not included).

The repository contains all the files needed to build the kit can be found in the [Hardware](https://github.com/Xila-Project/Hardware) repository.

## Case

The case is a 3D model which can be printed easily with any 3D printer.

## WT32-SC01 Plus

The WT32-SC01 Plus is a development board based on the ESP32-S3, which offers the following features:

- 16 Megabytes of flash memory and 2 Megabytes of PSRAM.
- A 3.5-inch capacitive LCD touch screen (480x320).
- A I2S DAC / Amplifier.
- A 3,3 V regulation circuit.

It can be bought on [AliExpress](https://fr.aliexpress.com/item/1005004267336768.html).

## Daughter board

The daughter board is an extension board which can be screwed at the rear of the WT32-SC01 Plus. It adds the following features:

- Battery management circuit : charge (TP4056) and protection (DW01 + FS8205).
- A boost converter from battery voltage to 5V (MT3608)
- A latch circuit to completely turn on/off the device.
- External IO connectors (2x10 pins MX connectors).
- A jack connector for the speaker.
- A power button.

## Battery

The battery is a regular 1 cell (3.7 V) 2000 mAh LiPo battery. It's connected on the daughter board. It can be bought on [Amazon](https://www.amazon.fr/dp/B08214DJLJ?psc=1&ref=ppx_yo2ov_dt_b_product_details).

:::{note}
You can use any kind of lithium battery, as long as it is a single cell battery (3.7 V)
:::

## Speaker

The speaker is a regular 8 Ohm 1 W speaker. It's connected on the daughter board. It can be bought on [LCSC](https://www.lcsc.com/product-detail/_INGHAi-_C530547.html).


