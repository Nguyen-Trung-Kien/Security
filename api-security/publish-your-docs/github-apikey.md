---
description: >-
  GitHub is an online software development platform. It's used for storing,
  tracking, and collaborating on software projects
---

# Github apikey

## Search

#### Github regex

```
/^ghp_[a-zA-Z0-9]{36}$/
```

## Exploit

### Get list repos

```
CURL requests
curl -H "Authorization: token <your_github_token>" https://api.github.com/user/repos
```

### Check users

```
curl -H "Authorization: token <your_github_token>" https://api.github.com/user
```

### Read Contents

```
curl -H "Authorization: token <your_github_token>" https://api.github.com/repos/owner/:repo/git/trees/main?recursive=1
```
