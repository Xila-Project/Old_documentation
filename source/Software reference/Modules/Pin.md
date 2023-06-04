# 🔛 Pin

Here you will find a full description of the `Pin` module.

## 👓 Overview

`Pin` allows to easily use I/O pins and communication peripherals.

### Types

This module uses the following types :

```{toctree}
    :maxdepth: 1

Pin/Serial
Pin/Two Wire
```
- `Digital_State_Type`
- `Mode_Type`
- `Interrupt_Mode_Type`


## 💡 Example

```cpp
    using namespace Xila;
    using namespace Pin_Types;

    void Interrupt_Handler()
    {
        // - Do stuff
    }


    void GPIO_Test()
    {
        Pin.Set_Mode(12, Mode_Type::Output);    // Set pin 5 as an output.

        Pin.Digital_Write(12, Digital_State_Type::High);    // Set pin to an high state.

        Pin.Set_Mode(12, Digital_State_Type::Input_Pull_Up);    // Set pin 5 as an input with a pull-up resistor attached.

        uint16_t State = Pin.Digital_Read(12);        // Read pin digital state.

        State = Pin.Analog_Read(12);                  // Read pin analog state.

        Pin.Attach_Interrupt(12, Interrupt_Handler, Interrupt_Mode_Type::Rising);   // Attach an interrupt function to the pin 12 when the pin signal rise.

        Pin.Detach_Interrupt(12); // Disable interrupt on pin 12.
    }
```

## 📚 API reference

```{eval-rst}
.. doxygenenum:: Xila_Namespace::Pin_Types::Digital_State_Type

.. doxygenenum:: Xila_Namespace::Pin_Types::Mode_Type

.. doxygenenum:: Xila_Namespace::Pin_Types::Interrupt_Mode_Type

.. doxygenvariable:: Xila_Namespace::Pin

.. doxygentypedef:: Xila_Namespace::Pin_Type

.. doxygenclass::   Xila_Namespace::Pin_Class
    :members:
```