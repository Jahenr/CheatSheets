# Docker Cheatsheet

## Docker CLI

### Basic Commands
- `docker version`: Display the Docker version information
- `docker info`: Display system-wide information
- `docker container ls`: List running containers
- `docker container ls -a`: List all containers (running and stopped)
- `docker container stop <container-id>`: Stop a running container
- `docker container rm <container-id>`: Remove a stopped container
- `docker image ls`: List available images
- `docker image rm <image-id>`: Remove an image

### Working with Containers
- `docker container run <image-name>`: Create and start a new container from an image
- `docker container run -it <image-name> <command>`: Start a new container interactively
- `docker container exec -it <container-id> <command>`: Run a command in a running container
- `docker container cp <container-id>:<src-path> <dest-path>`: Copy files from the container
- `docker container cp <src-path> <container-id>:<dest-path>`: Copy files to the container


### Working with Images
- `docker image build -t <image-name> <path>`: Build an image from a Dockerfile
- `docker image pull <image-name>`: Pull an image from a registry
- `docker image push <image-name>`: Push an image to a registry

### Docker Compose
- `docker-compose up`: Create and start containers defined in the `docker-compose.yml` file
- `docker-compose down`: Stop and remove containers, networks, and volumes
- `docker-compose ps`: List running containers
- `docker-compose logs`: View output logs from containers

### Some Examples
- `docker run -v volume:/data/db -p 27017:27017 mongo`
- `docker exec -it my-redis /bin/bash`
- `docker run --name my-redis -d -p 6379:6379 redis `
- `docker exec -it container_id /bin/bash`: Go inside the container

## Dockerfile

### Basic Instructions
- `FROM <image>`: Specify the base image
- `WORKDIR <path>`: Set the working directory
- `COPY <src> <dest>`: Copy files or directories to the container
- `RUN <command>`: Execute commands during the build
- `ENV <key>=<value>`: Set environment variables
- `EXPOSE <port>`: Expose a port to the host
- `CMD ["<executable>", "<param1>", "<param2>"]`: Set the default command to run when the container starts
- `ENTRYPOINT ["<executable>", "<param1>", "<param2>"]`: Set the executable to be run when the container starts

### Best Practices
- Use a minimal base image
- Leverage build cache with `--cache-from` flag
- Use multi-stage builds for optimized images
- Lint your Dockerfile with tools like `hadolint`
- Use `.dockerignore` to exclude unnecessary files from the build context