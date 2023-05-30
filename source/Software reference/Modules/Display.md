# 🖥️ Display

Here you will find a full description of the display abstraction layer.

## 👓 Overview

This abstraction layer is responsible to drive the display.
In addition, this API supports resource protection to avoid data collisions when sending information.
This API rest upon the Nextion Library. For the full API, please visit the library page.

## 💡 Example

```cpp
    using namespace Xila;

    Display.Set_Brightness(127); // - Set the display brightness to 50%.

    Display.Set_Standby_Time(60); // - Set the display standby time to 1 minute.

    auto Brightness = Display.Get_Brightness(); // - Get the display brightness.

    auto Standby_Time = Display.Get_Standby_Time(); // - Get the display standby time.

    auto Vertical_Definition = Display.Get_Vertical_Definition(); // - Get the display vertical definition.

    auto Horizontal_Definition = Display.Get_Horizontal_Definition(); // - Get the display horizontal definition.
```

## 📚 API reference

```{eval-rst}
.. doxygenvariable::  Xila_Namespace::Display

.. doxygentypedef::   Xila_Namespace::Display_Type

.. doxygenclass::   Xila_Namespace::Display_Class
    :members:
```

