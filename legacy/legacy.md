# Artemis Nova (Ubuntu 20.04 LTS)

Guide for Enviroment configuration. To start, please follow the [Initial Configuration](./guides/InitialConfig.md) guide

## Deploy with ansible

Create custom configuration files

- `cp example.playbook.yml playbook.yml`
- `cp example.hosts.yml hosts.yml`
- `cp example.vars.yml vars.yml`

Modify hosts file and specify your hosts, ip's, usernames and ssh ports

- Host list `nano hosts.yml`
- Variable list `nano vars.yml`
- Main playbook `nano playbook.yml` (See [Roles](./roles/index.md))

Deploy all with:

`ansible-playbook -i hosts.yml playbook.yml -K`

## Use custom configuration per host

Create a new config file

`cp config/example.sshd_config config/custom.sshd_config`

Use custom `sshd_config_path` configuration file on `hosts.yml` *It asumes you saved it on config*

```yaml
localhost:
  ansible_host: 127.0.0.1
  ansible_port: 22
  host_user: angel
  sshd_config_path: "custom.sshd_config"
```

## Termux mode

Pre-requisites:

- ssh
- git
- python-apt (`pip install -e "git+https://salsa.debian.org/apt-team/python-apt.git@1.4.0_beta3#egg=python-apt"`)
