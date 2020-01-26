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

