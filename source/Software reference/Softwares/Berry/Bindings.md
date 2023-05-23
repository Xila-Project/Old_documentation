# ⛓️ Bindings

In order to use the Xila API from Berry, a binding is required.

In addition to that, since Berry is written in C, some weird tricks are required.

A script that generates the binding for (almost) all the Xila API is available in `Berry/Generator/` folder. It is written in Python and uses the [PyGCCXML](https://github.com/CastXML/pygccxml) library to parse the Xila header files. It's a bit messy but it works.

To generate the binding, you need to run the script with the following commands :

```bash
cd lib/Berry/Generator
python3 Generator.py
```

A part of the binding is manually written in `Berry/src/Manual/` folder.

So, it is possible to use the almost whole API of Xila in Berry (some particular cases of methods / classes are still to be treated).