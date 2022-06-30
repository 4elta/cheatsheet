# objdump

display information from object files (i.e. executables)

## disassemble an executable

* intermix source code with disassembly (`S`)
* use AT&T syntax (`M`)

```
objdump -D -S -M att <executable>
```

## disassemble shellcode

* specify the target architecture (`m`)

```
objdump -D -b binary -m <i386|x64> -M att <shellcode>
```

## [...](https://linux.die.net/man/1/objdump)
