# Google Drive Api

## Search

```
googleapis.com/drive AND key
```

## Exploit

```
GET https://www.googleapis.com/drive/v3/files/{{randstr}}.txt/?key={{token}}&supportsAllDrives=true HTTP/1.1
Referer: {{BaseURL}}
Content-Type:application/json
```

