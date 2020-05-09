# Prerequisites

**Notice**: It is important to install the **exact** versions of the tools mentioned hereafter (special exception for Visual Studio 2013, for which you can also use the Professional or Enterprise editions). **Do not come complaining if you didn't install the correct versions of the tools**.

1. Download [Visual Studio 2013 Community Edition](https://my.visualstudio.com/Downloads?q=visual%20studio%202013&wt.mc_id=o~msft~vscom~older-downloads) ([direct](https://go.microsoft.com/fwlink/?LinkId=532495&clcid=0x409)) (**make sure to install MFC**).
2. Download [Qt 5.6.3 (x86) for MSVC2013](https://sourceforge.net/projects/x64dbg/files/qt/qt-opensource-windows-x86-msvc2013-5.6.3.exe/download), install in `C:\Qt\qt-5.6.3-x86-msvc2013`.
3. Download [Qt 5.6.3 (x64) for MSVC2013](https://sourceforge.net/projects/x64dbg/files/qt/qt-opensource-windows-x86-msvc2013_64-5.6.3.exe/download), install in `C:\Qt\qt-5.6.3-x64-msvc2013`.
4. Download [Qt Creator 4.3.1](https://download.qt.io/archive/qtcreator/4.3/4.3.1/qt-creator-opensource-windows-x86-4.3.1.exe), install in `C:\Qt\qtcreator-4.3.1`.
5. Clone the repository (`development` branch) to your local drive. **Make sure to include the submodules in your clone command!**
```
git clone --recurse-submodules -b development https://github.com/x64dbg/x64dbg.git
```

### Qt

Qt has [made some changes to their licensing](https://www.qt.io/blog/qt-offering-changes-2020) and deleted all the LTS packages (including source code) from their website. The original installers are mirrored on [SourceForge](https://sourceforge.net/projects/x64dbg/files/qt/) and [OSDN](https://osdn.net/projects/x64dbg/storage/qt/).

There is also a portable Qt archive `Qt5.6.3-msvc2013-installed.7z`, which is just both those installers extracted.

# Compiling x64dbg

1. Run `install.bat` to initialize the pre-commit formatting hooks
2. Run `setupdeps.bat` to copy the dependencies
3. Open `x64dbg.sln` in Visual Studio 2013
4. Compile the solution **in Release mode**
5. Open `src\gui\x64dbg.pro` in Qt Creator
6. Compile the GUI **in Release mode**.

## Compiling with different Visual Studio/Qt versions

While unsupported (as in don't come complain), people have built x64dbg with Visual Studio 2015/2017 and/or newer Qt versions. If you use a different Qt version you have to delete all Qt-related DLLs from the `bin` directory and replace them with ones from your Qt version.

If you encounter build errors with newer Qt or Visual Studio versions, a [pull request](https://github.com/x64dbg/x64dbg/pull/1687) is appreciated.

## Video

*This video is slightly outdated.* The process is still the same, except that you have to install Qt 5.6.0 (see the first section of this documented).

There is a video available where the build process (after installing the prerequisites) is shown. It is available on [YouTube](https://youtu.be/M3J2wpXpeX0) and in [SWF Format](https://mega.nz/#!D4x1wQZD!LNz_K4GOhNuJlgS1oztlgdRhoZwPODWyQdd6ISUVvF0).

This is a video by `a_a_` but it uses Visual Studio 2017 and Qt 5.8 (both of which are currently not officially supported): https://vimeo.com/213004417  Note: The video is a bit dated, and the `copy_libs.bat` script displayed in the video does not copy all required DLLs to the output folder. Make sure to run `setupdeps.bat` before running the `copy_libs.bat` displayed in the video in order to copy all required DLLs to the output folder. Alternatively, run `setupdeps.bat` and then delete all the Qt DLLs in the output bin folder, and replace them with ones from your Qt version.

## Custom paths

If you install Qt and/or Visual Studio in different paths, you can set (global) environment variables to make [setenv.bat](https://github.com/x64dbg/x64dbg/blob/development/setenv.bat) create a custom environment for compiling with [build.bat](https://github.com/x64dbg/x64dbg/blob/development/build.bat).

- `set QT32PATH=C:\Qt\qt-5.6.3-x86-msvc2013\5.6\msvc2013\bin`
- `set QT64PATH=C:\Qt\qt-5.6.3-x64-msvc2013\5.6\msvc2013_64\bin`
- `set QTCREATORPATH=C:\Qt\qtcreator-4.3.1\bin`
- `set VSVARSALLPATH=C:\Program Files (x86)\Microsoft Visual Studio 12.0\VC\vcvarsall.bat`