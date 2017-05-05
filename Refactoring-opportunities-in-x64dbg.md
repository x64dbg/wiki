This is just a list of things that could be improved in the code. Feel free to add something if you find anything.
# GUI
- Menu shortcut system (Configuration.cpp contains duplicate descriptions for actions made with `makeShortcutAction`)
- Refactor common menu entries for rapid feature deployment in new views
- Convert everything to `MenuBuilder`
# DBG
- Clean up `debugger.cpp` and `debugger.h`. This file currently serves multiple purposes.
- Move the database and dbghelp to a separate component.
# YzDbg
- Supports ODBGScript
- Supports memory breakpoints
- Supports memory watching similar to CheatEngine
- Includes instruction emulator
- Shows modified memory of current dump (possible with shadow buffer)
- Supports mode of operation that doesn't attach but uses process manipulation APIs
- info box shows mnemonic brief in cn.
- disassembly preview support dump
- can drag the registers view to scroll
- does not support ymm register
- support "dd" command which dumps the data and set dump mode to dword.
- support timeout in disassembly preview