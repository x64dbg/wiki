# Prerequisites

**Notice**: It is important to install the **exact** versions of the tools mentioned hereafter (special exception for Visual Studio 2013, for which you can also use the Professional or Enterprise editions). Don't come complaining if you didn't install the correct versions of the tools.

1. [Download Visual Studio 2013 Community Edition](https://www.visualstudio.com/en-us/news/vs2013-community-vs.aspx) (make sure to install MFC)
2. Download [Qt 5.6.0 (x32) for MSVC2013](http://download.qt.io/official_releases/qt/5.6/5.6.0/qt-opensource-windows-x86-msvc2013-5.6.0.exe), install in `C:\Qt\qt-5.6.0-x86-msvc2013`.
3. Download [Qt 5.6.0 (x64) for MSVC2013](http://download.qt.io/official_releases/qt/5.6/5.6.0/qt-opensource-windows-x86-msvc2013_64-5.6.0.exe), install in `C:\Qt\qt-5.6.0-x64-msvc2013`.
4. Download [Qt Creator 4.0.0](http://download.qt.io/official_releases/qtcreator/4.0/4.0.0/qt-creator-opensource-windows-x86-4.0.0.exe), install in `C:\Qt\qtcreator-4.0.0`.
5. [Get the Dependencies](Getting the Dependencies)
6. Clone the repository to your local drive. **Make sure to include the submodules in your clone command!**
```
git clone --recurse-submodules https://github.com/x64dbg/x64dbg.git
```

## Custom paths

If you install Qt and/or Visual Studio in different paths, you can set (global) environment variables to make [setenv.bat](https://github.com/x64dbg/x64dbg/blob/development/setenv.bat) create a custom environment for compiling with [build.bat](https://github.com/x64dbg/x64dbg/blob/development/build.bat).

- `set QT32PATH=C:\Qt\qt-5.6.0-x86-msvc2013\5.6\msvc2013\bin`
- `set QT64PATH=C:\Qt\qt-5.6.0-x64-msvc2013\5.6\msvc2013_64\bin`
- `set QTCREATORPATH=C:\Qt\qtcreator-4.0.0\bin`
- `set VSVARSALLPATH=C:\Program Files (x86)\Microsoft Visual Studio 12.0\VC\vcvarsall.bat`
- `set COVERITYPATH=C:\coverity\bin`
- `set DOXYGENPATH=C:\Program Files\doxygen\bin`

# For tools

**Notice**: You don't need to do this every time if you want to *develop* for x64dbg. In that case see the [For developers](https://github.com/x64dbg/x64dbg/wiki/Compiling-the-whole-project#for-developers) section.

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

*This video is slightly outdated.* The process is still the same, except that you have to install Qt 5.6.0 (see the first section of this documented).

There is a video available where the build process (after installing the prerequisites) is shown. It is available on [YouTube](https://youtu.be/M3J2wpXpeX0) and in [SWF Format](https://mega.nz/#!D4x1wQZD!LNz_K4GOhNuJlgS1oztlgdRhoZwPODWyQdd6ISUVvF0).