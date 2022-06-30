# buffer overflow

## 0. provoke a crash

* use [SPIKE](https://resources.infosecinstitute.com/topic/intro-to-fuzzing/), a fuzzer creation kit
* https://boofuzz.readthedocs.io/en/stable/index.html
* https://zeroaptitude.com/zerodetail/fuzzing-with-boofuzz/
* https://medium.com/@Z3R0th/a-simple-buffer-overflow-using-vulnserver-86b011eb673b

## 1. find the offset from the start of the input to where the instruction pointer resides

create a unique pattern to overflow the buffer:

```
$ msf-pattern_create -l <length>
Aa0Aa1Aa2Aa3Aa4Aa5Aa6Aa7...
```

the value of the instruction pointer at the time of overflow can then be used to determine the (exact) offset:

```
$ msf-pattern_offset -l <length> -q <value of EIP>
[*] Exact match at offset <number>
```

## 2. identify bytes that cannot be included in the payload

if the vulnerability we are going to exploit is based on string copy/manipulation functions we cannot use the null byte (i.e. `0x00`) as it acts as a terminator for these functions.
in web applications, `0x0d` (i.e. `\r` ) followed by `0x0a` (i.e. `\n` ) delimit messages from each other.

to identiy additional bytes that must not be included, just send them all (one by one).
make sure that the process crashes!
inspect the stack and look for bytes missing or any other irregularities in the sequence.
repeat the process after you excluded bytes.

## 3. redirect execution to the shellcode

assumption: 

1. EAX points to the beginning of the buffer
2. buffer starts with *x* (e.g. less than 16) bytes we cannot control
3. ESP points almost to the end of the buffer (i.e. too little space for any shellcode)

instructions for getting EIP to point to our shellcode:

1. `JMP ESP`
2. `ADD EAX,16`
3. `JMP EAX`

get opcode for these instructions:

```
$ msf-nasm_shell
nasm > jmp esp
00000000  FFE4              jmp esp
nasm > add eax,16
00000000  83C010            add eax,byte +0x10
nasm > jmp eax
00000000  FFE0              jmp eax
```

solution:

1. find the address of a `JMP ESP` instruction:
    * [Windows: Immunity Debugger](/tools/#immunity-debugger-w)
    * [Linux: edb](/tools/#edb)
2. overwrite EIP with that address
3. write `0x83c010ffe0` to where ESP points to (i.e. almost at the end of the buffer)
