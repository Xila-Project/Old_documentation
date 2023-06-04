# ⚡️ Flash

Here you will find a full description of the flash abstraction layer.

## 👓 Overview

`Flash` module is responsible for everything related to flash memory, such as reading, writing, erasing etc.

## Types

`Flash` is using the following types :

- `Partition_Subtype_Type`
- `Flash_Mode_Type`

## 💡 Example

```cpp
    using namespace Xila;
    using namespace Flash_Types;

    uint32_t Free_Flash_Space = Flash.Get_Sketch_Free_Space(); // -- Get flash free space in bytes.

    Static_String_Type<32> MD5_Checksum;
    
    Flash.Get_Sketch_MD5(MD5_Checksum);              // -- Get sketch MD5 checksum.
    
    if (MD5_Checksum == "5d8c1b4b4b5d8c1b4b4b5d8c1b4b4b5d") // Check if the MD5 checksum is correct.
    {
        // Do stuff when the MD5 checksum is correct.
    }
    
    uint32_t Sketch_Size = Flash.Get_Sketch_Size();                // Get sketch size in bytes.
    uint32_t Flash_Size = Flash.Get_Size();                    // Get flash size in bytes.
    uint32_t Speed = Flash.Get_Speed();                        // Get flash read speed in bytes / seconds.
    Flash_Mode_Type Flash_Mode = Flash.Get_Mode()                  // Get flash mode.
    uint32_t Buffer[128];
    if (Flash.Read(0x100, Buffer, sizeof(Buffer)) == Xila.Success) // Read data from flash at the 0x100 offset
    {
        // Do stuff when the operation succeed.
    }
```
## 📚 API reference

```{eval-rst}
.. doxygennamespace:: Xila_Namespace::Flash_Types

.. doxygenvariable:: Xila_Namespace::Flash

.. doxygentypedef:: Xila_Namespace::Flash_Type

.. doxygenclass::   Xila_Namespace::Flash_Class
    :members:
```