# Immunity Debugger (W)

debugger with a Python API

## find the address of a desired instruction (to overwrite EIP with)

### 1. find suitable modules to look for instructions

```
!mona modules
```

* the address of the desired instruction must not contain any "bad" bytes (*Base*, *Top*)
* the module must always reside at the same location (*Rebase: False*)
* ASLR must be disabled (*ASLR: False*)
* DEP should be disabled (*NXCompat: False*)

### 2. select a suitable module

1. press `alt+E`
2. double-click the chosen module

### 3. search for the desired instruction

1. press `ctrl+F`
2. input the instruction
  
in case the instruction wasn't found and DEP is disabled: 

```
!mona find -s "<opcode>" -m <module name>
```


