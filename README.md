Simple Ansible playbook to setup vault on a VM
steps are as follows:
git clone https://github.com/iamrawtion/vaultsetup.git
cd vaultsetup
vagrant up
ansible-playbook tasks/main.yml -i tests/inventory 
