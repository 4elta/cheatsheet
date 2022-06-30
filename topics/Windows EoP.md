# Windows EoP

## get domain admins

```
net group "domain admins"
```

only lists *users*, not other *groups*

### directory service query

```
dsquery group -name "Domain Admins" | dsget group -expand -members
```

### Get-ADGroupMember

```
Get-ADGroupMember "Domain Admins" -Recursive
```

does not show the groups

