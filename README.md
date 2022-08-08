# ansible-task

Prerequisite:
1. Install Ansible on the host;
2. Run `ssh-copy-id -i ~/.ssh/id_rsa.pub ubuntu@host`;
3. Make the user member of the sudoers on the remote host.

Ansible Playbook for deploying webserver application. The deploy process consist of next steps:

1. Installation and configuration of nginx;
2. Installation and configuration of postgres;
3. Deploy and configuration of python web app;
4. Configuration of the network;
5. Make changes in `hosts` and `group_var/vars.yml` `playbook.yml` files if needed.

Clone the repository to the home directory and start the deploy by running the next commands:

``
cd ansible-task
``
``
ansible-playbook -i hosts rproxy-playbook.yml -b --ask-vault-password
``

Enter the Ansible Vault Password

---
Tested on Ubuntu 22.04.1 LTS

Used Resources:
https://github.com/mrlesmithjr/ansible-netplan
