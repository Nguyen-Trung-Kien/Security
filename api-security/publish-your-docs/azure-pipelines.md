---
description: >-
  Azure Pipelines is the part of Azure DevOps that automatically builds, tests,
  and deploys code projects. Azure Pipelines combines continuous integration,
  continuous testing, and continuous delivery to
---

# Azure Pipelines

## Search

```
dev.azure.com AND Authorization
```

## Exploit

### Get user info

```
GET https://dev.azure.com/{organization}/_apis/graph/users?api-version=7.1-preview.1

curl -u :YOUR_PERSONAL_ACCESS_TOKEN \
     "https://dev.azure.com/your_organization/_apis/graph/users?api-version=7.1-preview.1"

```

### Get user info via id

```
GET https://dev.azure.com/{organization}/_apis/graph/users/{userId}?api-version=7.1-preview.1

curl -u :YOUR_PERSONAL_ACCESS_TOKEN \
     "https://dev.azure.com/your_organization/_apis/graph/users/{userId}?api-version=7.1-preview.1"


```

### Get list projects

```
GET https://dev.azure.com/{organization}/_apis/projects?api-version=7.1-preview.4


curl -u :YOUR_PERSONAL_ACCESS_TOKEN \
     "https://dev.azure.com/your_organization/_apis/projects?api-version=7.1-preview.4"

```
