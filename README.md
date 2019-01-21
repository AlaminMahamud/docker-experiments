# Docker Experiments
A Self Sufficient RT for containers.

## Commands

``` bash
docker version
---------------

| Client:       |             |         |          |          |       |
| Version:      | 18.03.1-ce  |         |          |          |       |
| API           | version:    | 1.37    |          |          |       |
| Go            | version:    | go1.9.5 |          |          |       |
| Git           | commit:     | 9ee9f40 |          |          |       |
| Built:        | Wed         | Jun     |       20 | 21:43:51 |  2018 |
| OS/Arch:      | linux/amd64 |         |          |          |       |
| Experimental: | false       |         |          |          |       |
| Orchestrator: | swarm       |         |          |          |       |
|               |             |         |          |          |       |
| Server:       |             |         |          |          |       |
| Engine:       |             |         |          |          |       |
| Version:      | 18.03.1-ce  |         |          |          |       |
| API           | version:    | 1.37    | (minimum |  version | 1.12) |
| Go            | version:    | go1.9.5 |          |          |       |
| Git           | commit:     | 9ee9f40 |          |          |       |
| Built:        | Wed         | Jun     |       20 | 21:42:00 |  2018 |
| OS/Arch:      | linux/amd64 |         |          |          |       |
| Experimental: | false       |         |          |          |       |


```

``` bash
docker info
-----------------
| Containers:   | 29                                                          |                                          |                 |      |          |           |            |        |        |
| Running:      | 0                                                           |                                          |                 |      |          |           |            |        |        |
| Paused:       | 0                                                           |                                          |                 |      |          |           |            |        |        |
| Stopped:      | 29                                                          |                                          |                 |      |          |           |            |        |        |
| Images:       | 39                                                          |                                          |                 |      |          |           |            |        |        |
| Server        | Version:                                                    | 18.03.1-ce                               |                 |      |          |           |            |        |        |
| Storage       | Driver:                                                     | overlay2                                 |                 |      |          |           |            |        |        |
| Backing       | Filesystem:                                                 | extfs                                    |                 |      |          |           |            |        |        |
| Supports      | d_type:                                                     | true                                     |                 |      |          |           |            |        |        |
| Native        | Overlay                                                     | Diff:                                    | true            |      |          |           |            |        |        |
| Logging       | Driver:                                                     | json-file                                |                 |      |          |           |            |        |        |
| Cgroup        | Driver:                                                     | cgroupfs                                 |                 |      |          |           |            |        |        |
| Plugins:      |                                                             |                                          |                 |      |          |           |            |        |        |
| Volume:       | local                                                       |                                          |                 |      |          |           |            |        |        |
| Network:      | bridge                                                      | host                                     | macvlan         | null | overlay  |           |            |        |        |
| Log:          | awslogs                                                     | fluentd                                  | gcplogs         | gelf | journald | json-file | logentries | splunk | syslog |
| Swarm:        | inactive                                                    |                                          |                 |      |          |           |            |        |        |
| Runtimes:     | runc                                                        |                                          |                 |      |          |           |            |        |        |
| Default       | Runtime:                                                    | runc                                     |                 |      |          |           |            |        |        |
| Init          | Binary:                                                     | docker-init                              |                 |      |          |           |            |        |        |
| containerd    | version:                                                    | 773c489c9c1b21a6d78b5c538cd395416ec50f88 |                 |      |          |           |            |        |        |
| runc          | version:                                                    | 4fc53a81fb7c994640722ac585fa9ca548971871 |                 |      |          |           |            |        |        |
| init          | version:                                                    | 949e6fa                                  |                 |      |          |           |            |        |        |
| Security      | Options:                                                    |                                          |                 |      |          |           |            |        |        |
| apparmor      |                                                             |                                          |                 |      |          |           |            |        |        |
| seccomp       |                                                             |                                          |                 |      |          |           |            |        |        |
| Profile:      | default                                                     |                                          |                 |      |          |           |            |        |        |
| Kernel        | Version:                                                    | 4.15.0-29-generic                        |                 |      |          |           |            |        |        |
| Operating     | System:                                                     | Ubuntu                                   | 18.04           | LTS  |          |           |            |        |        |
| OSType:       | linux                                                       |                                          |                 |      |          |           |            |        |        |
| Architecture: | x86_64                                                      |                                          |                 |      |          |           |            |        |        |
| CPUs:         | 4                                                           |                                          |                 |      |          |           |            |        |        |
| Total         | Memory:                                                     | 7.703GiB                                 |                 |      |          |           |            |        |        |
| Name:         | personal-laptop                                             |                                          |                 |      |          |           |            |        |        |
| ID:           | WALD:W6HD:5VFX:KW3E:XRMQ:DMOP:GA37:YBMW:XLIT:4B4H:ZQI2:H22E |                                          |                 |      |          |           |            |        |        |
| Docker        | Root                                                        | Dir:                                     | /var/lib/docker |      |          |           |            |        |        |
| Debug         | Mode                                                        | (client):                                | false           |      |          |           |            |        |        |
| Debug         | Mode                                                        | (server):                                | false           |      |          |           |            |        |        |
| Registry:     | https://index.docker.io/v1/                                 |                                          |                 |      |          |           |            |        |        |
| Labels:       |                                                             |                                          |                 |      |          |           |            |        |        |
| Experimental: | false                                                       |                                          |                 |      |          |           |            |        |        |
| Insecure      | Registries:                                                 |                                          |                 |      |          |           |            |        |        |
| 127.0.0.0/8   |                                                             |                                          |                 |      |          |           |            |        |        |
| Live          | Restore                                                     | Enabled:                                 | false           |      |          |           |            |        |        |
|               |                                                             |                                          |                 |      |          |           |            |        |        |
```


### Options
```bash
      --config string      Location of client config files (default "/home/alamin/.docker")
  -D, --debug              Enable debug mode
  -H, --host list          Daemon socket(s) to connect to
  -l, --log-level string   Set the logging level ("debug"|"info"|"warn"|"error"|"fatal") (default "info")
      --tls                Use TLS; implied by --tlsverify
      --tlscacert string   Trust certs signed only by this CA (default "/home/alamin/.docker/ca.pem")
      --tlscert string     Path to TLS certificate file (default "/home/alamin/.docker/cert.pem")
      --tlskey string      Path to TLS key file (default "/home/alamin/.docker/key.pem")
      --tlsverify          Use TLS and verify the remote
  -v, --version            Print version information and quit

```

### Management Commands
``` bash
  config      Manage Docker configs
  container   Manage containers
  image       Manage images
  network     Manage networks
  node        Manage Swarm nodes
  plugin      Manage plugins
  secret      Manage Docker secrets
  service     Manage services
  swarm       Manage Swarm
  system      Manage Docker
  trust       Manage trust on Docker images
  volume      Manage volumes
```

* Syntax

``` bash
docker <management-command> <sub-command> (options)
```

### Containers
* Syntax

``` bash
docker container <COMMAND> (Options)

[
   attach,
   commit,
   cp,
   create,
   diff,
   exec,
   inspect,
   kill,
   logs,
   ls,
   pause,
   port,
   prune,
   rename,
   restart,
   rm,
   run,
   start,
   stop,
   top,
   unpause,
   update,
   wait
]

```


``` bash
 # Start a container
 docker container run --publish 8080:80 nginx
 # Start a detached container
 docker container run --publish 8080:80 --detach nginx
 # Start a named detached container
 docker container run \
                  --publish 8080:80 \
		  --detach \
		  --name webhost nginx
 
 # Show running containers
 docker container ls
 # Show all containers
 docker container ls -a
 # logs
 docker container logs <container-name> | <container-id>
 # stats
 docker container stats [<container-name> | <container-id>]
 # top
 docker container top [<container-name> | <container-id>]
 # inspect
 docker container inspect [<container-name> | <container-id>]
```
## Docker Networking
* Network Drivers
  * **bridge** - default
	* usecase - applications run in stand alone containers that need to communicate
  * **host** - remove network isolation between the container and the docker host, and use the host's networking directly.
	* usecase - available for swarm
  * **overlay** network
	- connect multiple docker daemons together and enable swarm services to communicate with each other. 
	- use overlay networks to facilitate communication between a swarm service and a stand-alone container, or between two stand-alone containers on different docker daemons
  * **macvlan** network
	- assign a MAC address to a container, appear as a physical device.
	- routes traffic to a container by MAC address.
  * **none** - disable all networking

* Network Driver Summary
  - User Defined Bridge: best when you need multiple containers to communicate on the same docker host.
  - Host Network: network stack should not be isolated but other stack of docker should.
  - Overlay Network: best when running on cluster or swarm
  - Macvlan Network: best when migrating from a VM setup or need your containers to look like Physical hosts on your network, each with a unique MAC Address

* Extra Drivers EE
  - HTTP Routing Mesh
  - Session Stickiness
## Communicating between containers

``` bash
docker run -d --name redis-server redis
```

``` bash
docker  run --link redis-server:redis alpine env
```

``` bash
docker run --link redis-server:redis alpine cat /etc/hosts
```

``` bash
docker run --link redis-server:redis alpine ping -c 1 redis
```

``` bash
docker run -d -p 3000:3000 \
	--link redis-server:redis \
	katacoda/redis-node-docker-example
```

``` bash
curl docker:3000
```

``` bash
docker run -it \
	--link redis-server:redis \
	redis redis-cli -h redis
```
## More Networking in Docker
* Create Network
```
docker network create backend-network
```
* Connect to network
```
docker run -d --name=redis \
              --net=backend-network \
              redis
```

Unlike using links, docker network behave like traditional networks where nodes can be attached/detached.

```
docker run --net=backend-network alpine env
docker run --net=backend-network alpine cat /etc/hosts
```

Instead, the way containers can communicate via an Embedded DNS Server in Docker.
The DNS Server in assigned to all containers via the IP `127.0.0.11` and set in the `/etc/resolv.conf`

When containers attempt to access other containers via a well-known name, such as Redis, the DNS server will return the IP address of the correct Container. In this case, the fully qualified name of Redis will be redis.backend-network.
```
docker run --net=backend-network alpine ping -c1 redis
```

* Connect two containers
```
docker network create frontend-network
```
When using the connect command it is possible to attach existing containers to the network.
```
docker network connect frontend-network redis
docker run -d \
           -p 3000:3000 \
           --net=frontend-network \
           katacoda/redis-node-docker-example
```

```
curl docker:3000
# tip: to resolve ip address of a host -
# getent hosts <host> | awk '{print $1}'
```

* Connect Container with Alias
this will connect redis instance to the frontend-network with the alias of db

```
docker network create frontend-network2
docker network connect --alias db frontend-network2 redis
```

Now reach to `redis` using alias `db`, they will be given the IP address of our Redis container.

```
docker run --net=frontend-network2 alpine ping -c1 db
```

* Disconnect Containers
```
docker network ls
```

```
docker network inspect <network-name>
```

```
docker network disconnect <network-name> <container-name>
```
## Persisting Data using volumes
Docker Volumes allows you to upgrade containers, restart machines and share data without data loss. This is essential when updating database or application versions.

Docker Volumes are created and assigned when containers are started. Data Volumes allow you to map a host directory to a container for sharing data.

This mapping is bi-directional. It allows data stored on the host to be accessed from within the container. It also means data saved by the process inside the container is persisted on the host.

```shell
docker run -v /docker/redis-data:/data --name r1 redis redis-server --appendonly=yes
cat data | docker exec -i r1 redis-cli --pipe
ls /docker/redis-data
docker run -v /docker/redis-data:/backup ubuntu ls /backup
```

* Shared Volumes
An alternate approach is to use `--volumes-from`. The parameter maps the mapped volumes from the source container to the container being launched

In this case, we're mapping our Redis container's volume to an Ubuntu container. The /data directory only exists within our Redis container, however, because of -volumes-from our Ubuntu container can access the data.

```
docker run --volumes-from r1 -it ubuntu ls /data
```

* Read-only volumes
If the container attempts to modify data within the directory it will error.
```
docker run -v /docker/redis-data:/data:ro -it ubuntu rm -rf /data
```

## Managing Log Files
* Docker Logs
```docker run -d --name redis-server redis```
```docker logs  redis-server```

### Syslog
By default, the Docker logs are outputting using the json-file logger meaning the output stored in a JSON file on the host. This can result in large files filling the disk. As a result, you can change the log driver to move to a different destination.

The Syslog log driver will write all the container logs to the central syslog on the host. "syslog is a widely used standard for message logging. It permits separation of the software that generates messages, the system that stores them, and the software that reports and analyses them

The log-driver is designed to be used when syslog is being collected and aggregated by an external system.

### Example
```docker run -d --name redis-syslog --log-driver=syslog redis```

### Accessing Logs
you need to access them via the syslog stream

### Disable Logging
```docker run -d --name redis-none --log-driver=none redis```
```docker inspect --format '{{ .HostConfig.LogConfig }}' redis-server```