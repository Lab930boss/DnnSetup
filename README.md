# DnnSetup
This page includes Deep Learning environment setup instruction and other useful projects
This instruction is for linux 16.04 with Nivida GPU

## CUDA setup 
1. Nvidia Graphics driver installation  <br />
  $ sudo add-apt-repository ppa:graphics-drivers/ppa  <br />
  $ sudo apt-get update  <br />
  $ sudo apt-get install nvidia-375  <br />

  After this, reboot 
  $ sudo reboot  <br />
  
  When u type  $ nvidia-smi   , you should see the following message. 
  
![Alt text](https://github.com/Lab930boss/DnnSetup/blob/master/nvidia%20driver%20info.png?raw=true "GPU info") <br />

2. CUDA toolkit installation  <br />
  please download cuda_8.0.61_375.26_linux.run from the following link <br />
  https://drive.google.com/open?id=1f_HjxCg30BCD9r8OfhtsaXyKChhAiy8s <br />
  Then run the following command for installation <br />
  $ sudo sh cuda_8.0.61_375.26_linux.run <br />
 
3. Run folloiinwg commands for the environment settings
  $ echo -e "\n## CUDA and cuDNN paths"  >> ~/.bashrc     <br />
  $ echo 'export PATH=/usr/local/cuda-8.0/bin:${PATH}' >> ~/.bashrc     <br />
  $ echo 'export LD_LIBRARY_PATH=/usr/local/cuda-8.0/lib64:${LD_LIBRARY_PATH}' >> ~/.bashrc     <br />

  Check if the following lines are created in the ~./bashrc <br />

  export PATH = /usr/local/cuda-8.0/bin : $ { PATH } <br />
  export LD_LIBRARY_PATH = /usr/local/cuda-8.0/lib64 : $ { LD_LIBRARY_PATH } <br />

4. Run following commands to check if CUDA is installed properly <br />
  $ source ~/.bashrc  <br />
  $ nvcc --version  <br />
  nvcc: NVIDIA (R) Cuda compiler driver  <br />
  Copyright (c) 2005-2016 NVIDIA Corporation  <br />
  Built on Tue_Jan_10_13:22:03_CST_2017  <br />
  Cuda compilation tools, release 8.0, V8.0.61  <br />

5. As a final step of CUDA installation, check the CUDA path
  $ which nvcc  
  /usr/local/cuda-8.0/bin/nvcc

## CuDNN v5.1 
1. Join the site in the following link and download CuDNN v5.1 Library (cudnn-8.0-linux-x64-v5.1.tgz) for Linux
  https://developer.nvidia.com/rdp/cudnn-download

  You can also download cudnn-8.0-linux-x64-v5.1.tgz  from the following link <br />
  https://drive.google.com/open?id=1f_HjxCg30BCD9r8OfhtsaXyKChhAiy8s <br />

2. Run the following commands
 Note: If nvcc result is not "/usr/local/cuda-8.0/bin/nvcc", use nvcc output instead of "/usr/local/cuda-8.0/bin/nvcc" after "which nvcc"

  $ tar xzvf cudnn-8.0-linux-x64-v5.1.tgz <br />
  $ which nvcc <br />
  /usr/local/cuda-8.0/bin/nvcc <br />
  $ sudo cp cuda/lib64/* /usr/local/cuda-8.0/lib64/ <br />
  $ sudo cp cuda/include/* /usr/local/cuda-8.0/include/ <br />
  $ sudo chmod a+r /usr/local/cuda-8.0/lib64/libcudnn* <br />
  $ sudo chmod a+r /usr/local/cuda-8.0/include/cudnn.h <br />

## NVIDIA CUDA Profile Tools Interface 
  sudo apt-get install libcupti-dev <br />

## TensorFlow setup 
  Install python 3.6.3 first. Keep Enterng and select yes for all question during installation process <br />
  $ bash Anaconda3-4.3.0-Linux-x86_64.sh <br /> 
  $ source ~/.bashrc <br />
  
  Run python and check version <br />
  $ python <br />
  Python 3.6.0 |Anaconda 4.3.0 (64-bit)| (default, Dec 23 2016, 12:22:00)  <br />
  [GCC 4.4.7 20120313 (Red Hat 4.4.7-1)] on linux <br />
  Type "help", "copyright", "credits" or "license" for more information. <br />
  

  Install tensorflow following instruction in the following link <br />
  https://www.tensorflow.org/install/install_linux <br />
  Note: There are multiple installatio method introduced in the website. Just use pip3 based installation unless you really want isolated development environment.

## TensorFlow tutorial & example 
  Here is the best tensorflow tutorial  <br />
  https://github.com/Lab930boss/DeepLearningZeroToAll.git   <br />

  Though the vidoe lecture is in Korean, the example is self-contained and well coded.   <br />
  You will immediately tell what each lab does when you read lab project file name   <br />
  Fyi there is lecture note link. The lecture note is written in English   <br />
  https://goo.gl/jPtWNt

## OpenCV setup instruction for Ubuntu
https://github.com/jayrambhia/Install-OpenCV


## Yolo2 darknet


## FaceNet

