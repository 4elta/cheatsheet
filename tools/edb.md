# edb

cross platform AArch32/x86/x86-64 debugger

## find the address of a desired instruction (to overwrite EIP with)
 
### 1. find suitable modules to look for instructions

* use the *OpcodeSearcher* plugin: `ctrl+O`

### 2. select a suitable module

* the address of the desired instruction must not contain any "bad" bytes (*Start*, *End*)
* DEP should be disabled (*Permissions*: `r*x`)

### 3. select the *Jump Equivalent* (e.g. *ESP -> EIP*)

### 4. click *Find*

## [...](https://github.com/eteran/edb-debuggerr)
