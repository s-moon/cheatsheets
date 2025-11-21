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

### Create an image
```
$ docker image build -t logicalmoon/gsd:ctr2023 .
```
* logicalmoon is the docker hub a/c. 
* gsd is the name of the repository.
* ctr2023 is the tag name.
* . is the current directory

### Building multi architecture images
```
$ docker buildx build --platform linux/arm64/v8,linux/amd64 --push --tag logicalmoon/gsd:ctr2023 .
```
Note: won't work on Mac

### Listing images
```
$ docker image ls
```

### Delete image
```
$ docker image rm logicalmoon/gsd:ctr2023
```

### Start a container
```
$ docker container run -d --name web -p 8000:8080 logicalmoon/gsd:ctr2023 
```
* 8000 is the external port
* 8080 is the internal port
* web is the name given for this container
* -d run detached from the terminal

### Listing containers
```
$ docker container ls
```
Use -a if you want to see all containers, including stopping ones

### Stop the container
```
$ docker container stop web
```

### Start the container (other way)
```
$ docker container start web
```

### Pushing to the registry
```
$ docker image push logicalmoon/gsd:ctr2023
```

### Credit
Some of this comes from the excellent article series by Yannick at [https://tech.osteel.me/posts/docker-for-local-web-development-part-1-a-basic-lemp-stack](https://tech.osteel.me/posts/docker-for-local-web-development-part-1-a-basic-lemp-stack). Please do check his blog out - it's fantastic. The rest comes from a Pluralsight course by Nigel Poulter (also excellent).
