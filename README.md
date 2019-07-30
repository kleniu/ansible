# ansible
Simple ansible repo

## ad-hoc commands

```
ansible all -i hosts -u hlfd -m ping
```

```
ansible all -i hosts -u hlfd -m setup
```

update cache, upgrade and installing packages
```
ansible all -i hosts -u hlfd -m apt -a 'update_cache=yes' --become
ansible all -i hosts -u hlfd -m apt -a 'upgrade=dist update_cache=yes' --become
ansible all -i hosts -u hlfd -m apt -a 'name=aptitude state=latest' --become

```

## invoke playbooks
```
ansible-playbook -i hosts nodeplaybook.yaml 
```

## roles via ansible galaxy

create the dirs and then fill the yaml files
```
mkdir roles && cd roles
ansible-galaxy init common
ansible-galaxy init apache
```

# Source
```
https://www.redhat.com/rhtapps/promo-do007
https://www.howtoforge.com/ansible-guide-ad-hoc-command/
```
