---
description: >-
  Crawls arbitrary websites using the Chrome browser and extracts data from
  pages using JavaScript code
---

# Apify

Search

```
api.apify.com AND /apify_api_/
```

## Exploit

get actor

```
GET /v2/acts HTTP/2
Host: api.apify.com
Authorization: Bearer apify_api_[id]
Accept-Encoding: gzip, deflate
Accept: */*
Accept-Language: en-US;q=0.9,en;q=0.8
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/114.0.5735.199 Safari/537.36
Cache-Control: max-age=0


```

get users

```
GET /v2/users/me HTTP/2
Host: api.apify.com
Authorization: Bearer apify_api_IyxytYGIfOEpJfylFJkPxNaETpzRvF1eUqX0
Accept-Encoding: gzip, deflate
Accept: */*
Accept-Language: en-US;q=0.9,en;q=0.8
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/114.0.5735.199 Safari/537.36
Cache-Control: max-age=0


```
