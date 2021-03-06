# php修行之路

## 目录


- [学习步骤](#学习步骤)
- [官方文档](#官方文档)
- [社区](#社区)
- [工具](#工具)
- [书籍](#书籍)
- [视频教程](#视频教程)
- [学习网站](#学习网站)
- [博客](#博客)
- [知识图谱](#知识图谱)

## 加群交流

微信群"PHP开发交流群"

由于微信群的限制，超过 100 人就不能扫码加群。所以可以先关注我公众号，然后发送 `PHP开发`，按照提示一步一步加群。

![PHP开发交流区群](http://img.blog.csdn.net/20161229104305784?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXFfMjg4MzIxMzU=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

因为下面的视频教程大多数在我的云盘上存着，而且公开分享有可能获取不到，遇到这种情况也可以加群，进群之后我重新给你发链接，同时在这边及时更新。

## 学习步骤

### 第一阶段

1. 首先对HTML+CSS有一个基础的了解，做出一个简单的页面，感受一下网页开发的乐趣。（HTML+CSS）
2. 接着简单的学习一下JavaScript，了解网页的动态交互效果是怎么做出来的。（JavaScript）
3. 学习一点Linux基础课程，因为大多数的web站点都是部署在Linux服务器上的，所以你需要了解一下简单的Linux操作。（Linux基础）
4. 当你对这些都有一点基础的了解之后，这时候开始学习PHP语法的效果可能会更好。所以就开始你的PHP学习之路吧！（PHP语法）
5. 可能经过之前的了解，你知道大多数的PHP站点都是需要数据库的，这里我们一般说PHP和MySQL会更配哦！那么我的建议是MySQL确实是一个不错的选择。（MySQL数据库了解）
6. 当你有了这些基础知识之后，你已经可以创造一些简单的小玩意了！哦！这时候你可能会问我该在哪里跑我的程序呢？有了问题就要解决么！毕竟我们程序员的主要职责就是debug了。所以开始搭建你的LAMP环境吧！（注意：我这里说的是LAMP环境，可能大部分人用的是Windows系统，毕竟这也算是中国国情了么！而且确实在Windows上搭建WAMP环境对于不习惯使用命令行的人来说确实会方便不少，但是对于你以后在公司工作来说，这却不是一个很好的选择！是的，没错！公司90%以上使用的都是Linux系统。当你在学习刚开始的时候就用LAMP环境，这样你就能更好的适应公司的环境，毕竟Linux系统的命令行操作的命令那么杂，如果你不经常使用，过不了几天你学过的那些Linux基础就忘光了。之后还得增加学习成本来重新学习LAMP环境，那么一开始就使用它，何乐而不为呢？   -- 这里可能和前几个学习步骤有点冲突，毕竟当你翻开第一本PHP语法书的时候，他基本上讲的就是环境搭建，所以我这个步骤可能有点靠后了，这个就根据你个人的学习习惯来调整就好。如果你喜欢准备的万无一失在开始你的编程之旅，那么我按照这个学习顺序走就可以了！当然如果你之前已经了解过一点相关知识，那么别犹豫，直接搭建好环境开干！）
7. 要是你按照这个顺序已经学到这里了，那么现在开始做一个界面精美的留言本吧！一个留言本基本上就都考核了你的基础知识了。你可以用你学到的HTML+CSS，JavaScript做一个好看又有动态交互的界面。再用PHP语法来连接数据库，编写逻辑，操作数据。这些就考验了你对PHP语法的简单运用！然后你要是按照我第六条建议搭建的是LAMP环境，那么你在建表的时候就不免用到切换用户，进入目录，创建目录等等一系列Linux命令，当然了，对于新手来说，我的建议是在命令行下建表，这样更加有利于你对sql语句的学习。

### 第二阶段

到了第二阶段，可能对于热爱学习的你来说，已经不仅仅满足于做一个简单的留言本了！毕竟这对于现代的我们来说这可能已经是上个世纪的东西了，谁稀罕？  而且你可能这个时候已经慢慢的认识到了，现在已经是面向对象的世界了。俗话说“万事万物皆对象”，要是还用原生脚本来编写的话，虽然我得承认他们的速度是最快的，但是在这个需求多变的世界中，需求的改变时时刻刻都在发生，当然如果你的产品经理人不错的话，他可能会提前给你确定好大部分的需求，这样你改动的时候可能会少一点。可惜天不遂人愿，他们大多被叫做产品狗，意思你自己体会去吧。这样你如果用原生写出来的项目，只要有一点点的变动，你可以自己试试，看看会不会把你整的喊爸爸。
这样，为了我们自己的身体健康，我们就需要有一种高度封装的代码，耦合性极低，大家谁都不影响谁，你让我改动这一块，我就仅仅需要动这一块就好了。而且你想用我这一个功能，随便用，你只要按照我给你的那个属性直接用就行！谁让我们牛逼了。看到这儿，你是不是对这个神奇的东西有了很大的期待啊？没错，这个神奇的东西就是我们上面说的面向对象的思想。相信我，当你真正掌握了面向对象的思想，你就会感受到人间自有真情在。

 - 上面大体的说了一下面向对象的好处，现在我们就来学习一下吧！这个时候就应该学学PHP的进阶内容了，关于PHP的面向对象编程，我们需要了解命名空间，类，继承，接口，类自动加载等等（PHP面向对象编程）。这个面向对象的思想是最难转化的，可能你已经习惯了面向过程编程，感觉逻辑就是应该按照你的思路来走，刚刚上手面向对象编程，你可能会觉得很变扭。但是，相信我，在前期你可能需要强迫一下自己，当你真正熟悉了oop之后你可能就再也离不开他了。

 - 上面说完了PHP的面向对象编程，那么我们就该思考一个问题了。我的逻辑编码已经有那么一点点登堂入室的感觉了，但是发现在连接数据库的时候还是使用的是原来的连接方式感觉好变扭啊，而且万一哪天我心情不好，想换个数据库玩玩，那我还得把这段连接代码删除，找到专门连接其他数据库的连接方式。有没有一些一劳永逸的方法呢？别担心，已经有大神为我们解决了。下面我们就说说进阶的第二个话题-数据库。在这里我介绍两个oop方式的数据库扩展（PDO，mysqli）。PDO已经实现了通过对象封装让我们用一段代码可以随意切换数据库，做到了想换就换，心随我动。而mysqli是MySQL的进阶版本，现在官方推荐的是这个。（PDO，mysqli）

 - 当然这是说的我们后端的进阶，那么可能有的同学就说了，写前端的JavaScript也好费劲，调用一个简单的id就需要写那么一长串代码，好费劲啊！别担心，这就是我要给你们介绍的JavaScript的进阶jQuery，他对原生的dom进行了封装，让你用更少的代码来完成更多的事儿，同时他又是看着那么简洁，优雅。毕竟我们可是高贵的程序猿，可不是民工。追求的是艺术和科技的结合。（jQuery）

第二阶段是改变你的思维方式，让你换个思路去看世界。思想变过来了，我们不妨用我们这一阶段学到的东西，来吧你的之前做的留言本，全都换成面向对象编程。这样你可能就感受到它的魅力了。

### 第三阶段

当你完成了上面两个阶段，如果你是一步一个脚印的来走的话。我相信的摩天大楼就在你的眼前。那还等什么，赶快建起高楼，走上人生巅峰，迎娶白富美吧！但是，要是我们还是像之前那样打地基一步一个脚印的去盖的话，那这摩天大楼何时才能完工呢？这个时候我们就需要站在巨人的肩膀上来实现了。我们只需要把摩天大楼装修的漂漂亮亮的就好，至于搭建脚手架这种事让巨人去帮你做吧。所以第三阶段我们就需要学习如何使用框架了。毕竟前人栽树后人乘凉，我们只需要拿来用就好。这里我介绍几个当前PHP主流的框架，也是我经常使用的这几个（Laravel，Yii，Thinkphp）。
 - Laravel是以PHP最优雅的框架来著称的，它运用了很多先进的思想，优雅的设计。在你使用它的时候你会感觉你在打造的是一个艺术品。不过又有点就会有缺点，因为他先进的思想，优雅的设计导致他相比较其他框架来说反应有点慢，毕竟贵族永远都是那么慢条斯理。
 
 - Yii就想一个朝气蓬勃的青年，他快捷，高效，安全，当你使用它的时候你会感觉非常顺手。
 
 - Thinkphp是国内的一个框架，他是我认识的第一个框架，他非常的简洁，给了你极大地便利，当你想要使用它的时候，你可以把它捡起来，不需要的话，随手扔掉就好。但是他有一个我不能忍受的缺点就是他有一些函数的命名仅仅使用一个字母来命名，虽然简洁，就我本身而言我感觉极其不友好。
 上面就是我介绍的几个框架，俗话说：一法通百法通，当你能深刻的理解一个框架的时候，在上手其他框架的时候，仅仅是表达方式上的不同。
 
 下面我们介绍几个前端框架，让我们写界面也能写的更加优雅：（bootstrap，Vue，angular.js）
 
 - bootstrap这个框架可以说是后端程序员的福音，对于一个讨厌写界面，而且写出的界面毫无美感的你来说。bootstrap里面的栅格系统，会让你只关心你的逻辑实现，至于界面的话很简单的就能搭建出一个简洁优雅的界面来。
 
 - Vue 这可以说是一个跟得上潮流的框架，它的MVVM模式，数据绑定的思想都可以让你更加方便的来调用后台数据，而且他及其小巧，更加方便你的定制。现在好多公司都在在它的基础上来搭建内部脚手架。所以学习他，绝对是一个不错的投资。
 
 - angular.js 相信程序猿没有听过Google的应该很少吧。没错他就是Google开源出来的一个框架，相信质量是一定有保障的。而且他火热的社区氛围，也保障了它的生命力。他也用了MVC的模式，可以实现双向数据绑定。这么多的优点，难道你就不心动么？
 
 
 ### 第四阶段
 
 对于已经走完以上几个阶段的人最容易出现的问题就是PHP好简单啊！PHP在手，天下我有的感觉。感觉再也没有了当年学习的热情，尤其是你还做过一些零零散散的项目，更是觉得在PHP上有更大的进步空间。我当年也是这样，感觉谁都很菜，自以为已经深谙PHP之道了。有这种感觉很正常，毕竟PHP非常简单，甚至最难的数据结构都已经有大神给你封装成函数，随便掉用即可。但是PHP简单，可是web开发可是博大精深啊。在这个阶段，你就需要往更深层次来走了，虽然还没达到研究PHP内部实现的程度，但是下面我说的这些知识已经够你专研一阵子了。
 
  - 首先从上个阶段你对框架的运用，你已经理解到MVC模式的思想了么？这个时候就是需要你去了解的了。（MVC）
  
  - 看着大神给你搭好的脚手架，你现在光是会用，难道对他们神奇的封装一点都不好奇么？为什么这样调用，你就能实现你想要的功能？所以是时候自己尽自己最大的努力搭建一个你自己的脚手架了，即使你自己将来不用，但是如果你自己写一遍的话，你就能对框架的宏观搭建有一个更深的了解。（搭建自己的框架）
  
  - 同样的话对前端框架也是有用的，当然如果你是主攻后端的话，我的建议是那你只要简单了解一下内部思想就好了。毕竟编程编的是思想，所不定他的思想是对你有用的，那么你可能就会搭建出一个更好的框架，变成传说中的大神。
  
  - 你在第三阶段的时候有没有感觉，有时候你解决某个逻辑的时候想到了一个特别好的解决方法，为此你还高兴不已。但是我要告诉你，在此之前可能对于一个资深工程师来说这就是一个简单的设计模式，已经被用了好多年。所以这个阶段我推荐你去看一下设计模式的书，在之前大神们已经给出了23中设计模式。他们都是思想的精华，值得你仔细研读。（设计模式）
  
  - 还有你之前可能只是简单的传值，但是你却不知道他们内部是怎么做到的，也有可能你知道，但是却不是很清楚。所以在这个阶段我推荐你看看HTTP协议，TCP/IP原理，Apache服务器内部配置，Auth协议。这些已经涉及到了一些内部原理，他可能枯燥无味，但是这些知识绝对是你成神路上必不可少的东西。（HTTP，TCP/IP，Apache，Auth协议）
  
  
 达到上面这些程度的，可以说你已经很厉害了，带领一个小团队基本不成问题。但是如果我想成为业内的大神该怎么办呢？这个时候你就需要往更深的程度发展了，比如说服务器，PHP原理什么的，因为我自己也在摸索，所以对于更高的程度也。。。。。



## 官方文档

- [PHP手册](http://u.720life.cn/g/7f82165747542a5b8ecd7c5c7645dc9ae4ddb337c7b74a2e9e70fb4973e73c12c566d044d4107bec0df4561f6fab3b1a) 
- [JavaScript 参考文档](http://u.720life.cn/g/a69e8f5dba5b4106ccc3875c547b1484a6bf67fa438ba2a919d3804020328d146404367ebf08fca646b6d498f227e07316daade82fed39d71cd0ddaeb0a2e5aacb27e80f91cb86b17dd4c7b0773e03c6) 
- [HTML教程](http://u.720life.cn/g/cab8351abd4235975d753f18e4a6c5716f2fdf0dd245b705146c0fdf053d1a788b528ecf705a597bd6eab5771060eea4) 
- [css3教程](http://u.720life.cn/g/099f51a56d4403ecef9788827bcd5cee7faabbc2b0b91c79fc1c43d5c797bb0d) 
- [css教程](http://u.720life.cn/g/099f51a56d4403ecef9788827bcd5cee695abf99397decc502d93af3b55daa65) 
- [mysql教程](http://u.720life.cn/g/78acf0dff7caf4ea5341ce0f0c4833e466b3d1e3b6fe1a6dfde462136eb1d8cb94a0a75cd39462285508e880a6eff0ce) 
- [MySQL PDO教程](http://u.720life.cn/g/78acf0dff7caf4ea5341ce0f0c4833e4553229e089840fad676400a1b2185297cd04fc91626c01f16ff952be02d244c8) 
- [MySQLi 函数](http://u.720life.cn/g/099f51a56d4403ecef9788827bcd5cee1936eef0c2dcc7b77a0d5aa1a4ab2b5a70b8cf3c73692cfac87a635ccb426264cea49a99090c20ca16b7818b477c304f) 
- [jQuery API 中文文档](http://u.720life.cn/g/6fe71836240acef38e3c647f9ec46b1afe20b79fafb55c378bb29644cca58ea3) 
- [Vue.js教程](http://u.720life.cn/g/1c3db3fec6433a3fb191bb48af91f3bbfb63bda838a789d43b99de7e588c09b6) 
- [AngularJS](http://u.720life.cn/g/24a67d6669a3cb44a74b6274d840b9c629219d7ebf2a2fdb3e157a63286022ca) 
- [Yii文档](http://u.720life.cn/g/fe8a38bb73e3e7f08cb5ef55b3e59247374c73a6da8ab43ed6b956d9087fcba3) 
- [Laravel5.1教程](http://u.720life.cn/g/96ac050cd485599f1c17cee16e38fe3e657d828a2c8e8980edfdc591515533cb893d26233ebde88e9ce15a11280d9c7e) 
- [ThinkPhp手册](http://u.720life.cn/g/878e0df3d929ca76f397cbe4f760e1b0e5bfd5933e69fe8d69d2beab041b594a) 

## 社区
- [StackOverflow](http://u.720life.cn/g/ddb1c8aa997182cb1a4af16f7df3945225291d6bf6ed809a575b730d6a89356e) 
- [SegmentFault](http://u.720life.cn/g/6900aa436d7855810ebad430307e6f919f14b8af37b8d4136375f90a9f99268b) 
- [github](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046d45c0ae7090bb1b2bd83912ab32555db) 
- [Yii](http://u.720life.cn/g/fe8a38bb73e3e7f08cb5ef55b3e5924790265e85dab2301e8500e2625e7dd21e) 
- [Vue中文社区](http://u.720life.cn/g/77af731258e86b31d1f927be97262b9325294432b384edaf438998ef9cd1977f) 
- [angular中文社区](http://u.720life.cn/g/7d2480f31c1c571bde369789c1658392830f185c4c1c089f69f7b12f7742a5ed) 
- [bootstrap](http://u.720life.cn/g/5dc63d04a35b84846e193be705862c773cff2a22a6b2940498e28eb01e58b4bd) 
- [Laravel社区](http://u.720life.cn/g/ff3399089b3832085c090d6930f1cbc6ff63c806e394ff21adab935e132f090a) 



## 工具
- [PHPstorm](http://u.720life.cn/g/a27ddb2b79548d3a829f3f0224b2480d1d457c9c34deab202304a32c462b597790d76272ba0b1ed8191382f48a373a63) 
- [Sublime](http://u.720life.cn/g/d074782214cd124a4d254dfb12494f9f1edb730f2b6144bdb20533f4543ce9d5) 
- [Notepad++](http://u.720life.cn/g/f08efd16883fe42d486befb954ceb20f36e79bb9b46167002562a3d6b4f0dbf6289a12336c35fe936c02e4027cc00f00b9fa5d58196ef7f699d7cfda2881dc68) 
- [SQLyog](http://u.720life.cn/g/985247d2fd6afba0b883f0e07a8f366e9d29d009354d9537dc940ae5dfcb935648dfa175caf373c69632c32bcf3214f5) 
- [centos 6.5 nginx安装与配置](http://u.720life.cn/g/4e20e720fe373c1a62f69fb6778bcfe31a7ca542a7a9920f536b2ff27a3656094545bf166c21d64088b0829efd13d416f62fb27f0eaebb2850363966337a9f90) 
- [CentOS上使用yum安装Apache](http://u.720life.cn/g/211b4c50bfd79a9a1b9c5e5a04ba2aa1c42a20e5a894bd154cf7f4f063b6180951a36f4d8aaa615a68f7a0cd3f26af2c15c4c053d25f3c88479c14c3c57b8ed4)  
- [CentOS6.4下Mysql数据库的安装与配置](http://u.720life.cn/g/94c1d8931f8bedcd3eeaf8cdeb6a662f0b898ec4d92f96f4a75b9060af8554152eed7062f1465c8843617fc7ea9cd68787881f4f4560add2e62989c89f95b078d1036c02d7eab4146a0531a161ec5958) 
- [Composer](http://u.720life.cn/g/d71b72c612d063f04d6d3ffd67aa07f721c48fc801fbec611bcb43e52ad3c076) 
- [npm中文文档](http://u.720life.cn/g/9185627ab456ba51671e9db9f8e0ece0660cdb0d34dc5dee63ed5ca3f22ae828b69342994e7950e86ccdb311110ef78f3fe33a902ce067b823080aed53662da4) 


## 书籍

- [Bootstrap用户手册：设计响应式网站](http://u.720life.cn/g/a109a0615ed740cf52cdd9f7a4793a418ff44834a5940249906c62d134503891) 
- [PHP-Debug-Manual-public](http://u.720life.cn/g/a109a0615ed740cf52cdd9f7a4793a413765fd24cbc06eec7123c66ab3500a02) 
- [Computer Science Made Simple Learn How Hardware And Software Work](http://u.720life.cn/g/a109a0615ed740cf52cdd9f7a4793a41416435dced6a40aa2abc1565999f4dd8) 
- [大话设计模式](http://u.720life.cn/g/a109a0615ed740cf52cdd9f7a4793a416a1ff048819546da245958087bd79422) 
- [yii2forbeginners](http://u.720life.cn/g/a109a0615ed740cf52cdd9f7a4793a41b9edc9f407482d3a73c9965ade659b2b) 
- [HTTP权威指南](http://u.720life.cn/g/a109a0615ed740cf52cdd9f7a4793a415036fd0511526778a9a964a73c98c9e7) 
- [TCP/IP三卷经典](http://u.720life.cn/g/a109a0615ed740cf52cdd9f7a4793a41284a75061d558eadc115ce446d4e4d22) 

## 视频教程

下面这些视频是我在学习过程中看过的，感觉讲的比较清晰的，根据学习的难易程度依次往下排序的：

### 第一阶段

1. [HTML视频](http://u.720life.cn/g/a109a0615ed740cf52cdd9f7a4793a418513aa4c73658a96eb00bb68cdc099de) 
2. [CSS视频](http://u.720life.cn/g/a109a0615ed740cf52cdd9f7a4793a4130ce812bbd65ce5c0909fe5241746991) 
3. [JavaScript视频](http://u.720life.cn/g/a109a0615ed740cf52cdd9f7a4793a41b8450bf298657fcab8128f8f7fdee86f) 
4. [php快速入门](http://u.720life.cn/g/d47e402704915d3bea7686bcd5bdba934c7745c7c540d38169ca9c9e005c9d02c8bc9aacabe87dca269d052cccaaf908)  提取码: yraj
5. ~~[php基础巩固]http://pan.baidu.com/s/1pLnm4Wj)视频太老了 不适合现在学习了  可以看书或者之有合适的再分享出来~~  
6. ~~[PHP深入理解]http://pan.baidu.com/s/1dEFaXkH)视频太老了 不适合现在学习了  可以看书或者之有合适的再分享出来~~  
7. [Linux入门](http://u.720life.cn/g/a109a0615ed740cf52cdd9f7a4793a41340d99585ef2b1708d1156ae3e106f73) 
8. [MySQL入门](http://u.720life.cn/g/a109a0615ed740cf52cdd9f7a4793a41a9da0845ec69bbd0d0fe368f652ace01) 
9. [Apache简介](http://u.720life.cn/g/a109a0615ed740cf52cdd9f7a4793a41e164b532fa3ea2651b4129dae8ea0ff8) 
10. [LAMP经典入门](http://u.720life.cn/g/a109a0615ed740cf52cdd9f7a4793a41a5c0496e040b4fdbc0208b688d352027) 

### 第二阶段

1. [PDO详解](http://u.720life.cn/g/a109a0615ed740cf52cdd9f7a4793a413915e323ac9afdb3b23357ee44a8e675) 
2. [jQuery](http://u.720life.cn/g/a109a0615ed740cf52cdd9f7a4793a4108a0766b7f2a3566a4ef8c4fa0b63dc8) 
3. [HTML5视频](http://u.720life.cn/g/a109a0615ed740cf52cdd9f7a4793a419b9a442d9731c27e68d536979ce38b4e) 
4. [CSS3视频](http://u.720life.cn/g/a109a0615ed740cf52cdd9f7a4793a415bf2be1d3fea5ac286f8e834f1760cfd) 
5. [php面向对象编程](http://u.720life.cn/g/9bdca284b716378ad8944a645c76d018c3bc5f078889939dcdbf6fff6c2e42c4) 

### 第三阶段

这一部分的框架学习，我感觉直接进入实战，然后结合官方文档效果比较好，相反要是结合一些基础视频反而显得有点儿啰嗦！适合自己就好。（这一部分视频是我从网上收集来的，可能会涉及到侵权问题导致分享失败，如果特别需要可以加我微信之后和我说一下-zzc960316）

1. [zend framework](http://u.720life.cn/g/a109a0615ed740cf52cdd9f7a4793a416eeb864771ace04c6185b11587f9cc2b) 
2. [Yii2.0全力出击打造完整电商平台](http://u.720life.cn/g/a109a0615ed740cf52cdd9f7a4793a4193c18e81d2e7a2c285f2900f46cc2d54) 
3. [前端到后台ThinkPHP开发整站](http://u.720life.cn/g/a109a0615ed740cf52cdd9f7a4793a41b7a54abeff3546e9f317b5b11955357e) 
4. [知乎实战laravel](http://u.720life.cn/g/a109a0615ed740cf52cdd9f7a4793a412e2c5834191b58a7591e457cbea6b3f1) 
5. [6小时jQuery开发小应用无密码](http://u.720life.cn/g/a109a0615ed740cf52cdd9f7a4793a41f143b1949f8406b03395d0d0d64606af) 
6. [vue实战](http://u.720life.cn/g/a109a0615ed740cf52cdd9f7a4793a419428f44e97f6648b3e4c0ea9a3f6a79f) 
7. [从零开始打造自己的PHP框架](http://u.720life.cn/g/9bdca284b716378ad8944a645c76d018f6c0c2759a12a5f7cd73ed3eca68e246) 

### 第四阶段

我感觉这一阶段更适合读书，读一些讲解原理的书，而且也没有什么太好的视频。
1. [OAuth2.0协议](http://u.720life.cn/g/9bdca284b716378ad8944a645c76d0186363fb75a3fa47bd4ee41e566381747a) 
2. [mysql优化](http://u.720life.cn/g/a109a0615ed740cf52cdd9f7a4793a412b868ae6846169587ff4d91e64141129) 
3. [数据结构与算法1](http://u.720life.cn/g/a109a0615ed740cf52cdd9f7a4793a41a393fe326f0702b6c3cb8b9e7205a61a) 
4. [数据结构与算法2](http://u.720life.cn/g/a109a0615ed740cf52cdd9f7a4793a419201cd190177eeb17492e5af7519a963) 


## 学习网站
1. [慕课网](http://u.720life.cn/g/9bdca284b716378ad8944a645c76d0180d8602b12b2f70c405e7f27244946df375801473ccc161bb4d1ab930a1e0f698)    可以让你及时了解最新的技术，也有一些小的知识点讲解的非常不错。
2. [计蒜客](http://u.720life.cn/g/e714b52ef63b4ff68d18b6cc70a72e624c5e17935560d4738819910d1eb41216)    这里的课程大多数是cs，偏向理论，非常不错，但是收费。
3. [实验楼](http://u.720life.cn/g/5548c6c8eb0c0de8c16249cde4dfa3ef3211b4f1520bb10cc4456f5a84259688)    你可以在这里及时编码，知识讲的也不错，可以来看看。

## 博客

博客这个会随时更新，遇到比较好的就会放上来。

1. [张智超的博客](http://u.720life.cn/g/5997fd1f539dfbe7c9c67736234755a458c09bb17ede07ab68b407c9b87cf93d) 
2. [刘伟技术博客](http://u.720life.cn/g/5997fd1f539dfbe7c9c67736234755a4299cbe5699cafbdaf1cb8942e625a2ca8f655b7c54c900d660f1e8cac05af0221e0409f50340dda849465d87592251d5)  这个设计模式讲的不错
3. [鸟哥的博客](http://u.720life.cn/g/5bb3e5989797a86a9bec41dfc8c807872155131a1519ae4fc318d9994772add3)   这是大神的博客，值得关注
4. [张宴de博客](http://u.720life.cn/g/99f809f30eb46cca2e0b5e940cdcbc0dd8d9c00e5a761d18cefd7ce666b8b52c) 

## 知识图谱

我会添加一些比较好的知识图谱，持续更新。。。

 - [php开发图谱]http://lib.csdn.net/qq_28832135/chart/php开发  这是我在CSDN创建的一个知识图谱，因为受邀知识库的特邀编辑，我每天会审核一些PHP的博文，如果比较好的话，在我审核后，我会顺手加到我的个人图谱中，有兴趣的可以关注一下。










 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)