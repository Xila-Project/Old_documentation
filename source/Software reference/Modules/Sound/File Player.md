# `File_Player_Type`

Here you will find a full description of the `File_Player_Type`.

## 👓 Overview

This type allows to play a file to an output stream.

## 💡 Example

```cpp
    using namespace Xila;
    using namespace Xila::Sound_Types;

    void My_Software::Play_Music()
    {
        File_Type Sound = Drive.Open("Sound.wav"); // Open file.

        WAV_Decoder_Type WAV_Decoder;
        File_Player_Type File_Player(Sound.Get_Current_Output_Stream(), Output_Stream, WAV_Decoder);

        File_Player.Begin();

        File_Player.Set_Time(15); // Set time to 15 seconds.

        auto Current_Time = File_Player.Get_Time(); // Get current time (15).
        auto Total_Time = File_Player.Get_Total_Time(); // Get total time.

        while (File_Player.Loop() != 0)
            Main_Task.Delay(2);         // Add delay to avoid overloading the system.

        File_Player.End();
    }

```

## 📚 API reference

```{eval-rst}
.. doxygentypedef:: Xila_Namespace::Sound_Types::File_Player_Type

.. doxygenclass::   Xila_Namespace::Sound_Types::File_Player_Class
    :members:
```