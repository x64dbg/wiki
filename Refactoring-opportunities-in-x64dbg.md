This is just a list of things that could be improved in the code. Feel free to add something if you find anything.
# GUI
- Menu shortcut system (Configuration.cpp contains duplicate descriptions for actions made with `makeShortcutAction`)
- Refactor common menu entries for rapid feature deployment in new views
- Convert everything to `MenuBuilder`
# DBG
- Clean up `debugger.cpp` and `debugger.h`. This file currently serves multiple purposes.
- Move the database and dbghelp to a separate component.