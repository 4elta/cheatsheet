# nikto

web server scanner

## scan the specified web server (at port 80)

```
nikto -h <host>
```

## scan multiple ports

```
nikto -h <host> -p 80,88,443
```

## don't scan for denial-of-service vulnerabilities

```
nikto -h <host> -T x6
```

## [...](https://cirt.net/nikto2-docs/options.html)
