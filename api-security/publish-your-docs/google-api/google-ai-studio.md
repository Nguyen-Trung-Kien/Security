# Google AI Studio

## Search

```
// Some code
```

## Exploit

```
curl \
  -H 'Content-Type: application/json' \
  -d '{"contents":[{"parts":[{"text":"Explain how AI works"}]}]}' \
  -X POST 'https://generativelanguage.googleapis.com/v1beta/models/gemini-1.5-flash-latest:generateContent?key=YOUR_API_KEY'
```

Burpsite requests

```
POST /v1/models/gemini-pro:generateContent?key=apikey HTTP/2
Host: generativelanguage.googleapis.com
Accept-Encoding: gzip, deflate
Accept: */*
Accept-Language: en-US;q=0.9,en;q=0.8
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/114.0.5735.199 Safari/537.36
Cache-Control: max-age=0
Content-Type: application/json
Content-Length: 58

{"contents":[{"parts":[{"text":"Explain how AI works"}]}]}
```
