# smbclient

client to access SMB/CIFS resources

## list services/shares (anonymous access)

* don't ask for password (`N`)

```
smbclient -L <host> -N
```

## list services/shares (authenticated)

```
smbclient -L <host> -U <user> //<NetBIOS name>
```

## upload files

* specify host if it is different from the NetBIOS name (`I`)

```
smbclient -I <host> -W <workgroup> -U <user> -c 'put <file>' //<NetBIOS name>/<share>/<path> <password>
```

## download complete directories

```
smbclient -I <host> -W <workgroup> -U <user> -c 'tarmode FULL; recurse ON; prompt OFF; mget ./' //<NetBIOS name>/<share>/<path> <password>
```

## [...](https://www.samba.org/samba/docs/current/man-html/smbclient.1.html)
