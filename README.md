# Tensorflow_install(Ubuntu 14.04+Titan X+CUDA7.5)

## Install Essential(NVIDIA Driver &CUDA)
 - Step1. Install Ubuntu 14.04
 - Step2. sudo apt-get update && sudo apt-get install build-essential
 - Step3. Install Nvidia driver(http://askubuntu.com/questions/451221/how-do-i-install-the-nvidia-driver-for-a-geforce-gt-630)
 - Step4. Install CUDA
 - Step5. Edit ~/.bashrc file and add following two lines
 	* export PATH=/usr/local/cuda/bin:$PATH
 	* export LD_LIBRARY_PATH=/usr/local/cuda/lib64:$LD_LIBRARY_PATH
 - Step6. Install Cudnn
 
## Install Tensorflow
### Install Docker
**Using nvidia-docker, DO not need to install Nvidia direver, CUDA  and Cudnn** 
 - Step1. Install docker: https://docs.docker.com/engine/installation/
 - Step2. Install nvidia-docker: https://github.com/NVIDIA/nvidia-docker
 - Step3. Run docker: 
 - More Tensorflow docker tags: https://hub.docker.com/r/tensorflow/tensorflow/tags/

## Docker manual
 - http://pyrasis.com/Docker/Docker-HOWTO (Koean)
 - http://m.blog.naver.com/alice_k106/220340499760 (Korean)
 
## Docker simple commands  
 - sudo nvidia-docker ps -a: See all containers ID 
 - sudo nvidia-docker commit ID dockername:Tags : After installing something, Give new tags
 - sudo nvidia-docker run dockername:Tags /bin/bash: run nvidia-docker
 - Container list: sudo docker ps -a
 - Remove container: sudo docker rm ContainerID
 - Image list: sudo docker images
 - Remove Images: sudo docker rmi Imagename:Tags
 - Commit images: sudo docker commit Imagename:newTags
 - Push Image to dockerhub: sudo docker push Imagename:Tags (For first time login required,like github)
 
## Docker adduser 
 - Run docker 
 - Write: groupadd -r groupname -g 1000 && useradd -u 1000 -r -g username -d <home/dir> -s /sbin/nologin -c "Docker image user" yjyoon && chown -R useradd:groupname <home/dir>

## Install Ubuntu mate 
 http://wincloud.link/pages/viewpage.action?pageId=9175071
 
  
 

