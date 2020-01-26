# ansible-galaxy

## Install ansible

```bash
sudo yum install python3
python3 -m venv venv-ansible
source venv-ansible/bin/activate
pip install ansible
ansible-galaxy
```

## Setup requirements

```bash
cat requirement.yml
# from galaxy
- src: yatesr.timezone

# from GitHub
- src: https://github.com/davidboukari/ansible-roles.git
```

## Create a role

```bash
ansible-galaxy init <newRole>
```

## Playbook sample for a role

```bash
cat playbook.yml
---
 - name: Install Graphical Mode and vnc tools
   become: true
   hosts: localhost
   roles:
    - {role: graphical-user}
```

## Install a role

```bash
cd $HOME/.ansible/roles
ansible-playbook -b -vvv playbook.yml
```
