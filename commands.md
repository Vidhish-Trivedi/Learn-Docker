# Docker Commands:

-   Running a container in detached mode, similar to running in background.
-   Running a container in attached mode, similar to running in foreground.

| Task                                                                            | Command                                                   |
| ------------------------------------------------------------------------------- | --------------------------------------------------------- |
| Build (Create an image from a Dockerfile)                                       | docker build <path_to_dockerfile>                         |
| Run and publish a port on a local port (Creates a new container, attached mode) | docker run -p <local_port>:<container_port> <image_id>    |
| (Re)start an existing container (detached mode)                                 | docker start <container_name/id>                          |
| (Re)start an existing container (attached mode)                                 | docker start -a <container_name/id>                       |
| (Re)start an existing container (interactive)                                   | docker start -i <container_name/id>                       |
| Run a container in detached mode                                                | docker run -p <local_port>:<container_port> -d <image_id> |
| Attach terminal to a container                                                  | docker attach <container_name/id>                         |
| Run an image as a container interactively                                       | docker run -it <image_name>                               |
| View logs of a detached container (use -f after logs, to follow)                | docker logs <container_name/id>                           |
| List running processes (containers)                                             | docker ps                                                 |
| List all processes (containers)                                                 | docker ps -a                                              |
| Stop a running container                                                        | docker stop <container_name>                              |
| Pull an image from docker hub                                                   | docker pull <image_name>                                  |
| Run an image from docker hub                                                    | docker run <image_name>                                   |
