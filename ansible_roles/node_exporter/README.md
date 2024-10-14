# Ansible roles

Проект содержит роли Ansible.

## Playbooks

- `playbook.yml`: Main playbook for server configuration.
- `deploy.yml`: Playbook for deploying applications.
- `backup.yml`: Playbook for performing backups.

## Inventory

The inventory file `inventory` contains the list of servers grouped by environment.

### Example Inventory File
ini
[development]
server1 ansible_host=192.168.0.101
server2 ansible_host=192.168.0.102
[production]
server3 ansible_host=192.168.0.201
server4 ansible_host=192.168.0.202

## Usage

To run the main playbook on the production servers:

bash
ansible-playbook -i inventory playbook.yml --limit production
