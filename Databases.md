```json
{
 "functions": [
  {
   "manual": false,
   "end": "0xC1B59",
   "module": "ntdll.dll",
   "start": "0xC1A80",
   "icount": "0x2C"
  },
  {
   "manual": false,
   "end": "0xC1B97",
   "module": "ntdll.dll",
   "start": "0xC1B60",
   "icount": "0xF"
  }
 ],
 "comments": [
  {
   "manual": true,
   "module": "ntdll.dll",
   "text": "ThreadHandle = GetCurrentThread()",
   "address": "0xC1B79"
  },
  {
   "manual": true,
   "module": "ntdll.dll",
   "text": "ThreadInformation",
   "address": "0xC1B70"
  },
  {
   "manual": true,
   "module": "ntdll.dll",
   "text": "ThreadInformationClass = 0x11 (ThreadHideFromDebugger)",
   "address": "0xC1B75"
  },
  {
   "manual": true,
   "module": "ntdll.dll",
   "text": "ThreadInformationLength",
   "address": "0xC1B6A"
  }
 ],
 "labels": [
  {
   "manual": true,
   "module": "ntdll.dll",
   "text": "DoBreakProcess",
   "address": "0xC1B60"
  }
 ],
 "arguments": [
  {
   "manual": true,
   "end": "0xC1B84",
   "module": "ntdll.dll",
   "start": "0xC1B6A",
   "icount": "0x0"
  }
 ],
 "bookmarks": [
  {
   "manual": true,
   "module": "ntdll.dll",
   "address": "0xC1AC6"
  },
  {
   "manual": true,
   "module": "ntdll.dll",
   "address": "0xC1BA0"
  }
 ],
 "breakpoints": [
  {
   "address": "0xC1B97",
   "commandText": "",
   "enabled": true,
   "fastResume": false,
   "oldbytes": "0xCCC3",
   "type": 0,
   "module": "ntdll.dll",
   "titantype": "0x0",
   "name": "",
   "breakCondition": "",
   "logText": "",
   "logCondition": "",
   "silent": false,
   "commandCondition": ""
  },
  {
   "address": "0x1FB0",
   "commandText": "",
   "enabled": true,
   "fastResume": false,
   "oldbytes": "0x5340",
   "type": 0,
   "module": "x64dbg.exe",
   "titantype": "0x0",
   "name": "",
   "breakCondition": "",
   "logText": "",
   "logCondition": "",
   "silent": false,
   "commandCondition": ""
  },
  {
   "address": "0x1300",
   "commandText": "",
   "enabled": true,
   "type": 1,
   "module": "x64dbg.exe",
   "titantype": "0xB47",
   "name": "",
   "breakCondition": "",
   "logText": "",
   "logCondition": "",
   "silent": false,
   "commandCondition": "",
   "fastResume": false
  }
 ]
}
```