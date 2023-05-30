# `IP_Address_Type`

## 👓 Overview

In order to simplify the use of IP addresses, Xila has wrapper for it: `IP_Address_Type`.

## 💡 Example

```cpp
using namespace Xila;
using namespace Xila::Communication_Types;

IP_Address_Type IP(); // - Create a blank IP address.
IP_Address_Type IP_1(192, 168, 1, 1); // - Create and set IP address.
```

## 📚 API reference

```{eval-rst}
.. doxygentypedef:: Xila_Namespace::Communication_Types::IP_Address_Type

.. doxygenclass:: Xila_Namespace::Communication_Types::IP_Address_Class
    :members:
```

