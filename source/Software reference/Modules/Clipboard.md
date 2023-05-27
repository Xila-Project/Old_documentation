# 📋 Clipboard

Here you will find a full description of the `Clipboard` module.

## 👓 Overview

`Clipboard` allows to copy and paste data between softwares.

:::{warning}
Be careful, the clipboard is shared between all softwares and no check is done on the content. Never trust the clipboard content.
:::

## 💡 Examples

```cpp
    using namespace Xila;

    Clipboard.Copy("Hello world !"); // Copy "Hello world !" to the clipboard.

    char Buffer[20];
    Clipboard.Paste(Buffer, sizeof(Buffer)); // Paste the clipboard content to Buffer.

    Static_String_Type<20> Static_String;
    // Paste the clipboard content to Static_String.
    if (Clipboard.Paste(Static_String) == "Hello world !")  // Always false.
    {
        // ...
    }

    Clipboard.Copy(205); // Copy the number 205 to the clipboard.

    auto Number = Clipboard.Paste();
```

## 📚 API reference

```{eval-rst}
.. doxygenvariable::  Xila_Namespace::Clipboard

.. doxygentypedef::   Xila_Namespace::Clipboard_Type

.. doxygenclass::   Xila_Namespace::Clipboard_Class
    :members:
```