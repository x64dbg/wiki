# Prerequisites

**Notice**: It is important to install the **exact** versions of the tools mentioned hereafter (special exception for Visual Studio 2013, for which you can also use the Professional or Enterprise editions). **Do not come complaining if you didn't install the correct versions of the tools**.

1. [Download Visual Studio 2013 Community Edition](https://www.visualstudio.com/vs/older-downloads/#visual-studio-2013) (**make sure to install MFC**)
2. Download [Qt 5.6.2 (x32) for MSVC2013](https://download.qt.io/official_releases/qt/5.6/5.6.2/qt-opensource-windows-x86-msvc2013-5.6.2.exe), install in `C:\Qt\qt-5.6.2-x86-msvc2013`.
3. Download [Qt 5.6.2 (x64) for MSVC2013](https://download.qt.io/official_releases/qt/5.6/5.6.2/qt-opensource-windows-x86-msvc2013_64-5.6.2.exe), install in `C:\Qt\qt-5.6.2-x64-msvc2013`.
4. Download [Qt Creator 4.3.1](https://download.qt.io/official_releases/qtcreator/4.3/4.3.1/qt-creator-opensource-windows-x86-4.3.1.exe), install in `C:\Qt\qtcreator-4.3.1`.
5. Clone the repository to your local drive. **Make sure to include the submodules in your clone command!**
```
git clone --recurse-submodules https://github.com/x64dbg/x64dbg.git
```

## Custom paths

If you install Qt and/or Visual Studio in different paths, you can set (global) environment variables to make [setenv.bat](https://github.com/x64dbg/x64dbg/blob/development/setenv.bat) create a custom environment for compiling with [build.bat](https://github.com/x64dbg/x64dbg/blob/development/build.bat).

- `set QT32PATH=C:\Qt\qt-5.6.2-x86-msvc2013\5.6\msvc2013\bin`
- `set QT64PATH=C:\Qt\qt-5.6.2-x64-msvc2013\5.6\msvc2013_64\bin`
- `set QTCREATORPATH=C:\Qt\qtcreator-4.3.1\bin`
- `set VSVARSALLPATH=C:\Program Files (x86)\Microsoft Visual Studio 12.0\VC\vcvarsall.bat`
- `set COVERITYPATH=C:\coverity\bin`

# Compiling x64dbg

1. Run `install.bat` to initialize the pre-commit formatting hooks
2. Run `setupdeps.bat` to copy the dependencies
3. Open `x64dbg.sln` in Visual Studio 2013
4. Compile the solution (F7)
5. Open `src\gui\x64dbg.pro` in Qt Creator
6. Compile the GUI.

## Compiling with different Visual Studio/Qt versions

While unsupported (as in don't come complain), people have built x64dbg with Visual Studio 2015/2017 and/or newer Qt versions. If you use a different Qt version you have to recompile [snowman](https://github.com/x64dbg/snowman) (or use [SnowmanDummy](https://github.com/x64dbg/SnowmanDummy)) **and** delete all Qt-related DLLs from the `bin` directory and replace them with ones from your Qt version.

If you encounter build errors with newer Qt or Visual Studio versions, a [pull request](https://github.com/x64dbg/x64dbg/pull/1687) is appreciated.

## Video

*This video is slightly outdated.* The process is still the same, except that you have to install Qt 5.6.0 (see the first section of this documented).

There is a video available where the build process (after installing the prerequisites) is shown. It is available on [YouTube](https://youtu.be/M3J2wpXpeX0) and in [SWF Format](https://mega.nz/#!D4x1wQZD!LNz_K4GOhNuJlgS1oztlgdRhoZwPODWyQdd6ISUVvF0).

This is a video by `a_a_` but it uses Visual Studio 2017 and Qt 5.8 (both of which are currently not officially supported): https://vimeo.com/213004417  (
The video is a bit dated, and the "copy_libs.bat" script displayed in the video does not copy all required DLLs to the output folder. Make sure to run setupdeps.bat before running the "copy_libs.bat" displayed in the video in order to copy all required DLLs to the output folder. Alternatively, run setupdeps.bat and then delete all the Qt DLLs in the output bin folder, and replace them with ones from your Qt version.