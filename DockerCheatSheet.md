#Build an Image from a Dockerfile
docker build -t <image_name>

#Build an Image from a Dockerfile without the cache
docker build -t <image_name> . –no-cache

#List local images
docker images

#Delete an Image
docker rmi <image_name>

#Remove all unused images
docker image prune 

#Login into Docker
docker login -u <username>

#Publish an image to Docker Hub
docker push <username>/<image_name>

#Search Hub for an image
docker search <image_name>

#Pull an image from a Docker Hub
docker pull <image_name>
  
#Start the docker daemon
docker -d

#Get help with Docker. Can also use –help on all subcommands
docker --help

#Display system-wide information
docker info
  
#Create and run a container from an image, with a custom name:
docker run --name <container_name> <image_name>

#Run a container with and publish a container’s port(s) to the host.
docker run -p <host_port>:<container_port> <image_name>

#Run a container in the background
docker run -d <image_name>

#Start or stop an existing container:
docker start|stop <container_name> (or <container-id>)

#Remove a stopped container:
docker rm <container_name>

#Open a shell inside a running container:
docker exec -it <container_name> sh

#Fetch and follow the logs of a container:
docker logs -f <container_name>

#To inspect a running container:
docker inspect <container_name> (or <container_id>)

#To list currently running containers:
docker ps

#List all docker containers (running and stopped):
docker ps --all

#View resource usage stats
docker container stats
  
  
