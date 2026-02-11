# Docker playground

## Description:

A simple Vagrantfile to setup an debian 13 box, install docker and docker-compose.

## Usage:

First, clone the repo:

   ```
   git clone https://github.com/kevinwaro/docker_playground && cd docker_playground
   ```

Then let Vagrant create and provision the vms:

   ```
   vagrant up
   ```

Once everything is provisionned, you can ssh to the master node and start playing with the swarm:

   ```
   $ docker version
   Client: Docker Engine - Community
    Version:           29.2.1
    API version:       1.53
    Go version:        go1.25.6
    Git commit:        a5c7197
    Built:             Mon Feb  2 17:17:31 2026
    OS/Arch:           linux/amd64
    Context:           default

   Server: Docker Engine - Community
    Engine:
     Version:          29.2.1
     API version:      1.53 (minimum version 1.44)
     Go version:       go1.25.6
     Git commit:       6bc6209
     Built:            Mon Feb  2 17:17:31 2026
     OS/Arch:          linux/amd64
     Experimental:     false
    containerd:
     Version:          v2.2.1
     GitCommit:        dea7da592f5d1d2b7755e3a161be07f43fad8f75
    runc:
     Version:          1.3.4
     GitCommit:        v1.3.4-0-gd6d73eb8
    docker-init:
     Version:          0.19.0
     GitCommit:        de40ad0
  
   $ docker compose version
   Docker Compose version v5.0.2
   ```

## Credits:

* author: kevinwaro
* contact: kevinwaro@yahoo.fr

## License:

This project is licensed under the GNU GPLv3 License - see the [License.md](License.md) file for details
