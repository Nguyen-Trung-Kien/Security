---
description: >-
  Bitlinks are shortened links. They could begin with the bit.ly domain or your
  own custom branded short domain (BSD).
---

# Bitly



## Search

```
api-ssl.bitly.com
```

## Exploit

Get users

```
GET /v4/user HTTP/2
Host: api-ssl.bitly.com
Authorization: Bearer {{token}}
```

Create short link

```
POST /v4/shorten HTTP/2
Host: api-ssl.bitly.com
Content-Type: application/json
Authorization: Bearer {{token}}

{ 
 "long_url": "https://dev.bitly.com", 
 "domain": "bit.ly",
 "group_guid": "Ba1bc23dE4F" 
 }
```
