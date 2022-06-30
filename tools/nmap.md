# nmap

network exploration tool and port scanner

## TCP "SYN" scan

* scan all ports (`p-`)

```
sudo nmap -sS -p- <host>
```

## TCP "connect" scan

* skip host discovery
* scan HTTP-specific ports

```
nmap -sT -Pn -p 80,443,8080 <host>
```

## UDP scan

* perform version detection (`sV`)
* scan top-1000 ports

```
nmap -sU -sV --top-ports 1000 <host>
```

## detailed TCP+UDP scan

* OS detection (`O`)
* version detection (`sV`)
* run specified scripts

```
sudo nmap -sS -sU -O -sV --script default,discovery,vuln -p T:21,22,80,U:-1024
```

## [...](https://nmap.org/book/man.html)
