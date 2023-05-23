# 📅 `Date_Type` / `Time_Type`

## 👓 Overview

In order to simplify the use of dates and times, Xila has defined two types: `Date_Type` and `Time_Type`.

:::{tip}
    `Date_Type` is an alias of `Date_Class` and `Time_Type` is an alias of `Time_Class`.
:::

## 💡 Example

```cpp
using namespace Xila;

Date_Type Date_1(2020, 12, 31); // - Create and set date.

Date_Type Date_2;
Date_2.Set(2008, 4, 24); // - Set date.


Date_Type Date_4;
// - Set each part of the date independently.
Date_4.Set_Day(1);
Date_4.Set_Month(1);
Date_4.Set_Year(2000);

Date_Type Date_3 = Date_1;  // Copy.

// - Check if dates are equal.
if (Date_1 == Date_3)   
{
    // Always true.
}

// - Check if dates are different.
if (Date_1 != Date_2)   
{
    // Always true.
}

```

## 📚 API reference

```{eval-rst}
.. doxygentypedef:: Xila_Namespace::Date_Type

.. doxygenclass:: Xila_Namespace::Date_Class
    :members:

.. doxygentypedef:: Xila_Namespace::Time_Type

.. doxygenclass:: Xila_Namespace::Time_Class
    :members:
```