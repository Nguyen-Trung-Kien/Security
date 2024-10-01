---
description: >-
  Salesforce is the world's most trusted customer relationship management (CRM)
  platform.
---

# Salesforce

## Search

```
client_secret AND client_id
```

## Exploit

```
curl https://login.salesforce.com/services/oauth2/token -d 'grant_type=password&client_id=ID&client_secret=SECRET&username=USER&password=PASSWORD' -H "X-PrettyPrint: 1"
```

```
POST /services/oauth2/token HTTP/1.1
Host: login.salesforce.com
Accept-Encoding: gzip, deflate
Accept: */*
Accept-Language: en-US;q=0.9,en;q=0.8
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/114.0.5735.199 Safari/537.36
Connection: close
Cache-Control: max-age=0
X-PrettyPrint: 1
Content-Type: application/x-www-form-urlencoded
Content-Length: 280

grant_type=password&client_id=&client_secret=&username=m&password=
```
