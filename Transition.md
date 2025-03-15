Because of the increased maintenance burden and lack of resources, we have decided to _permanently_ drop support for the following operating systems:

|OS|EOL Date|x64dbg|
|-|-|-|
|Windows 8.1|[January 2023](https://learn.microsoft.com/en-us/lifecycle/products/windows-81)|2 extra years|
|Windows 7|[January 2020](https://learn.microsoft.com/en-us/lifecycle/products/windows-7)|5 extra years|
|Windows XP|[April 2014](https://learn.microsoft.com/en-us/lifecycle/products/windows-xp)|11 extra years|

For the past 11 years, x64dbg has used Visual Studio 2013 and Qt 5.6 to produce the releases. These technologies are so old that it is almost impossible to legally obtain them and this prevents new contributors joining the project.

Very soon we will transition to Visual Studio 2022 and Qt 5.15. You can find more technical information in issue [#3412](https://github.com/x64dbg/x64dbg/issues/3412).

Binary compatibility has been an important goal from the start of the project and the very first plugins ever created still work today. Unfortunately this transition means that **plugins using Qt will need to be updated and recompiled to work**.

To summarize:
- Operating systems below Windows 10 will not longer be supported in newer x64dbg versions.
- Certain plugins linking to Qt will stop working.
- We plan to make it easier for new contributors to join the project.

## Future plans

After this transition we are planning some exciting updates. Follow [@x64dbg](https://x.com/x64dbg) and the [blog](https://x64dbg.com/blog/) to stay up to date!
