# Build 3 Nodes Hadoop Cluster
###1. create directory to save your container
```
mkdir bigdata
cd bigdata
```
###2. build hadoop cluster image
```
sudo docker pull joway/hadoop-cluster
git clone https://github.com/joway/hadoop-cluster-docker
```
###3. build bridge for hadoop network
```
sudo docker network create --driver=bridge hadoop
```
###4. start container
```
cd hadoop-cluster-docker
sudo ./start-container.sh
```
###5. start hadoop in container
```
./start-hadoop.sh
```
