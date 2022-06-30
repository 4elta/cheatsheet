# rpcclient

tool for executing client-side MS-RPC functions

## enumerate domain users and groups

* specify the commands to be run once connected (`c`)
* authenticate via a Null Session (`N`)

```
rpcclient -c 'enumdomusers;enumdomgroups' -N <host>
```

## get a user's privileges

```
rpcclient -U <user> -c "enumprivs" <host>
```

## reset a user's password

the account used for authentication needs to have the "Reset user passwords and force password change at next logon" permission (see [malicious.link](https://malicious.link/post/2017/reset-ad-user-password-with-linux/))

```
rpcclient -c 'setuserinfo2 <username> 23 <password>' -U <support> <host>
```

## [...](https://www.samba.org/samba/docs/current/man-html/rpcclient.1.html)
