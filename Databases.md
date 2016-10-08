The databases produced by x64dbg are (lz4 compressed) JSON files. **This format can change, see [DbSave](https://github.com/x64dbg/x64dbg/blob/development/src/dbg/database.cpp#L38) for the code producing these databases.**

```python
{
 "functions": [
  {
   "manual": false, # created by a computer
   "end": "0xC1B59", //function end (relative to the base of 'module')
   "module": "ntdll.dll", //module the function is in
   "start": "0xC1A80", //function start (relative to the base of 'module')
   "icount": "0x2C" //optional, number of instructions in the function
  }
 ],
 "comments": [
  {
   "manual": true, //created by the user
   "module": "ntdll.dll", //module the comment is in
   "text": "ThreadHandle = GetCurrentThread()", //comment text
   "address": "0xC1B79" //comment address (relative to the base of 'module')
  }
 ],
 "labels": [
  {
   "manual": true, //created by the user
   "module": "ntdll.dll", //module the label is in
   "text": "DoBreakProcess", //label text
   "address": "0xC1B60" //label address (relative to the base of 'module')
  }
 ],
 "bookmarks": [
  {
   "manual": true, //created by the user
   "module": "ntdll.dll", //module the bookmark is in
   "address": "0xC1AC6" //bookmark address (relative to the base of 'module')
  }
 ],
 "breakpoints": [
  {
   "address": "0x1FB0", //breakpoint address (relative to the base of 'module')
   "commandText": "", //command to execute on hit
   "enabled": true, //breakpoint is enabled
   "fastResume": false, //fast resume is disabled
   "oldbytes": "0x5340", //original bytes at the breakpoint location
   "type": 0, //BPSOFTWARE (see https://github.com/x64dbg/x64dbg/blob/development/src/dbg/breakpoint.h#L13)
   "module": "x64dbg.exe", //breakpoint module
   "titantype": "0x0", //creation flags (see https://github.com/x64dbg/x64dbg/blob/development/src/dbg/breakpoint.h#L6)
   "name": "", //breakpoint name
   "breakCondition": "", //break condition
   "logText": "", //log text
   "logCondition": "", //log condition
   "silent": false, //silent breakpoint
   "commandCondition": "" //command condition
  }
 ]
}
```