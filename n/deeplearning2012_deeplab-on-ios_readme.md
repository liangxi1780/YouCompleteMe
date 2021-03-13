# Tensorflow-lite Deeplab RealTime 

## 1. Demo
![](http://www.ibbwhat.com/optimize1.gif)
![](http://www.ibbwhat.com/optimize2.gif)

## 2. Requirements:
- [Apple Developer Program Account](http://u.720life.cn/g/bebc106f44851209ec2c00eafe2b7bd67ba6856ae9d4c3372b8bd5e926f826ea)  (Simulator doesn’t have a camera)
- [Xcode 9.2](http://u.720life.cn/g/a69e8f5dba5b4106ccc3875c547b1484b947ce4c830cf222f1b91fc41f144391391262246f04e5d0c2b0630e184040a4) 
- [OpenCV 3.3.1 iOS Pack](http://u.720life.cn/g/bebc106f44851209ec2c00eafe2b7bd67ba6856ae9d4c3372b8bd5e926f826ea) 
- [Git LFS](http://u.720life.cn/g/b87e4c9a63ae57fc3eb7a94918b6f101dc6cc1e6193fd4c2aca9c88b88d4a391) 
- [Tensorflow-lite](http://u.720life.cn/g/de14350178d8232a6828b0e4db6a4d7b7f99c49f4a01623e62b0cb41458a88e0) 
- any iOS device with a decent camera


## 3. Code reference

- Opencv 
  Example application made for [this post](http://u.720life.cn/g/ce19288caac4b59057ec565c52ba1b368ec76f5ad496e848b56c78b6bba170caad2e1d95718b24afdc1c6ce65e37709dacb8103cc83b944ba2944ceb3a6ce4d9c27e7c2644045671be55866e0420fc2d0bfb7b57be38082d31ec0c2279cb2df3 

- Tensorflow 
  Example application made for [this post](http://u.720life.cn/g/de14350178d8232a6828b0e4db6a4d7b7f99c49f4a01623e62b0cb41458a88e0c1e80dc39b403ec99b5b009d61bb80ab92b1cb55ab179967fe30f1d62606e29e) 

- Model File: 
  DeepLab segmentation [download](http://u.720life.cn/g/6b8381a0f346a49d58454a5f95046f72773a95ea637ab88c30ee720c748edfa974297f75e77715affeabf7d1c36d75282307140966dfa4f0cf72fd3c80180f0c4ef87ea4073c3559db57e1e605dfece377cbef736b31dddac79c58099cf9d92611f46d3a9da28a8addc189bfd9a14ee8) 
  (image segmentation model that assigns semantic labels (e.g., dog, cat, car) to every pixel in the input image)

## 4. Installation:
```
git clone https://github.com/toniz/deeplab-on-ios.git
cd deeplab-on-ios/
pod install
open DeeplabOnIOS.xcworkspace
```


*   DeepLabv3+:
```
@inproceedings{deeplabv3plus2018,
  title={Encoder-Decoder with Atrous Separable Convolution for Semantic Image Segmentation},
  author={Liang-Chieh Chen and Yukun Zhu and George Papandreou and Florian Schroff and Hartwig Adam},
  booktitle={ECCV},
  year={2018}
}
```




 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)