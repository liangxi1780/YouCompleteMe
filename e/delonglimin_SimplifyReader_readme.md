###简阅


一款基于Google Material Design设计开发的Android客户端，包括新闻简读，图片浏览，视频爽看 ，音乐轻听以及二维码扫描五个子模块。项目采取的是MVP架构开发，由于还是摸索阶段，可能不是很规范。但基本上应该是这么个套路，至少我个人认为是这样的~恩，就是这样的！

###效果图

![image](https://raw.githubusercontent.com/chentao0707/server/master/SimplifyReader/images/all_in_one.jpg)


![image](https://raw.githubusercontent.com/chentao0707/server/master/SimplifyReader/images/project.gif)

![image](https://raw.githubusercontent.com/chentao0707/server/master/SimplifyReader/images/qrcode.gif)

![image](https://raw.githubusercontent.com/chentao0707/server/master/SimplifyReader/images/project_struct.png)

###Demo下载
[火速跳转](http://u.720life.cn/g/8815754ee12efa4e18da59f15da59f79d53031df54a680f7f0ab2660937f5ef3)  | [Download-APK](http://u.720life.cn/g/bb9e19de933fd87f05600116164183c0b3ddd62d3854e3432c88c12f9e59c662bebf8ff96f0ce5096266bc3c108889340318e6fff7a9dbf103941e9634f81f574239132aba23d8ab754ddf9b829708c3f1a987faecfd9d6a5390249e6d359c46) 

![image](https://raw.githubusercontent.com/chentao0707/server/master/SimplifyReader/images/download.png)

###模块分析

####新闻简读

* 介绍：API使用的是凤凰新闻客户端的接口，我只是简单的获取了新闻的列表和详情数据，由于api和凤凰新闻客户端完全一致，鉴于侵权问题我就不开源出来了。至于接口是如何获取的？Google，百度，调试获取日志，我能说的只有这么多。

* 功能：列表页使用自定义的ListView(自动加载更多）显示新闻列表，详情使用的是WebView加载，支持滑动返回。对于多图
新闻的处理，使用的和主流新闻客户端类似，滑动切换多张图片，可双指缩放图片大小！

####图片浏览

* 介绍：API使用的是百度图片的搜索接口，由于网上有很多的开发者开源了这个接口，所以我也就放出来，如有侵权请及时告知。

* 功能：列表页使用的瀑布流效果（增加了下拉刷新和上拉加载更多）详情页和列表页的切换增加了一个图片放大或缩小到指定位置的效果，图片也可以双指缩放！

####视频爽看

* 介绍：API使用的是优酷开放平台的SDK，不过要吐槽的一点是，优酷的SDK真心不好用，还是Eclipse版本的，我是一点点移植到Android Studio平台的，但是它的接口还是很丰富的，好好的利用一下，还是能够做出一个优秀的APP的。

* 功能：列表页使用了Google的CardView，简单的获取了一些视频的基本数据。播放页使用了优酷提供的视频播放器组件，传入视频ID就可以播放视频了，只要调通了SDK，其他的都是一些简单的数据获取！

####音乐轻听

* 介绍：API获取的是豆瓣音乐的数据，由于也不是开放API，如有侵权请及时告知。

* 功能：播放音乐的界面是我自定义的一个唱机的View，很多思路都是从网上学习借鉴过来的，自己重新造了个轮子。UI和网易云音乐对比的话，只能说是形似神不似了，没有人家做的细致！

####二维码扫描

* 介绍：这个完全是我自己单独开发的类库，之前也有开源出来，这次又再一次重构优化，后期会单独剥离二维码扫描模块，做成类库和Demo的形式，提供Android Studio版本。

* 功能：扫描界面使用xml进行布局，然后加入属性动画。这样布局更具有优势，更利于多屏幕适配。解码模块使用的是两个主流的开源库Zbar和ZXing，进过多次测试发现，ZBar虽然扫描效率和速度高于ZXing，但是经常扫描出错误的信息，可能由于太灵敏的缘故把，综合二者的优缺点还是建议使用ZXing来解码，并且这个项目还在长期维护更新！

###致谢

* 苦于没有后台支持，找到这些支持JSON数据格式的开放接口可谓是煞费苦心，前前后后尝试了很多次才找到，也感谢网友们提供的接口！

* 界面的原型都是我自己构思的，后期的切图美化主要是Chris帮忙完成的，很感谢他业余时间和我一起完成这样一个APP！

* 项目中大量使用了Github上面优秀的开源项目，我会列举出来！其他一些代码片段就不一一致谢了，很感谢这些开放源码的技术大牛们，让我学到了很多！

* 最后如果觉得我的项目对你有所帮助，请点击我的支付宝付款码请我喝杯咖啡把~当然我也希望你们能够多多**fork**，多多**star**，多多**follow**，这将给我更多的动力开源更多的项目！

###开源项目说明

> **ButterKnife**

* **Link:** [https://github.com/JakeWharton/butterknife](http://u.720life.cn/g/54145d0471d91890860f7f8463c030462ec0046a56ff71603124e14e6be01c12558e29f736d9da626e50c93ab74a76b8) 

* **License:** `Licensed under the Apache License, Version 2.0 (the "License");`

> **AndroidTagGroup** 

* **Link:** [https://github.com/2dxgujun/AndroidTagGroup](http://u.720life.cn/g/54145d0471d91890860f7f8463c030469ac3339bcccfb15888fd498e764fe609622b8799a8b824ed36046af009f43dde) 

* **License:** `Licensed under the Apache License, Version 2.0 (the "License");`

> **NineOldAndroids** 

* **Link:** [https://github.com/JakeWharton/NineOldAndroids](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304659025559bfb23926de35bb070bb806b2fe56d3d87cf923b549a48308b2ffef55)  

* **License:** `Licensed under the Apache License, Version 2.0 (the "License");`

> **SystemBarTint**

* **Link:** [https://github.com/jgilfelt/SystemBarTint](http://u.720life.cn/g/54145d0471d91890860f7f8463c030465fe6507eba341e60082d599bd9cc44fb029a905b0777c63d44251e5a21bc4374) 

* **License:** `Licensed under the Apache License, Version 2.0 (the "License");`

> **Android-Universal-Image-Loader**

* **Link:** [https://github.com/nostra13/Android-Universal-Image-Loader](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046d7b7fecec8c72fdeda13bcc3230f11270723e803153a8fdddcb7ee1b747b8cefc7a6a3e5d792f6881aac3a309e8aaada) 

* **License:** `Licensed under the Apache License, Version 2.0 (the "License");`

> **PhotoView**

* **Link:** [https://github.com/chrisbanes/PhotoView](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304681eaa486aaf0b66017460e3510793c486a54ce5384cbd06aa0e9b4755ab0978d) 

* **License:** `Licensed under the Apache License, Version 2.0 (the "License");`

> **OkHttp** 

* **Link:** [https://github.com/square/okhttp](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046a1a49e86ff63d2259c9fa2db786827e2) 

* **License:** `Licensed under the Apache License, Version 2.0 (the "License");`

> **SmartTabLayout**

* **Link:** [https://github.com/ogaclejapan/SmartTabLayout](http://u.720life.cn/g/54145d0471d91890860f7f8463c030469917de7556d2b018d63d9267796a5ddfce0bda65c8ab4afa158ca703d66207ee) 

* **License:** `Licensed under the Apache License, Version 2.0 (the "License");`

> **SwipeBackLayout**

* **Link:** [https://github.com/ikew0ng/SwipeBackLayout](http://u.720life.cn/g/54145d0471d91890860f7f8463c030461c7a15b0838529771d925e71d8c6f647e9849aa1e8784cb20288bacc74c25ed7) 

* **License:** `Licensed under the Apache License, Version 2.0 (the "License");`

> **ImageBlurring**

* **Link:** [https://github.com/qiujuer/ImageBlurring](http://u.720life.cn/g/54145d0471d91890860f7f8463c030464c3793fd3b60e1bf6dc667a97682d421ae13a3a9d1401236f10d607aee686034) 

* **License:** `Licensed under the Apache License, Version 2.0 (the "License");`

> **PinterestLikeAdapterView**

* **Link:** [https://github.com/dodola/PinterestLikeAdapterView](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046f1af91dbf4af5e38602e1d9399b302d7508fe17c98c576fe56952648bed0113974326110fbd3274d89c23877cf94ce0e) 

* **License:** `Licensed under the Apache License, Version 2.0 (the "License");`

> **Material-Dialogs**

* **Link:** [https://github.com/afollestad/material-dialogs](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046c10f4609c887b6c6920a493c81185ff3e39e73cae4bf009a3984c8f16cfce065) 

> **EventBus**

* **Link:** [https://github.com/greenrobot/EventBus](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046189082b87c82768be0521336e3986e7f55a2038da7674d19212c63233857cf08) 

> **Gson** 

* **Link:** [https://github.com/google/gson](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046d12e769b56e529b87bc22488dd9e124f) 

> **Volley** 

* **Link:** [https://android.googlesource.com/platform/frameworks/volley](http://u.720life.cn/g/56e220b236c4ae56c0fa270f62d2a7b3d6d52d2725324e53b0d7f1edb25a1546a0c62b659b2f67c742f30b70e2c948155f7447fbb215059143f5a7f6563ddc2b) 

> **Umeng** 

* **Link:** [http://www.umeng.com/](http://u.720life.cn/g/74c7651e3989650ce35e536ab7c55cd92f059ae704d913661f91f2d5f85c8b85) 

> **Youku**

* **Link:** [http://open.youku.com/](http://u.720life.cn/g/9efe45e89d582e17ff689cbb547db1d27a2c7e7409033652bab3f57093c5ec08) 

###打赏我

![Image](https://raw.githubusercontent.com/SkillCollege/server/master/SimplifyReader/images/pay_qrcode.png)

###关于我

* **QQ:** 1076559197
* **QQ Tribe:** 345470463
* **Weibo:** [http://weibo.com/obsessive1990](http://u.720life.cn/g/c1e3906cb73241d8bdbe53b5d457b17d4bacd44623b5b60c8ee3a949141f3c15) 
* **Email:** [1076559197@qq.com](mailto:1076559197@qq.com) | [tchen0707@gmail.com](mailto:tchen0707@gmail.com)
* **Github:** [https://github.com/chentao0707](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304691842913fb3a6d71d7f4510733c0ee61) 
* **Blog:** [http://www.qingcore.com](http://u.720life.cn/g/f2716d726e518c5f98da534f932ca3a654d0ed57a5068a32791c453791052754) 

###项目主页

[http://www.qingcore.com/SimplifyReader/](http://u.720life.cn/g/f2716d726e518c5f98da534f932ca3a66aae2c11af7ae967a89d0d28a24a25b673b716db634a6518eb622f2109244451) 

###License

```
Copyright (c) 2015 [1076559197@qq.com | tchen0707@gmail.com]

Licensed under the Apache License, Version 2.0 (the "License”);
you may not use this file except in compliance with the License.
You may obtain a copy of the License at
   
   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)