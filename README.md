KYPO Sandbox Logging Msfconsole Commands
=========

This role provides local Metasploit command logging.

## Authors

Name          | Email          
------------- | ------------
Pavel Šeda    |   441048@mail.muni.cz

Requirements
------------

* Metasploit 

Example Playbook
----------------
```
- hosts:
      - routers
      - hosts
  become: true
  roles:
    - role: kypo-sandbox-logging-msf

```