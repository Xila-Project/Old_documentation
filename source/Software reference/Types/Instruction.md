# ✉️ `Instruction_Type`

Here you will find a full description of the `Instruction_Type`.

## 👓 Overview

To allow `Modules` and `Software` to communicate with each other, Xila uses `Queue` systems. These allow you to send and receive data asynchronously. In order to have a standard format during this communication, the `Instruction_Type` type has been defined.

## 💡 Example

```cpp
    using namespace Xila;

    void My_Software::Main_Task(void*)
    {
        while (true)
        {
            if (this->Available_Instruction())
            {
                Instruction_Type Instruction = this->Get_Instruction();
                if (Instruction.Get_Sender() == &Graphics)
                {
                    switch (Instruction.Graphics.Get_Code())
                    {
                    case Graphics_Types::Event_Code_Type::Clicked:
                        Graphics_Types::Object_Type Target = Instruction.Graphics.Get_Target()
                        
                        // - Do something with the target.

                        break;
                    }
                }

            }

        }
    }
```

## 📚 API reference

```{eval-rst}
.. doxygentypedef:: Xila_Namespace::Instruction_Type

.. doxygenclass::   Xila_Namespace::Instruction_Class
    :members:
```