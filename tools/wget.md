# wget

non-interactive network retriever

## download a single file

```
wget <URL>
```

on windows add `-outfile <filename>`

## download and execute a script

* write to STDOUT (`-O -`) and pipe it to `bash`

```
wget -O - <URL> | bash
```

## download all files from a FTP server which allows anonymous access

```
wget -r ftp://<host>/
```

## download all files under a specified directory

* don't ascend to the parent directory (`np`)
* don't download auto-generated `index.html` files (`R`)

```
wget -r -np -R "index.html" <URL>
```

## [...](https://www.gnu.org/software/wget/manual/wget.html)
