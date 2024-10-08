---
description: >-
  Dyte's API follows the REST principles. It has predictable resource-oriented
  URLs, accepts JSON-encoded request bodies, returns JSON-encoded responses, and
  uses standard HTTP response codes, authentic
---

# Dyte API

## Search

```
// Some code
```

## Exploit

create meetings

```
POST /v2/meetings HTTP/1.1
Host: api.dyte.io
Authorization: Basic []
Accept-Encoding: gzip, deflate
Accept: */*
Accept-Language: en-US;q=0.9,en;q=0.8
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/114.0.5735.199 Safari/537.36
Connection: close
Cache-Control: max-age=0
Content-Type: application/json
Content-Length: 99

{
  "title": "Sample meeting",
  "preferred_region": "ap-south-1",
  "record_on_start": false
}
```
