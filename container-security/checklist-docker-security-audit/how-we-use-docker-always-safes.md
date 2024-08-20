# How we use docker always safes!

* #### Keep Host and Docker up to date <a href="#rule-0-keep-host-and-docker-up-to-date" id="rule-0-keep-host-and-docker-up-to-date"></a>
* #### Do not expose the Docker daemon socket (even to the containers) <a href="#rule-1-do-not-expose-the-docker-daemon-socket-even-to-the-containers" id="rule-1-do-not-expose-the-docker-daemon-socket-even-to-the-containers"></a>
  *
* #### Set a user <a href="#rule-2-set-a-user" id="rule-2-set-a-user"></a>
* #### Limit capabilities (Grant only specific capabilities, needed by a container) <a href="#rule-3-limit-capabilities-grant-only-specific-capabilities-needed-by-a-container" id="rule-3-limit-capabilities-grant-only-specific-capabilities-needed-by-a-container"></a>
  * [ ] Do not run containers with the _--privileged_ flag (when run we will bypass seccomp, AppArmor, or SELinux tools
* [ ] a
*
*

{% embed url="https://cheatsheetseries.owasp.org/cheatsheets/Docker_Security_Cheat_Sheet.html" %}
