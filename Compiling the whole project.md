# The easy way #

The easy way of compiling goes like this:

1. [Download Visual Studio 2013 Community Edition](https://www.visualstudio.com/products/visual-studio-community-vs) (make sure to install MFC)
2. [Download & Install Qt 4.8.6 (x32) for MSVC2013](http://sourceforge.net/projects/qt64ng/files/qt/x86/4.8.6/msvc2013/qt-4.8.6-x86-msvc2013.exe/download)
3. [Download & Install Qt 4.8.6 (x64) for MSVC2013](http://sourceforge.net/projects/qt64ng/files/qt/x86-64/4.8.6/msvc2013/qt-4.8.6-x64-msvc2013.exe/download)
4. [Download Qt Creator](http://download.qt-project.org/official_releases/qtcreator/3.1/3.1.1/qt-creator-opensource-windows-x86-3.1.1.exe)
5. Set up kits for x32 and x64 in Qt Creator
6. Clone the repository on your PC
7. Run `install.bat` to initialize the repository
8. Open `x64_dbg.sln` in VisualStudio 2013
9. Compile the solution (F7)
10. Open `x64_dbg_gui\Project\DebuggerX64.pro` in Qt Creator
11. Setup Qt Creator (x64+x32) to compile in a directory inside the `bin\*` directory (see screenshot)
12. Click the '*Add Build Step*' button
13. Browse for `prebuildStep.bat`
14. Set arguments to the architecture `x32` or `x64`
15. Set working directory to `%{sourceDir}`
16. Move the build step up so it's the first in *Build Steps*
17. Click the '*Add Build Step*' button
18. Browse for `afterbuildStep.bat`
19. Set arguments to architecture (`x32` or `x64`) [space] `%{buildDir}\release` or `%{buildDir}\debug`
20. Set working directory to `%{sourceDir}`
21. Build the GUI (see screenshot)
22. [Get the Dependencies](Getting the Dependencies)
23. Enjoy!

More Qt versions available [here](https://sourceforge.net/projects/qt64ng/files)

# Screenshot #
![Build Configuration](/mrexodia/x64_dbg/wiki/images/x64dbg_build_example_new.png)