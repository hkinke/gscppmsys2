# Getting Started with C/C++ and MSYS2

## Introduction

Msys2 offers the same tools as Linux to build software on Windows.

## Installation

- Download and install MSYS2 ([page](https://www.msys2.org/),[installer](https://github.com/msys2/msys2-installer/releases/download/2023-03-18/msys2-x86_64-20230318.exe)). You can also use package managers like `Chocolatey` or `Scoop` to install MSYS2:
    Use this command to install with Chocolatey:
    ```ps1
    choco install msys2
    ```
    Use this command to install with scoop:
    ```ps1
    scoop install msys2
    ```
- Install `gcc`
    ```bash
    pacman -S mingw-w64-x86_64-gcc
    ```
- Install `ninja`
    ```bash
    pacman -S git mingw-w64-x86_64-ninja 
    ```
- Install `cmake`
    ```bash
    pacman -S mingw-w64-x86_64-cmake
    ```
- Install [Visual Studio Code](https://code.visualstudio.com/Download).
- Install [C/C++ Extension Pack](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cmake-tools) for Visual Studio Code. You can also install from commandline
    ```
    code --install-extension ms-vscode.cpptools-extension-pack
    ```
- The next step is to clone starting repository
    ```bash
    git clone https://github.com/hkinke/gscppmsys2.git hello
    ```
- Change the folder
    ```bash
    cd hello
    ```
- Change the replace `gscppmsys2` in `CMakeLists.txt` with the name of your project by example `hello`.
    ```cmake
    cmake_minimum_required(VERSION 3.18)


    project(hello)

    add_executable(main main.cpp)
    ```
- From Visual Studio Code, choose the `Mingw64` kit, configure, and build your project.
- Lunch you application (you can use Visual Studio Code integrated terminal `` Ctrl+Shift+` ``)
    ```bash
    ./build/main
    ```
    which gives the output
    ```plain
    hello from Msys2
    ```

