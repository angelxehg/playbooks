# Oceanic Nova

Configure new DigitalOcean VPS easily

## Installation

Install and configure Ansible, hosts and vars

- Install ansible: `sudo apt install ansible -y`

- Install plugins: `ansible-galaxy collection install ansible.posix`

- Create custom configuration files:

  - Copy vars file: `cp example.vars.yml vars.yml`

  - Copy hosts file: `cp example.hosts.yml hosts.yml`

## Configure new VPS

Setup a new VPS with analitics and update packages

- Run initial playbook: `ansible-playbook -i hosts.yml initial.yml`
<!-- `ansible-playbook -i hosts.yml start.yml -K` -->
