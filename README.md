# ANSIBLE ROLE TELEGRAF

## Description
Ansible role for Telegraf agent deployment.

(See InfluxDB repository: https://github.com/influxdata/telegraf)
<br/><br/>

## Prepare an Ansible environment for deploying the role
Steps to prepare an Ansible environment for deploying the role:
```
$ cd <deployment location>
$ view agents.yml
~
---
- hosts: all
  become: True
  gather_facts: False
  roles:
    - telegraf
...
~
$ mkdir roles
$ cd roles/
$ git clone https://github.com/Guilleloper/ansible-role-telegraf
$ mv ansible-role-telegraf/ telegraf/
$ cd ..
```
<br/><br/>
## Deploy Telegraf:
```
$ ansible-playbook agents.yml --diff --check
$ ansible-playbook agents.yml --diff
```
