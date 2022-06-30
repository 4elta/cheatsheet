# tcpdump

dump traffic on a network

## capture traffic from/to a specific host and from a specific port

* print each packet in ASCII (`A`)

```
sudo tcpdump -A host <IP address or hostname> and dst port <port number/name>
```

## capture traffic on a specific interface

```
sudo tcpdump -i <interface>
```

## capture traffic of a specific network

* write the raw packets to a file (`w`)

```
sudo tcpdump -w <file> net <CIDR notation>
```

## read from a given dump file

```
tcpdump -r <file>
```

## [...](https://www.tcpdump.org/manpages/tcpdump.1.html)
