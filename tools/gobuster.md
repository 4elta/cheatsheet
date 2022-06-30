# gobuster

find directories, files and virtual hosts

## brute-force subdirecories

* print full (expanded) URLs (`e`)

```
gobuster dir -u <URL> -w <wordlist> -e
```

## brute-force subdomains (i.e. virtual hosts)

```
gobuster vhost -u <URL> -w <wordlist>
```

## HTTP Basic Authentication

* skip TLS certificate verification (`k`)

```
gobuster dir -U <username> -P <password> -k -u <URL> -w <wordlist>
```

## [...](https://github.com/OJ/gobuster)
