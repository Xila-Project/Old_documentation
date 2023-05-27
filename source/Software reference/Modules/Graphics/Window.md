# `Window_Type`

## 👓 Overview

`Window_Type` is the parent class of all the graphics elements for a software. When creating the parent window of a software, you have to pass the owner software. This way, the Window, the owner user are recorded and the window is created in the user's screen (see `Screen_Type`).

You can also create a sub-window by passing a parent window with the regular `Window_Type:Create` method.

:::{warning}
The window is not automatically deleted when the software is closed. You have to delete it manually in the software destructor (all children will be deleted automatically).
:::

It uses the following types :
- `Window_State_Type`

## 💡 Example

```cpp
    using namespace Xila;
    using namespace Xila::Graphics_Types;

    void My_Software::Set_Interface()
    {
        Window_Type Window;
        Window.Create(this);
        Window.Set_Title("My Software");
        
        Label_Type Label;
        Label.Create(Window.Get_Body());
        Label.Set_Text("Hello World !");
        Label.Set_Alignment(Alignment_Type::Center);
    }
```

## 📚 API reference

```{eval-rst}
.. doxygenenum:: Xila_Namespace::Graphics_Types::Window_State_Type

.. doxygentypedef:: Xila_Namespace::Graphics_Types::Window_Type

.. doxygenclass::   Xila_Namespace::Graphics_Types::Window_Class
    :members:
```