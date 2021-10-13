# Container Technologies  

- Docker  ![img](https://www.docker.com/blog/wp-content/uploads/2013/11/homepage-docker-logo.png)  

- ContainerD  ![img](https://i1.wp.com/www.docker.com/blog/wp-content/uploads/3a660141-cb0c-426b-9b6b-cec7b8a2f548-1.jpg?resize=389%2C117&ssl=1)  

## How To Install?  

- Docker : 
1. ```sudo apt update```  
2. ```sudo apt install apt-transport-https ca-certificates curl software-properties-common```  
3. ```curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -```  
4. ```sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu bionic stable"```  
5. ```sudo apt update```  
6. ```apt-cache policy docker-ce```  
7. ```sudo apt install docker-ce```  

- ContainerD : 
1. ```sudo apt update``` 
2. ```sudo apt-get install -y containerd```
3. ```unzip v1.5.7.zip```

##  Pulling A Container Image  

- Docker : ```docker pull redis```  

- ContainerD : ```ctr image pull docker.io/library/redis:alpine```  

## Running A Container

### Initializing versus running the container, and why there is a difference

### Run and enter shell

### Run in detached mode


##  Logs & Status

- Docker : ```docker ps```  

- ContainerD : ```ctr task ls```  

## Stopping A Container

- Docker : ```docker stop containerName```  

- ContainerD : ```ctr task kill containerName```  

