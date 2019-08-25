# Docker commands

## Containers

- docker container top

  Process list in one container

- docker container inspect

  Show metadata about the container (startup, config, volumes, networking, etc.)

- docker container stats

  Shows container resource usage

- docker container run -it

  -t pseudo-tty
  simulates a real terminal, like what SSH does

## Getting a Shell Inside Containers

- docker container run -it

  Start new container interactively

- docker container exec -it

  Run Additional command in existing container

* Notes about Different Linux Distributions

  Alpine does not have bash installed, just sh.

## Docker Networks Concepts for private and public Comms in containers

-p (--publish) to assign port
it is always HOST:CONTAINER format

docker run --name nginx -p 8080:80 nginx

docker container inspect --format "{{ .NetworkSettings.IPAddress }}" nginx

- docker container port CONTAINER

  Quick port check

## Docker Networks: CLI Management

- docker network ls

  Shows networks

- docker network inspect

  Inspect a network

- docker network create --driver

  Create a network

- docker network connect

  Attach a network to container

- docker network disconnect

  Detach a network from container
