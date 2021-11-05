# Project 3  

## Investigate available mounts  
### For the two engines of your choice (of which Docker can be one choice) state:  
- the mount type(s) available & how to use the mount type(s) for the container  
: Docker - Bind Mounts, Volume, tmpfs mount, read-only Bind Mount  

```
Bind Mount 
$ docker run -d \ it \ --name name \ mount type=bind,source=/hostfolder,target=/containerfolder\ bindname
$ docker inspect containername
```  
```
Volume Mount 
$ docker volume create newvolume
```  
```
tmpfs Mount 
$ docker run -d \-it \--name tmptest \--mount type=tmpfs,destination=/app \nginx:latest
```  
- LXC  
:LXC - Bind Mount
```
Bind Mount
$ lxc.mount.entry = /path/to/folder/on/host /path/to/mount/point none bind 0 0
or
$ lxc config device add <container name> <name> disk source=<root path> path=<end path>
```  

## Investigate building images for the container engine  
###  For the two container engines of your choice (of which Docker can be one choice) state  
###  build an image (the command) & Write to file  

- Docker : 
```
********* Install Required Packages
$npm install express-generator -g

********* Install dependencies
$ npm install
$ npm start

// create a file with the dockerfile name & .dockerignore
$ touch Dockerfile
$ touch .dockerignore

********* Build Architecture
# Filename: Dockerfile 
FROM node:10-alpine
WORKDIR /usr/src/app
COPY package*.json ./
RUN npm install
COPY . .
EXPOSE (Port Number)
CMD ["npm", "start"]

********* Now Build Image
$ docker build .


```  

- LXC    : 
```
********* Create a base container
$ sudo apt install debootstrap

********* Create Debian with debootstrap
$ mkdir /tmp/sid-lxd
$ sudo debootstrap sid /tmp/sid-lxd

********* Create a metadata file (metadata.yaml )to describe things like name, date, architecture, then create a tarball from this file  
$ tar -cvzf metadata.tar.gz metadata.yaml

********* Now Build An Image
$ lxc image import metadata.tar.gz --alias sid-nodejs

********* Create your new container from this image
$ lxc launch sid-nodejs 

********* The architechture is contained in the metadata.yaml
architecture: x86_64
creation_date: 1424284563
properties:
  description: Ubuntu 18.04 LTS Intel 64bit
  os: Ubuntu
  release: bionic 18.04
templates:
  /etc/hosts:
    when:
      - create
      - rename
    template: hosts.tpl
    properties:
      foo: bar
  /etc/hostname:
    when:
      - start
    template: hostname.tpl
  /etc/network/interfaces:
    when:
      - create
    template: interfaces.tpl
    create_only: true
```  


