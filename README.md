# Build 3 Nodes Hadoop Cluster

***1. create directory to save your container***
```
mkdir bigdata
cd bigdata
```
***2. build hadoop cluster image***
```
sudo docker pull joway/hadoop-cluster
git clone https://github.com/joway/hadoop-cluster-docker
```
***3. build bridge for hadoop network***
```
sudo docker network create --driver=bridge hadoop
```
***4. start container***
```
cd hadoop-cluster-docker
sudo ./start-container.sh
```
***5. start hadoop in container***
```
./start-hadoop.sh
```


# cheatsheet for docker

***1. manage container***
$ docker ps # list all running containers
   -a # list all containers
   -q # list all containers id

$ docker run [params] image_name exec_command # run containers then exec_commond
   -i # keep stdin opended
   -t # distribute VT to container, it will enter VT automatically
   -d # container runs in the background
   -name # name
   -rm # delete container after exit
e.g. docker run -it ubuntu:14.04

$ docker rm # delete container
$ docker rm container_id 
$ docker rm container_id -f
$ docker stop contaner_id
$ docker start container_id
