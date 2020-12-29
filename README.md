# Playbooks

Colección de Ansible Playbooks para configurar automáticamente distintos Stacks de desarrollo.

## Preparación

Configuración de la máquina Host

- Instalar Ansible: `sudo apt install ansible whois -y`

- Crear archivo de Hosts: `cp ./hosts/example.yml ./hosts/localhost.yml`

- Asegurate que tu clave privada tenga los permisos correctos: `chmod 600 [KEY]`

## Ejecución

Ejecución de los playbooks. Se pedirá la contraseña de SUDO:

- Configuración minima: `ansible-playbook -i ./hosts/localhost.yml minimal.yml -K`

- Instalación de Python: `ansible-playbook -i ./hosts/localhost.yml python.yml -K`

- Instalación de NodeJS: `ansible-playbook -i ./hosts/localhost.yml nodejs.yml -K`

- Instalación de Docker: `ansible-playbook -i ./hosts/localhost.yml docker.yml -K`

- Instalación de MongoDB: `ansible-playbook -i ./hosts/localhost.yml mongodb.yml -K`
