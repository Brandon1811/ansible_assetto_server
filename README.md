Uses ansible to install https://github.com/JustaPenguin/assetto-server-manager via docker-compose onto a CIS hardened Ubuntu 20.04 LTS server

Prerequisites:
1. A ubuntu 20.04 VPS server with a sudo capable (non-root) user capable of ssh w/o a password
2. ansible installed on your host/control machine

How to use:
1. $ git clone https://github.com/Brandon1811/ansible_assetto_server
2. $ cd ./ansible_assetto_server
3. $ ansible-galaxy install -p roles -r requirements.yml
4. $ cp example_inventory inventory
5. update your inventory file with your server(s) 
6. for each host in your inventory file, copy the example host_vars file into ./host_vars and update with your specific install details (usernames, passwords, etc.)
7. $ cp example_host_vars.yml host_vars/HOST_NAME.yml
8. $ ansible-playbook main.yml -i inventory -K 
   1. Can add --limit host1 to run playbook on the single host1 host (replace host1 with a hostname from your inventory file) 
