# 📝 Log

Here you will find a full description of `Log` module.

## 👓 Overview

`Log` module is responsible for everything related to logging to the standard output (usually the serial port). It proposes macros and methods to log messages, warnings and errors. To set the log level, change the `Log_Level` constant in the `platformio.ini` file.

Here is the list of available log macros :
- `Log_Raw` : Log a raw message.
- `Log_Raw_Line` : Log a raw message with a new line.
- `Log_All` : Log a message with all the information (function name, line number, file name, verbose level).
- `Log_Error` : Log an error message (available when `Log_Level` >= 1).
- `Log_Warning` : Log a warning message (available when `Log_Level` >= 2).
- `Log_Information` : Log an information message (available when `Log_Level` >= 3).
- `Log_Debug` : Log a debug message (available when `Log_Level` >= 4).
- `Log_Trace` : Log a trace message (function name, line number, file name) (available when `Log_Level` >= 4).
- `Log_Verbose` : Log a message with the verbose level (available when `Log_Level` >= 5).


## 💡 Example

```cpp

    int My_Variable = 42;
    Log_Verbose("My Software", "My variable is equal to %d.", My_Variable);

    char* My_String = "Hello World !";
    Log_Information("My Software", "My string is equal to %s.", My_String); 
```

## 📚 API reference

```{eval-rst}
.. doxygenvariable::  Xila_Namespace::Log

.. doxygentypedef:: Xila_Namespace::Log_Type

.. doxygenclass::   Xila_Namespace::Log_Class
    :members:
```
