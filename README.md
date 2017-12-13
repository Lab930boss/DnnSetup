# DnnSetup
This page includes Deep Learning environment setup instruction


## CUDA setup 
1. Nvidia Graphics driver installation
  $ sudo add-apt-repository ppa:graphics-drivers/ppa
  $ sudo apt-get update
  $ sudo apt-get install nvidia-375

  After this, reboot 
  $ sudo reboot
  
  When u type  $ nvidia-smi   , you should see the following message. 
  
Mon Mar  6 01:01:51 2017
+-----------------------------------------------------------------------------+
| NVIDIA-SMI 375.39                 Driver Version: 375.39                    |
|-------------------------------+----------------------+----------------------+
| GPU  Name        Persistence-M| Bus-Id        Disp.A | Volatile Uncorr. ECC |
| Fan  Temp  Perf  Pwr:Usage/Cap|         Memory-Usage | GPU-Util  Compute M. |
|===============================+======================+======================|
|   0  GeForce GTX 970     Off  | 0000:05:00.0      On |                  N/A |
|  0%   29C    P8    12W / 180W |    292MiB /  4034MiB |      0%      Default |
+-------------------------------+----------------------+----------------------+
                                                                               
+-----------------------------------------------------------------------------+
| Processes:                                                       GPU Memory |
|  GPU       PID  Type  Process name                               Usage      |
|=============================================================================|
|    0      1128    G   /usr/lib/xorg/Xorg                             169MiB |
|    0      1887    G   compiz                                         121MiB |
+-----------------------------------------------------------------------------+

## TensorFlow setup 
- Python 3.6.3 is recommended 

## TensorFlow tutorial & example 

## Yolo2 darknet

## FaceNet

