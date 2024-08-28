---
description: >-
  An open-source container image registry that provides image management,
  security scanning, and access control.
---

# Harbor



## Search



## Exploit

Login and Get access token

```
POST https://your-harbor-server/api/v2.0/oidc/token
Content-Type: application/x-www-form-urlencoded

grant_type=password&username=<username>&password=<password>

curl -X POST -H "Content-Type: application/x-www-form-urlencoded" -d "grant_type=password&username=YOUR_USERNAME&password=YOUR_PASSWORD" "https://your-harbor-server/api/v2.0/oidc/token"

```

return is

```
{
  "access_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxMjM0NTY3ODkwIiwibmFtZSI6Ikpva...",
  "token_type": "bearer",
  "expires_in": 3600
}

```

Get list projects

```
curl -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     "https://your-harbor-server/api/v2.0/projects"

```

Get details projects

```
curl -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     "https://your-harbor-server/api/v2.0/projects/1"

```

Get list repos

```
curl -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     "https://your-harbor-server/api/v2.0/projects/1/repositories"

```

