Functional Tests
================

How to run functional tests?

* Edit /etc/ansible/hosts and add at least one machine to the group called
  clients. E.g.:

```ini
[clients]
centos7.example.com
```

* You have to be able to login to all machines in group using ssh key
  (not password).
* Execute following commands:

```bash
cd ./ansible_playbooks
ansible-playbook ./register_system.yml
ansible-playbook ./attach_subscriptions.yml
ansible-playbook ./test_install_remove_packages.yml
ansible-playbook ./test_not_remove_prod_cert_for_disabled_repo.yaml
```

