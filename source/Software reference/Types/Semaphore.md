# 🚦 `Semaphore_Type`

## 👓 Overview

A semaphore is a variable or abstract data type used to control access to a common resource by multiple tasks and avoid critical section problems in a concurrent system. 

For a more concise use, `Semaphore_Type` also offers the `Auto_Semaphore_Type`, which take and give the semaphore automatically according to the scope.

### Types

`Semaphore_Type` uses the following types :
- `Semaphore_Type_Type`
- `Auto_Semaphore_Type`

## 💡 Example

```cpp
    using namespace Xila;

    Semaphore_Type Semaphore;
    if (Semaphore.Create(Semaphore_Type_Type::Recursive_Mutex) == Result_Type::Success)
    {
        Semaphore.Take();
        // - Do something.
        Semaphore.Give();
        // - Do something.

        // - Or use the Auto_Semaphore_Type.
        {
            Auto_Semaphore_Type Auto_Semaphore(Semaphore);
            // - Do something.
        }

        Semaphore.Delete();
    }
```


## 📚 API reference

```{eval-rst}
.. doxygenenum:: Xila_Namespace::Semaphore_Type_Type

.. doxygentypedef:: Xila_Namespace::Auto_Semaphore_Type

.. doxygenclass:: Xila_Namespace::Auto_Semaphore_Class
    :members:

.. doxygentypedef::   Xila_Namespace::Semaphore_Type

.. doxygenclass::   Xila_Namespace::Semaphore_Class
    :members:
```