[![License: Apache 2.0](https://img.shields.io/badge/license-Apache--2.0-blue.svg)](https://www.apache.org/licenses/LICENSE-2.0.html)

Ansible Base System Playbook
============================

This playbook should be used to provision basic roles on a newly deployed server.

Usage
=====

You should make sure to init all submodules, like so:
```
git submodule update --init --recursive
```
or clone this repo recursively, like so:
```
git clone --recursive $URI
```

From there, you have three basic roles to provision:
* core.role - Basic system configuration
* active-directory.role - Provision SSSD to connect server to an AD auth back-end
* RHEL-STIG.role - Advanced system hardening role

See the individual roles for the configuration options that are available. Use
 settings.yml and settings.vault.yml for your custom options.

Contributors
============

* Ted Salmon <tsalmon@laslabs.com>

Maintainer
==========

[![LasLabs Inc.](https://laslabs.com/logo.png)](https://laslabs.com)

This module is maintained by [LasLabs Inc.](https://laslabs.com)

* https://repo.laslabs.com/projects/DEP/repos/ansible-base/
