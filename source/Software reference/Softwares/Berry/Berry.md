# 🍓 Berry

Here you will find a full description of the `Berry` software.

## Table of contents

```{toctree}
:maxdepth:  1
Syntax
Bindings
```

## 👓 Overview

Berry is a software that embed a berry virtual machine that allow the compilation and execution of [Berry-Lang](https://github.com/berry-lang/berry) (like a JVM for Java). [Berry-Lang](https://github.com/berry-lang/berry) is an interpreted language.

It has been chosen because :
- It is lightweight.
- Easy to learn (Python-like syntax).
- Quite fast.
- Implement advanced programming concept (class, operators overload).

At startup, Berry (`Berry_Class::Load_Softwares_Handles()`) looks for all software folder that contains a "Main.be" file in the `/Softwares` folder. Then, it creates handles for all of them and registers all of them to the `Software` module.

When a user launch a Berry software, the Softwares is firstly compiled to bytecode and then loaded in memory for execution. Once the software execution is finished (escape the global scope), all software freed all at once. No need to delete anything since everything is allocated in the VM virtual memory.

## 💡 Examples

Multiples examples are available :
- [Berry REPL](https://github.com/Xila-Project/Berry_REPL)
- [Rangefinder](https://github.com/Xila-Project/Rangefinder)
- [Calculator](https://github.com/Xila-Project/Calculator)

You can also use the [template](https://github.com/Xila-Project/Berry_Software_Template).

## 📚 API reference

```{eval-rst}
.. doxygenclass:: Berry_Class
    :members:
```