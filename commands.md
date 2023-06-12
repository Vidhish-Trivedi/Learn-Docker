# Docker Commands

-   Running a container in detached mode, similar to running in background.
-   Running a container in attached mode, similar to running in foreground.
-   Below are a few commonly used commands, may also use multiple flags at once.
-   For tagged images, we can use name:tag instead of image_id for tagged images.
-   Official Docker Image Registry - Docker Hub, can share private, public or official images as repositories.

| Task                                                                            | Command                                                               |
| ------------------------------------------------------------------------------- | --------------------------------------------------------------------- |
| Build (Create an image from a Dockerfile)                                       | docker build <path_to_dockerfile>                                     |
| Build (Create an image) and set its tag (name:tag OR repository:tag)            | docker build -t <repo_name:tag> <path_to_dockerfile>                  |
| Run and publish a port on a local port (Creates a new container, attached mode) | docker run -p <local_port>:<container_port> <image_id>                |
| Run as a container, remove on exit                                              | docker run -p <local_port>:<container_port> --rm <image_id>           |
| (Re)start an existing container (detached mode)                                 | docker start <container_name/id>                                      |
| (Re)start an existing container (attached mode)                                 | docker start -a <container_name/id>                                   |
| (Re)start an existing container (interactive)                                   | docker start -i <container_name/id>                                   |
| Run a container in detached mode                                                | docker run -p <local_port>:<container_port> -d <image_id>             |
| Run a container and set its name                                                | docker run --name <name_of_container> <image_id>                      |
| Attach terminal to a container                                                  | docker attach <container_name/id>                                     |
| Run an image as a container interactively                                       | docker run -it <image_name>                                           |
| View logs of a detached container (use -f after logs, to follow)                | docker logs <container_name/id>                                       |
| List running processes (containers)                                             | docker ps                                                             |
| List all processes (containers)                                                 | docker ps -a                                                          |
| Stop a running container                                                        | docker stop <container_name>                                          |
| Pull an image from docker hub                                                   | docker pull <image_name>                                              |
| Pull an image a private registry                                                | docker pull <host:image_name>                                         |
| Push images to docker hub (Alternatively, share Dockerfile with source code)    | docker push <image_name>                                              |
| Push images to a private registry                                               | docker push <host:image_name>                                         |
| Run an image from docker hub                                                    | docker run <image_name>                                               |
| Remove a container (should be stopped first)                                    | docker rm <space_seperated_container_names>                           |
| List all images                                                                 | docker images                                                         |
| Remove an image (all associated containers must be removed first)               | docker rmi <image_id>                                                 |
| Remove all images with no associated containers                                 | docker image prune                                                    |
| Remove all images, including tagged images                                      | docker image prune -a                                                 |
| Copy files to a running container                                               | docker cp <src_path_local> <dest_path_container[container_name:path]> |
| Copy files from a running container                                             | docker cp <src_path_container[container_name:path]> <dest_path_local> |
| Rename/Retag an imgae                                                           | docker tag <old_name> <new_name>                                      |
| Login to docker (one-time)                                                      | docker login                                                          |
| Logout from docker                                                              | docker logout                                                         |
