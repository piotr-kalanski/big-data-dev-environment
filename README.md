# big-data-dev-environment

Instruction how to setup Big Data local development environment to speed up development.

# High level design

Virtual machine with installed linux OS and multiple services (Kafka, Elasticsearch, Kibana, MySQL).

All installed services are accessible from host machine.

![](images/dev_environment_concept.png)

# Instruction

## Download VirtualBox

Download VirtualBox from: https://www.virtualbox.org/wiki/Downloads 

## Create and configure new VM with Ubuntu OS

### Create new virtual machine

Click new VM:

![](images/virtualbox_new_vm.png)

Enter below settings:

![](images/virtualbox_new_vm_settings.png)

![](images/virtualbox_new_vm_settings_disk.png)

### Download Ubuntu ISO

Go to website https://www.ubuntu.com/download/desktop and download Ubuntu ISO.

![](images/download_ubuntu_iso.png)

### Install Ubuntu OS on virtual machine

Go to storage settings for newly created virtual machine:

![](images/virtualbox_vm_storage_settings.png)

choose download Ubuntu ISO image:

![](images/virtualbox_vm_storage_settings_iso_image.png)

after selecting result should look like:

![](images/virtualbox_vm_storage_settings_selected_iso.png)

Run virtual machine and start installation process:

![](images/ubuntu_install_1.png)

![](images/ubuntu_install_2.png)

![](images/ubuntu_install_3.png)

based on https://linus.nci.nih.gov/bdge/installUbuntu.html

### Configure port forwarding for virtual machine

Go to global settings:

![](images/virtualbox_global_settings.png)

Add new NAT network:

![](images/virtualbox_network_settings.png)

Go to port forwarding rules:

![](images/virtualbox_network_setting.png)

Enter port forwarding rules:

![](images/virtualbox_port_forwarding_rules.png)

where `10.0.2.15` is IP address of guest machine (virtual machine) that can be checked with `ifconfig` command.

Go to virtual machine settings and configure network settings:

![](images/virtualbox_vm_setttings.png)

## Install software and configure services 

There are two options for installing and configuring services:
- automated way - using ansible playbook which is documented in [ansible] folder
- manually installing and configuring services which is documented in [manual] folder