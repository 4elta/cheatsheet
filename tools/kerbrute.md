# kerbrute

enumerate and brute-force Active Directory accounts

## enumerate/verify usernames

```
kerbrute userenum --dc <domain controller> -d <example>.<local> <usernames.txt>
```

## brute-force a user's password

only run this if you are sure there is no lockout policy!

```
kerbrute bruteuser --dc <domain controller> -d <domain> <passwords.txt> <username>
```

## [...](https://github.com/ropnop/kerbrute)
