---
description: >-
  Calendly is the modern scheduling platform that makes “finding time” a breeze.
  When connecting is easy, your teams can get more done
---

# Calendly APi



## Search

```
calendly.com/api/v1 AND X-Token
```

## Exploit

Get list event

```
GET /scheduled_events
Host: api.calendly.com
Authorization: Bearer YOUR_ACCESS_TOKEN

```

Get user (old version)

```
GET /sapi/v1/users/me
Host: api.calendly.com
X-TOKEN: TOKEN
```

Get user new version

```
curl --request GET \
  --url https://api.calendly.com/users/me \
  --header 'Accept: application/json' \
  --header 'Authorization: Bearer 123'
```
