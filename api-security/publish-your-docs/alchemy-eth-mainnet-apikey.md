---
description: use for create block
---

# Alchemy - eth-mainnet - apikey



## Search

### Github

```
eth-mainnet.alchemyapi.io AND apikey
```

## Exploit

```
POST /v2/apikey HTTP/2
Host: eth-mainnet.alchemyapi.io
Accept-Encoding: gzip, deflate
Accept: */*
Accept-Language: en-US;q=0.9,en;q=0.8
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/114.0.5735.199 Safari/537.36
Cache-Control: max-age=0
Content-Type: application/x-www-form-urlencoded
Content-Length: 63

{"jsonrpc":"2.0","method":"eth_blockNumber","params":[],"id":0}
```

{% embed url="https://docs.alchemy.com/reference/ethereum-api-faq" %}
