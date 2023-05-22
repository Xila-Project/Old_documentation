# 👥 Accounts

Here you will find a full description of the `Accounts` module.

## 👓 Overview

This module is responsible for managing user accounts, session and ensuring a minimum of security (although primitive).

Each user credentials are stored in a register specific to each user. The credentials are hashed, salted and peppered multiple times before being stored.

:::{caution}
In spite that credentials are hashed, salted and peppered, this module cannot be considered as secure. So don't use it for sensitive data.
:::

The user `Xila` is the **system user** and thus cannot be deleted. It has the highest privileges and special treatment.

:::{note}
Only one user can be logged at a time. When a user is logged, the other users are locked.
:::

### 〰️ Types

`Accounts` uses the following types :
- `User_Type` : A class that represents a user account.
- `User_State_Type` : An enumeration that represents the state of a user account.

## 💡 Example

```cpp
    using namespace Xila;

    if (Xila.Account.Check_Credentials("User", "Password") == Xila.Success) // -- Check if the credentials are correct.
    {
        // -- Do stuff when the credentials are rights.
    }
    else
    {
        // -- Do stuff when the credentials are wrong.
    }
    char Username[9];
    strlcpy(Username, Xila.Account.Get_Current_Username(), sizeof(Username));   // -- Get username of the current user.
    if (Xila.Account.Get_State == Xila.Account.Logged)  // -- Check user session state.
    {
        // -- Do stuff when user is connected.
    }
    else if (Xila.Account.Get_State == Xila.Account.Locked)
    {
        // -- Do stuff when user account is locked.
    }
    else
    {
        // -- Do stuff when no user is connected.
    }
```

## 📚 API reference

```{eval-rst}

.. doxygennamespace:: Xila_Namespace::Accounts_Types
    :members:

.. doxygenvariable::  Xila_Namespace::Accounts
    
.. doxygentypedef::   Xila_Namespace::Accounts_Type

.. doxygenclass::   Xila_Namespace::Accounts_Class
    :members:
```