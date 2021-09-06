# Generic Playbook To Setup Hardened Configs For OpenSSH 

The `create_openssh_config.yml` playbook calls the `harden_openssh` role to push a hardened OpenSSH config file onto the target hosts.

* The config file is derived from a Jinja template, [`sshd_config.j2`](roles/harden_openssh/templates/sshd_config.j2)
* This config file contains specific filters based on the target's Linux distribution, for example:
> ```{% if ansible_os_family == "RedHat" %}```
* Thus, only the OpenSSH configurations specific to each target host get configured.
* The last step is to reload the SSHD service on the target machine.

### To call the playbook use the below command:

`ansible-playbook create_openssh_config.yml`

### Assumptions:
- The hosts variable references hosts groups defined in the inventory file.
> Example: 
```
[prod_hosts]
server01.example.com
server03.example.com
```
- The inventory file is referenced in the `ansible.cfg` local configuration file.