# Docker
## Setup
```
Brew install bash-completion
```
## Logs
```
Docker container logs container_name
```
## Containers
Run a container
```
docker container run --publish 80:80 nginx
```

Run a container with custom settings
```
docker container run --publish 8080:80 --name my_container -d nginx:1.11 nginx -T
```

Specify a name for the container
```
docker container run --publish 80:80 —name container_name nginx
```

Run in the background
```
docker container run --publish 80:80 —detach (or -d) —name container_name nginx
```

Stop the container
```
docker container stop “first 3 digits of the container id”
```

List active containers
```
docker container ls
docker container ls -a
```

Display container status
```
docker container top "container name"
```

Remove a container
```
docker container rm "first 3 digits"
```

Force remove
```
docker container rm -f "first 3 digits"
```

Show details of one container config
```
docker container inspect "container name"
```

Performance stats for all containers
```
docker container stats "container name"
```

Download an image
```
docker pull "image name"
```

Check port
```
docker container port "container name"
```

#### Networks
List Networks
```
docker network ls
```

Inspect Network
```
docker network inspect
```

Create a network
```
docker network create --driver
```
Attach a network to container
```
docker network connect
```
DNS Round Robin Test
```
docker container run -d --net <network name> --net-alias <network alias name> elasticsearch:2
```
## Images
List images
```
docker image ls
```
Build an image
```
docker image build -t custom_nginx .
```

Inspect an image
```
docker image inspect <image name>
```
#### Mysql
```
docker container run -d -p 3606:3306 --name mysql -e MYSQL_RANDOM_ROOT_PASSWORD=yes mysql
```

#### Apache
```
docker container run -d --name webserver -p 8080:80 httpd
```
## Ports
nginx: 80:80
httpd: 8080:80
mysql: 3306:3306
