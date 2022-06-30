# wfuzz

web fuzzer

## find directories/files on a web server

```
wfuzz -w <wordlist> <URL>/FUZZ
```

## fuzz POST requests

* specify data, which implicates a POST request (`d`)
* specify cookie (`b`)

```
wfuzz -w <wordlist> -d "<name>=FUZZ" -b <name>=<value> <URL>
```

## fuzz HTTP verbs

```
wfuzz -w <wordlist> -X FUZZ <URL>
```

## brute-force subdomains

```
wfuzz -w <wordlist> -H "host: FUZZ.<domain>" <URL>
```

## multiple payloads

```
wfuzz -w <users> -w <passwords> -d "user=FUZZ&pass=FUZ2Z" <URL>
```

## hide specific responses

* hide responses with specified response code(s) (`hc`)
* hide responses with a specified number of chars (`hh`)

```
wfuzz -w <wordlist> --hc 404 --hh <# or chars> <URL>/FUZZ
```

## [...](https://wfuzz.readthedocs.io/en/latest/)
