# Ansible role for auditd

# Requirements
* Debian

# Defaults

```
audit_rules_tpl: "audit_rules.j2"
audit_rules: []
audit_buffer: 81920
```

# Usage
```
- hosts: localhost
  roles:
        - auditd
  vars:
          audit_rules:
                  - { rule: '-a always,exit -S all -F uid=www-data', comment: "hallo" }
                  - { rule: '-a always,exit -S all -F uid=root' }

```
