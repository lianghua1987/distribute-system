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



