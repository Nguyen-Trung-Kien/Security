---
description: >-
  Azure API Management is a hybrid, multicloud management platform for APIs
  across all environments. As a platform-as-a-service, API Management supports
  the complete API lifecycle.
---

# Azure - APIM

## Search

```
Ocp-Apim-Subscription-Key AND azure-api.net NOT /"query": "subscription-key"/
```

## Exploit

```
https://{host}.azure-api.net/{api-path}/
Ocp-Apim-Subscription-Key: key
```
