# Docker Fedora Systemd

[![build status](https://img.shields.io/docker/cloud/build/daosdo/fedora-systemd)](https://hub.docker.com/repository/docker/daosdo/fedora-systemd)

Fedora image that has systemd enabled.

## Branches

Each branch in the repository is used for building a specific version.

| Branch | Fedora Version | FROM Docker image tag |
| ------ | -------------- | --------------------- |
| master | latest         | latest                |
| 33     | 33             | 33                    |

## Usage

### Run it

```
docker run -d \
  --tty \
  --privileged \
  --volume /sys/fs/cgroup:/sys/fs/cgroup:ro \
  --name daosd-fedora33-systemd \
  daosdo/fedora-systemd:33
```

Adding `--tty` allocates a pseudo-TTY and enables color in the logs when
running `docker logs`.

### Enter it

```
docker exec -it daosd-fedora33-systemd /bin/bash
```

### Remove it

```
docker rm -f daosd-fedora33-systemd
```
