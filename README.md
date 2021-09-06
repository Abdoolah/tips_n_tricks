## Tips & Tricks
This repository holds some useful and handy techniques to setup or deploy scripts, playbooks or apps I have had experience with.

- The Kubernetes deployments have been tested to work as expected on `Fedora 34` running `KIND` local Kubernetes cluster and `docker` version 20.10. 

- The Ansible playbooks are successfully run from within `Kali Linux`.

---

## K8s Prometheus via ArgoCD + Helm - Manual Installation
This is a quick and dirty manual deployment of Prometheus on a local Kubernetes cluster. The steps involve the installation of ArgoCD and the deployment of Prometheus using it's Helm chart.

[Prometheus-Manual_Installation](Prometheus-Manual_Installation/README.md)

---

## Ansible Series - Generic Playbook to install SSH Keys onto target hosts
A simple playbook to propagate one's public keys on target hosts.

[Generic-AddKey](Ansible/Generic_AddKey)

---

## Ansible Series - OpenSSH Configuration Hardening
This playbook deploys a custom hardened OpenSSH configuration file based on the target machine's Linux Distribution.

[OpenSSH Hardening](Ansible/OpenSSH_Hardening)

---

## Ansible Series - Set Sudo Privileges for specific commands
Using VISUDO and groups to allow a remote non-sudo user the ability to run specific elevated commands.

[Set Sudo Access](Ansible/Provide_Sudo_Access)

---

## Ansible Series - Upgrade Debian Servers
A playbook which will retrieve the list of updates available on the target hosts and safely update the machine, one host at a time. 

[Do Package Upgrade](Ansible/Upgrade_Servers)

---

## K8s Prometheus via ArgoCD + Helm - Using Ansible
This writeup promises the deployment of Prometheus on a local Kubernetes cluster as well but using a bit more of Infrastructure as Code automation thanks to Ansible. 

[Prometheus-Ansible](Prometheus-Ansible)
