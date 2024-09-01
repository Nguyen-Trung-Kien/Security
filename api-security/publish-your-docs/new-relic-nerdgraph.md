# New Relic NerdGraph

## Search

```
api.newrelic.com/graphql AND API-Key 
```

## Exploit

```
POST https://api.newrelic.com/graphql
Content-Type: application/json
API-Key: "{{token}}"
body: "{ \"query\":  \"{ requestContext { userId apiKey }}\" }"
```
