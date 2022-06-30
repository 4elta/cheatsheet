# sqlmap

detect and exploit SQL injection flaws

## detect/verify vulnerability in a GET request

* specify testable parameter(s) (`p`)

```
sqlmap -u <URL incl. query parameters> -p <parameter(s)>
```

## detect/verify vulnerability in a POST request

```
sqlmap -u <URL> --data="k=v&key=value" -p <parameter(s)>
```

## list all tables

* specify the backend DB management schema (`dbms`)

```
sqlmap -u <URL> -p <parameter> --dbms=<DBMS> --tables
```

## dump specific tables of a specific database

* specify the database (`D`)
* specify the table(s) (`T`)

```
sqlmap -u <URL> -p <parameter> --dbms=<DBMS> -D <database> -T <table(s)> --dump
```

## [...](https://github.com/sqlmapproject/sqlmap/wiki/Usage)
