# Ansible playbook for configuring environment

## Install ansible

First you have to install ansible, you can do it with:

    sudo apt-get install ansible

## Configure all services

Run ansible playbook:

    ansible-playbook site.yml -i hosts
    
## Configure only selected services

You can also configure selected services:

### Configuring only Kafka ecosystem

    ansible-playbook confluent.yml -i hosts
    
### Configuring only Elasticsearch with Kibana

    ansible-playbook elasticsearch.yml -i hosts
    
### Configuring only MySQL

    ansible-playbook mysql.yml -i hosts