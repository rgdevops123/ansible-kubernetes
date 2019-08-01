# ansible-kubernetes

- Install Kubernetes Cluster with Ansible.
- OS: CentOS 7
- Kubernetes Version: 1.15.1

## Before Install
- Use DNS Server or update /etc/hosts for all servers.

### Install Master
- Run the playbook.

```
ansible-playbook -i hosts master.yml

   On AWS EC2 Instances:
ansible-playbook -i hosts --key-file "~/kube.pem" -u centos master.yml
```

### Install Workers
- Run the playbook.
```
ansible-playbook -i hosts workers.yml

   On AWS EC2 Instances:
ansible-playbook -i hosts --key-file "~/kube.pem" -u centos workers.yml
```
