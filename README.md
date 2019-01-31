Julia docker container
=====

[![Docker Build Status](https://img.shields.io/docker/build/jgoldfar/julia-docker.svg) ![Docker Pulls](https://img.shields.io/docker/pulls/jgoldfar/julia-docker.svg)](https://hub.docker.com/r/jgoldfar/julia-docker/)


Setup
-----
First, add your local user to docker group:
```bash
sudo usermod -aG docker YOURUSERNAME
```

build:
```bash
docker build -t jgoldfar/julia-docker:vxx ./vxx
```

where `vxx` is one of `v07` (for Julia v0.7.x), `v10` (for Julia v1.0.x), or `v11` (for Jula v1.1.x). 

Usage:
-----

```bash
docker run --rm -i --user="$(id -u):$(id -g)" --net=none -v "$(pwd)":/data jgoldfar/julia-docker
```
Your working directory is mounted to `/data` inside container, in case you have scripts or local packages to run.

-----

## Container Descriptions

* `v07`: Latest Julia v0.7 release

* `v10`: Latest Julia v1.0.x release

* `v11`: Latest Julia v1.1.x release
