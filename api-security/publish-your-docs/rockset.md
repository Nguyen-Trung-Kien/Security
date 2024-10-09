# Rockset

Search

```
/https?:\/\/[^\/\s]+\.rockset\.com/ AND "ApiKey" AND api
```

Exploit

```
curl --request GET \
    --url https://api.rs2.usw2.rockset.com/v1/orgs/self/users/self/apikeys \
    -H 'Authorization: ApiKey
```
