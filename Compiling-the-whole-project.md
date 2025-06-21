## Prerequisites

**Notice**: It is important to install the **exact** versions of the tools mentioned hereafter.

1. Install [Visual Studio 2022](https://visualstudio.microsoft.com/vs/)
   - Select _Desktop development with C++_, _CMake_ and _Git_.
8. Clone the repository to your local drive. **Make sure to include the submodules in your clone command!**
```
git clone --recursive https://github.com/x64dbg/x64dbg.git
```

Below is a video showing the installation process on a fresh VM:

https://github.com/user-attachments/assets/c9dd862c-88e3-4a11-a261-d6105fd6df41

## Compilation

The project uses a CMake project, which automatically fetches all the necessary dependencies. You can use many IDEs to work with CMake projects:

- [Visual Studio](https://learn.microsoft.com/en-us/cpp/build/cmake-projects-in-visual-studio)
- [Clion](https://www.jetbrains.com/clion)
- [Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cmake-tools)
- [Qt Creator](https://doc.qt.io/qtcreator)

Open the project folder in your favorite IDE and hit _Build_ to compile the project.

Below is a video showing the build process in Visual Studio:

https://github.com/user-attachments/assets/3217a2a1-1c2f-4a84-928f-8018017d51e2
