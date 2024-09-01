# MoonPay API

## Search

```
api.moonpay.com AND apiKey
```

## Exploit

Get list transactions

```
curl -X GET "https://api.moonpay.io/v3/transactions" \
-H "Authorization: Bearer YOUR_API_KEY"
```

Get currents user

```
curl -X GET "https://api.moonpay.io/v3/me" \
-H "Authorization: Bearer YOUR_API_KEY"
```

check

```
https://api.moonpay.com/v3/currencies/btc/buy_quote?apiKey={{token}}&baseCurrencyAmount=1
```
