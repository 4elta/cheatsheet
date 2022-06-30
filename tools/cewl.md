# cewl

custom wordlist generator

## spider the specified URL

* specify max. depth (`d`)
* specify min. word length (`m`)

```
cewl -d 3 -m 5 <URL>
```

## *HTTP Basic Authentication*

* save result to a file (`w`)

```
cewl --auth_type basic --auth_user <user> --auth_pass <password> -w <result> <URL>
```

## [...](https://digi.ninja/projects/cewl.php#usage)
