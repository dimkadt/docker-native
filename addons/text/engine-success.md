### Connect to the environment
```
eval $(docker-machine env ${env.envName})
```

### Connect the engine to a swarm cluster
```
docker swarm join --token $TOKEN $HOST:$PORT
```
