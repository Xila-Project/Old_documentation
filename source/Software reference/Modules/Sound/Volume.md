# `Volume_Type`

## 👓 Overview

This stream allows to control the volume of another stream.

It uses the type `Volume_Configuration_Type` to set and get the volume configuration.

## 💡 Example

```cpp
    using namespace Xila;
    using namespace Sound_Types;

    Volume_Type Volume(Sound.Get_Current_Output_Stream())

    auto Configuration = Volume.Get_Default_Configuration(); // Get default configuration.

    Volume.Begin(Configuration);
    Volume.Set_Volume(127); // Set volume to 1/2.
```

## 📚 API reference

```{eval-rst}

.. doxygentypedef:: Xila_Namespace::Sound_Types::Volume_Configuration_Type

.. doxygenclass::   Xila_Namespace::Sound_Types::Volume_Configuration_Class
    :members:

.. doxygentypedef:: Xila_Namespace::Sound_Types::Volume_Type

.. doxygenclass::   Xila_Namespace::Sound_Types::Volume_Class
    :members:

```