## Tips & Tricks
This repository holds some useful and handy techniques to setup or deploy scripts, playbooks or apps I have had experience on.

These have been tested to work as expected on `Fedora 34` running `KIND` local Kubernetes cluster and `docker` version 20.10. 

---

## K8s Prometheus via ArgoCD + Helm - Manual Installation
This is a quick and dirty manual deployment of Prometheus on a local Kubernetes cluster. The steps involve the installation of ArgoCD and the deployment of Prometheus using it's Helm chart.

[Prometheus-Manual_Installation](prometheus-manual-installation.md)


---

## K8s Prometheus via ArgoCD + Helm - Using Ansible
This writeup promises the deployment of Prometheus on a local Kubernetes cluster as well but using a bit more of Infrastructure as Code automation thanks to Ansible. 

[Prometheus-Ansible](prometheus-ansible.md)