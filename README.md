Ansible roles and playbooks

* Actually some tests using molecule are broken due to external dependencies



```
ansible-playbook -i hosts playbooks/docker.yml -e "myhosts=swarm action=install docker_use_lvm=true docker_pvname=/dev/sdb" -u root
```


```
ansible-playbook -i hosts playbooks/docker.yml -e "myhosts=swarm action=swarm" -u root

```