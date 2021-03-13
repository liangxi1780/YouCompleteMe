hutool
======

 ![封面](http://img.hb.aicdn.com/61f84090279e1aaf49a11301dea2b3f453d2ad9028aaf4-R12vgs_fw658) 

一个Java基础工具类，类似于[jodd]http://jodd.org/)和[Apache commons lang]http://commons.apache.org/)的Java工具类。

## 简介
[Hutool](http://u.720life.cn/g/54145d0471d91890860f7f8463c030464890b78bf8a4fe32681c0079c41812768bccbb9e0fb5631dffb2fe5c41587f347412ad8889fcf746a993ff78ccd2c941559f3dc3919214a86650027a68e108437d555dc21098f468dbda60966a6ba6ad6ef949d55af313dd179a7813d6985152  Commons Lang]http://commons.apache.org/)和[JODD]http://jodd.org/)里的一些写法，不过大部分还是自己写的，希望你看了之后会有所启发或者能给你工作中带来帮助。说实话我现在写代码已经离不开自己这个工具包了，叫做Hutool也有“糊涂”之意，表示很多功能糊里糊涂就实现了。好吧，言归正传，说说里面一些好玩的方法（工具包中大部分是一些静态方法）。

## 设计哲学
[Hutool](http://u.720life.cn/g/54145d0471d91890860f7f8463c030464890b78bf8a4fe32681c0079c418127657cd477b902d7c20ac3b59e23dabe0e1744518bf863f08a6392b593d0b8e83703defd59d55c2c4750a8db89fadad0304cbc4aec2910f56a6b189d7142818a949f4f6ef86cd7085fc637b688fefeedb450f7ef280e470c1f6ff113d800119c6194efeb958392074e14facdba38c68fad69807c4091d4b90d1576cb0dda56ef7e89152c66f783cd6ddfddacb4f0309c644 

1. 减少代码录入。
2. 常用功能组合起来，实现一个功能只用一个方法。
3. 简化Java API，原来需要几个类实现的功能我也只是用一个类甚至一个方法（想想为了个线程池我得new多少类……而且名字还不好记）
4. 对于null的处理我没有可以回避，而是采取“你给我null我也给你返回null”这种思想，尽量不在工具类里抛空指针异常（这思想稍猥琐啊……直接把包袱扔给调用者了，好吧，谁让你给我null了）。
5. 一些固定使用的算法收集到一起，不用每次问度娘了（例如Base64算法、MD5、Sha-1，还有Hash算法）
6. 借鉴[Python]https://www.python.org/)的很多小技巧（例如列表切片，列表支持负数index），让Java更加好用。
7. 非常好用的ORM框架，同样借鉴[Python]https://www.python.org/)的[Django]https://www.djangoproject.com/)框架，以键值对的实体代替对象实体，大大降低数据库访问的难度（再也不用像Hibernate一样配置半天ORM Mapping了）。
8. 极大简化了文件、日期的操作，尤其是相对路径和绝对路径问题做了非常好的封装，降低学习成本。

## 安装
### Maven
在项目的pom.xml的dependencies中加入以下内容:

```xml
 
     com.xiaoleilu 
     hutool 
     X.X.X 
 
```

注：工具包的**版本**可以通过 [http://search.maven.org/](http://u.720life.cn/g/686169b320f6084fa4aea25a9bdaff1caf834fc52c57643856e0bb0c6908ce5b)  搜索`hutool`找到项目。

### 非Maven项目
可以从[http://search.maven.org/](http://u.720life.cn/g/686169b320f6084fa4aea25a9bdaff1caf834fc52c57643856e0bb0c6908ce5b)  搜索`hutool`找到项目，点击对应版本，下面是相应的Jar包，导入即可使用。

最新的2.13.1版本Jar下载地址：[http://search.maven.org/remotecontent?filepath=com/xiaoleilu/hutool/2.13.1/hutool-2.13.1.jar](http://u.720life.cn/g/686169b320f6084fa4aea25a9bdaff1caa751985d864b0e0000eb86d3370b62366cdf58530c81db8dbcbc9433631c6073e70770f231c45f1be8638b2f2112b73ec0e5dabfcaa258bdf04a5645270ab0c9d3f0b7c3114be4e68df7311660ab525) 

Java doc下载地址：[http://search.maven.org/remotecontent?filepath=com/xiaoleilu/hutool/2.13.1/hutool-2.13.1-javadoc.jar](http://u.720life.cn/g/686169b320f6084fa4aea25a9bdaff1caa751985d864b0e0000eb86d3370b62366cdf58530c81db8dbcbc9433631c6073e70770f231c45f1be8638b2f2112b73ec0e5dabfcaa258bdf04a5645270ab0c77027bcf1cc5085737f3d24c8aaa562a363c70e556c3665e9747ec416ac9445a) 

## 文档请移步 

[Hutool Wiki @ osc](http://u.720life.cn/g/17a180c798e6efa0a4495086733fde19b994d90e60e641368865fcaf5cdaf5d8) 

[Hutool Wiki @ github](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046707fe3a61e2887e2dc70b2f3f1aa57552a6c5d02a25644616bea7f99ea9b2084) 



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)