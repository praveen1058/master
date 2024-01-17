## INSTALL DOCKER
A very detailed instructions to install Docker are provide in the below link

https://docs.docker.com/get-docker/

For Demo-
sudo apt update
#for update the system

sudo apt install docker.io -y
#for install the docker

sudo systemctl status docker
#for check status of docker service
sudo systemctl start docker
#to start the service

sudo usermod -aG docker ubuntu
#add docker user to ubuntu group (docker demon run as root permission)
## Docker Demon run as root why ??
By default, the Docker daemon (dockerd) runs with elevated privileges, often as the root user. This is because Docker requires certain permissions to interact with the host system's kernel features, such as namespaces and control groups, which are crucial for creating and managing containers. \n

docker run hello-world
#check docker is working