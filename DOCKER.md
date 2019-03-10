# Docker
&nbsp;
## Setup
```
Brew install bash-completion
```
&nbsp;
## Logs
```
Docker container logs container_name
```
&nbsp;
## Containers
Run a container
```
docker container run --publish 80:80 nginx
```
&nbsp;
Run a container with custom settings
```
docker container run --publish 8080:80 --name my_container -d nginx:1.11 nginx -T
```
&nbsp;
Specify a name for the container
```
docker container run --publish 80:80 —name container_name nginx
```
&nbsp;
Run in the background
```
docker container run --publish 80:80 —detach (or -d) —name container_name nginx
```
&nbsp;
Stop the container
```
docker container stop “first 3 digits of the container id”
```
&nbsp;
List active containers
```
docker container ls
docker container ls -a
```
&nbsp;
Display container status
```
docker container top "container name"
```&nbsp;

Remove a container
```
docker container rm "first 3 digits"
```
&nbsp;
Force remove
```
docker container rm -f "first 3 digits"
```
&nbsp;
Show details of one container config
```
docker container inspect "container name"
```
&nbsp;
Performance stats for all containers
```
docker container stats "container name"
```
&nbsp;
Download an image
```
docker pull "image name"
```
&nbsp;
Check port
```
docker container port "container name"
```
&nbsp;
#### Networks
List Networks
```
docker network ls
```
&nbsp;
Inspect Network
```
docker network inspect
```
&nbsp;
Create a network
```
docker network create --driver
```
&nbsp;
Attach a network to container
```
docker network connect
```
&nbsp;
DNS Round Robin Test
```
docker container run -d --net <network name> --net-alias <network alias name> elasticsearch:2
```
&nbsp;
## Images
List images
```
docker image ls
```
&nbsp;  
Build an image
```
docker image build -t custom_nginx .
```
&nbsp;
Inspect an image
```
docker image inspect <image name>
```
&nbsp;  
#### Mysql
```
docker container run -d -p 3606:3306 --name mysql -e MYSQL_RANDOM_ROOT_PASSWORD=yes mysql
```
&nbsp;
#### Apache
```
docker container run -d --name webserver -p 8080:80 httpd
```
&nbsp;
## Ports
nginx: 80:80
&nbsp;
httpd: 8080:80
&nbsp;
mysql: 3306:3306
