# ⌨️ Keyboard

Here you will find a full description of the keyboard abstraction layer.

## 👓 Overview

`Keyboard` module is responsible for everything related to keyboard external keyboard, such as keystrokes, special keys etc. The latter is based on the [PS2Keyboard](https://github.com/PaulStoffregen/PS2Keyboard) library by [Paul STOFFREGEN](https://github.com/PaulStoffregen).

## 💡 Example

```cpp
    using namespace Xila;

    Keyboard.Clear();                  // -- Clear all registered keystrokes in the buffer.
    if (Keyboard.Available())          // -- Check if any keystroke is available in the buffer.
    {
        uint8_t Input = Keyboard.Read();   // -- Read a regular character from the keyboard.
        Input = Keyboard.Read_Raw();       // -- Read a special input from the keyboard.
    }
```

## 📚 API reference

```{eval-rst}
.. doxygenvariable:: Xila_Namespace::Keyboard

.. doxygentypedef::   Xila_Namespace::Keyboard_Type

.. doxygenclass::   Xila_Namespace::Keyboard_Class
    :members:
```