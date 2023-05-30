# `Software_Handle_Type`
 
Here you will find a full description of the `Software_Handle_Type`.

## 👓 Overview

In order to manage software, `Softwares` modules uses `Software_Handle_Type`. The latter contains the basic information of the software in question (name and constructor call). It's also used to identify a software (see `Software_Type`). `Software_Handle_Type` is intended to be derived by the developer, in order to create a software handle for each software.

:::{important}
Software handle must be registered in by the `Softwares` module in order to be used (using `Softwares.Register_Handle` method).
:::

## 💡 Example

```cpp
    using namespace Xila;

    class My_Software_Class : public Software_Type
    {
    public:
        static class My_Software_Handle_Class : public Software_Handle_Type
        {
        public:
            My_Software_Handle_Class() : Software_Handle_Type("My software") {} // - Register the software handle.

            void Create_Instance(const Accounts_Types::User_Type* Owner_User) const override // - Create a new instance of the software.
            {
                new My_Software_Class(Owner_User);
            }
        } My_Software_Handle;

        // ...
        
    private:

        // ...

        My_Software_Class();

        // ...

        friend class My_Software_Handle_Class; // - Allow the handle to access the software's constructor.
    };

```

## 📚 API reference

```{eval-rst}
.. doxygenclass:: Xila_Namespace::Softwares_Types::Software_Handle_Class
    :members:
```

