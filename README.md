# Oceanic Nova

Configure new DigitalOcean VPS easily

## Installation

Install and configure Ansible, hosts and vars

- Install ansible & dependencies: `sudo apt install ansible whois -y`

- Install plugins: `ansible-galaxy collection install ansible.posix`

- Generate hashed password: `mkpasswd --method=sha-512`

- Create custom configuration files:

  - Copy vars file: `cp example.vars.yml vars.yml`. Here you need a github account with ssh keys, git config details and the hashed password. You can also filter hosts.

  - Copy hosts file: `cp example.hosts.yml hosts.yml`. Here you configure the hosts direction, user and other host specific variables

## Configure new VPS

Setup a new VPS with analitics and update packages

- Run initial playbook: `ansible-playbook -i hosts.yml initial.yml`

## Run some playbooks

- Run nodejs playbook: `ansible-playbook -i hosts.yml nodejs.yml -K`
