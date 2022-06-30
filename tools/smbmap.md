# smbmap

enumerate Samba shares

## list all directories and files

* authenticate via an empty password (`p`)

```
smbmap -R -H <host> -u anything -p ''
```

## list all drives on the specified host

```
smbmap -L -H <host> -d <domain> -u <admin> -p <password>
```

## download a file

* authenticate via LM/NTLM hash (`p`)

```
smbmap --download <path> -H <host> -u <username> -p '<LM hash>:<NTLM hash>'
```

## [...](https://github.com/ShawnDEvans/smbmap)
