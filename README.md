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

