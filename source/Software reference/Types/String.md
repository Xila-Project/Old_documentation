# 🔡 `String_Type` / `Static_String_Type`


## 👓 Overview

In order to avoid the `cstring` library which is necessary to reduce the memory footprint of strings, but is also tedious to use.
Xila implements classes allowing to manipulate character strings in a simple and efficient way.

::::{tab-set}
:::{tab-item} String_Type
`String_Type` is a class that allows to manipulate character strings. It is a dynamic string, which means that it can be modified in size. It is also a class that allows to manage the memory of the character string in a simple and efficient way. In order to avoid wasting memory,some operations have been prohibited (+) which can be substituted by other more efficient operations (+=).
:::

:::{tab-item} Static_String_Type
Similar to `String_Type` (it's parent class), `Static_String_Type` is a template class for manipulating strings. However, unlike `String_Type`, `Static_String_Type` is a static string, i.e. it cannot be changed in size. It is therefore faster to handle, but requires a static memory allocation which is not practical.
:::
::::

:::{warning}
`String_Type` cannot be pre-allocated when it's declared as a global variable.
It's due to the fact that it uses dynamic memory allocation, which may not be active at time of global variable creation.
:::

:::{important}
It's highly recommended to use `Static_String_Type` instead of `String_Type` when possible since it's faster, more efficient and avoid memory fragmentation.
:::

## 💡 Example

```cpp
    using namespace Xila;
       
    String_Type String_1("Hello world !"); // Create a String object and copy "Hello world !" to it.

    Static_String_Type<64> String_2;
    String_2 = "from Xila"; // Copy "from Xila" to String_2.

    String_1.Remove(String_1.Length() - sizeof(" !") + 1, sizeof(" !") - 1); // Remove " !" from String_1.
    String_1 += String_2; // Concatenate String_2 to String_1.

    if (String_1 == "Hello world from Xila") // Always true.
    {
        // ...
    }
```

## 📚 API reference

```{eval-rst}
.. doxygentypedef:: Xila_Namespace::String_Type

.. doxygenclass:: Xila_Namespace::String_Class
    :members:

.. doxygentypedef:: Xila_Namespace::Static_String_Type

.. doxygenclass:: Xila_Namespace::Static_String_Class
    :members:
```