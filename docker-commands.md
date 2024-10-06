## Docker Commands and Explanations

### Basic Docker Commands

1. **`docker run hello-world`**
   - Runs the `hello-world` Docker image, which is a simple image used to verify that Docker is installed and working correctly.

2. **`docker run -it ubuntu`**
   - Runs an Ubuntu container in interactive mode with a terminal session attached.

3. **`docker run -it -p <outer_machine_port>:<docker_port> <image_name>`**
   - Runs a container in interactive mode, mapping a port from the host machine to the container.

4. **`exit`**
   - Exits the interactive terminal session of a running container.

5. **`docker stop <container_id/container_name>`**
   - Stops a running container.

6. **`docker start <container_id/container_name>`**
   - Starts a stopped container.

7. **`docker container ls`**
   - Lists all running containers.

8. **`docker container ls -a`**
   - Lists all containers, including stopped ones.

9. **`docker images`**
   - Lists all Docker images on the local machine.

10. **`docker exec -it <container_id> bash`**
    - Opens an interactive terminal session inside a running container.

### Docker Image and Container Management

11. **`docker build --no-cache -t story_vol .`**
    - Builds a Docker image named `story_vol` from the Dockerfile in the current directory, without using the cache.

12. **`docker build -t <image_name>`**
    - Builds a Docker image with the specified name from the Dockerfile in the current directory.

13. **`docker login`**
    - Logs into Docker Hub or another Docker registry.

14. **`docker push <image_name>`**
    - Pushes a Docker image to Docker Hub or another Docker registry.

### Docker Compose Commands

15. **`sudo docker compose up`**
    - Starts and runs the services defined in the `docker-compose.yml` file.

16. **`sudo docker compose down`**
    - Stops and removes the containers defined in the `docker-compose.yml` file.

17. **`docker compose up -d`**
    - Starts the services defined in the `docker-compose.yml` file in detached mode (running in the background).

### Docker Network Commands

18. **`docker network inspect bridge`**
    - Inspects the default `bridge` network.

19. **`docker network ls`**
    - Lists all Docker networks.

20. **`docker run -it --network=host busybox`**
    - Runs a `busybox` container using the host network.

21. **`docker run -it --network=none busybox`**
    - Runs a `busybox` container with no network.

22. **`docker network create -d bridge youtube`**
    - Creates a new Docker network named `youtube` using the `bridge` driver.

23. **`docker run -it --network=youtube --name tony_stark ubuntu`**
    - Runs an Ubuntu container named `tony_stark` on the `youtube` network.

24. **`docker run -it --network=youtube --name dr_strange busybox`**
    - Runs a `busybox` container named `dr_strange` on the `youtube` network.

25. **`docker run -it -v /Users/abcuser/Desktop/test-folder:/home/abc ubuntu`**
    - Runs an Ubuntu container with a volume mounted from the host's `test-folder` to the container's `/home/abc` directory.

### Dockerfile Commands

26. **`FROM ubuntu`**
    - Specifies the base image for the Dockerfile.

27. **`RUN apt-get update`**
    - Updates the package list in the container.

28. **`RUN apt-get install -y curl`**
    - Installs `curl` in the container.

29. **`RUN curl -sL https://deb.nodesource.com/setup_18.x | bash -`**
    - Downloads and runs the Node.js setup script.

30. **`RUN apt-get upgrade -y`**
    - Upgrades all installed packages in the container.

31. **`RUN apt-get install -y nodejs`**
    - Installs Node.js in the container.

32. **`WORKDIR /app`**
    - Sets the working directory for the container to `/app`.

33. **`COPY package.json package.json`**
    - Copies `package.json` from the host to the container.

34. **`COPY package-lock.json package-lock.json`**
    - Copies `package-lock.json` from the host to the container.

35. **`RUN npm install`**
    - Installs Node.js dependencies in the container.

36. **`COPY main.js main.js`**
    - Copies `main.js` from the host to the container.

37. **`ENTRYPOINT ["node", "main.js"]`**
    - Specifies the command to run when the container starts.

---
