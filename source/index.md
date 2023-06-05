# 👋 Welcome to the documentation of Xila

# 📬 Introduction

Xila is an open-source operating system aimed at embedded systems that provides a user-friendly interface with powerful features.
It is designed to run on microcontroller with limited resources while providing efficient and scalable performance.
The project aims to provide a fully functional operating system that can perform tasks such as multitasking, memory management, input-output handling, and file system management in constrained environments.

With Xila, developers can build applications for all sorts of end-devices like robotics, smart home automation, wearables, and much more.
Xila provides its users with a structured API, a high-level programming language, powerful tools, and clear documentation for ease of use and integration.

The key objective of the project is to make development faster by leveraging Xila’s modular architecture, expandable library of drivers and libraries, and well-documented codebase.
By utilizing these tools, developers can rapidly prototype and deploy new products without worrying about lower-level details.

## 🏃 Getting started

[Get started](<./Get started/Use.md>) to use Xila.

## ✅ Features

- A complete and easy to use API split into modules :
  - Management :
    - [](<./Software reference/Modules/Accounts.md>) : multi-user support.
    - [](<./Software reference/Modules/Graphics.md>) : support for easy GUI development.
    - [](<./Software reference/Modules/System.md>) : system management.
    - [](<./Software reference/Modules/Softwares.md>) : softwares management.
    - [](<./Software reference/Modules/Power.md>) : power management.
  - Abstraction :
    - [](<./Software reference/Modules/Drive.md>) and file system.
    - [](<./Software reference/Modules/Display.md>).
    - [](<./Software reference/Modules/Communication.md>) : WiFi, Bluetooth (soon).
    - [](<./Software reference/Modules/Flash.md>) : Flash memory management.
    - [](<./Software reference/Modules/Memory.md>) : RAM and PSRAM management.
    - [](<./Software reference/Modules/Pin.md>) : Inputs / Outputs.
    - [](<./Software reference/Modules/Keyboard.md>) : PS2 external keyboard support.
    - [](<./Software reference/Modules/Sound.md>) : multi-inputs / outputs from : I2S, MP3, WAV, Files ...
  - Complementary :
    - [](<./Software reference/Modules/Log.md>) : simple logging system (serial output).
    - [](<./Software reference/Modules/Clipboard.md>) : simple system-shared clipboard.
    - [](<./Software reference/Modules/Mathematics.md>) : advanced mathematics functions.
  
- [Hardware development kit](https://github.com/Xila-Project/Hardware).
- Driver system to fit any type of architecture.
- High level Python-like programming language support : [Berry](https://berry-lang.github.io/).
- Graphical [Shell](https://github.com/Xila-Project/Shell).
- Multiple native software : [File manager](https://github.com/Xila-Project/File_Manager), [Preferences](https://github.com/Xila-Project/Preferences).
- Multiple berry software : [REPL](https://github.com/Xila-Project/Berry_REPL), [Rangefinder](https://github.com/Xila-Project/Rangefinder), [Calculator](https://github.com/Xila-Project/Calculator), etc.

## ✅ Requirements

Currently, Xila doesn't support a lot of board, but this list can easily be extended by adding drivers for new boards which is easy do. See [Supported hardware](../Hardware%20reference/Supported%20hardware) section for more information.

## 📖 Table of contents

```{toctree}
   :caption:   🚀 Get started
   :maxdepth:  1

Get started/Use
Get started/Development
Get started/Contributing
```

```{toctree}
   :caption:   📖 Software reference   
   :maxdepth:  2

Software reference/Structure
Software reference/Nomenclature
Software reference/Modules/Modules
Software reference/Registries/Registries
Software reference/Softwares/Softwares
Software reference/Types/Types
```

```{toctree}
   :caption:   🔌 Hardware reference
   :maxdepth:  1
Hardware reference/Supported hardware
Hardware reference/Reference kit
```

```{toctree}
   :caption:   ℹ️ About
   :maxdepth:  1

About/Change log
About/Roadmap
About/License
About/Credits
```

