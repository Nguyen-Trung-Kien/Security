---
description: >-
  SonarQube provides code quality analysis and integrates with CI/CD to manage
  code quality.
---

# SonarQube Api



## Search



## Exploit

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

