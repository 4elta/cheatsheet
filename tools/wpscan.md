# wpscan

WordPress security scanner

## update database

```
wpscan --update
```

## enumerate vulnerable plugins/themes and users

* plain-text format (`f`) 
* save findings to a file (`o`)

vulnerable plugins/themes, timthumbs, config backups, DB exports, user IDs (1--10), media IDs (1--100)

```
wpscan -e vp,vt,u -f cli-no-color -o <findings> --url <URL>
```

## brute-force users' passwords

```
wpscan -U <usernames> -P <passwords> --url <URL>
```

## [...](https://wpscan.org/#usage)
