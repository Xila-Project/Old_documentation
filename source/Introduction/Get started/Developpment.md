# 🔧 Get started with software development on Xila

## 🔧 Native software

### ✅ Requirements

- [Visual Studio Code](https://code.visualstudio.com/)
- [Platform IO IDE](https://platformio.org/install/ide?install=vscode) extension.
- [Git](https://git-scm.com/downloads).
- [Supported hardware](../../Hardware%20reference/Supported%20hardware.md).

### 📖 Steps

1. **Clone** the [Code](https://github.com/Xila-Project/Code)  repository :
```bash
git clone https://github.com/Xila-Project/Code.git --recurse-submodules
```

2. **Open** the cloned folder with Visual Studio Code :
```bash
code Code
```

3. **Open** the project in `Platform IO` (`platformio.ini` file).

4. **Change** the **selected environment** to the one corresponding to your hardware.

## 🍓 Berry software

### ✅ Requirements

- [Visual Studio Code](https://code.visualstudio.com/)
  - [Berry extension](https://marketplace.visualstudio.com/items?itemName=berry.berry)
- [Git](https://git-scm.com/downloads)

### 📖 Steps

1. **Create** a repository from the [Berry software template](https://github.com/Xila-Project/Berry_Software_Template).

2. **Clone** the repository :
```bash
git clone <URL of the forked repository> --recurse-submodule
```

3. Install Berry interpreter :
     - Linux (Debian) :
        - `sudo apt install libreadline-dev`
        - `cd Berry`
        - `make`
        - `make install`
    - Windows :
        - `cd Berry`
        - `make`
    - MacOS :
        - `brew install readline`
        - `cd Berry`
        - `make`
        - `make install` 

*Official installation steps can be found [here](https://github.com/berry-lang/berry).*

4. **Build** your software :
```bash
berry -c Main.be
```