# 🚀 Get started using Xila

Here you will find how to get started with Xila hardware and software.

## ✅ Requirements

- [Supported hardware](../../Hardware%20reference/Supported%20hardware.md).
- An SD card.
- [Visual Studio Code](https://code.visualstudio.com/) with [Platform IO IDE](https://platformio.org/install/ide?install=vscode) extension.
- [Git](https://git-scm.com/downloads).

## 📖 Steps

1. **Clone** the xila repository :
```bash
git clone https://github.com/Xila-Project/Code --recurse-submodules
```
:::{tip}
This operation can take a while since Git have to download all of the submodules.
:::

2. **Open** the cloned folder with Visual Studio Code.

```bash
code Xila
```

3. **Open** `Platform IO` and open the `Code` folder as a project.

:::{tip}
This operation can take a while since Platform IO have to download all the libraries. 
:::

4. **Change** the **selected environment** to the one corresponding to your hardware.

5. **Plug** your hardware to your computer and **upload** the code to it.

6. **Connect** your SD card to your computer and **format** it to FAT32.

7. **Copy** the content of the [Drive](https://github.com/Xila-Project/Code/tree/main/Drive) folder to the SD card.