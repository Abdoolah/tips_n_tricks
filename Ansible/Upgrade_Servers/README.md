# Generic Playbook to update target servers

The `deb_upgrade.yml` playbook calls two roles:
1. [Get_Package_Facts_](roles/Get_Package_Facts_/tasks/main.yml)
1. [Perform_Upgrade___](roles/Perform_Ugrade____/tasks/main.yml)
to firstly get the list of packages that have new updates that can be applied and then perform the actual upgrade of those packages. 

* This playbook only works on one host at a time and stops completely if there are any errors reported during the tasks execution. 
* A user approval prompt was included in the initial playbook but dismissed / commented out during the subsequent runs.
* If a reboot is required post upgrade, the playbook initiates the reboot and wait for the host to get back online and connected.

### To call the playbook use the below command:

`ansible-playbook deb_upgrade.yml`

### Assumptions:
- The hosts variable references hosts groups defined in the inventory file.
> Example: 
```
[prod_hosts]
server01.example.com
server03.example.com
```
- The inventory file is referenced in the `ansible.cfg` local configuration file.