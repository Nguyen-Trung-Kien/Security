---
description: >-
  CircleCI is a continuous integration and continuous delivery platform that can
  be used to implement DevOps practices.
---

# CircleCI Apikey



## Detect

```
Circle-Token: YOUR_CIRCLECI_TOKEN
```

## Search

```
Circle-Token
```

## Exploit

### Get projects

```
curl -H "Circle-Token: YOUR_CIRCLECI_TOKEN" \
     "https://circleci.com/api/v2/projects"
```

### Get Details Pipeline

```
curl -H "Circle-Token: YOUR_CIRCLECI_TOKEN" \
     "https://circleci.com/api/v2/pipeline/{pipeline-id}"
```

### Get Jobs list workflows

```
curl -H "Circle-Token: YOUR_CIRCLECI_TOKEN" \
     "https://circleci.com/api/v2/pipeline/{pipeline-id}/workflow"
```
