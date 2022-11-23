# Docker
Docker is an open source platform that enables developers to build, deploy, run, update and manage containers—standardized, executable components that combine application source code with the operating system (OS) libraries and dependencies required to run that code in any environment.

The container is a sandboxed process (an isolated testing environment that enables users to run programs or open files without affecting the application, system or platform on which they run) on a machine that is isolated from all other process on the host machine.

- **Container Image**
When running container, it uses a isolated filessystem. This custom filesystem is provided by container image. since the image contain the container filesystem, it must contain everything needed to run an application. ie all dependencies, configuration, scripts, binaries etc. The image also contain other configuration for a container such as environment variable, a default command to run and ither metadata.  


Installation and practice

    sudo apt-get update
<br>
    
    sudo apt-get install -y docker.io
<br>
      
    docker -v
<br>

    sudo docker info
<br>
start the docker daemon

    sudo service docker start
<br>
For docker images

    sudo docker images
<br>
For docker Container details

    sudo docker ps -a
<br>
To stop or delete container

    sudo docker stop container_id
    sudo docker rm container_id
    
<br>
It will pull the hello-world image and if it is not there, then run the container.

    sudo docker run hello-world
<br>
It will pull the latest images of docker container and lunch the container. The if we do ls then we find out that we are inside the ununtu os running on a docker container.

    sudo docker run -it ubuntu
<br>

    history
    
- **Docker run**

Docker run command is used to do following things: 
  - Create a new container if it does not exist 
  - Run a newly created or previously created container from the image provided 
  
You need to have an image first in order to run this command. If you do not have an image it does following things: 
  - Try to find docker image locally 
  - If image is not found it tries to find image on Docker hub 
  - If it finds the image it downloads it store in the image cache 
  - Creates a container from the downloaded or local image 
  - If image can not be found on local or on docker hub it gives you no error and does nothing
  
 # Map a Host port to a Container Port
 The Container port 80 can be access on port 8001 on host machine.
  
    sudo docker run -i -d -t -p 8001:80 nginx
   
