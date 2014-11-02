# Ansible code for basic Rails web server on CentOS 6.5

_Description: This is Ansible code for building Nginx + ruby 2.1.4/RVM/Rails + PostgreSQL or MySQL on CentOS 6.5.

## Project Setup

 1. `brew install python`

 2. `sudo easy_install pip`

 3. `sudo pip install ansible`

 4. `git clone https://github.com/morizyun/centos_ansible_rails.git`

 5. `cd centos-ansible-rails`

 6. Fill information;
    - create ./hosts_production file like `[web] IP_ADDRESS ansible_ssh_user=USER_NAME ansible_connection=ssh ansible_ssh_private_key_file=~/ssh/path/to` 
    - HOST_NAME in roles/nginx/files/production/nginx.conf
    - vars in ./playbook_production

 7. `export ANSIBLE_HOSTS=./hosts_production`

 8. 
    - no sudo password: `ansible-playbook ./playbook_production.yml`
    - having sudo password: `ansible-playbook ./playbook_production.yml -K`
