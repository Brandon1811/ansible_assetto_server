How to use:

1. $ git clone {{github url here}}
2. $ cd ./ansible_assetto_server
3. $ ansible-galaxy install -p roles -r requirements.yml
4. $ ansible-playbook main.yml -i inventory -K 
   1. Can add --limit host1 to run playbook on the single host1 host (replace host1 with a hostname from your inventory file) 