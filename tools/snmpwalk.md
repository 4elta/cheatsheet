# snmpwalk

retrieve a subtree of management values using SNMP (simple network management protocol)

## retrieve all information

* use `public` as the community string (`c`)
* use version 1 of SNMP (`v`)

```
snmpwalk -c public -v 1 <host>
```

## retrieve a specified subtree (i.e. system information)

```
snmpwalk -c <community> -v 1 <host> 1.3.6.1.2.1.1
```

## [...](http://www.net-snmp.org/docs/man/snmpwalk.html)
