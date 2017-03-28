[![License: Apache 2.0](https://img.shields.io/badge/license-Apache--2.0-blue.svg)](https://www.apache.org/licenses/LICENSE-2.0.html)


Core Role
=========

This role handles basic server setup such as:
* Setting the server timezone and hostname
* Installing basic applications needed on all servers
* Installing fail2ban and configuring for SSH protection
* Hardening the system SSHd configuration to prevent DOS attacks

Usage
=====

Use like any other playbook.

Example Playbook
----------------

```
    - hosts: servers
      roles:
         - { role: core.role }
```

Role Variables
--------------
| Name | Description |
| :--: | :---------: |
| system_hostname | FQDN Hostname for the machine |
| system_timezone | Timezone for the server. UTC is default |
| fail2ban_service_enabled | Enable the fail2ban service. Options are yes/no |
| fail2ban_service_state | State of the service. Options are started/stopped |
| fail2ban_pkg_state | State of the package. Default is installed |
| fail2ban_config_ignoreip | Any IP CIRDs that are exempt from bans |
| fail2ban_config_bantime | Default time to ban an IP. Default is 600 seconds |
| fail2ban_config_maxretry | Maximum connection retries before ban is issued |
| fail2ban_config_destemail | The user who should receive emails from fail2ban about bans |
| fail2ban_config_jail_ssh_enabled | Monitor SSH login attempts for potential attacks. Options are yes/no |
| fail2ban_config_jail_sshddos_enabled | Enable SSH DOS protection Options are yes/no |

Requirements
============

There are no prerequisites.

Dependencies
============

There are no dependencies.

Credits
=======

Contributors
============

* Ted Salmon <tsalmon@laslabs.com>

Maintainer
==========

[![LasLabs Inc.](https://laslabs.com/logo.png)](https://laslabs.com)

This module is maintained by [LasLabs Inc.](https://laslabs.com)

* https://repo.laslabs.com/projects/DEP/repos/ansible-base/
