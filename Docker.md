# Docker
Docker is an open source containerization platform. It enables developers to package applications into containers—standardized executable components combining application source code with the operating system (OS) libraries and dependencies required to run that code in any environment. Containers simplify delivery of distributed applications, and have become increasingly popular as organizations shift to cloud-native development and hybrid multicloud environments ([source](https://www.ibm.com/cloud/learn/docker)).

### Start and run the containers in the background
```
$ docker compose up -d
```
If you update docker-compose.yml, an image or a Dockerfile, running this command again will pick up the changes automatically.

### Restart the containers
```
$ docker compose restart
```
Useful when some changes require a process to restart, e.g. restart Nginx to pick up some server configuration changes.

### List the containers
```
$ docker compose ps
```

### Tail the containers' logs
```
$ docker compose logs [service]
```
Replace [service] with a service name (e.g. nginx) to display this service's logs only.

### Stop the containers
```
$ docker compose stop
```

### Stop and/or destroy the containers
```
$ docker compose down
```

### Stop and/or destroy the containers and their volumes (including named volumes)
```
$ docker compose down -v
```

### Delete everything, including images and orphan containers
```
$ docker compose down -v --rmi all --remove-orphans
```
Orphan containers are left behind containers that used to match a Docker Compose service but are now not connected to anything, which sometimes happens while you're building your Docker setup.

### Credit
All of this comes from the excellent article series by Yannick at [https://tech.osteel.me/posts/docker-for-local-web-development-part-1-a-basic-lemp-stack](https://tech.osteel.me/posts/docker-for-local-web-development-part-1-a-basic-lemp-stack). Please do check his blog out - it's fantastic.
