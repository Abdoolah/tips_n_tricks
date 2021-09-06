# Generic Playbook to install your SSH Keys onto target hosts

The `add_key.yml` playbook calls the [`copy_authorized_keys`](roles/copy_authorized_keys/tasks/main.yml) role which uses the [`authorized_key`](https://docs.ansible.com/ansible/latest/collections/ansible/posix/authorized_key_module.html) module to set your authorized key on the target hosts for the user account passed as parameter.

### To call the playbook use the below command:

`ansible-playbook add_key.yml --extra-vars ¨who=<target_user>¨`

### Assumptions:
- The hosts variable references hosts groups defined in the inventory file.
> Example: 
```
[prod]
server01.example.com
server03.example.com
```
- The inventory file is referenced in the `ansible.cfg` local configuration file.
- The _<target_user>_ account exists on the target hosts.