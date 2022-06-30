# grep

**g**lobally search for a **r**egular **e**xpression and **p**rint matching lines

## search specific files for some specific strings

* supress error messages (`s`) 
* ignore case distinctions (`i`)
* recurse into directories (`r`) 
* prefix each line of output with the line number (`n`)

```
grep --include=*.{txt,cfg,conf} -sirn -e 'password' -e 'key' /
```

## show hidden input elements

* use extended regular expression (`E`)

```
grep --include=*.{html,php} -sirn -E 'type=.?hidden.?' .
```

## display only non-comment lines

```
grep '^[^#;]' <file>
```

## [...](https://www.gnu.org/software/grep/manual/grep.html)
