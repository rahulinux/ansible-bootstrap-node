# Ansible bootstrap node

### Introduction 

This ansible playbook will help you to setup bootstrap node, which will be use for interacting with kubernetes cluster using ansible-kubernetes-module 

### Prerequisite 

**Install ansible**

```shell
sudo pip install ansible==2.4.2.0
```

### Configuration 

  - You need inventory file which created during installation of kubernetes 
    - Check existing inventory file to create yours
  - You can modify inventory as per your need, but at least `kube-master` is needed

### Test inventory & connection 

```
ansible -i inventory  all -a 'uptime'
```
Once this working, you ready to setup bootstrap node

### Usage

```shell
ansible-playbook -i inventory setup_boostrap_node.yaml
``` 
