centos_ansible_rails
====

Ansible code for ruby 2.2.0/rvm/PostgreSQL/Nginx in Amazon Linux or CentOS 6.5

## Preparation

Install Python/pip/Ansible

 1. `brew install python`

 2. `sudo easy_install pip`

 3. `sudo pip install ansible`

 4. `git clone git@github.com:morizyun/centos_ansible_rails.git`

 5. `cd centos_ansible_rails`

## Usage

### Production

 1. `export ANSIBLE_HOSTS=./ansible/hosts_production`

 2. `ansible-playbook ./ansible/playbook_production.yml -K`
 
 3. type `passw0rd` in Password
 
 3. set rails-project to `/var/rails/`

## Basic Information

1. PostgreSQL ROOT PASS : ``(nothing)
