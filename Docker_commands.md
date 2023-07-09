# Docker commands :- 
1. **docker run**: This command is used to run a container from an image.
   
   **docker run <image_name>**
   ![image](https://github.com/Manoj123-github/Docker/assets/76830665/f2420612-ebdf-4ed5-bd63-46b14d605244)

3. **docker pull:** This command allows you to pull any image which is present at the official registry of docker, Docker hub. By default, it pulls the latest image, but you can also mention the version of the image.

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

6. **docker stop/start** : This command allows you to stop/start a container if it has crashed or you want to switch to another one.

   **docker stop <container_ID>**

7. **docker rm:** To delete a container. By default when we a container is created, it gets an ID as well as an imaginary name such as confident_boyd, heuristic_villani, etc. You can either mention the container name or its ID.

Some important flags:

    **-f flag:** remove the container forcefully.
    
    **-v flag:** remove the volumes.
    
    **-l flag:** remove the specific link mentioned.

** docker rm {options} <container_name or ID> **

8. **docker images:** Lists all the pulled images which are present in our system.

 **docker images**

![image](https://github.com/Manoj123-github/Docker/assets/76830665/05c274d4-0680-4d04-9d54-17517691e19e)


9. **Using Bash**

You can directly access the bash of the Docker Container and execute commands there. It’s very easy to launch the bash of the Container and you can do so using this command.

**sudo docker run -it ubuntu bash **

![image](https://github.com/Manoj123-github/Docker/assets/76830665/ef7bf9a2-7b12-4a9a-ae2c-a46e24c585a1)
