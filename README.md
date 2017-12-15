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

Check if the following lines are created in the ~./bashrc

export PATH = /usr/local/cuda-8.0/bin : $ { PATH } <br />
export LD_LIBRARY_PATH = /usr/local/cuda-8.0/lib64 : $ { LD_LIBRARY_PATH } <br />

## TensorFlow setup 
- Python 3.6.3 is recommended 

## TensorFlow tutorial & example 

## Yolo2 darknet

## FaceNet

