# Ansible Role: firewall

Role to setup and manage firewall on Debian based distros.

Requirements
------------
* Ansible 2.3.0

## Variables
```
ssh_port: 22
ssh_strict: "False"

allowed_ports:
  - 80
  - 443

# Allowed ips list (full access)
allowed_ips: []

# Group list allowed ips list (full access)
group_allowed_ips: []

# Local allowed ips list (full access)
local_allowed_ips:
  - "127.0.0.1"
  - "192.168.1.0/24"

iptables_service: 'netfilter-persistent'
```
## Playbook example:
```
---
- hosts: all
  roles:
    - firewall
```

License
-------
MIT

Author Information
------------------
Ivan Tuzhilkin ivan.tuzhilkin@gmail.com
