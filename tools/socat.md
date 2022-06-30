# socat

establish two bidirectional byte streams and transfers data between them

## TCP port forwarder

* forward connections to *listening port* on the local host to *host:port* (can be a docker container, etc.)

```
socat TCP-LISTEN:<listening port>,fork TCP:<host>:<port>
```

## [...](http://www.dest-unreach.org/socat/doc/socat.html)
