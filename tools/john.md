# john

password cracker

## crack the specified hash file

```
john --wordlist:<wordlist> <hashes>
```

## specify the hash format

* list all supported formats: `john --list:formats`

```
john --format:<format> --wordlist:<wordlist> <hashes> 
```

## dynamically generate passwords based on rules

```
john --wordlist:<wordlist> --rules:best64 <hashes>
```

### custom rules

* use the word as is (`:`)
* append the current year (`Az"2020"`)
* capitalize the first character (`c`)

```
$ cat john-local.conf
[List.Rules:custom]
:
Az"2020"
c
cAz"2020"
```

```
john --wordlist:<wordlist> --rules:custom <hashes>
```

## additional utilities

### unshadow

```
unshadow /etc/passwd /etc/shadow > unshadowed
```

### create hash files from encrypted/password-protected files

* find transformation utilities: `locate *2john*`

```
zip2john <zip archive> > hash
```

## [...](https://www.openwall.com/john/doc/)
