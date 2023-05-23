# 🛜 WiFi

Here you will find a complete description of the WiFi abstraction layer.

## 👓 Overview

Xila provides a WiFi abstraction layer to simplify the use of WiFi. It is based on the ESP32 WiFi library for Arduino.

It's composed of 3 sub-modules: 
- `Station`
- `Access Point`
- `Scan`

## 💡 Example

```cpp
    using namespace Xila;

    WiFi.Station.Connect("SSID", "Password"); // - Connect to a WiFi network.
    WiFi.Station.Disconnect(); // - Disconnect from the current WiFi network.
    WiFi.Station.Get_IP_Address(); // - Get the IP address of the current WiFi network.
    WiFi.Station.Get_MAC_Address(); // - Get the MAC address of the current WiFi network.
    WiFi.Station.Get_SSID(); // - Get the SSID of the current WiFi network.
    WiFi.Station.Get_Status(); // - Get the status of the current WiFi network.

    WiFi.Scan.Begin();


    WiFi.Scan.Get_Informations();
    WiFi.Scan.Clean();
    
```

## 📚 API reference

```{eval-rst}

.. doxygenenum:: Xila_Namespace::Communication_Types::Status_Type
    
.. doxygenenum:: Xila_Namespace::Communication_Types::Mode_Type
    
.. doxygenenum:: Xila_Namespace::Communication_Types::Authentication_Mode_Type

.. doxygenenum:: Xila_Namespace::Communication_Types::WPA2_Authentication_Method_Type

.. doxygentypedef:: Xila_Namespace::Communication_Types::WiFi_Type

.. doxygenclass::   Xila_Namespace::Communication_Types::WiFi_Class
    :members:
```
