Here is command for installation, uninstallation, configuration places, configuration for external roles, checking configuration.
### Ansible installation
```bash
yum install ansible
apt install ansible
```
```bash
pip3 install ansible 
# for python2 - default installation 
pip install ansible
```
remote machine should have 'python' - 'gather_facts: False' or 'gather_facts: no' otherwise

## uninstall
```bash
rm -rf $HOME/.ansible
rm -rf $HOME/.ansible.cfg
sudo rm -rf /usr/local/lib/python2.7/dist-packages/ansible
sudo rm -rf /usr/local/lib/python2.7/dist-packages/ansible-2.5.4.dist-info
sudo rm -rf /usr/local/bin/ansible
sudo rm -rf /usr/local/bin/ansible-config
sudo rm -rf /usr/local/bin/ansible-connection
sudo rm -rf /usr/local/bin/ansible-console
sudo rm -rf /usr/local/bin/ansible-doc
sudo rm -rf /usr/local/bin/ansible-galaxy
sudo rm -rf /usr/local/bin/ansible-inventory
sudo rm -rf /usr/local/bin/ansible-playbook
sudo rm -rf /usr/local/bin/ansible-pull
sudo rm -rf /usr/local/bin/ansible-vault
sudo rm -rf /usr/lib/python2.7/dist-packages/ansible
sudo rm -rf /usr/local/lib/python2.7/dist-packages/ansible
```

## ansible configuration places
* path variable $Ansible_Config
* ~/.ansible.cfg
* /etc/ansible/ansible.cfg
```bash
ansible-config view
# list of possible environment variables
ansible-config dump
```

### configuration for external roles
filename: ~/.ansible.cfg
```properties
[defaults]
roles_path = ~/repos/project1/roles:~/repos/project2/roles
```

### check configuration
```bash
ansible-config view
```
