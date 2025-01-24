# geodns-web-setup

olegrumpy.ru

## How to run Ansible

Manually:
```shell
ansible-playbook -i inventory.hosts --limit olegrumpy_hk --diff main.yml
```

Also check scripts in ansible directory