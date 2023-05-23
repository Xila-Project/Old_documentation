# 🧩 Module

Here you will find a full description of module.

## 👓 Overview

Xila has a modular architecture which means that each system part is a module.
A module is a part of the system responsible for a specific task (hardware abstraction layer, management or complementary library).
This way, it's easier to add new features and debug the system since it reduces coupling.

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

Here you will find a full description of `Module_Type`.

## 👓 Overview

A module is a part of the system responsible for a specific task. `Module_Type` is the base type that could be used type that represents a module. 
It can be a hardware abstraction layer, a software or a library.
`Module_Type` is a type that represents a module in the system. It's also 

`Module_Type` is an alias of `Module_Class`.

## 💡 Example

## 📚 API reference

```{eval-rst}
.. doxygentypedef:: Xila_Namespace::Module_Type

.. doxygenclass::   Xila_Namespace::Module_Class
    :members:
```