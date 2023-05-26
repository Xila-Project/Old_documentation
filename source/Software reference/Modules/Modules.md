# 🧩 Module

Here you will find a full description of module.

## 👓 Overview

Xila has a modular architecture which means that each system part is a module.
A module is a part of the system responsible for a specific task (hardware abstraction layer, management or complementary library).
This way, it's easier to add new features and debug the system since it reduces coupling and polymorphism is used to make the system more flexible.

`Module_Type` is the base type that could be derived to create a module.

:::{note}
`Software_Type` is also a child class of `Module_Type`.
:::

Here is the list of the modules :

```{toctree}
:maxdepth:  1
Accounts
Clipboard
Communication
Display
Drive
Flash
Pin
Graphics
Keyboard
Mathematics
Memory
Power
Softwares
Sound
System
```

## 💡 Example

## 📚 API reference

```{eval-rst}
.. doxygentypedef:: Xila_Namespace::Module_Type

.. doxygenclass::   Xila_Namespace::Module_Class
    :members:
```