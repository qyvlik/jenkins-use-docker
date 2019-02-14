# jenkins-use-docker

Use docker run jenkins, and call docker other api in jenkins.

## startup

1. copy the [.env.example](./.env.example) to [.env](./.env)
2. modify the `DOCKER_PATH`, `LIBLTDL_PATH`, `DOCKER_VOLUMES` to match your machine.
3. to start up: `docker-compose up -d`

### example of .env for ubuntu & centos

```
DOCKER_PATH=/usr/local/bin/docker
LIBLTDL_PATH=/usr/lib/x86_64-linux-gnu/libltdl.so.7
DOCKER_VOLUMES=~/dockr-volumes/
```
