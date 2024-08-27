---
description: >-
  Apigee is Google Cloud's native API management platform that can be used to
  build, manage, and secure APIs — for any use case, environment, or scale.
  Apigee offers high performance API proxies to crea
---

# Apigee



## Search

```
enterprise.apigee.com AND Authorization
```



## Exploit



```
https://apimonitoring.enterprise.apigee.com/alerts
Authorization: Bearer {{token}}
```

Get list api

```
curl -X GET "https://apigee.googleapis.com/v1/organizations/<YOUR_APIGEE_ORG>/apis" \
-H "Authorization: Bearer <YOUR_ACCESS_TOKEN>"
```

Create new api

```
curl -X POST "https://apigee.googleapis.com/v1/organizations/<YOUR_APIGEE_ORG>/apis" \
-H "Authorization: Bearer <YOUR_ACCESS_TOKEN>" \
-H "Content-Type: application/json" \
-d '{
  "name": "<YOUR_API_NAME>",
  "displayName": "<YOUR_API_DISPLAY_NAME>",
  "description": "<YOUR_API_DESCRIPTION>"
}'
```

Get details of api

```
curl -X GET "https://apigee.googleapis.com/v1/organizations/<YOUR_APIGEE_ORG>/apis/<YOUR_API_NAME>" \
-H "Authorization: Bearer <YOUR_ACCESS_TOKEN>"
```

Get enviroments

```
curl -X GET "https://apigee.googleapis.com/v1/organizations/<YOUR_APIGEE_ORG>/environments" \
-H "Authorization: Bearer <YOUR_ACCESS_TOKEN>"
```

