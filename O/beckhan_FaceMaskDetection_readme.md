# FaceMaskDetection

## [updates]
### 人脸口罩检测，现开源所有主流框架模型和推理代码，支持的框架如下：

 - [x] PyTorch
- [x] TensorFlow（包含tflite模型和pb模型）
- [x] Keras
- [x] MXNet
- [x] Caffe

**检测人脸并判断是否佩戴了口罩， 并开源近8000张人脸口罩标注数据**

Detect faces and determine whether they are  wearing mask.

**首先，祝愿我国和世界各国早日战胜新冠肺炎疫情，武汉加油！中国加油！**

*  我们开源了人脸口罩检测的**所有主流框架（PyTorch、TensorFlow、Keras、MXNet和caffe）的相应模型**（使用keras训练的模型，并转换得到的其他框架模型），并提供了**所有五大框架**的的推理代码。所有模型都在`models`文件夹下。


* 开源了标注的7959张人脸标注图片，数据集来自于[WIDER Face]http://shuoyang1213.me/WIDERFACE/)和[MAFA]http://www.escience.cn/people/geshiming/mafa.html)数据集, 我们重新修改了标注并进行了校验(主要是
MAFA和WIDER Face的人脸位置定义不一样，所以我们进行了修改标注)并将其开源出来。（有需要的朋友，敬请关注我们新建的公众号AIZOO（本文末也有二维码，可以扫描关注），回复**口罩数据集**就可以了。公众号刚开，恳请大家帮忙关注和扩散一下～）


![](img/demo.png)

关于本项目的介绍，请参考以下三篇我们公众号的文章

* [AIZOO开源人脸口罩检测数据+模型+代码+在线网页体验，通通都开源了](http://u.720life.cn/g/408fb60b53d11d245635ad5e8e8cd6973891e79ab5fcfefa61d7751fd36b96f845f88d527540193a6ac5b2fc05f53ec97ca3cf8ecbb6fd7c54937aecac2bd5b59843cd022e57edb2c03ce966a1ea71229b6dbcbf9771b488075da087a17a2a5df69c5d3007d37d059486b33cf79da9792dcff0736d97ce7b1b944253c4821e5b2eaaa8c55503164cb45c65e271f36da59591c8b5992b9aae53bf5e1775994a81800ec416604fb223cc30cc073826d70ed83b499ac6814d7a7e7828f5d34b225919a32e1f90e95815838a9796d3d2a594fc636efb9910269cc99f159c14dc4a500ce035bd8bc2d7fd61c9ad3e0a01b7c7b4c61c44f98720b2b0752adb964db18a6953e12ca93f63bbc53aa9dd58152a30a412da75aeded1a7632dd49938c13508da8e9f2e9feb010f1f4ffc421c43376ffb2f019b9088b3d0080f9166a7e81b5736ea8809e65dfc3f10c2d962cc5ef0ec202a7cdac596b6d29bd7f5cf8182f015e274d9183d793eb0c91b3a1659d8610e352702cb25ed30bea74de96e65f152616ead7b1489300d0d25dcecec31aec2336a32eae91e169b99b62e1089db81102e) 

* [人脸口罩检测现开源PyTorch、TensorFlow、MXNet等全部五大主流深度学习框架模型和代码](http://u.720life.cn/g/408fb60b53d11d245635ad5e8e8cd6973891e79ab5fcfefa61d7751fd36b96f845f88d527540193a6ac5b2fc05f53ec9b401e777dc986ccb61dee2c1e60e6b5bf4227a71623f5bbec93c4e222d527f6fff98f2f84d3f45417c2a3eb6a9d471f217085d8fc4ace9c50f459d3e7c9dc4aaac88e5f79266029ff81177bfc0201cb3e785244cf1cc3050004a62866ec2dafbad5008bf2b99329bac7dd4630f2c5305f523a24052acd82b73ef458d51d18dcdb6531ae900192cf921113729d3379118f50e8e6ffbd6a81cf942fe16baa8922d478b79dbcdaad2459d8fa2ee4684eed4083feea1c52529dce9c17b44f1c17468d8025555a1fe80762f3464e3d4d56eac175673d57fda2b9b783cde18c2a55b3e484393d39680e0168b7a1c409ce92dab80197e987ba194f7f075d0d5a33d26d5035ded8b98a9239f49d27a8cdbddfbe6de8bbd67bd8d5aa0507647dfb9e1e3a61c8bfd836557cf4d280815f6487f6d707469f0634412eb8ad523e25068fa95c28cb8ab284078ba4055f677b29d2cce04d24c415143ba99a8d1d89ade7d82b31ee7bdd4c916e74facecaaf386afbef302) 

* [如何在浏览器运行深度神经网络？以人脸口罩识别为例进行讲解](http://u.720life.cn/g/408fb60b53d11d245635ad5e8e8cd6973891e79ab5fcfefa61d7751fd36b96f845f88d527540193a6ac5b2fc05f53ec9201a4fab09018d1be7c948a631db3fff797152eea767bfc2c8abb103da045b042776feffb6f8b11389e9ed69aaa76a698912f1010a3483c718a2c214c6ee1d4b2173ea3cba8a25939ed35390f8d83d8e3b77ed77119cf2d94eeb22c69d251b2799a3ed5196d33c187420da8d62732c2a63cc2bee532446c68efde94a927b1489c4fab6ba9cd6814872c5a1c83727f62479c949798f59e3a9a9662b3631770c194ddcc09642bf433ef3d4321d320dbc1579260f827bec6925e4c5d95ad895c550ae04b81e723d679858d0be15ea56de0fe2e9e5c269d7a65cd2dee53bdcc4d2eb9ebd1cc9dffa853a823817ef33cfa9f3100f16fb5619b36c4344307fde3c7fa9fbfec74968652f3e5fc3cc232644d13f30b0aeeb0c25d1e039354800a0571a58801568e628dee79d29c5f2878828d66b55a056f069bf22cbc12d481b889a15c64abfd3feb14f3c262c1c51d5d9722fe624b2474f3c7007268613bcc346da2a72fc285227008f0d059f5e83cf3ba2ebc6) 

我们也使用TensorFlow.js部署了一个网页版，大家可以点击下面链接访问
欢迎大家点击链接在线体验

[aizoo.com跑在您浏览器的口罩检测模型](http://u.720life.cn/g/9c76c5ba0e2e2a962d1ecd6acc8d2b5f7d81f67478a2af30a0b05588f5ebc55cada38548d377a166c0f8bd1d0f06b777) 
## 模型结构
我们在本项目中使用了SSD类型的架构，为了让模型可以实时的跑在浏览器以及终端设备上，**我们将模型设计的非常小，只有101.5万个参数**。模型结构在本文附录部分。

本模型输入大小为260x260，主干网络只有8个卷积层，加上定位和分类层，一共只有24层（每层的通道数目基本都是32\64\128），所以模型特别小，只有101.5万参数。模型对于普通人脸基本都能检测出来，但是对于小人脸，检测效果肯定不如大模型。具体效果，大家可以点击以下链接，访问我们的网站在线体验效果。
[aizoo.com跑在您浏览器的口罩检测模型](http://u.720life.cn/g/9c76c5ba0e2e2a962d1ecd6acc8d2b5f7d81f67478a2af30a0b05588f5ebc55cada38548d377a166c0f8bd1d0f06b777) 

网页使用了Tensorflow.js库，所以模型是完全运行在您浏览器里面的。运行速度的快慢，取决于您电脑配置的高低。

模型在五个卷积层上接出来了定位分类层，其大小和anchor设置信息如下表.


| 卷积层 | 特征图大小 | anchor大小 | anchor宽高比（aspect ratio）|
| ---- | ---- | ---- | ---- |
|第一层|33x33|0.04,0.056|1,0.62,0.42|
|第二层|17x17|0.08,0.11|1,0.62,0.42|
|第三层|9x9|0.16,0.22|1,0.62,0.42|
|第四层|5x5|0.32,0.45|1,0.62,0.42|
|第五层|3x3|0.64,0.72|1,0.62,0.42|

## 运行方法
### pytorch
如果您要运行图片：
```
python pytorch_infer.py  --img-path /path/to/your/img
```
如果您要在视频上跑，只需要：
```
python pytorch_infer.py --img-mode 0 --video-path /path/to/video  
# 如果要打开本地摄像头, video_path填写0就可以了，如下
python pytorch_infer.py --img-mode 0 --video-path 0
```
### TensorFlow/Keras/MXNet/Caffe
另外四大框架运行方法基本类似，只不过将`pytorch_infer.py`中`pytorch`的换成`对应框架名字即可即可`，以`TensorFlow`为例：
```
python tensorflow_infer.py  --img-path /path/to/your/img
```
**注意，对于caffe的推理，我们使用了permute层，所以需要使用caffe-ssd，也就是SSD作者开源的[caffe版本]https://github.com/weiliu89/caffe/tree/ssd)**，官方版本的caffe并不包含permute层。您也可以使用opencv的dnn模块来加载模型推理，opencv支持permute层。

不过如果您需要可以在官方版本的caffe上可以运行的模型，也可以联系我们修改模型，实现不需要permute层的模型。
## 附录
### 问题反馈与交流
欢迎AI圈和科技圈的朋友关注我们的公众号，这是我们分享AI技术和资讯的地方。我们要做的事情是搭建开发者和AI算法和产品需求方的一个桥梁，欢迎有AI算法需求的朋友关注我们，也欢迎有熟练算法和开发经验的工程师添加我们，与我们交流。

![](img/wx.png)

**如果你有任何问题，欢迎关注我们的公众号，通过后台给我留言，或者添加作者元峰的微信AIZOOTech与我联系 ，我会将您拉入AIZOO技术交流群。**
我们的技术交流群二维码，欢迎算法开发者和需求方进群交流，请输入备注，例如`张三丰-浙大-目标检测`或者`张三丰-腾讯-图像分割`

![](img/wxgroup.jpeg)


### 模型结构图
为了可视化方便，我们省略了BN层，如果您要查看完整模型，可以查看`img`文件夹的`face_mask_detection.hdf5.png`图片

![](img/face_mask_detection.caffemodel.png)

### 测试集PR曲线

因为WIDER face是一个任务比较复杂的数据集，我们的模型又设计的非常小，所以对于人脸的PR曲线并不是那么性感。这点可以通过设计大模型来提升对于小人脸的检测效果，如果您有需求，欢迎通过上述二维码联系我们。
![](img/pr_curve.png)

因为WIDER face是一个任务比较复杂的数据集，我们的模型又设计的非常小，所以对于人脸的PR曲线并不是那么性感。**这点可以通过设计大模型来提升对于小人脸的检测效果，如果您有需求，欢迎通过上述二维码联系我们。**
![](/img/pr_curve.png)


### 我们的网页长这样
欢迎大家点击链接在线体验

[aizoo.com跑在您浏览器的口罩检测模型](http://u.720life.cn/g/9c76c5ba0e2e2a962d1ecd6acc8d2b5f7d81f67478a2af30a0b05588f5ebc55cada38548d377a166c0f8bd1d0f06b777) 

![](img/facemask.gif)










 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)