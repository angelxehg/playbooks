# Playbooks

Colección de Ansible Playbooks para configurar distintos Stacks

## Preparación

Configuración de la máquina Host

- Instalar Ansible: `sudo apt install ansible whois -y`

- Crear archivo de Hosts: `cp ./hosts/example.yml ./hosts/localhost.yml`

- Asegurate que tu clave privada tenga los permisos correctos: `chmod 600 [KEY]`

## Ejecución

Ejecución de los playbooks

- Configuración minima: `ansible-playbook -i ./hosts/localhost.yml minimal.yml`

- Instalación de Python: `ansible-playbook -i ./hosts/localhost.yml python.yml`

- Instalación de NodeJS: `ansible-playbook -i ./hosts/localhost.yml nodejs.yml`

- Instalación de Docker: `ansible-playbook -i ./hosts/localhost.yml docker.yml`

- Instalación de MongoDB: `ansible-playbook -i ./hosts/localhost.yml mongodb.yml`
