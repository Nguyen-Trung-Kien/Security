---
description: >-
  SonarQube provides code quality analysis and integrates with CI/CD to manage
  code quality.
---

# SonarQube Api



## Search



## Exploit



```
https://sonarcloud.io/api/authentication/validate
Authorization: Basic {{base64(token + ':')}}
```

Get projects

```
curl -u YOUR_TOKEN: \
     "https://your-sonarqube-server/api/projects/search"
```

Get details projects

```
curl -u YOUR_TOKEN: \
     "https://your-sonarqube-server/api/projects/show?key=project_key_1"

```

