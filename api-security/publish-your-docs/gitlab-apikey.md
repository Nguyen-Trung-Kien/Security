---
description: >-
  GitLab is an Open Source code repository and collaborative software
  development platform for large DevOps and DevSecOps projects
---

# Gitlab apikey

## Search

#### Gitlab regex

```
\b((?:ghu|ghs)_[a-zA-Z0-9]{36})\b

/\b(gho_[a-zA-Z0-9]{36})\b/

\b(ghp_[a-zA-Z0-9]{36})\b

\b(ghr_[a-zA-Z0-9]{76})\b

\b(glpat-[0-9a-zA-Z_-]{20})(?:\b|$)
```

## Exploit

### Get list projects

```
curl --header "PRIVATE-TOKEN: {token}" "https://gitlab.com/api/v4/projects"
```

### Get user

```
curl --header "PRIVATE-TOKEN: {token}" "https://gitlab.com/api/v4/user"
```
