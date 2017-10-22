# Ansible playbook for configuring environment

## Install ansible

    sudo apt-get install ansible

## Run playbook

    ansible-playbook site.yml -i hosts
    
You can also configure selected services:

### Configuring only Kafka ecosystem

    ansible-playbook confluent.yml -i hosts
    
### Configuring only Elasticsearch with Kibana

    ansible-playbook elasticsearch.yml -i hosts
    
### Configuring only MySQL

    ansible-playbook mysql.yml -i hosts