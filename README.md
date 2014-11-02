# CentOS 6.5/ruby 2.1.4/Nginx/Rails + PostgreSQL or MySQL

_Description: CentOS 6.5/ruby 2.1.4/Nginx + PostgreSQL or MySQL

## Project Setup

 1. Download and install Vagrant http://www.vagrantup.com/

 2. Download and install VirtualBox https://www.virtualbox.org/

 3. `brew install python`

 4. `sudo easy_install pip`

 5. `sudo pip install ansible`

 6. `git clone https://github.com/morizyun/centos-ansible-rails`

 7. `cd centos-ansible-rails`

 8 Fill information
    - create hosts_production file like `[web] IP_ADDRESS ansible_ssh_user=USER_NAME ansible_connection=ssh ansible_ssh_private_key_file=~/ssh/path/to` 
    - HOST_NAME in roles/nginx/files/production/nginx.conf
    - vars in playbook_production

 9. `export ANSIBLE_HOSTS=./ansible/hosts_production`

10. 
    - no sudo password: `ansible-playbook ./ansible/playbook_production.yml`
    - having sudo password: `ansible-playbook ./ansible/playbook_production.yml -K`
