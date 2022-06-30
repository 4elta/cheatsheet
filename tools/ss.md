# ss

utility to investigate sockets

## display listening and non-listening UDP/TCP sockets

* display listening and non-listening sockets (`a`)
* include UDP sockets (`u`)
* include TCP sockets (`t`)
* do not try to resolve service names (`n`)

```
ss -autn
```

## display all established SSH connections

```
ss -o state established '( dport = :ssh or sport = :ssh )'
```

## [...](https://linux.die.net/man/8/ss)
