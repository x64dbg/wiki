Because of the increased maintenance burden and lack of resources, we have decided to _permanently_ drop support for the following operating systems:

|OS|EOL Date|x64dbg|Status|
|-|-|-|-|
|Windows XP|[April 2014](https://learn.microsoft.com/en-us/lifecycle/products/windows-xp)|11 extra years|**No longer runs**|
|Windows 7|[January 2020](https://learn.microsoft.com/en-us/lifecycle/products/windows-7)|5 extra years|Unsupported|
|Windows 8.1|[January 2023](https://learn.microsoft.com/en-us/lifecycle/products/windows-81)|2 extra years|Unsupported|

For the past 11 years, x64dbg has used Visual Studio 2013 and Qt 5.6 to produce the releases. These technologies are so old that it is almost impossible to legally obtain them and this prevents new contributors joining the project.

We have transitioned to Visual Studio 2022 and Qt 5.15. You can find more technical information in issue [#3412](https://github.com/x64dbg/x64dbg/issues/3412).

Binary compatibility has been an important goal from the start of the project and the very first plugins ever created still work today. Unfortunately this transition means that **plugins using Qt will need to be updated and recompiled to work**.

To summarize:
- Operating systems below **Windows 10** will not longer be supported in newer x64dbg versions. **Windows XP** will no longer run x64dbg. **Windows 7** currently can still run x64dbg, but it may break at any time.
- Certain plugins linking to Qt will stop working.
- We plan to make it easier for new contributors to join the project.

## Future plans

After this transition we are planning some exciting updates. Follow [@x64dbg](https://x.com/x64dbg) and the [blog](https://x64dbg.com/blog/) to stay up to date!

## Older versions

For users who need an older version of x64dbg that works on Windows XP, you can build the [`xp-deprecated`](https://github.com/x64dbg/x64dbg/tree/xp-deprecated) branch with the instructions [here](https://github.com/x64dbg/wiki/blob/14c46b3e482f0fa025c349946b1f18cdab89ed60/Compiling-the-whole-project.md). Note that you are fully on your own and no support will be provided. Some notes for trying to get the project to build/run for XP:

- Compiler options
  - `/Zc:threadSafeInit-`
  - `-DWINVER=0x0502`
  - `-D_WIN32_WINNT=0x0502`
  - `-DNTDDI_VERSION=0x05010300`
- Last supported MSVCRT version: 14.27.29016
- Last supported toolset: 14.27.29110
- Links
  - https://github.com/Chuyu-Team/YY-Thunks
  - https://github.com/shorthorn-project/One-Core-API-Source
  - https://github.com/YuZhouRen86/VxKex-NEXT
  - https://code.videolan.org/videolan/vlc/-/tree/43da4df125d484066576ffcfecd9ba1a8b15c3ff/contrib/src/qt

_Note_: If you decide to maintain XP support somewhere, let us know so we can edit the wiki!
