# Container Technologies  

- Docker  
- ContainerD

## How To Install?  

- Docker : 
![img](https://www.docker.com/blog/wp-content/uploads/2013/11/homepage-docker-logo.png)
- ContainerD : 
![img](https://i1.wp.com/www.docker.com/blog/wp-content/uploads/3a660141-cb0c-426b-9b6b-cec7b8a2f548-1.jpg?resize=389%2C117&ssl=1)
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

