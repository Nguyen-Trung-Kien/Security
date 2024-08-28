---
description: >-
  Semaphore is a hosted continuous integration and deployment service used for
  testing and deploying software projects hosted on GitHub and BitBucket.
---

# Semaphore



## Search

```
app.semaphoreci.com/api/v1 AND Authorization
```

## Exploit

### Get projects

```
curl -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     "https://app.semaphoreci.com/api/v1/projects"

```

### Get pipeline

```
curl -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     "https://app.semaphoreci.com/api/v1/projects/your_project_id/pipelines"

```

### Get users

```
curl -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     "https://app.semaphoreci.com/api/v1/users"

```
