# Tensorflow_install(Ubuntu 14.04+Titan X)

## Install Essential(NVIDIA Driver &CUDA)
 - Step1. Install Ubuntu 14.04
 - Step2. Install Nvidia driver
 - Step3. Install CUDA
 - Step4. Edit ~/.bashrc file and add following two lines
 	* export PATH=/usr/local/cuda/bin:$PATH
 	* export LD_LIBRARY_PATH=/usr/local/cuda/lib64:$LD_LIBRARY_PATH
 - Step5. Install Cudnn
 - Step6. sudo apt-get update && sudo apt-get install build-essential
 
## Install Tensorflow


