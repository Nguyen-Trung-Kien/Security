---
description: >-
  Image Security (Bảo mật hình ảnh container) -> Secure the Build (mở rộng) ->
  Secure the Data -> Expose secrets
---

# Image Security

## Vulnerability Scanning

_Automatic_:

Use tools like Trivy, Clair, or anchore-engine to scan for vulnerabilities in the image.

_Manual testing_:

Review the source code, and version vulnerability, check for leaked credentials, API key, secret key, etc.

## Image Source Verification

Check the origin of images, and ensure Docker Images and their components are pulled from trusted and tested sources.

## Principle Of Least privilege

make sure the image is not configured to run as root (unless necessary)
