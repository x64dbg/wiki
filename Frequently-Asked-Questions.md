This section contains questions frequently encountered about x64dbg. Feel free to add your own answers to not-so-obvious things.

***

**Q**: How do I remove the `Debug with x64dbg` entries from my context menu?

**A**: Download & execute [this](https://raw.githubusercontent.com/x64dbg/x64dbg/master/x64dbg_shell_remove.reg) regfile (remember to `Save as...`).

***

**Q**: Help, I cannot change the command line of a target program!

**A**: Use the `Debug -> Change Command Line` option:

![command line](http://i.imgur.com/Sh0PQnz.png)

***

**Q**: Building x64dbg is complicated, help me out!

**A**: A guide to building x64dbg is available [here](https://github.com/x64dbg/x64dbg/wiki/Compiling-the-whole-project). Notice that you **do not have to build all the dependencies for yourself!** Just follow the guide and use the compiled dependencies from the [latest snapshot](http://snapshots.x64dbg.com).

***

**Q**: How do I contribute?

**A**: You can check out [this](https://github.com/x64dbg/x64dbg/wiki/How-to-contribute%3F) dedicated page for more information on how to contribute.

***

**Q**: How do the commands mentioned in the [help](http://help.x64dbg.com) work?

**A**: Basically the commands work like assembler (with comma separated arguments). `mov eax, 0x1234` is a valid command. You can enter them in the command bar (not in the command line of x64dbg):

![command bar](http://i.imgur.com/plSfLnr.png)