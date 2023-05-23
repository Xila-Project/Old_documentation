# 🔈 Sound

Here you will find a full description of the `Sound` abstraction layer.

## 👓 Overview

This module allows to play multiples streams of audio to multiples outputs. It is using [Arduino Audio Tools](https://github.com/pschatzmann/arduino-audio-tools) library from [Phil Schatzmann](http://pschatzmann.ch/).

```{mermaid}
flowchart LR
    subgraph Inputs
        direction LR
        File
        Web_stream[Web stream]
    end
    Inputs-->Mixer
    Mixer-->Volume
    subgraph Outputs
        direction LR
        D.A.C.
        P.W.M.
        Bluetooth
    end
    Volume-->Outputs
```

## Types

The `Sound` module is using the following types :

```{toctree}
    :maxdepth: 1

Sound/I2S
Sound/File Player
Sound/Volume
Sound/Stream
Sound/Decoder
```



## 💡 Example

```cpp
    using namespace Xila;
    using namespace Xila::Sound_Types;

    auto Volume = Sound.Get_Volume();   // -- Get current volume.

    Sound.Set_Volume(150); // -- Set volume to .

    Stream_Type& Stream = Xila.Sound.Get_Current_Output_Stream();
```

## 📚 API reference

```{eval-rst}
.. doxygenvariable:: Xila_Namespace::Sound

.. doxygentypedef:: Xila_Namespace::Sound_Type

.. doxygenclass::   Xila_Namespace::Sound_Class
    :members:
```
