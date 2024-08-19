# Small Scope (lower than 10)

With a low number of domains, you need to visit each website, perform each feature, and evaluate the entire website to find vulnerabilities.

## Use website

Use the website like a normal user, to find a bug, you need to know how the website or application works, and whether a certain issue is a bug or just a feature.

## File Javascript analytics

Carefully analyze any javascript files you find (in source code or Wayback machine) anywhere on the site.

try find

* api endpoint
* username/password
* secret key
* subdomain

## Detect technology

Discover the website's deployment technology, plugins, and supporting tools. Find out the CVEs of these technologies corresponding to the versions obtained.

## Fuzzing And Check endpoint  for information exposure

* Fuzzing all path
* access /robots.txt /sitemap.xml /sitemap.txt may expose some paths to special endpoints

## Test Parameter

Try ' in all parameters you encounter

Try test top 10 owasp web vulnerability in that

## Test Header

Try sql injection in header

```
User-Agent: "XOR(if(now()=sysdate(),sleep(5),0))XOR"
X-Forwarded-For: 0'XOR(if(now()=sysdate(),sleep(6),0))XOR'Z
```

