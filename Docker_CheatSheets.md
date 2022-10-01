# Docker Info
## Check if Docker running
$ docker info
Client:
 Context:    default
 Debug Mode: false
 Plugins: ...
Server: ...
 Operating System: Docker Desktop
 OSType: linux
 Architecture: x86_64 ...

# Docker Version
$ docker version
Client:
 Cloud integration: v1.0.24
 Version:           20.10.17 ...
Server: Docker Desktop 4.10.1 (82475)
 Engine:
  Version:          20.10.17 ...
  
# Docker Container Registry
Docker Hub: https://hub.docker.com/
Google Container Registry: https:///cloud.google.com/container-registry/
AWS Elastic Container Registry: https://aws.amazon.com/id/ecr/

# List Images on Docker
$ docker images

# Download Image from Docker Hub
$ docker pull [image-name]:[image-version]
$ docker pull cygnus7/app-golang:1.0

# List Running Container on Docker
$ docker container ls

# List All Container on Docker
$ docker container ls --all

# Create Container
$ docker container create --name [container-name] [image-name]:[image-version]

# Run Container on Docker
$ docker container start [container-name]

# Stop Container on Docker
$ docker container stop [container-name]

# Delete Container
## Must stop the container first
$ docker container rm [container-name]

# Expose Port for Container
$ docker container create --name [container-name] -p [exposed-port]:[container:port] [image-name]:[image-version]
$ docker container create --name mongoserver1 -p 8080:27017 mongo:4.1

# Delete Image
## Must delete container that use the image
$ docker image rm [image-name]:[image-version]

# Create Dockerfile
## Create file with name "Dockerfile"

# Build Docker image from Dockerfile
$ docker build --tag [image-name]:[image-version] [directory-of-Dockerfile]
$ docker build --tag app-golang:1.0 .

# Login to Dockerhub
$ docker Login

# Push Image to Registry / Dockerhub
## Change tag first from local-tag to repo-tag
$ docker tag [local-tag] [repo-tag]
$ docker tag app-golang:1.0 cygnus7/app-golang:1.0
$ docker push [image-name]:[image-tag]
$ docker push cygnus7/app-golang:1.0

# Docker Network
$ docker network create [network-name]
$ docker network connect [network-name] [container-name]

# Docker Compose
## Create file with name "docker-compose.yml"
$ docker-compose up -d
$ docker-compose down
$ docker-compose start
$ docker-compose stop

# Docker Volume
$ docker volume create [volume-name]

# Login to Docker Container
$ docker exec -ti [container-name] [command]
$ docker exec -ti redis /bin/bash

# Kitematic
## Legacy Desktop Version of Docker Desktop
Download from "https://github.com/docker/kitematic/releases"

# Remove Docker Garbage
$ docker image prune
$ docker container prune
$ docker network prune
## Clear all mentioned above
$ docker system prune
$ docker system prune -a --volumes
WARNING! This will remove:
  - all stopped containers
  - all networks not used by at least one container
  - all volumes not used by at least one container
  - all images without at least one container associated to them
  - all build cache

# Check Reclaimable Space
$ docker system df
