# Playbooks

Colección de Ansible Playbooks para configurar distintos Stacks

## Preparación

Configuración de la máquina Host

- Instalar Ansible: `sudo apt install ansible whois -y`

- Copiar archivos de configuración:
  - Hosts: `cp ./config/hosts.yml ./`
  - Variables: `cp ./config/vars.yml ./`

- Asegurate que tu clave privada tenga los permisos correctos: `chmod 600 [KEY]`

## Ejecución

Ejecución de los playbooks

- Configuración minima: `ansible-playbook -i hosts.yml minimal.yml`

- Instalación de Docker: `ansible-playbook -i hosts.yml docker.yml`
