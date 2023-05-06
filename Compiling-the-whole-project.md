# Prerequisites

**Notice**: It is important to install the **exact** versions of the tools mentioned hereafter.

1. Install [Visual Studio 2013](https://my.visualstudio.com/Downloads?q=visual%20studio%202013%20with%20update%205&wt.mc_id=o~msft~vscom~older-downloads) (**make sure to install MFC**). You need to sign in with a Microsoft account (or GitHub) to access this page.

![Visual Studio 2013 Download](https://user-images.githubusercontent.com/2458265/236622035-cb8cfd3c-a2cf-41c8-a027-668fc8510eab.png)

2. Download [Qt 5.6.3 (x86) for MSVC2013](https://osdn.net/projects/x64dbg/storage/qt/qt-opensource-windows-x86-msvc2013-5.6.3.exe), install in `C:\Qt\qt-5.6.3-x86-msvc2013`.
3. Download [Qt 5.6.3 (x64) for MSVC2013](https://osdn.net/projects/x64dbg/storage/qt/qt-opensource-windows-x86-msvc2013_64-5.6.3.exe), install in `C:\Qt\qt-5.6.3-x64-msvc2013`.
4. Download [Qt Creator 4.3.1](https://download.qt.io/archive/qtcreator/4.3/4.3.1/qt-creator-opensource-windows-x86-4.3.1.exe), install in `C:\Qt\qtcreator-4.3.1`.
5. Install [CMake](https://cmake.org/download/) based on your architecture.
6. Install [Windows SDK](https://developer.microsoft.com/en-us/windows/downloads/windows-sdk/).
7. Clone the repository (`development` branch) to your local drive. **Make sure to include the submodules in your clone command!**
```
git clone --recurse-submodules -b development https://github.com/x64dbg/x64dbg.git
```

### Qt

Qt has [made some changes to their licensing](https://www.qt.io/blog/qt-offering-changes-2020) and deleted all the LTS packages (including source code) from their website. The original installers are mirrored on [SourceForge](https://sourceforge.net/projects/x64dbg/files/qt/) and [OSDN](https://osdn.net/projects/x64dbg/storage/qt/).

There is also a portable Qt archive [Qt5.6.3-msvc2013-installed.7z](https://osdn.net/projects/x64dbg/storage/qt/Qt5.6.3-msvc2013-installed.7z), which is just both those installers extracted.

#### Configuring Qt Creator

If you downloaded `Qt5.6.3-msvc2013-installed.7z` you have to create your own kits. Relevant documentation:

- https://doc.qt.io/qtcreator/creator-project-qmake.html#setting-up-new-qt-versions
- https://doc.qt.io/qtcreator/creator-targets.html

Some screenshots showing how to configure 32-bit MSVC2013 Qt 5.6.3:

![qt versions](https://i.imgur.com/ceYmTu5.png)

![qt kit](https://i.imgur.com/UjOqr9v.png)

Pay attention to the warnings and select the compiler version that matches your Qt version (`x86` for 32-bit, `amd64` for 64-bit).

# Compiling x64dbg

1. Run `install.bat` to initialize the pre-commit formatting hooks
2. Run `setupdeps.bat` to copy the dependencies
3. Open `x64dbg.sln` in Visual Studio 2013
4. Compile the solution **in Release mode**
5. Open `src\gui\x64dbg.pro` in Qt Creator
6. Compile the GUI **in Release mode**.

## Compiling with different Visual Studio/Qt versions

While unsupported, people have built x64dbg with Visual Studio 2015/2017/2019 and/or newer Qt versions. If you use a different Qt version you have to run `windeployqt.exe --force x64gui.dll` to do this automatically.

If you encounter build errors with newer Qt or Visual Studio versions, a pull request is appreciated!

You can get the latest Qt versions from: https://www.qt.io/offline-installers

If you do not like Qt Creator you can try the [Qt Visual Studio Tools](https://marketplace.visualstudio.com/items?itemName=TheQtCompany.QtVisualStudioTools2019).

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