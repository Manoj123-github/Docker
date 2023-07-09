# Docker Volumes

# Problem Statement
It is a very common requirement to persist the data in a Docker container beyond the lifetime of the container. However, the file system of a Docker container is deleted/removed when the container dies.

# Solution

There are 2 different ways how docker solves this problem.

   1. Volumes
   2. Bind Directory on a host as a Mount

![image](https://github.com/Manoj123-github/Docker/assets/76830665/1a32757f-a515-4a10-acef-df437e3773fb)



1. Volumes are stored in a part of the host filesystem which is managed by Docker (/var/lib/docker/volumes/ on Linux). Non-Docker processes should not modify this part of the filesystem. Volumes are the best way to persist data in Docker.

2. Bind mounts may be stored anywhere on the host system. They may even be important system files or directories. Non-Docker processes on the Docker host or a Docker container can modify them at any time.

3. tmpfs mounts are stored in the host system’s memory only, and are never written to the host system’s filesystem.

# Volumes

Volumes aims to solve the same problem by providing a way to store data on the host file system, separate from the container's file system, so that the data can persist even if the container is deleted and recreated.

Volumes can be created and managed using the docker volume command. You can create a new volume using the following command:

**docker volume create <volume_name>**

Once a volume is created, you can mount it to a container using the -v or --mount option when running a docker run command.

For example:

**docker run -it -v <volume_name>:/data <image_name> /bin/bash**

This command will mount the volume <volume_name> to the /data directory in the container. Any data written to the /data directory inside the container will be persisted in the volume on the host file system.
 
# Bind Directory on a host as a Mount

Bind mounts also aims to solve the same problem but in a complete different way.

Using this way, user can mount a directory from the host file system into a container. Bind mounts have the same behavior as volumes, but are specified using a host path instead of a volume name.

For example,

**docker run -it -v <host_path>:<container_path> <image_name> /bin/bash**

   
