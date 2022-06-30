# findstr (W)

locate files containing a specific string of plain text

## search for files containing the word `password`

* search in the current directory and all subdirectories (`s`)
* skip files with non-printable chars (`p`)
* ignore case distinctions (`i`)
* prefix each line of output with the line number (`n`)

```
findstr /spin "password" *.txt
```

## print all non-comment lines

```
findstr /vn "#" <file>
```

## [...](https://www.computerhope.com/findstr.htm)
