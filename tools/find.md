# find

locate files based on user-specific criteria

## locate the `proof.txt` file

* show its path (`-print`)

```
find <path> -name proof.txt -print
```

## recursive directory listing

* show the files' along their attributes (`-ls`)

```
find <path> -ls
```

## find all executables modified within a specific time frame

* files modified after 2019-08-24 but before 2 weeks ago

```
find <path> -type f -executable -newermt '2019-08-24' \! -newermt '2 weeks ago' -ls
```

## execute a command on each find

```
find <path> <expression> -exec <command> {} \;
```

## [...](https://www.gnu.org/software/findutils/manual/html_mono/find.html)
