# Docker Overview

# Docker official Documentation 
https://docs.docker.com/get-started/ 

# What is a container?
Simply put, a container is a sandboxed process on your machine that is isolated from all other processes on the host machine. That isolation leverages kernel namespaces and cgroups, features that have been in Linux for a long time. Docker has worked to make these capabilities approachable and easy to use. To summarize, a container:

   1. Is a runnable instance of an image. You can create, start, stop, move, or delete a container using the DockerAPI or CLI.
   2. Can be run on local machines, virtual machines or deployed to the cloud.
   3. Is portable (can be run on any OS).
   4. Is isolated from other containers and runs its own software, binaries, and configurations.

in simple word, A container is a bundle of Application, Application libraries required to run your application and the minimum system dependencies.A Docker container image is a lightweight, standalone, executable package of software that includes everything needed to run an application: code, runtime, system tools, system libraries and settings. Additionally, Docker containers are designed to be minimal, only including what is necessary for the application to run, further reducing their size.

![image](https://github.com/Manoj123-github/Docker/assets/76830665/806a994b-f91e-4dda-8e7d-d34e8d8c63ab)

Below is the screenshot of official ubuntu base image which you can use for your container. It's just ~ 22 MB, isn't it very small ? on a contrary if you look at official ubuntu VM image it will be close to ~ 2.3 GB. So the container base image is almost 100 times less than VM image.

![image](https://github.com/Manoj123-github/Docker/assets/76830665/9fca6f41-2164-4b6f-bd8f-f02f456f7189)


![image](https://github.com/Manoj123-github/Docker/assets/76830665/e95144e4-cafd-47c8-9fb8-61005c810ca3)



# What is Docker ?

Docker is a containerization platform that provides easy way to containerize your applications, which means, using Docker you can build container images, run the images to create containers and also push these containers to container regestries such as DockerHub.

In simple words, you can understand as containerization is a concept or technology and Docker Implements Containerization.

Docker is a set of platforms as a service (PaaS) products that use the Operating system level visualization to deliver software in packages called containers. Containers are isolated from one another and bundle their own software, libraries, and configuration files; they can communicate with each other through well-defined channels. All containers are run by a single operating system kernel and therefore use fewer resources than a virtual machine.

# Docker Architecture 

![image](https://github.com/Manoj123-github/Docker/assets/76830665/02d83aa6-2a31-481e-a6a9-c3f8d05d5e54)

# Docker Daemon
Docker daemon manages all the services by communicating with other daemons. It manages docker objects such as images, containers, networks, and volumes with the help of the API requests of Docker.

sudo systemctl start/stop/status docker 

# Docker Client
he docker client, the docker users can interact with the docker. The docker command uses the Docker API. The Docker client can communicate with multiple daemons. When a docker client runs any docker command on the docker terminal then the terminal sends instructions to the daemon. The Docker daemon gets those instructions from the docker client withinside the shape of the command and REST API’s request.

# Docker registries 
All the docker images are stored in the docker registry. There is a public registry which is known as a docker hub that can be used by anyone. We can run our private registry also. With the help of docker run or docker pull commands, we can pull the required images from our configured registry.

# Docker Images
An image contains instructions for creating a docker container. It is just a read-only template. It is used to store and ship applications. 
You might create your own images or you might only use those created by others and published in a registry. To build your own image, you create a Dockerfile with a simple syntax for defining the steps needed to create the image and run it. Each instruction in a Dockerfile creates a layer in the image.

# Dockerfile

Dockerfile is a file where you provide the steps to build your Docker Image.
