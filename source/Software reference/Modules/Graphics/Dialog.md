# `Dialog_Type`

## 👓 Overview

Dialog is a child class of `Window_Type` that can be used to create a dialog box.

## 💡 Example

```cpp
    using namespace Xila;
    using namespace Xila::Graphics_Types;

    void My_Software::Open_Dialog()
    {
        Dialog_Type Dialog;
        Dialog.Create(this);
        Dialog.Set_Title("Information");
    
        Label_Type Label;
        Label.Create(Dialog.Get_Body());
        Label.Set_Text("Hello World !");
        Label.Set_Alignment(Alignment_Type::Center);

        while (Dialog.Is_Valid())
            Main_Task.Delay(100);   // - Wait for the dialog to be closed.
    }
```

## 📚 API reference

```{eval-rst}
.. doxygentypedef:: Xila_Namespace::Graphics_Types::Dialog_Type

.. doxygenclass::   Xila_Namespace::Graphics_Types::Dialog_Class
    :members:
```