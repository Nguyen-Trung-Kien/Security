# Medium Scope For domain and subdomain

It is important to find out as many subdomains as possible and dig deep into how subdomains work.

## Subdomain

### Open source github

Search from multiple sources, as many as possible.

3 opensource i always use to

```
https://github.com/tomnomnom/assetfinder
https://github.com/owasp-amass/amass
https://github.com/projectdiscovery/subfinder
```

if you have a lot of time to wait or use as much as possible, for me, it's not necessary, I use a lot and filter out some necessary ones for my tools.

### Dork

Use many search engines like google, yahoo, duckduckgo, bing, etc. to search

```
site:*.domain.dtl
```

{% embed url="https://dorki.attaxa.com/" %}
I suggest use that
{% endembed %}

### Online search

Fofa

```
https://en.fofa.info/result?qbase64=ZG9tYWluPSJleGFtcGxlLmNvbSI%3D
```

Censys

```
https://search.censys.io/search?resource=hosts&sort=RELEVANCE&per_page=25&virtual_hosts=INCLUDE&q=https://search.censys.io/search/report?resource=hosts&q=services.tls.certificate.parsed.subject.common_name:example.com&virtual_hosts=INCLUDE&field=services.tls.certificate.parsed.subject.common_name&num_buckets=1000
```

Shodan

```
https://www.shodan.io/search?query=ssl.cert.subject.cn%3A*.example.com
```

Try find more

## Scan Port

With a not-too-large number of domains (unless you are a subdomain of a large company with several thousand live subdomains or more), you can scan the top port 1000 of these IP domains.



```
cat ip | naabu --top-ports 1000
```

{% embed url="https://github.com/projectdiscovery/naabu" %}
tools scan port
{% endembed %}

## FUZZING Content

always fuzzing in any website you see, try and try

```
dirsearch -u https://domain.dtl -w /path/to/wordlist.txt -x 404
ffuf -u https://domain.dtl/FUZZ -w /path/to/wordlist.txt -c -fc 404
```

