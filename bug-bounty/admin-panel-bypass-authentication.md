# Admin Panel Bypass Authentication

## FUZZING

Fuzzing with each language and specific wordlist

for example a page written in php is fuzzing \*.php

```
If found response 302 with large content
-> try setup match & replace with 302 to 200
```

{% embed url="https://selective-gym-948.notion.site/Admin-Panel-Pwn-6704187430914b57a924c82929232445" %}
Amazing checklist
{% endembed %}

## BLIND XSS

Try put Bxss Payload in anywhere, all input

## SQL injection

Try put Sql injection payload in login/password input

{% embed url="https://book.hacktricks.xyz/pentesting-web/login-bypass/sql-login-bypass" %}

```
https://medium.com/@medz20876/blog-post-bypassing-an-admin-panel-with-sql-injection-20b844442711
```

## Reset Password

We need do any requests and view reponses, in this case show how we need, that reponses reset password leak token, lead account takeover

{% embed url="https://assassin-marcos.medium.com/breaking-the-barrier-admin-panel-takeover-worth-3500-78da79089ca3" %}

## Read File Javascript

We should do that , find some apikey we can unauthenticated access

## Recon

Always find all information related to this domain on multiple sources.

```
- Waybackmachine
- Dork
- Urlscan
- Github, gitlab, vv
```
