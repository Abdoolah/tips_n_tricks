# Provide Sudo Access to users on target hosts for specific elevated commands

The `grant_sudo_access.yml` playbook calls the [`visudo_command`](roles/visudo_command/tasks/main.yml) role which 
1. Adds a group on the target host
1. Add the target user to the newly created group
1. Installs the specific command 
1. And creates a VISUDO file that grants passwordless sudo access to execute the command for the group.

### To call the playbook use the below command:

`ansible-playbook grant_sudo_access.yml`

Assumptions:
- The hosts variable references hosts groups defined in the inventory file.
> Example: 
```
[prod]
server01.example.com
server03.example.com
```
- The inventory file is referenced in the ansible.cfg local configuration file.
- The _<target_user>_ account exists on the target hosts.
- The user running the playbook _(as defined in the inventory file)_ has ```root``` access on the target hosts.