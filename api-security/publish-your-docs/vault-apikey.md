---
description: HashiCorp Vault is an identity-based secrets and encryption management system
---

# Vault Apikey

## Search

```
X-Vault-Token AND /https?:\/\/[^\/\s]+\.*\.com/ AND ( /hvs.*/ OR /hvb.*/ OR /hvr.*/ )
```

## Exploit

```
curl -H "X-Vault-Requests: true" -H "X-Vault-Token: " https://domain/v1/sys/mounts | jq
```
