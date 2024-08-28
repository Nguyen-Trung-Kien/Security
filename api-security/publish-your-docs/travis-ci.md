---
description: >-
  Travis CI is a hosted, distributed continuous integration service used to
  build and test software projects hosted at GitHub and Bitbucket. Travis CI is
  configured by adding a file named `. travis. yml
---

# Travis CI



## Search

```
api.travis-ci.com
```

## Exploit

### Get repos

```
curl -H "Authorization: token YOUR_TRAVIS_TOKEN" \
     https://api.travis-ci.com/repos
```

### Get list build

```
curl -H "Authorization: token YOUR_TRAVIS_TOKEN" \
     https://api.travis-ci.com/repos/owner/repo/builds
```

###
