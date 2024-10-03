# Basic Command

Login

```
gcloud auth activate-service-account --key-file=service_account2.json
```

List Credentialed Accounts

```
gcloud auth list
gcloud config list
```

Choose email active

```
gcloud config set account [email]
```

Get list project

```
gcloud projects list
```

Show metadata project

```
gcloud projects describe [projectid]
```

Choose project to access

```
gcloud config set project [projectid]
```

When choose project do list services of project

```
gcloud services list
```

Get permission&#x20;

```
 gcloud projects get-iam-policy ranger-8961d --format="json(bindings)"
```

Logout

```
gcloud auth revoke

gcloud auth revoke --all (all account wil log out     )
```



{% embed url="https://cloud.google.com/sdk/docs/cheatsheet" %}
