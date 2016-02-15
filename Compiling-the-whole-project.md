# Prerequisites

**Notice**: It is important to install the **exact** versions of the tools mentioned hereafter (special exception for Visual Studio 2013, for which you can also use the Professional or Enterprise editions). Don't come complaining if you didn't install the correct versions of the tools.

1. [Download Visual Studio 2013 Community Edition](https://www.visualstudio.com/en-us/news/vs2013-community-vs.aspx) (make sure to install MFC)
2. [Download & Install Qt 4.8.6 (x32) for MSVC2013](http://sourceforge.net/projects/qt64ng/files/qt/x86/4.8.6/msvc2013/qt-4.8.6-x86-msvc2013.exe/download)
3. [Download & Install Qt 4.8.6 (x64) for MSVC2013](http://sourceforge.net/projects/qt64ng/files/qt/x86-64/4.8.6/msvc2013/qt-4.8.6-x64-msvc2013.exe/download)
4. [Download Qt Creator 3.1.1](http://download.qt-project.org/official_releases/qtcreator/3.1/3.1.1/qt-creator-opensource-windows-x86-3.1.1.exe)
5. [Get the Dependencies](Getting the Dependencies)
6. Clone the repository to your local drive. Make sure to include the submodules in your clone command:
```
git clone --recurse-submodules https://github.com/x64dbg/x64dbg.git
```

# For tools

**Notice**: You don't need to do this every time if you want to *develop* for x64dbg. In that case see the "For developers" section.

1. Run `build.bat x32` and `build.bat x64` to build everything.

# For developers

1. Run `install.bat` to initialize the repository
2. Open `x64dbg.sln` in Visual Studio 2013
3. Compile the solution (F7)
4. Open `src\gui\x64dbg.pro` in Qt Creator
5. Compile the GUI.

**Notice**: Sometimes if you modifiy `Q_OBJECT` header files you need to rebuild the GUI to fix a weird crash.

More Qt versions available [here](https://sourceforge.net/projects/qt64ng/files)

# Video

There is a video available where the build process (after installing the prerequisites) is shown. It is available on [YouTube](https://youtu.be/M3J2wpXpeX0) and in [SWF Format](https://mega.nz/#!D4x1wQZD!LNz_K4GOhNuJlgS1oztlgdRhoZwPODWyQdd6ISUVvF0).