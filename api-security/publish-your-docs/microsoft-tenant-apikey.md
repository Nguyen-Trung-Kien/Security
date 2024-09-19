# Microsoft tenant apikey

Search

```
// Some code
```

## Exploit

```
curl -X POST -H 
"Content-Type: application/x-www-form-urlencoded" 
-d 'client_id=<CLIENT_ID>&scope=https://graph.microsoft.com/.default&client_secret=<CLIENT_SECRET>&grant_type=client_credentials' 
'https://login.microsoftonline.com/<TENANT_ID>/oauth2/v2.0/token'
```
