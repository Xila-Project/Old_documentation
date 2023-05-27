# `Screen_Type`

## 👓 Overview

Screen is the parent container of all the graphics elements. It's owned by a user and managed by `Shell`. It's needed to create a window (see `Window_Type`).

## 💡 Example

```cpp
    using namespace Xila;
    using namespace Graphics_Types;

    void Shell_Class::Set_Interface()
    {
        Screen_Type Screen;
        Screen.Create(this);
        Screen.Load();

        Window_Type Window;
        Window.Create(this);
        Window.Set_Title("My Software");
    }
``` 

## 📚 API reference

```{eval-rst}
.. doxygentypedef:: Xila_Namespace::Graphics_Types::Screen_Type

.. doxygenclass::   Xila_Namespace::Graphics_Types::Screen_Class
    :members:
```