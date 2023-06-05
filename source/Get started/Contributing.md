# 🔬 Get started contributing

Here you will find how to get started to contribute to Xila.

## Code

### ✅ Requirements

- [Supported hardware](../../Hardware%20reference/Supported%20hardware.md).
- [Git](https://git-scm.com/downloads).
- [Visual Studio Code](https://code.visualstudio.com/) with [Platform IO IDE](https://platformio.org/install/ide?install=vscode) extension.

### 📖 Steps

1. **Fork** the [Code](https://github.com/Xila-Project/Code) repository on GitHub.

2. **Clone** the forked repository :
```bash
git clone <URL of the forked repository> --recurse-submodule
```
:::{note}
This operation can take a while since Git have to download all of the submodules.
:::

3. **Open** the cloned folder with Visual Studio Code.
```bash
code Xila
```

4. **Open** `Platform IO` and open the `Code` folder as a project.

:::{note}
This operation can take a while since Platform IO have to download all the libraries. 
:::

5. **Change** the **selected environment** to the one corresponding to your hardware.

## 📖 Documentation

### ✅ Requirements

- [Git](https://git-scm.com/downloads)
- [Python](https://www.python.org/downloads/)
- [Doxygen](https://www.doxygen.nl/download.html)
- [Sphinx](https://www.sphinx-doc.org/en/master/usage/installation.html)
- [Myst-Parser](https://myst-parser.readthedocs.io/en/latest/index.html)
- [Breath](https://breathe.readthedocs.io/en/latest/)
- [Linkify-it-py](https://linkify-it-py.readthedocs.io/en/latest/index.html)
- [Sphinx book theme](https://sphinx-book-theme.readthedocs.io/en/stable/)
- [Sphinx copybutton](https://sphinx-copybutton.readthedocs.io/en/latest/)
- [Sphinx mermaid](https://github.com/mgaitan/sphinxcontrib-mermaid)
- [Sphinx design](https://sphinx-design.readthedocs.io/en/latest/)

:::{tip}
All of the python dependencies can be installed using pip :
```bash
pip install -r /path/to/Documentation/requirements.txt
```
:::

### 📖 Steps

1. **Fork** the [Documentation](https://github.com/Xila-Project/Documentation) repository on GitHub.

2. **Clone** the forked repository :
```bash
git clone <URL of the forked repository> --recurse-submodule
```
:::{note}
This operation can take a while since Git have to download all of the submodules.
:::

3. **Open** a terminal and go to the `Documentation` folder.

4. **Build** the documentation using the following commands :
```bash
make html
```

The result then can be found in the `Documentation/build/html` folder.

## Website

### ✅ Requirements

- [Hugo](https://gohugo.io/getting-started/installing/)
- [Git](https://git-scm.com/downloads)

### 📖 Steps

1. **Fork** the [Website](https://github.com/Xila-Project/Website) repository on GitHub.

2. **Clone** the forked repository :
```bash
git clone <URL of the forked repository> --recurse-submodule
```

3. **Open** a terminal and go to the `Website` folder.

4. **Build** the website using the following commands :
```bash
hugo server
```