```
ansible myhosts -m ping -i inventory.ini

ansible-playbook -i myhosts.ini --ask-become-pass playbook.yaml
```