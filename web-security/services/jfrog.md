---
description: >-
  The JFrog Platform gives you an end-to-end pipeline to control the flow of
  your binaries from build to production. Power your software updates to the
  edge.
---

# Jfrog



## Search

```
// Some code
```

## Default login

```
admin/password
```

## Anonymous Access

```
curl http://localhost:8081/artifactory/ui/repodata?deploy=true
or in high version
curl http://localhost:8081/artifactory/ui/api/v1/ui/repodata?deploy=true
```

CVE-2019-9733: Authentication bypass (<6.8.6) On older versions of Artifactory (up to 6.7.3) X-Forwarded-For: 127.0.0.1

{% embed url="https://www.errno.fr/artifactory/Attacking_Artifactory.html" %}
