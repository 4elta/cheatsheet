# responder

MitM credential harvester

## capture password hashes on a Windows network

* listen on a specific interface (`I`)

```
sudo responder -I <iface>
```

* send an email to all members of the network, containing links to an SMB share (e.g. `\\nessuno\pwn`) and/or HTTP file (e.g. `http://nessuno/pwn`)
* for [cracking](#john), use the whole hash (e.g. `<user>::<host>:<challenge>:<NTv2>`) 

## [...](https://github.com/lgandx/Responder)
