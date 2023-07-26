# Docker Installation on Ubuntu
# officials Page 
https://docs.docker.com/engine/install/ubuntu/

# Installing Docker Engine Steps :- 
sudo apt-get update
 
$ sudo apt-get install \
    ca-certificates \
    curl \
    gnupg \
    lsb-release

$ sudo mkdir -p /etc/apt/keyrings
$ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg

$ echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
  
$ sudo apt-get update

$ sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin

$ sudo groupadd docker

$ sudo usermod -aG docker $USER


# Check if docker is successfully installed in your system
$ sudo docker run hello-world

![image](https://github.com/Manoj123-github/Docker/assets/76830665/f68aac39-58df-4c65-8faf-cd203ac4941c)
