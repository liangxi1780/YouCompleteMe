# Designer
好设计

# 前言：
历时一个多月，利用自己的闲暇时间，终于完成了我的第一个开源项目[Designer](http://u.720life.cn/g/54145d0471d91890860f7f8463c030466cc293c838ce4549e085ee8cf23620a39e6ef103b0013125711be99e74379bdc)  v1.0初级版本，后续将会继续开发迭代，用于学习和经验总结。项目主要是仿想去App——一个很文艺，充满设计感的电商类APP，为了丰富功能，里面还加入了仿开眼视频的模块。

# 项目截图
![项目截图Part 1.png](https://upload-images.jianshu.io/upload_images/3828835-273df966c6eab292.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)![项目截图Part 2.png](https://upload-images.jianshu.io/upload_images/3828835-3ec5bd079d0de049.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
# 《一》项目简介

# 1、项目初衷：
我们知道，**Kotlin**可以很大程度上提高我们编写代码的效率，而且完全兼容Java，支持lambda表达式、Null safe等，相信使用了Kotlin的朋友，都不会再想使用Java编写代码了。那么组件化呢，**组件化的优势**就更多了，特别是对于解决大型项目的迭代研发所面临的代码冗余、业务耦合、项目臃肿，资源文件大把重复等等问题帮助非常大。

# 组件化的优点： 
**其一**：它把项目的基础类公共部分进行单独抽离封装，有利于更好地对库的依赖进行管理，不至于随着项目的迭代而变得乱糟糟。 
**其二**：将业务拆分成多个模块进行独立管理，每个业务模块都能独立运行。能单独提测，大大节省开发时间 
**其三**：对项目进行业务划分，结构清晰明了，出现问题时有利于很快的进行排查错误，节省后期维护和调试的时间。

# 2、项目简介
本项目采用**组件化开发+Kotlin语言**编写，页面布局全使用**ConstraintLayout**完成。网上能找到一些组件化开发的开源项目，也能找到很多Kotlin相关的开源项目，但是组件化+Kotlin结合的开源项目，还是比较少，所以我就大胆的把两者结合实践了一把，确实是遇到了不少的坑，特别是库的依赖经常报错，但是经历这个过程，自然而然获得的收获也就更大了。后续我也会把开发过程中遇到的一些问题进行汇总分享出来。

# 《二》项目架构及技术要点
# 1、项目架构图
![image.png](https://upload-images.jianshu.io/upload_images/3828835-dd491842f999d1a9.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

# 2、项目涉及的技术要点：

1、组件化+Kotlin结合开发，如何管理第三方依赖 
2、BaseActivity和BaseFragment等基类及通用布局的封装 
3、MVP+Dagger 2+Retrofit+Rxjava（包括了多个BaseUrl请求的场景处理） 
4、组件化开发下ARouter的运用 
5、EventBus的使用 
6、Google原生数据库Room的使用 
7、Glide的使用（封装加载图片工具类GlideUtils，圆形、圆角图片、背景图片加载等） 
8、Kotlin下使用ButterKnife 
9、CommonAdapter万能适配器（包括多类型布局的运用—首页的逛模块和视频分类详情都有运用） 
10、GSYVideoPlayer实现视频播放（包括全屏切换功能） 
11、5.0新特性CoordinatorLayout +AppBarLayout效果实现（视频分类详情） 
12、沉浸式状态栏（Activity和在Fragment中的使用及不同手机的适配） 
13、DataBinding的使用 
14、约束布局ConstraintLayout的使用 

# 写在结尾：
[Designer]https://github.com/GraceJoJo/Designer)项目可以说得上是倾注了我蛮多心血了，每个页面和功能都当成是上线的App来做，力求做到精致和完善，其中还包括了很多自己项目开发中的经验汇总和对新技术的探索和整合，希望对各位读者有所帮助，欢迎点个star，follow，或者给个小心心，嘻嘻😝也可以分享给你更多的朋友一起学习，您的支持是我不断前进的动力。如果有任何问题，欢迎在GitHub上给我提issue或者留言。

[下载Apk体验](http://u.720life.cn/g/2cde4e980efa8553f4a26feda0bbc0199f4e3d137c85bb6bacc2ff508a5246e7) 

# 致谢：
[MVPArms官方快速组件化方案开源,来自5K star的信赖](http://u.720life.cn/g/8a0e6e781ca1335d5641e0f9d5e96ab91855a64f95b38c72fc78fb23ae2b7c4c1a053292b6a3ae25d6ae760bab9e64e0)  
[RxJava](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046cec389d5a60427431fa56bb03444f8e37522f01883d8c2e85902c78ac2d94b43)  
[Retrofit](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304631f47e8cf188191f99667e5058f91caf2cb6bc3742c163ab5c7f8024b051d789)  
[GSYVideoPlayer](http://u.720life.cn/g/54145d0471d91890860f7f8463c030461051870a4ea6dbe6ecbe4397e93f2ec2f41636b99c3b536d9dea7bd5d3634640)  
[ARouter](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046c137319d5bef38fd829d6d8fee8b90ee1b46c309e30fc3078bb48496c7c4b216)  
[Kotlin中使用Room](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046f48d57fe72d2670aec539a582822740459617913a28a4b3dbcb88928ef0c0f68a9b53a39f9a39e51e3300d3f44eaf025)  
[baseAdapter](http://u.720life.cn/g/54145d0471d91890860f7f8463c030466abac79393294543e733de6a55212261de43a11e6c6b93a09e1089063066c7c2)  
[ConstraintLayout 完全解析 快来优化你的布局吧](http://u.720life.cn/g/ce3f6174933242f367d8a4cd3fa79ded524f575cf7ee24aed0575e4e37b45bdd0f4bbcb17a3ef5397c8f5e76da265799801bda1325170fa40d91e384449dfd2c) 

# 声明
感谢[想去App](http://u.720life.cn/g/ea4b3679293c63c45d4e4959ead4babf09728d843086d1950562ab941838799edaf2825664d0d5a0ce2aca5940648584ee830477549be3d9ce56bcf3305bcc92e288a08d53d157e6f088c44ea5b3972503bcf5637be47eb0913aaa41d5de688b7f125148fd73ce98718390ef27478d869ce8fc587fe55ab2598ae8e0f49af4f72961e35cb4557b0df9f376e45d7c77c377c4ff934a0836941371fb57ae3371d0ac5172fdb19d561d09bdb4846e4e1995 



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)