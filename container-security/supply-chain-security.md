# Supply Chain Security

## Dependency Management:

&#x20;Check and manage software components in docker images such as libraries, and image bases regularly to ensure no malicious dependencies are used, and regularly scan image containers.

## Image Signing:&#x20;

Use digital signatures (Docker Content Trust) to ensure that images are not modified during distribution.

## Compromised Registries:&#x20;

Keep up-to-date with the Registry where images are pulled, and check for warnings from these sources. You can use a self-built registry for easy control.

## Image source:&#x20;

Always make sure images are pulled from a clear source, always test images before building.
