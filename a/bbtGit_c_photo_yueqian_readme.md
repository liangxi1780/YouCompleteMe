# C语言_电子相册_粤嵌项目

#### 介绍
在arm开发板LCD屏幕上显示制定路径的JPG图片组，首页显示提示语句，并通过获取屏幕手势左滑右滑显示上一张或下一张图片，上滑自动播放，下滑退出程序。

说明：

主函数：showphoto.c   功能：调用其它功能函数 


链表操作函数：dirlinklist.c 功能：创建了双向循环链表 用于存放jpg图片信息，并将其信息结点插入链表中。


屏幕手势函数：getmotion.c 功能：定义枚举类型，通过获取lcd屏幕坐标的变化，判断上下左右的手势，并返回至主函数。


图片解码显示函数：jpg.c 功能：将jpg图片解码成lcd可以显示的RGB数据并将其映射至显存中，显示图片。



注意：1.jpg图片解码需要第三方库文件支持，并且也需上传至arm开发板,可自行百度下载。


     2.gcc编译时主函数showphoto.c时，需要用 arm-linux-gcc编译，可自行百度下载。


     3.编译时制定头文件以及库文件路径且需要告诉arm开发板用到的库文件路径，如： arm-none-linux-gnueabi-gcc show_jpeg.c  -o show_jpeg         -I /home/gec/jpeglib/include/          -L /home/gec/jpeglib/lib/ -ljpeg  -Wl，-rpath=./lib -ldl


#### 码云特技

1. 使用 Readme\_XXX.md 来支持不同的语言，例如 Readme\_en.md, Readme\_zh.md
2. 码云官方博客 [blog.gitee.com](http://u.720life.cn/g/4d9d51ba66eeb41dfb9759648c593bf554785fd0e6ab49d2f13e98afcb69bbc7) 
3. 你可以 [https://gitee.com/explore](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6ed27d15edf43aa40a6d37a2a10b263e5a)  这个地址来了解码云上的优秀开源项目
4. [GVP](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6eb5ad9b84ebe402667383e4a11c785b2d)  全称是码云最有价值开源项目，是码云综合评定出的优秀开源项目
5. 码云官方提供的使用手册 [https://gitee.com/help](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6ebbaab544314b1a4bd89bdd984a12bd00) 
6. 码云封面人物是一档用来展示码云会员风采的栏目 [https://gitee.com/gitee-stars/](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e43c4696b881f436e3c9d0b3d64c264cb) 


 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)