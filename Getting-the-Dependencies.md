# Getting the Dependencies

**You do not have to do all these steps to get started with x64dbg development!** Just run `setupdeps.bat` to extract the dependencies in your build directory.

## Building dependencies by hand (not recommended)

x64dbg has various dependencies. Here is a list of them and how you can obtain them yourself. The easiest method is simply downloading the latest release from [Github](https://releases.x64dbg.com) and extract the binaries in the `bin` directory, but here is a guide **in case you want to do it manually** (Which you don't because it is hard to do and will waste your time. The snowman depends on QT library. If you compiled x64gui with debug build profile. Then you need download snowman source code and compile it using debug build profile too. Otherwise you will encounter crash issue).

### BeaEngine
Clone and compile the repository [here](https://bitbucket.org/mrexodia/beaengine).

### Capstone
Clone and compile the repository [here](https://github.com/aquynh/capstone).

### dbghelp & symserv
Get [Debugging Tools For Windows](https://go.microsoft.com/fwlink/p/?linkid=84137) and extract dbghelp.dll and symsrv.dll from the installation directory.

### DeviceNameResolver
Clone and compile the repository [here](https://bitbucket.org/mrexodia/devicenameresolver).

### jansson
Clone the repository [here](https://bitbucket.org/mrexodia/jansson), checkout the branch 'jansson_x64dbg' and compile using Visual Studio 2010.

### lz4
Clone and compile the repository [here](https://bitbucket.org/mrexodia/lz4).

### Scylla
Download the binaries from [here](https://tuts4you.com/download.php?view.3503), or manage to compile the repository [here](https://github.com/NtQuery/Scylla). Don't forget to rename to Scylla.dll.

### TitanEngine
Clone and compile the repository [here](https://bitbucket.org/titanengineupdate/titanengine-update).

### XEDParse
Clone and compile the repository [here](https://bitbucket.org/mrexodia/xedparse).

### snowman
Clone and compile the repository [here](https://github.com/x64dbg/snowman). You need to have Boost and Qt 4 (same version you use to compile x64dbg). You can also use [SnowmanDummy](https://github.com/x64dbg/SnowmanDummy) to disable snowman.