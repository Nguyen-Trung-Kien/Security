---
description: >-
  GoCardless is a fintech company that specialises in bank payments including
  recurring payments, Direct Debit processing and Open Banking
---

# Gocardless api

## Search

```
/api\.gocardless\.com/ AND /live_/
```

## Exploit

```
GET /customer_bank_accounts HTTP/2
Host: api.gocardless.com
Authorization: Bearer a
Gocardless-Version: 2015-07-06

```
