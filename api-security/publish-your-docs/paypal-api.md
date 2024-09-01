# PayPal API

Search

```
sandbox.paypal.com/v1/ AND Authorization
```

## Exploit

```
https://api-m.sandbox.paypal.com/v1/identity/oauth2/userinfo?schema=paypalv1.1
Content-Type: application/json
Authorization: Bearer {{token}}
```
