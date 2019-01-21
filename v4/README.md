```bash
docker-machine create --driver virtualbox myvm1
docker-machine create --driver virtualbox myvm2
docker-machine ls
docker-machine ssh myvm1 "docker swarm init --advertise-addr <myvm1 ip>"
docker-machine ssh myvm2 "docker swarm join \
--token <token> \
<ip>:2377"
docker-machine ssh myvm1 "docker node ls"
```