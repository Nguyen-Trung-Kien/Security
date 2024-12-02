---
description: Email Services
---

# Sparkpost

### Search

```
/SPARKPOST_KEY/
```

### Exploit

```
POST /api/v1/transmissions HTTP/2
Host: api.sparkpost.com
Authorization: apikey
Accept-Encoding: gzip, deflate
Accept: */*
Accept-Language: en-US;q=0.9,en;q=0.8
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/114.0.5735.199 Safari/537.36
Cache-Control: max-age=0
Content-Type: application/json
Content-Length: 236

{
    "content": {
      "from": "email send",
      "subject": "Hello, World!",
      "text": "This is a test email sent via SparkPost API."
    },
    "recipients": [
      { "address": "email get" }
    ]
  }
```
