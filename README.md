zabbix
======

[![Ansible Role](https://img.shields.io/ansible/role/3405.svg)](https://galaxy.ansible.com/list#/roles/3405)

Installs and configures Zabbix agent.

Requirements
------------

This role requires Ansible 1.4 or higher.

Role Variables
--------------

| Name                       | Default              | Description                                                       |
|----------------------------|----------------------|-------------------------------------------------------------------|
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
```
- hosts: all
  roles:
    - { role: kbrebanov.zabbix }
```

Install Zabbix agent specifying version
```
- hosts: all
  roles:
    - { role: kbrebanov.zabbix, zabbix_version: 2.2 }
```

License
-------

BSD

Author Information
------------------

Kevin Brebanov
