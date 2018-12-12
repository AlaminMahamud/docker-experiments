```bash
docker swarm init
docker stack deploy -c docker-compose.yml <name>
docker service ls
docker container ls -q


# Scale the app
docker stack deploy -c docker-compose.yml <name>

# take down the app and the swarm
docker stack rm <name>

# take down the swarm
docker swarm leave --force
```