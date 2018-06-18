## Original fil
[Docker for beginners](https://docker-curriculum.com)

Used: Docker version 1.13.1, build 584d391/1.13.1

## Useful commands

```bash
docker --version

# Hello from Docker.
docker run hello-world 

# download the busybox image
docker pull busybox

# a list of all images on your system
docker images

# shows you all containers that are currently running
docker ps

# a list of all containers that we ran
docker ps -a

# run a Docker container based on this image
docker run busybox

# ran the echo command in our busybox container and then exited it.
docker run busybox echo "hello from busybox"

# Running the run command with the -it flags attaches us to an interactive tty
# in the container
docker run -it busybox sh

# automatically deletes the container once it's exited from
docker run --rm busybox echo "hello from busybox"

# deletes all containers that have a status of exited
# -q flag, only returns the numeric IDs
# -f filters output based on conditions provided
docker rm $(docker ps -a -q -f status=exited)
# or double sudo
sudo docker rm $(sudo docker ps -a -q -f status=exited)

# delete images that you no longer need by running
docker rmi #<id>
```
