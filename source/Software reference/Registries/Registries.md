# 📜 Registries

Here you will find how Xila stores its configuration.

## 👓 Overview

Xila use registries to store its configuration. It is a way to store data in a file. These registries have the `.xrf` extension and are contained in the `/Xila/Registry` folder. Thanks to JavaScript Object Notation (J.S.O.N.), these registries are quite easy to apprehend by hand.

During startup, Xila checks and loads its various registers. If a registry is corrupted, it will automatically reset with default values. If the registry is not corrupted, but the data in the registry is incorrect, you can still delete it. Xila will regenerate it automatically.

Here you will find how to configure Xila in depth so that it can adapt to all your needs.

Xila use registries to store its configuration.
These registries have the `.xrf` extension and are contained in the `/Xila/Registry` folder.
Thanks to JavaScript Object Notation (J.S.O.N.), these registries are quite easy to apprehend.

During startup, Xila checks and loads its various registers.
If a registry is corrupted, it will automatically reset with default values.
If the registry is not corrupted, but the data in the registry is incorrect, you can still delete it.
Xila will regenerate it automatically.

Each registry begin with a `Registry` key.
It allows you to know if the loaded register is indeed the one targeted.

:::{warning}
Be careful with the `System.xrf` registry. Because this one cannot be repaired automatically.
If a corruption occur, it is then necessary to manually replace the latter with a healthy file (can be found in install archive).
:::

## 📚 Registries reference

### Display

| 

### Keyboard

| Key         | Type    | Default value                     |
| ----------- | ------- | --------------------------------- |
| `Registry`  | String  | `Keyboard`                        |
| `Data Pin`  | Integer | `Xila_Default_Keyboard_Data_Pin`  |
| `Clock_Pin` | Integer | `Xila_Default_Keyboard_Clock_Pin` |
| `Layout`    | Integer | `Xila_Default_Keyboard_Layout`    |


### Communication

#### WiFi

| Parent         | Key                           | Type    | Default value |
| -------------- | ----------------------------- | ------- | ------------- |
| -              | `Registry`                    | String  | `WiFi`        |
| -              | `Mode`                        | String  | `Station`     |
| -              | `Transmission power`          | Integer | -             |
| -              | `Station`                     | Object  | -             |
| `Station`      | `IP Address`                  | Integer | -             |
| `Station`      | `Subnet Mask`                 | Integer | -             |
| `Station`      | `Gateway`                     | Integer | -             |
| `Station`      | `DNS_1`                       | Integer | -             |
| `Station`      | `DNS_2`                       | Integer | -             |
| `Station`      | `IP v6`                       | String  | -             |
| `Station`      | `Automatic reconnection`      | Boolean | -             |
| `Station`      | `Access points`               | Array   | -             |
| -              | `Access point`                | Object  | -             |
| `Access point` | `SSID`                        | String  | -             |
| `Access point` | `Password`                    | String  | -             |
| `Access point` | `Channel`                     | Integer | -             |
| `Access point` | `Hidden`                      | Boolean | -             |
| `Access point` | `Maximum Stations`            | Integer | -             |
| `Access point` | `IP Address`                  | Integer | -             |
| `Access point` | `Subnet Mask`                 | Integer | -             |
| `Access point` | `Gateway`                     | Integer | -             |
| `Access point` | `DHCP Lease Start IP Address` | Integer | -             |




### Power

| Key                 | Type    | Default value                          |
| ------------------- | ------- | -------------------------------------- |
| `Registry`          | String  | `Power`                                |
| `Battery`           | Object  | -                                      |
| `Minimum Voltage`   | Integer | Xila_Default_Battery_Minimum_Voltage   |
| `Maximum Voltage`   | Integer | Xila_Default_Battery_Maximum_Voltage   |
| `Sensing pin`       | Integer | Xila_Default_Battery_Sensing_Pin       |
| `Charging pin`      | Integer | Xila_Default_Battery_Charging_Pin      |
| `Conversion factor` | Integer | Xila_Default_Battery_Conversion_Factor |

### Sound

.. csv-table::
    :header-rows:   1
    :file:          Registries/Sound.csv

### System

.. csv-table::
    :header-rows:   1
    :file:          Registries/System.csv



