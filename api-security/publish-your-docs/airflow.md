---
description: >-
  Apache Airflow® is an open-source platform for developing, scheduling, and
  monitoring batch-oriented workflows.
---

# Airflow

## Search

```
api/v1/dags AND /https?:\/\/[^\/\s]+\.*\.com\/[^?\s]*/ AND --user NOT example
```

## Exploit

```
curl -X GET "http://<airflow_url>/api/v1/dags" \
--user "username:password"
```
