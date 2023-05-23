# 🗂️ Structure

Here you will find a full description of the Xila's structure.

Xila is made up of the following repositories :

| Repository | Description |
| :--- | :--- |
| [Code](https://github.com/Xila-Project/Code) | Contains the source code. |
| [Documentation](https://github.com/Xila-Project/Documentation) | Contains the sources of the [documentation](https//documentation.xila.dev). |
| [Website](https://github.com/Xila-Project/Website) | Contains the source code of the [website](https://xila.dev). |
| [Berry Software Template](https://github.com/Xila-Project/Berry_Software_Template) | Template repository to create software for Xila with [Berry](https://github.com/berry-lang/berry). |
| [Assets](https://github.com/Xila-Project/Assets) | Contains the assets (images, sounds, etc.). |
| [Hardware](https://github.com/Xila-Project/Hardware) | Contains the design (case, pcb, schematics, etc.) of hardware development kit. |
| [Shell](https://github.com/Xila-Project/Shell) | Contains the source code of the shell software. |
| [File Manager](https://github.com/Xila-Project/File_Manager) | Contains the source code of the file manager software. |
| [Preferences](https://github.com/Xila-Project/Preferences) | Contains the source code of the preferences software. |
| [Berry_REPL](https://github.com/Xila-Project/Berry_REPL), [Rangefinder](https://github.com/Xila-Project/Rangefinder), [Calculator](https://github.com/Xila-Project/Calculator), etc. | Contains berry softwares that are developed for example purposes. |


## Code

Here is a graph representing all of the dependencies between the different files of Xila.

```{mermaid}

stateDiagram-v2

    state Platform_IO {
        Board
        Flags
    }

    Platform_IO --> Configuration

    state Configuration {
        Configuration.hpp
        Paths.hpp
        Hardware.hpp
    }

    state Base_Types {
       Base_Types.hpp
       IP_Address.hpp
       
    }

    Base_Types --> Module.hpp

    Configuration --> Module.hpp

    Module.hpp --> Modules

    Module.hpp --> Software.hpp

    Module.hpp --> Software_Handle.hpp

    Software_Handle.hpp --> Software.hpp

    state Modules {
        Accounts.hpp
        Clipboard.hpp
        Display.hpp
        Drive.hpp
        Time.hpp
        Flash.hpp
        Keyboard.hpp
        Mathematics.hpp
        Memory.hpp
        Pin.hpp
        Power.hpp

        state Communication.hpp {
            WiFi.hpp
            Bluetooth.hpp

        }

        state Graphics {
            Animation.hpp
            Arc.hpp
            
        }
    }

    Modules --> Core.hpp

    Core.hpp --> Xila.hpp

    Core.hpp --> Sources

    state Sources {
        Core.cpp
    }

    Xila.hpp --> User_Part

    Xila.hpp --> Softwares

    state Softwares {
        Shell.hpp
        ...
    }
    
    state User_Part {
        Main.cpp
    }

```