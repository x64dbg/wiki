This section contains questions frequently encountered about x64dbg. Feel free to add your own answers to not-so-obvious things.

***

**Q**: Why isn't process X shown in the attach dialog?

**A**: If x64dbg cannot get a handle to a process it will not show it in the attach dialog. Go to setting and make sure the `Enable Debug Privilege` option is checked in the `Engine` tab. Also make sure you are running x64dbg as an administrator. If your process is still not shown, make sure a kernel driver is not [protecting it](http://www.alex-ionescu.com/?p=97).

![debug priv](https://i.imgur.com/juQs94X.png)

***

**Q**: Help, I cannot change the command line of a target program!

**Q**: Help, how do I pass arguments to the program I want to debug? 

**A**: Use the `Debug -> Change Command Line` option:

![command line](http://i.imgur.com/Sh0PQnz.png)

***

**Q**: Building x64dbg is complicated, help me out!

**A**: A guide to building x64dbg is available [here](https://github.com/x64dbg/x64dbg/wiki/Compiling-the-whole-project). Notice that you **do not have to build all the dependencies for yourself!** Just follow the guide and use the compiled dependencies from the [latest snapshot](http://snapshots.x64dbg.com).

***

**Q**: How do I contribute?

**A**: You can check out [this](https://github.com/x64dbg/x64dbg/wiki/Contributing) dedicated page for more information on how to contribute.

***

**Q**: How do the commands mentioned in the [help](http://help.x64dbg.com) work?

**A**: Basically the commands work like assembler (with comma separated arguments). `mov eax, 0x1234` is a valid command. You can enter them in the command bar (not in the command line of x64dbg):

![command bar](http://i.imgur.com/plSfLnr.png)

***

**Q**: Does x64dbg make entries in registry or create files in system directories? Or it's portable (like OllyDbg)?

**A**: Unlike OllyDbg, x64dbg is fully portable (all paths are relative to the x64dbg executables and in Olly you have absolute plugin and UDD paths). This means you can copy you x64dbg.ini anywhere without having to change anything.  
Per default x64dbg will not create any registry entries. However if you use it as a JIT debugger it will change that key. Same applies for x96dbg.exe *(that creates a `Debug with x64dbg` entry in file explorer context menu)*.

***

**Q**: How do I remove the `Debug with x64dbg` entries from my context menu?

**A**: Download & execute [this](https://raw.githubusercontent.com/x64dbg/x64dbg/development/bin/x64dbg_shell_remove.reg) regfile (remember to `Save as...`).