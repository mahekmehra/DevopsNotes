# DOCKER COMMANDS CHEAT SHEET (WITH USES)

1. BASIC COMMANDS

---

docker --version
→ Shows installed Docker version.

docker info
→ Displays detailed system-wide Docker information (containers, images, storage driver, etc.).

docker history <image>
→ Shows history of an image (layers and commands used).

docker pull <image>
→ Downloads image from Docker Hub.

docker images
→ Lists all downloaded Docker images.

2. RUNNING CONTAINERS

---

docker run <image>
→ Creates and starts a container.

docker run -it <image>
→ Runs container in interactive mode.

docker run -d <image>
→ Runs container in background (detached mode).

docker run --name <name> <image>
→ Assigns a custom name to container.

docker run --rm <image>
→ Automatically removes container after it stops.

docker run -p <host_port>:<container_port> <image>
→ Maps ports (makes container accessible externally).

docker run -e VAR=value <image>
→ Sets environment variable inside container.

docker run -v <host_path>:<container_path> <image>
→ Mounts volume (host ↔ container).

3. CONTAINER MANAGEMENT

---

docker ps
→ Shows running containers.

docker ps -a
→ Shows all containers (running + stopped).

docker start <container>
→ Starts stopped container.

docker stop <container>
→ Stops running container.

docker restart <container>
→ Restarts container.

docker pause <container>
→ Pauses container.

docker unpause <container>
→ Resumes container.

docker kill <container>
→ Force stops container.

docker rm <container>
→ Deletes container.

docker container prune
→ Removes all stopped containers.

4. EXECUTION & INTERACTION

---

docker exec -it <container> bash
→ Opens terminal inside container.

docker exec -it <container> <command>
→ Runs command inside container.

docker attach <container>
→ Attach to running container.

docker logs <container>
→ Shows logs.

docker logs -f <container>
→ Shows logs in real-time.

5. COPY FILES

---

docker cp <container>:<path> <host_path>
→ Copy from container to host.

docker cp <host_path> <container>:<path>
→ Copy from host to container.

6. IMAGE MANAGEMENT

---

docker rmi <image>
→ Deletes image.

docker rmi -f <image>
→ Force deletes image.

7. VOLUME COMMANDS

---

docker volume create <name>
→ Creates volume.

docker volume ls
→ Lists volumes.

docker volume inspect <name>
→ Shows volume details.

docker volume rm <name>
→ Deletes volume.

docker volume prune
→ Deletes unused volumes.

docker run -v <volume>:<container_path> <image>
→ Mount volume into container.

8. NETWORK COMMANDS

---

docker network ls
→ Lists networks.

docker network inspect <network>
→ Shows network details.

docker network create <name>
→ Creates network.

docker run --network <network> <image>
→ Runs container in specific network.

9. BUILDING IMAGES

---

docker build -t <name>:<tag> .
→ Builds image from Dockerfile.

docker run -d -p <port>:<port> --name <name> <image>
→ Runs built image.

10. USEFUL EXAMPLES

---

Run nginx:
docker run -d -p 8080:80 nginx

Run MySQL:
docker run -d -p 3307:3306 -e MYSQL_ROOT_PASSWORD=root mysql:8

Run with environment variables:
docker run -e APP_ENV=production nginx

Run with volume:
docker run -v mydata:/app/data ubuntu

11. IMPORTANT FLAGS

---

-it → Interactive terminal
-d  → Detached mode
-p  → Port mapping
-e  → Environment variable
-v  → Volume mount
--name → Container name
--rm → Auto remove


