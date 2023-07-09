# Docker commands :- 
1. **docker run**: This command is used to run a container from an image.
   **docker run <image_name>**
   ![image](https://github.com/Manoj123-github/Docker/assets/76830665/f2420612-ebdf-4ed5-bd63-46b14d605244)

2. **docker pull:** This command allows you to pull any image which is present at the official registry of docker, Docker hub. By default, it pulls the latest image, but you can also mention the version of the image.

**docker pull <image_name>**

![image](https://github.com/Manoj123-github/Docker/assets/76830665/bc3d46a2-6e0f-47ff-8888-22eb3a357bef)

3. **docker ps:** This command (by default) shows us a list of all the running containers. We can use various flags with it.

    **-a** flag:  shows us all the containers, stopped or running.
    **-l** flag: shows us the latest container.
    **-q **flag: shows only the Id of the containers. 

 **docker ps [options..]**

 ![image](https://github.com/Manoj123-github/Docker/assets/76830665/74ac4cf5-91ec-4adb-b456-7193e280efcb)

4. Docker Prune : This command allows you to clean up unused images.
   docker image prune

![image](https://github.com/Manoj123-github/Docker/assets/76830665/21ce7c05-6e72-4486-b20e-e9c4a916680c)

**-a **flag :- to remove all images which is not used by existing conatianers.
