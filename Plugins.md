# You can suggest an edit in the [x64dbg/wiki](https://github.com/x64dbg/wiki) repository.

## Official Templates

- [PluginTemplate](https://github.com/x64dbg/PluginTemplate): Visual Studio template to easily develop plugins.
- [QtPlugin](https://github.com/x64dbg/QtPlugin): Demonstrates how to write a plugin that adds a `QWidget` tab.

## Debugging

To make it easier to debug plugins you can use the [PluginDevHelper](https://github.com/x64dbg/PluginDevHelper) to automatically reload the plugin when you build it in Visual Studio. The CMake `PluginTemplate` automatically detects `PluginDevBuildTool.exe` and sets this up for you, but you can also set it up manually by following the instructions in the README.

## Example plugins

Plugins with minimal functionality to show how certain APIs can be used.

- https://github.com/mrexodia/StackContains
- https://github.com/mrexodia/TimeStampFormat
- https://github.com/mrexodia/PasteFile
- https://github.com/mrexodia/JNIEnv
- https://github.com/mrexodia/regstep
- https://github.com/mrexodia/BreakpointUnresolved
- https://github.com/mrexodia/ClickCatcher
- https://github.com/mrexodia/Diff
- https://github.com/mrexodia/LogString
- https://github.com/mrexodia/ExtendDumpSel
- https://github.com/mrexodia/ModulePathList
- https://github.com/mrexodia/TracePlugin
- https://github.com/mrexodia/FloatConvert
- https://github.com/mrexodia/DrDecode
- [C# plugin examples](https://github.com/x64dbg/DotX64Dbg/tree/master/bin/dotplugins/example)

## User-maintained Templates

- [Borland C++](https://github.com/ThunderCls/x64dbgBccPlugin) by [ThunderCls](https://github.com/ThunderCls).
- [C#](https://github.com/mrexodia/DotNetPluginCS) by [adams85](https://github.com/adams85).
- [VB.NET](https://github.com/Ahmadmansoor/x64dbgDotNetPlugin) by [Ahmadmansoor](https://github.com/Ahmadmansoor).
- Assembler [x86](https://github.com/mrfearless/x64dbg-Plugin-SDK-for-x86-Assembler) and [x64](https://github.com/mrfearless/x64dbg-Plugin-SDK-For-x64-Assembler) by [fearless](https://www.letthelight.in).
- [Visual Studio](https://github.com/mrfearless/x64dbg-plugin-template-for-Visual-Studio) by [fearless](https://www.letthelight.in).
- [Delphi](https://github.com/quygia128/x64_dbg_SDK_Delphi) by [quygia128](https://github.com/quygia128).
- [Rust crate](https://lib.rs/crates/x64dbg_sdk_sys) by [luyikk](https://github.com/luyikk), example plugin: [x64dbg_xpause_example](https://github.com/luyikk/x64dbg_xpause_example).

## Integrations

- [x64dbgida](https://github.com/x64dbg/x64dbgida) by [mrexodia](https://github.com/mrexodia): Official x64dbg plugin for IDA Pro.
- [x64dbgbinja](https://github.com/x64dbg/x64dbgbinja) by [mrexodia](https://github.com/mrexodia): Official x64dbg plugin for Binary Ninja.
- [lst2x64dbg](https://github.com/utkonos/lst2x64dbg) by [utkonos](https://github.com/utkonos): Extract labels from IDA .lst or Ghidra .csv file and export x64dbg database.
- [x64dbgcutter](https://github.com/yossizap/x64dbgcutter) by [yossizap](https://github.com/yossizap): Import and export x64dbg comments/breakpoints/labels/bookmarks in Cutter.
- [Generate PEB32 types JSON](https://gist.github.com/utkonos/7f82d27a389222352a671b2135aacb38) by Malware Utkonos.
- [execution-trace-viewer](https://github.com/teemu-l/execution-trace-viewer) by [teemu-l](https://github.com/teemu-l): Tool for viewing and analyzing execution traces.
- [JITCall](https://github.com/stevemk14ebr/RETools/tree/master/JITCall): An Olly-inspired DLL loader for x64dbg using JIT compiling instead of asm. Now you can call exports in x64dbg, without rundll32.
- [x64dbg-tracedump.py](https://github.com/mrexodia/dumpulator/blob/main/tests/x64dbg-tracedump.py) by [mrexodia](https://github.com/mrexodia): Standalone python script to convert x64dbg traces into a textual format.
- [UniPatch](https://github.com/fjlj/UniPatch): A tool to parse *.1337 files (exported from x64dbg) and patch the target x86 or x64 file. Also supports "loader mode", where the file will be patched in memory at runtime rather than modifying the file.

## Plugins

# _Check the [x64dbg-plugin](https://github.com/topics/x64dbg-plugin?o=desc&s=updated) GitHub topic for the latest plugins._
- \[[Download](https://github.com/x64dbg/ScyllaHide/releases)\] [ScyllaHide](https://github.com/x64dbg/ScyllaHide) by Aguila & cypher: Open-source user-mode Anti-Anti-Debug plugin.
- \[[Download](https://github.com/mrexodia/TitanHide/releases)\] [TitanHide](https://github.com/mrexodia/TitanHide) by [mrexodia](https://mrexodia.cf): Open-source kernel-mode Anti-Anti-Debug plugin.
- \[[Download](https://github.com/Nukem9/SwissArmyKnife/releases)\] [SwissArmyKnife](https://github.com/Nukem9/SwissArmyKnife) by [Nukem](https://github.com/Nukem9): x64dbg utility for linker map files, diff files, peid/ida signatures, and code signature generation.
- [Highlightfish](https://github.com/Insid3CodeTeam/Highlightfish) by [Insid3Code](https://github.com/Insid3CodeTeam): Plugin to customize x64dbg colors and Highlightings.
- \[[Download](https://rammichael.com/downloads/multiasm.rar)\] [Multiline Ultimate Assembler](https://github.com/m417z/Multiline-Ultimate-Assembler) by [RaMMicHaeL](https://rammichael.com): Multiline Ultimate Assembler is a multiline (and ultimate) assembler (and disassembler) plugin. It's a perfect tool for modifying and extending a compiled executable functionality, writing code caves, etc.
- [OllyMigrate](https://low-priority.appspot.com/ollymigrate) by [lowprio20](https://low-priority.appspot.com): This plugin make it possible to pass debuggee to another debugger without restarting (like VM live migration).
- [OllyDumpEx](https://low-priority.appspot.com/ollydumpex/) by [lowprio20](https://low-priority.appspot.com): Process memory dumper for x64dbg, OllyDbg and Immunity Debugger.
- [IDASkins](https://github.com/Nukem9/IDASkins) by [Nukem](https://github.com/Nukem9): Advanced skinning plugin for IDA PRO, ported to x64dbg.
- [ret-sync](https://github.com/bootleg/ret-sync) by [bootleg](https://github.com/bootleg): ret-sync is a set of plugins that helps to synchronize a debugging session (WinDbg/GDB/LLDB/OllyDbg2/x64dbg) with IDA disassembler.
- \[[Download](https://github.com/a1ext/labeless/releases)\] [labeless](https://github.com/a1ext/labeless) by [a1ext](https://github.com/a1ext): Labels/Comments synchronization between IDA PRO and dbg backend (OllyDbg1.10, OllyDbg 2.01, x64dbg), Remote memory dumping tool (including x64-bit), Python scripting tool.
- \[[Download](https://github.com/jdavidberger/chaiScriptPlugin/releases)\] [ChaiScript](https://github.com/jdavidberger/chaiScriptPlugin) by [jdavidberger](https://github.com/jdavidberger): Plugin which enables chai scripts to run inside of x64dbg.
- APISearch [x86](https://github.com/mrfearless/APISearch-Plugin-x86), [x64](https://github.com/mrfearless/APISearch-Plugin-x64) by [fearless](https://www.letthelight.in): A plugin to allow searching for API calls and/or searching online from command bar.
- AutoCmdLine [x86](https://github.com/mrfearless/AutoCmdLine-Plugin-x86) [x64](https://github.com/mrfearless/AutoCmdLine-Plugin-x64) by [fearless](https://www.letthelight.in): A plugin to remember the command line and load it up automatically (now built in x64dbg).
- APIInfo [x86](https://github.com/mrfearless/APIInfo-Plugin-x86) by [fearless](https://www.letthelight.in): A plugin to populate the comments with windows api calls.
- CodeShot [x86](https://github.com/mrfearless/CodeShot-Plugin-x86) by [fearless](https://www.letthelight.in): A plugin to capture the x64dbg screen to an image file.
- \[[Download](https://github.com/TheCrazyT/x64dbg-plugin-quickaccess/releases/)\] [QuickAccess](https://github.com/TheCrazyT/x64dbg-plugin-quickaccess) by [TheCrazyT](https://github.com/TheCrazyT): For the lazy people that can't remember all the shortcuts. Just press `Ctrl+3` and you can access any menu.
- \[[Download](https://ci.appveyor.com/project/mrexodia/x64dbg-python/build/artifacts)\] [x64dbgpy](https://github.com/x64dbg/x64dbgpy): Automating x64dbg using Python.
- \[[Download](https://github.com/torusrxxx/x64dbgpatchexporter/releases)\] [x64dbgpatchexporter](https://github.com/torusrxxx/x64dbgpatchexporter) by [torusrxxx](https://github.com/torusrxxx/): Export patches with a template.
- [xLCB](https://github.com/ThunderCls/xLCB) by [ThunderCls](https://reversec0de.wordpress.com): Plugin that mimics the function of the original LCB plugin for OllyDbg by scherzo.
- [xdbg](https://github.com/brock7/xdbg) by [brock7](https://github.com/brock7): Open-source user-mode Anti-Anti-Debug plugin for x64dbg & cheatengine.
- \[[Download](https://github.com/torusrxxx/x64dbg-xpause/releases)\] [X-Pause](https://github.com/torusrxxx/x64dbg-xpause) by [torusrxxx](https://github.com/torusrxxx): Guaranteed to pause the debuggee.
- <del>\[[Download](https://github.com/torusrxxx/ExtraInfo/releases)\] [ExtraInfo](https://github.com/torusrxxx/ExtraInfo) by [torusrxxx](https://github.com/torusrxxx): Show extra information in the info box.</del> Important: This plugin has been deprecated because it is now a core feature of x64dbg. Please use newer versions of x64dbg directly.
- [x64_tracer](https://github.com/KurapicaBS/x64_tracer) by [KurapicaBS](https://github.com/KurapicaBS): Conditional branch logger for x64dbg.
- [xHotSpots](https://github.com/ThunderCls/xHotSpots) by [ThunderCls](https://github.com/ThunderCls): This is the new plugin rewrite based on the deprecated [MagicPoints](https://github.com/ThunderCls/MagicPoints). This plugin is intended to give the user the option to access certain points of the debugged application when events addresses are calculated, thus permiting to intercept such points to stop execution right before those events are executed.
- \[[Download](https://github.com/ThunderCls/xAnalyzer/releases/)\] [xAnalyzer](https://github.com/ThunderCls/xAnalyzer) by [ThunderCls](https://github.com/ThunderCls): xAnalyzer is capable of calling internal commands of x64dbg to make all kind of analysis and also integrates one of his own. This plugin is going to make an extensive function calls analysis to add complementary information, something close at what you get with OllyDbg.
- \[[Download](https://github.com/XeroNicHS/x64dbg_AttachHelper/releases/)\] [AttachHelper](https://github.com/XeroNicHS/x64dbg_AttachHelper) by [XeroNicHS](https://www.xeronichs.com): This plugin automatically restores 'DbgBreakPoint', 'DbgUiRemoteBreakin'.
- [x64dbgpy plugin template](https://github.com/techbliss/x64dbgpy-Plugin-Template) by [Storm Shadow](https://github.com/techbliss): This plugin helps you build your python plugins for x64dbpy.
- [x64dbgpy plugin Screen recorder ](https://github.com/techbliss/Screen_Recorder_x64dbg) by [Storm Shadow](https://github.com/techbliss): Plugin for screen recording, made for x64dbgpy.
- [x64dbgpy script editor](https://github.com/techbliss/X64dbg_script_editor) by [Storm Shadow](https://github.com/techbliss): Full script editor for x64dbgpy.
- [OW Imports](https://github.com/qwerty9384/Overwatch-IAT-Deobfuscation) by qwerty9384: Label obfuscated imports for Overwatch.
- \[[Download](https://github.com/codecat/ClawSearch/releases)\] [ClawSearch](https://github.com/codecat/ClawSearch) by [Codecat](https://github.com/codecat): A memory scanner plugin for x64dbg, inspired by Cheat Engine.
- \[[Download](https://github.com/changeofpace/PE-Header-Dump-Utilities/releases)\] [PE Header Dump Utilities](https://github.com/changeofpace/PE-Header-Dump-Utilities) by [changeofpace](https://github.com/changeofpace): Adds several commands to x64dbg for dumping PE header information by address. 
- \[[Download](https://www.unknowncheats.me/forum/downloads.php?do=file&id=19286)\] [Overwatch Dump Fix](https://github.com/changeofpace/Overwatch-Dump-Fix) by [changeofpace](https://github.com/changeofpace): This plugin removes anti-dumping and obfuscation techniques from the popular FPS game Overwatch.
- \[[Download](https://github.com/x64dbg/LabelPEB/releases)\] [LabelPEB](https://github.com/x64dbg/LabelPEB) by [torusrxxx](https://github.com/torusrxxx): Add labels for fields in PEB.
- \[[Download](https://ci.appveyor.com/project/mrexodia/slothbp/build/artifacts)\] [SlothBP](https://github.com/x64dbg/SlothBP) by [blaquee](https://github.com/blaquee): Collaborative Breakpoint Manager for x64dbg.
- \[[Download](https://github.com/0ffffffffh/Api-Break-for-x64dbg/releases)\] [APIBreak](https://github.com/0ffffffffh/Api-Break-for-x64dbg) by [Oguz Kartal](https://oguzkartal.net): A x64dbg plugin to set breakpoints Win32/64 API calls visually & easly. It has both x86 and x64 bit version.
- \[[Download](https://ci.appveyor.com/project/mrexodia/system/build/artifacts)\] [system](https://github.com/x64dbg/system) by [mrexodia](https://mrexodia.cf): Plugin to execute system commands.
- \[[Download](https://github.com/changeofpace/Force-Page-Protection/releases/tag/v1.0)\] [Force Page Protection](https://github.com/changeofpace/Force-Page-Protection) by [changeofpace](https://github.com/changeofpace): This plugin sets the page protection for memory mapped views in scenarios which cause NtProtectVirtualMemory to fail.
- [cndsteroids](https://github.com/pastaCLS/cndsteroids) by [pastaCLS](https://github.com/pastaCLS): Plugin to compare strings in conditional expressions.
- \[[Download](https://github.com/x64dbg/Fuck1481/releases/download/Fuck1481/Fuck1481.zip)\] [Fuck1481](https://github.com/x64dbg/Fuck1481) by [x64dbg](https://x64dbg.com): Fixes [x64dbg#1481](https://github.com/x64dbg/x64dbg/issues/1481).
- \[[Download](https://github.com/stonedreamforest/NaiHeQiao/releases/download/2017-3-12/2017-3-12.rar)\] [NaiHeQiao](https://github.com/stonedreamforest/NaiHeQiao) by [Tennn](https://github.com/stonedreamforest): Open-source x86/x64 usermode anti-anti-debug plugin, when the built-in debugger engine has a debug signal processing failure: [x64dbg#1462](https://github.com/x64dbg/x64dbg/issues/1462).
- \[[Download](https://github.com/x64dbg/GetCharABCWidthsI_cache/releases/download/1529ac3e/GetCharABCWidthsI_cache.zip)\] [GetCharABCWidthsI_cache](https://github.com/x64dbg/GetCharABCWidthsI_cache) by [x64dbg](https://x64dbg.com): Plugin to improve performance of `QWindowsFontEngine::getGlyphBearings`.
- \[[Download](https://github.com/klks/checksec/releases/download/20170327/Checksec_v0.1.zip)\] [checksec](https://github.com/klks/checksec) by [klks](https://github.com/klks): Plugin checks modules for security features enabled such as SafeSEH/GS/DEP/ASLR/CFG.
- \[[Download](https://github.com/David-Reguera-Garcia-Dreg/DbgChild/releases)\] [DbgChild](https://github.com/David-Reguera-Garcia-Dreg/DbgChild) by [Dreg](https://github.com/David-Reguera-Garcia-Dreg): This plugin is intended to give the user the option to debug (auto-attach) the child processes created by debugee.
- \[[Download](https://github.com/levisre/TransX64Dbg/releases/download/v1/TransX64Dbg_v1.7z)\] [TransX64Dbg](https://github.com/levisre/TransX64Dbg) by [levisre](https://github.com/levisre): Small Plugin to make x64dbg Window becomes transparent.
- \[[Download](https://github.com/mrfearless/Today-Plugin-x86/blob/master/release/Today.dp32?raw=true)\] [Today-Plugin-x86](https://github.com/mrfearless/Today-Plugin-x86) by [mrfearless](https://github.com/mrfearless): An x86 plugin to lists days of interest: national, commemorative, awareness or international observance days.
- \[[Download](https://github.com/mrfearless/Today-Plugin-x64/blob/master/release/Today.dp64?raw=true)\] [Today-Plugin-x64](https://github.com/mrfearless/Today-Plugin-x64) by [mrfearless](https://github.com/mrfearless): An x64 plugin to lists days of interest: national, commemorative, awareness or international observance days.
- \[[Download](https://github.com/horsicq/nfdx64dbg/releases)\] [nfdx64dbg
](https://github.com/horsicq/nfdx64dbg) by [hors](https://github.com/horsicq): Linker/Compiler/Tool detector.
- \[[Download](https://github.com/x64dbg/strmatch/releases)\] [strmatch](https://github.com/x64dbg/strmatch) by [x64dbg](https://x64dbg.com): Simple string matching plugin for x64dbg. Supports UTF8, UTF16 and Local codepages.
- \[[Download](https://github.com/x64dbg/AutoExportPatches/releases)\] [AutoExportPatches](https://github.com/x64dbg/AutoExportPatches) by [x64dbg](https://x64dbg.com): Plugin that automatically stores patches in the database and restores them on restart.
- \[[Download](https://github.com/mrexodia/YaraGen/releases)\] [YaraGen](https://github.com/mrexodia/YaraGen) by [mrexodia](https://github.com/mrexodia): Plugin for x64dbg to generate Yara rules from function basic blocks.
- \[[Download](https://github.com/atom0s/CeAutoAsm-x64dbg/archive/master.zip)\] [CeAutoAsm](https://github.com/atom0s/CeAutoAsm-x64dbg) by [atom0s](https://github.com/atom0s): Plugin for x64dbg to use Cheat Engine auto assembler scripts from the debugger command line.
- \[[Download](https://github.com/LFriede/x64dbg-updater/releases)\]
[x64dbg-Updater](https://github.com/LFriede/x64dbg-updater) by [gORDon_vdLg](https://github.com/LFriede): Plugin which updates to new snapshot with one click and optionally checks for new snapshots on startup.
- \[[Download](https://github.com/mrfearless/CopyToAsm-Plugin-x86/blob/master/release/CopyToAsm.dp32?raw=true)\] [CopyToAsm-Plugin-x86](https://github.com/mrfearless/CopyToAsm-Plugin-x86) by [mrfearless](https://github.com/mrfearless): An x86 plugin to copy a selected disassembly range in the x64dbg cpu view tab and convert to a assembler style code and output to clipboard or the reference view tab.
- \[[Download](https://github.com/mrfearless/CopyToAsm-Plugin-x64/blob/master/release/CopyToAsm.dp64?raw=true)\] [CopyToAsm-Plugin-x64](https://github.com/mrfearless/CopyToAsm-Plugin-x64) by [mrfearless](https://github.com/mrfearless): An x64 plugin to copy a selected disassembly range in the x64dbg cpu view tab and convert to a assembler style code and output to clipboard or the reference view tab.
- \[[Download](https://github.com/x64dbg/DbGit/releases/download/v0.1/DbGit_86828fb1.zip)\]
[DbGit](https://github.com/x64dbg/DbGit) by [mrexodia](https://github.com/mrexodia): Simple plugin to automatically add x64dbg databases to version control.
- \[[Download](https://github.com/Vicshann/GhostDbg/releases)\]
[GhostDbg](https://github.com/Vicshann/GhostDbg) by [Vicshann](https://github.com/Vicshann): Noninvasive debugging plugin for x64dbg.
- [EasyLabelView](https://github.com/phiDelPark/x64DbgPlugins) by phiDel: Show bookmarks, labels, comments in the stack window.
- \[[Download](https://github.com/Ahmadmansoor/x64dbgScript.git)\] [x64dbgScript](https://github.com/Ahmadmansoor/x64dbgScript.git) by [Ahmadmansoor](https://github.com/Ahmadmansoor): a x64dbg script system support.
- \[[Download](https://github.com/secrary/idenLib/releases)\] [idenLib](https://github.com/secrary/idenLib) by [Lasha Khasaia, @qaz_qaz](https://github.com/secrary/)  : plugin to identify library functions, When analyzing malware or 3rd party software, it's challenging to identify statically linked libraries and to understand what a function from the library is doing.
- \[[Download](https://github.com/horsicq/stringsx64dbg/releases)\] [stringsx64dbg](https://github.com/horsicq/stringsx64dbg) by [hors](https://github.com/horsicq): Strings plugin. ANSI and UNICODE. RegEXP support
- \[[Download](https://github.com/horsicq/pex64dbg/releases)\] [pex64dbg](https://github.com/horsicq/pex64dbg) by [hors](https://github.com/horsicq): PE Viewer
- \[[Download](https://github.com/x64dbg/snowman/releases/latest)\] [snowman](https://github.com/x64dbg/snowman) by [x64dbg](https://x64dbg.com): Snowman decompiler plugin.
- \[[Download](https://github.com/stonedreamforest/Mirage/releases)\] [Mirage](https://github.com/stonedreamforest/Mirage) by [Tennn](https://github.com/stonedreamforest): kernel-mode Anti-Anti-Debug plugin. `based on intel vt-x && ept technology`.
- \[[Download](https://github.com/Andy53/ERC.Xdbg/releases)\] [ERC.Xdbg](https://github.com/Andy53/ERC.Xdbg) by [Andy53](https://github.com/Andy53): An X64dbg Plugin of the ERC Library. ERC is an exploit development framework similar to Mona.py.
- \[[Download](https://github.com/sicaril/BaymaxTools)\] [Baymax toOls v1.0 beta for x64dbg](https://github.com/sicaril/BaymaxTools) by [Nisy/PYG](https://www.chinapyg.com/): Extract the signature(pattern) of the selected instruction and check the number of times the signature(pattern) appears in the current search module.    
- \[[Download](https://github.com/colinsenner/rtti-plugin-x64dbg/releases)\] [RTTI Info](https://github.com/colinsenner/rtti-plugin-x64dbg) by [colinsenner](https://www.colinsenner.com/blog): Displays detailed run-time type information if available by selecting an object address in the memory dump.
- \[[Download](https://github.com/0ffffffffh/yummyPaste/releases)\] [yummyPaste](https://github.com/0ffffffffh/yummyPaste) by [Oguz Kartal](https://oguzkartal.net): a plugin to able to paste the various type of formatted binary data into the x64dbg's disassembler or dump section.
- [ASLR-Removal](https://github.com/AandersonL/x64dbg-ASLR-Removal) by [Aandersonl](https://github.com/AandersonL): Plugin to remove the ASLR from the current file.
- \[[Download](https://github.com/morsisko/xSelectBlock/releases/)\] [xSelectBlock](https://github.com/morsisko/xSelectBlock) by [morsisko](https://github.com/morsisko): Plugin to select block of data in dump widget easier.
- \[[Download](https://github.com/morsisko/xFindOut/releases/)\] [xFindOut](https://github.com/morsisko/xFindOut) by [morsisko](https://github.com/morsisko): Plugin to find out what writes to/accesses particular address
- \[[Download](https://github.com/VenTaz/Themidie/releases/)\] [Themidie](https://github.com/VenTaz/Themidie) by [VenTaz](https://github.com/VenTaz): Plugin to bypass Themida 3.x Anti-Debugger / VM / Monitoring programs checks (x64)
- \[[Download](https://github.com/David-Reguera-Garcia-Dreg/xshellex/releases/)\] [xshellex](https://github.com/David-Reguera-Garcia-Dreg/xshellex) by [Dreg](https://github.com/David-Reguera-Garcia-Dreg/): With xshellex you can paste any kind of c-shellcode strings in x64dbg. Also you can convert clipboard "x64dbg-binary-copy" to c-shellcode string.
- \[[Download](https://github.com/nblog/Vm2Import)] [Vm2Import](https://github.com/nblog/Vm2Import) by [nblog](https://github.com/nblog): fix vmprotect import function used unicorn-engine.
- \[[Download](https://github.com/jonatan1024/CpuidSpoofer/releases/latest)] [CPUID Spoofer](https://github.com/jonatan1024/CpuidSpoofer) by [jonatan1024](https://github.com/jonatan1024): Modify the behaviour of the CPUID instruction.
- \[[Download](https://github.com/robiot/x64dbg-DiscordRPC/releases/latest)] [x64dbgRPC](https://github.com/robiot/x64dbg-DiscordRPC) by [robiot](https://github.com/robiot): Discord Rich Presence Plugin For x64dbg
- \[[Download](https://github.com/Air14/HyperHide/releases/latest)] [HyperHide](https://github.com/Air14/HyperHide) by [Air14](https://github.com/Air14): Hypervisor based anti anti debug plugin for x64dbg
- \[[Download](https://github.com/ross-weir/x64dbg_rc/releases)] [x64dbg_rc](https://github.com/ross-weir/x64dbg_rc) by [Ross Weir
](hhttps://github.com/ross-weir): Remote control plugin for x64dbg
- \[[Download](https://github.com/mooncat-greenpy/x64dbg_GolangAnalyzerPlugin/releases)] [x64dbg_GolangAnalyzerPlugin](https://github.com/mooncat-greenpy/x64dbg_GolangAnalyzerPlugin) by [mooncat-greenpy](https://github.com/mooncat-greenpy): Analyze Golang with x64dbg
- \[[Download](https://github.com/mooncat-greenpy/x64dbg_TraceExecLoggerPlugin/releases)] [x64dbg_TraceExecLoggerPlugin](https://github.com/mooncat-greenpy/x64dbg_TraceExecLoggerPlugin) by [mooncat-greenpy](https://github.com/mooncat-greenpy): TraceExecLogger saves information when debugging. Logs are stored in JSON format.
- \[[Download](https://github.com/ElvisBlue/x64dbgpython/releases)] [x64dbgpython](https://github.com/ElvisBlue/x64dbgpython) by [ElvisBlue](https://github.com/ElvisBlue): Python 3 plugin for x64dbg.
- \[[Download](https://github.com/ZehMatt/x64dbgPlaytime/releases)] [x64dbgPlaytime](https://github.com/ZehMatt/x64dbgPlaytime) by [ZehMatt](https://github.com/ZehMatt): Plugin for x64Dbg adding Lua scripting.
- \[[Download](https://github.com/x64dbg/DotX64Dbg/releases)] [DotX64Dbg](https://github.com/x64dbg/DotX64Dbg) by [ZehMatt](https://github.com/ZehMatt): x64dbg plugin that enables C# plugins with hot-loading support and scripting.
- \[[Download](https://github.com/gmh5225/X64DBG-ViewDllNotification/releases)] [X64DBG-ViewDllNotification](https://github.com/gmh5225/X64DBG-ViewDllNotification) by [gmh5225](https://github.com/gmh5225): View a a list of DLL notification callbacks (`LdrpDllNotificationList`).
- \[[Download](https://github.com/nblog/x64dbgpy3/releases/latest)] [x64dbgpy3](https://github.com/nblog/x64dbgpy3) by [nblog](https://github.com/nblog): x64dbg python3 plugin.
- \[[Download](https://github.com/m417z/x64dbg-symbol-tldr/releases/latest)\] [x64dbg-symbol-tldr](https://github.com/m417z/x64dbg-symbol-tldr) by [m417z](https://github.com/m417z): An x64dbg plugin which helps make sense of long C++ symbols.
- \[[Download](https://github.com/nblog/x64dbg-yaraScan/releases/latest)\] [x64dbg-yaraScan](https://github.com/nblog/x64dbg-yaraScan) by [nblog](https://github.com/nblog): Yara support in x64dbg.
- \[[Download](https://github.com/Internet-2-0/Malcore-x64dbg/releases/latest)\] [Malcore](https://github.com/Internet-2-0/Malcore-x64dbg) by [Malcore](https://sponsors.x64dbg.com/malcore): This x64dbg plugin allows you to upload your sample to Malcore and view the results.
- [Gx64Sync](https://github.com/diommsantos/Gx64Sync) by [diommsantos](https://github.com/diommsantos): Advanced synchronization between Ghidra and x64Dbg.
- \[[Download](https://dariushoule.github.io/x64dbg-automate-pyclient/installation/)\] [x64dbg Automate](https://dariushoule.github.io/x64dbg-automate-pyclient/) by [darbonzo](https://x64.ooo): Full featured debugger automation in Python 3.
- x64DbgMCPServer [https://github.com/AgentSmithers/x64DbgMCPServer] [x64] by [AgentSmithers](https://ControllingTheInter.net): A MCPServer bridge plugin used for AI powered automated reverse engineering.
- 
## Plugin manager

- https://github.com/horsicq/x64dbg-Plugin-Manager

## Other tools

- https://github.com/chausner/1337patch
- [x64dbgpylib](https://github.com/x64dbg/x64dbgpylib): Port of windbglib to x64dbgpy, in an effort to support mona.py in x64dbg
- \[[Download](https://github.com/therealdreg/x64dbg-exploiting/releases)] [x64dbg-exploiting](https://github.com/therealdreg/x64dbg-exploiting) by [Dreg](https://github.com/therealdreg): Package to make it easier to replace Immunity and provide explitation-related functionality (x64dbgpy, mona).
