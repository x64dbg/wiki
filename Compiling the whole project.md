# The easy way #

The easy way of compiling goes like this:

1. [Download VisualStudio 2010](http://download.microsoft.com/download/2/4/7/24733615-AA11-42E9-8883-E28CDCA88ED5/X16-42552VS2010UltimTrial1.iso)
2. [Download & Install Qt 4.8.6 (x32) for MSVC2010](http://download.qt-project.org/official_releases/qt/4.8/4.8.6/qt-opensource-windows-x86-vs2010-4.8.6.exe)
3. [Download & Install Qt 4.8.6 (x64) for MSVC2010](http://sourceforge.net/projects/qtx64/files/qt-x64/4.8.6/msvc2010/qt-4.8.6-x64-msvc2010-rev1.exe/download)
4. [Download Qt Creator](http://download.qt-project.org/official_releases/qtcreator/3.1/3.1.1/qt-creator-opensource-windows-x86-3.1.1.exe)
5. Set up kits for x32 and x64 in Qt Creator
6. Clone the repository on your PC
7. Run `install.bat` to initialize the repository
8. Open `x64_dbg.sln` in VisualStudio 2010
9. Compile the solution (F7)
10. Open `x64_dbg_gui\Project\DebuggerX64.pro` in Qt Creator
11. Setup MSVC2010 (x64+x32) to compile in a directory inside the `bin\*` directory
12. Click the '*Add Build Step*' button
13. Browse for `prebuildStep.bat`
14. Set arguments to the architecture `x32` or `x64`
15. Set working directory to `%{sourceDir}`
16. Move the build step up so it's the first in *Build Steps*
17. Click the '*Add Build Step*' button
18. Browse for `afterbuildStep.bat`
19. Set arguments to architecture (`x32` or `x64`) [space] `%{buildDir}\release` or `%{buildDir}\debug`
20. Set working directory to `%{sourceDir}`
21. Build the GUI
22. [Get the Dependencies](Getting the Dependencies)
23. Enjoy!

More Qt versions available [here](http://www.tver-soft.org/qt64)

# Screenshot #
![Build Configuration](/mrexodia/x64_dbg/wiki/images/x64dbg_build_example_new.png)