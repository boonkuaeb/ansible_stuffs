Ansible roles and playbooks

* Actually some tests using molecule are broken due to external dependencies



```
ansible-playbook -i hosts playbooks/docker.yml -e "myhosts=swarm action=install docker_use_lvm=true docker_pvname=/dev/sdb" -u root
```


```
ansible-playbook -i hosts playbooks/docker.yml -e "myhosts=swarm action=swarm" -u root

```


```
export DOCKER_HOST=192.168.60.10
```

```
docker service create --name viz \
--publish 8090:8080 \
--mount=type=bind,src=/var/run/docker.sock,dst=/var/run/docker.sock \
--constraint=node.role==manager \
 dockersamples/visualizer
```


`open http://192.168.60.10`




----------------------------------



