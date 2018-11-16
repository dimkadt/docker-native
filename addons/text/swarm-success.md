### Connect to the environment
```
eval $(docker-machine env ${env.envName})
```

### Add a Manager node to the cluster
```
docker swarm join --token \
${globals.manager_token} \
${nodes.cp.master.extIPs[0]}:2377
```

### Add a Worker node to the cluster
```
docker swarm join --token \
${globals.worker_token} \
${nodes.cp.master.extIPs[0]}:2377
```
