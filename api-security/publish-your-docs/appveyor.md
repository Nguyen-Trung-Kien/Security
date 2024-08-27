---
description: >-
  AppVeyor is a hosted, distributed continuous integration service used to build
  and test projects hosted on GitHub and other source code hosting services on a
  Microsoft Windows virtual machine, as well
---

# AppVeyor



## Search

Github

```
// Some code
```

## Exploit

#### List projects

```
curl -X GET "https://ci.appveyor.com/api/projects" \
-H "Authorization: Bearer <YOUR_API_TOKEN>"
```

Get details a projects

```
curl -X GET "https://ci.appveyor.com/api/projects/<PROJECT_ID>" \
-H "Authorization: Bearer <YOUR_API_TOKEN>"
```

Create new projects

```
curl -X POST "https://ci.appveyor.com/api/builds" \
-H "Authorization: Bearer <YOUR_API_TOKEN>" \
-H "Content-Type: application/json" \
-d '{
  "accountName": "<YOUR_ACCOUNT_NAME>",
  "projectSlug": "<YOUR_PROJECT_SLUG>",
  "branch": "<YOUR_BRANCH_NAME>",
  "commit": "<YOUR_COMMIT_HASH>"
}'
```

Get list deployment

```
curl -X GET "https://ci.appveyor.com/api/deployments" \
-H "Authorization: Bearer <YOUR_API_TOKEN>"
```

Get all build of projects

```
curl -X GET "https://ci.appveyor.com/api/projects/<PROJECT_ID>/builds" \
-H "Authorization: Bearer <YOUR_API_TOKEN>"
```
