---
description: >-
  The dbt Cloud API v2 contains endpoints for enqueuing runs from a job, polling
  for run progress, and downloading artifacts after jobs
---

# DTB CLoud API

## Search

```
cloud.getdbt.com/api/v2
```

## Exploit

Get users info

```
GET https://cloud.getdbt.com/api/v2/accounts/{account_id}/users/
Authorization: Bearer YOUR_API_TOKEN
```

Get list projects

```
GET https://cloud.getdbt.com/api/v2/accounts/{account_id}/projects/
Authorization: Bearer YOUR_API_TOKEN
```
