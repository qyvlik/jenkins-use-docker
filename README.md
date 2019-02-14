# jenkins-use-docker

Use docker run jenkins, and call docker other api in jenkins.

## startup

1. copy the [.env.example](./.env.example) to [.env](./.env)
2. modify the `DOCKER_PATH`, `LIBLTDL_PATH`, `DOCKER_VOLUMES` to match your machine.
3. to build: `docker-compose build`
4. to start up: `docker-compose up -d`
5. to fix `Permission denied`, `chown -R NOT_ROOT_USER:NOT_ROOT_USER ${DOCKER_VOLUMES}` to change the `DOCKER_VOLUMES` owner.

### example of .env for ubuntu

```
DOCKER_PATH=/usr/local/bin/docker
LIBLTDL_PATH=/usr/lib/x86_64-linux-gnu/libltdl.so.7
DOCKER_VOLUMES=~/docker-volumes/
```

### example of .env for centos

```
DOCKER_PATH=/bin/docker
LIBLTDL_PATH=/lib64/libltdl.so.7
DOCKER_VOLUMES=~/docker-volumes/
```