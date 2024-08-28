---
description: >-
  asana is a web and mobile "work management" platform designed to help teams
  organize, track, and manage their work
---

# Asana

## Search

```
0\/[a-z0-9]{32} (regex github)
```

## Exploit

Get user information

```
GET /api/1.0/users/me HTTP/1.1
Host: app.asana.com
Authorization: Bearer 0/----key
Accept-Encoding: gzip, deflate
Accept: */*
Accept-Language: en-US;q=0.9,en;q=0.8
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/114.0.5735.199 Safari/537.36
Connection: close
Cache-Control: max-age=0
```

```
Get task information
https://app.asana.com/api/1.0/projects/{project_id}/tasks
Get section information
https://app.asana.com/api/1.0/projects/{project_id}/sections
Get section's task information
https://app.asana.com/api/1.0/sections/{section_id}/tasks
```
