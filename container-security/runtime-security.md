---
description: >-
  Runtime Security is an important part of container security and it focuses on
  protecting applications and services running in a container environment in
  real-time.
---

# Runtime Security

Runtime Security (Bảo mật trong quá trình chạy container) -> Environment Security (đảm bảo low privilen)

## Least Privilege:

Ensure that the container is only granted the necessary permissions to execute its tasks, you can use tools such as Seccomp, and SELinux to manipulate this.

## Threat Detection:&#x20;

Use runtime monitoring tools like Falco to detect abnormal activity inside containers

## Resource Control:&#x20;

Configure resource limits (CPU, RAM) to prevent DoS attacks from containers.

## Why do that?

* Detection of IOC (Indicator Of Compromise)
* Detect Zero Days attack
* Compliance requirement
* Recommended in highly dynamic environments





{% embed url="https://github.com/krol3/container-security-checklist?tab=readme-ov-file#secure-the-container-runtime" %}
