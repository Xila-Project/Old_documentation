# 📋 Clipboard

Here you will find a full description of the `Clipboard` module.

## 👓 Overview

This module is responsible to copy and paste data between softwares.

## 💡 Examples

```cpp
    using namespace Xila;

    void Function_A()
    {
        char String_To_Copy[] = "String to copy";
        Xila.Clipboard.Copy(String_To_Copy, sizeof(String_To_Copy));    // -- Copy a string into the clipboard.
    }

    void Function_B()
    {
        char String_To_Paste[32];
        Xila.Clipboard.Paste(String_To_Paste, sizeof(String_To_Paste)); // -- String to paste from the clipboard.
        Xila.Clipboard.Clear(); // -- Clear the clipboard.
    }
```

## 📚 API reference

```{eval-rst}
.. doxygenvariable::  Xila_Namespace::Clipboard

.. doxygentypedef::   Xila_Namespace::Clipboard_Type

.. doxygenclass::   Xila_Namespace::Clipboard_Class
    :members:
```