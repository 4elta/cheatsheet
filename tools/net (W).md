# net (W)

manage a network from the command prompt

## list all (network) users

```
net user
```

## list all members of the *domain admins* group

```
net group "domain admins"
```

## add a new user

```
net user <username> <password> /add
```

## add a specified user to the *administrators* group

```
net localgroup administrators <username> /add
```

## add a specified user to the *remote desktop users* group

```
net localgroup "remote desktop users" <username> /add
```

## [...](https://www.computerhope.com/nethlp.htm)
