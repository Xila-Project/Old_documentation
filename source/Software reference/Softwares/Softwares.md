# 📦 Softwares

Here you will find a full description of included native softwares.

## 👓 Overview

Here is the list of included softwares :

```{toctree}
:maxdepth: 1
Shell/Shell
Berry/Berry
File manager/File manager
Preferences/Preferences
```

You can add softwares by using the `Register_Handle` from [`Softwares`](<../Modules/Softwares.md>) module in the `main.cpp`.

See the [`Softwares`](<../Modules/Softwares.md>) module for more information.

## 💡 Example


```{code-block} cpp
    :caption: main.cpp
    :emphasize-lines: 12, 13, 14

    #include "Xila.hpp"

    #include "Shell.hpp"
    #include "Preferences.hpp"
    #include "File_Manager.hpp"
    #include "Berry.hpp"

    using namespace Xila;

    void setup()
    {
    Softwares.Register_Handle(Shell_Class::Handle);
    Softwares.Register_Handle(Preferences_Class::Handle);
    Softwares.Register_Handle(File_Manager_Class::Handle);
    
    // ...
    }

    /// ...
```