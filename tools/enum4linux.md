# enum4linux

enumerate data from Windows and Samba hosts

## enumerate users

* get detailed list of users (`d`)
* enumerate group and member list (`G`)
* enumerate users via RID cycling (`r`)

```
enum4linux -U -d -G -r <host>
```

## all simple enumerations

* authenticate via the specified username and password

```
enum4linux -a -u <username> -p <password> <host>
```

## [...](https://labs.portcullis.co.uk/tools/enum4linux/)
