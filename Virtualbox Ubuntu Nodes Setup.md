**Virtualbox Ubuntu Nodes Setup**

Network:

Change to "**Bridge Adapter**", Select "**En0 WIFI**"

```
Sudo apt-get upgrade
sudo apt-get purge openssh-server
sudo apt-get install openssh-server
```

SSH from Mac and install docker.io

```
ssh hua@10.0.0.77
sudo apt install docker // ?? Maybe not
sudo apt install docker.io

systemctl start docker
systemctl enable docker // load on startup
systemctl stop docker
```

Yum: 

The `yum` package manager comes from RedHat and its derivatives. It installs rpm packages from repositories that store such packages. The Debian (and by extension, Ubuntu) repositories have .deb packages instead.

```
Sudo apt install yum
sudo apt install yum-utils
```

Docker Steps:

```
docker search tomcat
docker pull tomcat:latest
sudo docker run --name mytomcat -d 33e02377a00f //deamond
docker stop CONTAINER_ID
docker rm CONTAINER_ID
docker run --name mytomcat -p  8888:8080 tomcat
-p: port mapping -> HOST_PORT:CONTAINER_PORT
docker logs CONTAINER_ID
```

Run Mysql

```
sudo docker run -p 3306:3306 --name mysql -e MYSQL_ROOT_PASSWORD=root -d mysql
```

