# Docker file docker-compose.yaml - Dockerfile

## Docker-Compose.yaml

* [ ] Do not run containers as root
  * [ ] Specify user with 'user' command: user: "1000:1000"
  *
* [ ] Configure permissions for volumes
  * [ ] Use :ro to mount volumes with read-only permissions if writing is not required.
    * [ ] `volumes: - ./public:/var/www/html:ro`
  * [ ] Alternatively, grant permissions to that volume
    * [ ] `chown 1000:1000 /path/to/volume`
    * [ ] And the volume should be in a subfolder
    * [ ] public folder must exist, if it does not exist it will create a new folder and this folder defaults to **root permission**, need to manually configure above
  * [ ] Use environment variables safely
    * [ ] Don't show credentials or anythings secret
    * [ ] Set environment variables in a separate file (like .env) and not in the source code
  *   [ ] Limit resource usage

      * [ ] Set resource limits like CPU and RAM to avoid containers consuming too many resources.

      `resources: limits: cpus: "0.5" memory: "256M`"
  * [ ] Do not expose unnecessary ports
  * [ ] Use specific image versions (image: nginx:1.21.0-alpine **NOT** **use** image: nginx:latest)
  * [ ] Secure network configuration

> Use tools like Docker Bench Security to automatically test Docker and Docker Compose security configurations.

## Dockerfile

* [ ] Do not run the application with root permissions
* [ ] Use the USER command to set up a non-root user. (eg: USER 1001)
* [ ] Use the ADD command sparingly
  * [ ] Use COPY instead of ADD when not necessary to avoid automatic file downloads and decompression.
* [ ] Install only necessary packages
  * [ ] Do not install many unnecessary packages, which makes it difficult to manage and detect security errors
* [ ] Remove temporary files and caches
  * [ ] Clean up unnecessary files after installing packages to reduce image size and attack surface.
  * [ ] `RUN apt-get clean && rm -rf /var/lib/apt/lists/*`
* [ ] Use specific image versions (image: nginx:1.21.0-alpine **NOT** **use** image: nginx:latest)
* [ ] Managing sensitive information
  * [ ] Don't show credentials or anythings secret
* [ ] Manage permissions for files and folders
  * [ ] Set read-only access to non-writeable folders
