# hydra

brute-force authentication

## HTTP Basic Authentication

* exit after the first successful login (`f`)

```
hydra -l <username> -P <passwords> -f <server> http[s]-get <path>
```

## HTTP form authentication

* try one password with each login then move to the next password (`u`)

```
hydra -L <usernames> -P <passwords> -u -f <server> http[s]-<get|post>-form '<path>:<user>=^USER^&<password>=^PASS^:<failure message>'
```

## SMBv1

```
hydra -L <usernames> -P <passwords> -u -f <server> smb
```

## get module-specific help

```
hydra -U <module>
```

## [...](https://github.com/vanhauser-thc/thc-hydra)
