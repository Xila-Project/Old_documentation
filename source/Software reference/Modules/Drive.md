# 💾 Drive

Here you will find a full description of the drive abstraction layer.

## 👓 Overview

This module is an abstranction layer for the drive and its file system.

It uses the following types :
- `Seek_Mode_Type`
- `File_Type` 
- `Drive_Type_Type`

## 💡 Example

```cpp
    using namespace Xila;
    using namespace Drive_Types;

    File_Type File = Drive.Open("/Test.txt")  // Open file in write mode, if the file does not exist, it will be created automatically.

    if (!File)  // Always check if the file was opened correctly.
    {
        // Do something if the file can't be opened.
    }

    File.Set_Position(0);
    File.Write_String("Hello world !");

    Drive.Make_Directory("/Folder");

    File_Type Folder = Drive.Open("/Folder");

    if (!Folder)
    {
        // Do something if the folder can't be opened.
    }


    Xila_Namespace::Drive_Class::Sd_Card_Type Card_Type = Xila.Drive.Type();    // -- Get card type.
    uint64_t Card_Size = Xila.Drive.Get_Size();     // Get card size.
    uint64_t Available_Bytes = Xila.Drive.Get_Total_Size();    // Get current partition available space.
    uint64_t Used_Bytes = Xila.Drive.Get_Used_Size();          // Get current partition used space.

    Xila.Drive.Make_Directory("/Folder");       // Create a new folder.
    bool Exist = Xila.Drive.Exist("/Folder");   // Check if the folder was created.
    if (Exist)
    {
        Xila.Drive.Remove_Directory("/Folder"); // Delete "Folder".
    }

    File_Type New_File = Xila.Drive.Open("/File", true);    // Open a file in write mode, if the file does not exist, it will be created automatically.
    New_File.Write_String("Hello World");              // Add "Hello World" into file.
    New_File.Close();                           // Close file.
    Xila.Drive.Rename("/File", "/New_File");    // Rename "File" into "New_File".
    Xila.Drive.Remove("/New_File");             // Delete "New_File".
```
    
## 📚 API reference

```{eval-rst}
.. doxygenenum:: Xila_Namespace::Drive_Types::Seek_Mode_Type

.. doxygentypedef:: Xila_Namespace::Drive_Types::File_Type

.. doxygenclass::  Xila_Namespace::Drive_Types::File_Class
    :members:

.. doxygenvariable:: Xila_Namespace::Drive

.. doxygentypedef:: Xila_Namespace::Drive_Type

.. doxygenclass::   Xila_Namespace::Drive_Class
    :members:
```
