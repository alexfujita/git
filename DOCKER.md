# Docker
<br>
## Setup
```
Brew install bash-completion
```
<br>
## Logs
```
Docker container logs container_name
```
<br>
## Containers
Run a container
```
docker container run --publish 80:80 nginx
```
<br>
Run a container with custom settings
```
docker container run --publish 8080:80 --name my_container -d nginx:1.11 nginx -T
```
<br>
Specify a name for the container
```
docker container run --publish 80:80 —name container_name nginx
```
<br>
Run in the background
```
docker container run --publish 80:80 —detach (or -d) —name container_name nginx
```
<br>
Stop the container
```
docker container stop “first 3 digits of the container id”
```
<br>
List active containers
```
docker container ls
docker container ls -a
```
<br>
Display container status
```
docker container top "container name"
```
<br>
Remove a container
```
docker container rm "first 3 digits"
```
<br>
Force remove
```
docker container rm -f "first 3 digits"
```
<br>
Show details of one container config
```
docker container inspect "container name"
```
<br>
Performance stats for all containers
```
docker container stats "container name"
```
<br>
Download an image
```
docker pull "image name"
```
<br>
Check port
```
docker container port "container name"
```
<br>
#### Networks
List Networks
```
docker network ls
```
<br>
Inspect Network
```
docker network inspect
```
<br>
Create a network
```
docker network create --driver
```
<br>

Attach a network to container
```
docker network connect
```
<br>
DNS Round Robin Test
```
docker container run -d --net <network name> --net-alias <network alias name> elasticsearch:2
```
<br>
## Images
List images
```
docker image ls
```
<br>
Build an image
```
docker image build -t custom_nginx .
```
<br>
Inspect an image
```
docker image inspect <image name>
```
<br>


#### Mysql
```
docker container run -d -p 3606:3306 --name mysql -e MYSQL_RANDOM_ROOT_PASSWORD=yes mysql
```
<br>
#### Apache
```
docker container run -d --name webserver -p 8080:80 httpd
```
<br>

## Ports
nginx: 80:80
httpd: 8080:80
mysql: 3306:3306
