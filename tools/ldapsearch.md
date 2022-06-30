# ldapsearch

perform a search on an LDAP server (see [Get-ADObject](#get-adobject-w))

## list all objects in the directory tree

* use simple (`x`) anonymous authentication (no username/password)
* specify the search base (`b`)

```
ldapsearch -x -H ldap://<example>.<local> -b 'dc=<example>,dc=<local>' 'objectclass=*'
```

## list all users which have logged in at least once

```
ldapsearch -x -H ldap://<host> -b <search base> '(&(objectclass=user)(!(objectclass=computer))(lastLogon>=1))'
```

## show only specific attributes of an object

```
ldapsearch -x -H ldap://<host> -b <search base> <filter> <attr1> <attr2>
```

## authenticate as the specified user

```
ldapsearch -x -H ldap://<host> -b <search base> -D <username>@<host> -w <password> <filter>
```

## [...](https://www.openldap.org/software/man.cgi?query=ldapsearch)
