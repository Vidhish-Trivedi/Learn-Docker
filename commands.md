# Docker Commands:

| Task                                      | Command                                                |
| ----------------------------------------- | ------------------------------------------------------ |
| Build (Create an image from a Dockerfile) | docker build <path_to_dockerfile>                      |
| Run and publish a port on a local port    | docker run -p <local_port>:<container_port> <image_id> |
| List running processes                    | docker ps                                              |
| List all processes                        | docker ps -a                                           |
| Stop a running container                  | docker stop <container_name>                           |
| Pull an image from docker hub             | docker pull <image_name>                               |
| Run an image from docker hub              | docker run <image_name>                                |
| Run an image interactively                | docker run -it <image_name>                            |
