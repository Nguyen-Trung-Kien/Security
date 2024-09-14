# Keycloak

## Search

```
// Some code
```

## Pentest map

### Check if it's keycloak

1. In source code have "keycloak" keywork
2. path /protocol/openid-connect/token/

(authen) check version

```
/auth/admin/serverinfo
```

### FUZZING Real

```
https://host.dtl/auth/realms/$master$/
```

{% embed url="https://gist.githubusercontent.com/Nguyen-Trung-Kien/0bdfa82abc5795b7b9aa2e9f8e72573a/raw/890a59bdebbc6e3942e0b7526632c853e0b49ffa/api%20wordlist.txt" %}

### Check Register enabled

```
auth/realms/<realm_name>/login-actions/registration?client_id=<same_as_the_login_page>&tab_id=<same_as_the_login_form>
```



### Port Scan

```
Somethings, keycloak start with another services
```

### Fresh fruit juices

```
standalone/configuration/mgmt-users.properties
domain/configuration/mgmt-users.properties
standalone/configuration/mgmt-groups.properties
domain/configuration/mgmt-groups.properties
```



### Requests basic

### Get token

version < Keycloak 17.0+

```
POST /auth/realms/{realms}/protocol/openid-connect/token HTTP/2
Host: host
Accept-Encoding: gzip, deflate
Accept: */*
Accept-Language: en-US;q=0.9,en;q=0.8
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/114.0.5735.199 Safari/537.36
Cache-Control: max-age=0
Content-Type: application/x-www-form-urlencoded
Content-Length: 156

grant_type=password&client_id=rns:roc:portal&client_secret=&username=&password=@&scope=openid+offline_access
```

version >= Keycloak 17.0+

```
POST /realms/{realms}/protocol/openid-connect/token HTTP/2
Host: host
Accept-Encoding: gzip, deflate
Accept: */*
Accept-Language: en-US;q=0.9,en;q=0.8
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/114.0.5735.199 Safari/537.36
Cache-Control: max-age=0
Content-Type: application/x-www-form-urlencoded
Content-Length: 156

grant_type=password&client_id=rns:roc:portal&client_secret=&username=&password=@&scope=openid+offline_access
```

#### Get user infor

```
GET /realms/roc/protocol/openid-connect/userinfo HTTP/2
Host: host
Authorization: Bearer 
Accept-Encoding: gzip, deflate
Accept: */*
Accept-Language: en-US;q=0.9,en;q=0.8
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/114.0.5735.199 Safari/537.36
Cache-Control: max-age=0


```



### GUI Access

```
https://host/admin/{realms}/console/
```
