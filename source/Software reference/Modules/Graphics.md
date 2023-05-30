# 📊 Graphics

Here is the full description of the Graphics module. 

## 👓 Overview

It is a dumb C++ wrapper for [LVGL](https://lvgl.io) with additional features.
It allows the developer to create complex graphic interface with ease.

:::{warning}
It is not recommended to use the LVGL API directly as it is not thread safe.
The wrapper is designed to support concurrent execution using [](<../Types/Semaphore.md>)
:::

It depends on the [](<./Display.md>) module.

## 💡 Example

```cpp
    using namespace Xila;
    using namespace Xila::Graphics_Types;

    Window_Type Window;
    Window.Create(this);
    Window.Set_Title("Window");

    Object_Type Object;
    Object.Create(Window.Get_Body());
    Object.Set_Alignment(Alignment_Type::Center, 0, 10);    // Set the alignment to center with a 10 pixels offset on the y axis.
    Object.Set_Size(100, Percentage(100));  // Set the size to 100 pixels width and 100% parent window height.

    Object.Delete();
```

## 📚 API reference

:::{note}
Since it's mainly a wrapper and the library is huge, the full documentation is currently not supplied here (maybe later). Please refer to the [LVGL documentation](https://docs.lvgl.io/master/) for more information. 
:::

Widgets have been wrapped into classes which have the same name as the original widget with the `_Type` suffix. Here's the list of the widgets :

- `Bar_Type`
- `Button_Matrix_Type`
- `Button_Type`
- `Calendar_Type`
- `Canvas_Type`
- `Chart_Type`
- `Checkbox_Type`
- `Color_Wheel_Type`
- `Drop_Down_List_Type`
- `Image_Type`
- `Keyboard_Type`
- `Label_Type`
- `Line_Type`
- `List_Type`
- `Menu_Type`
- `Object_Type`
- `Point_Type`
- `QRCode_Type`
- `Roller_Type`
- `Slider_Type`
- `Spinbox_Type`
- `Style_Type`
- `Switch_Type`
- `Table_Type`
- `Tabs_Type`
- `Text_Area_Type`

Some widget have also been added :

:::{toctree}
    :maxdepth: 1
Graphics/Window
Graphics/Dialog
Graphics/File Explorer
Graphics/Screen
:::

These wrapper only contains a pointer to the LVGL objects. The widget is created and deleted by using `Create(...)` and `Delete()` methods (not created / deleted with wrapper constructor / destructor). Then the widget can be used as usual (functions are almost the same as the original LVGL widget). The heritage of widget have been respected, and casting is possible (using the copy constructor from the base type `Object_Type`). The type checking is then performed using the `Widget_Type::Class` (wrapper for `lv_class_t`).

See [](<../Nomenclature.md>) for more information about the naming convention.

