# Pytorch-XNOR-Net
XNOR-Net, with binary gemm and binary conv2d, support both CPU and GPU.


# MNIST

## Usage
### Train:
~~~shell
cd <Repository Root>/MNIST/
python3 main.py --arch Bin_LeNet
python3 main.py --arch LeNet
~~~
### Evaluate:
~~~shell
cd <Repository Root>/MNIST/
python3 main.py --arch Bin_LeNet --evaluate --pratrain ./model/Bin_LeNet.best.pth
python3 main.py --arch LeNet --evaluate --pratrain ./model/LeNet.best.pth
~~~
|  Network  | Accuracy |  SIZE   |
|  -------  | -------- |  ----   |
|   LeNet   |  99.50%  |  1.7 MB |
| Bin_LeNet |  99.45%  |  102 KB |


# Cifar10

## Usage
### Train:
~~~shell
cd <Repository Root>/Cifar10/
python3 main.py --arch Bin_VGG16 #(11, 13, 16, 19)
python3 main.py --arch VGG16 #(11, 13, 16, 19)
~~~
### Evaluate:
~~~shell
cd <Repository Root>/Cifar10/
python3 main.py --arch Bin_VGG16 --evaluate --pratrain ./model/Bin_VGG16.best.pth
python3 main.py --arch VGG16 --evaluate --pratrain ./model/VGG16.best.pth
~~~
|  Network  | Accuracy |  SIZE    |
|  -------  | -------- |  ----    |
|   VGG13   |  92.40%  |  37.7 MB |
| Bin_VGG13 |  85.20%  |  1.3  MB |
|   VGG16   |  92.29%  |  59.0 MB |
| Bin_VGG16 |  85.16%  |  2.0  MB |


# Environment
## Software

* Python  3.5
* Pytorch 0.3.1
* CUDA    8.0
* gcc     5.4

## Hardware

* NVIDIA GTX 1080
* Intel  i5-6500 CPU @ 3.20GHz × 4
