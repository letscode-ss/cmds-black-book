#CCC (Cool Curl Cmds)

# Run curl with temp host entry
```
curl -k -HHost:hosturl --resolve hostname:port:ipaddress https://hostname:<port>/uri
```

# Run telnet with curl
```
timeout 3s curl -v telnet://<host>:<port>
```
