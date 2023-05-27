# ⚙️ System

Here you will find a full description of the system module.

## 👓 Overview

The `System` module is responsible to coordinate the other modules and to provide system related operations and information.

## 💡 Example

```cpp
    using namespace Xila;

    Static_String_Type<64> Device_Name;

    System.Get_Device_Name(Device_Name); // Get the device name.

    uint32_t CPU_Frequency = System.Get_CPU_Frequency(); // Get the CPU frequency.

    System.Set_Device_Name("My Device"); // Set the device name.

    Time_Type Time = System.Get_Time(100); // Get the current time with a 100ms timeout for NTP synchronization.

```

## 📚 API reference

```{eval-rst}
.. doxygenvariable::  Xila_Namespace::System

.. doxygentypedef:: Xila_Namespace::System_Type

.. doxygenclass::   Xila_Namespace::System_Class
    :members:
```