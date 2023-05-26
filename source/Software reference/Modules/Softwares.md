# 📦 Softwares

Here you will find a full description of the software management API.

## 👓 Overview

This module is responsible for everything related to software management, such as loading, minimization, closing, watchdog etc.

A software is owned by a user, that's why the owner user is passed to the software when it's created (thought the `Software__Handle_Type::Create_Instance` methods).

:::{note}
`Software_Type` is a child class of `Module_Type`.
:::

It's using `Softwares_Types::Software_Type` 

## Types

Softwares module is using the following types :

:::{toctree}
    :maxdepth: 1
Softwares/Software Handle
Softwares/Software
:::

## 💡 Example

```cpp
    
```

## 📚 API reference

```{eval-rst}

.. doxygentypedef:: Xila_Namespace::Softwares_Type

.. doxygenclass::   Xila_Namespace::Softwares_Class
    :members:
```