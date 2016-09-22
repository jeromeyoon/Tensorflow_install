# Tensorflow_install(Ubuntu 14.04+Titan X+CUDA7.5)

## Install Essential(NVIDIA Driver &CUDA)
 - Step1. Install Ubuntu 14.04
 - Step2. sudo apt-get update && sudo apt-get install build-essential
 - Step3. Install Nvidia driver(http://askubuntu.com/questions/451221/how-do-i-install-the-nvidia-driver-for-a-geforce-gt-630)
 - If you want to use docker, skip to Install Tensorflow Via docker
 - Step4. Install CUDA
 - Step5. Edit ~/.bashrc file and add following two lines
 	* export PATH=/usr/local/cuda/bin:$PATH
 	* export LD_LIBRARY_PATH=/usr/local/cuda/lib64:$LD_LIBRARY_PATH
 - Step6. Install Cudnn
 - Step7. apt-cache policy libcudnn5 (To verify installed Cudnn)
 
## Install Tensorflow Via Docker
**Using nvidia-docker, DO not need to install, CUDA  and Cudnn** 
 - Step1. Install docker: https://docs.docker.com/engine/installation/
 - Step2. Install nvidia-docker: https://github.com/NVIDIA/nvidia-docker
 - Step3. Install tensorflow docker: https://www.tensorflow.org/versions/r0.10/get_started/os_setup.html#docker-installation 
 - More Tensorflow docker tags: https://hub.docker.com/r/tensorflow/tensorflow/tags/

## Docker manual
 - http://pyrasis.com/Docker/Docker-HOWTO (Koean)
 - http://www.slideshare.net/pyrasis/docker-fordummies-44424016 (Korean)
 - http://m.blog.naver.com/alice_k106/220340499760 (Korean)
 
## Docker essential commands  
 - sudo nvidia-docker commit ID dockername:Tags : After modifying something in a docker image, making a new docker image's tag
 - sudo nvidia-docker run docker_imagename:Tags /bin/bash: run nvidia-docker
 - sudo docker ps -a: See all containers ID 
 - Remove container: sudo docker rm ContainerID
 - sudo docker images: See all Image list
 - Remove Images: sudo docker rmi Imagename:Tags
 - Push Image to dockerhub: sudo docker push Imagename:Tags (For first time login required,like github)
 
## Docker adduser 
 - Run docker 
 - Write: groupadd -r groupname -g 1000 && useradd -u 1000 -r -g username -d <home/dir> -s /sbin/nologin -c "Docker image user" yjyoon && chown -R useradd:groupname <home/dir>

## Install Ubuntu mate 
 http://wincloud.link/pages/viewpage.action?pageId=9175071
 
  
 

