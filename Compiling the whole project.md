# The easy way #
The easy way of compiling goes like this:

1. [Download VisualStudio 2012](http://www.microsoft.com/en-us/download/details.aspx?id=30678)
2. [Download Qt5 (x64+x32) for MSVC2012](http://qt-project.org/downloads)
3. [Download Qt Creator](http://qt-project.org/downloads#qt-creator)
4. Clone the repository on your PC
5. Open 'x64_dbg.sln' in VisualStudio2012
6. Compile (in this order): x64_dbg_bridge, x64_dbg_dbg, x64_dbg_exe
4. Open 'x64_dbg_gui\Project\DebuggerX64.pro' in Qt Creator
5. Setup MSVC2012 (x64+x32) to compile in a directory inside the 'bin\*' directory
6. Click the 'Add Build Step' button
7. Browse for 'prebuildStep.bat'
8. Set arguments to the architecture 'x32' or 'x64'
9. Set working directory to '%{sourceDir}'
10. Move the build up so it's the first Build Step
11. Click the 'Add Build Step' button
12. Browse for 'afterbuildStep.bat'
13. Set arguments to architecture ('x32' or 'x64') [space] '%{buildDir}\release' or '%{buildDir}\debug'
14. Set working directory to '%{sourceDir}'