**Essential Docker Commands for DevOps Engineers**
Docker has revolutionized the way we build, ship, and run applications. As a DevOps engineer, mastering Docker commands is essential for efficient container management, deployment, and troubleshooting. This post will cover the fundamental Docker commands you need to streamline your workflows and enhance productivity.
 
**1. Building Docker Images**
Building images is a core part of the Docker workflow. Here’s how to do it:
docker build -t <image-name>:<tag> <path>
•	-t: Tags the image with a name and optional tag (default latest).
•	<path>: Path to the directory containing the Dockerfile.
Example:
docker build -t myapp:v1 .
 
**2. Running Containers**
Running containers from images is the next step.
docker run -d -p <host-port>:<container-port> --name <container-name> <image-name>
•	-d: Runs the container in detached mode (in the background).
•	-p: Maps ports between the host and the container.
•	--name: Assigns a name to the container.
Example:
docker run -d -p 5000:80 --name webserver nginx
 
**3. Listing Docker Containers**
To list running containers:
docker ps
To list all containers (including stopped ones):
docker ps -a
 
**4. Stopping and Removing Containers**
Stop a running container:
docker stop <container-name>
Remove a stopped container:
docker rm <container-name>
Example:
docker stop webserver
docker rm webserver
 
**5. Viewing Logs**
Access container logs for troubleshooting:
docker logs <container-name>
 
**6. Interacting with a Running Container**
To access the terminal of a running container:
docker exec -it <container-name> /bin/bash
•	-it: Interactive mode with a TTY.
Example:
docker exec -it webserver /bin/bash
 
**7. Removing Docker Images**
To remove an image:
docker rmi <image-name>
Force remove (if in use):
docker rmi -f <image-name>
 
**8. Pruning Unused Resources**
Clean up unused containers, networks, and images:
docker system prune
Add -a to remove all unused images:
docker system prune -a
 
**9. Saving and Loading Docker Images**
Save an image to a tar file:
docker save -o <file-name>.tar <image-name>
Load an image from a tar file:
docker load -i <file-name>.tar
 
**10. Docker Compose**
Run multi-container applications using Docker Compose:
docker-compose up -d
Stop Compose services:
docker-compose down
 
**Final Thoughts**
Mastering these Docker commands will significantly enhance your ability to manage containerized environments. As DevOps practices continue to evolve, Docker remains at the heart of CI/CD pipelines, microservices, and cloud deployments.
