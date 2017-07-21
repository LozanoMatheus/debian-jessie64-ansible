# VM + Debian 8 (Jessie) + Ansible
## Description
This file will create a Virtual Machine using Vagrant and VirtualBox using Debian Jessie x64 and Ansible was pre-installed.

## Pre-reqs
* [VirtualBox](https://www.virtualbox.org/wiki/Downloads) - To create Virtual Machines
* [Vagrant](https://www.vagrantup.com/downloads.html) - Automation and Build your build VMs

## How-to | Step-by-step
Download file and enter in folder
```
git clone https://github.com/LozanoMatheus/debian-jessie64-ansible.git
cd debian-jessie64-ansible
```

Download and create your VM
```
vagrant up
```

## Guides
### How-to Access your VM
```
vagrant ssh
```
or
```
vagrant ssh $ID or $VM_NAME
```
> Get ID/Name from vagrant global-status command

### How-to show all VMs/Boxes in your Vagrant
```
vagrant global-status
```

### How-to delete a VM in your Vagrant and VirtualBox
```
vagrant destroy $ID or $VM_NAME
```
> This option will delete files from your disk, but the Boxe of debian-jessie64-ansible still in local machine

> Get ID/Name from vagrant global-status command

### How-to delete all VM in your Vagrant and VirtualBox
```
vagrant destroy
```
> This option will delete files from your disk, but the Boxe of debian-jessie64-ansible still in local machine

