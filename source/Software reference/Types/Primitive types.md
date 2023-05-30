# 🧱 Primitive types

Xila provides a set of primitive types, which are defined in `Xila` namespace.

## 👓 Overview

### Fixed size data types

| Type             | Size    | Range                           |
| ---------------- | ------- | ------------------------------- |
| `Byte_Type`      | 1 byte  | 0 to 255                        |
| `Word_Type`      | 2 bytes | 0 to 65 535                     |
| `DWord_Type`     | 4 bytes | 0 to 4 294 967 295              |
| `QWord_Type`     | 8 bytes | 0 to 18 446 744 073 709 551 615 |
| `Boolean_Type`   | 1 byte  | 0 (false) to 1 (true)           |
| `Character_Type` | 1 byte  | 0 (NULL) to 255 (Delete)        |

### Natural

| Type                 | Size                       |
| -------------------- | -------------------------- |
| `Short_Natural_Type` | Half of the registers size |
| `Natural_Type`       | Register size              |
| `Size_Type`          | Register size              |
| `Long_Natural_Type`  | Twice the register size    |

:::{tip}
For example on a 32-bit system, a `Natural_Type` is a 4 bytes unsigned integer.
:::

### Integer

| Type                 | Size                       |
| -------------------- | -------------------------- |
| `Short_Integer_Type` | Half of the registers size |
| `Integer_Type`       | Register size              |
| `Long_Integer_Type`  | Twice the register size    |

:::{tip}
For example on a 32-bit system, an `Integer_Type` is a 4 byte signed integer.
:::

### Real

| Type              | Size                     |
| ----------------- | ------------------------ |
| `Float_Type`      | Register size            |
| `Long_Float_Type` | Twice the registers size |

:::{tip}
For example, on a 32-bit system, a `Float_Type` is a 4 byte floating point number.
:::

### Enumerations

| Type          | Size   | Description                                                                                  |
| ------------- | ------ | -------------------------------------------------------------------------------------------- |
| `Result_Type` | 1 byte | Used to return a result : `Result_Type::Success`, `Result_Type::Error`, etc. |


## 💡 Example

```cpp
    using namespace Xila;             // - - Import Xila namespace.
    
    // - Fixed size data types
    Byte_Type My_Byte = 0x01;                   // - - Create a byte variable.
    Word_Type My_Word = 0x0123;                 // - - Create a word variable.
    DWord_Type My_DWord = 0x012345;             // - - Create a double word variable.
    QWord_Type My_QWord = 0x0123456789ABCDEF;   // - - Create a quad word variable.
    Boolean_Type My_Boolean = true;             // - - Create a boolean variable.
   
    // - Integer types
    Short_Type My_Short = 0x0001;               // - - Create a short variable.
    Integer_Type My_Integer = 0x00000001;       // - - Create a integer variable.
    Long_Type My_Long = 0x0000000000000001;     // - - Create a long variable. 

    // - Natural types
    Short_Natural_Type My_Short_Natural = 0x0001;           // - - Create a short natural variable.
    Natural_Type My_Natural = 0x00000001;                   // - - Create a natural variable.
    Long_Natural_Type My_Long_Natural = 0x0000000000000001; // - - Create a long natural variable.

    // - Real types
    Float_Type My_Float = 0.0;      // -- Create a float variable.
    Double_Type My_Double = 0.0;    // -- Create a double variable.

```