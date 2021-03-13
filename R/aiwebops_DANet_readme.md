# [Dual Attention Network for Scene Segmentation(CVPR2019)](http://u.720life.cn/g/ef50ff7c3b5c85de9d07d6f28fa05754b2f97fdec0f6222fa6f0fe2af725157e71dc121a15e67d07657eabd529922895) 
[Jun Fu](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046d66984803e3bdbd4a916cb3b5960c468  [Jing Liu](http://u.720life.cn/g/5824c9371ec1b3afeb826d7e9b7ac6ef1322c22bb253f838e80bd831b107fd6be8fb2e3f9f70af44effec166661084cb140c04a19676c45f307f97fe72b56e45  [Haijie Tian](http://u.720life.cn/g/54145d0471d91890860f7f8463c030465ae597049ed95d77f5584b7a4073fbb0  [Yong Li](http://u.720life.cn/g/eb8c59e57258bf4fdaf06243da728264ca200df8225959fad2197668fffe9814  Yongjun Bao, Zhiwei Fang,and Hanqing Lu 
## Introduction

We propose a Dual Attention Network (DANet) to adaptively integrate local features with their global dependencies based on the self-attention mechanism. And we achieve new state-of-the-art segmentation performance on three challenging scene segmentation datasets, i.e., Cityscapes, PASCAL Context and COCO Stuff-10k dataset.

![image](img/overview.png)

## Cityscapes testing set result

We train our DANet-101 with only fine annotated data and submit our test results to the official evaluation server.

![image](img/tab3.png)

## Usage

1. Install pytorch 

  - The code is tested on python3.6 and official [Pytorch@commitfd25a2a](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046213e100d703bc1a33acc62d362359d829184ae3765f261d760e86afe196b338dfc272c8f2d03fea44791d8484808672353d58241c730256a348f3b55b1f2ba4bfd46754ccb5d6d7eadc39012aabf5845  please install PyTorch from source.
  - The code is modified from [PyTorch-Encoding](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046aa74862345eca1c61d4950d6c75f88df0d6cc1d047e32049072237b7427e7e1d182bb1de005e3d6832c11babcc85951e  
  
2. Clone the repository:

   ```shell
   git clone https://github.com/junfu1115/DANet.git 
   cd DANet 
   python setup.py install
   ```
   
3. Dataset

  - Download the [Cityscapes](http://u.720life.cn/g/93d7635cef9a4049180896abf1ebad7a9867a0e59a0856e5f37ad99f8041536cb233ed6c69a035896970236d71329452)  dataset and convert the dataset to [19 categories](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046a96ae3536e0129df89e88aa682042481444c67f5f194a28e0c5f959ae16c8c7dadac38c9a341934bab7850b53c128cae02ceae2e1de5e486a048320da73ff61d6cc7de391f86149d73fbf37225c34545  
  - Please put dataset in folder `./datasets`

4 . Evaluation

  - Download trained model [DANet101](http://u.720life.cn/g/3a38f42308c8ee71aa166c0591609e00a7077e4f2d534815140bc1d16084b944b034a370bb087f2a4ec29b754304ca1cda856043771dfb2ed96ea9fd449a3f3178879c282ef73d8c3272cca0aebe68eb)  and put it in folder `./danet/cityscapes/model`
  - Evaluation code is in folder `./danet/cityscapes`
  - `cd danet`

  - For single scale testing, please run:
  
   ```shell
   CUDA_VISIBLE_DEVICES=0,1,2,3 python test.py --dataset cityscapes --model danet --resume-dir cityscapes/model --base-size 2048 --crop-size 768 --workers 1 --backbone resnet101 --multi-grid --multi-dilation 4 8 16 --eval
   ```
   
  - For multi-scale testing, please run:
  
   ```shell
   CUDA_VISIBLE_DEVICES=0,1,2,3 python test.py --dataset cityscapes --model danet --resume-dir cityscapes/model --base-size 2048 --crop-size 1024 --workers 1 --backbone resnet101 --multi-grid --multi-dilation 4 8 16 --eval --multi-scales
   ```  
   
  - If you want to visualize the result of DAN-101, you can run:
 
   ```shell
   CUDA_VISIBLE_DEVICES=0,1,2,3 python test.py --dataset cityscapes --model danet --resume-dir cityscapes/model --base-size 2048 --crop-size 768 --workers 1 --backbone resnet101 --multi-grid --multi-dilation 4 8 16
   ```
   
5. Evaluation Result:

   The expected scores will show as follows:
   
   (single scale testing denotes as 'ss' and multiple scale testing denotes as 'ms')
   
   DANet101 on cityscapes val set (mIoU/pAcc): **79.93/95.97** (ss) and **81.49/96.41** (ms)


6. Training:

  - Training code is in folder `./danet/cityscapes`
  - `cd danet`
  
   You can reproduce our result by run:

  ```shell
   CUDA_VISIBLE_DEVICES=0,1,2,3 python train.py --dataset cityscapes --model  danet --backbone resnet101 --checkname danet101  --base-size 1024 --crop-size 768 --epochs 240 --batch-size 8 --lr 0.003 --workers 2 --multi-grid --multi-dilation 4 8 16
   ```
 
   Note that: We adopt multiple losses in end of the network for better training. 
   

## Citation
If DANet is useful for your research, please consider citing:
```
@article{fu2018dual,
  title={Dual Attention Network for Scene Segmentation},
  author={Jun Fu, Jing Liu, Haijie Tian, Yong Li, Yongjun Bao, Zhiwei Fang,and Hanqing Lu},
  booktitle={The IEEE Conference on Computer Vision and Pattern Recognition (CVPR)},
  year={2019}
}
```
## Acknowledgement
Thanks [PyTorch-Encoding](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046aa74862345eca1c61d4950d6c75f88df0d6cc1d047e32049072237b7427e7e1de807fca3c4d85e6e71a22a0cbe9709b9  especially the Synchronized BN!



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)