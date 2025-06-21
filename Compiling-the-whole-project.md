## Prerequisites

- Install [Visual Studio](https://visualstudio.microsoft.com/vs/)
  - Select _Desktop development with C++_, _CMake_ and _Git_.

Below is a video showing the installation process from start to finish:

https://github.com/user-attachments/assets/c9dd862c-88e3-4a11-a261-d6105fd6df41

## Compilation

You need to clone the repository on your local drive. **Make sure to include the submodules in your clone command!**

```sh
git clone --recursive https://github.com/x64dbg/x64dbg.git
```

The project uses a CMake project, which automatically fetches all the necessary dependencies. You can use many IDEs to work with CMake projects:

- [Visual Studio](https://learn.microsoft.com/en-us/cpp/build/cmake-projects-in-visual-studio)
- [Clion](https://www.jetbrains.com/clion)
- [Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cmake-tools)
- [Qt Creator](https://doc.qt.io/qtcreator)

Simple open the project folder in your favorite IDE and hit _Build_ to compile the project.

Below is a video showing the compilation process in Visual Studio:

https://github.com/user-attachments/assets/3217a2a1-1c2f-4a84-928f-8018017d51e2
