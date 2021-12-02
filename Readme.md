# Docker playground

## Description:

A simple Vagrantfile to setup an debian 11 box, install docker and docker-compose.

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
   vagrant ssh
   $ docker version
   Client: Docker Engine - Community
    Version:           20.10.11
    API version:       1.41
    Go version:        go1.16.9
    Git commit:        dea9396
    Built:             Thu Nov 18 00:37:33 2021
    OS/Arch:           linux/amd64
    Context:           default
    Experimental:      true

   Server: Docker Engine - Community
    Engine:
     Version:          20.10.11
     API version:      1.41 (minimum version 1.12)
     Go version:       go1.16.9
     Git commit:       847da18
     Built:            Thu Nov 18 00:35:39 2021
     OS/Arch:          linux/amd64
     Experimental:     false
    containerd:
     Version:          1.4.12
     GitCommit:        7b11cfaabd73bb80907dd23182b9347b4245eb5d
    runc:
     Version:          1.0.2
     GitCommit:        v1.0.2-0-g52b36a2
    docker-init:
     Version:          0.19.0
     GitCommit:        de40ad0

   $ docker-compose version
   docker-compose version 1.29.2, build unknown
   docker-py version: 5.0.3
   CPython version: 3.9.2
   OpenSSL version: OpenSSL 1.1.1k  25 Mar 2021
   ```

## Credits:

* author: kevinwaro
* contact: kevinwaro@yahoo.fr

## License:

This project is licensed under the GNU GPLv3 License - see the [License.md](License.md) file for details
