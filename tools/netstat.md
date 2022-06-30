# netstat

print network connections (see [ss](#ss)), routing tables (see [ip](#ip))

## display listening and non-listening UDP/TCP sockets

* display listening and non-listening sockets (`a`)
* include UDP sockets (`u`)
* include TCP sockets (`t`)
* do not try to resolve service names (`n`)

```
netstat -autn
```

## display the routing table

```
netstat --route
```

## [...](https://linux.die.net/man/8/netstat)
