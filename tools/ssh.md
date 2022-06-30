# ssh

login and/or execute commands on a (remote) system

## login as the specified user on the specified host

* specify an identity file (i.e. private key) for public key authentication (`i`)

```
ssh -i <identity> <user>@<host>
```

## execute a command at the other system

```
ssh <user>@<host> <command>
```

## proxy (i.e. SOCKS4/5) traffic through SSH

* don't execute a remote command (`N`)

```
ssh -N -D <port> <user>@<host>
```

## forward connections made to local port to the destination port on the destination host

```
ssh -N -L <local port>:<destination host>:<destination port> <user>@<host>
```

## SSH jumping

```
ssh -J <user>@<jumper> <user>@<destination>
```

## misc utilities

### generate an identity (i.e. private/public key pair)

```
ssh-keygen -f <identity>
```

### copy identity to remote system

```
ssh-copy-id <user>@<host>
```

### hidden prompt inside an SSH session

* hit enter
* input `~C` (no need to hit enter!)
* now you could configure port forwarding etc.

```
ssh> -L 9000:localhost:9000
```

## [...](https://linux.die.net/man/1/ssh)
