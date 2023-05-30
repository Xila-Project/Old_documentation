# ⛓️ Bindings

Here you will find a full description of how the bindings are generated.

## 👓 Overview

In order to use the Xila API from Berry, a binding is required.
A part of the binding is manually written in `Berry/src/Manual/` folder. But since Xila API is quite big, it is not possible to write the whole binding manually. So a script is used to generate the binding is available in `Berry/Generator/` folder. It is written in Python and uses the [PyGCCXML](https://github.com/CastXML/pygccxml) library to parse the Xila header files. It's a bit messy but it works.

## 📦 Install

To install the required libraries, run the following commands :

```bash
pip install pygccxml
```

:::{note}
If you are using recent version of Ubuntu, you must use `apt` to install `pygccxml` :

```bash
sudo apt install python3-pygccxml
```
:::

## ⚙️ Generate

To generate the binding, first you need to update the `Berry/Generator/compile_commands.json` :

1. Go the the Platform IO panel.
2. Click on the `Project Tasks` button.
3. Click on `Build` button.
4. Click on `Generate Compilation Database` button.

Then, you need to run the script with the following commands :

```bash
cd lib/Berry/Generator
python3 Generator.py
```

So, it is possible to use the almost whole API of Xila in Berry (some particular cases of methods / classes are still to be treated).