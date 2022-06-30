# curl

non-interactively transfer data from or to a server (e.g. FTP, HTTP, SMB, etc.)

## post form-encoded data

```
curl -d user=alice -d password=secret <URL>
```

## post JSON data

```
curl -d @/path/to/data.json -H "Content-Type: application/json" <URL>
```

## include sent/received HTTP headers in the output

```
curl -v <URL>
```

## proxy through Burp/ZAP

* do not verify the server's (X.509) certificate (`k`)

```
curl -x localhost:8080 -k <URL>
```

## connect through a UNIX domain socket

```
curl --unix-socket /var/run/docker.sock http://localhost/containers/json
```

## [...](https://curl.haxx.se/docs/manpage.html)
