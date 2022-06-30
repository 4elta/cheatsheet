# mysql, mariadb

simple MySQL/MariaDB shell

## connect to a specified database

no space between `-p` and the actual password

```
mysql -u <username> -p<password> <database>
```

## run non-interactively

```
mysql -u <username> -p<password> < commands.sql > results.txt
```

## navigate within mysql

* show databases: `show databases;`
* select a database: `use <database>;`
* show tables: `show tables;`
* describe a table: `describe <table>;`

## [...](https://mariadb.com/kb/en/mysql-command-line-client/)
