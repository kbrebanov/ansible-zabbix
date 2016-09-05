zabbix
======

[![Build Status](https://travis-ci.org/kbrebanov/ansible-zabbix.svg?branch=master)](https://travis-ci.org/kbrebanov/ansible-zabbix)

Installs and configures Zabbix agent.

Requirements
------------

This role requires Ansible 1.9 or higher.

Role Variables
--------------

| Name                       | Default              | Description                                                       |
|:---------------------------|:---------------------|:------------------------------------------------------------------|
| zabbix_version             | 2.4                  | Version of Zabbix to install                                      |
| zabbix_agent_log_file_size | 0                    | Maximum size of log file in MB (0-1024) 0 - disables log rotation |
| zabbix_agent_server        | 127.0.0.1            | Zabbix server address                                             |
| zabbix_agent_server_active | 127.0.0.1            | Zabbix server address for active checks                           |
| zabbix_agent_hostname      | "{{ ansible_fqdn }}" | Fully qualified name of host                                      |

Dependencies
------------

None

Example Playbook
----------------

Install Zabbix agent
```yaml
- hosts: all
  roles:
    - name: kbrebanov.zabbix
```

Install Zabbix agent specifying version
```yaml
- hosts: all
  vars:
    zabbix_version: 2.2
  roles:
    - name: kbrebanov.zabbix
```

License
-------

BSD

Author Information
------------------

Kevin Brebanov
