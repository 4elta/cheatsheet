# netsh (W)

configure and display status of various network components

## display firewall status

```
netsh advfirewall show currentprofile
```

## disable firewall

```
netsh advfirewall set currentprofile state off
```

## display firewall status (Windows XP and earlier)

```
netsh firewall show state
```

## disable firewall (Windows XP and earlier)

```
netsh firewall set opmode mode=DISABLE
```

## [...](https://www.computerhope.com/netsh.htm)
