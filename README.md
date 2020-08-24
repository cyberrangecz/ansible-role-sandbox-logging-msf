KYPO Sandbox Logging Msfconsole Commands
=========

This role provides local Metasploit command logging.

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


License
-------

MIT
