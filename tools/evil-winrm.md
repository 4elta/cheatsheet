# evil-winrm

WinRM shell for hacking

## authenticate via password

```
evil-winrm -i <host> -u <user>@<domain> -p <password>
```

## authenticate via LM/NTLM hash

```
evil-winrm -i <host> -u <user>@<domain> -H <LM/NTLM hash>
```

## file upload/download

```
> upload <local file>
> download <remote file>
```

## [...](https://github.com/Hackplayers/evil-winrm)
