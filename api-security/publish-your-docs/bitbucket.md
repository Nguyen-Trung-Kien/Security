---
description: Bitbucket Pipelines provides a built-in CI/CD solution within Bitbucket.
---

# Bitbucket

## Search

```
api.bitbucket.org/2.0 AND Authorization
```

## Exploit

### Get all repos

```
GET /2.0/repositories/{space} HTTP/2
Host: api.bitbucket.org
Authorization: Basic 
Accept-Encoding: gzip, deflate
Accept: */*
Accept-Language: en-US;q=0.9,en;q=0.8
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/114.0.5735.199 Safari/537.36
Cache-Control: max-age=0
```

### Get user information

```
curl -u username:app_password \
     "https://api.bitbucket.org/2.0/user"
```
