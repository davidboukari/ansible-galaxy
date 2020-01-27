# ansible-galaxy

## Install ansible

### with python venv module

```bash
sudo yum install python3
python3 -m venv venv-ansible
source venv-ansible/bin/activate
pip install ansible
ansible-galaxy
```

### with python virtualenv module

```bash
sudo pip3 install virtualenv
virtualenv -p  /usr/bin/python venv_python2
source venv_python2
pip install ansible
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
