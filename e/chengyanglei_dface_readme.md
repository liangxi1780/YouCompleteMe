 
 
 

-----------------
# DFace • [![License](http://pic.dface.io/apache2.svg)](https://opensource.org/licenses/Apache-2.0)


| **`Linux CPU`** | **`Linux GPU`** | **`Mac OS CPU`** | **`Windows CPU`** |
|-----------------|---------------------|------------------|-------------------|
| [![Build Status](http://pic.dface.io/pass.svg)](http://pic.dface.io/pass.svg) | [![Build Status](http://pic.dface.io/pass.svg)](http://pic.dface.io/pass.svg) | [![Build Status](http://pic.dface.io/pass.svg)](http://pic.dface.io/pass.svg) | [![Build Status](http://pic.dface.io/pass.svg)](http://pic.dface.io/pass.svg) |


**基于多任务卷积网络(MTCNN)和Center-Loss的多人实时人脸检测和人脸识别系统。**


[Github项目地址](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046ec4b2bca1ff109b7de2db44a6808f6a4f89bd4e8f10d7ba50874cced90c62a57)   

[Slack 聊天组](http://u.720life.cn/g/00fdc27f9a108dd8d0e40474fc9cd2f7d8b47f1c508cad246c4a96d8a11a3739)   



**DFace** 是个开源的深度学习人脸检测和人脸识别系统。所有功能都采用　**[pytorch](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046213e100d703bc1a33acc62d362359d82a492185a899a29e973c0f4b11374ba0f 　框架开发。pytorch是一个由facebook开发的深度学习框架，它包含了一些比较有趣的高级特性，例如自动求导，动态构图等。DFace天然的继承了这些优点，使得它的训练过程可以更加简单方便，并且实现的代码可以更加清晰易懂。
DFace可以利用CUDA来支持GPU加速模式。我们建议尝试linux GPU这种模式，它几乎可以实现实时的效果。
所有的灵感都来源于学术界最近的一些研究成果，例如　[Joint Face Detection and Alignment using Multi-task Cascaded Convolutional Networks](http://u.720life.cn/g/ef50ff7c3b5c85de9d07d6f28fa05754eeb6f24ae19b28fd7f88086229c73b36)  和 [FaceNet: A Unified Embedding for Face Recognition and Clustering](http://u.720life.cn/g/ef50ff7c3b5c85de9d07d6f28fa0575405aa36c04f319dc0cad04154ec6c55ac) 


**MTCNN 结构**　　

![mtcnn](http://affluent.oss-cn-hangzhou.aliyuncs.com/html/images/mtcnn_st.png)


**如果你对DFace感兴趣并且想参与到这个项目中, 以下TODO是一些需要实现的功能，我定期会更新，它会实时展示一些需要开发的清单。提交你的fork request,我会用issues来跟踪和反馈所有的问题。也可以加DFace的官方Q群 681403076 也可以加本人微信 jinkuaikuai005**

###  TODO(需要开发的功能)
- 基于center loss 或者triplet loss原理开发人脸对比功能，模型采用ResNet inception v2. 该功能能够比较两张人脸图片的相似性。具体可以参考 [Paper]https://arxiv.org/abs/1503.03832和[FaceNet]https://github.com/davidsandberg/facenet
- 反欺诈功能，根据光线，质地等人脸特性来防止照片攻击，视频攻击，回放攻击等。具体可参考LBP算法和SVM训练模型。
- 3D人脸反欺诈。
- mobile移植，根据ONNX标准把pytorch训练好的模型迁移到caffe2,一些numpy算法改用c++实现。
- Tensor RT移植，高并发。
- Docker支持，gpu版

## 安装
DFace主要有两大模块，人脸检测和人脸识别。我会提供所有模型训练和运行的详细步骤。你首先需要构建一个pytorch和cv2的python环境，我推荐使用Anaconda来设置一个独立的虚拟环境。**如果使用GPU训练模式，需要安装Nvidia的cuda和cudnn。** 目前作者倾向于Linux Ubuntu安装环境。感谢热心网友提供windows DFace安装体验，windos安装教程具体
可参考他的[博客](http://u.720life.cn/g/39149d2728625c32662dda37d510ef8b0a81c434b357086aa3399edb7f444751a3190074623df19f177cad0a6f5d0e6199176bc220e29122fe3984ebb501264f3921e58c2047e64a115ab80bc0c2c5ea) 


### 依赖
* cuda 8.0
* anaconda
* pytorch
* torchvision
* cv2
* matplotlib

```shell
git clone https://gitee.com/kuaikuaikim/dface.git
```

在这里我提供了一个anaconda的环境依赖文件environment.yml （windows请用environment-win64.yml），它能方便你构建自己的虚拟环境。

```shell
cd dface  

conda env create -f environment.yml
```

添加python搜索模块路径  

```shell
export PYTHONPATH=$PYTHONPATH:{your local DFace root path}
```



### 人脸识别和检测

如果你对mtcnn模型感兴趣，以下过程可能会帮助到你。

#### 训练mtcnn模型

MTCNN主要有三个网络，叫做**PNet**, **RNet** 和 **ONet**。因此我们的训练过程也需要分三步先后进行。为了更好的实现效果，当前被训练的网络都将依赖于上一个训练好的网络来生成数据。所有的人脸数据集都来自　**[WIDER FACE](http://u.720life.cn/g/53c48e02676e0a16489aa80dd11fb89378c066dbaca33f86cbabb3519250330eca08d9a14eaf573aec15f027047e801130f6bf42df1c1213c6dfae772f86994a  和 **[CelebA]http://mmlab.ie.cuhk.edu.hk/projects/CelebA.html)**。WIDER FACE仅提供了大量的人脸边框定位数据，而CelebA包含了人脸关键点定位数据。以下训练除了　生成ONet的人脸关键点训练数据和标注文件　该步骤使用CelebA数据集，其他一律使用WIDER FACE。如果使用wider face的 wider_face_train.mat 注解文件需要转换成txt格式的，我这里用h5py写了个 [转换脚本](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6ea96d1697c7c536dffea9477b0a55834ce55cee014c9ff51579eeed163fdc8cc32633ed52044669003d4cf8e68d4b3989116bd8336a1874bb24566e49e1a30e7544181f367eec54472a76890ab816c31c315a66e0b73ee1d9b8d3891b5a71d7ee  这里我提供一个已经转换好的wider face注解文件 [anno_store/wider_origin_anno.txt](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6ea96d1697c7c536dffea9477b0a55834ce55cee014c9ff51579eeed163fdc8cc3f77b66d6edb4da30a84540ae881cca4ec14ce55539a299280c6a5b9c6e9b1ae4c83f6adeebccd6985c21eb2f886851dd  以下训练过程参数名--anno_file默认就是使用该转换好的注解文件。

  
* 创建 dface 训练数据临时目录，对应于以下所有的参数名　--dface_traindata_store
```shell
mkdir {your dface traindata folder}
```


* 生成PNet训练数据和标注文件

```shell
python dface/prepare_data/gen_Pnet_train_data.py --prefix_path {注解文件中图片的目录前缀,就是wider face图片所在目录} --dface_traindata_store {之前创建的dface训练数据临时目录}　--anno_file {wider face 注解文件,可以不填，默认使用anno_store/wider_origin_anno.txt}
```
* 乱序合并标注文件

```shell
python dface/prepare_data/assemble_pnet_imglist.py
```

* 训练PNet模型


```shell
python dface/train_net/train_p_net.py
```
* 生成ＲNet训练数据和标注文件

```shell
python dface/prepare_data/gen_Rnet_train_data.py --prefix_path {注解文件中图片的目录前缀，就是wider face图片所在目录} --dface_traindata_store {之前创建的dface训练数据临时目录} --anno_file {wider face 注解文件,可以不填，默认使用anno_store/wider_origin_anno.txt} --pmodel_file {之前训练的Pnet模型文件}
```
* 乱序合并标注文件

```shell
python dface/prepare_data/assemble_rnet_imglist.py
```

* 训练RNet模型

```shell
python dface/train_net/train_r_net.py
```

* 生成ONet训练数据和标注文件

```shell
python dface/prepare_data/gen_Onet_train_data.py --prefix_path {注解文件中图片的目录前缀，就是wider face图片所在目录} --dface_traindata_store {之前创建的dface训练数据临时目录} --anno_file {wider face 注解文件,可以不填，默认使用anno_store/wider_origin_anno.txt} --pmodel_file {之前训练的Pnet模型文件} --rmodel_file {之前训练的Rnet模型文件}
```

* 生成ONet的人脸五官关键点训练数据和标注文件

```shell
python dface/prepare_data/gen_landmark_48.py
```

* 乱序合并标注文件(包括人脸五官关键点)

```shell
python dface/prepare_data/assemble_onet_imglist.py
```

* 训练ONet模型

```shell
python dface/train_net/train_o_net.py
```

#### 测试人脸检测  

**如果不想训练，直接加Q群获取模型参数文件运行DFace，把onet_epoch.pt,pnet_epoch.pt,rnet_epoch.pt三个文件放到model_store目录即可**

```shell
python test_image.py
```    

### 人脸对比  
TODO 根据center loss实现人脸识别

#### 测试效果  
![mtcnn](http://affluent.oss-cn-hangzhou.aliyuncs.com/html/images/dface_demoall.PNG)  


### QQ交流群(模型获取请加群)  

#### 681403076 
 
![](http://affluent.oss-cn-hangzhou.aliyuncs.com/html/images/dfaceqqsm.png)

#### 本人微信  

##### jinkuaikuai005  

![](http://affluent.oss-cn-hangzhou.aliyuncs.com/html/images/perqr.jpg)  



## License

[Apache License 2.0](LICENSE)




 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)