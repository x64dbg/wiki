This section contains questions frequently encountered about x64dbg. Feel free to add your own answers to not-so-obvious things.

***

**Q**: Why isn't process X shown in the attach dialog?

**A**: If x64dbg cannot get a handle to a process it will not show it in the attach dialog. Go to setting and make sure the `Enable Debug Privilege` option is checked in the `Engine` tab. Also make sure you are running x64dbg as an administrator. If your process is still not shown and you are running Windows 8.1 or later, make sure the kernel is not [protecting it](http://www.alex-ionescu.com/?p=97). This protection can be removed by a kernel driver such as [PPLKiller](https://github.com/Mattiwatti/PPLKiller).

![debug priv](https://i.imgur.com/juQs94X.png)

***

**Q**: Help, I cannot change the command line of a target program!

**Q**: Help, how do I pass arguments to the program I want to debug? 

**A**: Use the `File -> Change Command Line` option:

![command line](https://i.imgur.com/bziM4hw.png)

***

**Q**: Building x64dbg is complicated, help me out!

**A**: A guide to building x64dbg is available [here](https://github.com/x64dbg/x64dbg/wiki/Compiling-the-whole-project). If you follow the steps correctly there should be no issues compiling x64dbg.

***

**Q**: How do I contribute?

**A**: You can check out [this](https://github.com/x64dbg/x64dbg/wiki/Contributing) dedicated page for more information on how to contribute.

***

**Q**: How do the commands mentioned in the [help](http://help.x64dbg.com) work?

**A**: Basically the commands work like assembler (with comma separated arguments). `mov eax, 0x1234` is a valid command. You can enter them in the command bar (not in the command line of x64dbg):

![command bar](http://i.imgur.com/plSfLnr.png)

***

**Q**: Does x64dbg make entries in registry or create files in system directories? Or it's portable (like OllyDbg)?

**A**: Unlike OllyDbg, x64dbg is fully portable (all paths are relative to the x64dbg executables and in Olly you have absolute plugin and UDD paths). This means you can copy your x64dbg.ini anywhere without having to change anything.
  
Per default x64dbg will not create any registry entries. However if you use it as a JIT debugger it will change that key. Same applies for x96dbg.exe *(that creates a `Debug with x64dbg` entry in file explorer context menu)*.

***

**Q**: How do I remove the `Debug with x64dbg` entries from my context menu?

**A**: Download & execute [this](https://raw.githubusercontent.com/x64dbg/x64dbg/development/bin/x64dbg_shell_remove.reg) regfile (remember to `Save as...`).

***

**Q**: How can I automatically attach x64dbg to a process on startup?

**A**: This can be achieved with the [Image File Execution Options](https://blog.malwarebytes.com/101/2015/12/an-introduction-to-image-file-execution-options/) registry key. You can use the [GFlags](https://github.com/x64dbg/x64dbg/issues/816) utility to do this from a graphical user interface.

***

**Q**: How can I use [PLMDebug](https://docs.microsoft.com/en-us/windows-hardware/drivers/debugger/plmdebug) with x64dbg?

**A**: Use `plmdebug /enableDebug <Package> "C:\path\to\x64dbg\release\x96dbg.exe"` (you can also use `x32dbg.exe` or `x64dbg.exe` but with `x96dbg.exe` it will automatically choose the correct architecture). See issue [#1698](https://github.com/x64dbg/x64dbg/issues/1698) for more information.

***

**Q**: Why are not all my patches being applied (`0/X patch(es) applied!` message box)?

**A**: Probably you are trying to patch in a section that has no representation on disk (`SizeOfRawData` is zero or you are patching after the end of a section). You can confirm this by checking if the address you want to patch has a file offset:

![no file offset](https://i.imgur.com/fVMYaHE.png)

***

**Q**: How can I use debug symbols in the DWARF format (MinGW `-g` option) with x64dbg?

**A**: There is no direct support for DWARF symbols in x64dbg, however you can use [cv2pdb](https://github.com/rainers/cv2pdb) to convert the DWARF symbols to PDB.

***

**Q**: I want to learn reversing, and I know how to program. Where do I start?

**A**: mrexodia recommends these links:

- http://crackmes.cf
- https://www.amazon.com/Practical-Reverse-Engineering-Reversing-Obfuscation/dp/1118787315
- https://www.amazon.com/Reversing-Secrets-Engineering-Eldad-Eilam/dp/0764574817/
- https://beginners.re/
- https://legend.octopuslabs.io/sample-page.html
- https://reversewithme.blogspot.com/2012/10/why-lena151-tutorials-wont-teach-you.html
- https://reverseengineering.stackexchange.com/questions/6801/general-consensus-on-lenas-tutorials
- http://godbolt.org
- https://lifeinhex.com/how-to-learn-reverse-engineering/
- https://gynvael.coldwind.pl/?id=664