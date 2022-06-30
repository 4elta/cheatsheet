# mysqldump

dump MySQL/MariaDB databases

## dump database to a file

no space between `-p` and the actual password

```
db=<database>; mysqldump -u <username> -p<password> $db > $db.sql
```

## [...](https://mariadb.com/kb/en/mysqldump/)
